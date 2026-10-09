---
id: "starchat-security"
entity: "starchat"
title: "Control, privacy and clear limits"
source: "https://github.com/skyyware/starchat/blob/v0.2.0/SECURITY.md"
retrieved_at: "2026-10-09"
review_status: "reviewed"
source_version: "skyyware/starchat v0.2.0"
public_path: "/resources/security"
topic_terms: ["privacy", "security", "safety", "datenschutz", "sicherheit", "private", "secrets", "schutz"]
links: [{"label": "Control, privacy and clear limits", "url": "https://chat.stage.dev/resources/security"}, {"label": "Read this installation’s privacy notice", "url": "https://chat.stage.dev/legal"}, {"label": "Discuss technical safeguards with Stage", "url": "https://stage.dev/?q=How%20does%20Starchat%20enforce%20installation%20scope%2C%20source%20isolation%20and%20independent%20answer%20review%2C%20and%20what%20should%20an%20operator%20verify%3F"}]
---

A Starchat installation has a defined purpose and its own knowledge. The purpose is reasserted on every request. Messages and retrieved information cannot legitimately grant new powers or turn it into an assistant for unrelated tasks. Generated answers are checked before they are shown, including a separate review.

Those safeguards reduce risk but do not guarantee perfect accuracy or protection against every attack. The owner must check the collection, allowed links, actual model connection, operational controls and the answers people receive. Starchat should be useful with ordinary relevant writing and explanation requests instead of rejecting them merely because they are phrased differently.

This public installation stores the visible conversation locally in the browser. A bounded conversation and relevant public knowledge are processed through the configured OpenAI connection to prepare and review the answer. Do not enter secrets or sensitive personal records. The legal and privacy notice describes this installation's actual setup.

Self-hosting the application is not a claim that model processing happens on the same server, that no provider receives information, or that an installation is automatically compliant with a law. Other deployments need their own truthful notice and appropriate assessment.

For source-supported technical architecture or configuration questions, use Stage. This chat can explain the practical tradeoffs for your intended audience without asking you to disclose credentials.
