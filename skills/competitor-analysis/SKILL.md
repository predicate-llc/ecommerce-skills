---
name: competitor-analysis
description: Helps sellers systematically research and analyze competitors on Amazon, Shopify, TikTok Shop, and other ecommerce platforms. Use when the user wants to identify competing products, deconstruct competitor listings, mine competitor reviews, find keyword gaps, analyze competitor advertising strategies, or build a differentiation opportunity matrix.
---

# Competitor Analysis / 竞品分析

> **Bilingual Support**: Respond in the same language the user writes in.
> 根据用户使用的语言（中文或英文）进行回复。

---

## When to Use / 适用场景

Load this skill when a seller wants to systematically research competitors — whether for launching a new product, defending market position, improving a listing, setting prices, or identifying gaps in the market.

**Trigger keywords / 触发关键词**:
`competitor`, `竞品`, `竞争对手`, `对标分析`, `competitor analysis`, `竞品调研`, `ASIN analysis`, `Best Seller`, `market research`, `竞品定价`, `竞品listing`, `competitor keyword`, `spy on competitors`, `竞品广告`

---

## Context to Gather / 前置信息收集

| # | Information | Why Needed |
|---|---|---|
| 1 | **Your product / ASIN** (or product concept if pre-launch) | The frame of reference for comparison |
| 2 | **Platform** (Amazon / Shopify / TikTok Shop / etc.) | Tools and methods differ by platform |
| 3 | **Marketplace** (US / UK / DE / JP / etc.) | Competitor sets and data availability differ |
| 4 | **Specific goal** — launch research, pricing decision, listing improvement, keyword gap, or market overview | Determines which dimensions of analysis to prioritize |
| 5 | **Known competitor ASINs or URLs** (optional) | Accelerates analysis; if not available, will be identified in Step 1 |
| 6 | **Price point / tier** (budget / mid / premium) | Competitor research should focus on the same price tier |
| 7 | **Key differentiator or USP** (if known) | Helps identify whether differentiation is strong enough |

---

## Framework / 执行框架

The analysis runs across **6 steps**. Steps 1–3 are always required. Steps 4–6 go deeper depending on the goal.

---

### Step 1: Identify the Competitive Set / 确定竞品范围

Never assume you know your competitors. Identify them systematically.

**Method 1: Keyword-based discovery (Amazon)**
1. Search your top 3 keywords on Amazon
2. Record the top 5–8 organic results on page 1
3. Record the top 3 sponsored results (these sellers are paying for visibility — they are serious competitors)
4. Note: the BSR #1 in your subcategory is always a key competitor

**Method 2: Best Sellers list**
1. Navigate: Amazon → Best Sellers → [Your Category] → [Your Subcategory]
2. Record top 10 products
3. Cross-reference with your keyword search results — the overlap is your core competitive set

**Method 3: "Customers also bought" / "Frequently bought together"**
- On your own ASIN or a top competitor's ASIN
- These reflect real buyer cross-shopping behavior

**Method 4: Tools**
- **Jungle Scout**: "Competitor Intelligence" feature; identifies ASINs stealing your keyword rank
- **Helium 10 Cerebro**: Run competitor ASIN through reverse ASIN lookup to see their keywords
- **Keepa**: See historical rank and price for any ASIN

**Competitor tier classification:**

| Tier | Criteria | How Many to Analyze Deeply |
|---|---|---|
| Direct competitors | Same product, same price range, same customer | 3–5 (deep analysis) |
| Adjacent competitors | Same category, slightly different use case or price | 2–3 (moderate analysis) |
| Aspirational benchmarks | Best Seller in category, even if outside your tier | 1–2 (benchmark only) |

**Deliverable: Competitor Shortlist**
Create a table:
```
| Rank | ASIN | Brand | Price | Reviews | Rating | BSR | Notes |
```

---

### Step 2: Listing Deconstruction / Listing 拆解

For each direct competitor, systematically analyze their listing.

#### 2a. Title Analysis
- What keywords are front-loaded in the first 80 characters?
- What differentiating attributes are mentioned (size, material, certification, compatibility)?
- What is the emotional or use-case hook in the title?
- Pattern: Do all top competitors use a similar title structure? If yes, that structure is likely optimized for the algorithm.

#### 2b. Bullet Points / Feature Bullets Analysis
- What are the top 3 benefits they lead with?
- What pain points do they address?
- What social proof signals are included (certifications, warranty, number of users)?
- What are they NOT saying? (Gaps = your opportunity)

**Pain point mining from bullets:**
Look for defensive language like:
- "Unlike flimsy alternatives..."
- "No more [problem]..."
- "Finally, a [product] that..."

These phrases reveal what buyers complain about with existing products — and what you should address.

#### 2c. Image Strategy Analysis

