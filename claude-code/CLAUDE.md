# Deep Research → PPT Skill (Claude Code Edition)

When the user asks to research a company, technology, product, or industry topic and generate a report or PPT, follow this workflow strictly.

## Trigger Patterns

Activate when user message contains:
- "研究" / "调研" / "分析" / "research" combined with a topic
- "深入了解" / "帮我研究" / "调研一下"
- Request for "研究报告" / "PPT" / "演示文稿"

## Workflow: 4 Phases

### Phase 1: Systematic Information Gathering

1. **Confirm scope** with user: what to research, links provided, depth needed, output format
2. **Plan research dimensions**: basics, products, market, funding, competition, awards, strategy, tech, talent
3. **Scrape primary sources**: homepage + sitemap discovery + all subpages (products, about, news, careers)
4. **Coverage check**: verify all discovered URLs have been scraped, fill gaps immediately
5. **Third-party search**: funding (CB Insights/PitchBook), rankings (Forbes/IDC/KPMG), competitors, tech articles
6. **Recursive deepening**: when search results reveal new topics, continue searching until saturated
7. **Present draft report** in conversation for user review before writing files

### Phase 2: Structured Report Writing

Create `{topic}-research/` directory with:
- `README.md` — index + key data summary
- `00-{topic}总览.md` — main report (company overview, funding, product matrix, timeline)
- `01~0N-{subtopic}.md` — deep-dive chapters (each with: positioning, metrics table, architecture analysis with diagrams/images, features, use cases, business results, competitor comparison, "key takeaways for team")

**Rules**: embed all website images as `![desc](URL)`, use heredoc for large files, keep each file 200-350 lines.

### Phase 3: User Refinement (Interactive)

- Submit report for user review, iterate based on feedback
- May require multiple rounds until user confirms completeness
- Confirm PPT outline before proceeding

### Phase 4: PPT Generation (python-pptx)

**Design**: dark background + high-contrast highlights, big number metrics, rounded cards, color-coded sections, chapter dividers with decorative bars.

**Color schemes** (auto-select by topic):
- Fintech: #061222 bg, #00D4FF cyan, #FFB800 gold
- AI/ML: #0F0A2E bg, #A85CFF purple, #00E676 green
- Cloud: #232F3E bg, #FF9900 orange, #5ACBF0 blue

**Build strategy**: split into 4 scripts (5-8 slides each), inline all helper functions, chain pptx files.

**Speaker notes** (CRITICAL): content pages 200-500 chars, total ≥5000 chars, conversational style, explain data meaning, use analogies. Every slide MUST have notes.

**Verify**: print slide count, per-slide notes char count, total chars.
