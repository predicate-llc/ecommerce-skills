# Amazon PPC Audit / 亚马逊广告诊断

> **Bilingual Support**: Respond in the same language the user writes in.
> 根据用户使用的语言（中文或英文）进行回复。

---

## When to Use / 适用场景

Load this skill when a seller wants to audit the structure, efficiency, and performance of their Amazon PPC (Pay-Per-Click) advertising campaigns, or when they want to reduce ACoS, improve ROAS, or restructure their ad account.

**Trigger keywords / 触发关键词**:
`PPC`, `advertising`, `ACoS`, `ROAS`, `广告`, `竞价`, `投流`, `sponsored products`, `亚马逊广告`, `广告优化`, `广告诊断`, `ad audit`, `campaign`, `keyword bids`, `广告预算`, `TACOS`, `广告结构`

---

## Context to Gather / 前置信息收集

Before running the audit, collect the following. Ask only for what is missing.

| # | Information | Why Needed |
|---|---|---|
| 1 | **Marketplace** (Amazon US / UK / DE / JP / etc.) | Benchmark CPCs and ACoS targets vary by market |
| 2 | **Product category** | Category average ACoS and competitive landscape affect target-setting |
| 3 | **Business model** (FBA / FBM / Vendor Central) | Affects margin structure and ACoS targets |
| 4 | **Current ACoS** (overall and by campaign, if available) | Baseline for diagnosis |
| 5 | **Target ACoS or Target ROAS** (if seller has one) | Without a target, audit cannot assess whether performance is acceptable |
| 6 | **Gross margin %** (approximate) | Required to calculate breakeven ACoS |
| 7 | **Monthly ad spend** (approximate) | Context for scale and optimization priority |
| 8 | **Campaign structure** — how many campaigns, types (SP/SB/SD), match types used | Core of structural audit |
| 9 | **Ad data export** (optional but ideal) — bulk file or campaign manager screenshot | Enables keyword-level analysis |
| 10 | **Business goal** — launch, growth, profit, defense | Determines the right ACoS target and optimization direction |

---

## Framework / 执行框架

The audit covers **6 dimensions**. Work through them in order, as later findings often depend on earlier ones.

---

### Step 1: Establish Financial Targets / 确定财务目标

Before diagnosing anything, establish the financial guardrails.

**Breakeven ACoS formula:**
```
Breakeven ACoS = Gross Margin %
```

Example: If a product sells for $30 and COGS + FBA fees + prep costs = $18, then:
- Gross margin = ($30 - $18) / $30 = 40%
- Breakeven ACoS = 40%
- Any campaign with ACoS > 40% is losing money on advertising

**Target ACoS by business goal:**

| Goal | Target ACoS (vs. Breakeven) |
|---|---|
| Aggressive launch (new product) | Breakeven + 5–15% (accept losses for rank) |
| Steady growth | Breakeven - 5–10% (slight profit on ads) |
| Profit maximization | Breakeven - 15–20% (strong profitability) |
| Defense (protect BSR) | Up to Breakeven (maintain position) |

**TACoS (Total Advertising Cost of Sale):**
```
TACoS = Total Ad Spend / Total Revenue (organic + ad)
```
TACoS measures ad efficiency relative to the entire business. As organic rank improves, TACoS should decrease even if ACoS stays flat.

**TACoS benchmarks:**
- New product (<3 months): TACoS 15–25% acceptable
- Established product (6+ months): TACoS 8–15%
- Mature/profitable product: TACoS <8%

---

### Step 2: Campaign Structure Audit / 广告结构诊断

A well-structured ad account separates campaign types, match types, and intent levels.

**The three ad types on Amazon:**

| Type | Abbreviation | Best Use |
|---|---|---|
| Sponsored Products | SP | Core workhorse; drives product detail page traffic |
| Sponsored Brands | SB | Brand awareness; requires Brand Registry |
| Sponsored Display | SD | Retargeting, competitor targeting, audience targeting |

**Recommended campaign structure (for a single ASIN):**

```
Campaign 1: SP — Auto (Discovery)
  └── Ad Group: [ASIN] Auto
      Purpose: Find new keywords; mine search term report

Campaign 2: SP — Manual Exact (Core Keywords)
  └── Ad Group: [ASIN] Exact
      Keywords: Top 5–10 proven converting terms; exact match only
      Purpose: Efficient spend on best performers

Campaign 3: SP — Manual Phrase (Expansion)
  └── Ad Group: [ASIN] Phrase
      Keywords: Core terms in phrase match; captures variants
      Purpose: Capture long-tail searches without overreach

Campaign 4: SP — Manual Broad (Research)
  └── Ad Group: [ASIN] Broad
      Keywords: Category terms; high negative list
      Purpose: Low-bid research; mine new converting terms

Campaign 5: SB — Brand Defense (if Brand Registered)
  └── Headline ad for own brand name; protects brand SERP

Campaign 6: SP — Competitor ASIN Targeting
  └── Product targeting (PT) on competitor ASINs
      Purpose: Poach consideration-stage traffic
```

