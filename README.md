# MicroBenchmark

**Find out which AI model is actually best at *your* work.**

Public leaderboards measure models on someone else's tasks. MicroBenchmark
builds benchmarks from the work you've already done with Claude Code and Codex.
It finds the tasks you really cared about: the files you kept revising and the
answers you kept correcting. It turns them into tests that reflect your own
standards, then shows you how different models and agents do on them in a
blind comparison.

**[⬇️ Download the latest release](https://github.com/AISmithLab/MicroBenchmark-Releases/releases/latest)**

---

## How it works

### 1. Discover the work worth measuring
MicroBenchmark scans your local Claude Code and Codex history and picks out
the deliverables you went back to again and again, like a doc you revised five
times or a plan you kept reshaping. These are the tasks where your taste shows.
You choose a date range and the app lists the opportunities it found.

### 2. Build a benchmark in one click
Pick an opportunity, or just describe what success looks like in your own
words. MicroBenchmark drafts a task and a scoring rubric based on your
preferences, saves the benchmark, and shows you a preview of how it grades a
real answer.

### 3. Compare models, blind
Choose two or more models or local agents and run them on the same task with
the same prompt. You score each answer 1–5 against the rubric without knowing
which model wrote it. Names are revealed only after you've confirmed every
score, so the ranking reflects the quality of the work and not the brand.

---

## Download

| Platform | File |
| --- | --- |
| **macOS** (Apple Silicon) | `MicroBenchmark_<version>_aarch64.dmg` |
| **Windows** (64-bit) | `MicroBenchmark_<version>_x64-setup.exe` |

Get both from the **[Releases page](https://github.com/AISmithLab/MicroBenchmark-Releases/releases/latest)**.
You can ignore the other files there (`.tar.gz`, `.sig`, `latest.json`). The
app uses them to update itself.

### Installing on macOS
1. Open the `.dmg` and drag **MicroBenchmark** into **Applications**.
2. Launch it. The app is signed and notarized by Apple, so it opens without
   any security warning.

> Intel Macs aren't supported yet.

### Installing on Windows
1. Run the `-setup.exe` installer.
2. The installer isn't code-signed yet, so Windows SmartScreen may warn you.
   Click **More info → Run anyway** to continue.

### First launch
On first launch the app takes a moment to set itself up. There's nothing to
install separately: no Python, no Terminal, and no config files.

---

## Connecting a model provider

MicroBenchmark needs access to one AI model to analyze your history and draft
benchmarks. **Any one of these is enough:**

- **Claude Code** (if it's installed, the app uses your existing subscription)
- **Codex CLI** (uses your existing ChatGPT/Codex subscription)
- An **Anthropic**, **OpenAI**, or **Gemini** API key

Open **Settings** in the app to add API keys and choose which provider to try
first. The app shows which providers it has detected. Installed CLIs come
first by default because they don't cost anything beyond a subscription you
already pay for.

---

## Privacy

Your history stays on your machine unless you choose to send it.

- **Scanning is local.** Finding candidate tasks happens entirely on your
  computer, with no network requests and no model calls.
- **You approve before anything is sent.** Before analysis, the app tells you
  exactly what will go to your chosen provider: only the visible conversation
  text for the work you selected.
- **Hidden content is never sent.** Tool calls, tool outputs, hidden reasoning,
  system messages, and subagent activity are excluded.
- **Raw session files are never copied.** Your Claude Code and Codex logs stay
  where they are.
- **Agents run in isolation.** Local agents being evaluated run in a temporary
  folder, and only their final answer is kept.

---

## Updates

MicroBenchmark checks for new versions when it starts and asks before
installing an update. After the first install you don't need to come back here
to download new versions.

---

## Current limitations

- Runs on one computer for one user. There's no cloud sync or sharing yet.
- Each benchmark has one task, and each model answers it once per run.
- Supports macOS on Apple Silicon and 64-bit Windows. Intel Macs and Linux
  aren't supported yet.

---

<sub>This repository only hosts MicroBenchmark's installers and update files.
The app's source code is kept private.</sub>
