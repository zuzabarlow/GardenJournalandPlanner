# Garden Journal & Planner - Agile Project Plan

## Executive Summary
**Project:** Garden Journal & Planner MVP  
**Duration:** 10 weeks (5 sprints × 2 weeks)  
**Methodology:** Scrum with 2-week sprints  
**Team Size:** 3-4 developers + 1 PO/Designer  
**Target Release:** MVP v0.1  

---

## Team Structure

### Core Team
- **Product Owner** - Stakeholder representation, backlog prioritization
- **Scrum Master** (can be rotating) - Facilitate ceremonies, remove blockers
- **Full-Stack Developer (Lead)** - Architecture, core features
- **Frontend Developer** - UI/UX implementation, map canvas
- **Backend Developer** - Data layer, offline storage, sync
- **QA/Test Engineer** (part-time) - Test automation, acceptance testing

### Extended Team
- **UX Designer** (part-time) - Mockups, user flows
- **DevOps** (part-time) - CI/CD, deployment

---

## Sprint Plan Overview

### Sprint 0: Foundation (Week 0)
**Focus:** Setup and Planning
- Team onboarding
- Environment setup
- Architecture decisions
- Initial backlog grooming

### Sprint 1: Core Infrastructure (Weeks 1-2)
**Focus:** Technical foundation and data layer
- Database schema implementation
- Offline storage setup (IndexedDB/Dexie)
- Basic PWA shell
- CI/CD pipeline

### Sprint 2: Cataloging Module (Weeks 3-4)
**Focus:** Complete catalog functionality
- Plant catalog CRUD
- Seed packet management
- Search and filtering
- Basic UI components

### Sprint 3: Garden Map Core (Weeks 5-6)
**Focus:** Map visualization and areas
- SVG/Canvas implementation
- Garden and area creation
- Basic drawing tools
- Area properties management

### Sprint 4: Planting & Journaling (Weeks 7-8)
**Focus:** Plant placement and observations
- Plant marker placement
- Linking to catalog
- Observation creation
- Photo management basics

### Sprint 5: Polish & Release (Weeks 9-10)
**Focus:** Integration and MVP release
- Export/Import functionality
- UI polish and responsive design
- Bug fixes and performance
- Deployment preparation

---

## Detailed Sprint Breakdown

### Sprint 1: Core Infrastructure
**Sprint Goal:** Establish technical foundation with offline-first data layer

**User Stories:**
| Story | Points | Priority |
|-------|--------|----------|
| As a developer, I want a working development environment with hot reload | 3 | P0 |
| As a user, I want the app to work offline without any internet connection | 8 | P0 |
| As a developer, I want a robust data schema with migrations support | 5 | P0 |
| As a user, I want the app to load quickly on mobile and desktop | 3 | P0 |
| As a developer, I want automated tests running in CI/CD | 5 | P1 |
| As a user, I want a responsive navigation shell | 3 | P1 |

**Deliverables:**
- IndexedDB with Dexie.js configured
- PWA manifest and service worker
- Basic routing and navigation tabs
- Unit test framework
- CI/CD pipeline (GitHub Actions)

**Acceptance Criteria:**
- App loads offline after first visit
- Data persists between sessions
- Tests run automatically on commits
- Mobile responsive shell renders

---

### Sprint 2: Cataloging Module
**Sprint Goal:** Complete plant catalog with full CRUD operations

**User Stories:**
| Story | Points | Priority |
|-------|--------|----------|
| As a gardener, I want to add plants to my catalog with all details | 5 | P0 |
| As a gardener, I want to edit and delete catalog entries | 3 | P0 |
| As a gardener, I want to search plants by name | 3 | P0 |
| As a gardener, I want to filter plants by category and type | 5 | P0 |
| As a gardener, I want to track seed packets for each plant | 5 | P1 |
| As a gardener, I want to see a list of all my cataloged plants | 2 | P1 |
| As a gardener, I want to add photos to catalog items | 3 | P2 |

