# 42arch/skills

A collection of personal agent skills for AI coding assistants. Skills extend agent capabilities with specialized workflows, templates, and domain knowledge.

## Install a Skill

```bash
npx skills add 42arch/skills/<skill-name>
```

## Available Skills

### `web-nextjs-starter`

Scaffolds a modern, production-grade Next.js web application from a pre-built template.

**Triggers when:** User wants to start a new web project or Next.js app.

**Tech stack:** Next.js 16 · Tailwind CSS v4 · shadcn-ui · next-themes · pnpm

```bash
npx skills add 42arch/skills/web-nextjs-starter
```

### `tauri-starter`

Scaffolds a production-ready Tauri 2.0 desktop application with a Next.js 16 frontend.

**Triggers when:** User wants to start a "tauri app", "desktop app", or asks for a Tauri + Next.js + Tailwind CSS project.

**Tech stack:** Tauri 2.0 (Rust) · Next.js 16 · Tailwind CSS v4 · shadcn-ui · pnpm

```bash
npx skills add 42arch/skills/tauri-starter
```

---

## About Skills

Each skill lives in its own directory and contains:

- **`SKILL.md`** — Skill metadata (name, description) and step-by-step workflow instructions for the agent
- **`template/`** *(optional)* — Project template files copied during scaffolding

Skills follow the [skills.sh](https://skills.sh/) open agent skills format and are compatible with `npx skills`.
