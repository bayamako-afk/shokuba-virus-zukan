# shokuba-virus-zukan

**Production system and story bible for the vertical short drama series _職場ウイルス図鑑_.**

## Repository purpose
This repository is the **production-control hub** for _職場ウイルス図鑑_. It is designed to manage the materials needed before video generation, including Season planning, episode development, virus naming, character management, reusable templates, and production logs.

The repository is not intended to store heavy video masters as a primary purpose. Instead, it functions as the **single source of truth** for planning, structure, operational rules, and repeatable production inputs.

## Current production policy
Season 1 is structured around **the discovery and naming of workplace anomalies**. Each episode should stop **before counterattack**, preserving the uneasy feeling of recognition rather than resolution. Mamoru Moriya is treated not as a fixed absolute protagonist, but as a **representative observer** who can lead some episodes and remain peripheral in others.

## Recommended repository structure
| Path | Role |
|---|---|
| `docs/design/` | Core design documents, Season structure, and production architecture |
| `docs/operations/` | Operating rules, completion declarations, and control memos |
| `registry/` | Virus registry, character registry, and other canonical ledgers |
| `templates/` | Reusable templates for episode sheets, prompts, reviews, and asset tracking |
| `episodes/season1/` | Episode-by-episode working inputs for Season 1 |
| `production_logs/` | Review logs, release notes, and promotion decisions |
| `assets/reference/` | Lightweight reference assets and linked asset notes only |

## Initial workflow
The intended working order is simple. First, update the core design and operating rules in `docs/`. Second, maintain naming and role consistency in `registry/`. Third, create and refine each episode input in `episodes/season1/`. Fourth, store post-release observations in `production_logs/`. This keeps planning, execution, and review separated while preserving traceability.

## Season 1 starter set
The current starter focus for Season 1 is built around the following early candidates.

| Episode | Virus |
|---|---|
| EP001 | ため息ウイルス |
| EP002 | 差し戻し確認ウイルス |
| EP003 | 責任転嫁ウイルス |
| EP004 | 口頭指示ウイルス |
| EP005 | なぜか君担当ウイルス |

## Operating principle
The production rule for this repository is **structure first, generation later**. That means episode logic, character roles, ending format, and reusable assets should be fixed in Markdown before image or video work begins. This helps keep execution lightweight and repeatable across the Season 1 mass-production phase.

## Next repository actions
| Priority | Action |
|---|---|
| 1 | Place the core design and operations documents under `docs/` |
| 2 | Move the canonical registries into `registry/` |
| 3 | Create EP001–EP005 working files under `episodes/season1/` |
| 4 | Add shotlist drafts after episode sheets are fixed |
| 5 | Record review outcomes in `production_logs/` after release |

## Maintained by
This repository is maintained as a planning and control base for _職場ウイルス図鑑_ production.