**Deliverables:**
- Catalog list view with grid/list toggle
- Add/Edit plant form with validation
- Search bar with instant results
- Filter dropdowns (category, type, brand)
- Seed packet management UI
- 10+ sample plants pre-loaded

**Acceptance Criteria:**
- Can create plant with all fields
- Search returns results < 100ms
- Filters work independently and combined
- Data validates before saving
- Seed packets link to plants correctly

---

### Sprint 3: Garden Map Core
**Sprint Goal:** Interactive garden map with area management

**User Stories:**
| Story | Points | Priority |
|-------|--------|----------|
| As a gardener, I want to create my garden layout with orientation | 5 | P0 |
| As a gardener, I want to add beds and containers to my garden | 8 | P0 |
| As a gardener, I want to draw rectangular and circular areas | 5 | P0 |
| As a gardener, I want to set soil type and sun exposure for areas | 3 | P0 |
| As a gardener, I want to move and resize areas on the map | 5 | P1 |
| As a gardener, I want to delete areas without losing plant data | 2 | P1 |
| As a gardener, I want to upload a background photo of my garden | 3 | P2 |

**Deliverables:**
- SVG-based garden canvas
- Drawing tools (rectangle, circle)
- Area properties panel
- Drag and drop for areas
- North orientation indicator
- Touch-friendly controls

**Acceptance Criteria:**
- Can create garden with 5+ areas
- Areas render correctly on mobile
- Properties save and persist
- Smooth pan/zoom on touch devices
- Areas selectable with visual feedback

---

### Sprint 4: Planting & Journaling
**Sprint Goal:** Connect plants to map and enable observation tracking

**User Stories:**
| Story | Points | Priority |
|-------|--------|----------|
| As a gardener, I want to place plants from my catalog onto the map | 5 | P0 |
| As a gardener, I want to log observations for each plant | 5 | P0 |
| As a gardener, I want to attach photos to my observations | 8 | P0 |
| As a gardener, I want to see a timeline of plant activities | 3 | P0 |
| As a gardener, I want to record watering and feeding amounts | 3 | P1 |
| As a gardener, I want to filter observations by type | 2 | P1 |
| As a gardener, I want quick-action buttons for common tasks | 3 | P2 |

**Deliverables:**
- Plant marker placement tool
- Observation form with event types
- Photo capture and upload
- Timeline view per plant
- Journal feed with filters
- Thumbnail generation for photos

**Acceptance Criteria:**
- Plants link correctly to catalog
- Photos compress to < 500KB
- Timeline shows newest first
- Can add 10+ observations per plant
- Photos display in lightbox

---

### Sprint 5: Polish & Release
**Sprint Goal:** Integration, polish, and MVP deployment

**User Stories:**
| Story | Points | Priority |
|-------|--------|----------|
| As a gardener, I want to export all my data as JSON backup | 5 | P0 |
| As a gardener, I want to import data from a backup file | 5 | P0 |
| As a gardener, I want the app to load in under 3 seconds | 3 | P0 |
| As a gardener, I want consistent UI across all screens | 5 | P0 |
| As a gardener, I want help documentation for features | 3 | P1 |
| As a gardener, I want to export plant lists as CSV | 3 | P1 |
| As a developer, I want the app deployed to production | 3 | P0 |

**Deliverables:**
- Export/Import functionality
- Performance optimizations
- UI consistency pass
- Bug fixes from testing
- Production deployment
- Basic documentation

**Acceptance Criteria:**
- Export includes all data and photos
- Import restores complete state
- Lighthouse score > 90
- No critical bugs
- Deployed to production URL

---

## Velocity & Capacity Planning

### Team Velocity
- **Sprint 1:** 27 points (establishing baseline)
- **Sprint 2-4:** 26-29 points (steady state)
- **Sprint 5:** 24 points (focus on quality)
- **Total:** ~130 story points

