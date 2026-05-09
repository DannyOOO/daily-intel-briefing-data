# Daily Intel Briefing Data Feed

This repository stores the public JSON data feed for the Daily Intel Briefing website.

The stable entry point is `latest.json`. The published Manus site fetches this file at page load and falls back to embedded content if GitHub is unavailable. Daily scheduled briefing runs should overwrite `latest.json` and add a dated file under `archive/YYYY-MM-DD.json`.

## Data contract

`latest.json` contains a top-level `schema_version`, an `updated_at` timestamp, an `edition` object, and an `archive` list. Each edition contains three sections: `hypersonics`, `nuclear`, and `ai`. Each section contains exactly three items with `title`, `summary`, `why_it_matters`, `source_label`, and `source_url` fields.