| Image Slot | What to Record |
|---|---|
| Main image | Angle, background style, props used |
| Lifestyle image | Setting, model demographics, aspirational vs. practical |
| Infographic | Which features are called out? What specs are highlighted? |
| Comparison image | Do they compare vs. their own variants or vs. generic competitors? |
| Packaging | Premium or functional presentation? |
| Video | Does one exist? What is it demonstrating? |

**Key question**: What does their image set communicate about their target buyer? A lifestyle image showing a 25-year-old urban professional targets a very different customer than one showing a 50-year-old homeowner.

#### 2d. Pricing Structure
- Current price
- Price history (use Keepa for Amazon) — are they running frequent deals? What is their floor price?
- Coupon / deal frequency
- Variant pricing — what is the price spread across sizes/colors?
- Price per unit (for multi-packs) — are they competing on value or premium positioning?

---

### Step 3: Review Mining / 评价挖掘

Reviews are the most honest source of market intelligence. Buyers say things in reviews that no seller would put in marketing copy.

**Volume and quality metrics:**

| Metric | What It Tells You |
|---|---|
| Total review count | Market maturity; entry barrier |
| Review velocity (new reviews/month) | Current demand level |
| Star rating distribution | Where buyer satisfaction breaks down |
| % of 1-star and 2-star reviews | Product weakness exposure |
| Verified Purchase % | Review credibility |

**Qualitative analysis method:**

For each direct competitor, read:
- All 1-star reviews (min: 20)
- All 5-star reviews (min: 20)
- All reviews mentioning key themes in the last 90 days

**Extract two lists:**

**"What buyers love" (5-star themes):**
- These are the actual benefits driving purchase decisions
- Compare to the competitor's bullet points — are the same things mentioned? If not, their listing is not converting on its real strengths

**"What buyers hate" (1-star / 2-star themes):**
- These are your product development and differentiation opportunities
- Categorize complaints:

| Category | Example | Your Action |
|---|---|---|
| Product quality | "Broke after 2 weeks" | Stronger materials / warranty |
| Sizing/fit | "Runs small, order up" | Accurate size chart, FAQ |
| Listing accuracy | "Nothing like the photos" | Do not over-promise in your listing |
| Packaging | "Arrived damaged" | Better packaging brief |
| Instructions | "No assembly guide" | Include multi-language manual |
| Customer service | "No response to my message" | Differentiation through support quality |

**Review gap opportunity scoring:**
For each complaint theme in competitor reviews, score:
- Frequency: How often is this mentioned? (High / Medium / Low)
- Severity: How much does it impact purchase satisfaction? (Critical / Moderate / Minor)
- Addressability: Can you solve this in your product or listing? (Yes / Partial / No)

Any theme with High frequency + Moderate/Critical severity + Yes addressability = **top differentiation opportunity**.

---

### Step 4: Keyword Gap Analysis / 关键词差距分析

Identify keywords that competitors rank for that you do not — and vice versa.

**Tool-based approach:**

Using **Helium 10 Cerebro**:
1. Enter top 3 competitor ASINs
2. Export their keyword rankings
3. Filter for: Search Volume >500 AND your product does not rank in top 30
4. These are your keyword gaps → add to your listing and PPC campaigns

Using **Jungle Scout Keyword Scout**:
1. Enter a competitor ASIN
2. Review "Organic Rank" column
3. Sort by search volume descending
4. Any keyword where competitor ranks top 5 and you don't rank top 20 = priority gap

**Manual approach (no tools):**
1. Search each keyword you want to rank for
2. Note which page and position each competitor appears
3. Compare to your own ranking
4. If a competitor consistently ranks 1–3 positions and you rank 10–30, they have keyword authority you need to close

**Keyword overlap analysis:**

```
Your keywords ∩ Competitor's keywords = Battleground keywords (compete directly)
Competitor's keywords − Your keywords = Gap keywords (opportunities)
Your keywords − Competitor's keywords = Unique keywords (potential moat)
```

---

### Step 5: Advertising Intelligence / 广告策略推测

You cannot see a competitor's exact bids, but you can infer their strategy.

**What you can observe directly:**
- Which keywords show their sponsored ads (run searches manually or use tools)
- Which placements they target (product detail pages, search top)
- Whether they advertise on their own brand name
- Whether they run Sponsored Brands campaigns (requires Brand Registry)
- Video ads presence in search results

**Inference framework:**

| Observation | Inference |
|---|---|
| Ads appear on top keywords but not long-tail | Focused on efficiency; well-optimized campaigns |
| Ads appear on many irrelevant keywords | Running auto campaigns without aggressive negatives; budget is inefficient |
| Appearing on your own ASIN's product page | Actively targeting your customers; consider defensive SP campaign |
| Sponsored Brand ad with headline copy | Brand Registry active; mature brand building strategy |
| Flash deal + high PPC spending simultaneously | Launch phase or BSR boost attempt |