**Structural issues to flag:**

| Issue | Severity | Description |
|---|---|---|
| All keywords in one campaign | Critical | No budget control; no match-type isolation |
| Auto and manual keywords in same campaign | Critical | Cannot optimize bids separately |
| Broad match without negative keywords | High | Wasted spend on irrelevant searches |
| No exact match campaigns for top terms | High | Overpaying for best keywords via broad/phrase |
| No auto campaign | Medium | Missing keyword discovery opportunity |
| Campaigns not paused for out-of-stock ASINs | Critical | Burning budget with no conversion possible |
| Ad groups with >50 keywords each | Medium | Hard to manage; consider splitting by theme |

---

### Step 3: Keyword & Bid Analysis / 关键词与出价分析

**Keyword performance classification:**

Classify every keyword (or auto target) into one of four buckets using ACoS and spend:

| Bucket | Criteria | Action |
|---|---|---|
| **Stars** | ACoS < target ACoS AND significant spend | Increase bid 10–20%; expand match types |
| **Question Marks** | Low spend (insufficient data: <10 clicks) | Give more time or increase bid slightly to gather data |
| **Cash Cows** | Converting but ACoS slightly above target | Reduce bid 10–15%; do not pause |
| **Dogs** | ACoS >> target OR no conversions with >20 clicks | Reduce bid aggressively or pause; add to negatives |

**Bid adjustment rules:**
- **Bid too high**: ACoS > target × 1.3 → reduce bid by 15–25%
- **Bid too low (not getting impressions)**: Impression share <20% for a core term → increase bid 20–30%
- **No data yet**: <10 clicks → do not change bid; let it run
- **Consistent zero conversions (>30 clicks, 0 orders)**: Pause keyword; add as negative in broader match campaigns

**Keyword harvesting from Search Term Report (STR):**
1. Pull STR for the last 30–60 days
2. Filter for search terms with ≥10 clicks AND ACoS < breakeven → add to exact match campaign
3. Filter for search terms with ≥20 clicks AND 0 conversions → add as negative exact to all relevant campaigns
4. Filter for search terms with brand name (own or competitor) → separate into brand/competitor campaigns

---

### Step 4: Negative Keyword Optimization / 否定词优化

Negative keywords are often the highest-ROI optimization in a PPC audit. Most accounts are under-negated.

**Where to apply negatives:**

| Campaign Type | Negative Match Type | Reasoning |
|---|---|---|
| Auto campaigns | Negative exact + negative phrase | Precise control without blocking broad discovery |
| Broad match campaigns | Negative exact (for zero-converting exact terms) | Prevent spend on known non-converters |
| Phrase match campaigns | Negative exact (for specific bad performers) | Fine-tune without blocking all phrase variants |

**Automatic negative candidates (add without hesitation):**
- Words indicating wrong buyer intent: `free`, `diy`, `how to`, `vs`, `review`, `youtube`
- Wrong product category: e.g., if selling earbuds, negatives: `headphones stand`, `earbud case only`
- Competitor brand names (unless running a competitor targeting campaign intentionally)
- Own brand name (in non-brand campaigns, to prevent cannibalization)
- Irrelevant size/color/material variants: e.g., if only selling in blue, negative: `red`, `green`

**Negative keyword checklist:**
- [ ] Auto campaign has a negative keyword list with ≥20 terms
- [ ] Broad campaigns have negatives from last 60 days of STR analysis
- [ ] "Free" and "how to" type terms are negated across all campaigns
- [ ] Own brand name is negated in non-brand campaigns (to force branded traffic into brand campaign)
- [ ] Product variants not sold (wrong size/color) are negated

---

### Step 5: Budget & Dayparting Strategy / 预算与分时策略

**Budget allocation principles:**

| Campaign Priority | Budget Share |
|---|---|
| Exact match (proven converters) | 40–50% of total |
| Auto (discovery engine) | 20–25% |
| Phrase match (expansion) | 15–20% |
| Broad match (research) | 5–10% |
| Competitor targeting (SP or SD) | 5–10% |
| Sponsored Brands | 10–15% (if Brand Registered) |

**Budget issues to diagnose:**
- **Budget limited**: Campaign hits daily budget before midnight → increase budget or shift to portfolio budgets
- **Underspend**: Campaign has budget but low impression share → bids too low or listing quality suppressing ads
- **Budget imbalance**: 80%+ of spend in one campaign with no experiments → over-reliance on single strategy

**Dayparting (Scheduled bidding):**
Amazon allows bid adjustments by day of week (not hour of day) natively. For hour-level control, use third-party tools (Pacvue, Perpetua, Helium 10 Adtomic).

