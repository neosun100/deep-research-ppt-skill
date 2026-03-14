# 🔬 Deep Research → PPT Skill

> 对任意课题进行系统性深度研究，输出结构化Markdown报告 + 带详细演讲备注的专业PPT

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## ✨ 功能

- 🔍 **系统性信息采集** — 官网全站抓取 + 第三方交叉验证 + 递归深入搜索
- 📝 **结构化报告** — 总览 + 分章节深度文档（含架构图、性能指标、竞品对比）
- 🎨 **炫酷PPT生成** — 深色科技风、大数字指标、圆角卡片、颜色编码
- 🎤 **详尽演讲备注** — 每页200-500字，总计7000+字，拿着就能演讲30-45分钟
- 🔄 **多轮锤炼** — 用户交互式完善，直到满意再生成PPT

## 🚀 安装

### Kiro CLI

```bash
git clone https://github.com/neosun100/deep-research-ppt-skill.git
cp -r deep-research-ppt-skill/skill ~/.kiro/skills/deep-research-ppt
```

### Claude Code (CC)

```bash
# 项目级（推荐）
git clone https://github.com/neosun100/deep-research-ppt-skill.git
mkdir -p .claude
cp deep-research-ppt-skill/claude-code/CLAUDE.md .claude/

# 全局级
cat deep-research-ppt-skill/claude-code/CLAUDE.md >> ~/.claude/CLAUDE.md
```

### OpenClaw

```bash
git clone https://github.com/neosun100/deep-research-ppt-skill.git
cp -r deep-research-ppt-skill/openclaw/ ~/.openclaw/skills/deep-research-ppt/
```

## 📖 使用方法

在任意支持的AI编程助手中，输入触发语句：

```
帮我研究华锐技术 https://www.archforce.cn/
深入调研一下这家公司
研究一下这个技术方向，输出PPT
```

Skill自动触发，按4个阶段执行：

```
阶段1: 信息采集 → 阶段2: 报告撰写 → 阶段3: 用户锤炼 → 阶段4: PPT生成
  ↓                  ↓                  ↓                  ↓
 抓取/搜索/整理      总览+分章节文档      多轮交互完善        python-pptx生成
```

### 阶段详解

**阶段1 信息采集：**
- 抓取用户提供的所有链接（主页+站点地图+所有子页面）
- 覆盖率检查：对照sitemap确认无遗漏
- 第三方搜索：融资(CB Insights/PitchBook)、行业榜单(Forbes/IDC)、竞品对比
- 递归深入：从搜索结果发现新话题继续追踪

**阶段2 报告撰写：**
- 创建 `{课题}-research/` 目录
- `00-总览.md` — 公司全貌、融资、产品体系、市场地位
- `01~0N-{子主题}.md` — 每个技术/产品的深度分析（含架构图、性能指标、竞品对比、关键认知）

**阶段3 用户锤炼：**
- 用户审阅报告，提出反馈
- 多轮迭代完善，直到确认完整
- 确认PPT大纲后进入生成

**阶段4 PPT生成：**
- 自动选择匹配主题的配色方案
- python-pptx分段构建（每段5-8页避免超时）
- 每页带200-500字详尽演讲备注
- 最终验证：页数、备注字数、覆盖完整性

## 🎨 PPT配色方案

| 主题 | 底色 | 主色 | 强调色 | 效果 |
|---|---|---|---|---|
| 金融科技 | 深蓝 #061222 | 青 #00D4FF | 金 #FFB800 | 科技感+信任感 |
| AI/ML | 深紫 #0F0A2E | 紫 #A85CFF | 绿 #00E676 | 未来感+智能感 |
| 云计算 | 深灰 #232F3E | 橙 #FF9900 | 蓝 #5ACBF0 | 专业稳重 |
| 区块链 | 暗黑 #0A0A1A | 绿 #00FF88 | 红 #FF4444 | 赛博朋克 |
| 通用 | 深蓝灰 #1A2332 | 蓝 #4A90D9 | 橙 #F5A623 | 商务专业 |

## 📊 质量标准

| 维度 | 标准 |
|---|---|
| 备注字数 | 内容页 ≥200字，总计 ≥5000字 |
| 演讲时长 | 拿着备注可完成30-45分钟演讲 |
| PPT页数 | 20-35页，16:9宽屏 |
| 信息覆盖 | 官网所有产品页+第三方数据源交叉验证 |
| 设计风格 | 深色背景+高对比高亮+大数字指标+圆角卡片 |

## 📁 项目结构

```
deep-research-ppt-skill/
├── README.md                    # 本文件
├── LICENSE                      # MIT License
├── skill/
│   └── SKILL.md                 # 核心Skill定义（Kiro格式）
├── claude-code/
│   └── CLAUDE.md                # Claude Code适配版
├── openclaw/
│   └── SKILL.md                 # OpenClaw适配版
└── examples/
    └── archforce/               # 华锐技术研究示例
        ├── README.md
        ├── 00-总览.md
        ├── 01-基础软件全栈.md
        └── ppt/build_p1.py
```

## 🤝 贡献

欢迎提交PR！特别欢迎：
- 新的PPT配色方案和页面布局模板
- 更多AI编程助手的适配（Cursor、Windsurf等）
- 更好的备注写作模板和示例
- Bug修复和文档改进

## 📄 License

MIT
