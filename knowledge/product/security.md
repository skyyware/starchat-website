---
id: "starchat-security"
entity: "starchat"
title: "Scope and security boundaries"
source: "https://github.com/skyyware/starchat/blob/v0.1.2/SECURITY.md#L1-L54"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/security"
topic_terms: ["security", "scope", "injection", "sicherheit", "schutz"]
links: [{"label": "Scope and security boundaries — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.2/SECURITY.md#L1-L54"}, {"label": "Scope and security boundaries — guide", "url": "https://chat.stage.dev/resources/security"}]
---

Every installation defines its permitted purpose on the server. Each request rebuilds those instructions. Current messages, old assistant turns, compact history, retrieved sources and code are untrusted data. None can grant new tools, change the installation or expand its purpose.

The application validates host and source owner, input sizes, output shape, allowed HTTPS links, document freshness and explicit resource paths. The answer is rendered as text. The connector has no browsing, shell tools, transaction or submission authority. An independent model call reviews each candidate answer, including code, suggestions and compact memory, before release. Failed or invalid review hides the candidate. Unrelated requests get a fixed orientation to the installation's purpose.

These layers reduce risk, but no finite test or prompt proves immunity to prompt injection or perfect factual accuracy. The output review uses the same configured model and may share failure modes. Keep secrets and private customer material out of indexed sources. Do not give this chat authority to perform irreversible actions based on model judgments.

Operators are responsible for HTTPS, private runtime, current dependencies, provider terms and spending limits, real retention settings and tests against their own use case. composer audit checks known advisories; a clean result is not a guarantee of no vulnerabilities. Repository updates and deployments are deliberate, not automatic background actions.
