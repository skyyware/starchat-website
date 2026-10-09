---
id: "starchat-operations"
entity: "starchat"
title: "Test and maintain an installation"
source: "https://github.com/skyyware/starchat/blob/v0.1.4/docs/installation.md#L1-L70"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/operations"
topic_terms: ["operations", "test", "deploy", "update", "maintenance", "version", "latency", "speed", "slow", "Fast"]
links: [{"label": "Test and maintain an installation — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.4/docs/installation.md#L1-L70"}, {"label": "Test and maintain an installation — guide", "url": "https://chat.stage.dev/resources/operations"}]
---

The shared engine is versioned through Composer and the installation commits composer.lock. Updating source code does not deploy it. Before an engine update, review its changes, run composer check in the engine and test the consuming installation. Use composer audit to inspect known dependency advisories.

Knowledge updates require reviewing the source content and its useful links, editing Markdown and running vendor/bin/starchat index. No built-in crawler or automatic reviewer silently marks content checked. The current source lifetime is rechecked on lookup, so expired sources may stop supplying answers until reviewed again.

/health reports status, entity, document count, limiter availability, engine version and any operator-supplied build metadata. /sources explains source use. Public resources appear only for reviewed current documents with public_path. Each operator should configure private runtime, HTTPS, safe web-root rules, APCu, a suitable edge limit and a rollback path.

Model calls are limited to 25 seconds each with a shared 45-second request deadline. The browser timeout is 50 seconds. A host should allow at least 55 seconds. There are three concurrent request slots and an aggregate twenty-request-per-minute limit when APCu is enabled; these limits do not constitute a provider spending cap.

The default model profile is gpt-6-astra with low reasoning and Fast service. Source retrieval, optional model source selection, answer generation and independent answer review happen in sequence. The answer appears only after validation and review. Response headers provide Server-Timing for these phases and a fixed X-Starchat-Failure category on failures. They contain no conversation contents, private paths or user identifiers, and the engine does not write these diagnostics to disk. Actual speed depends on the request and provider; Fast is not an immediate-response guarantee.
