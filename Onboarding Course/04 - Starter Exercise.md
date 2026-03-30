# Module 4: Research, Build a Playbook, Create Your First Skill

Video Link: https://www.youtube.com/watch?v=4RjChTKM9fg

## What We're Doing

This is where everything comes together. You're going to:

1. Research a topic using Claude
2. Turn it into a playbook
3. Refine it with follow-up questions
4. Use the Anthropic skill-creator to turn it into a working skill
5. Run that skill on your own site

By the end of this module, you'll have built and run your own skill. Not one you bought — one you created.

## Why Playbooks Matter

In Module 3, you saw that skills have a `references/` folder with playbooks inside. Those playbooks are the backbone of every skill — they contain the methodology, the scoring criteria, the decision frameworks that make a skill consistently good. Without the playbook, a skill is just generic instructions. With it, it's expertise.

Here's why that matters right now:

1. **Playbooks make Claude smarter about your business.** When a playbook sits in your vault, Claude can reference it in future conversations.
2. **Playbooks are the first step to building your own skills.** Research → playbook → skill. That's the pattern.
3. **Playbooks compound.** A year from now, your Playbooks folder could contain twenty reference documents. That's your own methodology library that Claude can draw from at any time.

The pattern is: **research → playbook → refine → build a skill from it.**

And that's exactly what we're about to do.

## Part 1: Research

We're all going to research the same topic so the video matches what you see. The topic: **essential SEO components for an ecommerce product page**.

This builds on the Page Check example skill from Module 3 — but instead of a simple checklist, we're going to create a proper SEO-informed version backed by real research.

### Step 1: Ask Claude to Research

```
Research the critical SEO components for an ecommerce product page,
specifically for businesses in my niche. Cover everything from the
H1 tag to schema markup. Create a practical playbook I can reference
later. Save it to my SlingshotAI/Playbooks folder.
```

Claude will research and produce a playbook covering title tags, meta descriptions, H1 structure, image alt text, schema markup, internal linking, and more — tailored to your business niche.

### Step 2: Review What Came Back

Open the playbook in Obsidian. Read through it. It'll be useful, but probably a bit vague in places. That's normal — the first draft is a starting point, not a finished product.

### Step 3: Refine with Follow-Up Questions

This is where the playbook gets genuinely useful. Ask Claude to add the specifics:

```
This is good, but can you add the recommended character lengths for each
element? For example, what's the ideal H1 length, meta description length,
title tag length, alt text length? Add specific numbers wherever possible.
```

Claude updates the playbook with concrete numbers — not just "write a good meta description" but "keep it under 155 characters, front-load the keyword, include a call-to-action."

You can keep refining:

```
Can you also add common mistakes to avoid for each element? Things that
ecommerce sites in my niche often get wrong?
```

This back-and-forth is the pattern. Claude does the research; you direct and refine. Each round makes the playbook more specific and more useful.

### Step 4: Save the Finished Playbook

Once you're happy with it, check it's saved in `SlingshotAI/Playbooks/`. This playbook is now a permanent reference in your vault — and it's about to become the brain of your first skill.

## Part 2: Turn It Into a Skill

You've got the Anthropic skill-creator installed from Module 3. Now we're going to use it to turn your playbook into a working skill.

### Step 5: Ask Claude to Build the Skill

```
I want to create a skill called "seo-page-check" that uses the SEO playbook
I just created. The skill should:

1. Take a product page URL
2. Visit the page
3. Check each SEO element from my playbook (title tag, meta description,
   H1, images, alt text, schema, etc.)
4. Score each element as pass/fail against the criteria in the playbook
5. For any fails, explain what's wrong and how to fix it
6. Produce a clean checklist report

Use /skill-creator to build this properly with test cases.
```

Claude will use the skill-creator to:
- Write the SKILL.md based on your playbook
- Create test cases to verify it works
- Help you refine the skill description so it triggers correctly

### Step 6: Review the Skill

Claude will show you the SKILL.md it created. Look at it — you'll recognise the structure from the Page Check example in Module 3. Same pattern: frontmatter, instructions, output format. But this one has YOUR research behind it, with specific criteria from YOUR playbook.

### Step 7: Install It

Claude will install the skill to `~/.claude/skills/seo-page-check/`. Once installed, it's immediately available.

## Part 3: Run Your First Skill

### Step 8: Run It On Your Site

```
/seo-page-check https://your-site.com/products/your-best-seller
```

Replace the URL with one of your actual product pages.

Watch what happens. Claude visits the page, checks every SEO element against your playbook's criteria, and produces a scored report telling you exactly what's right and what needs fixing — with specific, actionable suggestions for each issue.

### Step 9: Check the Results

Open the report. You'll see passes and fails with explanations. This is a skill YOU built, using research YOU directed, checking YOUR actual product page.

If something doesn't look right — maybe a check is too strict, or it's missing something you care about — tell Claude:

```
The H1 check is too strict — in my niche, longer H1s are fine. Update
the playbook to allow up to 80 characters, and update the skill to match.
```

Claude updates both the playbook and the skill. Iterate until it works the way you want.

## What Just Happened

You just:

1. **Researched** a topic using Claude
2. **Created a playbook** with specific, actionable criteria
3. **Refined it** through back-and-forth conversation
4. **Built a skill** using the Anthropic skill-creator
5. **Ran that skill** on your own site and got real results
6. **Iterated** to improve it

This is the complete cycle. Every professional SlingshotAI skill follows the same pattern — it's just backed by years of ecommerce experience and hundreds of audits rather than a single research session.

But the point is: you can do this yourself. For any process in your business that follows a repeatable pattern, you can research it, build a playbook, and turn it into a skill.

## Your Playbook and Skill

You now have:
- A **SEO product page playbook** in `SlingshotAI/Playbooks/` — a reference you can update and refine over time
- A **working skill** at `~/.claude/skills/seo-page-check/` — run it on any product page, any time

Both are yours. They run on your machine, they use your criteria, and they get better the more you refine them.

---

[[03 - How Skills Work|← How Skills Work]] | [[05 - Install Your First Skill|Next → Install Your First Skill]]
