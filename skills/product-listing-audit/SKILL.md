# Product Listing Audit / 商品 Listing 诊断

> **Bilingual Support**: Respond in the same language the user writes in.
> 根据用户使用的语言（中文或英文）进行回复。

---

## When to Use / 适用场景

Load this skill when a seller wants to evaluate the quality of an existing product listing and identify concrete improvement opportunities.

**Trigger keywords / 触发关键词**:
`listing`, `product page`, `商品详情`, `标题优化`, `listing audit`, `listing quality`, `listing score`, `optimize listing`, `listing review`, `商品页面`, `listing诊断`, `优化listing`

---

## Context to Gather / 前置信息收集

Before running the audit, collect the following. Ask only for what is missing.

| # | Information | Why Needed |
|---|---|---|
| 1 | **Platform** (Amazon / Shopify / TikTok Shop / eBay / Walmart / other) | Rules and scoring weights differ by platform |
| 2 | **Marketplace / Region** (e.g., Amazon US, Amazon DE, Shopify US) | Character limits, language, and compliance requirements vary |
| 3 | **Product category** (e.g., Bluetooth Headphones, Kitchen Knives) | Category-specific image rules, keyword patterns, and buyer intent differ |
| 4 | **Current listing URL or ASIN** (optional but preferred) | Enables direct analysis |
| 5 | **Listing content** — title, bullet points, description, backend keywords (if no URL) | Raw material for audit |
| 6 | **Main target keywords** (2–5 terms seller wants to rank for) | Used to assess keyword coverage |
| 7 | **Competitor ASINs or URLs** (1–3, optional) | Benchmarking context |
| 8 | **Current performance data** (optional: CTR, CVR, sessions, unit session %) | Validates whether problems are theoretical or already hurting metrics |

---

## Framework / 执行框架

Run the audit across **5 dimensions**. Score each dimension, then compute a weighted total (0–100).

### Dimension 1: Title Quality / 标题质量 (25 points)

**Scoring rubric:**

| Score | Criteria |
|---|---|
| 22–25 | Contains primary keyword in first 80 chars; brand name present; core product type named; 2+ key attributes (size/color/material/count); no ALL CAPS; no special characters; within platform character limit |
| 15–21 | Meets most criteria; primary keyword present but not front-loaded; minor formatting issues |
| 8–14 | Primary keyword missing or buried; title reads like a list of specs with no natural flow |
| 0–7 | Keyword stuffed with no readability; exceeds character limit; missing product type entirely |

**Platform character limits:**
- Amazon (most categories): 200 bytes (≈ 150–200 characters depending on encoding)
- Amazon (some categories like Apparel): 80 characters
- Shopify product name: no hard limit, but 60–70 chars recommended for SEO meta title
- TikTok Shop: 34 characters (displayed title); up to 255 characters (full title field)
- eBay: 80 characters
- Walmart: 200 characters

**Checklist:**
- [ ] Primary keyword appears within first 80 characters
- [ ] Brand name included (Amazon: usually first; other platforms: flexible)
- [ ] Product type clearly stated (e.g., "Wireless Earbuds", "Stainless Steel Knife")
- [ ] Key differentiator mentioned (e.g., "Noise Cancelling", "BPA-Free", "Pack of 6")
- [ ] Within platform character limit
- [ ] No prohibited characters: `! " ' $ ? @ , ¡ ¿` (Amazon)
- [ ] Not duplicating the same keyword more than twice
- [ ] Readable as a sentence fragment, not just a keyword dump

---

### Dimension 2: Bullet Points / Feature Bullets 五点描述 (20 points)

**Scoring rubric:**

| Score | Criteria |
|---|---|
| 17–20 | 5 bullets present; each leads with a bolded benefit (not feature); addresses key buyer concerns; incorporates secondary keywords naturally; each bullet 150–200 chars; no redundancy between bullets |
| 11–16 | 4–5 bullets; benefit-led but inconsistent; keywords present but forced; some redundancy |
| 5–10 | Fewer than 4 bullets; feature-only (no buyer benefit translation); bullets very short (<80 chars) or very long (>300 chars) |
| 0–4 | Missing bullets; purely promotional language ("Best product ever!"); keyword stuffed |

**Bullet structure formula:**
```
[ALL-CAPS HOOK] — [Core benefit statement] — [Supporting feature/spec] — [Use case or social proof hint]
```

Example:
```
NOISE-FREE CALLS EVERYWHERE — Advanced CVC 8.0 microphone technology filters 
background noise so your voice stays crystal clear on calls, even in busy offices 
or crowded cafes.
```

