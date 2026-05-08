# Hondius Hantavirus Event Tracker

This repository publishes a public GitHub Pages site for the recent hantavirus outbreak linked to the expedition vessel _m/v Hondius_.

The source-of-truth research workspace is a private LLM-managed wiki. This repository is only the public publishing layer: it contains the event timeline, dated daily reports, and source reference cards needed for transparent citation.

## Public Site Structure

```text
docs/
  index.md
  timeline.md
  reports/
    YYYY-MM-DD.md
  sources/
    source-slug.md
  _config.yml
```

## Sync Workflow

Run the local-only sync script after the private wiki has been updated:

```bash
python3 scripts/sync-from-private-wiki.py
```

The sync script is intentionally not published in this public repository. It reads only the configured Hondius event timeline, configured daily report files, and cited `raw/events/` files from the private wiki. It does not traverse or mirror unrelated private-wiki content.

Expected maintenance chain:

```text
private wiki ingestion -> public sync -> git commit -> git push -> GitHub Pages publish
```

## Public Safety

- Do not copy unrelated private-wiki files into this repository.
- Do not publish personal, family, financial, child-related, Gmail, calendar, or private vault material.
- Publish source cards rather than full raw third-party captures.
- Cite official and primary sources first.
- Preserve official-source contradictions explicitly.

## GitHub Pages

Use GitHub Pages from the `docs/` folder on the `main` branch.
