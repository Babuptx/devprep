# DevPrep / Prep Pro — 1,200 Technical Interview Practice Questions

Free public static study guide with an original, modular question bank for software engineering, cloud, data/AI, security, reliability, careers, coding challenges, agentic AI, enterprise applications and mock interviews.

**Live:** https://babuptx.github.io/devprep/  
**Repository:** https://github.com/Babuptx/devprep

## Release v4.0

- **1,200 questions**: previous 700 retained and 500 new original practice Q&As added.
- **10 collapsible major groups, 21 knowledge areas**, all groups collapsed initially.
- The **five new groups** contain: Coding Challenges & Algorithmic Thinking (150), Agentic AI & Developer Automation (100), Industry IT & Enterprise Applications (125), Production Troubleshooting & SRE (75), and Mock Interviews & Case Studies (50).
- Coding challenges intentionally use **thinking hints**, reasoning, edge cases, and target complexity instead of full working code.
- Agentic AI includes design, evaluation, failure analysis and governance scenarios. Enterprise IT covers insurance, telecommunications, manufacturing, utilities, and financial services. SRE covers triage, recovery and postmortems. Mock interviews teach answer structure and handling follow-up questions.
- Consistent inline SVG icons appear in the group navigation, topics, and reading pane; no new icon-library dependency.
- One **slim fixed header** carries the Prep Pro brand, current area, local clock, font family/size controls, expand answers, and theme toggle.
- A **tiny fixed disclaimer footer** remains visible. Compact colored group bars and global navigation expand/collapse stay in the sidebar.
- Every topic is a separate JSON file and loaded **on demand**, retaining in-browser caching and topic search.

## Structure

```text
index.html                      Application shell, responsive navigation and UI
README.md                       Release and maintenance documentation
data/manifest.json              Navigation/group metadata, counts, paths
 data/*.json                     21 independent topic JSON files
research/SOURCES.md             Prior public-source coverage and editorial policy
```

## Question counts

| Group | New v4.0 questions |
|---|---:|
| Coding Challenges & Algorithmic Thinking | 150 |
| Agentic AI & Developer Automation | 100 |
| Industry IT & Enterprise Applications | 125 |
| Production Troubleshooting & SRE | 75 |
| Mock Interviews & Case Studies | 50 |
| **Total added** | **500** |
| **All questions after release** | **1,200** |

## Editorial integrity

The question sets are **original educational scenarios** informed by broad public discussion of interview topics and enterprise engineering practice. They are **not** verbatim confidential interview prompts, verified question lists from named employers, or empirically ranked by interview frequency. Responses are supplementary teaching material and must be checked against official technical references for consequential decisions.

## Updating data

Edit a single topic JSON file; update its `questionCount` in the manifest. Each Q&A keeps `q`, `basic`, `strong`, `takeaway`, optional `mermaid`, and optional `links`. Recent questions also include difficulty, industry tags, provenance, and version metadata.

Validate with `python -m json.tool` for all JSON and `node --check` for inline app scripts before deployment. Use GitHub Pages from `main` / root. Local previews require a local HTTP server; direct `file://` opening may block `fetch` for topic JSON. Static-site CDN resources require internet access.

## Privacy and accessibility

No login, API key, analytics, data collection or backend is required. Typography preferences are stored only in the visitor's browser, and the live clock uses the visitor's device time. The Q&A content and source remain available in the public repository.

Feedback and corrections: **babuptx@gmail.com**.
