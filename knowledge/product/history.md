---
id: "starchat-history"
entity: "starchat"
title: "Continue the conversation"
source: "https://github.com/skyyware/starchat/blob/v0.2.0/public/conversation.js"
retrieved_at: "2026-10-09"
review_status: "reviewed"
source_version: "skyyware/starchat v0.2.0"
public_path: "/resources/history"
topic_terms: ["conversation", "history", "verlauf", "gespräch", "saved", "speichern", "reload"]
links: [{"label": "Continue the conversation", "url": "https://chat.stage.dev/resources/history"}]
---

The visible conversation is kept in this browser and survives reloading. New conversation clears this installation's saved conversation, including in other open tabs. People who share the same browser profile may be able to see it.

The model receives a bounded recent part of the conversation, with a short summary where applicable. A long visible history does not mean every old sentence is supplied on every request. Each answer still uses the installation's fixed purpose and available evidence.

Questions can build on the current subject. For example, a person can ask for a shorter explanation or help drafting a relevant inquiry. An offered follow-up should work. The chat should not claim to send the draft or perform the action.

A link with a prepared question opens an editable draft in the destination chat. It preserves that destination's existing conversation and does not send the question automatically. The question is removed from the visible address after loading. URLs are not a private place for sensitive information, so handoff questions should be general and contain no personal details.
