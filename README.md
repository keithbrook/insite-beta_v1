# INSITE — a local AI workspace where conversations become knowledge

> Your AI conversations, sedimented into a knowledge map you own — entirely on your machine.

Most of what you work out with an AI simply evaporates. Good decisions, careful reasoning, hard-won context — trapped in a chat log, gone by the next session, re-explained from scratch every time. **INSITE is a desktop app that turns conversations into documents, connects those documents into a living map, and lets your next conversation start on top of everything you already know.** Knowledge map on the left, chat on the right — talk becomes knowledge, and knowledge becomes the memory of your next talk.

---

## What makes it different

**1. Everything on your machine, everything just files.**
Every note is plain Markdown (.md). It opens in Finder, edits in Obsidian, and remains yours if you delete the app. No account, no server — the app sends nothing anywhere.

**2. Designed not to make things up.**
Answers cite your notes by coordinate, and when there's no evidence, it **says so**. The AI never saves anything on its own (saving always goes through your confirmation), unconfirmed suggestions carry an explicit `[unconfirmed]` label, and everything saved records its provenance — your decision, or the AI's suggestion. The biggest risk of an AI that remembers is remembering wrong; half of this app exists to prevent exactly that.

**3. Your documents have versions and lineage.**
Rewriting a document never destroys the previous version — it stays in the lineage. You can diff any two versions, and the record shows what materials the rewrite used and who wrote it (you or the AI). Code has git. Now your writing has this.

**4. Knowledge becomes a map.**
Documents, conversations, and folders are drawn as a navigable graph. When a conversation branches, the branches show on the map; superseded versions hang off dotted lineage edges. You navigate the structure of your own thinking — that's the difference between this and a search box.

**5. It connects to Claude Desktop.**
Install the bundled MCP connector and Claude can recall your INSITE knowledge like memory. "What did we decide last time?" gets a real answer in a brand-new session.

**6. Local AI by default, cloud only by choice.**
If you have ollama installed, INSITE connects to it automatically; if not, the app provisions a managed local engine. Cloud models run only when you explicitly enable them — and the fallback is always local.

---

## Who it's for

- **Anyone running a long project** — planning, research, or a startup — tired of watching decisions and context evaporate between AI sessions
- **Anyone who writes with AI** — and wants drafts, revisions, and source material to stay untangled, with the system knowing which version is current
- **Anyone who wants AI without the cloud residue** — a tool where privacy is the default, not a setting

---

## Install (about 10 minutes)

1. **Requirements**: macOS (Apple Silicon)
2. Download `INSITE_0.1.7_aarch64.dmg` from the [latest release](../../releases/latest)
3. Follow the bundled **[INSTALL-GUIDE-v0.1.7.md](../../releases/latest)** — this is an unsigned beta, so first launch is right-click → Open
4. Using Claude Desktop? Install `insite-mcp.mcpb` as well — **the app and adapter ship as a set**

## Privacy promises

- Conversations, documents, and indexes all live locally. Disk encryption is delegated to macOS FileVault — the app deliberately does not encrypt your files, because your files staying plainly *yours* (openable by any tool) is the product's identity.
- Even problem reports contain only numbers and settings — zero conversation or document content. The app never sends them; you save a plain-text file, read it yourself, and decide.

## Beta status — honest disclosure

This is a beta. Known limitations and open verification items are listed plainly in each release's notes. If you get stuck, that's the most useful data you can give us: **Settings → Info → Create problem report → Save to file** → send us the file.