**Checklist:**
- [ ] All 5 bullet slots used
- [ ] Each bullet opens with the most important benefit, not the feature
- [ ] No bullet repeats information from the title or another bullet
- [ ] At least 3 secondary keywords distributed naturally across bullets
- [ ] Each bullet is 150–250 characters (sweet spot)
- [ ] No marketing superlatives without evidence ("world's best", "revolutionary")
- [ ] Pain point or use case addressed in at least 2 bullets

---

### Dimension 3: Image Quality / 图片质量 (25 points)

**Scoring rubric:**

| Score | Criteria |
|---|---|
| 22–25 | Main image: white background, product fills ≥85% of frame, high resolution (≥1500px on longest side, preferably 2000px+); 6–9 total images; lifestyle image included; infographic with key specs included; no watermarks on any image |
| 15–21 | Main image compliant; 4–6 total images; some lifestyle or infographic but not both; minor quality issues |
| 8–14 | Main image has issues (shadows, product <85% frame, low res); or fewer than 4 images; missing lifestyle |
| 0–7 | Main image non-compliant (colored background, watermark, accessories shown as main); only 1–2 images |

**Required image set (by slot):**
1. **Hero / Main image** — pure white background, product only, ≥85% frame fill
2. **Lifestyle image** — product in use, real environment, matches target buyer's world
3. **Feature callout infographic** — annotated with 3–5 key features/specs
4. **Size/dimension chart** — especially important for apparel, furniture, accessories
5. **Comparison image** — vs. competitor or vs. product variants (if applicable)
6. **Packaging image** — what arrives in the box
7. **Close-up detail shot** — texture, material, quality cue
8. **Social proof image** — review snippets, certifications, awards (if available)
9. **(Video — counts as a slot)** — product demo, 30–90 seconds

