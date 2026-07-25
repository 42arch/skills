# 42arch/skills

A collection of personal agent skills for AI coding assistants. Skills extend agent capabilities with specialized workflows, templates, and domain knowledge.

## Install a Skill

```bash
npx skills add 42arch/skills/<skill-name>
```

## Available Skills

### `app-starter`

Scaffolds a new project from a selection of templates in `vault42/app-starter`. This skill aggregates three subproject templates:
- **`nextjs-starter`**: Next.js 16 (App Router) + Tailwind CSS v4 + shadcn-ui + next-themes + next-intl (i18n) + PWA
- **`tauri-nextjs-starter`**: Tauri 2.0 (Rust) desktop app with Next.js 16 frontend, Tailwind CSS v4, and shadcn-ui
- **`vite-react-starter`**: React 19 + Vite 8 + Tailwind CSS v4 + shadcn-ui + React Router v8

**Triggers when:** User wants to start a new web, desktop, Next.js, Tauri, or React project, or specifically asks to use the `app-starter` template.

```bash
npx skills add 42arch/skills/app-starter
```

---

## About Skills

Each skill lives in its own directory and contains:

- **`SKILL.md`** — Skill metadata (name, description) and step-by-step workflow instructions for the agent
- **`template/`** *(optional)* — Project template files copied during scaffolding

Skills follow the [skills.sh](https://skills.sh/) open agent skills format and are compatible with `npx skills`.
