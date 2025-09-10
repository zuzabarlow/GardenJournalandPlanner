Garden Journal & Planner — Product Spec

1) Product vision
Help home gardeners plan, record, and learn from their gardens by combining a visual garden map, a structured plant catalog, and a simple activity journal (with photos). MVP works offline and stores data locally, with optional export/import.
2) Core modules (MVP)
Cataloging
Create and manage a catalog of plants and seed packets: name, variety, brand, seed vs seedling, days to maturity, notes.
Planning (Garden Map)
Draw or lay out garden areas (beds, pots, planter boxes). Place plant markers with labels on a map; mark orientation (north/south) and optional sun/wind exposure.
Journaling
Log observations per plant (dates, notes, actions like watering/feeding/spraying oil), attach photos, and view a timeline per plant.
3) Target users & scenarios
Home gardener with a small yard or balcony who wants to remember what was planted where and how it performed.
Key scenarios
Add a new seed packet to the catalog and plan where to sow it.
Place a marker for a plant in the garden map and label it.
Capture an observation with a photo and date (e.g., “Fed tomatoes”, “First flowers”, “Pest noticed”).
Review plant history before replanting next season.
4) Detailed feature specs (MVP)
4.1 Cataloging
User stories
As a user, I can add plants to a catalog with name, variety, brand, and type (seed or seedling) so I can reuse them when planning.
As a user, I can add seed packet details so I can track lot, best-by date, and remaining quantity.
Data fields
PlantCatalogItem:
id (uuid)
common_name (string, required)
scientific_name (string, optional)
variety (string)
brand (string)
category (enum: vegetable/fruit/herb/flower/other)
type (enum: seed/seedling)
days_to_maturity (int, optional)
frost_sensitive (bool, default false)
notes (string)
SeedPacket:
id (uuid)
catalog_item_id (fk -> PlantCatalogItem.id)
lot_code (string)
packed_on (date, optional)
best_by (date, optional)
quantity (string, e.g., “50 seeds”)
source (string: store/online/saved)
Acceptance criteria
Can create, edit, and delete catalog items and seed packets.
Catalog items list view with search/filter by name, category, brand, type.

4.2 Planning (Garden Map)
User stories
As a user, I can create my garden layout and mark orientation (north).
As a user, I can add one or more areas (beds, pots, planters) with shape and size.
As a user, I can place plant markers within areas and label them with catalog items.
As a user, I can capture per-area attributes like soil type and general sun exposure.
Map features (MVP)
Canvas with simple tools: Add Area (rectangle or circle), Add Marker (pin), Select/Move/Delete.
Orientation indicator (N arrow). Optional background image upload (photo of garden) with scale toggle.
Marker label shows common_name (+ variety if present). Tap to open plant details & journal.
Data fields
Garden:
id (uuid), name (string), address (optional), units (enum: metric/imperial)
orientation_deg (number, default 0 = north up)
Area (bed/plot/pot):
id (uuid), garden_id (fk)
name (string)
type (enum: bed/pot/planter/other)
shape (enum: rect/circle/poly)
geometry (object: coords in canvas space)
soil_type (enum: clay/loam/sandy/mixed/other)
sun_exposure (enum: full_sun/partial_shade/shade/unknown)
wind_exposure (enum: low/medium/high/unknown)
Planting (a placed plant):
id (uuid), area_id (fk), catalog_item_id (fk)
label (string, default from catalog)
method (enum: direct_sow/transplant)
date_sown (date, optional)
date_transplanted (date, optional)
position (x,y in canvas space)
spacing_cm (number, optional)
Acceptance criteria
Create a garden, add at least one area, place at least one plant marker linked to a catalog item.
Reposition markers via drag; delete and re-add without data loss in catalog.
Persist layout locally and reload without loss.

4.3 Journaling
User stories
As a user, I can log dated entries per planting: watering, feeding, pruning, pest/disease, germination, flowering, harvest, general notes.
As a user, I can add one or more photos to an entry.
As a user, I can filter the journal by plant or by action type.
Data fields
Observation:
id (uuid), planting_id (fk)
date (dateTime, required)
event_type (enum: note/water/feed/prune/pest/disease/germination/transplant/flower/harvest/frost/other)
amount (string, optional: e.g., “1L”, “2 scoops”)
product_name (string, optional: fertilizer/food name)
text (string, optional)
Photo:
id (uuid)
planting_id (fk) or area_id (fk)
file_uri (string), taken_at (dateTime), caption (string)
exif (object, optional)
Acceptance criteria
Create, edit, delete entries; attach and view photos (thumbnail + full view).
Timeline view per planting ordered by date.

5) Cross-cutting features
Search & filters: by plant name, variety, brand, category, action type, season/year.
Export/Import: JSON (all data) and CSV (catalog, plantings, observations); photos exported in a folder with references in JSON.
Units & locale: metric by default; configurable in Settings.
Orientation & exposure: Store garden orientation and optional exposure notes on areas/plantings for future features (sun-path analysis).

6) Non-functional requirements (MVP)
Offline-first: All reads/writes work without internet. Use local storage (e.g., IndexedDB).
Performance: <150ms perceived response for common actions on devices from the last 5 years.
Privacy: All data remains on device by default. No third-party analytics in MVP.
Accessibility: Keyboard navigable; text alternatives for photos; color-contrast compliant.

