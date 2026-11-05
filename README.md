# DevPrep / Prep Pro — 200 Technical Interview Q&As

**Version 2.0** · Public static study app covering 16 knowledge areas organized into five groups.

## Architecture

- `index.html` is the lightweight UI shell and JavaScript renderer; it does not embed the question bank.
- `data/manifest.json` is the grouped navigation manifest, listing topic files and question counts.
- `data/<topic>.json` is the independent Q&A content for each of the 16 knowledge areas.
- Topic JSON is fetched only upon selection and cached for the browser session.
- 200 total Q&As, including all nine original POC entries; each item includes a quick answer, strong answer and takeaway. Diagrams appear when provided and are intentionally optional for nonvisual questions.
- No accounts, API keys, backend, or personal candidate details are required.

## Publish

GitHub Pages project: https://babuptx.github.io/devprep/.
GitHub repository: https://github.com/Babuptx/devprep.

Pages settings: Settings → Pages → Deploy from a branch → `main` → `/(root)`.

## Editing Q&A content

Add a question to the appropriate file inside `data/`, maintaining the schema keys `q`, `basic`, `strong`, `takeaway`, `mermaid`, `links`. Update `questionCount` in the manifest to keep sidebar counts correct. Keep strong answers technically accurate, concise, and meaningful; include constraints and tradeoffs. When attaching a Mermaid definition, validate it before release.

For local preview, run `python -m http.server 8000` in the repo root and open http://localhost:8000; direct `file://` preview may block JSON fetches.

## Quality criteria

- All JSON files parse; manifest entries point to real topic files.
- Categories are organized into the five approved collapsible groups.
- All Q&A records have unique questions within their topic, valid fields and readable answers.
- HTML and JavaScript syntax pass validation; verify behavior in a live browser after deployment.
