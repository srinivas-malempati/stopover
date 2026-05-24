# 🛣️ Stopover — AI Road Trip Planner

> Plan your perfect road trip in 15 seconds. No signup. No friction.

![Stopover](https://img.shields.io/badge/Live-stopoverapp.vercel.app-ff7c2a?style=for-the-badge)
![PWA](https://img.shields.io/badge/PWA-Enabled-5A0FC8?style=for-the-badge)
![AI](https://img.shields.io/badge/AI-Groq%20LLaMA%203.3-00A67E?style=for-the-badge)
![Vercel](https://img.shields.io/badge/Deployed-Vercel-000000?style=for-the-badge)

---

## 🌍 Live App

**[stopoverapp.vercel.app](https://stopoverapp.vercel.app)**

Type any two cities in the world. Get a complete road trip plan in seconds.

---

## ✨ Features

- 🗺️ **AI-generated route** — curated stopovers between any two cities worldwide
- 💎 **Hidden gems** — off-the-beaten-path spots most tourists miss
- 💰 **Cost per person** — estimated spend at every stop
- 🅿️ **Parking info** — parking details at every activity
- 🌤️ **Live weather** — real-time weather at each stop
- 🏨 **Overnight stays** — hotel suggestions with price estimates
- 📄 **PDF export** — download your full itinerary to take offline
- 🌍 **Global support** — works for any country, distances and currency adapt automatically
- 📱 **PWA** — installable on iPhone and Android, works like a native app
- ⚡ **No signup required** — just type and go

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript |
| Backend | Vercel Serverless Functions |
| AI Model | Groq — LLaMA 3.3 70B |
| Weather | Open-Meteo API |
| PDF Export | jsPDF + html2canvas |
| Hosting | Vercel |

---

## 📁 Project Structure

```
stopover/
├── index.html          # Full frontend — UI, logic, styles
├── manifest.json       # PWA manifest
├── sw.js               # Service worker — offline + caching
├── public/
│   └── icons/
│       ├── icon-192.png   # PWA icon
│       └── icon-512.png   # PWA icon
└── api/
    └── route.js        # Vercel serverless function — Groq API call
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Vercel CLI
- Groq API key → [console.groq.com](https://console.groq.com)

### Local Development

```bash
# Clone the repo
git clone https://github.com/yourusername/stopover.git
cd stopover

# Install Vercel CLI
npm install -g vercel

# Add environment variable
echo "GROQ_API_KEY=your_key_here" > .env.local

# Run locally
vercel dev
```

App will be running at `http://localhost:3000`

### Deploy to Vercel

```bash
vercel --prod
```

---

## ⚙️ Environment Variables

| Variable | Description | Where to get it |
|---|---|---|
| `GROQ_API_KEY` | Groq API key for LLaMA model | [console.groq.com](https://console.groq.com) |

Set this in your Vercel project dashboard under **Settings → Environment Variables**.

---

## 📱 PWA Installation

**Android (Chrome):**
1. Open `stopoverapp.vercel.app` in Chrome
2. Tap the "Add to Home Screen" banner
3. Stopover appears as an app on your home screen

**iPhone (Safari):**
1. Open `stopoverapp.vercel.app` in Safari
2. Tap the Share button → "Add to Home Screen"
3. Stopover appears as an app on your home screen

---

## 🗺️ How It Works

1. User enters start city, end city, trip duration and vibe preferences
2. Frontend builds a detailed prompt and sends it to `/api/route`
3. Vercel serverless function calls Groq (LLaMA 3.3 70B) with the prompt
4. Groq returns a structured JSON itinerary
5. Frontend renders the route with weather, costs, parking and activities
6. User can export the full itinerary as a paginated PDF

---

## 🧠 Built By

**Srinivas** — QA Engineer turned AI product builder.

17 years in QA taught me exactly where products fail. Now I build to fix them from the start.

- 🔗 [LinkedIn](https://linkedin.com/in/srinivas-malempati)
- 🌐 [Stopover](https://stopoverapp.vercel.app)

---

## 📄 License

MIT License — free to use, modify and distribute.

---

*Built with curiosity, shipped with purpose.* 🛣️
