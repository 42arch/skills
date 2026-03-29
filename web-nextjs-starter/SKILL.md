---
name: web-nextjs-starter
description: Use this skill to scaffold a new Next.js project using a pre-defined production-grade template. Trigger this when the user wants to start a new web project, "web app", or specifically asks for a Next.js 16/Tailwind v4 starter with dark mode/theme support.
---

# web-nextjs-starter

This skill scaffolds a modern, high-performance web application based on a custom Next.js 16 template with Tailwind CSS v4, shadcn-ui (v4), next-themes (dark mode), and a strict ESLint configuration.

## Tech Stack
- **Framework**: Next.js 16.2.1 (App Router)
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn-ui (radix-lyra style)
- **Icons**: Phosphor Icons (v2 with Icon suffix convention)
- **Theme**: next-themes (Light/Dark/System support)
- **Linting**: @antfu/eslint-config (strict mode)
- **Package Manager**: pnpm

## Workflow

1.  **Initialize Project Directory**:
    Create a new directory for the project using the name provided by the user.

2.  **Apply Template**:
    Copy ALL contents from the skill's `template/` directory to the new project directory. This includes:
    - `package.json` (Update the `"name"` field to the new project name)
    - `components.json`
    - `eslint.config.mjs`
    - `next.config.ts`
    - `tsconfig.json`
    - `pnpm-lock.yaml` & `pnpm-workspace.yaml`
    - `src/` (Including `ThemeProvider` and `ModeToggle`)
    - `public/` (Static assets)

3.  **Install Dependencies**:
    Run `pnpm install` in the project directory to install dependencies and ensure the lockfile is respected.

4.  **Verification**:
    Run `pnpm lint` to ensure the project is correctly configured and passes all linting rules.

5.  **Final Steps**:
    - Remove any stray `.git` directories from the template copy.
    - Provide the user with a summary of the tech stack and the command to start development (`pnpm dev`).
