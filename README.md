# Millwood Homes — Critical Path Schedule Dashboard

A self-contained, single-page critical path scheduling dashboard. No backend, no
build step — it runs entirely in the browser.

## Live site

Once GitHub Pages is enabled (see setup below), the dashboard is available at:

`https://<your-username>.github.io/<repo-name>/`

## First-time setup after deploying

1. Open the live site.
2. Click **Import JSON** and select `data/millwood-schedule-template.json`
   (download it from this repo first, or import directly if you cloned it
   locally).
3. The dashboard loads your 98-task / 13-phase CPM schedule.

## Saving your work

The dashboard **autosaves automatically** to your browser's local storage —
every few seconds if there are unsaved edits, and again right before you
close the tab. Reloading the page or closing/reopening the browser won't
lose anything.

Autosave only lives in *that one browser, on that one device*, though — it
doesn't sync across devices and doesn't back itself up anywhere else. For
that:

- Click **Export JSON** to download a portable copy
  (`millwood-homes-schedule.json`) any time you want a backup or need to move
  the schedule to another device.
- To version it in this repo, replace `data/millwood-schedule-template.json`
  with your exported file and commit:

  ```bash
  cp ~/Downloads/millwood-homes-schedule.json data/millwood-schedule-template.json
  git add data/millwood-schedule-template.json
  git commit -m "Update schedule $(date +%Y-%m-%d)"
  git push
  ```

This gives you a version history of your schedule over time, even though the
dashboard itself has no database.
