# Module 3: How Skills Work

> **You're reading this in Obsidian.** That means the handoff worked — Claude set up your vault, installed SAM, and copied the course files. Everything from here runs inside the system.

## What We're Doing

Before you install your first skill, it helps to understand what a "skill" actually is. It's simpler than you might think.

## Watch First

> **Video:** https://www.youtube.com/watch?v=zGc5OU4AUx4

## What Is a Skill?

A skill is a set of instructions that tells Claude how to do something specific. That's it. It's a text file (called SKILL.md) that describes:

- What the skill does
- What steps to follow
- What inputs it needs
- What output to produce
- What reference materials to consult

Think of it like giving a very capable assistant a detailed brief for a specific task. Without the brief, the assistant is generally helpful. With the brief, the assistant is an expert at that particular thing.

## See One for Yourself

There's an example skill included with this course. Open it now:

**→ [[examples/example-skill/SKILL.md|Open the example skill]]**

This is a "Page Check" skill — it visits a product page URL and checks whether the essentials are present (title, description, images, price, CTA, meta description). Read through it. Notice:

- The **frontmatter** at the top (between the `---` lines) — this tells Claude the skill's name, when to use it, and how to trigger it
- The **checklist of elements** — specific things to check, with clear pass/fail criteria
- The **output format** — exactly what the result should look like, with an example
- The **"Important" section** — rules about how Claude should behave (be honest, give actionable suggestions)

That's a complete skill. It's just a text file with structured instructions. Every skill in the SlingshotAI store follows this same pattern — they're just more sophisticated, with deeper methodologies and scoring rubrics built from years of real-world work.

## What's in a Skill Package?

The example above is a simple skill — one file. When you install a skill from the SlingshotAI store, you typically get a folder with supporting materials:

```
skill-name/
├── SKILL.md                ← the instructions (the brain)
├── references/             ← playbooks, scoring rubrics, methodology docs
│   └── playbook.md
├── learn/                  ← learning content for SAM
│   ├── overview.md
│   ├── methodology.md
│   ├── exercises.md
│   └── faq.md
└── (scripts, templates)    ← some skills include helper scripts
```

The **SKILL.md** is the core. Everything else supports it.

## How Does Claude Find Skills?

Skills live in a specific folder on your machine:

```
~/.claude/skills/           ← global skills (work everywhere)
```

When Claude Code starts, it reads all the skills in this folder. When you type a command like `/mobile-audit`, Claude finds the matching skill and follows its instructions.

## How Does SAM Fit In?

SAM is itself a skill — but it's a special one. SAM searches other skills' `learn/` folders to teach you about them. When you ask SAM a question, it:

1. Searches all installed skills for relevant learning content
2. Finds the best match
3. Teaches you from that content, in Matt's voice, using your own business data

This means every skill you install automatically becomes something SAM can teach you about. You never need a separate course for each tool.

## Installing a Skill

When you buy a skill, Claude handles the installation:

1. You get access to a GitHub repository (just like you did with this course)
2. You give Claude the URL
3. Claude downloads the files and copies them to the right location (`~/.claude/skills/`)
4. The skill is immediately available

No terminal commands to memorise, no configuration files to edit. Claude reads the README and does the work.

## Free Skills from Anthropic

Anthropic — the company behind Claude — publishes their own free skills on GitHub. You can find them at github.com/anthropics/skills.

These cover things like general productivity, code review, and documentation. They're a great way to see how skills are structured if you're curious, and they're completely free to install.

Let's install one now. Type this into Claude:

```
I want to install a skill from Anthropic. What's available?
```

> **Note:** The prompts in this module are the latest versions. If the video shows slightly different wording, follow the written prompts here.

Claude will show you the list. When it does, ask it to **install the skill-creator** — we'll need this in Module 4 when you build your own skill:

```
Can you install the skill-creator skill? We'll need it later.
```

## Safety: Be Careful What You Install

This is important. A skill is a set of instructions that Claude follows — and Claude can do a lot. It can read files, write files, run commands, access your vault. That's what makes skills powerful, but it's also why you need to be careful about what you install.

**Only install skills from sources you trust.**

| Source | Trust level |
|---|---|
| **SlingshotAI store** | Trusted. Every skill is built and tested by Matt and the team. |
| **Anthropic's official skills** | Trusted. Published by the company that makes Claude. |
| **A skill someone sent you online** | Be cautious. Read the SKILL.md before installing. If it asks Claude to do things that seem unrelated to its stated purpose — like accessing files it shouldn't, sending data somewhere, or running scripts you don't understand — don't install it. |
| **A skill from an unknown marketplace** | Be cautious. Same rules as above. |

The good news: Claude asks for permission before it does things. If a skill tries to run a command or access a file, Claude will show you what it wants to do and wait for you to Allow or Deny. Pay attention to those permission prompts, especially with skills you didn't get from SlingshotAI or Anthropic.

**A simple rule:** if you wouldn't give a stranger access to your computer, don't install their skill.

## Try It: Explore What's Installed

Ask Claude:

```
What skills do I have installed? List them with a one-line description of each.
```

Right now you should see SAM (your learning mentor). After the next modules, you'll see more.

## The Key Insight

Skills aren't magic. They're structured instructions that make Claude consistently good at specific tasks. The methodology, the scoring rubrics, the playbooks — that's where the real value is. You're not buying software; you're buying expertise packaged in a way Claude can execute.

---

[[02 - Install and Set Up Obsidian|← Install & Set Up Obsidian]] | [[04 - Starter Exercise|Next → Starter Exercise]]

