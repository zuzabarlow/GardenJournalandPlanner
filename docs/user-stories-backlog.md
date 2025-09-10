# Product Backlog - User Stories

## Epic: Cataloging System

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| CAT-001 | As a gardener, I want to add plants to my catalog so I can reuse them when planning | 5 | • Form with all fields<br>• Validation for required fields<br>• Success confirmation<br>• Data persists |
| CAT-002 | As a gardener, I want to edit plant details so I can correct mistakes or add information | 3 | • Pre-filled edit form<br>• Save changes<br>• Cancel option<br>• Update confirmation |
| CAT-003 | As a gardener, I want to delete plants from my catalog so I can remove ones I no longer grow | 2 | • Delete confirmation<br>• Cascade handling<br>• Undo option<br>• List updates |
| CAT-004 | As a gardener, I want to search plants by name so I can quickly find specific varieties | 3 | • Search bar<br>• Real-time results<br>• Case insensitive<br>• Partial matching |
| CAT-005 | As a gardener, I want to filter plants by category so I can see only vegetables or flowers | 5 | • Category dropdown<br>• Multi-select<br>• Result count<br>• Clear filters |
| CAT-006 | As a gardener, I want to track seed packets so I know what seeds I have and their age | 5 | • Link to plant<br>• Lot/date fields<br>• Quantity tracking<br>• Source info |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| CAT-007 | As a gardener, I want to see seed packet expiry warnings so I use older seeds first | 3 | • Visual indicators<br>• Sort by date<br>• Alert threshold<br>• Bulk view |
| CAT-008 | As a gardener, I want to duplicate catalog entries so I can quickly add similar varieties | 2 | • Clone button<br>• Editable copy<br>• Name suffix<br>• Link option |
| CAT-009 | As a gardener, I want to mark plants as favorites so I can find my most-used ones quickly | 2 | • Star/favorite icon<br>• Filter favorites<br>• Sort option<br>• Toggle state |

---

## Epic: Garden Planning & Map

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| MAP-001 | As a gardener, I want to create my garden layout so I can plan where everything goes | 5 | • Name garden<br>• Set dimensions<br>• Choose units<br>• Set orientation |
| MAP-002 | As a gardener, I want to add garden beds to my map so I can organize planting areas | 8 | • Draw rectangles<br>• Draw circles<br>• Name areas<br>• Set properties |
| MAP-003 | As a gardener, I want to place plants on the map so I can track what's planted where | 5 | • Drag from catalog<br>• Position markers<br>• Show labels<br>• Link to data |
| MAP-004 | As a gardener, I want to move plants on the map so I can adjust my layout | 3 | • Select marker<br>• Drag to move<br>• Snap to grid<br>• Update position |
| MAP-005 | As a gardener, I want to record sun exposure for areas so I can plant appropriately | 3 | • Exposure options<br>• Visual indicators<br>• Area properties<br>• Save settings |
| MAP-006 | As a gardener, I want to see a north arrow so I know my garden's orientation | 2 | • Direction indicator<br>• Rotate option<br>• Always visible<br>• Adjustable |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| MAP-007 | As a gardener, I want to upload a background photo so my map matches reality | 3 | • Image upload<br>• Scale/position<br>• Opacity control<br>• Delete option |
| MAP-008 | As a gardener, I want to zoom and pan the map so I can see details or overview | 3 | • Pinch zoom<br>• Pan gesture<br>• Zoom controls<br>• Reset view |
| MAP-009 | As a gardener, I want to group plants together so I can manage companion plantings | 5 | • Multi-select<br>• Group creation<br>• Named groups<br>• Bulk actions |
| MAP-010 | As a gardener, I want to copy areas so I can quickly create similar beds | 2 | • Duplicate tool<br>• Position new<br>• Copy properties<br>• Rename copy |

---

## Epic: Journaling & Observations

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| JRN-001 | As a gardener, I want to log observations so I can track plant progress | 5 | • Date/time<br>• Event types<br>• Text notes<br>• Save entry |
| JRN-002 | As a gardener, I want to attach photos to observations so I can document visually | 8 | • Camera capture<br>• Gallery upload<br>• Multiple photos<br>• Thumbnails |
| JRN-003 | As a gardener, I want to see a timeline for each plant so I can review its history | 3 | • Chronological<br>• Event icons<br>• Expandable<br>• Photos inline |
| JRN-004 | As a gardener, I want to record watering so I can track irrigation frequency | 3 | • Quick action<br>• Amount field<br>• Date/time<br>• Repeat option |
| JRN-005 | As a gardener, I want to record feeding so I can track fertilizer applications | 3 | • Product name<br>• Amount used<br>• Application method<br>• Schedule |
| JRN-006 | As a gardener, I want to filter observations by type so I can see specific activities | 2 | • Type dropdown<br>• Multi-select<br>• Date range<br>• Clear filters |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| JRN-007 | As a gardener, I want quick-action buttons so I can log common tasks faster | 3 | • Water button<br>• Feed button<br>• Note button<br>• Photo button |
| JRN-008 | As a gardener, I want to bulk-log observations so I can update multiple plants at once | 5 | • Multi-select<br>• Same action<br>• Confirm dialog<br>• Success count |
| JRN-009 | As a gardener, I want to add captions to photos so I can remember details | 2 | • Text field<br>• Edit caption<br>• Show on hover<br>• Search captions |
| JRN-010 | As a gardener, I want to tag observations so I can categorize and find them | 3 | • Custom tags<br>• Auto-complete<br>• Tag filter<br>• Tag cloud |

---

