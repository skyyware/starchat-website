---
id: "starchat-knowledge"
entity: "starchat"
title: "Give your chat reliable knowledge"
source: "https://github.com/skyyware/starchat/blob/v0.1.3/docs/knowledge.md#L1-L50"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/knowledge"
topic_terms: ["knowledge", "markdown", "sources", "index", "wissen", "quellen"]
links: [{"label": "Give your chat reliable knowledge — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.3/docs/knowledge.md#L1-L50"}, {"label": "Give your chat reliable knowledge — guide", "url": "https://chat.stage.dev/resources/knowledge"}]
---

Each installation owns knowledge/<category>/*.md files. Each file has YAML front matter and a Markdown body. entity must match the installation ID. id, title, source, retrieved_at and review_status are required. Source and action URLs use HTTPS.

```yaml
---
id: product-setup
entity: example
title: Set up Example
source: https://example.test/documentation/setup
retrieved_at: '2026-10-09'
review_status: reviewed
topic_terms: [setup, installation]
public_path: /resources/setup
---
```

This metadata is an example; replace its ID, owner, URL and date with the actual source you checked. Facts and useful steps follow the front matter. A download is not a review. Mark reviewed only after checking the content, its conditions and useful links. Keep missing or conflicting information explicit.

source_max_age_days is configured per installation. valid_until may impose an earlier expiry. Retrieval checks both primary and supporting sources. topic_terms, phrase_terms and keywords help retrieval. based_on connects a guide to up to twelve direct supporting sources.

public_path deliberately publishes a current reviewed article. Without it, there is no raw public resource page, but facts may still appear in public answers. Never put private material or credentials in knowledge. Rebuild with vendor/bin/starchat index after a reviewed change. It validates and indexes; it does not browse, review or automatically refresh dates. Invalid sources and duplicate IDs or public paths prevent replacement of the accepted index.
