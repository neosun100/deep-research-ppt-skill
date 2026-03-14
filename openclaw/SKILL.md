# Deep Research → PPT Skill (OpenClaw Edition)

## Description
Systematically research any topic (company/technology/product/industry), output structured Markdown reports with deep-dive chapters, then generate professional PPT with detailed speaker notes using python-pptx.

## Triggers
- (研究 OR 调研 OR 分析 OR research) AND (公司 OR 技术 OR 产品 OR company OR technology)
- "帮我研究" OR "研究一下" OR "调研一下" OR "深入了解"
- (生成 OR 输出) AND (研究报告 OR PPT OR 演示文稿)

## Workflow

### Phase 1: Information Gathering
1. Confirm research scope with user
2. Plan research dimensions (9 dimensions: basics/products/market/funding/competition/awards/strategy/tech/talent)
3. Scrape all pages from provided URLs (homepage + map + all subpages)
4. Coverage check: verify all URLs scraped, fill gaps
5. Third-party search: funding data, industry rankings, competitor analysis
6. Recursive deepening: follow new topics found in search results
7. Present draft report in conversation

### Phase 2: Report Writing
- Create `{topic}-research/` with README + 00-overview + 01~0N deep chapters
- Each chapter: positioning, metrics, architecture (with images), features, results, competitor comparison, key takeaways
- Embed all website images, use heredoc for large files

### Phase 3: User Refinement
- Multiple rounds of feedback and iteration
- Confirm PPT outline before generation

### Phase 4: PPT Generation
- python-pptx, 16:9, dark theme matching topic
- Split build into 4 scripts (5-8 slides each), chain pptx files
- Speaker notes: 200-500 chars/content page, ≥5000 total, conversational style
- Verify: every slide has notes, total chars ≥5000

## Color Schemes
| Topic | Background | Primary | Accent |
|---|---|---|---|
| Fintech | #061222 | #00D4FF | #FFB800 |
| AI/ML | #0F0A2E | #A85CFF | #00E676 |
| Cloud | #232F3E | #FF9900 | #5ACBF0 |
| Blockchain | #0A0A1A | #00FF88 | #FF4444 |
| General | #1A2332 | #4A90D9 | #F5A623 |
