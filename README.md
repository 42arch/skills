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

**Tech stack:** Next.js 16 · Tailwind CSS v4 · shadcn-ui · next-themes · Phosphor Icons · pnpm

```bash
npx skills add 42arch/skills@web-nextjs-starter
```

---

## About Skills

Each skill lives in its own directory and contains:

- **`SKILL.md`** — Skill metadata (name, description) and step-by-step workflow instructions for the agent
- **`template/`** *(optional)* — Project template files copied during scaffolding

Skills follow the [skills.sh](https://skills.sh/) open agent skills format and are compatible with `npx skills`.
