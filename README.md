# 🌱 Garden Journal & Planner

> A comprehensive offline-first Progressive Web App for home gardeners to plan, track, and optimize their gardens through visual mapping, plant cataloging, and detailed journaling.

![Version](https://img.shields.io/badge/version-0.1.0--MVP-green)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-in%20development-yellow)
![Offline](https://img.shields.io/badge/offline-ready-brightgreen)

## 📖 Overview

Garden Journal & Planner helps home gardeners manage their gardens effectively by combining three core modules:
- **📚 Plant Catalog** - Comprehensive plant and seed packet database
- **🗺️ Garden Map** - Visual garden layout and planning tool
- **📔 Journal** - Detailed observation tracking with photos

The app works completely offline, stores all data locally for privacy, and provides export/import capabilities for backup and sharing.

## ✨ Features

### Core Modules (MVP v0.1)

#### 🌿 Cataloging System
- Create and manage plant catalog with varieties, brands, and growing details
- Track seed packets with lot codes, dates, and quantities
- Search and filter by name, category, type
- Support for vegetables, fruits, herbs, flowers

#### 🗺️ Garden Planning
- Interactive visual garden map with drag-and-drop
- Draw beds, pots, and planting areas
- Place plant markers from catalog
- Track sun exposure, soil type, and orientation
- Optional background photo upload for accurate mapping

#### 📝 Journaling
- Log observations with dates and event types
- Attach multiple photos per entry
- Track watering, feeding, pruning, pests, diseases
- Timeline view per plant
- Quick-action buttons for common tasks

### 🔧 Technical Features
- **100% Offline-First** - All features work without internet
- **PWA Ready** - Install as app on mobile/desktop
- **Privacy-Focused** - All data stays on your device
- **Fast Performance** - <150ms response times
- **Responsive Design** - Works on phone, tablet, desktop
- **Export/Import** - JSON and CSV formats with photo backup

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/yarn
- Modern browser (Chrome, Firefox, Safari, Edge)
- 100MB storage space for app and data

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/GardenJournalandPlanner.git
cd GardenJournalandPlanner

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Run tests
npm test
```

### Quick Start Guide

1. **Create Your Garden**
   - Name your garden and set orientation
   - Choose metric or imperial units
   
2. **Add Plants to Catalog**
   - Enter plant varieties you grow
   - Add seed packet details
   
3. **Design Your Layout**
   - Draw garden beds and containers
   - Place plants from catalog onto map
   
4. **Start Journaling**
   - Log observations and activities
   - Take photos to document progress

## 📊 Project Status

### Current Sprint: Sprint 1 - Core Infrastructure
- [x] Project setup and planning
- [ ] IndexedDB/Dexie configuration
- [ ] PWA manifest and service worker
- [ ] Basic navigation shell
- [ ] CI/CD pipeline

### Release Timeline
- **MVP v0.1** - Week 10 (Core features)
- **v0.2** - Week 14 (Calendar, reminders, templates)
- **v0.3** - Week 20 (Weather, analytics, CSV import)

### Progress Metrics
- **Story Points Completed:** 0/124
- **Test Coverage:** Target 80%
- **Performance Score:** Target 90+
- **Accessibility:** WCAG 2.1 AA

## 🏗️ Architecture

### Tech Stack
- **Frontend:** React/Vue/Vanilla JS (TBD)
- **Storage:** IndexedDB with Dexie.js
- **Maps:** SVG/Canvas for garden visualization
- **Photos:** File System Access API
- **Build:** Vite/Webpack
- **Testing:** Jest + Testing Library
- **CI/CD:** GitHub Actions

### Data Models
```javascript
// Core entities
- Garden (id, name, orientation, units)
- Area (id, type, shape, soil, exposure)
- PlantCatalogItem (id, name, variety, category)
- SeedPacket (id, catalogId, lot, dates)
- Planting (id, areaId, catalogId, position)
- Observation (id, plantingId, date, type, notes)
- Photo (id, uri, caption, metadata)
```

## 📁 Project Structure

```
GardenJournalandPlanner/
├── docs/               # Documentation
│   ├── spec.md        # Product specification
│   ├── feature-breakdown.md
│   ├── agile-project-plan.md
│   └── user-stories-backlog.md
├── src/               # Source code
│   ├── components/    # UI components
│   ├── modules/       # Core modules
│   ├── services/      # Data and storage
│   ├── utils/         # Utilities
│   └── assets/        # Images, icons
├── tests/             # Test files
├── public/            # Static assets
└── config/            # Configuration

```

## 🧪 Testing

```bash
# Run all tests
npm test

# Run with coverage
npm run test:coverage

# Run specific module
npm test -- --grep "Catalog"

# E2E tests
npm run test:e2e
```

### Test Coverage Goals
- Unit Tests: 80% coverage
- Integration Tests: Critical paths
- E2E Tests: Core user journeys

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Workflow
1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

### Code Standards
- ESLint configuration for code style
- Prettier for formatting
- Conventional commits
- 80% test coverage minimum
- Accessibility compliance

## 📈 Roadmap

### v0.1 MVP (Current)
- [x] Project planning and setup
- [ ] Core infrastructure
- [ ] Cataloging module
- [ ] Garden map
- [ ] Journaling
- [ ] Export/Import

### v0.2 Enhanced Usability
- [ ] Calendar view
- [ ] Local notifications
- [ ] Quick templates
- [ ] Bulk operations
- [ ] Advanced filtering

### v0.3 Intelligence
- [ ] Weather integration
- [ ] Sun path visualization
- [ ] Season summaries
- [ ] Analytics dashboard
- [ ] CSV import

### Future Ideas
- [ ] Multi-garden support
- [ ] Companion planting tips
- [ ] Community sharing
- [ ] Cloud sync option
- [ ] Native mobile apps

## 📝 Documentation

- [Product Specification](docs/spec.md)
- [Feature Breakdown](docs/feature-breakdown.md)
- [Agile Project Plan](docs/agile-project-plan.md)
- [User Stories Backlog](docs/user-stories-backlog.md)
- [API Documentation](docs/api.md) (coming soon)
- [User Guide](docs/user-guide.md) (coming soon)

## 🐛 Known Issues

See [Issues](https://github.com/yourusername/GardenJournalandPlanner/issues) for current bugs and feature requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Garden icon set by [Icons8](https://icons8.com)
- Inspired by traditional garden journals and modern farming apps
- Built with feedback from local gardening communities

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/yourusername/GardenJournalandPlanner/issues)
- **Discussions:** [GitHub Discussions](https://github.com/yourusername/GardenJournalandPlanner/discussions)
- **Email:** garden-app@example.com

## 🚦 Status Badges

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Tests](https://img.shields.io/badge/tests-0%20passed-red)
![Coverage](https://img.shields.io/badge/coverage-0%25-red)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen)

---

**Made with 💚 for gardeners, by gardeners**

*Happy Gardening! 🌻🥕🌿*