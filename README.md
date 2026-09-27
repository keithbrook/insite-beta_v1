# INSITE — a local AI workspace where conversations become knowledge

> Your AI conversations, kept as a knowledge map you own — entirely on your machine.

Most of what you work out with an AI simply evaporates. Good decisions, careful reasoning, hard-won context — trapped in a chat log, gone by the next session, re-explained from scratch every time. **INSITE is a desktop app that turns conversations into documents, connects them into a living map, and lets your next conversation draw on the most relevant of what you already know.** Files, map, and chat in one window — talk becomes knowledge, and knowledge becomes the memory of your next talk. No account, no server: everything stays on your Mac.

---

## What makes it different

**1. Everything on your machine, everything just files.**
Every note is plain Markdown (.md). It opens in Finder, edits in any editor, and remains yours if you delete the app. Already keep notes in Obsidian? Import your vault from Settings — a one-time copy that leaves your originals untouched — and those documents become INSITE knowledge too.

**2. It connects to Claude Desktop (MCP).**
Install the bundled connector and Claude can recall your INSITE knowledge like memory — "what did we decide last time?" gets a real answer in a brand-new session. You can bring Claude sessions into INSITE to keep and organize, place an imported session onto a related branch, and resume it later. The connector and the app talk over a local loopback connection.

**3. Saving goes through you.**
In chat, a note is saved when you say yes — the proposal shows where it will be filed. When an answer cites your notes, numbered footnotes link back to them. Conversations you import from Claude become notes automatically; attaching one to an existing branch stays a suggestion until you accept it. The biggest risk of an AI that remembers is remembering wrong; much of this app exists to keep you in that loop.

**4. Documents keep their lineage.**
Rewriting a document through the map keeps the previous version in its lineage — you can compare a version with the one it replaced, and the record keeps what materials the rewrite used. Code has git; your writing keeps its trail too.

**5. Knowledge becomes a map.**
Conversations and documents are drawn as navigable graphs — when a conversation branches, the branches show on the map. You can also drive the map from the chat box with short commands: find a note, cite it, branch from it, move it.

**6. Local AI by default, cloud only by choice.**
If ollama (0.3.4 or later) is already running when INSITE starts, it connects to it automatically; if not, one click in setup installs a dedicated local engine and downloads the chat model you pick. (Setup doesn't install the bge-m3 model for semantic search — type `bge-m3` into the model download box in Settings → LLM.) Cloud use is governed by a five-step dial in Settings → General — from Local only to Cloud only — available once you add a key: saving a key starts cloud at Balanced; set the dial to Local only to stay fully local while keeping your key. (Ollama cloud models, marked ☁, are the exception.)

---

## Who it's for

- **Anyone running a long project** — planning, research, or a startup — tired of watching decisions and context evaporate between AI sessions
- **Anyone who writes with AI** — and wants drafts, revisions, and source material to stay untangled
- **Anyone who wants AI without the cloud residue** — a tool where privacy is the default, not a setting

---

## Install (about 10 minutes)

1. **Requirements**: macOS (Apple Silicon)
2. Download `INSITE_*_aarch64.dmg` from the [latest release](../../releases/latest) → open it and drag INSITE into Applications
3. First launch (unsigned beta): right-click the app → "Open" → "Open". If macOS still blocks it (newer versions), open **System Settings → Privacy & Security** and choose **"Open Anyway"**.
4. Using Claude Desktop? Install `insite-mcp.mcpb` from the same release — **the app and connector ship as a set** (with INSITE running, drag it into Claude Desktop → Settings → Extensions)

**How to use it**: the **INSTALL-GUIDE** attached to the release (a non-developer walkthrough) and the [release notes](../../releases/latest).

---

## Privacy promises

- Conversations, documents, and indexes all live locally. The app sends nothing anywhere on its own — no account, no telemetry upload, no update phone-home.
- If you connect Claude Desktop, what Claude recalls from INSITE becomes part of your Claude conversation — handled by Anthropic like anything else you send to Claude. INSITE itself still transmits nothing.
- Disk encryption is delegated to macOS FileVault — the app deliberately does not encrypt your files, because your files staying plainly *yours* (openable by any tool) is the product's identity.
- The app's local API is locked behind a token, so other programs can't reach it by accident.
- Usage history is numbers and identifiers — which notes were retrieved, response times and processing counts, errors, plus an install id, the app version, the platform, and the name of your local chat model. **Never conversation content.** It stays on your Mac; it leaves only when you review what will be included, consent, and export a file you send yourself.

---

## Beta status — honest disclosure

This is a beta. Known limitations are listed plainly in each release's notes. If you get stuck, that's the most useful data you can give us — export from **Settings → Data → Usage history** and send us the file, or just tell us. 🙏
