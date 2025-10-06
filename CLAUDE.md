# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Vue 3 + Vite demo project showcasing Vue template syntax and component development. Uses **both Composition API and Options API patterns** side-by-side (with commented-out alternatives for learning purposes). Integrates Element Plus (desktop) and Vant (mobile) UI frameworks, and includes UnicornStudio for animated backgrounds.

**Tech Stack:**
- Vue 3 (Composition API & Options API)
- Vite 7.x
- Pinia (state management)
- Element Plus (desktop UI)
- Vant (mobile UI)
- Axios (HTTP client)
- UnicornStudio (background animations via CDN)
- ESLint + Prettier

## Development Commands

```bash
# Install dependencies
npm install

# Start dev server (default: http://localhost:5173)
npm run dev

# Build for production (outputs to dist/)
npm run build

# Preview production build
npm run preview
```

## Project Architecture

### Application Entry Point
- **index.html**: Loads UnicornStudio CDN script globally for background animations
- **main.js**: Creates Vue app instance and mounts to `#app` (NO router registered here currently)
- **App.vue**: Root component that imports BackgroundEffect and Home components directly (no router-view)

### Component Hierarchy
```
App.vue (root)
├── BackgroundEffect.vue (fixed background layer)
└── Home.vue (main content, delayed 2s display)
    ├── MobanYufa.vue (template syntax demo)
    ├── Shuxingbangding.vue (attribute binding examples)
    ├── Tiaojianxuanran.vue (conditional rendering)
    ├── Libiaoxuanran.vue (list rendering)
    ├── Keyguanlizhuangtai.vue (state management)
    ├── Shijianchuli.vue (event handling)
    ├── Shijianchuancan.vue (event parameter passing)
    └── Eventdemo.vue (event examples)
```

### File Structure
```
src/
├── components/
│   ├── BackgroundEffect.vue       # UnicornStudio animated background (Composition API)
│   ├── mobanyufa.vue              # Template syntax demo (Options API + commented Composition API)
│   ├── shuxingbangding.vue        # Attribute binding examples
│   ├── tiaojianxuanran.vue        # Conditional rendering
│   ├── libiaoxuanran.vue          # List rendering
│   ├── keyguanlizhuangtai.vue     # State management patterns
│   ├── shijianchuli.vue           # Event handling
│   ├── shijianchuancan.vue        # Event parameter passing
│   └── eventdemo.vue              # Event examples
├── views/
│   └── home.vue                   # Home page with 2s delayed display (Options API + commented Composition API)
├── router/
│   └── index.js                   # Empty router file (not configured or used)
└── style.css                      # Global styles
```

### Dual API Pattern Convention

**IMPORTANT**: Components contain both Options API (active) and Composition API (commented) for educational purposes:

```vue
<!-- Options API (active) -->
<script>
export default {
  components: { MobanYufa }
}
</script>

<!-- Composition API (commented reference) -->
<!-- <script setup>
import MobanYufa from '../components/mobanyufa.vue'
</script> -->
```

When modifying components, **preserve both versions** unless explicitly asked to switch.

### Component Patterns
- **Options API**: Currently active in App.vue, home.vue, mobanyufa.vue
- **Composition API**: Used in BackgroundEffect.vue; commented alternatives in other files
- **Component Imports**: Use relative paths (e.g., `../components/mobanyufa.vue`); `@/` alias NOT configured in vite.config.js
- **Background Integration**: BackgroundEffect.vue uses `onMounted` to initialize UnicornStudio after DOM loads

## Key Conventions

1. **No Active Router**: `src/router/index.js` is essentially empty (1 line); main.js does NOT call `.use(router)`; App.vue directly imports components instead of using `<router-view>`
2. **Delayed Content Display**: home.vue uses a 2-second `setTimeout` in `mounted()` hook before showing content (`showContent` state) to allow background animation to load
3. **UnicornStudio Integration**: Loaded via CDN in index.html; initialized in BackgroundEffect.vue's onMounted hook with project ID `BqS5vTHVEpn6NiF0g8iJ`
4. **Educational Code Comments**: Preserve commented-out Composition API examples in files for learning reference; this is a teaching project demonstrating both API styles

## Architecture Notes

- **No router currently active**: Router file is empty; components are directly imported in App.vue
- **Z-index layering**: BackgroundEffect (z-index: 0-1) → Home container (z-index: 10) → Home heading (z-index: 11)
- **Background rendering**: BackgroundEffect uses fixed positioning (`position: fixed`) with CSS gradient overlay and UnicornStudio animation layer
- **Async initialization**: UnicornStudio script loads via CDN; BackgroundEffect.vue polls for `window.UnicornStudio` availability before init
- **Dark theme**: App.vue has dark background (`background-color: #000`) to complement animated background; home.vue content appears white on dark