**Checklist:**
- [ ] Main image: white (#FFFFFF) background, no props unless they are sold with the product
- [ ] Main image resolution ≥ 1500px on longest side (2000px+ for zoom to activate on Amazon)
- [ ] At least one lifestyle image showing product in context
- [ ] At least one infographic/callout image
- [ ] Dimension or size reference image present (if size matters for the category)
- [ ] No text overlay on main image (Amazon policy)
- [ ] No competitor brand logos visible in any image
- [ ] Images are not blurry, washed out, or poorly lit

---

### Dimension 4: Keyword Coverage / 关键词覆盖 (15 points)

**Scoring rubric:**

| Score | Criteria |
|---|---|
| 13–15 | Primary keyword in title + ≥2 bullets + description; top 5 secondary keywords distributed across content; no obvious keyword gaps vs. competitor listings; backend search terms filled (Amazon) |
| 8–12 | Primary keyword present; some secondary keywords but gaps exist; backend terms partially filled or empty |
| 3–7 | Primary keyword missing from title or only appears once; secondary keywords not utilized; no backend terms |
| 0–2 | Listing has no discernible keyword strategy; generic or placeholder content |

**Keyword placement hierarchy (Amazon):**
1. Title (highest weight in A9)
2. Bullet points (high weight)
3. Backend Search Terms field (high weight, not visible to buyer)
4. Description / A+ Content (lower weight but contributes)
5. Subject Matter / Other backend fields (low weight)

**Backend Search Terms rules (Amazon):**
- Max 250 bytes (not characters — emoji/special chars count as multiple bytes)
- No repetition of words already in title or bullets (wastes space)
- No competitor brand names (policy violation)
- No ASINs
- Separate with spaces (not commas)
- Include common misspellings, synonyms, Spanish terms (for US marketplace)

**Checklist:**
- [ ] Primary keyword in title (first 80 chars)
- [ ] Primary keyword in ≥1 bullet
- [ ] Top 3 secondary keywords each appear at least once in bullets or description
- [ ] Amazon: Backend Search Terms field is filled (≥200 bytes used)
- [ ] No keyword stuffing (same phrase repeated 3+ times)
- [ ] Long-tail variants covered (e.g., "wireless earbuds for small ears" not just "wireless earbuds")

---

### Dimension 5: Reviews & Ratings Status / 评分与评价状态 (15 points)

**Scoring rubric:**

| Score | Criteria |
|---|---|
| 13–15 | ≥4.2 stars; ≥50 reviews (or ≥15 if new product <6 months); seller actively responds to negative reviews; review content is relevant and credible |
| 8–12 | 3.8–4.1 stars; 20–49 reviews; no responses to negative reviews |
| 3–7 | 3.5–3.7 stars; <20 reviews; presence of unaddressed 1-star reviews about recurring issues |
| 0–2 | <3.5 stars; <10 reviews; obvious fake review patterns; recent policy warnings |

**Critical thresholds:**
- **4.0 stars** — minimum viability threshold; below this, conversion drops sharply
- **4.3+ stars** — competitive threshold in most categories
- **15 reviews** — minimum social proof floor for new listings
- **50 reviews** — trust credibility threshold; significantly improves conversion

**Review health checklist:**
- [ ] Star rating ≥ 4.0
- [ ] Review count adequate for category maturity
- [ ] No clusters of 1-star reviews in last 30 days (indicates product or fulfillment issue)
- [ ] Seller has responded to at least 50% of 1-star and 2-star reviews
- [ ] Review content mentions product benefits (not just generic "great product")
- [ ] No obvious fake review patterns (multiple reviews on same day, same reviewer)

---

### Scoring Summary / 综合评分

| Dimension | Weight | Your Score | Weighted Score |
|---|---|---|---|
| Title Quality | 25 | /25 | |
| Bullet Points | 20 | /20 | |
| Image Quality | 25 | /25 | |
| Keyword Coverage | 15 | /15 | |
| Reviews & Ratings | 15 | /15 | |
| **TOTAL** | **100** | | **/100** |

**Score interpretation:**
- **85–100**: High-performing listing. Focus on A/B testing and iterative improvements.
- **70–84**: Good foundation. 2–3 targeted improvements will move the needle.
- **50–69**: Significant gaps. Prioritize images + title + keywords immediately.
- **Below 50**: Requires full listing rebuild. Current listing is likely suppressing organic rank.

---

## Platform Variants / 平台差异

### Amazon
- A9 algorithm weights title > bullets > backend search terms > description
- **Category-specific rules**: Electronics require safety warnings; Grocery requires ingredient disclosure; Clothing requires fabric composition
- **Listing suppression triggers**: missing main image, out-of-range price, ASIN variation errors
- **A+ Content**: available to Brand Registered sellers; replaces plain description; does NOT directly boost SEO but improves CVR by 3–10%
- **Character byte counting**: Amazon counts bytes, not characters; accented characters (é, ü) count as 2 bytes

### Shopify / DTC Stores
- SEO meta title and meta description are separate from product name and description — audit both
- **Meta title**: 50–60 characters recommended; include primary keyword + brand
- **Meta description**: 120–155 characters; include keyword + CTA + differentiator
- Product description supports HTML and can be long-form; use H2/H3 structure for readability
- Page speed directly impacts conversion; flag image files >200KB

### TikTok Shop
- Title displayed in the app is truncated at ~34 characters — front-load the most important information
- Product images should be square (1:1 ratio); first image is the "card cover" and appears in video shopping links
- Video content and product listing are tightly linked — audit should include whether product video exists
- TikTok Shop's "Product Showcase" tab on creator profiles requires strong thumbnail imagery

### eBay
- 80-character title limit — keyword density is critical
- Item Specifics (structured attributes) are heavily weighted in eBay's Cassini search algorithm
- Condition description is mandatory and legally binding — be precise
- Multiple images allowed (up to 24 free); use all available slots

### Walmart Marketplace
- Title: 200 characters; follow the format: [Brand] + [Product Type] + [Key Attributes]
- Walmart's search algorithm (Polaris) heavily weights item description for indexing
- Rich Media (360° spin, videos) available on Walmart — flag if not utilized
- Walmart requires specific attribute fields (shelf, sub-category) — incomplete attributes suppress listing

---

## Output Format / 输出格式

Deliver the audit as a structured report with the following sections:

---

### Listing Audit Report Template

```
# Listing Audit Report
Product: [Product Name]
Platform: [Platform + Marketplace]
Audit Date: [Date]
ASIN/SKU: [if applicable]

## Overall Score: XX/100 — [Grade: A/B/C/D/F]

## Score Breakdown
| Dimension         | Score  | Max |
|-------------------|--------|-----|
| Title Quality     | XX     | 25  |
| Bullet Points     | XX     | 20  |
| Image Quality     | XX     | 25  |
| Keyword Coverage  | XX     | 15  |
| Reviews & Ratings | XX     | 15  |
| TOTAL             | XX     | 100 |

## Priority Fixes (Impact-ranked)

### 🔴 Critical (Fix within 24 hours)
1. [Issue] — [Specific action] — [Expected impact]

### 🟡 Important (Fix within 7 days)
2. [Issue] — [Specific action] — [Expected impact]

### 🟢 Optimization (Fix within 30 days)
3. [Issue] — [Specific action] — [Expected impact]

## Dimension Analysis

### Title
Current: "[current title]"
Issues: [list issues]
Suggested: "[revised title]"

### Bullet Points
[Bullet-by-bullet analysis with rewrite suggestions]

### Images
[Image slot analysis — what exists, what's missing, what to change]

### Keywords
[Keyword gap analysis — missing terms, placement recommendations, backend terms suggestions]

### Reviews
[Current rating, review count, identified issues, recommended response templates]

## Next Steps
[Ordered action list with owner and timeline]
```

---

## Common Pitfalls / 常见误区

1. **Fixing title only, ignoring backend keywords**
   Backend Search Terms on Amazon capture long-tail traffic that can't fit in visible content. An optimized title with empty backend terms leaves significant rank potential untapped.

2. **Confusing features with benefits in bullets**
   "Our earbuds use 40mm drivers" is a feature. "Deep bass and crystal-clear highs that make every song sound like a live performance" is a benefit. Buyers buy benefits; features are just evidence.

3. **Using the same keyword too many times thinking it boosts rank**
   Amazon's A9 counts a keyword once regardless of repetition. Repeating "wireless earbuds" 7 times in bullets wastes character budget and harms readability.

4. **Uploading lifestyle images as the main image**
   Amazon strictly requires a pure white background for the main image. A non-compliant main image leads to listing suppression. Check this first in every audit.

5. **Treating all platforms as identical**
   A Shopify SEO audit requires checking meta fields (invisible to the buyer but critical for Google). A TikTok Shop audit requires checking the card thumbnail and video quality. Never apply Amazon logic blindly to other platforms.

6. **Ignoring image file size (Shopify/DTC)**
   A 5MB product image that loads in 3+ seconds kills mobile conversion. Always flag images >300KB on Shopify and recommend compression via TinyPNG or Shopify's built-in optimizer.

7. **Over-indexing on star rating, ignoring review content**
   A 4.2-star product where most 1-star reviews mention "broke after 2 weeks" is a product problem, not a listing problem. Distinguish between listing issues and product/fulfillment issues.

8. **Not considering mobile rendering**
   Over 70% of Amazon browsing is on mobile. Long bullet points get truncated. The first 1000 characters of the description may not be visible without tapping "Read more." Always audit mobile view.

---

## Related Skills / 相关技能

- [`keyword-research`](../keyword-research/SKILL.md) — Run before or after this audit to identify keyword gaps and generate an optimized keyword set
- [`amazon-ppc-audit`](../amazon-ppc-audit/SKILL.md) — Once the listing is optimized, audit the ad structure to ensure traffic is being captured efficiently
- [`competitor-analysis`](../competitor-analysis/SKILL.md) — Use to benchmark the audited listing against top competitors and identify differentiation opportunities
- [`a-plus-content`](../a-plus-content/SKILL.md) — After fixing the core listing, upgrade the description with A+ Content to boost conversion rate
- [`product-photography-brief`](../product-photography-brief/SKILL.md) — If the image audit reveals gaps, use this skill to generate a photography brief for reshoots

---

## Terminology / 术语对照

| English | 中文 | 说明 |
|---|---|---|
| Listing | 商品详情页 / Listing | 平台上的商品展示页面 |
| Title | 标题 | 商品名称，搜索权重最高 |
| Bullet Points / Feature Bullets | 五点描述 / 卖点 | Amazon 商品页面的五个要点 |
| Backend Search Terms | 后台搜索词 | Amazon 卖家后台填写、买家不可见的关键词字段 |
| A9 Algorithm | A9 算法 | Amazon 的搜索排名算法 |
| Conversion Rate (CVR) | 转化率 | 访客中实际下单的比例 |
| Click-Through Rate (CTR) | 点击率 | 曝光后点击进入详情页的比例 |
| Sessions | 访客数 | 一定时间内访问商品页的独立用户数 |
| Unit Session Percentage | 单次访问转化率 | Amazon 的转化率指标（订单数/访客数）|
| A+ Content / EBC | A+ 内容 / 增强品牌内容 | Amazon 品牌注册卖家可用的富媒体描述模块 |
| Listing Suppression | Listing 被压制/下架 | 因违规或缺失信息导致商品无法展示 |
| Main Image | 主图 | 搜索结果页显示的第一张图片 |
| Infographic | 信息图 / 卖点图 | 带有文字标注的产品功能说明图 |
| Hero Image | 主视觉图 | 最能代表产品的核心展示图 |
| Keyword Coverage | 关键词覆盖度 | 目标关键词在 Listing 各字段中的分布情况 |
| Long-tail Keyword | 长尾词 | 搜索量较小但购买意图明确的多词组合 |
| ACoS | 广告销售成本比 | 广告花费 ÷ 广告销售额，越低越好 |
| Star Rating | 星级评分 | 买家综合评分，满分5星 |
| Review Velocity | 评价增速 | 单位时间内新增评价数量 |
| Byte | 字节 | Amazon 字符限制的计量单位（英文字符=1字节，部分特殊字符=2字节）|