7) Data model (JSON schema sketches)
{
"Garden": {"id":"uuid","name":"string","address":"string?","units":"metric|imperial","orientation_deg":0},
"Area": {"id":"uuid","garden_id":"uuid","name":"string","type":"bed|pot|planter|other","shape":"rect|circle|poly","geometry":{},"soil_type":"clay|loam|sandy|mixed|other","sun_exposure":"full_sun|partial_shade|shade|unknown","wind_exposure":"low|medium|high|unknown"},
"PlantCatalogItem": {"id":"uuid","common_name":"string","scientific_name":"string?","variety":"string?","brand":"string?","category":"vegetable|fruit|herb|flower|other","type":"seed|seedling","days_to_maturity":90,"frost_sensitive":false,"notes":"string?"},
"SeedPacket": {"id":"uuid","catalog_item_id":"uuid","lot_code":"string?","packed_on":"date?","best_by":"date?","quantity":"string?","source":"string?"},
"Planting": {"id":"uuid","area_id":"uuid","catalog_item_id":"uuid","label":"string","method":"direct_sow|transplant","date_sown":"date?","date_transplanted":"date?","position":{"x":0,"y":0},"spacing_cm":30},
"Observation": {"id":"uuid","planting_id":"uuid","date":"dateTime","event_type":"note|water|feed|prune|pest|disease|germination|transplant|flower|harvest|frost|other","amount":"string?","product_name":"string?","text":"string?"},
"Photo": {"id":"uuid","planting_id":"uuid?","area_id":"uuid?","file_uri":"string","taken_at":"dateTime?","caption":"string?","exif":{}}
}

8) UX & screens (MVP)
Home: Tabs for Catalog, Map, Journal.
Catalog: list + search; add/edit catalog item; link to seed packets.
Map: canvas (toolbar: Select | Add Area | Add Marker | Delete); panel with area/planting properties; north arrow toggle; optional background image upload.
Plant detail: summary from catalog, placement(s) list, “Add observation”.
Journal: reverse-chronological feed; filters; quick-add actions (Water, Feed, Note, Photo).
Photo viewer: grid of thumbnails; full-screen lightbox.
Settings: units, export/import, backup/restore.

9) Technical approach (suggested)
Platform: Web app (PWA-capable). Works on desktop and mobile browsers.
State & storage: IndexedDB (e.g., Dexie) for structured data; File System Access API or browser-managed blobs for photos.
Map canvas: HTML5 Canvas or SVG. Start with SVG for easier hit-testing and scaling.
Media: Client-side image compression for photos; store original URI + generated thumbnails.
ID generation: UUID v4.
Note: If implementing a desktop app later, reuse the same JSON model and sync via a local file.

10) Acceptance tests (MVP)
Create 1 garden, 2 areas, and 3 catalog items; place 3 markers and reload the app — data persists.
Add an observation with 2 photos to one plant; view it in Journal and in Plant detail.
Export full dataset; clear storage; import JSON; all entities and photo links are restored.
Use the app with network disabled — all CRUD actions still work.

11) Release plan
v0.1 (MVP): Catalog, Map with areas/markers, Journal with photos, Export/Import, Offline-first.
v0.2: Calendar view (derived from observations), reminders (local notifications), quick templates (e.g., Water/Feed with default amounts).
v0.3 (Stretch): Weather hints, sun path overlay (manual orientation), season summaries, basic analytics (germination/harvest rates), CSV import for catalog.

12) Stretch ideas (post‑MVP)
Weather integration for planning weekends and frost alerts.
Sun exposure estimation from manual inputs; seasonal sunlight notes per area.
Companion planting tips (local rules, no ML required initially).
Multi-garden support (home + community plot).
Role-based sharing (read-only link for friends/neighbors).

13) Open questions (for Zuzanna)
Is offline-first a must-have for v0.1?
Do you want single-garden or multi-garden support in MVP?
For the map, should we allow a photo upload as a background (scaled) or keep it as simple shapes only in MVP?
How granular should soil and sun/wind exposure be — simple enums (as above) or free text?
Should reminders/notifications be included in v0.1 or v0.2?
Any specific export formats besides JSON/CSV you want (e.g., printable PDF map)?
Photos: store on device only or allow optional cloud backup later?
Do you need calendar and derived tasks (e.g., “repot in 2 weeks”) in MVP?

14) Glossary
Area: A bed/plot/pot defined on the map.
Planting: A placed instance of a plant (from the Catalog) within an Area.
Observation: A dated journal entry tied to a Planting (optionally with photos).
Seed Packet: A container of seeds associated with a catalog item.
Done! I’ve sorted your ideas into a clean, developer-ready spec and popped it on the canvas as “Garden Journal & Planner — Product Spec v0.1.” It covers MVP features, data model (JSON sketches), UX/screens, acceptance tests, and a short release plan so you can start coding right away in Claude.
A few quick decisions so I can tighten it further:
Offline-first: must-have for v0.1, or okay for v0.2?


Single garden vs multi-garden in MVP?


Garden map: allow background photo upload (scaled) in MVP, or stick to simple shapes first?


Soil/sun/wind: keep as simple enums (full sun/partial/shade etc.) or allow free text too?


Reminders/notifications (e.g., “feed in 2 weeks”): v0.1 or v0.2?


Exports: JSON + CSV enough, or do you want a printable PDF map/journal?


Photos: store on device only for now, or plan optional cloud backup later?


Any must-track actions beyond water/feed/prune/pest/disease/germination/flower/harvest?


Tell me your preferences and I’ll update the spec.

