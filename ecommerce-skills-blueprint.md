# ecommerce-skills · 全球电商经营者 Skills 库
**Blueprint v1.0 — 供 Claude Code 生成详细内容使用**

---

## 项目概览

| 字段 | 内容 |
|---|---|
| 仓库名 | `{your-handle}/ecommerce-skills` |
| 定位 | 面向全球电商经营者的 AI Agent Skills 库，覆盖从选品到售后的完整运营链路 |
| 目标用户 | 跨境电商卖家、DTC 品牌、多平台运营者、电商代运营团队 |
| 平台覆盖 | Amazon、Shopify、TikTok Shop、Shopee、Lazada、Temu、eBay、Walmart |
| 语言 | 双语（English + 中文），每个 SKILL.md 包含两种语言版本 |
| 分发方式 | skills.sh 生态，通过 `npx skills add` 安装 |

---

## 仓库目录结构

```
{your-handle}/ecommerce-skills/
├── README.md
├── skills/
│   ├── product-listing-audit/       # M1
│   ├── keyword-research/            # M1
│   ├── listing-localization/        # M1
│   ├── a-plus-content/              # M1
│   ├── product-photography-brief/   # M1
│   ├── supplier-sourcing/           # M2
│   ├── inventory-forecasting/       # M2
│   ├── freight-routing/             # M2
│   ├── customs-classification/      # M2
│   ├── quality-inspection-brief/    # M2
│   ├── amazon-account-health/       # M3
│   ├── amazon-ppc-audit/            # M3
│   ├── shopify-conversion-audit/    # M3
│   ├── tiktok-shop-ops/             # M3
│   ├── multi-channel-sync/          # M3
│   ├── influencer-outreach/         # M4
│   ├── email-flows-ecommerce/       # M4
│   ├── review-generation/           # M4
│   ├── cross-border-ad-creative/    # M4
│   ├── promo-planning/              # M4
│   ├── product-compliance-check/    # M5
│   ├── vat-gst-compliance/          # M5
│   ├── brand-protection/            # M5
│   ├── sales-data-analysis/         # M6
│   ├── competitor-analysis/         # M6
│   ├── pricing-strategy/            # M6
│   ├── market-entry-research/       # M6
│   ├── customer-dispute-handling/   # M7
│   ├── review-response/             # M7
│   └── return-reduction/            # M7
└── .agents/
    └── ecommerce-context.md         # 用户业务上下文模板
```

每个 skill 子目录包含：
```
skill-name/
├── SKILL.md          # 核心内容（必须）
└── references/       # 引用文档（按需）
    └── *.md
```

---

## SKILL.md 标准模板

> Claude Code 生成每个 SKILL.md 时，必须严格遵循以下结构。

```markdown
# {Skill Name} / {技能名称}

## When to Use / 适用场景
[一句话描述 agent 何时应加载此 skill]
[触发关键词列表]

## Context to Gather / 前置信息收集
[生成任务前需要向用户确认的信息清单]

## Framework / 执行框架
[分阶段的操作步骤、检查清单、决策树]
[包含具体的评判标准、数值门槛、示例]

## Platform Variants / 平台差异
[针对不同平台（Amazon/Shopify/TikTok Shop等）的特殊处理说明]

## Output Format / 输出格式
[报告结构模板、表格格式、推荐交付物形式]

## Common Pitfalls / 常见误区
[该领域最容易犯的错误，帮助 agent 规避]

## Related Skills / 相关技能
[上下游 skill 链接列表]
```

---

## 七大模块详细说明

---

### Module 1：商品与 Listing 管理

**模块目标**：帮助卖家创建和优化高转化率的商品页面

#### `product-listing-audit` ⭐ MVP 优先
- **用途**：对现有 Listing 进行全面质量诊断
- **核心框架**：标题结构检查 → 五点/描述质量 → 图片规范评估 → 关键词覆盖 → 评分与评价状态
- **平台差异**：Amazon（字符限制/A9算法权重）、Shopify（SEO meta）、TikTok Shop（视频封面联动）
- **输出物**：评分卡（0-100分）+ 优化优先级清单
- **触发词**：listing, product page, 商品详情, 标题优化

#### `keyword-research` ⭐ MVP 优先
- **用途**：电商场景下的关键词挖掘与布局规划
- **核心框架**：种子词扩展 → 搜索量/竞争度矩阵 → 买家意图分类（信息/导航/购买）→ 长尾词挖掘 → 关键词地图生成
- **工具引用**：Helium 10、Jungle Scout、亚马逊搜索建议、Google Keyword Planner
- **平台差异**：Amazon（后台 Search Terms 字段限制）、Google SEO（意图导向）、TikTok（话题标签联动）
- **输出物**：关键词分层表（核心/长尾/竞品词）
- **触发词**：keyword, 关键词, search terms, 搜索词

