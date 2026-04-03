# Module 9: Meet SAM — Your Slingshot AI Mentor

## What We're Doing

You've already been using Claude Code directly. Now it's time to meet SAM — the layer on top that turns every skill into a learning experience.

SAM stands for **Slingshot AI Mentor**. It's an AI tutor that sounds like Matt, knows every skill you've installed, and teaches using your own business data. It's the difference between reading a manual and having someone walk you through it on your site.

## SAM's First Run

If you haven't talked to SAM yet, type:

```
sam, hello
```

SAM will introduce itself and, if this is your first interaction, ask you a few questions to set up your member profile:
- Your company name
- Your store URL(s)
- What you sell
- Your ecommerce platform
- Your currency
- Your location
- Your experience level with AI

This takes about 2 minutes. SAM uses this profile to personalise everything — pricing in your currency, demos on your actual site, explanations matched to your experience level.

## What SAM Can Do

### Ask a Question

```
sam, why do mobile pages need sticky CTAs?
```

SAM searches your installed skills for relevant learning content and answers in Matt's voice — practical, not corporate, connected to your specific business.

### Learn a Topic

```
sam, teach me mobile auditing
```

SAM pulls you into a guided lesson using your own site. It asks questions, walks through concepts one at a time, and celebrates when you get something right.

### See a Skill in Action

```
sam, show me what Moby does
```

SAM explains the skill, offers to run it on your site as a demonstration, and walks through the output explaining what each section means and what to do about it.

### Discover What's Available

```
sam, what can I learn about?
```

SAM lists every installed skill that has learning content. As you buy more skills, this list grows automatically.

## SAM vs Claude

You might be wondering — why not just ask Claude directly?

**Claude** is your general assistant. It can do anything: write code, answer questions, process files, run commands. It's powerful but generic.

**SAM** is your ecommerce mentor. It speaks in Matt's voice, teaches from proven methodologies, and personalises everything to your business. When you ask SAM about mobile conversion, you get 20 years of ecommerce experience distilled into a conversation about YOUR site.

Use Claude for tasks. Use SAM for understanding.

## Try These

Spend 5 minutes playing with SAM. Here are some prompts to try:

```
sam, what's the difference between voice and tone?
```

```
sam, I want to improve my site
```

```
sam, what skills do I have installed?
```

```
sam, how do I set up Google Merchant Centre?
```

That last one is interesting — SAM doesn't have a skill for Google Merchant Centre. Watch how it handles a topic it doesn't have specific learning content for.

## Your Profile

Your member profile is saved at `~/.slingshot/profile.md`. You can update it anytime:

```
sam, update my profile
```

If you add a new store, change platforms, or want to adjust your experience level, SAM will update the file.

## Keeping SAM Updated

We regularly improve SAM — better teaching content, new framework knowledge, refined voice. To check for updates:

```
Check if there are updates to SAM on GitHub and install them
```

Claude will check the SlingshotAI onboarding repo for any changes to SAM's skill files and pull the latest version. This works for any installed skill, not just SAM — it's the same pattern:

```
Check for updates to [skill name] on GitHub
```

We'll let you know when significant updates ship, but it's good practice to check periodically — especially if SAM's knowledge seems out of date or you've seen us announce new features.

---

[[08 - Advanced Exercise|← Advanced Exercise]] | [[10 - Whats Next|Next → What's Next]]
