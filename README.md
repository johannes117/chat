# Chat Studio

A modern, open-source chat application that provides free access to powerful AI models including Google's Gemini, Anthropic's Claude, OpenAI's GPT, and more. Built with Next.js 15, React Router, and featuring a beautiful, responsive UI.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Next.js](https://img.shields.io/badge/Next.js-15+-black?logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-18+-blue?logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5+-blue?logo=typescript)](https://www.typescriptlang.org/)

## ✨ Features

### 🆓 **Free AI Access**
- **No API key required** to get started
- Free access to Gemini 2.5 Flash and Gemini 2.0 Flash models
- Host-provided API keys for immediate usage

### 🔑 **Flexible API Key Management**
- **Bring your own keys** for better rate limits and premium models
- Support for multiple AI providers:
  - 🟢 **Google AI** (Gemini 2.5 Pro, 2.5 Flash, 2.0 Flash)
  - 🟣 **Anthropic** (Claude 4 Sonnet, Haiku 3.5, Opus)
  - 🔵 **OpenAI** (GPT-4.1, o3, o4-mini)
  - 🟠 **OpenRouter** (Access to multiple models)
- User keys automatically override host keys when provided

### 💬 **Modern Chat Experience**
- Real-time streaming responses
- Conversation persistence with local storage
- Beautiful, responsive UI with dark/light mode
- LaTeX math rendering support
- Message editing and regeneration
- Auto-generated conversation titles

### 🔒 **Privacy & Security**
- All data stored locally in your browser
- No server-side conversation logging
- API keys encrypted and stored securely
- Open source and transparent

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ or Bun
- A Google AI API key (optional, for host setup)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/chat-studio.git
   cd chat-studio
   ```

2. **Install dependencies:**
   ```bash
   bun install
   # or
   npm install
   ```

3. **Set up environment variables (optional):**
   
   Create a `.env.local` file for host API key setup:
   ```bash
   # Optional: Provide free access to Gemini models for all users
   HOST_GOOGLE_API_KEY=your_google_api_key_here
   ```

4. **Start the development server:**
   ```bash
   bun run dev
   # or
   npm run dev
   ```

5. **Open your browser:**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🔧 Configuration

### Host API Key Setup (Optional)

To provide free access to Gemini models for all users:

1. Get a Google AI API key from [Google AI Studio](https://aistudio.google.com/apikey)
2. Add it to your `.env.local` file:
   ```
   HOST_GOOGLE_API_KEY=AIza...your_key_here
   ```
3. Restart your development server

**Benefits of host API key:**
- Users can chat immediately without setup
- Free access to Gemini 2.5 Flash and 2.0 Flash
- Users can still add their own keys for premium features

### User API Keys

Users can add their own API keys for:
- **Better rate limits**
- **Access to premium models** (Gemini 2.5 Pro, Claude 4, GPT-4.1)
- **Personal usage quotas**

## 📁 Project Structure

```
chat-studio/
├── app/                    # Next.js app router
│   ├── api/               # API routes
│   └── page.tsx           # Main page
├── components/            # Reusable UI components
├── frontend/              # Frontend-specific code
│   ├── components/        # React components
│   ├── hooks/            # Custom React hooks
│   ├── routes/           # Route components
│   ├── storage/          # Local storage utilities
│   └── stores/           # Zustand state management
├── lib/                  # Shared utilities
├── styles/               # Global styles
└── public/              # Static assets
```

## 🛠️ Technology Stack

- **Framework:** Next.js 15 with App Router
- **Frontend:** React 18, TypeScript
- **Routing:** React Router (client-side)
- **Styling:** Tailwind CSS + shadcn/ui
- **State Management:** Zustand
- **Database:** Dexie (IndexedDB)
- **AI SDKs:** Vercel AI SDK
- **Package Manager:** Bun

## 🎯 Supported AI Models

### Free Models (with host API key)
- ✅ Gemini 2.5 Flash
- ✅ Gemini 2.0 Flash

### Premium Models (require user API keys)
- 🔑 **Google:** Gemini 2.5 Pro
- 🔑 **Anthropic:** Claude 4 Sonnet, Haiku 3.5, Opus
- 🔑 **OpenAI:** GPT-4.1, GPT-4.1-mini, o3, o4-mini
- 🔑 **OpenRouter:** DeepSeek R1, Gemini via OpenRouter

## 🚀 Deployment

### Vercel (Recommended)

1. Fork this repository
2. Connect to Vercel
3. Add environment variables:
   ```
   HOST_GOOGLE_API_KEY=your_key_here
   ```
4. Deploy!

### Other Platforms

The app can be deployed on any platform that supports Next.js:
- Netlify
- Railway
- DigitalOcean App Platform
- Self-hosted with Docker

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Guidelines

- Use TypeScript for all new code
- Follow the existing code style
- Add tests for new features
- Update documentation as needed

## 📝 API Keys & Providers

### Getting API Keys

| Provider | Get API Key | Key Format |
|----------|-------------|------------|
| **Google AI** | [AI Studio](https://aistudio.google.com/apikey) | `AIza...` |
| **Anthropic** | [Console](https://console.anthropic.com/settings/keys) | `sk-ant-...` |
| **OpenAI** | [Platform](https://platform.openai.com/settings/organization/api-keys) | `sk-...` |
| **OpenRouter** | [Dashboard](https://openrouter.ai/keys) | `sk-or-...` |

### Rate Limits & Costs

- **Host keys:** Shared rate limits, free for users
- **User keys:** Personal quotas, user pays for usage
- **OpenRouter:** Often has free tier models available

## 🔒 Privacy & Security

- **Local Storage:** All conversations stored in browser's IndexedDB
- **No Server Logging:** Conversations never stored on servers
- **API Key Security:** User keys encrypted and stored locally
- **Host Key Security:** Server-side only, never exposed to client
- **HTTPS:** All API communications encrypted in transit

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Vercel AI SDK](https://sdk.vercel.ai/) for AI provider integration
- [shadcn/ui](https://ui.shadcn.com/) for beautiful UI components
- [Zustand](https://zustand-demo.pmnd.rs/) for state management
- [Dexie](https://dexie.org/) for local database management

## 📞 Support

- 🐛 **Bug Reports:** [Open an issue](https://github.com/your-username/chat-studio/issues)
- 💡 **Feature Requests:** [Open an issue](https://github.com/your-username/chat-studio/issues)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/your-username/chat-studio/discussions)

---

**Made with ❤️ by the Johannes du Plessis**