# Sources and capture log

Captured on 24 Nov 2026.

## E01 · Atom guide
| Source | Method |
|---|---|
| [tryatom.ai](https://tryatom.ai/) home, pricing and 17 template pages | Web fetch |
| Atom docs: installation, setup, first automation, effective prompts, common workflows, best practices, troubleshooting, skills, thinking modes, checkpoints, attachments, security, team AI setup, MCP Mode, pricing, usage limits | Web fetch (paths verified against the live docs sidebar) |
| [@daveylovescode](https://x.com/daveylovescode), latest 40 posts | Apify `apidojo/tweet-scraper` |
| X search for Atom posts and reviews | Apify `apidojo/tweet-scraper` |
| School of Motion, Product Hunt, Jake In Motion coverage | Web search |

## E02 · After Effects 27 video
| Source | Method |
|---|---|
| [YouTube RcNUE6lg3fE](https://www.youtube.com/watch?v=RcNUE6lg3fE), full transcript, chapters, description | Apify `johnvc/YoutubeTranscripts` |
| [Adobe what's new](https://helpx.adobe.com/after-effects/desktop/what-s-new/whats-new.html), [AI Assistant overview](https://helpx.adobe.com/after-effects/desktop/work-with-after-effects-ai-assistant/after-effects-ai-assistant-overview.html), [Adobe community post](https://community.adobe.com/announcements-527/after-effects-27-0-is-here-ai-assistant-3d-materials-and-what-to-try-first-1653289), [CG Channel](https://www.cgchannel.com/2026/11/adobe-releases-after-effects-27-0/), [Digital Production](https://digitalproduction.com/2026/11/17/after-effects-27-an-ai-assistant-because-apparently-we-needed-one/) | Web search and fetch |

## E03 · Templates directory
| Source | Method |
|---|---|
| [madbax.org/editor-zone](https://madbax.org/editor-zone/), [aepmotion.com](https://aepmotion.com/) | Web fetch |
| EarnEdits product pages (home page blocks direct fetches) | Web search snippets of earnedits.com |
| The other 28 names | 47 Google searches via Apify `apify/google-search-scraper`; each result checked against the creator's own store or channel |

## Media inventory
21 images, listed in [media-manifest.json](media-manifest.json): 17 Atom template thumbnails (cdn.davey.design) and 4 YouTube frames (i.ytimg.com). GitHub Actions downloads them into `docs/media/` on push.

## Rights
All quoted material belongs to its authors. This hub summarises and links; it doesn't redistribute paid files.
