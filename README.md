# BadeBhaiya AI 🧠

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-ISC-green.svg)
![Electron](https://img.shields.io/badge/Electron-33.2.0-47848F.svg)
![React](https://img.shields.io/badge/React-18.3.1-61DAFB.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-5.6.3-3178C6.svg)
![Stars](https://img.shields.io/github/stars/YuvvrajSingh/BadeBhaiya-AI?style=social)
![Forks](https://img.shields.io/github/forks/YuvvrajSingh/BadeBhaiya-AI?style=social)

_Your AI-powered coding companion for interviews and problem-solving_

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Development](#-development) • [Contributing](#-contributing)

</div>

---

## 🎯 What is BadeBhaiya AI?

BadeBhaiya AI is your ultimate coding companion that combines the power of AI with intuitive desktop functionality. Whether you're preparing for coding interviews, solving competitive programming problems, or need quick debugging assistance, BadeBhaiya AI has got you covered!

## 🚀 Features

- **🖼️ Screenshot Analysis**: Automatically capture and analyze coding problems from any source
- **🤖 AI-Powered Solutions**: Leverage Google's Gemini AI for intelligent problem solving
- **⚡ Real-time Processing**: Get instant solutions and debugging assistance
- **🔧 Debug Mode**: Advanced debugging capabilities for complex problems
- **⌨️ Global Shortcuts**: Quick access with customizable keyboard shortcuts
- **🎯 Queue Management**: Organize and manage multiple screenshots and solutions
- **🌐 Cross-Platform**: Works seamlessly on Windows, macOS, and Linux
- **🎨 Modern UI**: Clean, intuitive interface built with React and Tailwind CSS

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher) - [Download here](https://nodejs.org/)
- **Git** - [Download here](https://git-scm.com/)
- **Gemini API Key** - [Get from Google AI Studio](https://makersuite.google.com/app/apikey)

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YuvvrajSingh/BadeBhaiya-AI.git
cd BadeBhaiya-AI
```

### 2. Install Dependencies

Run setup.bat as administrator for Windows to create setup for this project.
Then

```bash
npm install
```

### 3. Environment Setup

Copy the example environment file and add your API key:

```bash
cp .env.example .env
```

Then edit `.env` and add your Gemini API key:

```bash
# .env
GEMINI_API_KEY=your_gemini_api_key_here
```

## 🚀 Usage

### Development Mode (Recommended)

For development and testing:

```bash
npm run app:dev
```

This command starts both the Vite dev server and Electron application concurrently.

### Production Build

To build the application for distribution:

```bash
npm run app:build
```

The built application will be available in the `release/` directory.

## ⌨️ Keyboard Shortcuts

| Shortcut                | Action                   |
| ----------------------- | ------------------------ |
| `Ctrl/Cmd + B`          | Toggle window visibility |
| `Ctrl/Cmd + H`          | Take screenshot          |
| `Ctrl/Cmd + Enter`      | Get solution             |
| `Ctrl/Cmd + Arrow Keys` | Move window position     |
| `Ctrl/Cmd + Q`          | Quit application         |

## 🔧 Development

### Project Structure

```
BadeBhaiya-AI/
├── .github/           # GitHub workflows and templates
├── electron/          # Electron main process files
├── src/              # React frontend source
├── dist-electron/    # Compiled Electron files
├── dist/            # Built frontend files (generated)
├── release/         # Distribution builds (generated)
├── .env.example     # Environment variables template
├── package.json     # Project configuration
├── vite.config.ts   # Vite configuration
└── README.md        # This file
```

### Available Scripts

| Command                | Description                                      |
| ---------------------- | ------------------------------------------------ |
| `npm run dev`          | Start Vite development server                    |
| `npm run app:dev`      | Start both Vite and Electron in development mode |
| `npm run build`        | Build the React application                      |
| `npm run app:build`    | Build and package the complete Electron app      |
| `npm run electron:dev` | Start Electron with compiled TypeScript          |
| `npm run clean`        | Clean build directories                          |
| `npm run watch`        | Watch TypeScript files for changes               |

### Technology Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Backend**: Electron 33, Node.js
- **AI Integration**: Google Gemini AI
- **Build Tools**: Vite, TypeScript Compiler
- **Bundling**: Electron Builder

## 🐛 Troubleshooting

### Common Issues

#### ❌ Application won't start

```bash
# Kill existing processes
taskkill /f /im electron.exe    # Windows
pkill -f electron               # macOS/Linux

# Clean and reinstall
npm run clean
rm -rf node_modules package-lock.json
npm install
npm run app:dev
```

#### ❌ Port conflicts

The application uses port `5173` by default. If you encounter port conflicts:

```bash
# Check what's using the port
netstat -ano | findstr :5173    # Windows
lsof -i :5173                   # macOS/Linux

# Kill the process using the port
taskkill /PID <PID> /F          # Windows
kill -9 <PID>                   # macOS/Linux
```

#### ❌ Build failures

```bash
# Clear TypeScript cache
npm run clean
rm -rf dist-electron/
npm run app:dev
```

#### ❌ API Issues

- Verify your Gemini API key is correct in `.env`
- Check your internet connection
- Ensure you have API quota remaining

### Known Issues

- **Window close button**: Currently non-functional, use `Ctrl/Cmd + Q` instead
- **Cache warnings**: Electron cache warnings are cosmetic and don't affect functionality

## 📝 Contributing

We welcome contributions from the community! Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on how to get started.

### Quick Start for Contributors

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Guidelines

- Follow the existing code style
- Add appropriate documentation
- Test your changes thoroughly
- Keep PRs focused and atomic

## 📄 License

This project is licensed under the ISC License - see the [LICENSE.md](LICENSE.md) file for details.

## 🤝 Support & Contact

- **Issues**: Feel free to report bugs and request features
- **Author**: [@YuvvrajSingh](https://github.com/YuvvrajSingh)
- **Pull Requests**: Always welcome and will be reviewed promptly

## 🙏 Acknowledgments

- Thanks to Google for the Gemini AI API
- Built with the amazing Electron and React ecosystems
- Inspired by the coding community's need for better tools

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ by the BadeBhaiya AI team

</div>
