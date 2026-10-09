---
id: "starchat-code-examples"
entity: "starchat"
title: "Code examples and exact source links"
source: "https://github.com/skyyware/starchat/blob/v0.1.3/src/App.php#L1-L70"
retrieved_at: "2026-10-09"
review_status: "reviewed"
public_path: "/resources/code-examples"
topic_terms: ["code", "examples", "php", "example", "beispiel"]
links: [{"label": "Complete front controller on GitHub", "url": "https://github.com/skyyware/starchat-website/blob/v0.1.0/public/index.php#L1-L6"}, {"label": "Code examples and exact source links — source", "url": "https://github.com/skyyware/starchat/blob/v0.1.3/src/App.php#L1-L70"}, {"label": "Code examples and exact source links — guide", "url": "https://chat.stage.dev/resources/code-examples"}]
---

Starchat shows code as text with syntax colors, horizontal scrolling and a copy button. It never executes a snippet. Supported answer languages are php, json, javascript, bash, yaml, text, css and html. Answers can include up to two code blocks with up to 6000 characters each. Copying requires a user click.

This minimal front controller starts an installation after Composer has installed the package:

```php
<?php
declare(strict_types=1);

require dirname(__DIR__) . '/vendor/autoload.php';

Starchat\App::run(dirname(__DIR__));
```

The application reads installation.json from that directory and serves only the configured entity. The HTTP server points at public/, not the repository root. Build its knowledge index before serving.

For a custom Stage application, new Starchat\App($root, $host) exposes handle($request), returning a Stage\Http\Response. Keep existing CMS and private routes in a private dispatcher and pass only the chat paths to this application. The constructor also accepts an optional Closure connector factory for controlled integration tests or another Stage Chat connector.

To link directly to implementation, add a checked GitHub permalink with a version and line range as a knowledge link. The model can select only offered link IDs; it cannot invent URLs. Generated examples are not a claim of execution or testing. Review and test them in your own environment.
