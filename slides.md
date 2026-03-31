---
theme: none
title: Rattler Workshop
info: |
  Building a package manager in Rust with the rattler library.
  A hands-on workshop for the conda team.
class: text-center
transition: fade
drawings:
  persist: false
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,400&family=IBM+Plex+Mono:wght@400;500&display=swap');

  :root {
    --tufte-bg: #fcf8f0;
    --tufte-fg: #111;
    --tufte-muted: #666;
    --tufte-accent: #a00000;
    --tufte-link: #a00000;
    --tufte-border: #e0d8c8;
  }

  html, body, #app, #slide-content {
    background: var(--tufte-bg) !important;
  }

  .slidev-layout {
    background: var(--tufte-bg) !important;
    color: var(--tufte-fg) !important;
    font-family: 'Crimson Pro', 'Georgia', serif !important;
    padding: 3rem 4.5rem !important;
  }

  h1, h2, h3 {
    font-family: 'Crimson Pro', 'Georgia', serif !important;
    font-weight: 400 !important;
    color: var(--tufte-fg) !important;
    letter-spacing: -0.01em;
  }

  h1 { font-size: 2.6rem !important; line-height: 1.15 !important; }
  h2 { font-size: 1.8rem !important; line-height: 1.25 !important; }

  p, li {
    font-size: 1.15rem !important;
    line-height: 1.65 !important;
    color: var(--tufte-fg);
  }

  ul {
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
    list-style: disc !important;
    padding-left: 1.5em !important;
  }

  ul ul {
    list-style: circle !important;
    margin-top: 0.2rem;
    margin-bottom: 0.2rem;
  }

  li {
    margin-bottom: 0.15rem;
  }

  code {
    font-family: 'IBM Plex Mono', monospace !important;
    font-size: 0.85em !important;
    background: #f0ece2 !important;
    padding: 0.1em 0.35em !important;
    border-radius: 2px !important;
    color: var(--tufte-fg) !important;
  }

  pre {
    background: #f0ece2 !important;
    border-radius: 4px !important;
    padding: 0.8rem 1rem !important;
    margin: 0.6rem 0 !important;
    line-height: 1.5 !important;
  }

  pre code {
    background: none !important;
    padding: 0 !important;
    font-size: 0.82rem !important;
    line-height: 1.5 !important;
  }

  .slidev-code-wrapper, .shiki {
    background: #f0ece2 !important;
    border-radius: 4px !important;
  }

  .shiki code {
    font-family: 'IBM Plex Mono', monospace !important;
    font-size: 0.82rem !important;
    line-height: 1.5 !important;
  }

  a { color: var(--tufte-link) !important; text-decoration: none !important; }
  a:hover { text-decoration: underline !important; }

  .newthought {
    font-variant: small-caps;
    font-size: 1.15em;
    letter-spacing: 0.05em;
  }

  .muted { color: var(--tufte-muted); }
  .accent { color: var(--tufte-accent); }

  .logo-row {
    display: flex;
    align-items: center;
    gap: 2rem;
    justify-content: center;
  }

  .logo-row img { height: 40px; }

  .schedule-grid {
    display: grid;
    grid-template-columns: 5.5rem 1fr;
    gap: 0.5rem 1.5rem;
    font-size: 1.1rem;
    line-height: 1.6;
  }

  .schedule-grid .time {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.9rem;
    color: var(--tufte-muted);
    text-align: right;
    padding-top: 0.1em;
  }

  .chapter-list {
    columns: 2;
    column-gap: 3rem;
    list-style: none;
    padding: 0;
  }

  .chapter-list li {
    font-size: 1rem !important;
    line-height: 1.8 !important;
    break-inside: avoid;
  }

  .chapter-list li .ch {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.8rem;
    color: var(--tufte-muted);
    margin-right: 0.4rem;
  }

  .exercise-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.95rem;
  }

  .exercise-table th {
    font-variant: small-caps;
    font-weight: 400;
    letter-spacing: 0.05em;
    text-align: left;
    border-bottom: 2px solid var(--tufte-fg);
    padding: 0.4rem 0.6rem;
  }

  .exercise-table td {
    padding: 0.35rem 0.6rem;
    border-bottom: 1px solid var(--tufte-border);
    font-size: 0.9rem !important;
    line-height: 1.5 !important;
  }

  .exercise-table tr:last-child td { border-bottom: none; }

  .tutor-box {
    background: #f3efe5;
    border-left: 3px solid var(--tufte-accent);
    padding: 1rem 1.5rem;
    margin: 1rem 0;
    font-size: 1rem;
  }
