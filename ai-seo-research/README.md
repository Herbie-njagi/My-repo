# AI-Powered SEO Content Production — Research Project

Research base for understanding how real practitioners are producing, scaling, and quality-controlling SEO content in the AI-search era (Google AI Overviews/AI Mode, ChatGPT/Perplexity answer engines, GEO/AEO).

## Why this topic
"AI-powered SEO content production" sits at the center of the biggest disruption to organic marketing in a decade — Gartner projects a meaningful decline in traditional search click volume by end of 2026 as AI answer engines absorb queries. That makes it high-value to understand *now*, from people who are actually running content operations through this shift rather than commentators reacting to it.

## Who's in here and why
10 practitioners — SEO/content leads at real companies (Ahrefs, Amsive, SparkToro, iPullRank), independent advisors with named enterprise clients (Coinbase, Ramp, Reddit, SAP), and agency founders running experiments with published data. Full annotated list with links: [`research/sources.md`](research/sources.md).

Selection bar: each person had to (a) currently practice — run an agency, lead a content team, or advise real companies — not just write *about* SEO, and (b) have a recent, findable public track record specifically on AI's impact on content production (not general SEO from 2019).

## What's collected so far
- [x] 10 experts identified, vetted, and annotated (`research/sources.md`)
- [ ] LinkedIn posts (`research/linkedin-posts/`) — pending manual collection, see `research/other/collect.md`
- [ ] YouTube transcripts (`research/youtube-transcripts/`) — pending local collection via `youtube-transcript-api`, see `research/other/collect.md`
- [x] Collection methodology + limitations documented (`research/other/collection-notes.md`)

## Repo structure
```
research/
  sources.md              # the 10 experts, annotated
  linkedin-posts/
    <author-slug>/         # five file per post
  youtube-transcripts/
    <author-slug>/         # one file per video transcript
  other/
    collection-notes.md    # methodology + why posts/transcripts aren't scraped in this pass
    collect.md              # ready-to-run local collection script (Claude Code / Codex)
```

## Next steps
Running `research/other/collect.md` locally with Claude Code or Codex (needs real network + git access this environment doesn't have) to pull the actual transcripts and post archives, committing per-author as you go rather than in one batch.
