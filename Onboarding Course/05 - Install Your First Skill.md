# Module 5: Install Your First Skill — Brand Voice

Video Link: https://www.youtube.com/watch?v=6OVG6bhXl7U

## What We're Doing

This module has two parts:

1. **Set up GitHub authentication** — so Claude can download private skill repos on your behalf
2. **Purchase and install your first skill** — Brand Voice, from the SlingshotAI store

In Module 2 we installed Git (the tool that downloads repos). Now we need to authenticate it with your GitHub account so Claude can access private repos — which is where all paid skills live.

## Part 1: Authenticate GitHub

### Why This Matters

In Module 2, Claude downloaded the onboarding course from a public GitHub repo — no login needed. But paid skills like Brand Voice live in **private** repos. To access those, Claude needs to be logged into your GitHub account.

This is a one-time setup. Once done, Claude can download and update any skill you've purchased.

### Step 1: Install the GitHub CLI

The GitHub CLI (`gh`) is a small tool that handles authentication. Ask Claude to install it:

```
Help me install the GitHub CLI (gh) on my machine.
```

Claude will detect your operating system and give you the right command:

- **Mac with Homebrew:** `brew install gh`
- **Mac without Homebrew:** Claude will help you install Homebrew first (`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`) then `brew install gh`
- **Windows:** `winget install --id GitHub.cli`
- **Direct download:** If none of the above work, go to cli.github.com

### Step 2: Create a GitHub Account (If You Don't Have One)

If you don't already have a GitHub account:

1. Go to **github.com**
2. Click **Sign up**
3. Create a free account (email + password)

The free account is all you need. You don't need a paid GitHub plan.

### Step 3: Log In

In the terminal (or ask Claude to guide you), run:

```
gh auth login
```

When prompted, choose:
- **GitHub.com** (not GitHub Enterprise)
- **HTTPS**
- **Login with a web browser**

Your browser opens. Log in to your GitHub account and authorise the CLI. Come back to VS Code — you're authenticated.

### Step 4: Verify It Worked

Run:

```
gh auth status
```

You should see your username and "Logged in." If you do, you're ready to download any private skill repo you have access to.

**Claude Code shortcut:** You can also just ask Claude: "Help me authenticate Git with my GitHub account" and it'll walk you through the whole process.

---

## Part 2: Purchase and Install Brand Voice

### Step 1: Purchase Brand Voice

> **Go to the SlingshotAI store** *(link to store)*
>
> Find **Brand Voice** ($49) and purchase it using your store credit.
> After purchase, you'll get access to the skill's private GitHub repo.

Brand Voice analyses your ecommerce site and produces a complete voice guide — the kind of document you'd hand to a copywriter or plug into any AI tool so everything you publish sounds like you.

### Step 2: Let Claude Install It

Once you've purchased and been granted access to the repo, tell Claude:

```
Install the Brand Voice skill from the SlingshotAI GitHub.
```

Claude will:
1. Clone the private repo (now possible because you authenticated GitHub)
2. Copy the SKILL.md and supporting files to `~/.claude/skills/brand-voice/`
3. Verify the skill is registered and available
4. Explain each step as it goes

You should see Claude confirm: "Brand Voice is installed and ready."

### Step 3: Run It

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

### Step 4: Review with SAM

After Brand Voice produces your guide, ask SAM about it:

```
sam, teach me about brand voice
```

SAM will walk you through the methodology — what the dimension scores mean, why the vocabulary bank matters, how to use the tone-by-context matrix. This is the `/learn` integration in action: every skill you install is automatically teachable through SAM.

## What Just Happened

You've completed the full member cycle:
1. **Authenticated GitHub** — so Claude can access private skill repos
2. **Purchased** a skill from the store (using credit)
3. **Installed** it via Claude from the private repo
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

[[04 - Starter Exercise|← Starter Exercise]] | [[05B - The Slingshot Framework|Next → The Slingshot Framework]]
