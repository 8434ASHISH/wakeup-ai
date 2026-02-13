# WakeUp AI - Development Guide

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Installation

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
WakeUP AI/
├── public/
│   └── tones/          # Alarm audio files
├── src/
│   ├── components/     # Reusable UI components
│   │   └── navbar.js
│   ├── screens/        # Application screens
│   │   ├── home.js
│   │   ├── quickNap.js
│   │   ├── customAlarm.js
│   │   ├── alarmRinging.js
│   │   ├── aiChat.js
│   │   └── calculators.js
│   ├── services/       # Core services
│   │   ├── storage.js
│   │   ├── gemini.js
│   │   ├── alarmEngine.js
│   │   └── audioPlayer.js
│   ├── styles/         # CSS stylesheets
│   │   ├── main.css
│   │   ├── components.css
│   │   ├── home.css
│   │   └── screens.css
│   ├── main.js        # Application entry point
│   └── router.js      # SPA router
├── .env               # Environment variables
├── .gitignore
├── index.html
├── package.json
├── vite.config.js
└── PRD.md            # Product requirements
```

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```
VITE_GEMINI_API_KEY=your_api_key_here
```

## 🎨 Features

### Core Features
- ⏰ **Custom Alarms** - Personalized alarms with purpose and tone
- 😴 **Quick Nap** - Power nap timer with circular selector
- 🤖 **AI Assistant** - Chat interface with alarm creation
- 🔢 **Student Tools** - 8 productivity calculators
- 🔥 **Streak Tracking** - Habit consistency monitoring

### AI Integration
- Purpose-driven wake-up messages
- Tone-based personality (Strict, Funny, Motivational, Calm)
- Natural language alarm creation
- Text-to-speech voice playback

### Technical Features
- Single-page application with client-side routing
- LocalStorage for data persistence
- Web Audio API for alarm tones
- Speech Synthesis API for AI voice
- Notification API for alarm alerts
- Responsive design (mobile + desktop)

## 🛠️ Development

### Adding New Screen

1. Create screen file in `src/screens/`
2. Add route in `src/router.js`
3. Create corresponding styles if needed

### Modifying Services

- **Storage**: `src/services/storage.js` - LocalStorage wrapper
- **Gemini AI**: `src/services/gemini.js` - AI integration
- **Alarm Engine**: `src/services/alarmEngine.js` - Alarm logic
- **Audio Player**: `src/services/audioPlayer.js` - Sound playback

## 📱 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Requires support for:
- Web Audio API
- Speech Synthesis API
- Notification API
- LocalStorage

## ⚠️ Important Notes

1. **API Key Security**: In production, use a backend proxy to protect the Gemini API key
2. **Browser Permissions**: App requires notification permission for alarm functionality
3. **Audio Autoplay**: Browser policies may block audio without user interaction

## 🐛 Known Issues

- npm not installed on current system (run `winget install OpenJS.NodeJS` to install)
- Custom alarm tone MP3 not included (uses generated tones as fallback)

## 📝 License

All rights reserved.
