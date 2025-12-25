# One Memory - AI Agent Context Manager

## 🚀 Overview
**One Memory** is a unified memory layer that eliminates context loss when switching between AI development tools (Claude Desktop, Cursor IDE, VSCode, etc.). It provides a shared memory system using Redis or LangChain memory, enabling AI agents to maintain and recall context seamlessly across sessions and platforms.

![One Memory Dashboard](screenshot.png)

## ✨ Features

### 🧠 **Shared Context Management**
- **Define Schema**: Flexible JSON/SQLite schemas for shared context fields
- **Real-time Communication**: Cross-platform APIs with Redis for instant context sharing
- **Tool Integration**: Plugins for Claude Desktop, Cursor IDE, VSCode, and more
- **State Persistence**: Local file or cloud backend storage for session continuity

### 🎨 **Frontend Highlights**
- **3D Visualization**: Interactive 3D memory node visualization using Three.js
- **Real-time Network Graph**: Live connections between different development tools
- **Glassmorphism UI**: Modern glass-like interface with gradient accents
- **Animated Dashboard**: Live statistics and memory usage visualization
- **Responsive Design**: Works seamlessly across desktop and mobile devices

## 🛠️ Technology Stack

### Frontend
- **Three.js** - 3D visualizations and animations
- **HTML5 Canvas** - Interactive network graphs
- **CSS3** - Glassmorphism effects and animations
- **Vanilla JavaScript** - No framework dependencies

### Backend (To be implemented)
- **Redis** - Real-time context sharing
- **Node.js/Express** - API server
- **LangChain Memory** - Memory management layer
- **SQLite/PostgreSQL** - Persistent storage

## 📦 Installation

### Prerequisites
- Modern web browser with WebGL support
- Node.js (for backend - coming soon)
- Redis (for backend - coming soon)

### Quick Start
1. Clone the repository:
```bash
git clone https://github.com/yourusername/one-memory.git
cd one-memory
```

2. Open the frontend:
```html
Simply open the `index.html` file in your browser
```

3. For full setup (backend coming soon):
```bash
# Backend installation (coming soon)
npm install
npm run dev
```

## 🎯 Usage

### Frontend Interface
1. **Dashboard**: View real-time memory usage and active sessions
2. **3D Visualization**: Interact with the memory node network
3. **Integration Status**: Monitor connection health with various tools
4. **Statistics**: Track context retrievals and system performance

### Integration with Development Tools
- **Claude Desktop**: Install the One Memory plugin
- **Cursor IDE**: Enable the memory extension
- **VSCode**: Add from the marketplace
- **Custom Integration**: Use our API for other tools

## 🏗️ Architecture

### Memory Schema
```json
{
  "session_id": "uuid",
  "tool_name": "claude|cursor|vscode",
  "context_data": {},
  "timestamp": "ISO8601",
  "metadata": {
    "project": "string",
    "language": "string",
    "priority": "number"
  }
}
```

### Data Flow
```
Development Tool → One Memory API → Redis Cache → LangChain Memory → Persistent Storage
         ↑                                          ↓
         └───────── Context Retrieval ←─────────────┘
```

## 📊 Performance Metrics
- **Latency**: < 50ms for context retrieval
- **Scalability**: Supports 1000+ concurrent sessions
- **Storage**: Configurable from local SQLite to cloud databases
- **Uptime**: 99.9% availability target

## 🔧 Configuration

### Environment Variables (Backend)
```bash
REDIS_URL=redis://localhost:6379
DATABASE_URL=postgresql://user:pass@localhost:5432/onememory
PORT=3000
NODE_ENV=production
```

### Frontend Customization
Edit the CSS variables in the `<style>` section to customize:
- Color scheme
- Animation speeds
- Layout dimensions
- Visual effects

## 🚀 Development

### Project Structure
```
one-memory/
├── index.html              # Main frontend file
├── README.md              # This file
├── assets/                # Images and static assets
├── css/                   # Stylesheets (if separated)
├── js/                    # JavaScript modules
│   ├── visualization.js   # 3D and network visualizations
│   ├── dashboard.js       # Dashboard functionality
│   └── api.js            # API communication
└── backend/               # Backend server (coming soon)
```

### Adding New Features
1. **New Tool Integration**: Extend the API client
2. **Additional Visualizations**: Add new Three.js scenes
3. **Custom Memory Types**: Extend the schema definition
4. **Analytics**: Implement tracking for specific metrics

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature-name'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

### Development Guidelines
- Follow the existing code style
- Add comments for complex logic
- Update documentation for new features
- Write tests for backend functionality

## 📚 Documentation

### API Reference (Coming Soon)
```
GET    /api/memory/:session_id    - Retrieve context
POST   /api/memory/               - Store context
PUT    /api/memory/:id            - Update context
DELETE /api/memory/:id            - Clear context
```

### Plugin Development
Documentation for creating custom integrations will be available in the `/docs` directory.

## 🎨 Design Principles

1. **Simplicity**: Easy to understand and use
2. **Performance**: Minimal latency, maximum throughput
3. **Reliability**: Consistent context across sessions
4. **Extensibility**: Easy to add new tools and features
5. **Security**: Encrypted data transmission and storage

## 📈 Roadmap

### Phase 1 (Current)
- ✅ Modern frontend with 3D visualization
- ✅ Basic dashboard with statistics
- ✅ Interactive network graph

### Phase 2 (In Progress)
- Backend API development
- Redis integration
- Basic plugin framework

### Phase 3 (Planned)
- Claude Desktop plugin
- Cursor IDE extension
- VSCode marketplace submission
- Advanced analytics dashboard

### Phase 4 (Future)
- Machine learning for context optimization
- Team collaboration features
- Enterprise SSO integration
- Advanced search and retrieval

## 👥 Team

**Project Lead**: Ramraj Nagar  
**Contributors**:  
**Special Thanks**: The open-source community and early testers

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- [Three.js](https://threejs.org/) for 3D visualization
- [LangChain](https://www.langchain.com/) for memory concepts
- [Redis](https://redis.io/) for real-time data storage
- All our contributors and users

## 📞 Support

- **GitHub Issues**: [Report bugs or request features](https://github.com/yourusername/one-memory/issues)
- **Documentation**: [Read the docs](https://github.com/yourusername/one-memory/wiki)
- **Email**: support@onememory.dev (coming soon)
- **Discord**: Join our community (coming soon)

---

<div align="center">
  <strong>Boost your developer flow with seamless context management</strong><br>
  <sub>One Memory - Remember everything, everywhere, all at once</sub>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
  <img src="https://img.shields.io/badge/status-alpha-orange" alt="Status">
</p>

---

**Note**: This is an alpha release. Backend functionality is in development. The frontend demonstrates the user interface and visualization capabilities of the proposed system.
