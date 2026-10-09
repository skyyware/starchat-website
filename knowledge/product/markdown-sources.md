---
{
  "id": "starchat-markdown-sources",
  "entity": "starchat",
  "title": "Your own reviewed knowledge collection",
  "source": "https://github.com/skyyware/starchat/blob/v0.2.0/docs/knowledge.md",
  "retrieved_at": "2026-10-09",
  "review_status": "reviewed",
  "source_version": "skyyware/starchat v0.2.0",
  "public_path": "/resources/markdown-sources",
  "topic_terms": [
    "external",
    "connector",
    "migration",
    "folder",
    "markdown"
  ],
  "links": [
    {
      "label": "Own and review your knowledge",
      "url": "https://chat.stage.dev/resources/knowledge"
    },
    {
      "label": "Ask Stage about migrating a Starchat knowledge collection",
      "url": "https://stage.dev/?q=How%20do%20I%20migrate%20a%20Starchat%20Markdown%20connector%20to%20installation-owned%20knowledge%20in%20v0.2.0%3F"
    }
  ]
}
---

Each Starchat installation owns a separately prepared Markdown knowledge collection. The previous external Markdown connector was removed in v0.2.0. A package guide or an arbitrary folder is no longer a live source for public answers.

If you used the previous connector, first decide which information actually helps your visitors. Read and rewrite it as owned articles for their questions, record the original source and exact reviewed version, and test those articles independently. Do not copy private material or turn an internal manual into public knowledge without review.

Remove the old manifest configuration, rebuild the index with the new engine and deliver the code and index together. The new engine rejects the old index format. Keep the previous code and index together for a possible rollback. A deployment or passing test does not itself establish that the articles are factually correct.

The old guide address remains available to explain this change. For an ordinary visitor, the useful question is who prepares the information and keeps it correct. For migration instructions, continue at Stage with the prepared question and send it when ready.
