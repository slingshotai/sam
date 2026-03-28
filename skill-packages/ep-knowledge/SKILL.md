---
name: ep-knowledge
description: "Search the eCommerce Podcast episode archive for examples, case studies, expert insights, and real-world evidence. Contains 283+ tagged episodes mapped to the Slingshot Framework areas (Sell, Story, Tech Stack, Marketing, Optimise, Experience, Growth) and FUEL marketing stages. Use when someone asks 'has anyone on the podcast talked about X', 'find me an EP episode about', 'what episodes cover Y', 'who talked about Z', 'evidence for', 'case study', 'example of', or wants real-world examples to support a point. Also use when SAM needs to reference specific episodes while teaching. NOT for creating episode content (use content-engine). NOT for packaging episodes (use episode-packaging). NOT for analysing videos (use igap). This is a knowledge retrieval skill — it finds and surfaces relevant episodes."
user-invocable: true
argument-hint: "topic_or_question"
---

# EP Knowledge Base

Search the eCommerce Podcast episode archive to find relevant episodes, case studies, expert insights, and real-world evidence.

## How It Works

1. Read the episode index at `5.Resources/05.AI/SlingshotAI/EP Tagging/episode-index.yaml`
2. Match the member's question against episode tags, titles, guests, key takeaways, and related skills
3. Return the most relevant episodes with context on why they're relevant

## Search Strategy

When a member asks a question, search across multiple dimensions:

### By Slingshot Area
If the question maps to a framework area, filter by `slingshot_areas`:
- "How do I improve my product pages?" → Optimise
- "How should my brand sound?" → Story
- "How do I get more repeat customers?" → Growth

### By FUEL Stage
If the question implies a maturity level, filter by `fuel_stages`:
- "I'm just getting started with email" → Foundation
- "I want to test new channels" → Unlock
- "How do I optimise what's already working?" → Elevate
- "What cutting-edge approaches should I try?" → Leapfrog

### By Topic
Search `menu_tags` and `key_takeaway` for specific topics:
- "referral programme" → match against menu_tags and takeaways
- "subscription churn" → match against menu_tags and takeaways

### By Guest
Search `guest` field when someone asks about a specific person or company.

### By Related Skill
When SAM is teaching about a skill, filter by `related_skills` to find supporting episodes:
- Teaching Moby methodology → find episodes tagged with `moby`
- Teaching Brand Voice → find episodes tagged with `brand-voice`

## Response Format

### For direct questions ("find me episodes about X")

Return 3-5 most relevant episodes:

```
## Episodes about [topic]

**EP [number]: [title]** — [guest] ([company])
[key_takeaway]
Slingshot: [areas] | FUEL: [stages]
→ Listen: [URL from episode file if available]

**EP [number]: [title]** — [guest] ([company])
[key_takeaway]
Slingshot: [areas] | FUEL: [stages]
→ Listen: [URL from episode file if available]

[etc.]
```

### For SAM teaching context ("what evidence supports X")

Return 1-2 most relevant episodes woven into the teaching:

"Jay Myers covered this on EP 283 — he found that a 0.4 increase in referral rate produced 56x more subscribers over 30 months. That's the Growth area of Slingshot in action."

### For broad exploration ("what episodes do you have about marketing")

Group by FUEL stage:

```
## Marketing Episodes

### Foundation (getting the basics right)
- EP [n]: [title] — [takeaway]
- EP [n]: [title] — [takeaway]

### Unlock (diversifying channels)
- EP [n]: [title] — [takeaway]

### Elevate (optimising what works)
- EP [n]: [title] — [takeaway]
```

## Reading Full Episode Content

The index contains tags and takeaways, but the full blog content lives in the episode files at `5.Resources/01.Work/EP/EP Episode Vault/`. When the member wants more detail:

1. Find the relevant episode in the index
2. Read the full file from the episode vault
3. Extract the specific section that answers their question
4. Present it in context

## Connecting to Slingshot Framework

When returning results, always connect episodes to the Slingshot Framework:
- "This episode maps to the **Optimise** area of Slingshot — specifically the 'Easy to find' pillar"
- "Jay covers **Growth** at the **Foundation** stage — getting the referral basics in place before trying to scale"

This helps members see how individual episodes fit into the bigger picture.

## Updating the Index

When new episodes are published and processed by the content engine:
1. Read the new episode file
2. Tag it per the tagging playbook at `5.Resources/05.AI/SlingshotAI/EP Tagging/tagging-playbook.md`
3. Append the entry to `episode-index.yaml`
