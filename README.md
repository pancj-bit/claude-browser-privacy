# Claude Browser Privacy

A Codex skill for reviewing local Claude sign-ins, setting up a dedicated Chrome profile without a Google account, and checking what that profile exposes to websites. It includes desktop instructions for macOS, Windows 11, and Linux.

## Install

Ask Codex to install the skill from its GitHub folder.

```text
Use $skill-installer to install https://github.com/pancj-bit/claude-browser-privacy/tree/main/skills/claude-browser-privacy
```

## Use

For the full setup, ask Codex to run the skill on the desktop where you use Chrome.

```text
Use $claude-browser-privacy to review my local Claude data, set up Chrome, and run the CleanIP check.
```

You can also request one step, such as checking whether the current Chrome profile uses Cloudflare Secure DNS. When a request includes deleting data, the skill identifies the affected accounts and profiles and asks before removal. [Read the skill](skills/claude-browser-privacy/SKILL.md)
