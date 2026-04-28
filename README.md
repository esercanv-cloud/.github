# esercanv-cloud/.github — Reusable Workflows

Bu repo **org-level default community health files** + **reusable GitHub Actions workflows** icerir.

## Yapi

```
.github/
├── profile/
│   └── README.md              # Org sayfasi (github.com/esercanv-cloud)
└── workflows/
    ├── markdown-frontmatter-lint.yml   # Karar 009 frontmatter check
    ├── json-validate.yml                # JSON syntax check
    └── secrets-scan.yml                 # Token hardcode (Kural 10) check
```

## Kullanim (diger repolardan)

```yaml
# .github/workflows/ci.yml
name: CI
on: [push, pull_request]
jobs:
  frontmatter:
    uses: esercanv-cloud/.github/.github/workflows/markdown-frontmatter-lint.yml@main
    with:
      paths: 'brain docs'
  json:
    uses: esercanv-cloud/.github/.github/workflows/json-validate.yml@main
  secrets:
    uses: esercanv-cloud/.github/.github/workflows/secrets-scan.yml@main
```

## Karar Referansi

- [Karar 002 — Client Repo Ayrimi](https://github.com/esercanv-cloud/WEAREMOOZE-OS/blob/main/brain/kararlar/karar-002-client-repo-ayrimi.md)
- [Karar 009 — Vault Beyin Standardi](https://github.com/esercanv-cloud/WEAREMOOZE-OS/blob/main/brain/kararlar/karar-009-vault-beyin-standardi.md)
- [Karar 010 — Cowork Stratejisi + Multi-Repo](https://github.com/esercanv-cloud/WEAREMOOZE-OS/blob/main/brain/kararlar/karar-010-cowork-stratejisi.md)