#### `listing-localization`
- **用途**：将现有 Listing 本地化为目标市场语言与文化表达
- **核心框架**：直译 → 文化适配 → 本地合规检查 → 平台规范匹配
- **语言对**：EN→DE/FR/ES/JP/AR/PT（涵盖主流跨境目标市场）
- **注意点**：避免机器直译、单位换算（lbs↔kg、inch↔cm）、法律合规表述（保健品/化妆品禁忌词）
- **输出物**：本地化版本对照表 + 合规风险标注
- **触发词**：localization, translate listing, 本地化, 翻译商品

#### `a-plus-content`
- **用途**：Amazon A+ 内容 / 品牌旗舰店 / Shopify 落地页内容策划
- **核心框架**：品牌故事模块 → 产品卖点可视化 → 对比表格设计 → CTA 布局
- **内容模块类型**：标准比较表、四图文、视频模块、常见问题
- **输出物**：模块内容脚本 + 设计 Brief（可传给设计师）
- **触发词**：A+, EBC, brand story, 品牌故事, 旗舰店

#### `product-photography-brief`
- **用途**：为产品摄影/渲染生成完整拍摄 Brief
- **核心框架**：主图规范（白底/尺寸/主体占比）→ 场景图策划 → 信息图内容规划 → 生活方式图参考
- **平台差异**：Amazon 主图严格规范 vs TikTok Shop 强调动态感
- **输出物**：拍摄清单 + 每张图的用途/构图/文案说明
- **触发词**：photography, product photo, 拍摄, 主图, 产品图

---

### Module 2：供应链与库存

**模块目标**：降低采购成本，优化库存效率，规避物流风险

#### `supplier-sourcing` ⭐ MVP 优先
- **用途**：从零开始寻找和评估供应商
- **核心框架**：平台搜索策略（1688/Alibaba/Made-in-China）→ 初步筛选标准 → 询盘模板 → 打样评估 → 工厂审核（资质/产能/质量体系）→ 价格谈判要点
- **输出物**：供应商对比评分矩阵 + 询盘邮件模板
- **触发词**：supplier, sourcing, 供应商, 采购, 1688, Alibaba

#### `inventory-forecasting`
- **用途**：基于销售数据计算补货时机与数量
- **核心框架**：日均销速计算 → 安全库存设定 → 补货点公式（ROP = 日均销量 × 采购周期 + 安全库存）→ 季节性系数调整 → 滞销品处理策略
- **输出物**：补货计划表（SKU/当前库存/建议补货量/补货时间）
- **触发词**：inventory, reorder, 库存, 补货, 断货

#### `freight-routing`
- **用途**：为货物选择最优物流方案
- **核心框架**：货物属性评估（重量/体积/时效要求/货值）→ 方案对比（海运FCL/LCL/空运/快递/铁路）→ 成本测算 → 风险评估（特货限制/清关风险）
- **输出物**：方案对比表（时效/成本/风险评级）
- **触发词**：freight, shipping, 物流, 运费, 海运, 空运

#### `customs-classification`
- **用途**：确定货物 HS 编码并评估关税成本
- **核心框架**：产品描述标准化 → HS 编码查询路径 → 主要目标市场税率查询（美国/欧盟/英国/澳洲）→ 贸易协定优惠判断 → 合规申报要点
- **注意点**：低报货值风险、特殊品类监管（电池/食品/化妆品）
- **输出物**：HS 编码建议 + 目标市场关税成本测算
- **触发词**：customs, HS code, tariff, 关税, 报关, 海关

#### `quality-inspection-brief`
- **用途**：生成工厂验货标准与检验报告框架
- **核心框架**：AQL 抽样标准选择 → 外观检验标准 → 功能性测试项目 → 包装/标签合规检查 → 缺陷分级（Critical/Major/Minor）→ 不合格品处理流程
- **输出物**：验货 Checklist + 缺陷等级表
- **触发词**：QC, inspection, 验货, 质检, 抽检

---

### Module 3：平台运营

**模块目标**：提升各平台账户健康度与运营效率

