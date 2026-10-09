---
id: "starchat-installation"
entity: "starchat"
title: "Build your own installation"
source: "https://github.com/skyyware/starchat/blob/v0.1.3/docs/installation.md#L1-L70"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/installation"
topic_terms: ["installation", "install", "setup", "composer"]
links: [{"label": "Complete front controller · reference v0.1.0", "url": "https://github.com/skyyware/starchat-website/blob/v0.1.0/public/index.php#L1-L6"}, {"label": "Build your own installation — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.3/docs/installation.md#L1-L70"}, {"label": "Build your own installation — guide", "url": "https://chat.stage.dev/resources/installation"}]
---

Start from the public skyyware/starchat-website repository. It is a real separate installation of the shared skyyware/starchat Composer package. It requires PHP 8.4 or later, mbstring, PDO SQLite with FTS5 and Composer. No frontend build is required.

```bash
git clone https://github.com/skyyware/starchat-website.git my-chat
cd my-chat
composer install
```

Change installation.json to your entity ID, allowed HTTPS hosts, purpose, text and colors. Replace knowledge/product with your own reviewed public sources. Replace the legal directory with accurate information about your operator and provider configuration. Use your own branding. Then build the disposable index:

```bash
vendor/bin/starchat index
```

Serve only public/ through HTTPS. Non-file requests go to public/index.php. Keep .runtime and provider credentials outside the web root and Git. Provision your own approved model connector. Copying a repository does not provide authentication, a server, paid access or a deployment.

As reviewed on 9 October 2026, this installation uses Starchat engine v0.1.3. The linked complete front controller is from the separate reference installation tag v0.1.0 and is unchanged here. The engine and reference installation have independent version numbers. The engine source link points to v0.1.3; the front-controller link points to v0.1.0.

The complete front controller is:

```php
<?php
declare(strict_types=1);

require dirname(__DIR__) . '/vendor/autoload.php';

Starchat\App::run(dirname(__DIR__));
```

The package installation guide documents the STARCHAT_RUNTIME, STARCHAT_CODEX_BINARY, STARCHAT_CODEX_HOME, STARCHAT_CODEX_WORK, STARCHAT_MODEL, STARCHAT_REASONING_EFFORT, STARCHAT_SERVICE_TIER and STARCHAT_MODEL_CATALOG settings. Defaults are gpt-6-astra, low reasoning and Fast service. An explicit STARCHAT_SERVICE_TIER=standard setting disables the optional tier; unsupported profiles fail rather than silently changing models. Model availability is account-dependent; nothing purchases or switches access automatically.
