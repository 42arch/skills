---
name: web-nextjs-starter
description: Use this skill to scaffold a new Next.js project using a pre-defined production-grade template. Trigger this when the user wants to start a new web project, "web app", or specifically asks for a Next.js 16/Tailwind v4 starter with dark mode/theme support, PWA and i18n.
---

# web-nextjs-starter

This skill scaffolds a modern, high-performance web application based on a custom Next.js 16 template with Tailwind CSS v4, shadcn-ui (v4), next-themes (dark mode), i18n and PWA support.

## Tech Stack
- **Framework**: Next.js v16 (App Router)
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn-ui (radix-lyra style)
- **Icons**: Phosphor Icons (v2 with Icon suffix convention)
- **Theme**: next-themes (Light/Dark/System support)
- **Linting**: @antfu/eslint-config (strict mode)
- **i18n**: next-intl
- **Package Manager**: pnpm

## Workflow

1.  **Initialize Project Directory**:
    Check if the current working directory is empty:
    - **Empty**: Use it directly as the project root.
    - **Not empty**: Inform the user and ask them to provide a project name. Create a new subdirectory and enter it:
      ```bash
      mkdir <project-name> && cd <project-name>
      ```

2.  **Apply Template**:
    Use `degit` to pull the starter template into the current directory (no git history). Then, **remove the `.github` folder** to ensure a clean start, and update the `package.json` `"name"` field to the new project name:
    ```bash
    pnpm dlx degit vault42/nextjs-starter .
    rm -rf .github
    ```

3.  **Install Dependencies**:
    Run `pnpm install` in the project directory to install dependencies and ensure the lockfile is respected.

4.  **Verification**:
    Run `pnpm lint` to ensure the project is correctly configured and passes all linting rules.

5.  **Final Steps**:
    Provide the user with a summary of the tech stack and the command to start development (`pnpm dev`).
