# Cesto Docs

Documentation for [Cesto](https://cesto.co) — invest in narrative-driven baskets of assets on Solana. Published with [Mintlify](https://mintlify.com) at **[docs.cesto.co](https://docs.cesto.co)**.

## Cesto Toolkit skill

Turn any coding agent into a full Cesto client — browse baskets, simulate portfolios, and post to Cesto Labs. Install with one line:

```bash
npx skills add cesto-co/cesto-skills --skill cesto-toolkit
```

Works with Claude Code, Cursor, Codex, Windsurf, and 60+ other agents. Source: [`cesto-co/cesto-skills`](https://github.com/cesto-co/cesto-skills) · Docs: [docs.cesto.co/cesto/skill](https://docs.cesto.co/cesto/skill).

## Structure

Two tabs: **Documentation** (the product) and **Developers** (everything you can build with).

- `cesto/` — product documentation (baskets, Labs, funding, rebalancing, security, the skill)
- `developers/` — the developer hub: surface comparison, integration decision, API keys
- `widgets/` — embeddable basket widgets (iframe, no key)
- `web-sdk/` — the Web SDK: `@cesto/web-sdk` + `@cesto/react`, the in-page invest flow (publishable `cesto_pk_` key)
- `sdk/` — the Server SDK: the `@cesto/sdk` TypeScript client reference (secret `cesto_sk_` key)
- `skill.md` — the agent skill served at the site root
- `docs.json` — Mintlify navigation and site config

The three developer surfaces are ordered by how much you build: Widgets → Web SDK → Server
SDK. `developers/choose-an-integration.mdx` is the page that routes people between them —
keep it accurate when any surface changes.

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify), then run the dev server from the repo root (where `docs.json` lives):

```bash
npm i -g mintlify
mintlify dev
```

## Publishing

Changes merged to the default branch deploy to production automatically via the Mintlify GitHub app.

### Troubleshooting

- Dev server won't start — run `mintlify install` to reinstall dependencies.
- A page 404s — make sure you're running from the folder that contains `docs.json`.