**Using Helium 10 Adtomic / Jungle Scout Advertising Analytics:**
- Some tools provide estimated PPC spend per ASIN
- Use as relative benchmarks (not absolute truths)

---

### Step 6: Differentiation Opportunity Matrix / 差异化机会识别

Synthesize all findings into a structured opportunity map.

**Dimensions to map:**

| Dimension | Your Current Position | Best Competitor | Gap / Opportunity |
|---|---|---|---|
| Price | | | |
| Review count | | | |
| Star rating | | | |
| Image quality | | | |
| Keyword coverage | | | |
| Key feature X | | | |
| Key feature Y | | | |
| Niche use case served | | | |

**Opportunity scoring criteria:**

For each identified gap or opportunity:
1. **Impact on buyer decision**: Would closing this gap meaningfully influence a purchase?
2. **Feasibility**: Can you address this in 30–90 days without redesigning the product?
3. **Defensibility**: If you close this gap, how hard is it for competitors to copy?

**High-value differentiation moves (examples by type):**

| Type | Example |
|---|---|
| Product feature gap | Competitor has no waterproof variant; add IP67 rating |
| Listing accuracy | Competitors over-promise; you show accurate in-use size images |
| Bundle opportunity | Competitor sells single unit; offer a 2-pack or kit with accessories |
| Underserved niche | Top competitors target US buyers; optimize for UK English and UK-specific use cases |
| Review theme | 40% of competitor 1-star reviews mention poor instructions; include video QR code in packaging |
| Keyword gap | Competitors rank for 200 keywords; you can target 50 uncontested long-tail terms |

---

## Platform Variants / 平台差异

### Amazon
- Primary tools: Helium 10, Jungle Scout, Keepa, Seller Sprite (for Asian markets)
- Search Term Report (your own) reveals which competitor keywords you are already appearing for
- Brand Analytics (available to Brand Registered sellers) shows top search terms, market share, and click share
- Amazon Attribution allows tracking of off-Amazon traffic sources

### Shopify / DTC
- Tools: SimilarWeb (traffic estimation), SEMrush / Ahrefs (keyword and content gap), SpyFu (ad copy)
- Competitor analysis focuses on: site structure, app stack (detected via BuiltWith), email capture strategy, ad creative (via Facebook Ad Library)
- Facebook Ad Library is free and shows all active ads from any page — invaluable for creative benchmarking

### TikTok Shop
- TikTok Creative Center shows top-performing ad creatives by category
- Creator Marketplace data shows which creators competitors are working with
- Hashtag search reveals competitor content strategy
- Product review content on TikTok videos is public intelligence

### Shopee / Lazada (Southeast Asia)
- Platform's "Top Sales" and "Mall" designation indicate market leaders
- Price sensitivity is higher; competitor pricing analysis is especially critical
- Review translation (from local language) often requires tool support

### eBay
- eBay's "Completed Listings" and "Sold Listings" filter shows actual sale prices (not just asking price)
- Terapeak (free for eBay sellers) provides 365 days of sales data by keyword and category
- Critical for understanding true market prices in secondhand/collectibles categories

---

## Output Format / 输出格式

```
# Competitor Analysis Report
Product: [Your Product / ASIN]
Platform: [Platform + Marketplace]
Analysis Date: [Date]
Goal: [Launch / Pricing / Listing Improvement / Market Overview]

## Competitive Landscape Summary
[2–3 sentence overview of market dynamics, barriers to entry, dominant players]

## Competitor Shortlist
| Rank | ASIN/URL | Brand | Price | Reviews | Rating | BSR | Tier |
|------|----------|-------|-------|---------|--------|-----|------|
| 1    |          |       |       |         |        |     |      |

## Key Findings by Dimension

### Listing Patterns
[What title structures, bullet themes, and image types dominate the top 5 results]

### Review Intelligence
Top "loves" (5-star themes):
1. [Theme] — mentioned in X% of 5-star reviews
Top "complaints" (1–2 star themes):
1. [Theme] — mentioned in X% of negative reviews

### Keyword Gaps
[Top 10 keywords competitors rank for that you don't — with search volume]

### Pricing Dynamics
[Price range, deal frequency, value vs. premium positioning]

### Advertising Patterns
[Observed ad strategy across competitors]

## Differentiation Opportunity Matrix
| Opportunity | Impact | Feasibility | Defensibility | Priority |
|-------------|--------|-------------|---------------|----------|
| [X]         | High   | Medium      | High          | P0       |

## Recommended Actions
### Immediate (0–2 weeks)
1. [Action]

### Short-term (2–8 weeks)
2. [Action]

### Strategic (2–6 months)
3. [Action]
```

