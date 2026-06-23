# INSITE Beta — Tester Guide · v0.1.0

> Private macOS (Apple Silicon) beta · a turnkey desktop app. Download it and you're ready to go.

## 1. Install (Apple Silicon Mac)

1. **Download**: https://github.com/keithbrook/insite-beta_v1/releases/latest → `INSITE_0.1.0_aarch64.dmg`.
2. **Install**: open the .dmg → **drag INSITE into your Applications folder**.
3. **First launch (unsigned app)**: double-clicking is blocked → **right-click the app → "Open" → "Open"** again (just once; after that, double-click works normally).
   - If you see *"INSITE is damaged and can't be opened"* (macOS quarantines downloads), run this one line in **Terminal**, then right-click → Open:
     `xattr -dr com.apple.quarantine /Applications/INSITE.app`
4. **Documents permission**: on first open, macOS asks to allow access to your Documents folder → **Allow** (your notes are stored there).
   - If it doesn't ask and the **left-hand vault looks empty**, go to System Settings → Privacy & Security → **Files and Folders** (or Full Disk Access), enable **INSITE**'s Documents access, and restart the app.

## 2. Set up an LLM — pick one (required)

INSITE needs an LLM to generate answers. Just do whichever is easier.

- **Local (free · private · recommended · nothing else to install)**
  An LLM engine (Ollama) is **built in**. Go to Settings (⚙) → LLM → **Download a model** and you're set.
  Recommended: **Qwen2.5 7B** (light and fast) or **Qwen2.5 14B** (balanced · default). The first download is a few GB, so it takes a while (one time only).
  *Smaller models can be weaker at quality and instruction-following — 14B+ or a cloud model is recommended.*

- **Cloud (fast · high quality · your own key)**
  Settings → LLM → choose Anthropic or OpenAI → **enter your own API key**.
  Keys are stored only on this machine (`~/.insite`) and never leave the app.

## 3. What to try — the core flow

1. **Chat → Brief**: ask a question in the chat on the right → get an answer (with citations [1][2]) → the key points accumulate as *briefs* (documents).
2. **Create a note**: top of the left explorer → **+ Note** → it opens immediately as `untitled`. **The top line is the title (which becomes the filename)**; below it is the body. Edit the title and press **Enter** (or click elsewhere) to apply it.
3. **Brief map** (top-left `brief`): a network map of briefs and folders. Click a node → a panel (open doc / cite / continue context).
4. **Context map** (top-left `context`): a map of your conversation branches.
   - **Brief-centric** (default): an overview showing *only* briefs.
   - **All turns**: the detailed view expanded to every turn — toggle to see the difference.
   - Click a brief node → continue / fork / new context / cite · you may also see 💡 suggestions.
5. **Select & branch**: click a node (single select) · `Shift`+click or `Shift`+drag (multi-select) · fork / merge.
6. **Settings**: LLM provider · model · apply intensity, rules, import/export.

## 4. Known limitations (it's a beta — thanks for bearing with it)

- macOS (Apple Silicon) only · unsigned (see step 1).
- Needs an LLM to work (step 2). Without one, you won't get answers.
- Small local models can be weaker and may attach citations incorrectly — 14B+/cloud recommended.
- The first answer, or a large model, can be slow.
- Where data lives: briefs = `~/Documents/INSITE` · conversations & settings = `~/.insite` · models = `~/.ollama`.
- An in-progress branch (no brief made yet) shows as a *thin dot (stub)* on the brief-centric map (intended behavior).
- New notes may show up as several `untitled` entries (auto-numbering arrives in the next version) — just rename them.

## 5. Feedback

- Jot down anything **odd, confusing, or slow** and send it to **Hoon** — screenshots are even better.
- Especially curious about: anything that blocked install / first launch, your LLM setup experience, and anything confusing in the editor or the maps.

---
*INSITE v0.1.0 beta · Apple Silicon macOS · unsigned build.*
