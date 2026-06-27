# Makfolio

![Makfolio Banner](/favicon.svg)

Makfolio is a high-performance portfolio and publishing system for Mirza Kaiyum (Product / Full Stack Engineer). It serves as both a curated showcase for projects and a content engine for long-form writings.

## Overview

The site is designed to keep runtime JavaScript minimal while still feeling dynamic and interactive. Astro handles content-driven SSR pages, while targeted client-side behavior powers infinite pagination and smooth reading ergonomics.

## Technical Stack

- **Framework**: Astro v6 (SSR)
- **Adapters**: Cloudflare, Vercel, and Netlify adapters are included
- **Styling**: Tailwind CSS v4 with `@tailwindcss/typography`
- **Motion**: `motion` for lightweight scroll interactions
- **Content Layer**: Astro Content Collections with schema validation
- **Tooling**: Wrangler for Cloudflare types

## Key Features

1. **Window-in-Window Layout**: A brutalist-inspired, nested shell layout that scales across sections.
2. **Infinite Scroll Pagination**: Uses Astro partial endpoints (`text/html`) and `IntersectionObserver` to progressively hydrate lists without heavy bundles.
3. **Dynamic Headings + Sticky TOC**: Extracted markdown headings feed a structured, sticky table of contents.
4. **Smart External Link Detection**: Content entries can map to external URLs and display normalized host labels (for example, `medium.com`).
5. **Tailwind Typography Controls**: Fine-tuned prose hierarchy and spacing for long-form reading.

## Getting Started

### Requirements

- Node.js `>=22.12.0`
- npm

### Install and Run

| Command | Action |
| :------ | :----- |
| `npm install` | Install dependencies |
| `npm run dev` | Start local development server |
| `npm run build` | Build production output |
| `npm run preview` | Preview the production build locally |
| `npm run generate-types` | Regenerate Wrangler/Cloudflare runtime types |
| `npx astro sync` | Refresh Astro content typings after moving/removing content files |

## Project Structure

- `/src/pages`: Route entry points, including index pages and dynamic `[slug].astro` routes.
- `/src/pages/partials`: Lightweight HTML partial endpoints used by infinite loading flows.
- `/src/content/projects`: Markdown project content rendered in the projects archive.
- `/src/content/writings`: Markdown writings rendered in the writings archive.
- `/src/content.config.ts`: Central schema definitions and content validation rules.

## Notes

This project began from a standard Astro setup and was extensively customized for performance, typography, and scalable content workflows.
