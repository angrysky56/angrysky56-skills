# ⚡ angrysky56-skills

A curated collection of high-performance skills and workflows for AI agents (Claude, Gemini, Antigravity, GSD, Cursor, Windsurf, etc.).

Designed to optimize LLM context efficiency, enforce systematic reasoning, and streamline autonomous execution.

---

## 📦 Included Skills

| Skill | Description | Key Features |
| :--- | :--- | :--- |
| [**`ai-cli`**](file:///home/ty/Repositories/ai_workspace/angrysky56-skills/ai-cli) | Replaces legacy GNU coreutils (`find`, `grep`, `cat`, `sed`, `ls`) with fast, token-efficient CLI tools (`rg`, `fd`, `ast-grep`, `bat`, `sd`, `jq`, `yq`, `tokei`, `eza`, `dust`, `procs`, `delta`, `just`). | • Token preservation & color stripping<br>• `.gitignore`-aware file & code search<br>• Structured JSON parsing & AST queries<br>• Cross-platform rules |
| [**`explorer`**](file:///home/ty/Repositories/ai_workspace/angrysky56-skills/explorer) | A general-purpose reasoning loop (**Frame**, **Generate**, **Ground**, **Deliver**) for open-ended, ambiguous, or high-stakes problem-solving. | • Premise checking & goal reframing<br>• Abductive candidate generation<br>• Evidence grounding & verification<br>• Actionable, high-density delivery |

---

## 🚀 Installation & Usage

### 1. Global Installation (Recommended)
Link or copy skill directories into your AI assistant's global configuration directory (e.g. `~/.gemini/config/skills/` or `~/.claude/skills/`):

```bash
# Symlink individual skills to your global config
ln -s ~/Repositories/ai_workspace/angrysky56-skills/explorer ~/.gemini/config/skills/explorer
ln -s ~/Repositories/ai_workspace/angrysky56-skills/ai-cli ~/.gemini/config/skills/ai-cli
```

### 2. Workspace Scope
To make skills available to an agent within a specific project repository, link them into the `.agents/skills/` folder at your project root:

```bash
mkdir -p .agents/skills
ln -s ~/Repositories/ai_workspace/angrysky56-skills/explorer .agents/skills/explorer
ln -s ~/Repositories/ai_workspace/angrysky56-skills/ai-cli .agents/skills/ai-cli
```

### 3. Registration via `skills.json`
For setups supporting custom skill manifests, register skills in `skills.json`:

```json
{
  "entries": [
    { "path": "/home/ty/Repositories/ai_workspace/angrysky56-skills/explorer" },
    { "path": "/home/ty/Repositories/ai_workspace/angrysky56-skills/ai-cli" }
  ]
}
```

---

## 🛠️ Skill Highlights

### 1. [`ai-cli`](file:///home/ty/Repositories/ai_workspace/angrysky56-skills/ai-cli)
Traditional shell tools were built for human interactive use. They often flood LLM context windows, get stuck in infinite directory loops, and output unstructured text.

`ai-cli` teaches agents to use modern alternatives:
* **Search & Discovery:** `fd` (replaces `find`), `rg` (ripgrep), `ast-grep` (structural code search).
* **Inspection & Editing:** `bat` (surgical line-range viewing), `sd` (safe string replacements).
* **Data Processing:** `jq` (JSON filtering), `yq` (YAML/TOML filtering), `tokei` (code stats).
* **System & Execution:** `eza` (tree view), `dust` (disk usage), `procs` (processes), `delta` (git diffs), `just` (recipe runner).

### 2. [`explorer`](file:///home/ty/Repositories/ai_workspace/angrysky56-skills/explorer)
When facing complex bugs, architectural choices, or vague prompts, agents tend to leap to first conclusions. `explorer` imposes a disciplined 4-phase reasoning protocol:

1. **Frame:** Identify the true goal behind a request and test underlying premises.
2. **Generate:** Formulate competing, plausible hypotheses rather than anchoring early.
3. **Ground:** Test claims against hard codebase facts and checkable empirical evidence.
4. **Deliver:** Provide concise, actionable conclusions with clear remedies and risk callouts.

---

## 📁 Repository Structure

```
angrysky56-skills/
├── ai-cli/                 # Modern CLI skill for agent token efficiency
│   ├── SKILL.md            # Agent skill instructions & invocation rules
│   ├── README.md           # Tool map & performance guidelines
│   ├── references/         # Cookbook, cross-platform quirks, installation
│   └── scripts/            # Environment verification scripts
├── explorer/               # Methodical reasoning loop skill
│   ├── SKILL.md            # Skill instructions & execution guidelines
│   ├── evals/              # Benchmark evaluation cases
│   └── references/         # In-depth guides (framing, claims, abduction, explaining)
└── README.md               # Repository documentation
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