## Epic: Data Management

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| DAT-001 | As a gardener, I want to export my data so I can backup or share it | 5 | • JSON export<br>• Include photos<br>• Download file<br>• Success message |
| DAT-002 | As a gardener, I want to import data so I can restore from backup | 5 | • File upload<br>• Validation<br>• Merge option<br>• Import report |
| DAT-003 | As a gardener, I want the app to work offline so I can use it in the garden | 8 | • Service worker<br>• Cache assets<br>• Queue sync<br>• Status indicator |
| DAT-004 | As a gardener, I want my data saved automatically so I don't lose work | 3 | • Auto-save<br>• Debounced<br>• Confirm save<br>• Recover drafts |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| DAT-005 | As a gardener, I want to export to CSV so I can use data in spreadsheets | 3 | • CSV format<br>• Column headers<br>• Download file<br>• Excel compatible |
| DAT-006 | As a gardener, I want to clear all data so I can start fresh | 2 | • Settings option<br>• Confirm dialog<br>• Progress bar<br>• Success message |
| DAT-007 | As a gardener, I want to see storage usage so I know how much space I'm using | 2 | • Storage meter<br>• By category<br>• Photo count<br>• Clear cache |

---

## Epic: User Interface & Experience

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| UI-001 | As a gardener, I want a mobile-friendly interface so I can use it on my phone | 5 | • Responsive<br>• Touch targets<br>• Readable text<br>• No scroll |
| UI-002 | As a gardener, I want clear navigation so I can find features easily | 3 | • Tab bar<br>• Icons + labels<br>• Active state<br>• Consistent |
| UI-003 | As a gardener, I want loading indicators so I know when actions are processing | 2 | • Spinners<br>• Progress bars<br>• Skeleton screens<br>• Feedback |
| UI-004 | As a gardener, I want error messages so I know when something goes wrong | 2 | • Clear text<br>• Recovery action<br>• Dismiss option<br>• Non-blocking |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| UI-005 | As a gardener, I want a dark mode so I can use the app at night | 3 | • Theme toggle<br>• System match<br>• Persist choice<br>• All screens |
| UI-006 | As a gardener, I want keyboard shortcuts so I can work faster on desktop | 3 | • Common actions<br>• Visible hints<br>• Customizable<br>• Help sheet |
| UI-007 | As a gardener, I want undo/redo so I can reverse mistakes | 5 | • Action history<br>• Undo button<br>• Redo button<br>• Limit stack |
| UI-008 | As a gardener, I want tooltips so I can understand features | 2 | • Hover help<br>• Touch help<br>• Dismiss option<br>• First-time |

---

## Epic: Settings & Configuration

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| SET-001 | As a gardener, I want to choose units so I can use metric or imperial | 2 | • Toggle switch<br>• Convert values<br>• Persist choice<br>• Apply globally |
| SET-002 | As a gardener, I want to set my location so the app can provide local information | 3 | • Location field<br>• Map picker<br>• Zone detection<br>• Privacy option |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| SET-003 | As a gardener, I want to customize quick actions so I can access my most-used features | 3 | • Action list<br>• Drag order<br>• Toggle visible<br>• Reset default |
| SET-004 | As a gardener, I want to set default values so I don't repeat common entries | 2 | • Default soil<br>• Default sun<br>• Default category<br>• Save prefs |
| SET-005 | As a gardener, I want notification preferences so I control what alerts I get | 3 | • Toggle types<br>• Time windows<br>• Frequency<br>• Test button |

---

## Epic: Performance & Quality

### Must Have (P0)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| PRF-001 | As a gardener, I want fast page loads so I don't wait to use the app | 3 | • <3s initial<br>• <150ms navigate<br>• Smooth scroll<br>• No jank |
| PRF-002 | As a gardener, I want smooth interactions so the app feels responsive | 3 | • 60fps animations<br>• Touch response<br>• No lag<br>• Feedback |
| PRF-003 | As a gardener, I want the app to work on older devices so I can use my existing phone | 5 | • iOS 12+<br>• Android 8+<br>• 2GB RAM<br>• Graceful degradation |

### Should Have (P1)
| ID | Story | Points | Acceptance Criteria |
|----|-------|--------|-------------------|
| PRF-004 | As a gardener, I want efficient photo storage so I don't fill up my device | 5 | • Compression<br>• Thumbnails<br>• Lazy load<br>• Cache management |
| PRF-005 | As a gardener, I want battery-efficient operation so my phone lasts in the garden | 3 | • Minimize wake<br>• Batch operations<br>• Dark mode<br>• Reduce animations |

---

## Story Point Summary

### By Epic
- **Cataloging:** 35 points
- **Garden Map:** 43 points  
- **Journaling:** 44 points
- **Data Management:** 28 points
- **UI/UX:** 27 points
- **Settings:** 13 points
- **Performance:** 19 points

### By Priority
- **P0 (Must Have):** 124 points
- **P1 (Should Have):** 85 points
- **Total:** 209 points

### Sprint Allocation
- **Available:** 130 points (5 sprints)
- **MVP Scope:** 124 points (P0 only)
- **Buffer:** 6 points (5%)

---

## Backlog Prioritization Matrix

| Epic | Business Value | Technical Risk | User Impact | Priority |
|------|---------------|---------------|-------------|----------|
| Cataloging | High | Low | High | Sprint 2 |
| Garden Map | High | Medium | High | Sprint 3 |
| Journaling | High | Medium | High | Sprint 4 |
| Offline/Data | Medium | High | High | Sprint 1 |
| Export/Import | Medium | Low | Medium | Sprint 5 |
| UI/UX | Medium | Low | High | All Sprints |
| Performance | Low | Medium | High | Sprint 5 |