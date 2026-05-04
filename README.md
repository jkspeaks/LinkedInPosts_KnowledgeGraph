# JK Thought Map

An interactive knowledge graph of 20 LinkedIn posts written between January 2025 and April 2026 — visualising topic clusters, writing phases, and thematic connections across 18 topic hubs.

**Live:** [portfolio.jkspeaks.com/thought-map.html](https://portfolio.jkspeaks.com/thought-map.html)

---

## What's in this repo

| Path | Description |
|---|---|
| `thought-map.html` | Standalone interactive graph — the entire app in one file |
| `Obsidian-Vault/` | Tagged markdown notes for every post and topic hub |
| `Obsidian-Vault/Posts/` | 20 post notes with YAML frontmatter and topic wikilinks |
| `Obsidian-Vault/Topics/` | 18 topic hub notes (AgenticAI, EnterpriseAI, Retail, etc.) |
| `Obsidian-Vault/_Dashboard.md` | Overview: post list, topic weights, evolution arc |

---

## The Graph

Built with D3.js v7 as a force-directed knowledge graph. No build step, no dependencies, no backend — open the HTML file in any browser.

**Nodes**
- **Topic hubs** (larger) — coloured by cluster: Core AI · Technical · Domain · Brand
- **Posts** (smaller) — coloured by writing phase (1–4)

**Edges** — a line between a post and a topic means that post covers that topic.

**Clusters**
| Cluster | Topics |
|---|---|
| Core AI | AgenticAI, EnterpriseAI, AIGovernance, AIStrategy |
| Technical | LLM, AIEngineering, AIResearch, MachineLearning, MemoryArchitecture |
| Domain | Retail, Commerce, MarTech, DataStrategy, DataQuality |
| Brand | Frameworks, PracticalAI, PromptEngineering, FutureOfWork |

**Controls**
- Hover a node → highlight connections
- Click a node → open detail panel
- Scroll / pinch → zoom · Drag background → pan
- Year & Cluster filters → focus on a slice
- Search box → jump to any post or topic
- ☀ / 🌙 toggle → light / dark theme

---

## Adding a New Post

Open `thought-map.html` in any text editor. Find the `DATA SECTION` block at the top of the `<script>` tag (marked with a `╔═══╗` border) and add a new entry to the `POSTS` array:

```js
{
  id:      "p021",
  title:   "Your Post Title",
  date:    "2026-05-15",
  format:  "article",          // article | carousel | whitepaper | report
  phase:   4,                  // 1 | 2 | 3 | 4
  summary: "One-line summary of what the post argues.",
  topics:  ["AgenticAI","EnterpriseAI"],
  url:     "https://www.linkedin.com/pulse/your-post-slug"
},
```

Then add a corresponding markdown note in `Obsidian-Vault/Posts/` following the existing format.

---

## Writing Evolution

| Phase | Period | Style |
|---|---|---|
| 1 | Jan – Mar 2025 | Analyst report mode — formal, citation-heavy, third-person |
| 2 | Apr – Aug 2025 | Confidence injection — first-person testing, listicles |
| 3 | Sep 2025 – Feb 2026 | Practitioner narrative — coined frameworks, bold predictions |
| 4 | Mar – Apr 2026 | Most refined — sharp hooks, war-story-led, strongest voice |

---

## Topic Weight

| Topic | Posts |
|---|---|
| AgenticAI | 10 |
| EnterpriseAI | 7 |
| Retail | 6 |
| LLM | 6 |
| AIEngineering | 6 |
| Frameworks | 6 |
| PracticalAI | 5 |
| Commerce | 5 |
| AIGovernance | 4 |
| MarTech | 4 |
| DataStrategy | 4 |
| AIStrategy | 4 |
| AIResearch | 3 |
| PromptEngineering | 2 |
| FutureOfWork | 2 |
| DataQuality | 2 |
| MachineLearning | 1 |
| MemoryArchitecture | 1 |

---

*Built by [JK](https://jkspeaks.com) · Updated through April 2026*
