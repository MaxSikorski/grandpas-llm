# 👴 grandpas-llm — AI-Powered Tech Support for the People Who Raised You

A portable skill file you feed to any LLM so it can co-pilot you through troubleshooting, optimizing, and maintaining your grandparent's (or parent's, or neighbor's, or that guy from church's) Windows laptop.

Because they taught you how to tie your shoes. The least you can do is fix their WiFi.

---

## The Problem

You're the family tech person. You got the job not because you applied, but because you once connected a printer 12 years ago and now you're IT support for life.

Your grandpa calls when "the computer is slow." Your mom calls when "my file disappeared." Your dad's friend Larry calls when "the Google isn't working." You want to help — but maybe you're a Mac user, or you just don't remember where Windows buries that one setting. And you *definitely* don't want to accidentally break the one machine they rely on to check email and watch YouTube videos about woodworking (or gospel music, or how to grow tomatoes — you know your person).

## The Solution

A single markdown file ([WINDOWS-HELPER-SKILL.md](./WINDOWS-HELPER-SKILL.md)) that gives any LLM the full context it needs to be your Windows co-pilot. Load it up, and the model knows:

- You're technical, but not a Windows expert.
- The end user is elderly and non-technical — and that's perfectly fine, they have other skills (like making the best biscuits you've ever had).
- The machine is probably low-spec (4–8 GB RAM, working harder than it should be).
- Safety matters — no destructive commands without confirmation. This is someone's *only* computer.
- **The user's familiar environment must not be disrupted.** If you move their desktop icons, you *will* get a phone call. Possibly several.

## How to Use It

### What You Need
- Access to any LLM via API (OpenRouter, Claude API, etc.) or a local model.
- A CLI tool that can interact with the model (Claude Code, aider, open-code, etc.).
- Your loved one's Windows laptop in front of you.
- Patience. And maybe a cup of whatever they insist on making you while you work.

### Quick Start

1. **Set up your API access** on their machine. Use a temporary, spend-capped API key. (Pro tip: set it to expire in 24 hours so you're not funding a rogue AI on grandpa's Dell.)
2. **Feed the skill file to your model.** Either paste the raw GitHub URL or copy the contents directly:
   ```
   https://raw.githubusercontent.com/MaxSikorski/grandpas-llm/main/WINDOWS-HELPER-SKILL.md
   ```
3. **Start with Phase 1.** Tell the model to walk you through a system assessment. Copy-paste the PowerShell commands it gives you. Marvel at the 47 startup programs.
4. **Work through the issues.** "Their computer is slow" → Phase 2. "They lost a file" → Phase 3 (it's in Downloads, it's *always* in Downloads). "I want to check for malware" → Phase 4.
5. **Clean up when you're done.** Revoke or let your API key expire. Uninstall any CLI tools if you don't plan to return soon. Accept the leftovers they're sending you home with.

## What's Inside the Skill File

| Phase | What It Covers |
|---|---|
| **1 — System Assessment** | Hardware specs, RAM usage, disk space, startup programs |
| **2 — Optimization** | Free up RAM, clear disk space, browser cleanup |
| **3 — Common Scenarios** | Lost files, slow internet, pop-ups, slow performance, accessibility |
| **4 — Security** | Windows Defender status, malware scans, suspicious processes |
| **5 — Future LLM Setup** | Scoping the machine for a local model deployment (Ollama, Gemma, etc.) |

Plus quick-reference tables for Windows paths and keyboard shortcuts — because you're not going to remember that `Win+Shift+S` is screenshot on Windows when you've been hitting `Cmd+Shift+4` for years.

## Long-Term Vision

Phase 5 exists because the dream is to *not* be on-call forever. With small, capable local models (like Google's Gemma 4 E2B at 2B parameters), it's becoming feasible to run a simple AI assistant directly on these low-spec machines — no API key, no ongoing cost. Pair that with a friendly chat UI and voice input, and grandpa could ask his own computer "where did my file go?" and actually get an answer.

Imagine: a world where you get a call from grandpa not because something's broken, but just because he wants to talk. That's the goal.

That's a separate project, but this skill file helps you scope the hardware while you're already sitting in front of it.

## Tips

- **Create a restore point first** (Phase 4 has the command) before making significant system changes. Future you will be grateful.
- **Don't rearrange their desktop.** I cannot stress this enough. That icon grid is a sacred map. They know exactly where "the email button" is. You move it, you become the reason "the email is gone."
- **Check the Downloads folder.** It contains every PDF, image, and installer they've downloaded since 2019. It's basically a digital junk drawer. Clean it *with them* so they don't panic.
- **Startup programs** are the number one cause of "my computer is slow." Forty-seven things launching at boot on 4 GB of RAM is not a recipe for success.
- **Ask before you "fix" things.** That toolbar you think is bloatware might be how they access their email. That weird browser homepage might be intentional. When in doubt, ask.
- **Be patient.** They're not dumb — they just didn't grow up with this stuff. They can tell you the weather by looking at the sky, fix an engine with a wrench and intuition, or cook a meal for twelve without a recipe. Computers just aren't their thing, and that's okay. The reason you're there is because someone trusts you with something they don't understand. That's love. Treat it that way.

## Contributing

If you've run into other common scenarios while helping non-technical family members, feel free to open a PR and add them to the skill file. Keep the same format: PowerShell-first, explain before executing, flag anything destructive.

Bonus points if your PR includes the story of what your grandparent said when you fixed it. We all need those stories.

## License

MIT — Use it, share it, help your people. They helped you first.
