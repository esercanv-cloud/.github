# WEAREMOOZE — Reklam Ajansi

> AI-native solo agency. WeAreMooze ana ajans, her yeni iş ayri repo (Karar 010).

## Aktif Repolar

| Repo | Amac |
|------|------|
| [WEAREMOOZE-OS](https://github.com/esercanv-cloud/WEAREMOOZE-OS) | Ana sistem: vault (2. beyin), skills, configs |
| [client-moozecreative-fullservice](https://github.com/esercanv-cloud/client-moozecreative-fullservice) | MoozeCreative — Shopify + Meta Ads |
| [client-reklamall-fullservice](https://github.com/esercanv-cloud/client-reklamall-fullservice) | Reklamall — Shopify + Meta Ads + TikTok |

## Mimari

- **Vault-first:** Tum bilgi `WEAREMOOZE-OS/brain/` icinde (Karar 009 — vault beyin standardi)
- **Multi-repo:** Her musteri/proje ayri repo (Karar 002 + Karar 010)
- **Cowork:** Esercan + Claude Code paralel (Karar 010 — cowork stratejisi)

## Reusable Workflows

Bu org repo (`.github`) **reusable workflow'lar** sunar. Diger repolar bunlari `uses:` ile cagirir.

### markdown-frontmatter-lint.yml
Karar 009 frontmatter zorunluluğu (type/title/tags/related/updated) kontrolu.

```yaml
jobs:
  lint:
    uses: esercanv-cloud/.github/.github/workflows/markdown-frontmatter-lint.yml@main
    with:
      paths: 'brain docs'
      strict: 'true'
```

### json-validate.yml
n8n workflow JSON, Shopify schema JSON syntax kontrolu.

```yaml
jobs:
  json:
    uses: esercanv-cloud/.github/.github/workflows/json-validate.yml@main
    with:
      paths: '**/*.json'
```

### secrets-scan.yml
Token hardcode (Kural 10) kontrolu — sk-/ghp_/EAA/AKIA pattern.

```yaml
jobs:
  secrets:
    uses: esercanv-cloud/.github/.github/workflows/secrets-scan.yml@main
```

## İletişim

- **Email:** esercanv@gmail.com
- **Web:** wearemooze.com (yapim asamasinda)
