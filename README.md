# INSITE Beta — Tester Guide · v0.1.1

> Private macOS (Apple Silicon) beta · a turnkey desktop app. Download it, open it, and a short setup wizard gets you going.

## 1. Install (Apple Silicon Mac)

1. **Download**: https://github.com/keithbrook/insite-beta_v1/releases/latest → `INSITE_0.1.1_aarch64.dmg`.
2. **Install**: open the .dmg → **drag INSITE into your Applications folder**.
3. **First launch (unsigned app)**: double-clicking shows *"Apple could not verify…"* → **right-click the app → "Open" → "Open"** (just once; after that, double-click works normally). **No Terminal needed.**
   - *(Rare fallback)* if you ever see *"INSITE is damaged"*, run this one line in Terminal, then right-click → Open:
     `xattr -dr com.apple.quarantine /Applications/INSITE.app`

## 2. First-run setup (wizard)

On first launch a short **setup wizard** walks you through two things:

1. **LLM** — pick one:
   - **Local (free · private · recommended)**: choose a model and click download. The local engine (Ollama, ~150 MB) is fetched **automatically** the first time, then the model itself (a few GB for a good one — Qwen2.5 14B recommended; smaller models are weaker). Nothing to install separately.
   - **Cloud (fast · your own key)**: choose Anthropic or OpenAI and paste your API key. Keys stay on your machine (`~/.insite`) and never leave the app. *(With cloud, no engine/model download.)*
2. **Notes folder** — where your notes live. The default (`~/INSITE`) works out of the box with **no permission prompts**. You can pick any folder; if you choose Documents/Desktop/Downloads, macOS asks for permission once.

You can change any of this later in Settings (⚙).

## 3. What to try — the core flow

1. **Chat → Brief**: ask a question in the chat on the right → get an answer (with citations [1][2]) → the key points accumulate as *briefs* (documents).
2. **Create a note**: top of the left explorer → **+ Note** → opens as `untitled`, the title selected so you can type a name right away. **The top line is the title (= the filename)**; below it is the body. Edit the title and press **Enter** (or click the body) to apply it.
3. **Brief map** (top-left `brief`): a network map of briefs and folders. Click a node → a panel (open doc / cite / continue context).
4. **Context map** (top-left `context`): a map of your conversation branches.
   - **Brief-centric** (default): an overview showing *only* briefs.
   - **All turns**: the detailed view expanded to every turn — toggle to see the difference.
   - Click a brief node → continue / fork / new context / cite · you may also see 💡 suggestions.
5. **Select & branch**: click a node (single select) · `Shift`+click or `Shift`+drag (multi-select) · fork / merge.
6. **Settings**: LLM provider · model · apply intensity, rules, import/export, notes location.

## 4. Known limitations (it's a beta — thanks for bearing with it)

- macOS (Apple Silicon) only · unsigned (right-click → Open on first launch, see step 1).
- Needs an LLM to work (step 2). Without one, you won't get answers.
- Small local models are weaker and may attach citations incorrectly — 14B+/cloud recommended.
- The first answer, or a large model, can be slow. The first local model download (engine + model) is a one-time several-GB fetch.
- Where data lives: notes = the folder you picked (default `~/INSITE`) · conversations & settings = `~/.insite` · models = `~/.ollama`.
- An in-progress branch (no brief made yet) shows as a *thin dot (stub)* on the brief-centric map (intended behavior).

## 5. Feedback

- Jot down anything **odd, confusing, or slow** and send it to **Hoon** — screenshots are even better.
- Especially curious about: install / first launch / the setup wizard, your LLM experience, and anything confusing in the editor or the maps.

---
*INSITE v0.1.1 beta · Apple Silicon macOS · unsigned build.*
