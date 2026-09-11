# Lithos - Interactive Geology Hero Section

A full-screen, dark-themed hero section for a geology brand with a cursor-following spotlight reveal effect.

## Tech Stack
- **React 18** + **TypeScript**
- **Vite** for fast development and building
- **Tailwind CSS** for styling
- **Lucide React** for icons
- **Inter** and **Playfair Display** fonts

## Features
- Cursor-following spotlight that reveals a second image through a soft circular mask
- Smooth animation on load with staggered text reveals
- Responsive design (mobile, tablet, desktop)
- Fixed navigation with logo and menu
- Premium animations with reduced motion support

## Getting Started

### Installation
```bash
npm install
```

### Development
```bash
npm run dev
```

### Build
```bash
npm run build
```

### Preview
```bash
npm run preview
```

## Project Structure
```
src/
├── components/
│   ├── Hero.tsx          # Main hero section component
│   └── RevealLayer.tsx   # Cursor-following spotlight mask component
├── App.tsx               # Root app component
├── main.tsx              # Entry point
└── index.css             # Global styles and animations
```

## Key Technical Details

### Spotlight Reveal Mechanic
- Mouse position is tracked and smoothly eased via `requestAnimationFrame`
- A canvas element draws a radial gradient at the cursor position
- The gradient is converted to a data URL and applied as a CSS mask
- This creates a soft, glowing circular reveal of the second image

### Animation Timeline
- Base image: Ken Burns zoom-out (1.8s)
- Heading line 1: Blur reveal at 0.25s
- Heading line 2: Blur reveal at 0.42s
- Bottom-left text: Fade up at 0.7s
- Bottom-right text: Fade up at 0.85s

## Browser Support
- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support (with -webkit- mask prefixes)
- Mobile: Optimized with `100dvh` for mobile browser chrome handling
