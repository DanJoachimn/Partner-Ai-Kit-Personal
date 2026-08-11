# Obsidian Vault — Simplified Second Brain

*The simplest vault that still feels like a second brain. Zero Hybrid Rule complexity. Zero Agent Brain. Just folders their AI can read and write, and a daily journal they can ignore or love.*

---

## What this gets them

A single place where everything about their business lives:

- Project briefs (client onboarding, spring launch, newsletter relaunch, podcast season 2)
- Meeting notes
- Daily journal (if they want one)
- Brand canon (voice guide, reference brands, do-not-use list)
- Random notes and clippings

Their AI can search the whole vault, pull up context from old meetings or past decisions, and write updates directly to it. That's the second-brain unlock — the AI doesn't forget between sessions, because everything it might need to remember lives in files it can read.

**Why this is worth doing for a time-squeezed founder:** every time they tell their AI "I decided X two weeks ago" and the AI says "remind me?" — that's a minute lost. A vault kills that tax.

---

## Install steps

### 1. Download Obsidian

Free from **obsidian.md**. Drag to Applications.

### 2. Open the vault setup.sh already built

The vault already exists at `~/[ai-name]/vault/` — setup.sh created it. Don't create a new one.

Open Obsidian → **"Open folder as vault"** → point it at `~/[ai-name]/vault`.

> ⚠️ **Never save the vault into `~/Documents/` or `~/Desktop/`.** Both are TCC-protected by macOS, which silently blocks the AI's background routines (2 AM memory compression, the Telegram poller) from reading anything inside them. The home folder is the safe spot, and that's why setup.sh puts it there. This isn't a preference — install #1 lost a week to it.

### 3. Copy the scaffold folders

From this `vault/` folder, copy the starter structure into their new vault:

```bash
# Adjust VAULT_PATH to wherever Obsidian created their vault
VAULT_PATH="$HOME/[ai-name]/vault"

cp -R "starter/"* "${VAULT_PATH}/"
```

They'll now have:

```
[BRAND]/
├── CLAUDE.md                    <- vault rules for their AI
├── Projects/
│   ├── [BRAND] — spring launch.md
│   ├── [BRAND] — client onboarding.md
│   ├── [BRAND] — newsletter relaunch.md
│   └── Podcast — season planning.md
├── Brand/
│   ├── Voice guide.md
│   ├── Reference brands.md
│   └── Do-not-use list.md
├── Daily/
│   └── (empty — daily notes go here)
├── Notes/
│   └── (empty — catch-all)
├── Meetings/
│   └── (empty — meeting notes go here)
└── Archive/
    └── (empty — old stuff)
```

### 4. Tell their AI about the vault

Add to their `~/[ai-name]/CLAUDE.md`, under "How we remember things":

```markdown
## The vault (second brain)

[PARTNER_NAME]'s vault lives at `~/[ai-name]/vault/` (created by setup.sh — deliberately OUTSIDE ~/Documents/, because macOS's privacy lock on Documents blocks the AI's background routines from reading it). It contains:
- Projects/ — one file per active [BRAND] project
- Brand/ — brand voice guide, reference brands, do-not-use list (READ THIS BEFORE DRAFTING)
- Daily/ — their daily journal (read-only for you unless they ask)
- Meetings/ — meeting notes
- Notes/ — their thinking-out-loud

On startup, you don't need to read the whole vault. When they ask about a project,
`Read` the relevant project file first. When drafting [BRAND] content, ALWAYS
`Read Brand/Voice guide.md` and `Brand/Do-not-use list.md` before writing.

You can append to Projects/ and Notes/ with their approval. Daily/ is their space —
don't write there unless they explicitly ask.
```

### 5. Turn on Obsidian's built-in plugins they'll actually use

In Obsidian → Settings → Core plugins, enable:

- **Daily notes** — so a new `Daily/2026-05-01.md` is one click away.
- **Backlinks** — shows which files mention the current file. Magic.
- **File recovery** — autosave. Saves them from themselves.

Keep the other core plugins off for now — out of the box Obsidian has ~30 and they only need these three to start.

**One community plugin worth adding later (Part 2):** **Smart Connections** — it builds a private, on-device "meaning fingerprint" of every note, which powers the `vault-semantic-search` skill (find notes by meaning, not just exact words). Optional, installed during Part 2's "Semantic search" stage — not now. If they opt in, that's the one community plugin the kit uses. Everything else stays off.

### 6. Open the vault in Obsidian (optional but recommended)

The vault already lives inside the AI's folder at `~/[ai-name]/vault/` — setup.sh put it there. No symlink, no moving anything. To browse it visually:

Open Obsidian → "Open folder as vault" → pick `~/[ai-name]/vault`.

**Do NOT move the vault into `~/Documents/`** (even though that feels like the natural home for documents). macOS puts a privacy lock (TCC) on Documents that silently blocks the AI's background routines — the 2 AM memory compression, the Telegram poller — from reading anything inside it. The vault stays in the home folder on purpose; backup happens via Time Machine + private GitHub instead of iCloud.

---

## The one rule they need to follow

**Don't nest folders more than two levels deep.** Obsidian handles deep nesting badly, and retrieval gets slow. If they find themselves making `Projects/[BRAND]/Campaigns/Spring launch/Research/`, stop. Flatten it.

Everything else about Obsidian is discoverable. They'll learn by using it.

---

## What this vault is NOT

- **Not a productivity system.** Obsidian is a file browser with a pretty UI. It doesn't "do" anything by itself.
- **Not a project manager.** Use Notion or Trello or paper for that. The vault is for knowledge, not tasks.
- **Not the Hab.** A power-user vault might have 40+ folders, an `_Brain/` system, a reflection firewall, and a Hybrid Rule. [PARTNER_NAME] does not need any of that. This scaffold is deliberately 6 folders. If they outgrow it, they outgrow it — but most people never do.

---

## When they hit a wall

- **"I can't find anything."** → Teach them Obsidian's global search (`Cmd+Shift+F`). It searches across every file instantly.
- **"It's getting messy."** → Archive aggressively. Move old project files to `Archive/`. Don't delete.
- **"I don't know where to put this."** → `Notes/`. Always `Notes/`. They can sort later.
