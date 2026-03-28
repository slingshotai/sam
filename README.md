# SlingshotAI — Onboarding

Welcome to SlingshotAI. This repo contains your onboarding course, SAM (your Slingshot AI Mentor), and the vault folder structure.

## Setup Instructions

To set up this repo in your Obsidian vault:

1. Clone this repo into a `SlingshotAI/` folder inside the Obsidian vault
2. Create empty folders if not present: `Playbooks/`, `Outputs/`, `Notes/`
3. Copy `skill-packages/sam/` to `~/.claude/skills/sam/`
4. Clone the EP Knowledge Base from `https://github.com/slingshotai/ep-knowledge` and install to `~/.claude/skills/ep-knowledge/` (copy SKILL.md, learn/, and references/ folders)
5. Remove the `skill-packages/` folder from the vault (already installed)
6. Remove this README.md from the vault (installation instructions only)
7. Set up the member profile at `~/.slingshot/profile.md` by asking:
   - Company name
   - Website URL(s) — support multiple sites (each with name, URL, what they sell, ecommerce platform)
   - Currency (e.g. GBP, USD, EUR)
   - Location (city, country)
   - Revenue stage (under $500k/yr or over $500k/yr)
   - AI experience level (never used / tried a few times / use regularly)
8. Save the profile using this frontmatter format:
   ```yaml
   ---
   company: [Company Name]
   sites:
     - name: [Brand Name]
       url: [https://...]
       sells: [What they sell]
       platform: [Shopify/WooCommerce/Craft Commerce/etc]
   currency: [GBP/USD/EUR]
   location: [City, Country]
   revenue_stage: [under_500k / over_500k]
   ai_experience: [never / tried_a_few_times / use_regularly]
   created: [today's date]
   ---
   ```
9. Confirm setup is complete and tell the member: "You're set up. Open Module 3 — How Skills Work — in Obsidian to continue the course."

## For Humans

If you're reading this on GitHub, this is the onboarding course for SlingshotAI members. To use it:

1. Install VS Code and Claude Code (Module 1 — on the SlingshotAI website)
2. Install Obsidian and create a vault (Module 2 — on the website)
3. Paste the setup prompt from Module 2 into Claude Code
4. Claude handles the rest — clones this repo, sets up your vault, and installs SAM

## What's Inside

```
Onboarding Course/     11 modules taking you from zero to running skills
  examples/            An example skill you can explore and run
Playbooks/             Empty — fills up as you research and install skills
Outputs/               Empty — fills up as skills generate reports and guides
Notes/                 Your space for personal notes and learnings
skill-packages/        SAM (Slingshot AI Mentor) — installed during setup
                       EP Knowledge Base installed separately from its own repo
```

## About SlingshotAI

SlingshotAI sells AI skill packages that run on your own Claude Code subscription. You own the tools, run them unlimited times, and learn AI fluency in the process. Skills cover mobile auditing, brand voice, content analysis, and more — with new skills shipping regularly.

Learn more at [slingshotai.com](https://slingshotai.com)
