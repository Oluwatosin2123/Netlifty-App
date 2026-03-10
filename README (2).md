# 🇳🇬 KiddiePlan Naija — Nigerian Children's Lifestyle PWA

> **Healthy, Stylish & Happy Kids** — Nigeria's #1 children's lifestyle platform for food plans, hairstyles & fashion.

![KiddiePlan Banner](https://images.unsplash.com/photo-1531123897727-8f129e1688ce?w=1200&q=80&auto=format&fit=crop)

---

## 🌟 Live Demo

🔗 **[https://kiddieplan-naija.netlify.app](https://kiddieplan-naija.netlify.app)**

---

## 📖 Project Overview

KiddiePlan Naija is a **Progressive Web App (PWA)** built for Nigerian parents to help plan and manage three key areas of their children's lives:

- 🍽️ **Nigerian Food Timetable** — age-specific nutritious meal plans
- 💇🏾 **African Hairstyle Gallery** — braids, cornrows, natural styles and more
- 👗 **Nigerian Kids Fashion** — Ankara, Aso-Oke, Agbada, and modern styles

The app is fully **installable on mobile phones** (Android & iPhone) without needing an App Store. It works **offline**, saves user data locally, and features **AI-powered suggestions** using the Claude AI API.

---

## 🚀 How This Project Was Built — Full Journey

### Stage 1 — The Idea 💡
The project started with a simple request:

> *"Hello, can you help me build an app that users can log into, basically for choosing three major things for children — Food timetable, Hairstyle, and Children fashion style."*

**Initial decisions made:**
- Mobile-friendly web app (not a native app)
- PIN-based login system
- Features: Weekly planner, image galleries, save favourites, AI-powered suggestions

---

### Stage 2 — First Prototype (Version 1) 🛠️
The first version was built as a basic mobile-friendly HTML app with:
- PIN login (`1234` default)
- 7-day food timetable
- Hairstyle gallery with animated 3D cartoon characters
- Fashion gallery with filter tabs
- AI suggestions (Claude API)
- Favourites system
- Bottom navigation bar

**File produced:** `kids-planner-app.html`

---

### Stage 3 — Nigerian/African Redesign (Version 2) 🇳🇬
After reviewing the first version, the app was completely rebuilt to be:
- Fully **Nigerian and African** in content and theme
- Custom **password creation** system (not a fixed PIN)
- Real **Nigerian stock photos** used throughout
- Authentic Nigerian content added:
  - Foods: Jollof rice, Egusi, Pounded Yam, Moi Moi, Akara, Ogi, Ofada rice, Efo Riro, Banga soup, Ewedu, Suya, Zobo, Chin Chin, Tiger Nut milk, and more
  - Hairstyles: Fulani Braids, Ghana Braids, Afro Puff, Cornrow All-Back, Bantu Knots, Box Braids, Shuku/Patewo, Twist Out, Zigzag Cornrows, Goddess Braids, Faux Locs, Crown Braids
  - Fashion: Ankara Ball Gown, Aso-Oke Set, Ankara Jumpsuit, Igbo George Wrapper, Hausa Kaftan, Agbada, Isiagu, Adire/Tie-Dye, School Uniform, Owambe Party Dress

**Key improvements:**
- User creates their own **parent name + child name + custom password**
- Auto-login after first registration (no re-entry needed)
- Forgot password → reset with child's name only (no email needed)
- Saved profile chips on login screen
- Age groups: Baby (0–12m), Toddler (1–3y), Preschool (3–5y), School (6–10y), Preteen (11–13y), Teen (14–17y)
- Each meal includes nutritional info (protein, vitamins, minerals)
- Nigerian flag green (`#008751`) as brand colour

**File produced:** `kiddieplan-nigeria.html`

---

### Stage 4 — PWA Upgrade (Version 3) 📲
The app was upgraded to a full **Progressive Web App** so users could install it directly on their phone home screen without needing the App Store.

**PWA features added:**
- `manifest.json` — app name, icons, theme colour, display mode
- `sw.js` — service worker for offline support and caching
- `icon-192.png` and `icon-512.png` — custom KiddiePlan app icons
- `beforeinstallprompt` event — shows install banner automatically on Android Chrome
- iPhone Safari instructions — Share → Add to Home Screen
- `appinstalled` event — hides banner, shows success toast

**File produced:** `kiddieplan-pwa-app.html` + `kiddieplan-pwa.zip`

---

### Stage 5 — Beautiful Landing Page (Version 4) 🌟
A full production-ready **marketing landing page** was designed to introduce the app before users log in. The design was built to look like a real startup product page.

**Landing page sections:**
- 🎯 **Hero Section** — photo collage of African children, headline, stats counter, floating badges
- 📢 **Trust Ticker Bar** — scrolling marquee in Nigerian green
- ✨ **3 Feature Cards** — Food Plans, Fashion, Hairstyles with real photos
- ⚡ **How It Works** — 4-step process on dark green background
- 👶 **Age Groups** — 4 photo cards (Baby → Teen)
- 💬 **Testimonials** — 3 Nigerian parent reviews
- 📲 **CTA Section** — big green call-to-action with install buttons
- 🦶 **Footer** — 4-column with links and social buttons

**Design system used:**
- Fonts: `Syne` (headings) + `Plus Jakarta Sans` (body)
- Colours: Forest green `#1A6B3C`, Gold `#F5A623`, Cream `#FFFBF2`
- Mesh gradient backgrounds, Ankara-inspired patterns
- Scroll reveal animations, floating photo collage, animated stat counters
- Fully responsive: mobile → tablet → desktop

**File produced:** `kiddieplan-landing.html`

---

### Stage 6 — Complete Unified App (Final Version) 🏆
The landing page and the full app were **merged into one single file** so the entire user journey flows seamlessly without switching files:

```
Landing Page → Create Account → Login → Forgot Password → Main App
```

**Complete user flow:**

| Step | Screen | Description |
|------|--------|-------------|
| 1 | 🌟 Landing Page | Beautiful marketing page with all features |
| 2 | 📝 Create Account | Parent name + Child name + Custom password |
| 3 | 🔐 Login | Child name + password → straight into app |
| 4 | 🔑 Forgot Password | Child name → set new password → back to login |
| 5 | 🏠 Main App | Home → Food → Hair → Fashion → AI → Favourites |

**Smart behaviours:**
- ✅ Auto-login — reopening app skips to home screen automatically
- ✅ Session memory via `sessionStorage` — no repeated logins
- ✅ Password reset with just child's name — no email needed
- ✅ Saved profile chips on login screen
- ✅ Back buttons on every auth screen return to landing

**File produced:** `kiddieplan-complete.html`

---

### Stage 7 — Netlify Deployment 🚀
The app was packaged and deployed to the internet using **Netlify** (free hosting).

**Deployment package contents:**
```
kiddieplan-netlify/
├── index.html        ← Main app (renamed from kiddieplan-complete.html)
├── manifest.json     ← PWA manifest for installability
├── sw.js             ← Service worker for offline support
├── icon-192.png      ← App icon (192×192px)
├── icon-512.png      ← App icon (512×512px)
└── _redirects        ← Netlify SPA routing fix
```

**Deployment steps:**
1. Unzip the package folder
2. Go to [netlify.com](https://netlify.com) → Sign up free
3. Drag and drop the folder onto the Netlify dashboard
4. App goes live in ~10 seconds
5. Rename site: Site configuration → Site details → Change site name

**File produced:** `kiddieplan-netlify.zip`

---

## ✨ Features

### 🔐 Authentication System
- Register with parent name + child name + custom password
- Login with child name + password
- Auto-login via `sessionStorage` after first login
- Forgot password — reset with child's name only
- Saved profile chips on login screen for quick access
- Sign out button in app header

### 🍽️ Nigerian Food Timetable
- 6 age groups: Baby, Toddler, Preschool, School, Preteen, Teen
- 7-day planner (Monday–Sunday) per age group
- 4 meals per day: Breakfast, Snack, Lunch, Dinner
- 100+ authentic Nigerian meals including:
  - Jollof Rice, Egusi Soup, Pounded Yam, Moi Moi, Akara, Ogi/Pap
  - Ofada Rice & Ayamase, Efo Riro, Banga Soup, Ewedu & Amala
  - Suya, Zobo, Chin Chin, Tiger Nut Milk, Pepper Soup, and more
- Full nutritional info per meal (protein grams, vitamins, minerals)

### 💇🏾 Hairstyle Gallery
12 African/Nigerian hairstyles:
- Fulani Braids, Ghana Braids, Afro Puff, Cornrow All-Back
- Bantu Knots, Box Braids, Shuku/Patewo, Twist Out
- Zigzag Cornrows, Goddess Braids, Faux Locs, Crown Braids

Filters: All | Braids | Cornrow | Natural | Updo

### 👗 Fashion Gallery
12 Nigerian/African fashion styles:
- Ankara Ball Gown, Aso-Oke Set, Ankara Jumpsuit
- Igbo George Wrapper, Hausa Kaftan, Ankara Shorts Set
- Nigerian School Uniform, Owambe Party Dress, Adire/Tie-Dye
- Agbada (Boys), Ankara Skirt Set, Isiagu (Igbo Boys)

Filters: All | Traditional | Casual | School | Party

### 🤖 AI-Powered Suggestions
- Powered by **Claude AI** (`claude-sonnet-4-20250514`)
- Categories: Nigerian Food Plan, Hairstyle Ideas, Fashion & Outfits, Full Weekly Plan
- Age-specific suggestions (Baby → Teen)
- Custom notes field (allergies, preferences, cultural background)
- Nigerian children's lifestyle expert system prompt

### ⭐ Favourites
- Save any hairstyle or fashion item with one tap
- Persisted per child profile in `localStorage`
- Remove anytime with trash icon
- Live count shown on home screen

### 📲 PWA Installation
- Auto install banner on Android Chrome
- iPhone: Share → Add to Home Screen
- Works offline after first visit
- Custom app icon on home screen
- Splash screen on launch

---

## 🎨 Design System

| Element | Value |
|---------|-------|
| Primary Green | `#1A6B3C` |
| Secondary Green | `#25A05A` |
| Gold/Accent | `#F5A623` |
| Background | `#FFFBF2` (warm cream) |
| Heading Font | `Syne` (800 weight) |
| Body Font | `Plus Jakarta Sans` |
| Border Radius | `20px` (cards), `50px` (pills) |
| Shadows | `0 8px 32px rgba(0,0,0,0.10)` |

---

## 🏗️ Tech Stack

| Technology | Usage |
|------------|-------|
| HTML5 | App structure |
| CSS3 | Styling, animations, responsive design |
| Vanilla JavaScript | App logic, routing, state management |
| Claude AI API | AI-powered suggestions |
| localStorage | User accounts, favourites, images |
| sessionStorage | Login session management |
| Service Worker | Offline support & caching |
| Web App Manifest | PWA installability |
| Netlify | Free hosting & deployment |
| Unsplash | Real African/Nigerian stock photos |
| Google Fonts | Syne + Plus Jakarta Sans |

---

## 📁 File Structure

```
kiddieplan-naija/
├── index.html          ← Complete app (landing + auth + app in one file)
├── manifest.json       ← PWA manifest
├── sw.js               ← Service worker
├── icon-192.png        ← App icon small
├── icon-512.png        ← App icon large
└── _redirects          ← Netlify routing
```

---

## 🔧 How to Run Locally

1. Download or clone the repository
2. Open the `kiddieplan-netlify` folder
3. Open `index.html` in any browser
4. That's it — no build tools, no npm, no setup needed! ✅

> For full PWA install to work, the app must be served over HTTPS (use Netlify or any web server).

---

## 📱 How Users Install the App

### Android (Chrome)
1. Open the live link in Chrome
2. A banner appears: **"Add KiddiePlan to Home Screen"**
3. Tap **Install** — done! 🎉

### iPhone (Safari)
1. Open the live link in Safari
2. Tap the **Share button** (box with arrow)
3. Tap **"Add to Home Screen"**
4. Tap **Add** — done! 🎉

---

## 🗺️ User Journey Map

```
🌐 Open App URL
      ↓
🌟 Landing Page
   (Hero, Features, Testimonials, CTA)
      ↓
   ┌──────────────────────────┐
   │  First time?             │
   │  → Create Account        │
   │    Parent name           │
   │    Child name            │
   │    Set password          │
   │    → Auto-login ✅       │
   │                          │
   │  Returning user?         │
   │  → Login                 │
   │    Child name            │
   │    Password              │
   │    → Into app ✅         │
   │                          │
   │  Forgot password?        │
   │  → Reset                 │
   │    Child name            │
   │    New password          │
   │    → Login ✅            │
   └──────────────────────────┘
      ↓
🏠 Home Screen
      ↓
  ┌───────────────────────────────────────┐
  │  🍽️ Food    💇🏾 Hair    👗 Fashion  │
  │  🤖 AI Ideas            ⭐ Favourites │
  └───────────────────────────────────────┘
```

---

## 🌍 Target Audience

- **Nigerian parents** and guardians
- Children aged **0–17 years**
- Families who want to raise **healthy, stylish and culturally connected** children
- Works perfectly for families across **Lagos, Abuja, Port Harcourt, Ibadan, Enugu** and beyond

---

## 🔮 Future Plans

- [ ] Upload real photos for each hairstyle and fashion card
- [ ] Add more Nigerian meals and recipes with step-by-step instructions
- [ ] Push notifications for daily meal reminders
- [ ] Multi-child profiles (manage more than one child)
- [ ] Social sharing — share your child's outfit or hairstyle
- [ ] Video tutorials for hairstyles
- [ ] Backend database (move from localStorage to cloud storage)
- [ ] Android APK / iOS App Store version

---

## 🙏 Acknowledgements

- Built with the assistance of **Claude AI** by Anthropic
- Photos from **Unsplash** (African/Nigerian themed)
- Fonts from **Google Fonts** (Syne, Plus Jakarta Sans)
- Hosted for free on **Netlify**
- Inspired by the beauty, culture and richness of **Nigerian families** 🇳🇬

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

**Made with ❤️ for Nigerian families 🇳🇬**

*Raising healthy, stylish and happy kids — one plan at a time.*

</div>
