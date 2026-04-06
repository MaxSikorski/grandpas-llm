# 🖥️ Elder Tech Support — LLM-Assisted Windows Helper

A portable skill file you feed to any LLM so it can co-pilot you through troubleshooting, optimizing, and maintaining an elderly person's Windows laptop.

---

## The Problem

You're the family tech person. Your parents, grandparents, or older friends call you when "the computer is slow" or "my file disappeared." You want to help — but maybe you're a Mac user, or you just don't remember where Windows buries that one setting. And you definitely don't want to accidentally break the one machine they rely on.

## The Solution

A single markdown file ([WINDOWS-HELPER-SKILL.md](./WINDOWS-HELPER-SKILL.md)) that gives any LLM the full context it needs to be your Windows co-pilot. Load it up, and the model knows:

- You're technical, but not a Windows expert.
- The end user is elderly and non-technical.
- The machine is probably low-spec (4–8 GB RAM).
- Safety matters — no destructive commands without confirmation.
- The user's familiar environment (desktop, browser, settings) should not be disrupted.

## How to Use It

### What You Need
- Access to any LLM via API (OpenRouter, Claude API, etc.) or a local model.
- A CLI tool that can interact with the model (Claude Code, aider, open-code, etc.).
- The elderly person's Windows laptop in front of you.

### Quick Start

1. **Set up your API access** on their machine. Use a temporary, spend-capped API key if you're using a paid service.
2. **Feed the skill file to your model.** Either paste the raw GitHub URL or copy the contents directly:
   ```
   https://raw.githubusercontent.com/YOUR_USERNAME/elder-tech-support/main/WINDOWS-HELPER-SKILL.md
   ```
3. **Start with Phase 1.** Tell the model to walk you through a system assessment. Copy-paste the PowerShell commands it gives you.
4. **Work through the issues.** "Their computer is slow" → Phase 2. "They lost a file" → Phase 3. "I want to check for malware" → Phase 4.
5. **Clean up when you're done.** Revoke or let your API key expire. Uninstall any CLI tools if you don't plan to return soon.

## What's Inside the Skill File

| Phase | What It Covers |
|---|---|
| **1 — System Assessment** | Hardware specs, RAM usage, disk space, startup programs |
| **2 — Optimization** | Free up RAM, clear disk space, browser cleanup |
| **3 — Common Scenarios** | Lost files, slow internet, pop-ups, slow performance, accessibility |
| **4 — Security** | Windows Defender status, malware scans, suspicious processes |
| **5 — Future LLM Setup** | Scoping the machine for a local model deployment (Ollama, Gemma, etc.) |

Plus quick-reference tables for Windows paths and keyboard shortcuts.

## Long-Term Vision

Phase 5 exists because the end goal isn't to always be the one providing tech support. With small, capable local models (like Google's Gemma 4 E2B at 2B parameters), it's becoming feasible to run a simple AI assistant directly on these low-spec machines — no API key, no ongoing cost. Pair that with a friendly chat UI and voice input, and your grandparent could ask their own computer for help.

That's a separate project, but this skill file helps you scope the hardware while you're already sitting in front of it.

## Tips

- **Create a restore point first** (Phase 4 has the command) before making significant system changes.
- **Don't rearrange their desktop.** Seriously. They know where their icons are.
- **Check the Downloads folder.** It's almost always full of forgotten files eating up disk space.
- **Startup programs** are the number one cause of "my computer is slow." Disable everything that doesn't need to be there.
- **Be patient.** The reason you're here is because someone trusts you with something they don't understand. That's a compliment.

## Contributing

If you've run into other common scenarios while helping non-technical family members, feel free to open a PR and add them to the skill file. Keep the same format: PowerShell-first, explain before executing, flag anything destructive.

## License

MIT — Use it, share it, help your people.
