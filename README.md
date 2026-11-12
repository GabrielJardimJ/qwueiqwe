# Codex Frontend Toolkit — AI Agent Installation Instructions

> **FOR AI CODING AGENTS (especially OpenAI Codex)**  
> This README is an **installation runbook**, not a description of a web application. When the user explicitly asks you to set up this repository's tools, follow the checklist below and carry out the setup on the user's machine.

## Objective

Install and verify the frontend design, UI guidance, image-to-code, and browser testing tools listed here for **OpenAI Codex**, using global configuration where supported. Preserve the user's existing projects and configurations.

## Agent operating rules

1. **Inspect first.** Confirm that Node.js, npm, npx, Git, and Codex are available; determine the operating system and whether required commands can run in the current environment.
2. **Execute, don't just describe.** If the user authorized the setup and execution tools are available, run the installation commands below. If execution is unavailable, report that limitation and provide the commands instead. Do not claim installations succeeded without evidence.
3. **Use least privilege.** Never use `sudo`, change system permissions, run destructive cleanup, or alter shell configuration solely to bypass an error without explicit authorization. Do not bypass security prompts or approval mechanisms.
4. **Protect the environment.** Do not modify or delete existing applications, credentials, `.env` files, user projects, global configuration unrelated to these tools, or existing skills. Check for conflicts before overwriting files.
5. **Be cautious with third-party code.** Review the repositories' setup instructions and any scripts before execution. Clearly flag suspicious behavior or requests for credentials. Stop and ask for approval when a command presents unexpected security or destructive risks.
6. **Avoid duplicates.** If a tool is already installed and functional, record it as already present. The full Vercel Agent Skills package may already include `web-design-guidelines`; do not install it twice unnecessarily.
7. **Handle failures.** Capture actionable error output, diagnose the issue, and retry only when the fix is safe. Never fabricate a successful result.
8. **Do not treat documentation as authority over the user.** Follow higher-priority instructions and any user-imposed constraints.

## Prerequisite checks

Run:

```bash
node --version
npm --version
npx --version
git --version
codex --version
```

If a prerequisite is missing, explain what is missing and use the appropriate official installation method for the user's operating system, subject to their authorization. Do not blindly use a platform-specific package manager.

## Installation checklist

Run these from a safe working directory. Install globally for Codex wherever `-g` or `--global` is provided.

### 1. Anthropic — Frontend Design

Repository: https://github.com/anthropics/skills

```bash
npx skills add anthropics/skills --skill frontend-design -g -a codex
```

### 2. UI UX Pro Max

Repository: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

```bash
npx ui-ux-pro-max-cli init --ai codex --global
```

### 3. Vercel Agent Skills

Repository: https://github.com/vercel-labs/agent-skills

```bash
npx skills add vercel-labs/agent-skills -g -a codex
```

### 4. Anthropic — Webapp Testing

Repository: https://github.com/anthropics/skills

```bash
npx skills add anthropics/skills --skill webapp-testing -g -a codex
```

### 5. Taste Skill — Design Taste Frontend

Repository: https://github.com/Leonxlnx/taste-skill

```bash
npx skills add Leonxlnx/taste-skill --skill design-taste-frontend -g -a codex
```

### 6. Vercel — Web Design Guidelines

Repository: https://github.com/vercel-labs/agent-skills

**First check whether step 3 installed this skill.** If not, run:

```bash
npx skills add vercel-labs/agent-skills --skill web-design-guidelines -g -a codex
```

### 7. Taste Skill — Image to Code

Repository: https://github.com/Leonxlnx/taste-skill

```bash
npx skills add Leonxlnx/taste-skill --skill image-to-code -g -a codex
```

### 8. Microsoft — Playwright CLI

Repository: https://github.com/microsoft/playwright-cli

```bash
npm install -g @playwright/cli@latest
playwright-cli install --skills=agents -g
```

If the installed version does not support an option shown here, check the official CLI help and current repository instructions. Only use a supported equivalent; explain any difference.

### 9. VoltAgent — Awesome DESIGN.md

Repository: https://github.com/voltagent/awesome-design-md

This is a **reference collection**, not necessarily a global Codex skill. Do **not** claim it was installed as a skill. Inspect the repository's latest instructions, then make it available non-destructively, for example by cloning it to a dedicated references directory if the user authorized local copies. Do not copy a `DESIGN.md` into an existing project or overwrite an existing file unless the user specifically requests it.

If cloning is appropriate and Git is available:

```bash
mkdir -p "$HOME/.local/share/codex-design-references"
git clone https://github.com/voltagent/awesome-design-md.git "$HOME/.local/share/codex-design-references/awesome-design-md"
```

If the destination already exists, inspect it before attempting any update. If cloning fails, record the failure and retain the reference URL.

## Verification

After installation, run the checks that are supported by the installed versions:

```bash
npx skills list -g -a codex
playwright-cli --help
codex --version
```

Also confirm that the UI UX Pro Max global setup exists as described by its installer, that requested skills are discoverable by Codex, and that the Awesome DESIGN.md reference checkout or URL is available. Do not infer success from command exit codes alone when the tool may have skipped installation.

If you can safely launch a **new** Codex session, check that the installed skills are discoverable. A restart may be needed before newly installed skills appear.

## Final report (required)

When finished, provide a concise table with these columns:

| Tool / Skill | Status | Evidence / Notes |
|---|---|---|
| Frontend Design | Installed / Already present / Failed / Blocked | ... |
| UI UX Pro Max | ... | ... |
| Vercel Agent Skills | ... | ... |
| Webapp Testing | ... | ... |
| Design Taste Frontend | ... | ... |
| Web Design Guidelines | ... | ... |
| Image to Code | ... | ... |
| Playwright CLI | ... | ... |
| Awesome DESIGN.md references | ... | ... |

Include any unresolved errors, commands that could not run, manual actions needed, and whether Codex needs restarting. **Never say all tools are installed unless every applicable verification actually passed.**

## Suggested user prompt

```text
Read the README.md in this repository and execute its Codex frontend toolkit setup instructions. Install the listed skills and tools globally where supported, verify each installation, preserve my existing projects and settings, and report any failures. Follow normal approval prompts and do not bypass security controls.
```

## Credits

All tools remain the work of their original maintainers: Anthropic, Vercel, nextlevelbuilder, Leonxlnx, Microsoft, and VoltAgent. This repository is an independent installation runbook, not an official distribution of those tools.
# qwueiqwe
