# VibeCode Platform 🚀

<div align="center">

![VibeCode Logo](https://via.placeholder.com/200x100/667eea/ffffff?text=VibeCode)

**A Bolt.new-inspired AI-powered no-code web development platform**

Build amazing web applications using natural language - no coding required!

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen)](https://nodejs.org/)
[![Python Version](https://img.shields.io/badge/python-%3E%3D3.11-blue)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/docker-supported-blue)](https://www.docker.com/)

[🌟 Live Demo](https://vibecode-demo.vercel.app) | [📖 Documentation](https://docs.vibecode.com) | [🎯 Roadmap](https://github.com/vibecode/platform/projects)

</div>

## ✨ Features

### 🎨 **Bolt.new-Inspired Interface**
- Beautiful, modern UI with stunning gradients
- Real-time code preview with Sandpack integration
- Intuitive drag-and-drop functionality
- Dark mode support

### 🤖 **AI-Powered Development**
- Generate complete applications from natural language prompts
- Support for multiple AI models (GPT-4, Claude, Gemini)
- Intelligent code completion and suggestions
- Automated testing and debugging

### 🛠️ **Full-Stack Platform**
- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **Backend**: Node.js, Express, TypeScript
- **AI Service**: Python, LangChain, FastAPI
- **Database**: PostgreSQL with Redis caching
- **Deployment**: Docker, Vercel, Netlify, AWS support

### 📦 **Project Management**
- Create and manage multiple projects
- Real-time collaboration
- Version control integration
- One-click deployment

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- Python 3.11+
- PostgreSQL (optional, SQLite for development)
- Docker (optional)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/vibecode-platform.git
cd vibecode-platform
```

### 2. Automated Setup

```bash
# Make setup script executable
chmod +x scripts/setup.sh

# Run the setup script
./scripts/setup.sh
```

This will:
- ✅ Check system requirements
- ✅ Install all dependencies
- ✅ Set up environment files
- ✅ Initialize the database
- ✅ Build all applications

### 3. Configure API Keys

Update your `.env` files with your API keys:

```bash
# backend/.env
OPENAI_API_KEY=your-openai-api-key
ANTHROPIC_API_KEY=your-anthropic-api-key
DATABASE_URL=postgresql://user:password@localhost:5432/vibecode

# ai/.env
OPENAI_API_KEY=your-openai-api-key
ANTHROPIC_API_KEY=your-anthropic-api-key
```

### 4. Start Development

```bash
# Start all services
npm run dev

# Or start individual services
npm run dev:frontend  # Frontend at http://localhost:3000
npm run dev:backend   # Backend at http://localhost:5000
```

### 5. Visit Your App

Open [http://localhost:3000](http://localhost:3000) to see VibeCode in action! 🎉

## 🐳 Docker Deployment

### Development with Docker

```bash
# Start all services with Docker
docker-compose -f docker/docker-compose.yml up

# With development tools (pgAdmin, Redis GUI)
docker-compose -f docker/docker-compose.yml --profile dev up
```

### Production Deployment

```bash
# Build and deploy to production
./scripts/deploy.sh docker --env production
```

## 📁 Project Structure

```
vibecode-platform/
├── 📁 frontend/              # Next.js React frontend
│   ├── 📁 components/        # Reusable UI components
│   ├── 📁 pages/            # Next.js pages
│   ├── 📁 styles/           # Tailwind CSS styles
│   └── 📁 hooks/            # Custom React hooks
├── 📁 backend/               # Node.js Express API
│   ├── 📁 src/
│   │   ├── 📁 controllers/  # API controllers
│   │   ├── 📁 routes/       # API routes
│   │   ├── 📁 middleware/   # Express middleware
│   │   └── 📁 models/       # Database models
├── 📁 ai/                   # Python AI service
│   ├── 📄 langchain_router.py  # AI model routing
│   ├── 📄 generate_code.py     # Code generation
│   └── 📄 requirements.txt     # Python dependencies
├── 📁 database/             # Database files
│   ├── 📁 migrations/       # SQL migrations
│   └── 📁 seed/            # Seed data
├── 📁 docker/               # Docker configuration
│   ├── 📄 docker-compose.yml  # Development setup
│   └── 📄 Dockerfile.*        # Service Dockerfiles
└── 📁 scripts/              # Deployment scripts
    ├── 📄 setup.sh         # Automated setup
    └── 📄 deploy.sh        # Deployment script
```

## 🎯 Usage Examples

### Generate a Todo App

1. Open VibeCode at [http://localhost:3000](http://localhost:3000)
2. Click "Start Building Now"
3. Enter prompt: *"Create a todo app with drag-and-drop functionality and dark mode"*
4. Watch as AI generates your complete application!
5. Preview in real-time and deploy with one click

### Supported Prompts

- *"Build a weather dashboard with charts and animations"*
- *"Create an e-commerce store with shopping cart"*
- *"Make a blog platform with markdown support"*
- *"Design a portfolio website with smooth animations"*

## 🔧 Configuration

### Environment Variables

#### Backend (.env)
```bash
NODE_ENV=development
PORT=5000
DATABASE_URL=postgresql://user:pass@localhost:5432/vibecode
JWT_SECRET=your-jwt-secret
OPENAI_API_KEY=your-openai-key
ANTHROPIC_API_KEY=your-anthropic-key
```

#### AI Service (.env)
```bash
OPENAI_API_KEY=your-openai-key
ANTHROPIC_API_KEY=your-anthropic-key
DEFAULT_MODEL=gpt-3.5-turbo
MAX_TOKENS=4000
```

### Supported AI Models

- **OpenAI**: GPT-4, GPT-3.5 Turbo
- **Anthropic**: Claude 3 Opus, Claude 3 Sonnet
- **Google**: Gemini Pro
- **Hugging Face**: Code Llama, Starcoder

## 📚 API Documentation

### Authentication
```bash
POST /api/auth/signup     # Create account
POST /api/auth/login      # Sign in
GET  /api/auth/me         # Get user profile
```

### Projects
```bash
GET    /api/projects      # List projects
POST   /api/projects      # Create project
GET    /api/projects/:id  # Get project
PUT    /api/projects/:id  # Update project
DELETE /api/projects/:id  # Delete project
```

### AI Generation
```bash
POST /api/ai/generate     # Generate code
POST /api/ai/explain      # Explain code
POST /api/ai/improve      # Improve code
POST /api/ai/debug        # Debug code
```

## 🚀 Deployment Options

### Vercel (Recommended for Frontend)
```bash
./scripts/deploy.sh vercel --env production
```

### Netlify
```bash
./scripts/deploy.sh netlify --env production
```

### Docker
```bash
./scripts/deploy.sh docker --env production
```

### AWS
```bash
./scripts/deploy.sh aws --env production
```

## 🧪 Testing

```bash
# Run all tests
npm test

# Frontend tests
cd frontend && npm test

# Backend tests
cd backend && npm test

# AI service tests
cd ai && python -m pytest
```

## 🤝 Contributing

We love contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@vibecode.com
- 💬 Discord: [Join our community](https://discord.gg/vibecode)
- 🐛 Issues: [GitHub Issues](https://github.com/your-username/vibecode-platform/issues)
- 📖 Docs: [Documentation](https://docs.vibecode.com)

## 🙏 Acknowledgments

- [Bolt.new](https://bolt.new) for inspiration
- [Next.js](https://nextjs.org/) for the amazing React framework
- [Tailwind CSS](https://tailwindcss.com/) for beautiful styling
- [LangChain](https://langchain.com/) for AI integration
- [Sandpack](https://sandpack.codesandbox.io/) for code preview

## 🗺️ Roadmap

- [ ] **v1.1**: Real-time collaboration
- [ ] **v1.2**: Plugin system
- [ ] **v1.3**: Mobile app
- [ ] **v1.4**: Advanced AI models
- [ ] **v1.5**: Enterprise features

---

<div align="center">

**Built with ❤️ by the VibeCode Team**

[⭐ Star us on GitHub](https://github.com/your-username/vibecode-platform) | [🐦 Follow on Twitter](https://twitter.com/vibecode)

</div>