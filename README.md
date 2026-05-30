# ✦ FitAI — AI-Powered Fashion Recommendation Platform

> A professional AI fashion platform built with Flask, MongoDB, Machine Learning, and OpenAI.

![FitAI Banner](https://via.placeholder.com/1200x400/040810/00d4ff?text=FitAI+%E2%80%94+AI+Fashion+Intelligence)

---

## 🚀 Features

| Feature | Tech Used |
|---|---|
| 🎯 AI Style Prediction | RandomForest ML (scikit-learn) |
| 🛍️ Product Catalog | MongoDB Atlas + PyMongo |
| 💬 StyleBot Chatbot | OpenAI GPT / Rule-based fallback |
| 📊 Analytics Dashboard | Chart.js + MongoDB Aggregation |
| 🔒 Authentication | Flask Sessions + Bcrypt |
| ✨ Premium UI | Glassmorphism + Particle Canvas |
| 💡 Lamp Login Animation | Pure CSS + JS |
| 🌐 Deployment Ready | Vercel + MongoDB Atlas |

---

## 🗂️ Project Structure

```
fitai/
├── app.py                    # Main Flask app, all routes
├── ml_models/
│   ├── __init__.py
│   └── fashion_predictor.py  # RandomForest ML model
├── templates/
│   ├── base.html             # Shared layout, navbar, footer
│   ├── index.html            # Homepage with hero, features
│   ├── login.html            # Lamp animation auth page
│   ├── predict.html          # AI prediction form + results
│   ├── products.html         # E-commerce catalog
│   ├── chatbot.html          # StyleBot chat interface
│   └── dashboard.html        # Analytics & user dashboard
├── static/
│   ├── css/
│   │   ├── style.css         # Main design system
│   │   └── login.css         # Lamp animation styles
│   └── js/
│       ├── particles.js      # Canvas particle background
│       ├── main.js           # Navbar, scroll, shared utils
│       ├── login.js          # Lamp toggle + auth forms
│       ├── predict.js        # ML prediction + rendering
│       ├── products.js       # Catalog + modal + favorites
│       ├── chatbot.js        # Chat UI + API calls
│       └── dashboard.js      # Chart.js + analytics
├── requirements.txt
├── vercel.json
├── .env.example
└── README.md
```

---

## ⚡ Quick Start

### 1. Clone & Install

```bash
git clone https://github.com/yourusername/fitai.git
cd fitai
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Configure Environment

```bash
cp .env.example .env
# Edit .env with your MongoDB URI and OpenAI key
```

### 3. Run

```bash
python app.py
# → http://localhost:5000
```

---

## 🍃 MongoDB Atlas Setup

1. Create free account at [cloud.mongodb.com](https://cloud.mongodb.com)
2. Create cluster (M0 Free Tier)
3. **Database Access** → Add user with password
4. **Network Access** → Add IP: `0.0.0.0/0` (allow all)
5. **Connect** → Drivers → Copy connection string
6. Paste into `.env` as `MONGO_URI`

### Collections Created Automatically:
- `users` — Auth data (hashed passwords)
- `predictions` — ML prediction history
- `favorites` — User saved products
- `chatbot_history` — Chat logs
- `fashion_products` — Product catalog
- `analytics` — Usage stats

---

## 🤖 ML Model Details

**Algorithm:** RandomForestClassifier (scikit-learn)  
**Training Data:** 2,000 synthetic records  
**Features:** Height, Weight, Age, BMI (derived)  
**Target:** Clothing size (XS/S/M/L/XL/XXL)  
**Style Prediction:** Rule-based on body type + gender + age

**Prediction Output:**
```json
{
  "style": "Minimalist",
  "alt_styles": ["Streetwear", "Casual Chic"],
  "size": "M",
  "bmi": 22.4,
  "bmi_category": "Normal weight",
  "confidence": 91,
  "size_confidence": 87.3,
  "outfits": ["White Oxford + slim chinos + white sneakers", ...],
  "color_palette": ["#FFFFFF", "#000000", "#F5F0EB", ...],
  "season_tip": "Invest in neutral basics..."
}
```

---

## 🚀 Deploy to Vercel

```bash
npm i -g vercel
vercel login
vercel --prod
```

Set environment variables in Vercel dashboard:
- `MONGO_URI`
- `SECRET_KEY`
- `OPENAI_API_KEY`

---

## 🎨 Design System

- **Theme:** Dark futuristic glassmorphism
- **Colors:** `#00d4ff` (neon blue), `#7b2ff7` (electric purple)
- **Fonts:** Syne (display), Space Grotesk (body), JetBrains Mono (code)
- **Effects:** Particle canvas, glow animations, glassmorphism cards
- **Login:** Lamp ON/OFF toggle animation with rope pull

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3.11 + Flask 3.0 |
| Database | MongoDB Atlas + PyMongo |
| ML | scikit-learn (RandomForest) |
| AI Chat | OpenAI GPT-3.5 / Fallback |
| Frontend | Vanilla JS + CSS Variables |
| Charts | Chart.js 4 |
| Particles | Canvas API |
| Fonts | Google Fonts (Syne + Space Grotesk) |
| Deployment | Vercel + MongoDB Atlas |

---

## 📋 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Homepage |
| GET/POST | `/login` | Auth login |
| POST | `/register` | Register |
| GET | `/logout` | Logout |
| GET | `/predict-page` | Prediction UI |
| GET | `/products` | Products catalog |
| GET | `/chatbot` | Chat UI |
| GET | `/dashboard` | Analytics |
| POST | `/api/predict` | Run ML prediction |
| GET | `/api/products` | Fetch products |
| POST | `/api/chat` | Chat with StyleBot |
| GET | `/api/dashboard` | Dashboard data |
| POST | `/api/favorites/toggle` | Save/unsave item |
| POST | `/api/seed-products` | Seed demo products |

---

## 📸 Portfolio Highlights

- ✅ Full-stack ML integration (not just a demo)
- ✅ Real database (MongoDB Atlas with 6 collections)
- ✅ Production auth (bcrypt + Flask sessions)
- ✅ OpenAI integration with graceful fallback
- ✅ Responsive on all screen sizes
- ✅ Professional glassmorphism UI
- ✅ Deployment-ready (Vercel + Atlas)

---

Built with ❤️ for IBM ML Project | Portfolio | Hackathon | Internship Showcase