### Capacity Allocation
- **Development:** 70%
- **Testing:** 15%
- **Meetings/Ceremonies:** 10%
- **Buffer/Fixes:** 5%

---

## Definition of Done

### Story Level
- [ ] Code complete and peer reviewed
- [ ] Unit tests written and passing (>80% coverage)
- [ ] Integration tests for critical paths
- [ ] Responsive design verified (mobile/tablet/desktop)
- [ ] Offline functionality verified
- [ ] Accessibility checked (keyboard nav, screen reader)
- [ ] Documentation updated
- [ ] No console errors or warnings
- [ ] Performance budget met (<150ms interactions)

### Sprint Level
- [ ] All stories meet DoD
- [ ] Sprint goal achieved
- [ ] Demo prepared and delivered
- [ ] Retrospective completed
- [ ] Technical debt logged
- [ ] Next sprint planned

### Release Level
- [ ] All acceptance tests passing
- [ ] Performance benchmarks met
- [ ] Security review completed
- [ ] Deployment guide updated
- [ ] Release notes prepared
- [ ] Stakeholder sign-off

---

## Sprint Ceremonies

### Schedule (2-week sprints)
| Ceremony | Duration | When | Participants |
|----------|----------|------|--------------|
| Sprint Planning | 2 hours | Day 1 | Whole team |
| Daily Standup | 15 min | Daily | Whole team |
| Backlog Grooming | 1 hour | Week 1, Day 3 | PO + Leads |
| Sprint Review/Demo | 1 hour | Last day | Team + Stakeholders |
| Retrospective | 1 hour | Last day | Whole team |

### Meeting Formats

**Sprint Planning**
1. Review sprint goal
2. Review velocity and capacity
3. Select and estimate stories
4. Break down into tasks
5. Commit to sprint backlog

**Daily Standup**
- What I did yesterday
- What I'm doing today
- Any blockers
- Quick parking lot for discussions

**Sprint Review**
- Demo completed work
- Review metrics
- Gather feedback
- Update product backlog

**Retrospective**
- What went well
- What could improve
- Action items
- Team health check

---

## Risk Management

### Technical Risks
| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|------------|
| IndexedDB storage limits | High | Medium | Implement quota management, compress photos |
| Cross-browser compatibility | High | Medium | Test on multiple browsers, use polyfills |
| Offline sync complexity | High | Low | Simple export/import first, defer sync |
| Performance on old devices | Medium | Medium | Progressive enhancement, lazy loading |
| SVG/Canvas performance | Medium | Low | Start simple, optimize based on metrics |

### Project Risks
| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|------------|
| Scope creep | High | High | Strict MVP definition, parking lot for v2 |
| Team availability | Medium | Medium | Cross-training, documentation |
| Stakeholder changes | High | Low | Regular demos, early feedback |
| Technical debt | Medium | Medium | 20% time for refactoring |
| Testing bottleneck | Medium | Medium | Test automation, pair testing |

---

## Success Metrics

### Sprint Metrics
- **Velocity:** Story points completed
- **Burndown:** Daily progress tracking
- **Defect Rate:** Bugs found/fixed per sprint
- **Test Coverage:** Maintain >80%
- **Cycle Time:** Story start to done

### Product Metrics
- **Performance:** Page load <3s, interactions <150ms
- **Offline Reliability:** 100% feature availability offline
- **Data Integrity:** Zero data loss reports
- **Accessibility:** WCAG 2.1 AA compliance
- **Browser Support:** Chrome, Firefox, Safari, Edge

### Business Metrics
- **Time to MVP:** 10 weeks target
- **Feature Completion:** 100% P0, 80% P1
- **User Feedback:** Post-launch survey
- **Adoption Rate:** Track installs/usage
- **Retention:** 30-day active users

---

## Release Planning

### MVP Release (v0.1)
**Target Date:** End of Week 10

**Release Criteria:**
- All P0 stories complete
- Zero critical bugs
- Performance benchmarks met
- Offline functionality verified
- Export/Import working
- Deployed to production

