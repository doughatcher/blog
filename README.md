# blog — doughatcher.com content + overrides

Private repo. Holds the C-level pillar essays, doughatcher-specific Hugo layout overrides (consulting page, publications page), site branding (doug.png, custom.css), and the **editorial-loop authoring workflow** that drafts and ships pillars.

Theme comes from [`doughatcher/dougie-theme`](https://github.com/doughatcher/dougie-theme), installed as a micro.blog plugin alongside this repo's deploy.

## What's here

```
content/blog/        — pillar essays. Edited via PRs against this repo.
content/consulting.md — doughatcher's consulting landing page.

layouts/consulting/  — doughatcher-specific consulting page template
layouts/publications/ — doughatcher-specific publications template

static/doug.png      — profile image
static/custom.css    — doughatcher-only CSS deltas over the Dougie theme
static/favicon.svg, static/site.webmanifest — branding

apps/editorial-loop  — Node app that orchestrates idea → draft → PR → publish.
                       Runs via .github/workflows/blog-*.yml.

.github/workflows/   — deploy.yml, blog-publish.yml, scheduled-backup.yml,
                       and the editorial-loop automation chain.
.github/deploy/      — Python scripts that auth + theme-reload + backup
                       against micro.blog.

syndicate/           — dev.to + LinkedIn cross-post adapters.

config.json          — doughatcher.com site config (title, baseURL, menu).
```

## What's NOT here

- **Theme layouts/static** — those live in [`doughatcher/dougie-theme`](https://github.com/doughatcher/dougie-theme). Install that plugin in the micro.blog UI for doughatcher.com.
- **Workers** (social-bridge, link-preview-service, slack-bot) — those stay in `doughatcher/dotcom` for now (they serve all three sites, not just doughatcher; not really blog concerns). Slack-bot's `BLOG_REPO` var still points here so vibe-edits land in this repo's PRs.

## Editorial-loop workflow

Same as it always was — pillars get drafted as PRs against this repo, reviewed, merged. On merge, the blog-publish workflow publishes the post to doughatcher.com via micro.blog Micropub.

## Syndication policy (LinkedIn is opt-in)

**Nothing auto-syndicates to LinkedIn.** This is deliberate.

- **Auto on merge** (`blog-publish.yml`): publishes to doughatcher.com and cross-posts only to the destinations in the `MICROBLOG_SYNDICATE_TO` repo variable (currently `threads`). LinkedIn is **not** in that list.
- **No `mp-syndicate-to` = suppressed, not defaulted.** `apps/editorial-loop/lib/microblog-poster.js` always sends an explicit empty `mp-syndicate-to[]=` when no targets are configured, so micro.blog's account-level cross-posting (incl. LinkedIn) never fires implicitly. Posts made directly in the micro.blog **web editor** bypass this code — LinkedIn auto-cross-post is also turned **off at the account level** as the backstop.
- **The lever** — to put a *specific* post on LinkedIn: add the **`syndicate-linkedin`** label to its (merged) PR. `syndicate-on-label.yml` then cross-posts that one post to LinkedIn explicitly. This is the only path to LinkedIn; use it intentionally.

## How doughatcher.com renders

1. micro.blog has Dougie plugin installed for the doughatcher.com site (pulls theme files from `doughatcher/dougie-theme`)
2. micro.blog's theme deploy points at THIS repo (executive-blog) for content + overrides
3. On render, Hugo merges: `dougie-theme/layouts/*` (base) + `executive-blog/layouts/*` (overrides) + `executive-blog/content/*`
4. Per-site plugin params from the Dougie plugin settings inject branding/CTA/etc

## Migration status

Created 2026-05-30 as part of the dougie-theme extraction. Renamed from `executive-blog` to `blog` shortly after. Live cutover from `doughatcher/dotcom` happens once Doug points doughatcher.com's micro.blog theme at this repo (theme id 102559) instead of dotcom (theme id 102558).
