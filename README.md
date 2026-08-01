# ⚡ angrysky56-skills

A curated collection of high-performance skills and workflows for AI agents (Claude, Gemini, Antigravity, GSD, Cursor, Windsurf, etc.).

Designed to optimize LLM context efficiency, enforce systematic reasoning, and streamline autonomous execution.

---

## 📦 Included Skills

| Skill                                                                                                  | Description                                                                                                                                                                                                  | Key Features                                                                                                                                                                       |
| :----------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**`adaptive-socio-emotional-knowledge-ecosysytem`**](./adaptive-socio-emotional-knowledge-ecosysytem) | Provides structured analytical patterns for understanding human behavior and intent through emotional substrates, Information Structure (IS) capture, and transition dynamics.                               | • 7 primary emotional systems (Panksepp)<br>• Dual Process Model (RWA/SDO) bridge<br>• 12-pattern behavioral library<br>• 5-step analytical query framework                        |
| [**`ai-cli`**](./ai-cli)                                                                               | Replaces legacy GNU coreutils (`find`, `grep`, `cat`, `sed`, `ls`) with fast, token-efficient CLI tools (`rg`, `fd`, `ast-grep`, `bat`, `sd`, `jq`, `yq`, `tokei`, `eza`, `dust`, `procs`, `delta`, `just`). | • Token preservation & color stripping<br>• `.gitignore`-aware file & code search<br>• Structured JSON parsing & AST queries<br>• Cross-platform rules                             |
| [**`companion-in-inquiry`**](./companion-in-inquiry)                                                   | Eradicates patronizing "therapist/lecturer" AI defaults and sycophancy, enforcing concrete mechanics over jargon for collaborative conceptual exploration.                                                   | • Anti-sycophancy clause & premise testing<br>• Concrete physical mapping & load-bearing tests<br>• Rejection of essay drift & false forks<br>• Peer-level collaborative discovery |
| [**`explorer`**](./explorer)                                                                           | A general-purpose reasoning loop (**Frame**, **Generate**, **Ground**, **Deliver**) for open-ended, ambiguous, or high-stakes problem-solving.                                                               | • Premise checking & goal reframing<br>• Abductive candidate generation<br>• Evidence grounding & verification<br>• Actionable, high-density delivery                              |

---

## 🚀 Installation & Usage

### 1. Global Installation (Recommended)

Link or copy skill directories into your AI assistant's global configuration directory (e.g. `~/.gemini/config/skills/` or `~/.claude/skills/`):

```bash
# Symlink skills to your global config directory
ln -s ~/your/path/to/angrysky56-skills/adaptive-socio-emotional-knowledge-ecosysytem ~/.gemini/config/skills/adaptive-socio-emotional-knowledge-ecosysytem
ln -s ~/your/path/to/angrysky56-skills/ai-cli ~/.gemini/config/skills/ai-cli
ln -s ~/your/path/to/angrysky56-skills/companion-in-inquiry ~/.gemini/config/skills/companion-in-inquiry
ln -s ~/your/path/to/angrysky56-skills/explorer ~/.gemini/config/skills/explorer
```

### 2. Workspace Scope

To make skills available to an agent within a specific project repository, link them into the `.agents/skills/` folder at your project root:

```bash
mkdir -p .agents/skills
ln -s ~/your/path/to/angrysky56-skills/adaptive-socio-emotional-knowledge-ecosysytem .agents/skills/adaptive-socio-emotional-knowledge-ecosysytem
ln -s ~/your/path/to/angrysky56-skills/ai-cli .agents/skills/ai-cli
ln -s ~/your/path/to/angrysky56-skills/companion-in-inquiry .agents/skills/companion-in-inquiry
ln -s ~/your/path/to/angrysky56-skills/explorer .agents/skills/explorer
```

### 3. Registration via `skills.json`

For setups supporting custom skill manifests, register skills in `skills.json`:

```json
{
  "entries": [
    {
      "path": "path/to/angrysky56-skills/adaptive-socio-emotional-knowledge-ecosysytem"
    },
    { "path": "path/to/angrysky56-skills/ai-cli" },
    { "path": "path/to/angrysky56-skills/companion-in-inquiry" },
    { "path": "path/to/angrysky56-skills/explorer" }
  ]
}
```

---

## 🛠️ Skill Highlights

### 1. [`adaptive-socio-emotional-knowledge-ecosysytem`](./adaptive-socio-emotional-knowledge-ecosysytem)

Analyzes human behavior, political positioning, conflict, and organizational dynamics through neurobiological substrates and narrative capture:

- **Biological Substrates:** Grounded in Panksepp's 7 primary emotional systems (_SEEKING_, _RAGE_, _FEAR_, _PANIC/GRIEF_, _CARE_, _PLAY_, _LUST_).
- **Information Structure (IS) Capture:** Identifies how narrative frameworks capture underlying emotional activations via cognitive energy (CE) efficiency.
- **Pattern Library:** 12 recurring behavioral patterns including Scapegoat Pivot, Coherence Timeout, Burnout Cascade, Algorithmic Escalation Ladder, Mirror Conflict, and Identity Lock-In.
- **Structured Reference Architecture:** Modularized into reference guides (`biological-substrates.md`, `pattern-library.md`, `example-applications.md`, `glossary-and-provenance.md`).

### 2. [`ai-cli`](./ai-cli)

Traditional shell tools were built for human interactive use. They often flood LLM context windows, get stuck in infinite directory loops, and output unstructured text.

`ai-cli` teaches agents to use modern alternatives:

- **Search & Discovery:** `fd` (replaces `find`), `rg` (ripgrep), `ast-grep` (structural code search).
- **Inspection & Editing:** `bat` (surgical line-range viewing), `sd` (safe string replacements).
- **Data Processing:** `jq` (JSON filtering), `yq` (YAML/TOML filtering), `tokei` (code stats).
- **System & Execution:** `eza` (tree view), `dust` (disk usage), `procs` (processes), `delta` (git diffs), `just` (recipe runner).

### 3. [`companion-in-inquiry`](./companion-in-inquiry)

Eliminates sycophantic, patronizing, or overly academic AI behavior during open-ended conceptual exploration:

- **Anti-Sycophancy Clause:** Rejects unearned flattery and false consensus, mechanically stress-testing load-bearing premises instead of giving defensive padding.
- **Concrete Mechanics:** Replaces abstract jargon with physical, mechanical metaphors and first-degree descriptions.
- **Peer Inquiry Protocol:** Eradicates analyst commentary ("What's interesting is..."), false forks, essay drift, and unsolicited summaries, maintaining a true peer dialogue.

### 4. [`explorer`](./explorer)

When facing complex bugs, architectural choices, or vague prompts, agents tend to leap to first conclusions. `explorer` imposes a disciplined 4-phase reasoning protocol:

1. **Frame:** Identify the true goal behind a request and test underlying premises.
2. **Generate:** Formulate competing, plausible hypotheses rather than anchoring early.
3. **Ground:** Test claims against hard codebase facts and checkable empirical evidence.
4. **Deliver:** Provide concise, actionable conclusions with clear remedies and risk callouts.

---

## 📁 Repository Structure

```
angrysky56-skills/
├── adaptive-socio-emotional-knowledge-ecosysytem/ # ASEKE behavioral analysis framework
│   ├── SKILL.md                                  # Core framework & 5-step query procedure
│   └── references/                               # Modular reference guides
│       ├── biological-substrates.md              # Panksepp's systems & political bridges
│       ├── pattern-library.md                    # 12 behavioral & IS capture patterns
│       ├── example-applications.md               # Real-world case study walkthroughs
│       └── glossary-and-provenance.md            # Key concepts, warnings & foundations
├── ai-cli/                                       # Modern CLI skill for agent token efficiency
│   ├── SKILL.md                                  # Agent skill instructions & invocation rules
│   ├── README.md                                 # Tool map & performance guidelines
│   ├── references/                               # Cookbook, cross-platform quirks, installation
│   └── scripts/                                  # Environment verification scripts
├── companion-in-inquiry/                         # Anti-sycophancy peer inquiry protocol
│   └── SKILL.md                                  # Companion in inquiry rules & constraints
├── explorer/                                     # Methodical reasoning loop skill
│   ├── SKILL.md                                  # Skill instructions & execution guidelines
│   ├── evals/                                    # Benchmark evaluation cases
│   └── references/                               # In-depth guides (framing, claims, abduction, explaining)
└── README.md                                     # Repository documentation
```

---

## ✍️ Adding New Skills

When adding a new skill to this repository, adhere to the standard skill layout:

1. Create a subdirectory for your skill (e.g., `my-skill/`).
2. Add a `SKILL.md` file with required YAML frontmatter:
   ```yaml
   ---
   name: my-skill
   description: Concise description of when and why an agent should trigger this skill.
   ---
   # Skill Title

   Instructions and rules for the agent...
   ```
3. Add optional supporting directories:
   - `references/` — Detailed reference guides and documentation.
   - `scripts/` — Executable utilities or test scripts.
   - `examples/` — Code templates or example outputs.
   - `evals/` — Evaluation benchmarks for testing skill execution.

---

## 📜 License

MIT License. Feel free to use, modify, and extend these skills in your AI workflows.
