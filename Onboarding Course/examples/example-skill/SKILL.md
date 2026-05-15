---
name: page-check
description: "Quick health check on an ecommerce product page. Visits the URL and checks for essential elements every product page needs: title, description, images, pricing, call-to-action, and meta description. Produces a simple pass/fail checklist. Use when someone says 'check this page', 'page check', 'is my product page OK', or shares a product URL and wants a quick review. NOT for a full mobile audit (use moby for that)."
user-invocable: true
argument-hint: "product_page_url"
---

# Page Check

A quick health check for ecommerce product pages. Visit the URL and verify the essentials are present.

## What You're Checking

Every product page needs these elements to convert. Check each one and report pass or fail.

### Essential Elements

| # | Element | What to look for | Pass criteria |
|---|---|---|---|
| 1 | **Product title** | An H1 or prominent heading with the product name | Present and descriptive (not just "Product") |
| 2 | **Product description** | Body text describing the product | At least 50 words |
| 3 | **Product images** | Photos or renders of the product | At least 3 images |
| 4 | **Price** | Visible pricing | Clearly displayed, not hidden behind a click |
| 5 | **Add to cart button** | A prominent call-to-action | Visible without scrolling on desktop |
| 6 | **Meta description** | The SEO snippet shown in search results | Present and under 160 characters |

## How to Run the Check

1. Visit the URL provided by the user
2. Check each element in the table above
3. For each element, record pass or fail with a brief note

## Output Format

Produce a clean checklist:

```
## Page Check: [Product Name]
**URL:** [url]
**Checked:** [today's date]

| # | Element | Result | Note |
|---|---|---|---|
| 1 | Product title | ✅ Pass | "Omega 3 DHA — Plant-Based" |
| 2 | Description | ✅ Pass | 147 words |
| 3 | Images | ❌ Fail | Only 2 images found |
| 4 | Price | ✅ Pass | £24.99 clearly displayed |
| 5 | Add to cart | ✅ Pass | Visible above the fold |
| 6 | Meta description | ❌ Fail | 203 characters — over the 160 limit |

**Score: 4/6**

### Issues to Fix
- **Images:** Add at least 1 more product image. Consider showing the product from different angles or in use.
- **Meta description:** Trim to under 160 characters. Current description can be shortened by removing the repeated brand name.
```

## Important

- Be honest about what you find. Don't pass things that are borderline.
- For every fail, include a specific, actionable suggestion — not just "fix this."
- If the page doesn't load or the URL is wrong, say so immediately rather than guessing.
