# Role and Goal
You are an Expert Frontend Developer with deep knowledge of HTML5, Tailwind CSS, and modern UI/UX principles.
Your task is to build a single-page Landing Page (Smoke Test / Waitlist) for a French B2B SaaS targeting "Mandataires Automobiles" (Car Brokers).

# Tech Stack
- Single HTML file.
- Tailwind CSS (via CDN: `<script src="https://cdn.tailwindcss.com"></script>`).
- Tailwind config customization inside the `<script>` tag to add custom colors.
- Google Fonts (Inter).
- Lucide Icons (via CDN: `<script src="https://unpkg.com/lucide@latest"></script>`).

# Design System
- **Background:** Dark Mode Automotive (`bg-slate-900` with a subtle radial gradient `bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-slate-800 via-slate-900 to-black`).
- **Primary Color (Brand):** Slate Blue (Tailwind `blue-600` to `blue-500` for hovers).
- **Accent Color (Warnings/CTA):** Cyber Orange (Tailwind `amber-500`).
- **Typography:** 'Inter', sans-serif. Headings should be bold and geometric. Text should be highly readable.
- **Vibe:** Sleek, premium, glassmorphism elements, high-end car dashboard feel.

# Page Layout & French Copy

## 1. Navbar (Simple)
- Logo text: "AutoMarge Pro" (font-bold, text-xl, text-white).
- Right side: Minimal "Contact" link.

## 2. Hero Section
- **Layout:** Split-screen 60/40 on desktop (flex-col on mobile).
- **Left Column (Text):**
  - **Badge:** Small pill shape with an amber dot and text: "Nouveau Malus 2026 inclus" (border border-slate-700, text-slate-300).
  - **H1:** `Importez sans stress : Le coût de revient réel sur mobile.de, instantanément.` (text-4xl or 5xl, font-extrabold, text-white, leading-tight).
  - **H2:** `Plus besoin d'Excel. Notre extension Chrome calcule automatiquement le Malus Écologique 2026 (CO2 + Poids), le transport et votre marge directement sur l'annonce.` (text-lg, text-slate-400, mt-4).
  - **CTA Button:** `Rejoindre la Bêta Privée` (bg-blue-600 hover:bg-blue-500, text-white, px-6 py-3, rounded-lg, font-semibold, mt-8, with an arrow icon).
- **Right Column (Visual):**
  - Create a "Glassmorphism" floating card using Tailwind (`bg-white/10 backdrop-blur-md border border-white/20 rounded-xl p-6 shadow-2xl`).
  - Inside this card, build a mockup of our Chrome Extension Widget using the exact data provided below.

## 3. The "Aha!" Moment (The Widget Mockup Data)
*Build this purely in HTML/Tailwind inside the right column of the Hero section. It should look like a sleek pricing calculator panel.*

- **Header:** "Audi Q5 40 TDI S-line (2024)" (text-sm, text-slate-400)
- **Data Rows (flex, justify-between, py-2, border-b border-slate-700/50):**
  - Prix Net (Allemagne) : **45 000 €**
  - Transport (Munich → Toulouse) : **850 €**
  - Malus CO2 (175g/km) : **<span class="text-amber-500">6 050 €</span>**
  - Malus Masse (1950 kg) : **<span class="text-amber-500">3 500 €</span>**
  - Marge Mandataire : **2 000 €**
- **Total Row (mt-4, pt-4, border-t-2 border-slate-600):**
  - Prix Final Client (TTC) : **<span class="text-white text-2xl font-bold">57 400 €</span>**

## 4. Three Key Benefits (Features Section)
- **Layout:** Grid with 3 columns (`grid-cols-1 md:grid-cols-3 gap-8 mt-24 max-w-6xl mx-auto px-4`).
- **Cards:** Dark cards (`bg-slate-800/50 border border-slate-700 rounded-xl p-6 hover:border-blue-500 transition-colors`).
- **Card 1:**
  - Icon: Shield (Lucide). Color: Blue.
  - Title: `Malus 2026 certifié`
  - Text: `Calcul ultra-précis incluant les taxes CO2 et le malus masse (poids), mis à jour en temps réel.`
- **Card 2:**
  - Icon: Calculator (Lucide). Color: Green.
  - Title: `Calculateur de Marge`
  - Text: `Définissez vos frais de courtage et visualisez instantanément votre bénéfice net sur chaque véhicule.`
- **Card 3:**
  - Icon: Zap (Lucide). Color: Amber.
  - Title: `Gain de Temps : -15 min`
  - Text: `Ne quittez plus votre navigateur. Toutes les données critiques s'affichent là où vous travaillez.`

## 5. Bottom CTA (Lead Capture)
- **Layout:** Centered block with a gradient border (`max-w-3xl mx-auto mt-24 mb-24 p-12 bg-slate-800/80 rounded-2xl text-center border border-slate-700`).
- **Heading:** `Prêt à automatiser votre sourcing ?` (text-3xl font-bold text-white).
- **Sub-heading:** `Rejoignez les 50 premiers mandataires pour un accès anticipé à l'outil.` (text-slate-400 mt-2).
- **Form Layout:** Flex row (input + button) on desktop, flex col on mobile.
- **Input:** Placeholder `votre@email-professionnel.fr` (bg-slate-900 border border-slate-600 text-white px-4 py-3 rounded-l-lg md:w-96 focus:outline-none focus:border-blue-500).
- **Button:** `Obtenir mon accès prioritaire` (bg-blue-600 text-white px-6 py-3 rounded-r-lg font-semibold hover:bg-blue-500).
- **Footer Text:** `🔒 Zéro spam. Uniquement les accès pour la bêta.` (text-xs text-slate-500 mt-4).

# Deliverable
Return ONLY the complete HTML code. Do not include markdown formatting around the HTML, just the pure valid HTML code ready to be pasted into an index.html file. Make sure the Lucide icons are initialized via script at the end of the body.

