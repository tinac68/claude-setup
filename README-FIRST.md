# Starter kit: the four parts

From marianasmall/claude-code-starter-kit (checked out at commit c46365e). Nothing here includes the hooks, settings, or plugin packaging.

## What's in the folder

| Folder or file | What it is | Where it goes on your computer |
|---|---|---|
| CLAUDE.md.template | Your standing instructions for Claude (53 lines) | Copy to `~/.claude/CLAUDE.md`, then fill in the bracketed prompts |
| skills/ (6 folders) | Reusable procedures: bring-up-to-speed, humanizer, idea-to-scope, kaizen, learning-capture, meeting-recap | Copy each folder to `~/.claude/skills/` |
| commands/ (15 files) | Slash commands | Copy to `~/.claude/commands/`. In the plugin they are named `/kit:name`; copied by hand they are just `/name` |
| automation-recipes/ (17 guides + README) | Read-only step-by-step guides. Nothing to install | Keep as reference documents |

## Read before copying the commands

Most commands only write notes to `~/.claude/` (for example `note.md`, `debt.md`, `session-end.md`). Three need a closer look:

- **maintain.md:** runs `brew upgrade` and `npm` updates when you approve them, reads your Claude config (`~/.claude.json`, `settings.json`), scans for leaked secrets, and checks OAuth token files. Skip it unless you want that.
- **scaffold-project.md:** can offer `git rm --cached` on a private folder. That stops tracking the files but leaves them in git history.
- **permissions-audit.md:** reads and suggests changes to your permission rules. Review every suggestion before accepting.

## Changes to make for your work

- CLAUDE.md.template: replace `[YOUR_NAME]` and the bracketed prompts. The "Ask first" rule is good for a practice where mistakes are costly. Keep the "legal or evidence files" exclusion from the rename rule.
- humanizer: its rules (no em dashes, straight quotes, no boldface headers) match your writing preferences, so keep it on for drafts.
- Recipes 15 and 17 touch your inbox and money tracker. Run them on a copy of the data first.

## Install check

Start a new Claude Code session and run `/context`. `~/.claude/CLAUDE.md` should appear under Memory files.
