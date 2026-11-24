# How a new link becomes an entry

Send Claude the link (X post, YouTube video, article or site) and say "add this to the After Effects hub". Claude does the rest; this file records the steps so the result is always the same.

1. **Capture.**
   - X posts and articles: Apify (`xquik/x-tweet-scraper`, `xquik/x-article-scraper`, replies via `apidojo/tweet-scraper`).
   - YouTube: transcript, chapters and description via `johnvc/YoutubeTranscripts`.
   - Websites: normal fetch first, then Apify `apify/web-fetch` if blocked. Verify every link before it goes in.
2. **Write the entry.** Add `content/eNN-short-title.md`. Videos become concise articles with timestamp links. Guides cite their sources at the end.
3. **Register it.** Add the entry to `sources/entries.json` (id, file, title, kind, author, author_url, date, source, cover, summary, tags, and template_count where relevant) and its images to `sources/media-manifest.json` (path, original, mirror, kind, entry, title).
4. **Log the sources** in `sources/SOURCES.md`.
5. **Push.** The workflow downloads the images into `docs/media/`, switches links to local copies, and rebuilds the README and the website.

New template sites go straight into `content/e03-after-effects-templates.md`, in the right group, after a duplicate check.
