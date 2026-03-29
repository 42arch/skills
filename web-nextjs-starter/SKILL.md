---
name: web-nextjs-starter
description: Use this skill to scaffold a new Next.js project with TypeScript, Tailwind CSS, shadcn-ui, and strict ESLint rules. Trigger this when the user wants to start a new web project or "web app".
---

# web-nextjs-starter

This skill scaffolds a modern web application with a standardized configuration.

## Workflow

1.  **Initialize Next.js**:
    Run the following command to create a new Next.js project:
    `npx create-next-app@latest <project-name> --typescript --tailwind --eslint --app --src-dir --import-alias "@/*" --use-npm`

2.  **Apply Custom Configurations**:
    Overwrite the following files in the newly created project using the templates provided in the skill's `templates/` directory:
    - `next.config.mjs`
    - `tailwind.config.ts`
    - `eslint.config.mjs`
    - `components.json`
    - `src/app/globals.css`

3.  **Initialize shadcn-ui**:
    The `components.json` and `globals.css` templates will pre-configure shadcn-ui. No additional `init` command is required if the templates are correctly applied.

4.  **Verification**:
    Run `npm run lint` in the project directory to ensure everything is set up correctly.
