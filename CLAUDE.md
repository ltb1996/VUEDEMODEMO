# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Vue 3 + Vite demo project showcasing Vue template syntax and component development. Uses both Composition API and Options API patterns. Integrates Element Plus (desktop) and Vant (mobile) UI frameworks, though primarily demonstrates core Vue functionality.

**Tech Stack:**
- Vue 3 (Composition API & Options API)
- Vite 7.x
- Vue Router 4.x
- Pinia (state management)
- Element Plus (desktop UI)
- Vant (mobile UI)
- Axios (HTTP client)
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
- **main.js**: Creates Vue app instance, registers router, and mounts to `#app`
- **App.vue**: Root component containing `<router-view>` for route rendering
- **src/router/index.js**: Vue Router configuration with web history mode

### File Structure
```
src/
├── components/        # Reusable Vue components
│   ├── mobanyufa.vue           # Template syntax demo (Options API)
│   ├── shuxingbangding.vue     # Attribute binding examples
│   ├── tiaojianxuanran.vue     # Conditional rendering
│   ├── libiaoxuanran.vue       # List rendering
│   └── keyguanlizhuangtai.vue  # State management patterns
├── views/             # Route-level components
│   └── home.vue       # Home page (imports MobanYufa component)
├── router/
│   └── index.js       # Route definitions
├── assets/            # Static assets (images, etc.)
└── style.css          # Global styles
```

### Component Patterns
- **Options API**: Used in existing components (mobanyufa.vue demonstrates this pattern)
- **Composition API**: Supported via `<script setup>` syntax
- **Scoped CSS**: Use scoped styles for component isolation
- **Component Imports**: Use `@/` alias for src directory (e.g., `@/components/...`)

## Key Conventions

1. **Router Configuration**: Routes defined in `src/router/index.js` using createWebHistory
2. **Component Registration**: Components imported and registered in parent components or views
3. **UI Framework Selection**: Project includes both Element Plus and Vant; choose appropriate framework based on target platform (desktop vs mobile)
4. **Code Style**: ESLint + Prettier configured (though config files not present, dependencies installed)

## Architecture Notes

- Router is registered globally in main.js via `.use(router)`
- App.vue serves as shell with router-view for navigation
- Home view acts as demo page importing example components
- Components demonstrate specific Vue concepts (template syntax, binding, rendering, state)