Analyze performance by day:
- Pull campaign performance report, filter by date
- If weekend ACoS is significantly worse → reduce bids on Fri-Sun or pause low-performers
- If conversion rate peaks on specific days → increase bids on high-conversion days

---

### Step 6: Ad Creative & Placement Quality / 广告素材与位置分析

**Sponsored Products placement analysis:**

Amazon SP ads show in three placements:
1. **Top of Search (TOS)** — highest traffic, highest CPC, highest conversion for most categories
2. **Rest of Search (ROS)** — mid-page, lower CPC, moderate conversion
3. **Product Pages (PP)** — appears on competitor/related product detail pages; lower intent

Pull the Placement Report and compare ACoS by placement:

| Placement | Typical Pattern | Action |
|---|---|---|
| TOS ACoS < target | Increase TOS bid adjustment (up to +900%) | Capture more top-of-search real estate |
| TOS ACoS >> target | Reduce TOS adjustment or set to 0% | Stop overpaying for top positions |
| PP ACoS >> target | Reduce PP adjustment or set to 0% | Product page traffic often less qualified |

**Listing quality gate:**
PPC only converts if the landing page (product listing) converts. If CVR (unit session %) < 10% for a product in a non-commoditized category, fix the listing before increasing ad spend.

CVR benchmarks by category:
- Electronics: 8–12%
- Home & Kitchen: 12–18%
- Apparel: 6–10%
- Supplements/Health: 15–25%
- Toys: 12–20%

If below category benchmark → pause PPC scale-up; run `product-listing-audit` first.

---

### Audit Scoring Summary / 诊断评分

| Dimension | Max | Score |
|---|---|---|
| Financial targets established | 10 | /10 |
| Campaign structure | 25 | /25 |
| Keyword & bid management | 25 | /25 |
| Negative keywords | 20 | /20 |
| Budget & dayparting | 10 | /10 |
| Creative & placement | 10 | /10 |
| **TOTAL** | **100** | **/100** |

---

## Platform Variants / 平台差异

### Amazon US
- Most competitive market; highest CPCs (avg $0.75–$3.00+ for competitive categories)
- Largest keyword volume; deepest search term report data
- Brand Registry required for Sponsored Brands and Sponsored Display audience targeting

### Amazon Europe (DE, FR, IT, ES, UK)
- Cross-marketplace advertising not available (each marketplace has separate campaigns)
- EU CPCs typically 20–40% lower than US for equivalent categories
- Language-specific keyword research required; do not translate US keywords directly

### Amazon Japan (JP)
- Unique consumer behavior; brand trust is critical; CPC can be high in premium categories
- Both Japanese and English keywords perform; include both in campaigns

### Amazon Vendor Central
- AMS (Amazon Marketing Services) has different campaign mechanics than Seller Central
- Vendor-funded coupons and deals interact with PPC differently
- ACoS target logic is different (vendor margin structures are typically less transparent)

---

## Output Format / 输出格式

```
# Amazon PPC Audit Report
Marketplace: [Amazon XX]
Audit Period: [Date range]
Monthly Ad Spend: ~$[X,XXX]
Current ACoS: [X%]
Target ACoS: [X%]
Breakeven ACoS: [X%]

## Overall Score: XX/100

## Executive Summary
[3-sentence summary of biggest issues and estimated improvement potential]

## Critical Issues (Fix within 48 hours)
1. [Issue] — [Action] — [Expected impact on ACoS/spend]

## Priority Optimizations (Fix within 7 days)
2. [Issue] — [Action] — [Expected impact]

## Structural Recommendations (Fix within 30 days)
3. [Issue] — [Action] — [Expected impact]

## Campaign Structure Review
[Table of all campaigns with: name / type / spend / ACoS / status / recommendation]

## Top Keyword Actions
[Table: keyword / match type / clicks / orders / ACoS / action (bid up/down/pause/harvest)]

## Negative Keywords to Add Immediately
[List of 10–20 specific negative terms with match type and rationale]

## Budget Reallocation Recommendation
[Current vs. recommended budget distribution across campaign types]

## Next Review Date
[Recommend reviewing again in X days after implementing changes]
```

---

## Common Pitfalls / 常见误区

1. **Optimizing ACoS without knowing breakeven**
   An ACoS of 35% is excellent for a product with 50% margin but catastrophic for one with 30% margin. Always establish breakeven ACoS before assessing any campaign performance.

2. **Pausing campaigns instead of reducing bids**
   Pausing a campaign loses its performance history and rank signal. Default to bid reduction first; only pause if the keyword/product is genuinely not viable.

3. **Not using Search Term Report regularly**
   The STR is the single most valuable data source in Amazon PPC. Every week or two weeks, new irrelevant search terms are draining budget. Set a recurring calendar reminder.