---

## Common Pitfalls / 常见误区

1. **Analyzing only the BSR #1 and ignoring #2–#5**
   The top seller is often entrenched and hard to beat directly. Competitors ranked #2–#5 are often more vulnerable and reveal what's working at a scale you can realistically target.

2. **Mistaking correlation for causation in review analysis**
   A competitor has 4.8 stars and sells well. That does not mean their 4.8 stars caused their sales. It may be their price point, keyword rank, or ad spend. Distinguish what is driving success.

3. **Treating all negative reviews as product flaws**
   Many 1-star reviews are about shipping, customer service, or buyer error — not the product. Sort complaints by category before deciding what to "fix" in your own product.

4. **Benchmarking against categories, not subcategories**
   The relevant competitive set is your subcategory, not the entire parent category. "Sports & Outdoors" has very different dynamics than "Yoga Mats" — always narrow to the correct node.

5. **Ignoring review velocity**
   A competitor with 5,000 reviews but only gaining 10/month is stagnant. A competitor with 200 reviews gaining 80/month is on a growth trajectory. Velocity matters more than absolute count.

6. **Copying competitor keywords blindly without intent analysis**
   A keyword a competitor ranks for may have informational intent (users researching, not buying). Verify buyer intent before adding keywords to your PPC or listing.

7. **Failing to monitor competitors after launch**
   Competitive landscape changes. A competitor who is a non-factor today may launch a new improved product next month. Set a calendar reminder to re-run this analysis every 60–90 days.

8. **Over-analyzing and under-acting**
   Competitor analysis is an input, not an output. The goal is to make decisions. After the analysis, commit to 3 concrete changes. Do not keep gathering data indefinitely.

---

## Related Skills / 相关技能

- [`product-listing-audit`](../product-listing-audit/SKILL.md) — Use competitor listing intelligence to benchmark your own listing and identify gaps to close
- [`keyword-research`](../keyword-research/SKILL.md) — Competitor keyword data feeds directly into your keyword strategy
- [`amazon-ppc-audit`](../amazon-ppc-audit/SKILL.md) — Competitor advertising patterns inform your own campaign structure and defensive strategy
- [`pricing-strategy`](../pricing-strategy/SKILL.md) — Competitor price analysis is the essential input to your pricing model
- [`market-entry-research`](../market-entry-research/SKILL.md) — Use competitor analysis as the competitive dimension of a broader market entry assessment
- [`sales-data-analysis`](../sales-data-analysis/SKILL.md) — After launching or optimizing, compare your own metrics to competitor benchmarks

---

## Terminology / 术语对照

| English | 中文 | 说明 |
|---|---|---|
| Competitor Analysis | 竞品分析 | 系统研究竞争对手策略的方法论 |
| ASIN (Amazon Standard Identification Number) | 亚马逊商品标识号 | 亚马逊平台每个商品的唯一编号 |
| BSR (Best Seller Rank) | 畅销排名 | 亚马逊类目内的销量排名，数字越小越好 |
| Direct Competitor | 直接竞争对手 | 相同产品、相同价格区间、相同目标客户 |
| Competitive Set | 竞品集合 | 分析时选定的一组竞品 |
| Review Mining | 评价挖掘 | 系统分析评价内容以获取市场情报 |
| Review Velocity | 评价增速 | 单位时间内新增评价数量 |
| Keyword Gap | 关键词差距 | 竞品覆盖但自己未覆盖的关键词 |
| Reverse ASIN Lookup | ASIN反查 | 通过竞品ASIN查询其排名关键词的工具功能 |
| Price History | 价格历史 | 商品历史售价走势，用于判断定价策略 |
| Differentiation | 差异化 | 与竞品的核心区别点 |
| Unique Selling Proposition (USP) | 独特卖点 | 产品区别于竞品的核心价值主张 |
| Market Share | 市场份额 | 占类目总销售额的比例 |
| Click Share | 点击份额 | 某品牌/商品占类目总点击量的比例 |
| Pain Point | 痛点 | 买家未被满足的需求或不满 |
| Brand Analytics | 品牌分析 | Amazon品牌注册卖家专属数据工具 |
| Keepa | Keepa | 亚马逊商品价格和排名历史追踪工具 |
| Helium 10 | Helium 10 | 主流亚马逊卖家研究工具套件 |
| Jungle Scout | Jungle Scout | 主流亚马逊选品和竞品研究工具 |
| Facebook Ad Library | Facebook广告库 | Meta官方免费工具，可查看任何品牌的在投广告 |
| Terapeak | Terapeak | eBay官方提供的市场数据分析工具 |
| Completed Listings | 已结束的商品 | eBay中已完成销售的历史记录，反映真实成交价 |
| Positioning | 定位 | 产品在市场上相对竞品的差异化位置 |
