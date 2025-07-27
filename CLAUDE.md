# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Structure

This is a Sanity CMS project with two main directories:
- `the-wellspring/` - Sanity Studio for content management (blog template)
- `bhsme-app/` - Sanity SDK-based React app

## Common Development Commands

### The Wellspring (Sanity Studio)
```bash
cd the-wellspring
pnpm dev          # Start development server
pnpm build        # Build for production
pnpm start        # Start production server
pnpm deploy       # Deploy to Sanity
```

### BHSME App
```bash
cd bhsme-app
pnpm dev          # Start development server
pnpm build        # Build for production
pnpm start        # Start production server
```

## Architecture Overview

### The Wellspring Studio
- **Schema Types**: Located in `the-wellspring/schemaTypes/`
  - `post.ts` - Blog post content type
  - `author.ts` - Author information
  - `category.ts` - Post categories
  - `blockContent.ts` - Rich text editor configuration
- **Configuration**: `sanity.config.ts` defines project ID `6evqhot7` and dataset `production`
- **Plugins**: Uses Structure Tool and Vision Tool for querying

### BHSME App
- **Entry Point**: `src/App.tsx` - React app using `@sanity/sdk-react`
- **Configuration**: `sanity.cli.ts` defines organization ID and entry point
- **Note**: The SanityConfig in App.tsx needs projectId and dataset to be configured

## Key Configuration Files

- Both projects use TypeScript with strict configuration
- Package manager: pnpm (based on pnpm-lock.yaml files)
- Prettier configuration in the-wellspring: no semicolons, single quotes, 100 char width