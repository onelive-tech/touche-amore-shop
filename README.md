# Touché Amore

The theme code for the **Touché Amore** Shopify store (Sandbag), backed up from the
live theme every day by the olaf sync.

| | |
|---|---|
| Store | touche-amore-shop.myshopify.com |
| Client | Sandbag |
| Shopify admin | https://admin.shopify.com/store/touche-amore-shop/themes |
| HubSpot record | https://app.hubspot.com/contacts/21247421/record/2-48517891/32911212964 |
| Stage | Live |

## What this repo is

- `main` always matches the **live theme**. Every day the sync copies any
  changes made on live (including edits in the Shopify theme editor) into
  `main` as a commit by *ONELIVE Theme Sync*.
- Changes are made on a **ticket branch**, deployed to live, and recorded as a
  **pull request**. Nobody edits `main` directly.
- The sync never overwrites work in this repo. If the repo and live disagree,
  it stops and opens a **sync-review issue** ("on hold") so a person can decide.

## How to make a change

Use the **Olaf** extension in VS Code (❄️ in the left bar):

1. **Start a ticket**: paste the HubSpot ticket link. Olaf checks the store
   isn't on hold, brings `main` up to date with live, and makes your branch.
2. **Preview locally**: runs the theme on a development theme. Live isn't touched.
3. **Commit changes**: tick the files to include, check the suggested message, commit.
4. **Review & open the PR**: check the title, description and files, then open it.
5. **Deploy to Shopify**: pushes **only the files you changed** to live, after
   checking nobody else changed them on live. Before or after the PR.
6. **Update the HubSpot ticket**: paste the PR link into the ticket.

No VS Code? From a terminal: `olaf start <ticket>`, `olaf preview`,
`olaf commit -m "…"`, `olaf pr`, `olaf deploy`.

## If the store is on hold

Open the **sync-review** issue. It links a side-by-side compare of the repo and
live. Decide which is right; the issue explains how to release the store.

## Good to know

- Edits made in the Shopify theme editor are fine: they're backed up the next day.
- Don't push a whole theme to live (`shopify theme push` with no `--only`).
  Olaf deploys only your files, so it can't undo someone else's work.
- `README.md` isn't a theme file, so it's never deployed to Shopify.
- Questions: ask in #olafsync.

<!-- olaf:readme: added by the olaf rollout. Edit freely. -->
