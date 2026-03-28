# Module 2: Install Obsidian & Enter the System

## What We're Doing

This module has three parts:

1. Install Obsidian and create your vault
2. Understand what GitHub is (you'll need it in a moment)
3. **The handoff** — paste one prompt into Claude that sets everything up. From this point on, the rest of the course lives inside your vault.

This is the last module you'll follow from the website/PDF. After the handoff, you're inside the system.

## Watch First

> **Video:** [Installing Obsidian & entering the system] *(link to walkthrough video)*
>
> Matt shows you how to install Obsidian, explains GitHub in plain English, and walks through the handoff moment.

## Part 1: Install Obsidian

1. Go to **obsidian.md** (that's obsidian dot m-d)
2. Click **"Get Obsidian for free"** — it detects your operating system
3. On Mac: drag it to Applications. On Windows: run the installer.
4. Open Obsidian

### Create Your Vault

When Obsidian first opens, it asks you to create a vault. A vault is just Obsidian's word for a folder of notes — your digital filing cabinet.

1. Click **"Create new vault"**
2. Give it a name — your company name works well, or "My Business"
3. Pick where to save it — **important: read the note below about location**
4. Click Create

### Where to Put Your Vault

**Don't put it in iCloud, Dropbox, or Google Drive.** These cloud sync services can cause issues with Obsidian — corrupted files, sync conflicts, notes that silently overwrite each other. I learned this the hard way with iCloud.

Instead, save your vault to a **local, non-synced folder.** Something like:
- Mac: `/Users/yourname/Vaults/My Business`
- Windows: `C:\Users\yourname\Vaults\My Business`

**"But what about backups?"** Good question. Obsidian has its own sync service — Obsidian Sync — which costs a few dollars a month. It's designed specifically for vaults, handles conflicts properly, and encrypts everything end-to-end. It also syncs to your phone if you want to read notes on the go. I use it across all my devices and it works brilliantly.

You don't need Obsidian Sync to use SlingshotAI. Everything works locally. But if you want peace of mind and multi-device access, it's worth the few pounds a month.

If you ALREADY have an Obsidian vault, that works too. We'll create a SlingshotAI folder inside it, so it won't interfere with anything you've already got. (If your existing vault IS in iCloud/Dropbox and it's been working fine — don't panic. It works for many people. Just be aware of the risk if things start acting strange.)

### Quick Peek Behind the Curtain

If you open your vault folder in Finder (Mac) or Explorer (Windows), you'll see it's just a regular folder on your computer. The notes inside are plain text files with a .md extension. There's nothing proprietary, nothing locked in. If you ever decide to leave Obsidian, your notes go with you.

### Why Obsidian and Not Google Docs / Notion / etc?

Three reasons:

1. **It's local.** Your data stays on your machine. No third-party servers, no subscription, no "we updated our terms of service" surprises.
2. **Claude can read it.** Claude Code can directly access files on your machine. It can't access Google Docs or Notion without complex API setup.
3. **It grows with you.** As you build playbooks, save audit reports, and create voice guides, your vault becomes an increasingly valuable context store. The more Claude knows about your business, the better every skill works.

## Part 2: What Is GitHub?

You're about to use GitHub for the first time, so here's what it is in plain English.

GitHub is a website where people store and share files. Think of it as Google Drive for technical projects — but with a superpower: version control. Every change to every file is tracked, so you can always see what changed, when, and go back if needed.

For SlingshotAI, GitHub is how you:

- **Receive skills** — when you purchase a skill, you get access to a private GitHub repository (a folder of files on GitHub)
- **Get updates** — when we improve a skill (new checks, better playbooks, bug fixes), we push the update to the repo and you pull the latest version
- **Download the onboarding course** — which is what you're about to do right now

You don't need to be a developer to use GitHub. Here's what you actually do:

1. **First time:** Claude downloads (clones) a repository for you. You just give it the URL.
2. **Updates:** Claude pulls the latest changes. Just say "update my skills from GitHub."
3. **That's it.** You never need to learn Git commands. Claude handles them.

If you want to look at a GitHub repo in your browser, it's just a website with folders and files — nothing scary.

## Part 3: The Handoff — Enter the System

This is the moment where you go from following a PDF to working inside the system.

### Step 1: Open Your Vault in VS Code

In VS Code, go to **File → Open Folder** and select your Obsidian vault folder.

### Step 2: Paste This Prompt into Claude Code

Copy and paste this exact prompt:

```
I just joined SlingshotAI. Set up my vault for me:

1. Clone the SlingshotAI onboarding repo from https://github.com/slingshotai/slingshot-onboarding
2. Create this folder structure in my vault:
   - SlingshotAI/Onboarding Course/ (copy the course files here)
   - SlingshotAI/Playbooks/
   - SlingshotAI/Outputs/
   - SlingshotAI/Notes/
3. Install the SAM skill (Slingshot AI Mentor) to ~/.claude/skills/sam/
4. Run SAM's first-time setup to create my member profile

Walk me through each step and tell me what you're doing.
```

### Step 3: Follow Along

Claude will:
1. Download the course files from GitHub into your vault
2. Create the folder structure
3. Install SAM — your learning mentor
4. Ask you some questions to set up your member profile (company name, website, currency, etc.)

**Watch what Claude does.** It'll ask your permission before each step. Click Allow. This is the "Claude does the heavy lifting, you understand what's happening" pattern we talked about in the welcome video.

### Step 4: Check Obsidian

Switch to Obsidian. You should now see:

```
Your Vault/
├── SlingshotAI/
│   ├── Onboarding Course/    ← the rest of this course
│   │   ├── 03 - How Skills Work.md
│   │   ├── 04 - Starter Exercise.md
│   │   ├── ...
│   │   └── Scripts/
│   ├── Playbooks/            ← empty for now, fills up as you install skills
│   ├── Outputs/              ← empty for now, fills up as you run skills
│   └── Notes/                ← your space
```

## You're In

From this point on, open Module 3 in Obsidian. Every module from here is in your vault, and every exercise runs through Claude.

The handoff is done. Welcome to the system.

---

**→ Open Module 3 in Obsidian:** [[03 - How Skills Work|Next → How Skills Work]]

[[01 - Install VS Code and Claude Code|← Install VS Code & Claude Code]]
