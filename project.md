# Edumim Vue.js Project Overview

## 1. Project Purpose
Edumim is a Vue.js 3.4+ template for online courses and education platforms. It is designed as a multipage, responsive, and modern web application, featuring attractive homepages, course listings, instructor profiles, events, blogs, and more.

## 2. Documentation Summary
- **Location:** `public/documentation/`
- **Entry Point:** `index.html`
- **Sections:**
  - Introduction
  - Development Environment Setup
  - Pages Info (with images)
  - Dependencies
  - Fonts Used
  - SCSS File Run Instructions
  - Credits (images, packages)
  - Support
- **Key Setup Steps:**
  - Install Node.js and npm
  - Install Vue CLI globally: `npm install -g @vue/cli`
  - Install dependencies: `npm install`
  - Run dev server: `npm run serve`
  - Build for production: `npm run build`
  - Lint: `npm run lint`

## 3. Project Structure
```
edumim/
├── public/
│   ├── documentation/         # HTML documentation, images, CSS, JS
│   ├── favicon.ico, .png      # Favicons
│   └── index.html             # Main HTML entry
├── src/
│   ├── App.vue                # Root Vue component
│   ├── main.ts                # App bootstrapper
│   ├── router/
│   │   └── index.ts           # Vue Router setup
│   ├── Pages/                 # Top-level pages (About, Home, Blog, Courses, etc.)
│   ├── components/            # All Vue components, organized by feature/page
│   ├── assets/
│   │   ├── css/               # CSS files (style, responsive, etc.)
│   │   ├── img/               # Images (logos, banners, icons, etc.)
│   │   ├── fonts/             # Font files
│   │   └── custom.scss        # Custom SCSS
│   └── shims-vue.d.ts         # TypeScript shims
├── package.json               # Project metadata, dependencies, scripts
├── README.md                  # Basic setup instructions
├── tsconfig.json              # TypeScript config
├── vue.config.js              # Vue CLI config
└── babel.config.js            # Babel config
```

## 4. Routing & Pages
- Uses Vue Router (`src/router/index.ts`)
- Main routes:
  - `/` (HomeOnePage)
  - `/home-two`, `/home-three`
  - `/about`, `/about-two`
  - `/instructor`, `/instructor-two`, `/instructor-details`
  - `/event`, `/event-details`
  - `/courses`, `/courses-list`, `/courses-sidebar`, `/courses-details`
  - `/blog`, `/blog-sidebar`, `/blog-standard`, `/blog-details`
  - `/contact`
  - Catch-all: ErrorPage
- Each page imports and composes feature-specific components from `src/components/`

## 5. Components
- Organized by feature/page (e.g., `HomeOne/`, `About/`, `Blog/`, `Layouts/`)
- Layout components: Navbar, Footer, PreLoader, BackToTop, etc.
- Feature components: AboutUs, TeamMembers, FunFacts, TestimonialContent, etc.

## 6. Styling
- Main styles in `src/assets/css/style.css` (imported in `main.ts`)
- Uses SCSS (`custom.scss`)
- Google Fonts (DM Sans by default)
- Bootstrap 5 and BootstrapVueNext for layout and UI

## 7. Dependencies
- **Core:**
  - `vue@^3.4.21`
  - `vue-router@^4.3.0`
  - `bootstrap@^5.3.3`
  - `bootstrap-vue-next@^0.7.3`
  - `vue3-carousel@^0.3.1`
- **Dev:**
  - TypeScript, ESLint, Babel, Sass, Vue CLI plugins

## 8. Assets
- Images, icons, and fonts are in `src/assets/img/`, `src/assets/fonts/`, and subfolders
- Logos in `src/assets/img/logo/`
- Social icons, SVGs, and banners are organized by type

## 9. Build & Run
- **Development:** `npm run serve` (hot reload at `localhost:8080`)
- **Production:** `npm run build`
- **Lint:** `npm run lint`

## 10. Customization
- All components are modular and can be edited or extended
- SCSS variables in `style.css` and `custom.scss` for easy theming
- Fonts can be changed in the CSS/SCSS

## 11. Support
- Email: mychannel4651@gmail.com
- More info in `public/documentation/index.html`

---

This file can be updated as the project evolves. Use it as a reference for onboarding, editing, or extending the Edumim Vue.js template. 