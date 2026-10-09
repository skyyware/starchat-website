---
id: "starchat-branding"
entity: "starchat"
title: "Make it look like your organization"
source: "https://github.com/skyyware/starchat/blob/v0.1.2/examples/installation/installation.json#L1-L40"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/branding"
topic_terms: ["branding", "design", "styles", "colors", "logo"]
links: [{"label": "This installation on GitHub", "url": "https://github.com/skyyware/starchat-website"}, {"label": "Make it look like your organization — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.2/examples/installation/installation.json#L1-L40"}, {"label": "Make it look like your organization — guide", "url": "https://chat.stage.dev/resources/branding"}]
---

Appearance belongs to the installation. installation.json configures primary, accent, background and text colors, plus body and heading fonts. Available font keys are source-sans, roboto-slab, d-din, system-sans and system-serif.

```json
{
  "primary": "#014e66",
  "accent": "#e9004c",
  "background": "#ffffff",
  "text": "#002733",
  "font": "source-sans",
  "heading_font": "roboto-slab",
  "logo": "/branding/organization.svg",
  "logo_alt": "Your organization",
  "favicon": "/branding/favicon.svg",
  "stylesheet": "/branding/organization.css"
}
```

This object is the value of brand, not a complete installation.json. Put the referenced assets in public/branding. A configured logo replaces the text wordmark. copy provides the headline, introduction, fixed scope orientation and starting questions for each configured language. The chat supports a language selector and preserves the visible conversation.

The public reference website demonstrates a dark design in public/branding/starchat.css. Other installations can use completely different branding while retaining the same engine and accessible semantic controls. Review contrast, keyboard focus and narrow screens after changes.