#### `amazon-account-health` ⭐ MVP 优先
- **用途**：诊断 Amazon 账户健康状况并制定改善计划
- **核心框架**：账户健康评分解读 → 各指标达标线（ODR<1%/LSR<4%/VTR<4%）→ 绩效通知处理 SOP → 申诉信撰写框架 → 预防性监控清单
- **输出物**：账户健康报告 + 申诉信模板
- **触发词**：account health, suspension, 账户健康, 申诉, 绩效警告

#### `amazon-ppc-audit` ⭐ MVP 优先
- **用途**：审计并优化 Amazon PPC 广告结构与表现
- **核心框架**：广告结构评估（SP/SD/SB 组合）→ 关键词出价分析 → ACoS/RoAS 目标设定 → 否定词优化 → 预算分配逻辑 → Dayparting 策略
- **输出物**：广告诊断报告（问题分级）+ 优化行动清单
- **触发词**：PPC, advertising, ACoS, 广告, 竞价, 投流

#### `shopify-conversion-audit`
- **用途**：诊断 Shopify 独立站转化率瓶颈
- **核心框架**：流量质量评估 → 产品页转化分析 → 购物车/结账流程审查 → 网站速度检测 → 信任背书元素检查 → 移动端适配评估
- **输出物**：转化漏斗诊断报告 + 优化优先级矩阵
- **触发词**：Shopify, conversion rate, CVR, 转化率, 独立站

#### `tiktok-shop-ops`
- **用途**：TikTok Shop 内容电商日常运营 SOP
- **核心框架**：达人合作流程 → 自播间搭建标准 → 商品卡优化 → 流量推广工具（千川/附属计划）→ 数据复盘框架
- **平台特性**：内容即流量，视频/直播与商品强绑定
- **输出物**：周运营计划模板 + 达人合作 Brief 模板
- **触发词**：TikTok Shop, 抖音小店, 达人, 直播带货, 短视频电商

#### `multi-channel-sync`
- **用途**：多平台销售的库存/价格/订单同步策略
- **核心框架**：渠道优先级设定 → 库存分配逻辑 → 价格一致性策略（避免平台比价处罚）→ 工具选型（Linnworks/Sellbrite/ShipStation）→ 风险隔离原则
- **输出物**：多渠道运营架构图 + 工具选型建议
- **触发词**：multi-channel, omnichannel, 多平台, 渠道管理

---

### Module 4：营销与流量

**模块目标**：获取精准流量，提升品牌影响力与复购率

#### `influencer-outreach` ⭐ MVP 优先
- **用途**：KOL/KOC 合作从筛选到执行的完整流程
- **核心框架**：达人画像定义 → 筛选标准（粉丝量/互动率/受众匹配度）→ 初次联系话术 → 合作形式协商（买链接/免费寄样/佣金/付费）→ 内容 Brief 撰写 → 效果追踪方式
- **平台差异**：Instagram/YouTube/TikTok/Pinterest/小红书
- **输出物**：达人合作 Brief 模板 + 效果追踪表
- **触发词**：influencer, KOL, KOC, 达人, 网红, 红人营销

#### `email-flows-ecommerce`
- **用途**：设计电商核心邮件自动化序列
- **核心框架**：弃购挽回序列（3封）→ 新客欢迎序列（5封）→ 复购激活序列 → 售后关怀序列 → 会员/忠诚度邮件
- **工具引用**：Klaviyo、Mailchimp、Omnisend
- **输出物**：每条序列的发送时机/主题行/正文框架
- **触发词**：email, 邮件, abandoned cart, welcome series, Klaviyo

#### `review-generation`
- **用途**：合规地提升平台评价数量与质量
- **核心框架**：平台规则边界梳理（Amazon ToS/Google 政策）→ 包裹内卡设计规范 → 售后跟进话术 → Amazon "Request a Review" 自动化 → 差评预警与拦截
- **注意点**：严禁激励性评价（Amazon 封号风险）
- **输出物**：合规索评 SOP + 包装卡文案模板
- **触发词**：reviews, feedback, 评价, 刷单（反向提醒）, 好评

#### `cross-border-ad-creative`
- **用途**：跨境广告素材的策略框架与创意方向
- **核心框架**：目标受众画像 → 卖点提炼（功能/情感/社会证明）→ 素材类型选择（静态/视频/UGC）→ 钩子公式（痛点/好奇/反常识）→ 本地化注意事项 → A/B 测试框架
- **平台差异**：Meta（Story/Reels）、TikTok（原生感）、Google（购物广告图片规范）
- **输出物**：广告创意 Brief + 测试矩阵
- **触发词**：ad creative, 广告素材, Facebook广告, TikTok广告, 投流

