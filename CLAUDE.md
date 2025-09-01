# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev theme called "joyful-theme" - a presentation theme for the Slidev framework. Slidev is a slide maker and presentation tool for developers that uses Markdown for content and Vue.js for theming.

## Commands

Development commands (use `nr` to run scripts):
- `nr dev` - Start development server with live preview of example.md
- `nr build` - Build the presentation (uses example.md)
- `nr export` - Export presentation to PDF
- `nr screenshot` - Export presentation as PNG images

Package management uses pnpm (pnpm-lock.yaml present).

Linting:
- ESLint configured with `@storyblok/eslint-config`
- Config in `eslint.config.mjs` with console logging allowed

## Architecture

### Theme Structure
- **layouts/** - Vue components defining slide layouts (intro.vue, cover.vue)
- **components/** - Reusable Vue components (TheHeader.vue, TheIsotype.vue)
- **styles/** - CSS styling (index.ts imports base layouts + custom layout.css)
- **setup/** - Slidev configuration (shiki.ts for syntax highlighting themes)
- **public/** - Static assets
- **example.md** - Development preview file demonstrating the theme

### Key Technologies
- **Slidev** (@slidev/cli, @slidev/types) - Presentation framework
- **Vue.js** - Component framework (layouts and components are .vue files)
- **UnoCSS** - Utility-first CSS framework (basic config in unocss.config.ts)
- **Vite** - Build tool with SVG loader plugin
- **Shiki** - Syntax highlighting (configured for vitesse themes)

### Development Workflow
The theme is developed by editing layouts, components, and styles while previewing changes in example.md. The theme inherits base Slidev layouts and can be customized by removing the base import in styles/index.ts.

### Theme Configuration
Package.json includes slidev config with colorSchema: "both" and default fonts (Roboto sans, Fira Code mono). Theme supports both light and dark modes.