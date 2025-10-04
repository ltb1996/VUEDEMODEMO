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
└── Home.vue (main content)
    └── MobanYufa.vue (template syntax demo)
```

### File Structure
```
src/
├── components/
│   ├── BackgroundEffect.vue    # UnicornStudio animated background (Composition API)
│   ├── mobanyufa.vue            # Template syntax demo (Options API + commented Composition API)
│   ├── shuxingbangding.vue      # Attribute binding examples (empty)
│   ├── tiaojianxuanran.vue      # Conditional rendering (empty)
│   ├── libiaoxuanran.vue        # List rendering (empty)
│   └── keyguanlizhuangtai.vue   # State management patterns (empty)
├── views/
│   └── home.vue                 # Home page (Options API + commented Composition API)
├── router/
│   └── index.js                 # Router config exists but NOT currently used in main.js
└── style.css                    # Global styles
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

1. **No Active Router**: Router config exists in `src/router/index.js` but main.js does NOT call `.use(router)`; App.vue directly imports components instead of using `<router-view>`
2. **UnicornStudio Integration**: Loaded via CDN in index.html; initialized in BackgroundEffect.vue's onMounted hook with project ID `BqS5vTHVEpn6NiF0g8iJ`
3. **Educational Code Comments**: Preserve commented-out Composition API examples in files for learning reference
4. **Empty Component Files**: Several components (shuxingbangding.vue, tiaojianxuanran.vue, etc.) are placeholders for future demos

## Architecture Notes

- **No router currently active** despite router files existing; components are directly imported
- BackgroundEffect uses fixed positioning (`position: fixed; z-index: 0`) to layer behind content
- UnicornStudio script loads asynchronously; component waits for `window.UnicornStudio` before init
- App.vue has dark theme styling (`background-color: #000`) to complement animated background
