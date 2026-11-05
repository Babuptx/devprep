# DevPrep / Prep Pro — Technical Interview Prep

A public, static interview preparation site covering Software Engineering, Data, Infrastructure and AI Engineering.

## Version 1.1 — modular, lazy-loaded content

- 4 categories and 9 curated questions with basic answers, strong answers, takeaways and Mermaid visualizations.
- The HTML application shell is kept separate from the content. Its navigation uses `data/manifest.json`; each category is loaded on demand.
- Selected topic JSON is cached in memory during the browsing session, so revisiting a topic does not re-download it.
- No backend, API keys, user login, personal information or build pipeline is required.

## Repository structure

```text
index.html                 # Small application shell and rendering logic
README.md                  # Deployment / maintenance notes
data/
  manifest.json            # Sidebar topic metadata and paths
  system-design.json       # System design questions
  databases.json           # Database and caching questions
  ai-engineering.json      # AI engineering questions
  performance.json         # Performance / reliability questions
```

## GitHub Pages

Repository: `https://github.com/Babuptx/devprep`

In **Settings → Pages**, set Source = **Deploy from a branch**, Branch = **main**, Folder = **/ (root)** and save.

Expected site URL after Pages deploys: `https://babuptx.github.io/devprep/`.

For local previews, serve the repository through an HTTP server (e.g. `python -m http.server 8000`) rather than opening `index.html` with the `file://` scheme. Browser fetch restrictions can block JSON loading from a local file URL.

## Adding new questions

1. Edit only the relevant `data/<topic>.json` file. Each entry follows:

```json
{
  "q": "Question text",
  "basic": "A short, shallow answer",
  "strong": "A clear, detailed answer; limited HTML markup is supported",
  "takeaway": "One key lesson",
  "mermaid": "graph TD\n A --> B",
  "links": []
}
```

2. To introduce a **new category**, create `data/<new-id>.json` and add its metadata (`id`, `title`, `desc`, `icon`, `file`, `questionCount`) to `data/manifest.json`.
3. Keep content public/general-purpose; never include a candidate's résumé, private interview documents or personal identifiers.
4. Validate JSON, Mermaid syntax, mobile layout and all categories before release.
5. Publish in small commits or pull requests, targeting 50 → 100 → 150 → 200 Q&As.

## Notes

- Navigation manifest is small; all detailed question/diagram text is fetched only when needed.
- The POC uses Tailwind, Mermaid and Google Fonts via CDNs; an internet connection is needed.
- Topic files should remain moderately sized; for particularly large topics, split them further into subtopics and register each in the manifest.
