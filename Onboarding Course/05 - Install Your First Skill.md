# Module 5: Install Your First Skill — Brand Voice

## What We're Doing

This module has two parts:

1. **Set up GitHub authentication** — so Claude can download private skill repos on your behalf
2. **Purchase and install your first skill** — Brand Voice, from the SlingshotAI store

In Module 2 we installed Git (the tool that downloads repos). Now we need to authenticate it with your GitHub account so Claude can access private repos — which is where all paid skills live.

## Part 1: Authenticate GitHub

Video Link: https://www.youtube.com/watch?v=6OVG6bhXl7U

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

## Part 2: Purchase and Install Brand Voice Pro

Video link: https://www.youtube.com/watch?v=xrnExjNQVrA

### Step 1: Purchase Brand Voice Pro

> **Go to the SlingshotAI store** *(link to store)*
>
> Find **Brand Voice Pro** (£140 / $175) and purchase it using your store credit.
> After purchase, you'll get access to the skill's private GitHub repo.

Brand Voice Pro is the full package. It doesn't just define a single brand's voice — it builds a complete voice architecture across your entire portfolio. Whether you've got one brand or five, it:

- **Analyses your site(s)** and existing content
- **Builds individual voice guides** for each brand — traits, vocabulary, tone by context, sample rewrites
- **Creates a portfolio layer** showing what's shared vs unique across brands
- **Runs a differentiation check** to make sure your brands don't sound the same
- **Detects voice bleed** — where one brand's voice is leaking into another's content

If you've only got one brand right now, that's fine — it builds a single voice guide and you're set. When you add a second brand later, the portfolio features kick in.

### Step 2: Accept the GitHub Invitation

After purchase, you'll get an email from GitHub inviting you to collaborate on the `slingshotai/brand-voice-pro` repository. Click the link in the email and accept the invitation on GitHub.

If you can't find the email, go directly to: `github.com/slingshotai/brand-voice-pro/invitations`

### Step 3: Clone and Set Up

Once you've accepted the invitation, open Claude Code and type:

```
Clone the repo https://github.com/slingshotai/brand-voice-pro and set it up following the instructions in SKILL.md
```

Claude will:
1. Clone the private repo (this works because you authenticated GitHub in Part 1)
2. Follow the setup instructions in the SKILL.md
3. Copy the skill files to the right location
4. Explain each step as it goes

If Claude needs any help with setup, ask:

```
Can you help me with any set up on this skill that is needed?
```

You should see Claude confirm that Brand Voice Pro is installed and ready.

---

## Part 3: Run Brand Voice Pro

Video link: *(coming soon)*

### Step 1: Run It

Now use the skill:

```
/brand-voice-pro https://your-store-url.com
```

Replace with your actual store URL. Claude will:
1. Read your member profile (it already knows your business and all your sites from SAM's first-run questionnaire)
2. Ask whether you want to build voice guides for all your brands or just one to start
3. Walk you through brand personality questions for each brand
4. Analyse each site's existing content
5. Build individual voice guides + the portfolio architecture
6. Run a differentiation check if you have multiple brands
7. Save everything to your vault

This takes about 15-20 minutes per brand. The output is a complete voice system you'll use every time you write copy, brief a freelancer, or set up an AI writing tool.

### Step 2: Review with SAM

After Brand Voice Pro produces your guides, ask SAM about it:

```
sam, teach me about brand voice
```

SAM will walk you through the methodology — what the dimension scores mean, why the vocabulary bank matters, how to use the tone-by-context matrix, and how the portfolio layer keeps your brands distinct. This is the `/learn` integration in action: every skill you install is automatically teachable through SAM.

## What Just Happened

You've completed the full member cycle:
1. **Authenticated GitHub** — so Claude can access private skill repos
2. **Purchased** a skill from the store (using credit)
3. **Installed** it via Claude from the private repo
4. **Ran** it on your own business
5. **Learned** the methodology through SAM

This exact flow works for every skill in the catalogue. Moby, iGAP, Narrative Binding, the Slingshot Course — same process every time.

## Your Voice Guide(s)

The voice guide(s) Claude just created are yours to keep. Use them to:
- Brief freelance copywriters (hand them the specific brand's guide)
- Set up any AI writing tool (paste the relevant voice guide as context)
- Check your own writing against your defined voice
- Share with team members so everyone writes consistently
- Run periodic audits: `/brand-voice-pro audit` checks live content against the guides

Ask SAM if you want to understand any section in more depth.

---

[[04 - Starter Exercise|← Starter Exercise]] | [[05B - The Slingshot Framework|Next → The Slingshot Framework]]
