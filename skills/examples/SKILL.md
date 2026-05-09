---
name: examples
description: |
  Where to find example conscript studies by pattern. Reads repo paths
  from study-config.md.
user-invocable: false
---

Read `study-config.md` in the project root for example repo paths.

## Built-in congame examples

In the congame repo under `conscript/examples/`:

| File | Pattern |
|------|---------|
| `kitchen-sink.rkt` | Full flow, forms, consent branching, nested study |
| `form.rkt` | Minimal form with text + textarea |
| `tutorial.rkt` (in `congame-doc/conscript-examples/`) | Simple survey with variable interpolation |

## Pattern index

| Pattern | Search for |
|---------|-----------|
| Looping over rounds | `add1 rounds` |
| Treatment assignment | `shuffle` or `assigning-treatments` |
| Branching on treatment | `if competition?` |
| Matchmaking | `make-matchmaker` |
| Wait pages | `refresh-every` |
| Bot testing | `make-bot-model` |
| Autofill metadata | `make-autofill-meta` |

Search in congame examples first, then project-specific studies, then
other repos listed in `study-config.md`.
