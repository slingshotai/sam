# Module 6: Supercharge SAM's Brain & Install the EP Knowledge Base

## What We're Doing

In Module 2, SAM was installed with a starter brain — enough to teach the Slingshot Framework basics and answer general questions. Now that you've authenticated GitHub (Module 5), we can give SAM two major upgrades:

1. **The Full Brain** — deep framework knowledge, playbooks, and methodology
2. **The EP Knowledge Base** — 285+ searchable eCommerce Podcast episodes

Together, these turn SAM from a helpful mentor into a comprehensive ecommerce intelligence system.

> **Before you start:** Both the Brain and EP Knowledge Base are private repos. You need access to download them. If you haven't already, go to your account on the SlingshotAI website and make sure you've activated access to these repos. If you're not sure, check your account page — there'll be a section for activating your membership repos.

---

## Part 1: Install the Full Brain

### What's in the Full Brain?

SAM's brain has two sections:

#### Framework Knowledge
The complete Slingshot Framework with deep-dives into each area:
- **Sell** — Product Quadrant, hero product strategy, demand analysis
- **Story** — The Story Overlap, brand messaging, the We vs You diagnostic
- **Tech Stack** — platform strategy, mobile-first architecture
- **Marketing** — the full FUEL framework (Foundation → Unlock → Elevate → Leapfrog) across all 8 marketing areas
- **Optimise** — conversion pillars, product page methodology, CTA strategy
- **Experience** — post-purchase journey, unboxing, onboarding sequences
- **Growth** — the three growth variables, referral systems, loyalty

#### Playbooks
Research-backed playbooks on specific topics:
- Viral coefficient and referral-driven growth
- Paid membership programme design
- More added regularly as new research is completed

### Install It

> **Need access?** If Claude gets a permission error, you may need to activate your Brain access on the SlingshotAI website first. Go to your account page and check the membership repos section.

This is a one-prompt job. Ask Claude:

```
Clone SAM's brain from https://github.com/slingshotai/sam-brain and install it.
Put the brain folder at ~/.claude/skills/sam/brain/
```

> **Note:** The prompt above is the latest version. If the video shows slightly different wording, follow the written prompt here.

Claude will:
1. Clone the private repo (works because you authenticated GitHub in Module 5)
2. Copy the brain folder to SAM's skill directory
3. Confirm what was installed

### Test It

Ask SAM something that needs deep framework knowledge:

```
sam, explain the Story Overlap and how I can use it on my site
```

With the starter brain, SAM would give you the basics. With the full brain, SAM walks you through the complete methodology — the Venn diagram, the We vs You ratio diagnostic, the three-step process for finding your overlap, the Netflix headline formula, and specific examples you can apply to your business.

Try another:

```
sam, walk me through the FUEL matrix for my marketing
```

SAM now has the full 4x8 matrix — every marketing area at every FUEL stage — and can assess where your business sits across all 32 combinations.

---

## Part 2: Install the EP Knowledge Base

### What Is It?

The EP Knowledge Base is a searchable archive of 285+ eCommerce Podcast episodes. Every episode has been tagged with:

- **Slingshot areas** — which of the 7 framework areas it covers
- **FUEL stages** — the marketing maturity level of the tactics discussed
- **Key takeaway** — the single most actionable insight in one sentence
- **Related skills** — which SlingshotAI skills connect to the content
- **Full episode content** — the complete blog post and transcript

When you ask SAM a question, it can now pull in real-world evidence from founders, agency experts, and practitioners who've been on the show. Not just theory — proof that the methodology works, with specific examples.

### Install It

> **Need access?** Same as the brain — if Claude gets a permission error, activate your EP Knowledge access on the SlingshotAI website first.

```
Clone the EP Knowledge Base from https://github.com/slingshotai/ep-knowledge
and install it to ~/.claude/skills/ep-knowledge/
```

Claude will:
1. Clone the private repo
2. Copy the skill files, episode index, and all episode content
3. Confirm what was installed and how many episodes are available

### Test It

```
What EP episodes cover referral marketing?
```

Claude searches the tagged index and returns the most relevant episodes with their key takeaways and Slingshot Framework mapping.

Try connecting it to a skill you've used:

```
sam, I ran Brand Voice Pro and it mentioned the Story Overlap.
Are there any EP episodes where someone talks about this in practice?
```

SAM draws from the brain (the Story Overlap methodology) and the EP Knowledge Base (real examples from the podcast) to give you both the theory and the evidence.

---

## What Just Changed

SAM now has three knowledge layers working together:

1. **The Brain** — Matt's direct knowledge. The Slingshot Framework, FUEL, playbooks. When SAM teaches from this, it's "here's what I've learned over 20 years."
2. **EP Knowledge** — 285+ episodes of conversations with founders and experts. When SAM references this, it's "Jay Myers covered this on EP 283" — attributed, not presented as Matt's own insight.
3. **Skill-specific learning** — each skill you install has its own learn/ folder. When you ask about Brand Voice Pro or Moby, SAM teaches from that skill's content.

This is the full system. Every question you ask SAM can now draw from methodology, evidence, and skill-specific knowledge — all personalised to your business through your member profile.

## Keeping Everything Updated

Everything updates with one command:

```
sam, update
```

SAM checks all components — the skill itself, the brain, EP Knowledge, and any purchased skills — shows you what's changed, and asks before updating. New EP episodes, new framework content, refined playbooks — all delivered through this one command.

---

[[05 - Install Your First Skill|← Install Your First Skill]] | [[07 - The Slingshot Framework|Next → The Slingshot Framework]]
