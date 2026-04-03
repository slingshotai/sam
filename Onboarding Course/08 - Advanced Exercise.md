# Module 6: Advanced Exercise — APIs & MCP Servers

## Part 1: Introduction

Some SlingshotAI skills need to connect to external services. This module covers two types of connection:

1. **API keys** — passwords that let Claude access external data (like Google PageSpeed for site speed checks)
2. **MCP servers** — plugins that give Claude new capabilities (like Playwright for taking screenshots of websites)

This is the most technical module in the onboarding. If you can do this, you can handle anything SlingshotAI ships. And Claude does the heavy lifting — you just need to follow along and understand what's happening.

### Why Some Skills Need External Connections

Think of it this way:

- **API keys** give Claude access to **data** it can't get on its own. Google's PageSpeed data, Shopify analytics, search engine results — these live behind passwords.
- **MCP servers** give Claude new **abilities** it doesn't have natively. Taking screenshots of websites, reading your email, checking your calendar — these require plugins.

Most SlingshotAI skills don't need either. But the powerful ones do — Moby needs both a Google API key AND Playwright MCP. Once you've set these up once, they work for every skill that needs them.

**This module is optional.** If you want to skip it for now, that's fine — come back when you buy a skill that needs an API or MCP server. SAM can walk you through any of this at any time.

---

## Part 2: API Keys

Video link: *(coming soon)*

### What Is an API Key?

An API key is a password that lets Claude access an external service on your behalf. For example:

- **Moby (Mobile Audit)** needs a Google PageSpeed API key to check your site's speed
- **Narrative Binding** needs a Google API key to access research data
- Some future skills may need Shopify API access, analytics connections, etc.

The key is free to get (most services have a free tier). It lives on your machine — not in the cloud, not shared with anyone.

### The Exercise: Get a Google API Key

We're going to get a Google PageSpeed Insights API key. This is the most common API you'll need across SlingshotAI skills, and it's completely free.

#### Step 1: Ask Claude to Guide You

```
Help me get a Google PageSpeed Insights API key. I've never done this before —
walk me through every step and explain what's happening.
```

Claude will walk you through:
1. Going to the Google Cloud Console
2. Creating a project (or using an existing one)
3. Enabling the PageSpeed Insights API
4. Generating an API key
5. Saving it securely on your machine

#### Step 2: Verify It Works

Once you have the key, ask Claude:

```
Test my Google PageSpeed API key by checking the speed of my store: [your URL]
```

Claude will use the key to call the PageSpeed API and return your site's speed scores. If it works, the key is valid and you're set.

#### Step 3: Store It Securely

Claude will help you save the key in a way that any skill can access it without you re-entering it each time. This is a one-time setup.

### What Just Happened

You've now:
1. Obtained an API key from an external service
2. Connected it to Claude Code
3. Verified it works by making a real API call
4. Stored it for future use

This pattern applies to any skill that needs an API. The service changes (Google, Shopify, whatever), but the process is the same: get the key, give it to Claude, verify, store.

### What If Your IT Department Blocks This?

If you're in a corporate environment and can't access Google Cloud Console, options include:
- Running on a personal machine (the API only accesses public website data)
- Having IT approve Google Cloud Console access (it's a standard Google service)
- Using a dedicated machine for AI work

---

## Part 3: MCP Servers

Video link: *(coming soon)*

### What Is an MCP Server?

API keys give Claude access to data. MCP servers give Claude new abilities — things it can't do on its own.

MCP stands for Model Context Protocol. An MCP server is a plugin that extends what Claude can do. For example:

- **Playwright MCP** — lets Claude control a web browser. This is how Moby takes screenshots of your site on a simulated mobile phone.
- **Gmail MCP** — lets Claude read and send emails on your behalf
- **Google Calendar MCP** — lets Claude check your schedule and create events

Without Playwright installed, Claude can't take screenshots. With it installed, Claude can open any website, resize the browser to mobile dimensions, scroll through pages, and capture what it sees. That's the difference.

### How to Install an MCP Server

It's simpler than it sounds. Ask Claude:

```
Install the Playwright MCP server for me. I need it for the Moby mobile audit skill.
```

Claude will:
1. Install the MCP server (usually a single command)
2. Configure it to work with Claude Code
3. Verify it's connected

Some skills include their MCP requirements in the README. When Claude installs the skill, it'll tell you if an MCP server is needed and offer to install it.

### Which MCP Servers Will I Need?

Most SlingshotAI skills don't need any MCP servers. The ones that do will tell you during installation. The most common one is Playwright (for any skill that needs to look at websites).

You can see what MCP servers you have installed by asking:

```
What MCP servers do I have connected?
```

### Safety Note

The same safety rules apply to MCP servers as to skills — only install them from trusted sources. Anthropic maintains a list of verified MCP servers, and any MCP server required by a SlingshotAI skill has been tested by us.

---

## You're Ready for Anything

This was the hardest module in the onboarding. If you made it through, every skill in the SlingshotAI catalogue is now within your reach — including ones that need API keys and MCP servers.

---

[[07 - The Story Overlap|← The Story Overlap]] | [[09 - Meet SAM|Next → Meet SAM]]
