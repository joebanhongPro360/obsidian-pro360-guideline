# Raw Sources

Put original source material here before asking the LLM to ingest it into the wiki.

Prefer formatting new raw notes with the closest matching template in `../template/`.
If no template fits, keep the source readable and preserve unknown fields as `待補`.

Examples:

- Manually written project notes.
- Product or feature documentation excerpts.
- Meeting notes.
- PR, Issue, or release summaries.
- Screenshots or assets referenced by notes.

The LLM should treat this directory as source material. Generated summaries and cross-linked knowledge should live in `../wiki/`.

Before ingesting, the LLM should compare each raw source with `../template/` and report whether the format matches a known template.
If a raw source is missing expected fields or sections, the LLM should not rewrite it unless explicitly asked.