#### `promo-planning`
- **用途**：大促活动（黑五/Prime Day/双11）全周期策划 SOP
- **核心框架**：备货计划（T-90天）→ Listing 优化（T-60天）→ 广告预热（T-30天）→ 活动期执行（价格/库存/广告实时调整）→ 复盘分析
- **输出物**：大促倒计时检查清单 + 活动期监控仪表盘模板
- **触发词**：Black Friday, Prime Day, 双11, 大促, 活动策划

---

### Module 5：合规与法务

**模块目标**：规避跨境经营的法律与平台合规风险

#### `product-compliance-check` ⭐ MVP 优先
- **用途**：检查产品进入目标市场所需的认证与合规要求
- **核心框架**：产品品类判断 → 目标市场法规映射（美国/欧盟/英国/澳洲/日本）→ 认证清单生成（CE/FCC/FDA/REACH/ROHS/UL）→ 测试机构推荐 → 标签合规要求
- **高风险品类**：电子产品、儿童用品、食品/保健品、化妆品
- **输出物**：认证需求清单 + 合规时间轴估算
- **触发词**：compliance, certification, CE, FCC, FDA, 认证, 合规

#### `vat-gst-compliance`
- **用途**：欧美 VAT/GST 注册门槛判断与申报流程指南
- **核心框架**：注册触发条件（销售额门槛）→ 各市场注册流程（英国/德国/法国等欧盟/美国州税/澳洲GST）→ 申报周期与格式 → OSS（欧盟一站式申报）介绍 → 常见风险点
- **输出物**：VAT/GST 注册需求检查表 + 合规行动时间表
- **触发词**：VAT, GST, tax, 税务, 欧洲税, 增值税

#### `brand-protection`
- **用途**：商标注册、侵权监控与维权流程
- **核心框架**：目标市场商标注册优先级 → Amazon Brand Registry 申请流程 → 侵权监控方式（Listing 跟卖/知识产权侵权）→ 投诉/举报 SOP → 律师介入时机判断
- **输出物**：商标保护行动清单 + 侵权投诉模板
- **触发词**：trademark, brand registry, 商标, 跟卖, 侵权

---

### Module 6：数据与决策

**模块目标**：用数据驱动运营决策，识别机会与风险

#### `sales-data-analysis` ⭐ MVP 优先
- **用途**：电商核心经营指标的分析框架
- **核心框架**：核心指标体系（GMV/转化率CVR/客单价/复购率/LTV/退货率）→ 漏斗分析（曝光→点击→加购→购买）→ 广告指标（ACoS/ROAS/TACOS）→ 异常数据诊断 → 同比/环比分析
- **输出物**：经营数据仪表盘模板 + 异常归因分析框架
- **触发词**：data analysis, 数据分析, sales report, ACoS, 转化率, 业绩

#### `competitor-analysis` ⭐ MVP 优先
- **用途**：系统性研究竞争对手的 Listing/定价/关键词/评价策略
- **核心框架**：竞品识别（关键词排名/Best Seller 榜单）→ Listing 拆解（标题/卖点/图片策略）→ 定价策略分析 → 评价内容挖掘（好评/差评高频词）→ 广告投放推测 → 差异化机会识别
- **工具引用**：Jungle Scout、Helium 10、Keepa（价格历史）
- **输出物**：竞品对比矩阵 + 差异化机会清单
- **触发词**：competitor, 竞品, 竞争对手, 对标分析

#### `pricing-strategy`
- **用途**：制定或调整产品定价策略
- **核心框架**：成本结构拆解（货值/头程/平台费/广告/退货）→ 目标利润率设定 → 竞争对手价格区间分析 → 心理定价技巧 → 动态定价触发条件（库存/竞争/季节）→ 促销折扣对利润的影响测算
- **输出物**：定价测算模型（含各成本项）+ 价格调整 SOP
- **触发词**：pricing, price, 定价, 利润, 毛利

#### `market-entry-research`
- **用途**：评估进入新市场或新品类的可行性
- **核心框架**：市场规模初判 → 竞争格局分析（头部玩家/市场集中度）→ 准入壁垒评估（合规/物流/本地化成本）→ 目标客群需求验证 → 首批 MVP 产品选品建议 → 资源需求估算
- **输出物**：市场进入可行性报告（1-pager 格式）
- **触发词**：market research, new market, 市场调研, 新品类, 选品

---

### Module 7：客服与口碑

**模块目标**：提升买家体验，保护账户绩效，降低纠纷损失

