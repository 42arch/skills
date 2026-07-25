---
name: app-starter
description: "Use this skill to scaffold a new project using templates from vault42/app-starter. This skill supports three subproject templates: nextjs-starter (Next.js web application), tauri-nextjs-starter (Tauri desktop application), and vite-react-starter (Vite + React web application). Trigger this when the user wants to start a new web app, desktop app, Next.js app, Tauri desktop app, React application, or asks to use the app-starter template."
---

# app-starter

This skill scaffolds a modern, production-ready application using one of the templates in the `vault42/app-starter` repository:
- **`nextjs-starter`**: Next.js 16 (App Router), Tailwind CSS v4, shadcn-ui, next-themes, next-intl (i18n), and PWA.
- **`tauri-nextjs-starter`**: Tauri 2.0 (Rust) desktop app with Next.js 16 (App Router) frontend, Tailwind CSS v4, and shadcn-ui.
- **`vite-react-starter`**: React 19, Vite 8, Tailwind CSS v4, shadcn-ui, and React Router v8.

## Workflow

1.  **Ask for User Template Choice**:
    First, present the three template options to the user and ask which one they want to scaffold:
    1. **Next.js Starter (nextjs-starter)**
    2. **Tauri Next.js Starter (tauri-nextjs-starter)**
    3. **Vite React Starter (vite-react-starter)**

2.  **Initialize Project Directory**:
    Check if the current working directory is empty:
    - **Empty**: Use it directly as the project root.
    - **Not empty**: Inform the user and ask them to provide a project name. Create a new subdirectory and enter it:
      ```bash
      mkdir <project-name> && cd <project-name>
      ```

3.  **Apply Chosen Template**:
    Use `degit` to pull the specific starter template into the current directory (no git history). Then, **remove the `.github` folder** to ensure a clean start:
    - For **nextjs-starter**:
      ```bash
      pnpm dlx degit vault42/app-starter/nextjs-starter .
      rm -rf .github
      ```
    - For **tauri-nextjs-starter**:
      ```bash
      pnpm dlx degit vault42/app-starter/tauri-nextjs-starter .
      rm -rf .github
      ```
    - For **vite-react-starter**:
      ```bash
      pnpm dlx degit vault42/app-starter/vite-react-starter .
      rm -rf .github
      ```

4.  **Update Project Information**:
    Update the project name in the files relevant to the chosen template:
    - **nextjs-starter**:
      - `package.json`: Update the `"name"` field to `<project-name>`.
    - **tauri-nextjs-starter**:
      - `package.json`: Update the `"name"` field to `<project-name>`.
      - `src-tauri/tauri.conf.json`: Update `"productName"` to `<project-name>` and `"identifier"` to `com.example.<project-name>` (or similar unique identifier).
      - `src-tauri/Cargo.toml`: Update the `[package]` name.
    - **vite-react-starter**:
      - `package.json`: Update the `"name"` field to `<project-name>`.

5.  **Install Dependencies**:
    Run `pnpm install` in the project directory.

6.  **Verification**:
    Run `pnpm lint` to ensure the project is correctly configured and passes all linting rules.

7.  **Final Steps**:
    Provide the user with a summary of the tech stack and the commands to start development:
    - **nextjs-starter**:
      - `pnpm dev`: Start Next.js development server.
    - **tauri-nextjs-starter**:
      - `pnpm tauri dev`: Start the desktop development environment.
      - `pnpm dev`: Start the web-only Next.js development server.
    - **vite-react-starter**:
      - `pnpm dev`: Start Vite development server.
