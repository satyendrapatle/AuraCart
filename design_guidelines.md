# Design Guidelines: AI-Powered Futuristic E-Commerce Platform

## Design Approach
**Reference-Based Approach** drawing from Apple's minimalist precision, Tesla's futuristic aesthetic, and premium e-commerce platforms like Net-a-Porter and SSENSE. The design combines luxurious simplicity with cutting-edge technology presentation.

**Core Principles:**
- Futuristic minimalism with purposeful negative space
- Technology-forward interactions with subtle micro-animations
- Premium brand perception through restrained elegance
- AI-first experience with seamless human-machine interaction

## Color Palette

### Dark Mode Foundation (Primary)
- **Background Base**: 217 19% 12% (deep charcoal)
- **Surface Elevated**: 217 19% 16% (cards, panels)
- **Surface Highest**: 217 15% 20% (modals, overlays)

### Neon Accent System
- **Primary Glow**: 237 100% 70% (electric blue - CTAs, active states)
- **Secondary Glow**: 270 95% 75% (neon purple - highlights, badges)
- **Success Glow**: 166 70% 65% (cyan - confirmations)
- **Text Primary**: 0 0% 95% (near-white for headings)
- **Text Secondary**: 217 10% 65% (muted for body text)

### Gradient Applications
Use sparingly for maximum impact on hero sections, CTAs, and AI assistant panels:
- Primary gradient: `from-[237 100% 70%] via-[270 95% 75%] to-[237 100% 70%]`
- Glow effects: Apply `blur-xl opacity-50` overlays behind key elements

## Typography

**Font Stack:**
- **Primary**: Inter (via Google Fonts) - clean, modern, tech-forward
- **Accent**: Lexend (via Google Fonts) - futuristic headlines

**Scale:**
- Hero Display: text-6xl md:text-7xl lg:text-8xl font-bold tracking-tight
- Section Headers: text-3xl md:text-4xl lg:text-5xl font-semibold
- Product Titles: text-xl md:text-2xl font-medium
- Body Text: text-base leading-relaxed
- UI Elements: text-sm font-medium

## Layout System

**Spacing Primitives:** Use Tailwind units of **2, 4, 6, 8, 12, 16, 20, 24** for consistent rhythm.

**Container Strategy:**
- Full-width hero: w-full with inner max-w-7xl mx-auto
- Content sections: max-w-7xl mx-auto px-4 md:px-6 lg:px-8
- Product grids: gap-6 md:gap-8
- Vertical rhythm: py-16 md:py-20 lg:py-24 between sections

**Grid Systems:**
- Hero: Asymmetric 2-column (7-5 ratio on desktop, stack on mobile)
- Products: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4
- Features: grid-cols-1 md:grid-cols-3 with equal columns

## Component Library

### Navigation
Glass-morphism header with backdrop-blur-lg, border-b border-white/10, sticky positioning. Logo left, search center, cart/profile right with neon glow badges.

### Hero Section
Full-viewport height with animated gradient background, 3D product showcase or animated mesh gradient, AI-powered personalization tagline, dual CTAs (primary glow button + ghost outline).

### Product Cards
Elevated cards (bg-surface elevated) with hover lift effect (translate-y-[-4px]), product image with subtle zoom on hover, quick-add-to-cart overlay fade-in, AI suggestion badge with neon glow, rating stars with gradient fill.

### AI Assistant Chat
Fixed bottom-right floating bubble with pulsing glow animation, expanding chat panel (400px width) with glass-morphism backdrop, message bubbles with gradient backgrounds for AI vs user, typing indicator with animated dots, voice input button with waveform visualization.

### Shopping Cart
Slide-in drawer from right (w-full md:w-96), glass panel with blur, product mini-cards with quantity steppers, live price calculation with smooth number transitions, GPT assistant suggestion panel for related items, checkout CTA with gradient fill.

### Product Page
Split layout: 60% image gallery (with 360° viewer), 40% details panel, AI styling tips card with neon border, size/color selectors with glow on active, add-to-cart sticky on mobile.

### Search & Filters
Overlay search with backdrop blur, autocomplete dropdown with product previews, filter sidebar with checkbox groups, active filters as dismissible pills with neon borders.

### User Dashboard
Card-based layout with order timeline visualization, loyalty points with animated progress bars, AI insights panel showing personalized recommendations, order tracking with real-time status updates.

## Animation Guidelines

**Micro-interactions (60fps target):**
- Button hovers: scale-[1.02] with glow expansion
- Card hovers: translate-y-[-4px] with shadow-2xl shadow-primary/20
- Page transitions: fade + slide combinations (150-200ms)
- AI assistant: typing indicator, message fade-in, status pulsing

**Hero Animations:**
- Gradient mesh: slow drift animation (20s loop)
- Product showcase: gentle float + rotate on 3D axis
- Text: staggered fade-in from bottom

**Prohibited:** Avoid excessive spinning, bouncing, or aggressive animations that distract from content.

## Images

### Hero Section
**Large Hero Image/Video**: YES - Full-width immersive product showcase or abstract tech visualization (mesh gradients, particles, or 3D rendered products). Aspect ratio: 16:9 on desktop, 4:3 on mobile. Apply subtle parallax scroll effect.

### Product Images
High-quality product photography on transparent or gradient backgrounds. Include 360° interactive viewer with scrubbing controls. Lightbox zoom on click with smooth scale transition.

### Category Banners
Full-width imagery for category pages (1920x600px) with gradient overlays for text legibility.

### Trust Elements
Customer photos in testimonials (circular masks with neon borders), brand logos in partnership section (grayscale with glow on hover).

## Accessibility & Polish

- Maintain WCAG AAA contrast ratios despite dark theme (text primary at 95% lightness)
- Focus states: 2px neon glow ring on all interactive elements
- Loading states: skeleton screens with shimmer gradients
- Error states: subtle red glow (0 85% 65%) with shake animation
- Success states: cyan glow with checkmark fade-in

**Glass-morphism Formula:**
`backdrop-blur-lg bg-white/5 border border-white/10`

This creates the signature futuristic aesthetic across all elevated surfaces.