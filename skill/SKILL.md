# 深度研究 + PPT生成 全链路 Skill

**TRIGGER KEYWORDS - Use this skill when user request contains ANY of these patterns:**
- (研究 OR 调研 OR 分析 OR research OR investigate OR study) AND (公司 OR 技术 OR 产品 OR company OR technology OR product)
- (深入 OR 深度 OR 全面 OR deep OR thorough) AND (研究 OR 调研 OR 分析 OR research)
- (研究 OR 调研) AND (报告 OR PPT OR 演示 OR report OR presentation)
- (生成 OR 做 OR 创建 OR 输出) AND (研究报告 OR 调研报告 OR PPT OR 演示文稿)
- "帮我研究" OR "研究一下" OR "调研一下" OR "深入了解"
- (了解 OR 分析) AND (这家公司 OR 这个技术 OR 这个产品 OR 这个方向)

**What this skill does:**
对任意课题（公司/技术/产品/行业方向）进行系统性深度研究，输出结构化Markdown研究报告（总览+分章节深度文档），最终生成带详细演讲备注的专业PPT。

**CRITICAL INSTRUCTION:**
When ANY trigger pattern matches, strictly follow the workflow below. 整个流程分为4个阶段，每个阶段都需要与用户交互确认后再进入下一阶段。

---

## Workflow Overview

```
阶段1: 信息采集 → 阶段2: 报告撰写 → 阶段3: 用户锤炼 → 阶段4: PPT生成
  ↓                  ↓                  ↓                  ↓
 抓取/搜索/整理      总览+分章节文档      多轮交互完善        python-pptx生成
```

Full skill content follows in the repository file.