**Release Activities:**
1. Code freeze (Week 10, Day 3)
2. Final testing (Week 10, Day 4)
3. Deployment (Week 10, Day 5)
4. Monitoring and support

### Post-MVP Roadmap

**v0.2 (Weeks 11-14)**
- Calendar view
- Reminders/notifications
- Quick templates
- Bulk operations
- Enhanced mobile UX

**v0.3 (Weeks 15-20)**
- Weather integration
- Sun path visualization
- Analytics dashboard
- CSV import
- Companion planting

---

## Communication Plan

### Channels
- **Daily:** Slack/Teams for quick updates
- **Weekly:** Email status report
- **Sprint:** Demo video for stakeholders
- **Ad-hoc:** GitHub issues for bugs/features

### Stakeholder Updates
- Sprint review demos (bi-weekly)
- Progress dashboard (real-time)
- Release notes (per version)
- User feedback sessions (monthly)

### Documentation
- Technical: GitHub wiki
- User: In-app help
- API: Inline code docs
- Process: Confluence/Notion

---

## Tools & Infrastructure

### Development
- **IDE:** VS Code with extensions
- **Version Control:** Git + GitHub
- **Package Manager:** npm/yarn
- **Build Tool:** Vite/Webpack
- **Testing:** Jest + Testing Library

### Project Management
- **Board:** GitHub Projects / Jira
- **Communication:** Slack/Teams
- **Documentation:** Markdown/Wiki
- **Design:** Figma
- **Monitoring:** Sentry/LogRocket

### CI/CD
- **Pipeline:** GitHub Actions
- **Testing:** Automated on PR
- **Deployment:** Netlify/Vercel
- **Monitoring:** Uptime/performance
- **Analytics:** Privacy-friendly option

---

## Budget Considerations

### Development Costs
- Team: 4 people × 10 weeks
- Infrastructure: Minimal (static hosting)
- Tools: Open source preferred
- Testing devices: 2-3 phones/tablets

### Ongoing Costs
- Hosting: ~$20/month
- Domain: ~$15/year
- Error tracking: ~$30/month
- Future: Cloud storage for sync

---

## Quality Assurance Strategy

### Testing Pyramid
- **Unit Tests:** 60% - Components, utilities
- **Integration:** 30% - Module interactions
- **E2E Tests:** 10% - Critical user paths

### Test Coverage
- Catalog: Create, search, filter
- Map: Draw, place, move
- Journal: Add, photo, timeline
- Offline: CRUD without network
- Export: Complete data integrity

### Performance Testing
- Lighthouse CI on every build
- Load testing with 1000+ plants
- Memory profiling for leaks
- Device testing matrix

---

## Launch Strategy

### Soft Launch (Week 10)
- Internal team testing
- 5-10 beta users
- Feedback collection
- Bug fixes

### Public Launch (Week 11)
- Product Hunt submission
- Reddit gardening communities
- Social media announcement
- Documentation site live

### Support Plan
- GitHub issues for bugs
- Discord/Slack community
- FAQ documentation
- Video tutorials

---

## Continuous Improvement

### Post-MVP Process
- Bi-weekly releases
- User feedback integration
- Performance monitoring
- Security updates
- Feature flags for experiments

### Metrics Review
- Weekly metrics dashboard
- Monthly user feedback
- Quarterly roadmap review
- Annual architecture review

---

## Appendix: Story Point Reference

### Estimation Scale (Fibonacci)
- **1 point:** Simple change, <2 hours
- **2 points:** Small feature, <1 day
- **3 points:** Medium feature, 1-2 days
- **5 points:** Large feature, 2-3 days
- **8 points:** Complex feature, 3-5 days
- **13 points:** Epic, needs breakdown

### Velocity Assumptions
- Developer: 8-10 points/sprint
- Junior: 5-7 points/sprint
- Senior: 10-13 points/sprint
- Team of 3: 25-30 points/sprint