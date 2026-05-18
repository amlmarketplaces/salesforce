# amlmarketplaces/salesforce

Claude Code marketplace federating all `@amlplugins/salesforce-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-salesforce": {
      "source": { "source": "github", "repo": "amlmarketplaces/salesforce" }
    }
  },
  "enabledPlugins": {
      "salesforce-bulk@aml-salesforce": true,
      "salesforce-marketing-cloud@aml-salesforce": true,
      "salesforce-metadata@aml-salesforce": true,
      "salesforce-sobjects@aml-salesforce": true,
      "salesforce-soql@aml-salesforce": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/salesforce`, cached under `~/.claude/plugins/cache/aml-salesforce/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (6 total)

- `salesforce-bulk` — [@amlplugins/salesforce-bulk](https://github.com/amlplugins/salesforce-bulk)
- `salesforce-marketing-cloud` — [@amlplugins/salesforce-marketing-cloud](https://github.com/amlplugins/salesforce-marketing-cloud)
- `salesforce-metadata` — [@amlplugins/salesforce-metadata](https://github.com/amlplugins/salesforce-metadata)
- `salesforce-sobjects` — [@amlplugins/salesforce-sobjects](https://github.com/amlplugins/salesforce-sobjects)
- `salesforce-soql` — [@amlplugins/salesforce-soql](https://github.com/amlplugins/salesforce-soql)
- `salesforce-streaming` — [@amlplugins/salesforce-streaming](https://github.com/amlplugins/salesforce-streaming)

## Related

- npm packages: `@amlplugins/salesforce-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
