# Module 5: Install Your First Skill — Brand Voice

## What We're Doing

This is the intermediate exercise. You're going to:
1. Purchase your first skill from the SlingshotAI store using your included store credit
2. Download the skill package
3. Let Claude install it
4. Run it on your brand

This teaches the full cycle: purchase → download → install → run. Once you've done this once, you can do it for any skill in the catalogue.

## Step 1: Purchase Brand Voice

> **Go to the SlingshotAI store** *(link to Lemon Squeezy / store)*
>
> Find **Brand Voice** ($49) and purchase it using your store credit.
> After purchase, you'll get access to download the skill package.

Brand Voice analyses your ecommerce site and produces a complete voice guide — the kind of document you'd hand to a copywriter or plug into any AI tool so everything you publish sounds like you.

## Step 2: Download the Skill Package

After purchase, download the `slingshot-brand-voice` folder to your computer. Put it somewhere you can find it — your Downloads folder is fine.

## Step 3: Let Claude Install It

In Claude Code, say:

```
I've downloaded the Brand Voice skill to [path to your download].
Please install it for me and explain what you're doing.
```

Claude will:
1. Read the skill's README
2. Copy the SKILL.md and supporting files to `~/.claude/skills/brand-voice/`
3. Verify the skill is registered and available
4. Explain each step as it goes

You should see Claude confirm: "Brand Voice is installed and ready."

## Step 4: Run It

Now use the skill:

```
/brand-voice https://your-store-url.com
```

Replace with your actual store URL. Claude will:
1. Read your member profile (it already knows your business from SAM's first-run questionnaire)
2. Ask you a few questions about your brand personality
3. Analyse your site's existing content
4. Produce a complete voice guide
5. Save it to your vault

This takes about 15-20 minutes of conversation. The output is a document you'll use every time you write copy, brief a freelancer, or set up an AI writing tool.

## Step 5: Review with SAM

After Brand Voice produces your guide, ask SAM about it:

```
sam, teach me about brand voice
```

SAM will walk you through the methodology — what the dimension scores mean, why the vocabulary bank matters, how to use the tone-by-context matrix. This is the `/learn` integration in action: every skill you install is automatically teachable through SAM.

## What Just Happened

You've completed the full member cycle:
1. **Purchased** a skill from the store (using credit)
2. **Downloaded** the skill package
3. **Installed** it via Claude (no technical knowledge needed)
4. **Ran** it on your own business
5. **Learned** the methodology through SAM

This exact flow works for every skill in the catalogue. Moby, iGAP, Narrative Binding, the Slingshot Course — same process every time.

## Your Voice Guide

The voice guide Claude just created is yours to keep. Use it to:
- Brief freelance copywriters
- Set up any AI writing tool (paste it as context)
- Check your own writing against your defined voice
- Share with team members so everyone writes consistently

Ask SAM if you want to understand any section in more depth.

---

[[04 - Starter Exercise|← Starter Exercise]] | [[06 - Advanced Exercise|Next → Advanced Exercise]]

 