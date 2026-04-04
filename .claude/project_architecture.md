# Project Architecture

## Directory Structure
```
herelpt/
  index.html          - Homepage (video hero + parallax)
  about.html           - Mission, conditions, techniques, clinic gallery
  why-us.html          - 4 pillars, results section
  team.html            - Dr. Phil bio, team cards
  patient-info.html    - FAQ accordion, what to bring, intake forms
  optimize.html        - Seek Coffee, Fullscript, CellCore partnerships
  contact.html         - Contact form, info card, Google Maps embed
  css/
    style.css          - All styles (single file)
  js/
    main.js            - Mobile menu, sticky nav, FAQ accordion, contact form
  images/
    *.webp             - All images (downloaded from Squarespace CDN)
    hero-video.mp4     - Cropped trail video (unused - switched back to CloudFront)
    hero-video-v2.mp4  - Another crop attempt (unused)
  .claude/
    MEMORY.md          - This index
    *.md               - Memory files
```

## Page Structure (every page)
1. Topbar (announcement bar) - NOT on homepage (homepage has video nav)
2. Nav (sticky) - NOT on homepage (homepage has transparent video nav)
3. Page hero (dark overlay on image)
4. Content sections
5. Footer (dark, 4-column grid)

## Homepage Special
- Video hero with parallax (position: fixed)
- Transparent nav with backdrop blur bar
- Badge component (glassmorphism)
- Fustat font headline
- No topbar/announcement bar

## CSS Architecture
- Single file: css/style.css
- CSS custom properties for colors/spacing
- Component classes: .card, .testimonial, .tag, .partner, .team-card
- Layout: .grid, .grid-2, .grid-3, .grid-4, .grid-2-asym
- Sections: .section, .section-alt, .section-dark, .section-primary
- No CSS framework (no Tailwind, no Bootstrap)

## Fonts
- Headlines: Fustat 700 (loaded via Google Fonts)
- Body: Schibsted Grotesk 400-700
- Testimonial names: Caveat (handwritten)
- Hero-specific: also loads Inter, Noto Sans (from original hero spec)
