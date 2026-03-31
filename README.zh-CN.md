# AI 智能体的营销技能

专注于营销任务的 AI 智能体技能集合。为技术营销人员和创始人构建，帮助他们使用 AI 编码智能体处理转化率优化、文案撰写、SEO、分析和增长工程。适用于 Claude Code、OpenAI Codex、Cursor、Windsurf 以及任何支持 [Agent Skills 规范](https://agentskills.io) 的智能体。

[中文版本](README.zh-CN.md) | [English Version](README.md)

由 [Corey Haines](https://corey.co?ref=marketingskills) 构建。需要实际帮助？查看 [Conversion Factory](https://conversionfactory.co?ref=marketingskills) — Corey 的转化率优化、落地页和增长策略机构。想了解更多营销知识？订阅 [Swipe Files](https://swipefiles.com?ref=marketingskills)。想要一个使用这些技能成为你的 CMO 的自主 AI 智能体？试试 [Magister](https://magistermarketing.com?ref=marketingskills)。

不熟悉终端和编码智能体？查看配套指南 [Coding for Marketers](https://codingformarketers.com?ref=marketingskills)。

**欢迎贡献！** 发现改进技能的方法或有新技能要添加？[提交 PR](#贡献)。

遇到问题或有疑问？[打开 issue](https://github.com/coreyhaines31/marketingskills/issues) — 我们很乐意提供帮助。

## 什么是技能？

技能是为 AI 智能体提供特定任务的专业知识和工作流程的 Markdown 文件。当你将这些添加到项目中时，你的智能体可以识别你何时在处理营销任务，并应用正确的框架和最佳实践。

## 技能如何协同工作

技能相互引用并建立在共享上下文之上。`product-marketing-context` 技能是基础 — 所有其他技能首先检查它，以在执行任何操作之前了解你的产品、受众和定位。

```
                            ┌──────────────────────────────────────┐
                            │      product-marketing-context       │
                            │    (所有其他技能首先读取)           │
                            └──────────────────┬───────────────────┘
                                               │
    ┌──────────────┬─────────────┬─────────────┼─────────────┬──────────────┬──────────────┐
    ▼              ▼             ▼             ▼             ▼              ▼              ▼
┌──────────┐ ┌──────────┐ ┌──────────┐ ┌────────────┐ ┌──────────┐ ┌─────────────┐ ┌───────────┐
│  SEO 和  │ │   CRO    │ │内容和    │ │  付费和    │ │ 增长和   │ │  销售和     │ │  策略     │
│  内容    │ │          │ │  文案    │ │  测量      │ │ 留存     │ │  GTM        │ │           │
├──────────┤ ├──────────┤ ├──────────┤ ├────────────┤ ├──────────┤ ├─────────────┤ ├───────────┤
│seo-audit │ │page-cro  │ │copywritng│ │paid-ads    │ │referral  │ │revops       │ │mktg-ideas │
│ai-seo    │ │signup-cro│ │copy-edit │ │ad-creative │ │free-tool │ │sales-enable │ │mktg-psych │
│site-arch │ │onboard   │ │cold-email│ │ab-test     │ │churn-    │ │launch       │ │customer-  │
│programm  │ │form-cro  │ │email-seq │ │analytics   │ │ prevent  │ │pricing      │ │research   │
│schema    │ │popup-cro │ │social    │ │            │ │          │ │competitor   │ │           │
│content   │ │paywall   │ │          │ │            │ │          │ │             │ │           │
└────┬─────┘ └────┬─────┘ └────┬─────┘ └─────┬──────┘ └────┬─────┘ └──────┬──────┘ └─────┬─────┘
     │            │            │              │             │              │              │
     └────────────┴─────┬──────┴──────────────┴─────────────┴──────────────┴──────────────┘
                        │
         技能相互交叉引用：
           copywriting ↔ page-cro ↔ ab-test-setup
           revops ↔ sales-enablement ↔ cold-email
           seo-audit ↔ schema-markup ↔ ai-seo
           customer-research → copywriting, page-cro, competitor-alternatives
```

请参阅每个技能的 **相关技能** 部分，了解完整的依赖关系图。

## 可用技能

<!-- SKILLS:START -->
| 技能 | 描述 |
|-------|-------------|
| [ab-test-setup](skills/ab-test-setup/) | 当用户想要规划、设计或实施 A/B 测试或实验时。也适用于用户提及 "A/B... |
| [ad-creative](skills/ad-creative/) | 当用户想要生成、迭代或扩展广告创意 — 标题、描述、主要文本或完整广告... |
| [ai-seo](skills/ai-seo/) | 当用户想要优化内容以适应 AI 搜索引擎、被 LLM 引用或出现在 AI 生成的答案中... |
| [analytics-tracking](skills/analytics-tracking/) | 当用户想要设置、改进或审计分析跟踪和测量时。也适用于用户提及... |
| [churn-prevention](skills/churn-prevention/) | 当用户想要减少流失、构建取消流程、设置保留优惠、恢复失败付款或... |
| [cold-email](skills/cold-email/) | 编写获得回复的 B2B 冷邮件和后续序列。适用于用户想要编写冷外展邮件... |
| [competitor-alternatives](skills/competitor-alternatives/) | 当用户想要创建竞争对手比较或替代页面以进行 SEO 和销售支持时。也适用于... |
| [content-strategy](skills/content-strategy/) | 当用户想要规划内容策略、决定创建什么内容或确定要涵盖什么主题时。也... |
| [copy-editing](skills/copy-editing/) | 当用户想要编辑、审查或改进现有营销文案时。也适用于用户提及 "编辑此... |
| [copywriting](skills/copywriting/) | 当用户想要为任何页面编写、重写或改进营销文案 — 包括主页、落地页... |
| [customer-research](skills/customer-research/) | 当用户想要进行、分析或综合客户研究 — 包括访谈记录、调查、支持工单、评论挖掘、Reddit/G2/论坛研究、人物角色生成和客户声音 (VOC)... |
| [email-sequence](skills/email-sequence/) | 当用户想要创建或优化电子邮件序列、 drip 活动、自动电子邮件流程或生命周期电子邮件... |
| [form-cro](skills/form-cro/) | 当用户想要优化任何非注册/注册表单 — 包括线索捕获表单、联系表单... |
| [free-tool-strategy](skills/free-tool-strategy/) | 当用户想要规划、评估或构建用于营销目的的免费工具 — 线索生成、SEO 价值或... |
| [launch-strategy](skills/launch-strategy/) | 当用户想要规划产品发布、功能公告或发布策略时。也适用于用户... |
| [lead-magnets](skills/lead-magnets/) | 当用户想要创建、规划或优化用于电子邮件捕获或线索生成的铅磁铁时。也适用于... |
| [marketing-ideas](skills/marketing-ideas/) | 当用户需要为其 SaaS 或软件产品提供营销创意、灵感或策略时。也适用于... |
| [marketing-psychology](skills/marketing-psychology/) | 当用户想要将心理学原理、心理模型或行为科学应用于营销时。也适用于... |
| [onboarding-cro](skills/onboarding-cro/) | 当用户想要优化注册后入职、用户激活、首次运行体验或价值实现时间时。也... |
| [page-cro](skills/page-cro/) | 当用户想要优化、改进或增加任何营销页面的转化率 — 包括主页、落地... |
| [paid-ads](skills/paid-ads/) | 当用户需要 Google Ads、Meta (Facebook/Instagram)、LinkedIn、Twitter/X 等平台的付费广告活动帮助时... |
| [paywall-upgrade-cro](skills/paywall-upgrade-cro/) | 当用户想要创建或优化应用内付费墙、升级屏幕、追加销售模态框或功能门控时。也适用于... |
| [popup-cro](skills/popup-cro/) | 当用户想要创建或优化用于转化目的的弹出窗口、模态框、覆盖层、滑入或横幅时。也... |
| [pricing-strategy](skills/pricing-strategy/) | 当用户需要定价决策、包装或货币化策略帮助时。也适用于用户提及... |
| [product-marketing-context](skills/product-marketing-context/) | 当用户想要创建或更新其产品营销上下文文档时。也适用于用户提及... |
| [programmatic-seo](skills/programmatic-seo/) | 当用户想要使用模板和数据大规模创建 SEO 驱动的页面时。也适用于用户提及... |
| [referral-program](skills/referral-program/) | 当用户想要创建、优化或分析推荐计划、联盟计划或口碑策略时... |
| [revops](skills/revops/) | 当用户需要收入运营、线索生命周期管理或营销到销售交接流程帮助时... |
| [sales-enablement](skills/sales-enablement/) | 当用户想要创建销售资料、演示文稿、单页材料、异议处理文档或演示脚本时。也... |
| [schema-markup](skills/schema-markup/) | 当用户想要在其网站上添加、修复或优化 schema 标记和结构化数据时。也适用于... |
| [seo-audit](skills/seo-audit/) | 当用户想要审计、审查或诊断其网站上的 SEO 问题时。也适用于用户提及 "SEO... |
| [signup-flow-cro](skills/signup-flow-cro/) | 当用户想要优化注册、账户创建或试用激活流程时。也适用于用户... |
| [site-architecture](skills/site-architecture/) | 当用户想要规划、映射或重组其网站的页面层次结构、导航、URL 结构或内部... |
| [social-content](skills/social-content/) | 当用户需要为 LinkedIn、Twitter/X、Instagram 等平台创建、安排或优化社交媒体内容时... |
<!-- SKILLS:END -->

## 安装

### 选项 1：CLI 安装（推荐）

使用 [npx skills](https://github.com/vercel-labs/skills) 直接安装技能：

```bash
# 安装所有技能
npx skills add coreyhaines31/marketingskills

# 安装特定技能
npx skills add coreyhaines31/marketingskills --skill page-cro copywriting

# 列出可用技能
npx skills add coreyhaines31/marketingskills --list
```

这会自动安装到你的 `.agents/skills/` 目录（并为 Claude Code 兼容性符号链接到 `.claude/skills/`）。

### 选项 2：Claude Code 插件

通过 Claude Code 的内置插件系统安装：

```bash
# 添加市场
/plugin marketplace add coreyhaines31/marketingskills

# 安装所有营销技能
/plugin install marketing-skills
```

### 选项 3：克隆和复制

克隆整个仓库并复制 skills 文件夹：

```bash
git clone https://github.com/coreyhaines31/marketingskills.git
cp -r marketingskills/skills/* .agents/skills/
```

### 选项 4：Git 子模块

添加为子模块以便于更新：

```bash
git submodule add https://github.com/coreyhaines31/marketingskills.git .agents/marketingskills
```

然后从 `.agents/marketingskills/skills/` 引用技能。

### 选项 5：分叉和自定义

1. 分叉此仓库
2. 根据你的特定需求自定义技能
3. 将你的分叉克隆到你的项目中

### 选项 6：SkillKit（多智能体）

使用 [SkillKit](https://github.com/rohitg00/skillkit) 在多个 AI 智能体（Claude Code、Cursor、Copilot 等）之间安装技能：

```bash
# 安装所有技能
npx skillkit install coreyhaines31/marketingskills

# 安装特定技能
npx skillkit install coreyhaines31/marketingskills --skill page-cro copywriting

# 列出可用技能
npx skillkit install coreyhaines31/marketingskills --list
```

## 从 v1.0 升级

技能现在使用 `.agents/` 而不是 `.claude/` 作为产品营销上下文文件。移动你现有的上下文文件：

```bash
mkdir -p .agents
mv .claude/product-marketing-context.md .agents/product-marketing-context.md
```

技能仍然会检查 `.claude/` 作为后备，所以如果你不这样做，不会有任何问题。

## 使用

安装后，只需让你的智能体帮助你完成营销任务：

```
"帮我优化这个落地页的转化率"
→ 使用 page-cro 技能

"为我的 SaaS 编写主页文案"
→ 使用 copywriting 技能

"为注册设置 GA4 跟踪"
→ 使用 analytics-tracking 技能

"创建一个 5 封邮件的欢迎序列"
→ 使用 email-sequence 技能
```

你也可以直接调用技能：

```
/page-cro
/email-sequence
/seo-audit
```

## 技能类别

### 转化率优化
- `page-cro` - 任何营销页面
- `signup-flow-cro` - 注册流程
- `onboarding-cro` - 注册后激活
- `form-cro` - 线索捕获表单
- `popup-cro` - 模态框和覆盖层
- `paywall-upgrade-cro` - 应用内升级时刻

### 内容与文案
- `copywriting` - 营销页面文案
- `copy-editing` - 编辑和润色现有文案
- `cold-email` - B2B 冷外展邮件和序列
- `email-sequence` - 自动电子邮件流程
- `social-content` - 社交媒体内容

### SEO 与发现
- `seo-audit` - 技术和页面 SEO
- `ai-seo` - AI 搜索优化（AEO、GEO、LLMO）
- `programmatic-seo` - 规模化页面生成
- `site-architecture` - 页面层次结构、导航、URL 结构
- `competitor-alternatives` - 比较和替代页面
- `schema-markup` - 结构化数据

### 付费与分发
- `paid-ads` - Google、Meta、LinkedIn 广告活动
- `ad-creative` - 批量广告创意生成和迭代
- `social-content` - 社交媒体调度和策略

### 测量与测试
- `analytics-tracking` - 事件跟踪设置
- `ab-test-setup` - 实验设计

### 留存
- `churn-prevention` - 取消流程、保留优惠、催缴、付款恢复

### 增长工程
- `free-tool-strategy` - 营销工具和计算器
- `referral-program` - 推荐和联盟计划

### 策略与货币化
- `marketing-ideas` - 140 个 SaaS 营销创意
- `marketing-psychology` - 心理模型和心理学
- `launch-strategy` - 产品发布和公告
- `pricing-strategy` - 定价、包装和货币化

### 销售与 RevOps
- `revops` - 线索生命周期、评分、路由、管道管理
- `sales-enablement` - 销售演示文稿、单页材料、异议文档、演示脚本

## 贡献

发现改进技能的方法？有新技能要建议？欢迎 PR 和 issue！

请参阅 [CONTRIBUTING.md](CONTRIBUTING.md) 了解添加或改进技能的指南。

## 许可证

[MIT](LICENSE) - 随你所愿使用这些技能。