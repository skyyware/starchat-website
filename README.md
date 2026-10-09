# Starchat website

The working, public installation behind [chat.stage.dev](https://chat.stage.dev).
It explains Starchat using reviewed Markdown and links to the actual source.
The engine lives in [skyyware/starchat](https://github.com/skyyware/starchat) and
is installed through Composer. This repository owns its knowledge, identity,
styles and legal notice.

## Make your own

```bash
git clone https://github.com/skyyware/starchat-website.git my-chat
cd my-chat
composer install
```

Change `installation.json` to your identity, hosts, scope and branding. Replace
`knowledge/product/` with your reviewed public information. Replace `legal/`
with your operator and privacy information; the SKYYWARE details describe this
installation only. Adapt or replace `public/branding/`. Then build the index:

```bash
vendor/bin/starchat index
```

Configure HTTPS with `public/` as the document root and a front-controller rule.
Provision your own approved model connection using the
[engine installation guide](https://github.com/skyyware/starchat/blob/v0.1.4/docs/installation.md).
Credentials stay outside this repository. Nothing logs you into a provider,
purchases access, deploys a server or schedules updates automatically.

## Follow the pieces

- [Configuration](installation.json): purpose, hosts, copy and colors
- [Entrypoint](public/index.php): the complete application bootstrap
- [Knowledge](knowledge/product): the facts used to answer questions
- [Styles](public/branding/starchat.css): this installation's appearance
- [Source manifest](knowledge/sources.json): review provenance

Questions, examples and suggestions are tested against this installation's
purpose. Code is displayed, never executed. Review generated snippets before
using them. Keep an explicit lock file and test updates before deployment.

MIT. Starchat and SKYYWARE names identify the original project; use your own
identity for an independent service.