</style>

<!-- Slide 1: Cover -->

<div class="flex flex-col items-center justify-center h-full gap-6">
  <img src="/paxton-moon.png" class="h-72" style="border:none;box-shadow:none;" alt="The Rattler Book" />
  <div class="text-center">
    <h1 style="margin:0;">The Rattler Workshop</h1>
    <p class="muted" style="font-size:1.25rem!important; margin-top:0.5rem;">
      Building a package manager in Rust
    </p>
  </div>
  <div class="logo-row" style="margin-top:1rem;">
    <img src="/anaconda_logo.png" alt="Anaconda" />
    <span class="muted" style="font-size:1.5rem;">×</span>
    <img src="/prefix_logo.svg" alt="prefix.dev" />
  </div>
  <p class="muted" style="font-size:0.95rem!important;">March 31 – April 1, 2026 · 15:30 – 17:50</p>
</div>

---

<!-- Slide 2: Who am I -->

# <span class="newthought">Who am I</span>

**Tim de Jager**

<div class="mt-4">

- Main contributor to [pixi](https://github.com/prefix-dev/pixi) and [rattler](https://github.com/conda/rattler)
- Previously worked in robotics and gaming
- Now at [prefix.dev](https://prefix.dev/), building developer tooling on top of the conda ecosystem
- Wrote the Rattler Book with the help of Claude Opus
  - All text was heavily edited over many iterations
  - The introduction was written entirely by hand

</div>

<div class="flex items-center gap-4 mt-8">
  <img src="/prefix_logo.svg" style="height:48px;" />
</div>

---

<!-- Slide 3: Schedule overview -->

# <span class="newthought">Schedule</span>

Two afternoons, 2 hours 20 minutes each.

<div class="flex gap-16 mt-8">
<div class="flex-1">

### Day 1 · <span class="muted">Today</span>

<div class="schedule-grid mt-4">
  <span class="time">15:30</span> <span>This intro + setup</span>
  <span class="time">15:50</span> <span>Pick a chapter, start exercises</span>
  <span class="time">~17:00</span> <span>Check-in / questions</span>
  <span class="time">17:50</span> <span>Wrap up</span>
</div>

</div>
<div class="flex-1">

### Day 2 · <span class="muted">Tomorrow</span>

<div class="schedule-grid mt-4">
  <span class="time">15:30</span> <span>Continue exercises <em>or</em></span>
  <span class="time"></span> <span>switch to rattler PRs</span>
  <span class="time">~17:00</span> <span>Check-in / questions</span>
  <span class="time">17:50</span> <span>Wrap up + retro</span>
</div>

<p class="muted mt-6" style="font-size:0.95rem!important;">
Day 2 PR backlog: <a href="https://docs.google.com/document/d/1x-7l9eOZJhjv3SMVKcVGMXj8NkEvgK_jzNR_Ua6YD-c/edit?usp=sharing">rattler PR planning doc</a>
</p>

</div>
</div>

---

<!-- Slide 4: Why this book? -->

# <span class="newthought">Why this book?</span>

Conda can serve as a foundation for package managers **beyond Python**.

<div class="flex gap-10 mt-6">
<div class="flex-1">

**What the conda ecosystem offers:**

- Thousands of prebuilt binary packages in conda-forge
- Isolated environments (basically a linux-prefix)
- A language-agnostic package format
- Mature infrastructure, now available in Rust through Rattler

</div>
<div class="flex-1">

**Why Lua as the example?**

- Lightweight and self-contained
- The techniques apply to any language
- You will build **moonshot**, a complete Lua package manager

```
$ shot add lumen
$ shot install
  Solved 12 packages in 0.3s
$ shot run lua -e "require('lumen')"
```

</div>
</div>

---

<!-- Slide 4: What you will build -->

# <span class="newthought">What you will build</span>

The book implements **moonshot** command by command:

<ul class="chapter-list mt-4">
  <li><span class="ch">03</span> <code>init</code> · scaffold a project manifest</li>
  <li><span class="ch">04</span> <code>search</code> · query conda channels</li>
  <li><span class="ch">05</span> <code>add</code> · add packages to the manifest</li>
  <li><span class="ch">06</span> <code>lock</code> · solve dependencies</li>
  <li><span class="ch">07</span> <code>install</code> · download and link packages</li>
  <li><span class="ch">08</span> <code>shell-hook</code> · activate environments</li>
  <li><span class="ch">09</span> <code>run</code> · run commands in env</li>
  <li><span class="ch">10</span> <code>build</code> · build conda packages</li>
</ul>

<Sparkline />

---

<!-- Slide 5: The exercises -->

# <span class="newthought">Exercises</span>

Each chapter (3 through 10) has **3 exercises** graded by difficulty. 24 exercises total.

<table class="exercise-table mt-6">
  <tr>
    <th>difficulty</th>
    <th>example</th>
    <th>typical scope</th>
  </tr>
  <tr>
    <td style="color:var(--tufte-accent)">Easy</td>
    <td>Add a <code>requires-lua</code> field</td>
    <td>Add a field, parse it, wire a CLI flag</td>
  </tr>
  <tr>
    <td style="color:var(--tufte-accent)">Intermediate</td>
    <td>Lock file diff</td>
    <td>Combine existing APIs in a new way</td>
  </tr>
  <tr>
    <td style="color:var(--tufte-accent)">Hard</td>
    <td>Stacked environment activation</td>
    <td>Design decisions, multiple subsystems</td>
  </tr>
</table>

<div class="mt-6">

- Pick what interests you
- Every exercise has acceptance criteria so you know when you're done
- Start easy if you're new to the codebase

</div>

---

<!-- Slide 6: Interest areas -->

# <span class="newthought">Pick your interest</span>

Not every chapter appeals to everyone. Here is a rough map of what covers what.

<div class="flex gap-10 mt-4">
<div class="flex-1">

**CLI and manifest work** (ch 3, 5)

- Parsing TOML with Serde
- MatchSpec validation
- Wiring clap CLI flags

**Repodata and networking** (ch 4, 5)

- Querying channels through the Gateway
- Platform-specific packages
- Version comparison

</div>
<div class="flex-1">

**Solving and locking** (ch 6)

- The Resolvo SAT solver
- Virtual package overrides
- Lock file diffing

**Installation and environments** (ch 7, 8, 9)

- Prefix records, hard-linking
- Shell activation scripts
- Running commands inside environments

**Building packages** (ch 10)

- The `.conda` archive format
- Build scripts, metadata, variants

</div>
</div>

---

<!-- Slide 7: A literate program -->

# <span class="newthought">A literate program</span>

The book is written as a **literate program**. All source code lives inside the Markdown chapters; the Rust files are generated from the book, not the other way around.

<div class="flex gap-10 mt-6">
<div class="flex-1">

**How it works:**

- Code blocks in the book carry a `file=` attribute
- Named blocks can reference each other with `<<block-name>>`
- `pixi run tangle` generates `.rs` files from the book
- `pixi run stitch` pushes source edits back into the book

</div>
<div class="flex-1">

**Why this matters for you:**

- The prose explains *why* the code is written the way it is
- You can read code in the order it makes sense, not in file order
- The source files contain `// ~/~` markers from Entangled; ignore them
- For exercises, edit the `.rs` files directly (not the Markdown)

</div>
</div>

---

<!-- Slide 8: Using the book — navbar -->

# <span class="newthought">Using the book</span>

[prefix-dev.github.io/rattler-book](https://prefix-dev.github.io/rattler-book/). The header has a few buttons worth knowing about.

<div class="mt-4">
  <NavbarAnnotated />
</div>

<div class="flex gap-10 mt-4">
<div class="flex-1">

- **Focus mode** hides the left navigation for distraction-free reading
- Your preference is saved in the browser

</div>
<div class="flex-1">

- **Source viewer** opens a drawer with a file tree and a syntax-highlighted code editor
- Click any filename in a chapter to jump to that file

</div>
</div>

---

<!-- Slide 8b: Using the book — source viewer -->

# <span class="newthought">The source viewer</span>

<div class="flex gap-8 mt-4 items-start">
<div style="flex:1.4;">
  <img src="/book-source-viewer.png" style="width:100%;border:1px solid #e0d8c8;border-radius:4px;" alt="Source viewer" />
</div>
<div style="flex:1;">

- File tree on the left, code on the right
- Syntax-highlighted with CodeMirror
- Supports Rust, Lua, and TOML
- `»` markers show literate block boundaries
- Click any `file=` reference in a chapter to open the matching file and scroll to the right block

</div>
</div>

---

<!-- Slide 9: Your AI Tutor -->

# <span class="newthought">Your AI tutor</span>

The book ships with a **Socratic AI tutor** that guides you through exercises without giving you the answer.

<div class="mt-4">

**What the tutor does:**

- Asks what you've tried before offering help
- Gives leading questions instead of solutions
- Points to relevant code in the repo
- Helps you read compiler errors step by step
- Checks acceptance criteria when you're done
- **Will not** write solution code. Ever.

</div>

<div class="mt-4">

**Adapts to your Rust level:**

- **Beginner**: explains ownership, Serde, Result/Option, compiler errors
- **Intermediate**: focuses on Rattler APIs and the moonshot codebase
- **Advanced**: points to the right files, gets out of the way

</div>

---

<!-- Slide 7: AI Tutor Setup -->

# <span class="newthought">Setting up the tutor</span>

The tutor prompt lives in `TUTOR.md` at the book repo root.

<div class="mt-6">

**Claude Code** (recommended)

```bash
claude --append-system-prompt-file TUTOR.md
```

**Cursor**

- Create `.cursor/rules/tutor.mdc`
- Paste the contents of `TUTOR.md`

**GitHub Copilot**

- Copy `TUTOR.md` to `.github/copilot-instructions.md`

**Any other agent**

- Use `TUTOR.md` as the system prompt

</div>

---

<!-- Slide 9: Getting started -->

# <span class="newthought">Getting started</span>

<div class="flex gap-10 mt-6">
<div class="flex-1">

**1. Clone the book**

```bash
git clone https://github.com/tdejager/rattler-book
cd rattler-book
```

**2. Install dependencies**

```bash
pixi install
pixi run build  # verify it compiles
```

**3. Start the tutor**

```bash
claude --append-system-prompt-file TUTOR.md
```

</div>
<div class="flex-1">

**4. Pick an exercise**

Start with chapter 3 if you're new to the codebase. Tell the tutor:

<div class="tutor-box" style="font-size:0.95rem;">
  "I'd like to work on exercise 3.1"
</div>

**5. Build often**

```bash
pixi run build
pixi run shot init my-app
```

The Rust compiler is your best teacher.

</div>
</div>

---
layout: center
---

<div class="flex flex-col items-center justify-center gap-8">
  <h1 style="font-size:3rem!important;">Let's get started.</h1>
  <p class="muted" style="font-size:1.2rem!important;">
    Pick a chapter. Set up the tutor. Ask questions anytime.
  </p>
  <div class="logo-row" style="margin-top:2rem;">
    <img src="/anaconda_logo.png" alt="Anaconda" style="height:36px;" />
    <span class="muted" style="font-size:1.3rem;">×</span>
    <img src="/prefix_logo.svg" alt="prefix.dev" style="height:36px;" />
  </div>
</div>
