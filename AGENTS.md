# Frontend Knowledge Base Agent Guide

This vault follows the LLM-wiki pattern in `LLM-wiki.md`. The LLM maintains the generated wiki layer so the user can gradually learn the company's frontend projects, architecture, products, and workflows.

## Language and Style

- Write wiki content in Traditional Chinese.
- Keep frontend and product engineering terms in English when that is the team norm, for example React, routing, API, PR, CI, design system.
- Prefer concise, searchable notes over long essays.
- Use Obsidian links for important entities: `[[產品地圖]]`, `[[前端架構地圖]]`, `[[工作流程地圖]]`.
- Do not invent facts. Mark unknowns as `待補` and list the source needed to resolve them.

## Directory Ownership

- `raw/`: immutable source notes and imported material. Read from this directory, but do not rewrite its contents unless the user explicitly asks.
- `wiki/`: maintained knowledge base. Create and update these pages when ingesting sources or filing useful query results.
- `wiki/index.md`: content index. Update it whenever pages are added or materially changed.
- `wiki/log.md`: append-only activity log. Add an entry for each ingest, query filing, lint pass, or major maintenance update.

## Page Types

### Product Page

Use for products, product areas, or large customer-facing surfaces.

```markdown
# 產品名稱

## Summary
- 目的：
- 使用者：
- 目前狀態：

## Frontend Connections
- 關聯功能：
- 關聯模組：
- 常見工作：

## Product Context
- 商業目標：
- 使用情境：
- 重要限制：

## Open Questions
- 待補：

## Sources
- [[來源頁或 raw 檔名]]
```

### Feature Page

Use for product features, screens, flows, or user-facing capabilities.

```markdown
# 功能名稱

## Summary
- 功能目的：
- 所屬產品：
- 使用者：

## Frontend Implementation
- 入口：
- 主要元件：
- 狀態與資料流：
- 關聯 API：

## Workflow Impact
- 開發流程：
- 測試重點：
- 發版注意：

## Open Questions
- 待補：

## Sources
- [[來源頁或 raw 檔名]]
```

### Architecture Page

Use for frontend frameworks, modules, patterns, tooling, and cross-cutting technical concepts.

```markdown
# 架構或技術名稱

## Summary
- 用途：
- 使用範圍：
- 目前狀態：

## Where It Appears
- 關聯產品：
- 關聯功能：
- 專案位置：

## How It Works
- 核心概念：
- 資料流：
- 重要依賴：

## Change Notes
- 常見修改點：
- 風險：
- 驗證方式：

## Sources
- [[來源頁或 raw 檔名]]
```

### Workflow Page

Use for frontend development, review, release, QA, incident, and documentation workflows.

```markdown
# 流程名稱

## Summary
- 觸發情境：
- 參與角色：
- 產出物：

## Steps
1. 待補

## Related Knowledge
- 關聯產品：
- 關聯功能：
- 關聯架構：

## Failure Modes
- 常見問題：
- 預防方式：

## Sources
- [[來源頁或 raw 檔名]]
```

## Ingest Workflow

1. Read the new source from `raw/`.
2. Identify product, feature, architecture, workflow, people/team, and decision entities.
3. Create or update the relevant `wiki/` pages.
4. Add bidirectional links where useful. Every feature should link to its product and relevant frontend concepts when known.
5. Update `wiki/index.md` with new or changed pages and one-line summaries.
6. Append one entry to `wiki/log.md` using this format:

```markdown
## [YYYY-MM-DD] ingest | Source title
- Source: [[raw/source-file]]
- Updated: [[page-a]], [[page-b]]
- Notes:
```

## Query Workflow

1. Read `wiki/index.md` first.
2. Read the most relevant wiki pages.
3. Answer with links to wiki pages when possible.
4. If the answer reveals useful synthesis, ask whether to file it back into `wiki/`, unless the user already requested that.
5. If the wiki lacks enough information, say what is missing and suggest the next source to ingest.

## Maintenance Workflow

Periodically inspect for:

- Pages with no links or no inbound relationships.
- Repeated concepts that should be merged.
- Product pages without related features.
- Feature pages without frontend implementation notes.
- Architecture pages without product or workflow context.
- Stale claims contradicted by newer sources.

Log maintenance with:

```markdown
## [YYYY-MM-DD] lint | Wiki health check
- Checked:
- Updated:
- Follow-ups:
```
