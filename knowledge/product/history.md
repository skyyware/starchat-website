---
id: "starchat-history"
entity: "starchat"
title: "Conversation history and privacy"
source: "https://github.com/skyyware/starchat/blob/v0.1.2/public/conversation.js#L1-L70"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/history"
topic_terms: ["history", "conversation", "privacy", "verlauf", "context"]
links: [{"label": "Conversation history and privacy — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.2/public/conversation.js#L1-L70"}, {"label": "Conversation history and privacy — guide", "url": "https://chat.stage.dev/resources/history"}]
---

The complete visible conversation is stored locally in this browser using LocalStorage. It survives reload and restart until New conversation or clearing website data. Reset is synchronized across tabs for this installation. Other people using the same browser profile may read the conversation.

Each model request contains at most six previous answered pairs within an 11000-character history budget and, when available, up to 700 characters of compact context. The current question is at most 1800 characters. Earlier instructions inside compact context remain untrusted. A visible long conversation does not mean the whole transcript is sent to the model each time.

Questions, bounded conversation context and matching public evidence are processed by the configured provider. This website uses OpenAI through Stage Chat Codex. The application does not intentionally store chat bodies on the server. This statement is not a promise about provider processing; operator notices must describe actual configurations. Please do not enter personal or confidential data.

A failed request is retried in its existing conversation position instead of duplicating the user question. A new conversation invalidates late responses. Storage failures are visible and unsaved text is retained in the open tab. The chat does not create an account, case file, appointment or submitted application.
