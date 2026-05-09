# Claude Conscript Plugin — Usage Guide

[Conscript](https://joeldueck.com/what-about/congame/Conscript.html) is
a DSL for authoring online experiments, built on the
[congame](https://github.com/MarcKaufmann/congame) framework. This
plugin teaches Claude how to write, review, and deploy Conscript studies.

## Setup

```bash
cd ~/projects/your-study-project
claude --plugin-dir ~/projects/claude-conscript-plugin
```

## Skills

| Skill | What it does |
|-------|-------------|
| `/create-study` | Generate a new study. On first run, asks about your project to create a `study-config.md` that persists your answers for all future runs. Then generates a `.rkt` file. |
| `/study-review` | QA an existing study against a checklist |
| `/upload` | Deploy a study to a congame server |

## Creating your first study

```
/create-study Participants see draws from an urn and report beliefs
```

On first run, Claude asks setup questions (research domain, typical
structure, where your congame repo is). This is one-time — answers are
saved to `study-config.md` so future runs skip straight to generation.

After setup, Claude generates a `.rkt` file with all required parts:
steps, forms, variables, study flow, CSS, and a `-with-admin` variant
(a wrapper that adds bot models for automated testing).

## Reviewing and uploading

```
/study-review studies/my-study.rkt
/upload my-study
```

## Key concepts for newcomers

- **Study:** A sequence of steps (pages) participants go through
- **Step:** One page — can show content, collect form input, or run logic
- **`-with-admin` variant:** Every study needs one. It wraps the study
  with bot models so you can test it without clicking through manually.
- **Bot models:** Automated test actors that fill forms and click buttons
