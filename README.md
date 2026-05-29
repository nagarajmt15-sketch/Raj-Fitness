# 🏋️ Raj Fitness — Official Website

> **Forge Your Limit** · Ammapettai's most trusted gym since 2011

![Raj Fitness](https://img.shields.io/badge/Raj%20Fitness-Salem-red?style=for-the-badge)
![React](https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-5-purple?style=for-the-badge&logo=vite)
![Tailwind](https://img.shields.io/badge/Tailwind-3-teal?style=for-the-badge&logo=tailwindcss)

---

## 📌 About

Official website for **Raj Fitness Gym & Power Lifting**, Ammapettai, Salem.  
Built with React + Vite + TypeScript + Tailwind CSS + Three.js.

**Live URL:** *(Add your Netlify URL here after deploy)*  
**Location:** 14, Bhuvana Complex, 2nd Floor, Balaji Nagar 335, TVK Road, Ammapettai, Salem - 636003  
**Phone:** 098425 46263  
**Master Trainer:** Krishna

---

## 🗂️ Project Structure

```
raj-fitness/
├── public/
│   ├── favicon.svg              # Browser tab icon
│   ├── favicon.ico
│   ├── robots.txt
│   └── _redirects               # Netlify SPA routing fix
│
├── src/
│   ├── assets/                  # All images
│   │   ├── gallery-1.jpg        # Gym photos (1–14)
│   │   ├── result-1.jpg         # Transformation photos (1–10)
│   │   ├── program-weights.jpg  # Program card images
│   │   ├── program-fatloss.jpg
│   │   ├── program-personal.jpg
│   │   ├── program-women.jpg
│   │   └── trainer-krishna.png  # Trainer photo
│   │
│   ├── components/
│   │   ├── sections/            # Page sections
│   │   │   ├── Hero.tsx         # Landing hero + 3D dumbbell
│   │   │   ├── About.tsx        # Salem's home of transformations
│   │   │   ├── Programs.tsx     # 4 program cards with real photos
│   │   │   ├── Pricing.tsx      # Real fee structure from board
│   │   │   ├── Trainers.tsx     # Master Trainer Krishna profile
│   │   │   ├── Transformation.tsx  # Carousel with 10 result photos
│   │   │   ├── Gallery.tsx      # Auto-moving 3-row image gallery
│   │   │   ├── Contact.tsx      # Address + map + booking
│   │   │   └── Footer.tsx       # Full footer + WhatsApp FAB
│   │   │
│   │   ├── ui/                  # shadcn/ui components
│   │   ├── BookingDialog.tsx    # WhatsApp free trial booking
│   │   ├── Loader.tsx           # Page load animation
│   │   ├── Navbar.tsx           # Navigation bar
│   │   ├── NavLink.tsx          # Nav link component
│   │   ├── Reveal.tsx           # Scroll reveal animation
│   │   ├── ScrollDumbbell.tsx   # 3D Three.js dumbbell
│   │   ├── ScrollProgress.tsx   # Top scroll progress bar
│   │   └── SmoothCursor.tsx     # Custom cursor
│   │
│   ├── hooks/
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   │
│   ├── lib/
│   │   ├── contact.ts           # ⚠️ Gym contact info — edit here
│   │   └── utils.ts
│   │
│   ├── pages/
│   │   ├── Index.tsx            # Main page
│   │   └── NotFound.tsx         # 404 page
│   │
│   ├── App.tsx
│   ├── index.css                # Global styles + custom CSS classes
│   └── main.tsx
│
├── index.html                   # HTML entry + meta tags
├── package.json
├── vite.config.ts
├── tailwind.config.ts
└── tsconfig.json
```

---

## ⚡ Quick Start

### Prerequisites
- **Node.js 18+** — [nodejs.org](https://nodejs.org)

### Install & Run
```bash
# 1. Install dependencies
npm install

# 2. Start dev server
npm run dev

# 3. Open browser
# http://localhost:8080
```

### Build for Production
```bash
npm run build
# Output: dist/ folder
```

---

## ✏️ How to Edit Content

### Change gym contact info
Edit **one file** — everything updates automatically:
```ts
// src/lib/contact.ts
export const PHONE      = "9842546263";
export const PHONE_INTL = "919842546263";
export const PHONE_DISPLAY = "098425 46263";
export const ADDRESS_FULL  = "14, Bhuvana Complex...";
```

### Change pricing
```tsx
// src/components/sections/Pricing.tsx
const weightGain = [
  { months: "1 Month", entrance: 400, fees: 400, total: 800, offer: 750 },
  // edit rows here
];
```

### Add/replace images
Drop new images into `src/assets/` with these exact names:

| File name | Used in |
|-----------|---------|
| `gallery-1.jpg` to `gallery-14.jpg` | Gallery section |
| `result-1.jpg` to `result-10.jpg` | Transformation carousel |
| `program-weights.jpg` | Weight Gain card |
| `program-fatloss.jpg` | Weight Loss card |
| `program-personal.jpg` | Personal Training card |
| `program-women.jpg` | Ladies Fitness card |
| `trainer-krishna.png` | Trainer profile |

### Change navbar links
```tsx
// src/components/Navbar.tsx
const links = [
  { label: "About",    href: "#about" },
  { label: "Programs", href: "#programs" },
  // add/remove links here
];
```

---

## 🚀 Deploy to Netlify

### Option A — Drag & Drop (one-time)
1. `npm run build`
2. Go to [netlify.com](https://netlify.com) → Add new site → Deploy manually
3. Drag `dist/` folder → Done!

### Option B — GitHub Auto-Deploy (recommended)
```bash
# First time setup
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/YOUR_USERNAME/raj-fitness.git
git push -u origin main
```
Then in Netlify:
- Import from Git → GitHub → Select repo
- Build command: `npm run build`
- Publish directory: `dist`
- Deploy!

### Every future update
```bash
git add .
git commit -m "update pricing"
git push
# Netlify auto-builds and goes live in ~1 min ✓
```

> ⚠️ Make sure `public/_redirects` file exists with:
> ```
> /*    /index.html   200
> ```

---

## 🎨 Tech Stack

| Technology | Version | Purpose |
|-----------|---------|---------|
| React | 18 | UI framework |
| TypeScript | 5 | Type safety |
| Vite | 5 | Build tool |
| Tailwind CSS | 3 | Styling |
| Three.js | r128 | 3D dumbbell |
| @react-three/fiber | latest | Three.js in React |
| @react-three/drei | latest | Three.js helpers |
| shadcn/ui | latest | UI components |
| React Router | 6 | Routing |
| @tanstack/react-query | 5 | Data fetching |

---

## 🧩 Sections Overview

| Section | File | Key Feature |
|---------|------|-------------|
| Hero | `Hero.tsx` | 3D scroll-driven dumbbell, parallax cards |
| About | `About.tsx` | Stats, promises, Salem tagline |
| Programs | `Programs.tsx` | 4 cards with real photos + parallax |
| Pricing | `Pricing.tsx` | Real fee tables, Save % badge |
| Trainers | `Trainers.tsx` | Krishna profile with parallax photo |
| Transformation | `Transformation.tsx` | Carousel with zoom-focus + lightbox |
| Gallery | `Gallery.tsx` | 3 auto-moving rows, lightbox |
| Contact | `Contact.tsx` | Address, timings, Google Maps |
| Footer | `Footer.tsx` | Newsletter, links, social, WhatsApp FAB |

---

## 📱 Mobile Support

- Responsive on all screen sizes
- 3D dumbbell disabled on mobile (saves battery)
- Custom cursor disabled on touch devices
- Gallery switches to 2-col grid on mobile
- All buttons full-width on mobile

---

## 🔧 Customization Tips

### Parallax speed (Gallery)
```tsx
// src/components/sections/Gallery.tsx
const ROWS = [
  { speed: -0.5, ... },  // negative = left, positive = right
  { speed:  0.4, ... },  // increase number = faster
  { speed: -0.3, ... },
];
```

### 3D Dumbbell lighting
```tsx
// src/components/ScrollDumbbell.tsx
<pointLight position={[-4, -1.5, 4]} intensity={6.0} color="#ff1500" />
// increase intensity for brighter red glow
```

### Colors
```css
/* src/index.css */
--primary: 0 84% 45%;   /* red — change hue for different color */
```

---

## 📞 Gym Contact

| Info | Details |
|------|---------|
| **Name** | Raj Fitness Gym & Power Lifting |
| **Address** | 14, Bhuvana Complex, 2nd Floor, Balaji Nagar 335, TVK Road, Ammapettai, Salem - 636003 |
| **Phone** | 098425 46263 |
| **Trainer** | Master Trainer Krishna |
| **Google Rating** | 4.6★ (63 reviews) |
| **Established** | 2011 |

---

## 📄 License

Built exclusively for Raj Fitness, Ammapettai, Salem.  
© 2025 Raj Fitness. All rights reserved.