4. **Running auto and manual in the same campaign**
   This prevents independent bid and budget control. Auto campaigns should always be separate.

5. **Setting the same bid for all match types**
   Exact match keywords convert at a higher rate and deserve higher bids. Broad match is for research and should have the lowest bids. A common ratio is: Exact = 1.0x, Phrase = 0.7x, Broad = 0.4x.

6. **Ignoring placement data**
   Two campaigns with the same average ACoS may have very different placement distributions. One might be profitable at TOS and bleeding money on product pages. Placement-level data unlocks significant optimization.

7. **Scaling spend before fixing listing CVR**
   More traffic to a 5% CVR listing just amplifies losses. If CVR is below category benchmark, fix the listing first. PPC amplifies the listing, it does not fix it.

8. **Treating TACoS and ACoS as interchangeable**
   ACoS only measures ad revenue. TACoS shows whether ads are building organic momentum. A rising ACoS with falling TACoS is actually healthy — it means organic sales are growing faster than ad spend.

---

## Related Skills / 相关技能

- [`product-listing-audit`](../product-listing-audit/SKILL.md) — Fix listing quality before scaling PPC; low CVR makes all ad spend less efficient
- [`keyword-research`](../keyword-research/SKILL.md) — Build the master keyword list that feeds campaign keyword selection
- [`competitor-analysis`](../competitor-analysis/SKILL.md) — Identify competitor ASINs to target and understand the competitive bid landscape
- [`sales-data-analysis`](../sales-data-analysis/SKILL.md) — Interpret overall business metrics alongside PPC performance to see TACoS and full-funnel impact
- [`promo-planning`](../promo-planning/SKILL.md) — PPC strategy must shift during major promotions (budget increases, bid adjustments, defensive campaigns)

---

## Terminology / 术语对照

| English | 中文 | 说明 |
|---|---|---|
| PPC (Pay-Per-Click) | 按点击付费广告 | 亚马逊广告的计费模式 |
| Sponsored Products (SP) | 商品推广 | 最常用的广告类型，展示在搜索结果和详情页 |
| Sponsored Brands (SB) | 品牌推广 | 需要品牌备案，展示品牌Logo和多商品 |
| Sponsored Display (SD) | 展示型推广 | 支持再营销和受众定向 |
| ACoS (Advertising Cost of Sale) | 广告销售成本比 | 广告花费 ÷ 广告带来的销售额 |
| TACoS (Total ACoS) | 总体广告销售成本比 | 广告花费 ÷ 全店总销售额（含自然单）|
| ROAS (Return on Ad Spend) | 广告回报率 | 广告带来的销售额 ÷ 广告花费，ACoS的倒数 |
| Breakeven ACoS | 保本ACoS | 广告不亏损的最高ACoS，等于毛利率 |
| Campaign | 广告活动 | 广告的最高层级，设置预算和竞价策略 |
| Ad Group | 广告组 | Campaign下的分组，包含关键词和广告 |
| Keyword | 关键词 | 触发广告展示的搜索词 |
| Match Type | 匹配方式 | 控制关键词触发范围：精准/词组/广泛 |
| Exact Match | 精准匹配 | 只有搜索词与关键词完全一致才触发 |
| Phrase Match | 词组匹配 | 搜索词包含关键词短语即可触发 |
| Broad Match | 广泛匹配 | 搜索词包含关键词的各种变体均可触发 |
| Negative Keyword | 否定词 | 排除不相关搜索词，防止浪费预算 |
| Auto Campaign | 自动投放活动 | 亚马逊自动匹配搜索词，用于发现新词 |
| Manual Campaign | 手动投放活动 | 卖家手动指定关键词 |
| Search Term Report (STR) | 搜索词报告 | 显示实际触发广告的搜索词及其表现 |
| CPC (Cost Per Click) | 每次点击费用 | 每次广告点击的实际花费 |
| Bid | 出价 | 卖家愿意为每次点击支付的最高金额 |
| Impression Share | 展示份额 | 广告实际展示次数 ÷ 有资格展示的总次数 |
| Placement | 广告位置 | 搜索结果顶部/搜索结果其他位置/商品页面 |
| Top of Search (TOS) | 搜索结果顶部 | 转化率最高的黄金广告位 |
| Budget Cap | 预算上限 | 单个广告活动每日最大花费 |
| Portfolio | 广告组合 | 多个Campaign的预算管理容器 |
| Dayparting | 分时投放 | 按时间段调整广告出价 |
| Keyword Harvesting | 关键词收割 | 从搜索词报告中提取高绩效词加入手动活动 |
| CVR (Conversion Rate) | 转化率 | 广告点击后实际购买的比例 |
| ASIN Targeting | ASIN定向 | 直接针对竞争对手商品页面投放广告 |