#### `customer-dispute-handling` ⭐ MVP 优先
- **用途**：处理买家纠纷、退款申请与平台案件
- **核心框架**：纠纷类型识别（INR未收到/SNAD货不对/拒付款/质量问题）→ 各类型处理决策树 → 沟通话术原则（不认错/不激化/快速响应）→ 证据收集要点 → 升级至平台仲裁时机
- **平台差异**：Amazon A-to-Z / eBay 案件 / PayPal 争议 / Shopify Dispute
- **输出物**：纠纷处理决策树 + 各类型回复模板
- **触发词**：dispute, refund, claim, A-to-Z, 纠纷, 退款, 投诉

#### `review-response`
- **用途**：回复差评/中评，维护品牌形象
- **核心框架**：差评情绪识别（真实问题/无理取闹/竞争对手恶意）→ 公开回复策略（简短/专业/不辩解）→ 私信联系时机与话术 → 差评移除申请条件判断 → 防御性好评积累策略
- **输出物**：差评回复模板库（按问题类型分类）
- **触发词**：negative review, 差评, 评价回复, 1星

#### `return-reduction`
- **用途**：分析并系统性降低退货率
- **核心框架**：退货原因分类（描述不符/质量问题/买家误操作/物流损坏）→ 数据分析识别主因 → 针对性优化措施 → Listing 预期管理 → 包装改善 → 退货流程优化（减少摩擦同时保护账户）
- **输出物**：退货原因分析报告 + 降退货率行动计划
- **触发词**：return, return rate, 退货率, 退货

---

## .agents/ecommerce-context.md 模板

> 用户可在项目根目录创建此文件，供所有 skills 共享业务上下文。

```markdown
# My Ecommerce Business Context

## Business Overview
- Business Type: [e.g., Amazon FBA / Shopify DTC / Multi-channel]
- Main Categories: [e.g., Home & Kitchen, Sports & Outdoors]
- Target Markets: [e.g., US, UK, Germany, Japan]
- Annual Revenue Range: [e.g., $500K - $2M]

## Platform Presence
- Amazon: [Seller Central / Vendor Central / Not active]
- Shopify: [Store URL if applicable]
- TikTok Shop: [Active / Not active]
- Other: []

## Brand & Compliance
- Brand Registered: [Yes / No / In Progress]
- Key Certifications Held: [e.g., CE, FCC]
- VAT Registered In: [e.g., UK, Germany]

## Team & Tools
- Team Size: [Solo / 2-5 / 5+]
- Key Tools: [e.g., Helium 10, Klaviyo, ShipStation]
- Primary Ad Platforms: [e.g., Amazon PPC, Meta, TikTok Ads]

## Current Focus
- Top Priority: [e.g., Scaling Amazon US, Launching EU]
- Biggest Pain Point: [e.g., Rising ACoS, Low conversion rate]
```

---

## MVP 优先级（第一批生成顺序）

| 优先级 | Skill | 理由 |
|---|---|---|
| P0 | `product-listing-audit` | 最高频需求，几乎所有卖家都用得到 |
| P0 | `amazon-ppc-audit` | 广告费是最大痛点，ROI 直接可见 |
| P0 | `competitor-analysis` | 选品/定价/优化的基础，通用性强 |
| P1 | `keyword-research` | 与 listing 和 PPC 强联动 |
| P1 | `supplier-sourcing` | 跨境独特需求，现有 skills 生态空白 |
| P1 | `customer-dispute-handling` | 账户安全高优先级 |
| P1 | `product-compliance-check` | 跨境必须，错误成本极高 |
| P2 | `sales-data-analysis` | 数据驱动决策的基础 |
| P2 | `promo-planning` | 季节性强，需提前规划 |
| P2 | `influencer-outreach` | 品牌增长核心杠杆 |

---

## Claude Code 生成指令

使用此 Blueprint 生成详细 SKILL.md 时，请遵循以下指令：

1. **逐个生成**，每次处理一个 skill
2. **严格遵循** SKILL.md 标准模板结构
3. **内容深度**：每个 SKILL.md 不少于 300 行，包含具体数值门槛、判断标准、示例
4. **双语原则**：关键术语标注英文，框架标题英中对照，正文以英文为主（面向全球用户）
5. **平台差异**：凡涉及平台操作，必须分平台说明
6. **Related Skills**：每个 skill 必须链接至少 2 个相关 skill，形成知识图谱
7. **避免泛泛而谈**：不写通用营销建议，只写电商经营者能直接执行的操作性内容

---

*Blueprint v1.0 · Generated for Claude Code*
