# Frontend Knowledge Base Agent Guide

This vault follows the LLM-wiki pattern in `LLM-wiki.md`. The LLM maintains the generated wiki layer so the user can gradually learn the company's frontend projects, architecture, products, and workflows.

## Language and Style

- Write wiki content in Traditional Chinese.
- Keep frontend and product engineering terms in English when that is the team norm, for example React, routing, API, PR, CI, design system.
- Prefer concise, searchable notes over long essays.
- Use Obsidian links for important entities: `[[產品地圖]]`, `[[前端架構地圖]]`, `[[工作流程地圖]]`.
- Do not invent facts. Mark unknowns as `待補` and list the source needed to resolve them.

## Directory Ownership

- `raw/`: source notes and imported material. Preserve source facts and provenance. It is allowed to normalize formatting to match `template/` before ingesting, but do not invent facts, remove source context, or rewrite meaning.
- `template/`: source format templates. Use this directory to check whether `raw/` files follow an expected source structure before ingesting.
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
2. Inspect `template/` and compare the source against the closest matching template.
3. If the source does not follow a known template, normalize the raw note to the closest template before ingesting when this can be done without inventing facts or changing meaning.
4. Before normalizing a new raw source, ask the user to confirm metadata:
   - `source`: URL or `none`
   - `updated`: date/time or `none`
5. At minimum, add YAML frontmatter with `title`, `source`, and `updated`, followed by a `## Notes` section that explains how the raw note was preserved.
6. If the user provides `none` for `source` or `updated`, write `待補` for that field. If the user provides values, preserve them exactly unless they need Markdown/YAML escaping.
7. If expected fields are missing, mark them as `待補` instead of guessing.
8. If format issues block reliable ingestion even after normalization, report the issue and suggest which template the source should follow.
9. Mention the template name or normalization status in the ingest log.
10. Identify product, feature, architecture, workflow, people/team, and decision entities.
11. Create or update the relevant `wiki/` pages.
12. Add bidirectional links where useful. Every feature should link to its product and relevant frontend concepts when known.
13. Update `wiki/index.md` with new or changed pages and one-line summaries.
14. Append one entry to `wiki/log.md` using this format:

```markdown
## [YYYY-MM-DD] ingest | Source title
- Source: [[raw/source-file]]
- Updated: [[page-a]], [[page-b]]
- Template: template-name or 待補
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
