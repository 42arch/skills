---
name: tauri-starter
description: Use this skill to scaffold a new Tauri 2.0 desktop application using a Next.js 16 starter template. Trigger this when the user wants to start a "tauri app", "desktop app", or asks for a Tauri + Next.js + Tailwind CSS project.
---

# tauri-starter

This skill scaffolds a modern, production-ready Tauri 2.0 desktop application using Next.js 16 (App Router), Tailwind CSS v4, shadcn-ui, and a robust Rust-based backend.

## Tech Stack
- **Desktop Framework**: Tauri 2.0 (Rust)
- **Frontend Framework**: Next.js 16 (App Router)
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn-ui
- **Icons**: Phosphor Icons
- **Theme**: next-themes (Dark mode support)
- **Linting**: @antfu/eslint-config
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
    Use `degit` to pull the starter template into the current directory (no git history). Then, **remove the `.github/dependabot.yml` file and the `.github` folder** to ensure a clean start:
    ```bash
    pnpm dlx degit vault42/tauri-nextjs-starter .
    rm -rf .github
    ```

3.  **Update Project Information**:
    Update the project name in the following files:
    - `package.json`: Update the `"name"` field.
    - `src-tauri/tauri.conf.json`: Update `"productName"` and `"identifier"` (e.g., `com.example.<project-name>`).
    - `src-tauri/Cargo.toml`: Update the `[package]` name.

4.  **Install Dependencies**:
    Run `pnpm install` in the project directory.

5.  **Verification**:
    Run `pnpm lint` to ensure the project is correctly configured.

6.  **Final Steps**:
    Provide the user with a summary of the tech stack and the commands to start development:
    - `pnpm tauri dev`: Start the desktop development environment.
    - `pnpm dev`: Start the web-only development server.
