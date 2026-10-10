# Archived Starchat self-demo

This repository is retired under the owner's decision of 10 October 2026.
Its source and history are preserved for reference. Do not deploy or maintain
this installation. The successor at chat.stage.dev is the separate
[Stage chat demo](https://github.com/skyyware/starchat-demo), backed by the
regular website at [stage.dev](https://stage.dev). The shared Starchat core is
now private and requires authorized repository access.

The installation notes below describe the historical self-demo, not the current
service or a recommended new installation. Existing deployment artifacts and
runtime are retained outside this repository for rollback.

## Historical installation

The former public installation behind [chat.stage.dev](https://chat.stage.dev).
It helps people explore a chat for themselves, a product, an organization or a
public service. It uses separately reviewed Markdown and links to useful next
steps. Technical questions can continue at [Stage](https://stage.dev).
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
[engine installation guide](https://github.com/skyyware/starchat/blob/v0.2.0/docs/installation.md).
Credentials stay outside this repository. Nothing logs you into a provider,
purchases access, deploys a server or schedules updates automatically.

Each installation owns its knowledge collection. Package documentation supplies
evidence for an editorial review; it is not connected directly to the chat index.
When a feature, release or relevant fact changes, review the affected visitor
articles, update their provenance, rebuild the index and test actual answers.
There is no scheduled refresh. Immutable technical articles name their reviewed
version; changing information still expires under the configured age limit.

Run `composer check` after installing dependencies. It verifies each article's
owner, digest and package-source binding, then builds and checks an isolated
index. Actual model answers and browser behavior remain separate acceptance checks.

## Follow the pieces

- [Configuration](installation.json): purpose, hosts, copy and colors
- [Entrypoint](public/index.php): the complete application bootstrap
- [Knowledge](knowledge/product): the facts used to answer questions
- [Styles](public/branding/starchat.css): this installation's appearance
- [Source manifest](knowledge/sources.json): review provenance
- [Design](docs/design.md): original identity, typeface and source rights

Questions, examples and suggestions are tested against this installation's
purpose. Code is displayed, never executed. Review generated snippets before
using them. Keep an explicit lock file and test updates before deployment.

MIT. Starchat and SKYYWARE names identify the original project; use your own
identity for an independent service.
