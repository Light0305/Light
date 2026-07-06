# Contributing to Light Skills

Thank you for considering a contribution to Light Skills.

Light Skills is a public, domain-independent AI workflow skill package for research, competitions, and innovation projects. Contributions are welcome when they make the package more useful, more reliable, more honest about its limits, or easier to install across Codex, Claude Code, and OpenCode.

## What contributions are useful?

Good contributions include:

- fixing unclear skill instructions;
- improving cross-client compatibility;
- adding runnable self-tests for scripts;
- improving examples, installation docs, or release notes;
- reporting places where a skill overclaims what it can actually do;
- strengthening citation, evidence, privacy, or reproducibility checks;
- adding domain-neutral patterns that help many research areas;
- improving Python, R, LaTeX, or frontend-demo workflows.

Please avoid contributions that:

- embed one person's private research context into public skills;
- add unverifiable claims, fake DOI values, fake links, fake metrics, or fake citations;
- turn generated images into scientific evidence;
- require private MCP servers, local databases, credentials, or unpublished data for the public package to work;
- make broad promises such as guaranteed acceptance, guaranteed patents, or automatic scientific innovation.

## Repository structure

```text
Light-Skills/
├─ skills/       # Canonical skill source; each skill uses SKILL.md as the entry
├─ _shared/      # Shared contracts, evidence rules, gates, and helper guidance
├─ scripts/      # Installation and maintenance scripts
├─ docs/         # Compatibility notes, release gates, learning notes, and releases
├─ examples/     # End-to-end user-facing examples
├─ projects/     # Reproducible demo projects
└─ assets/       # Public brand, README, QR-code, and preview assets
```

## Before opening a PR

1. Fork the repository and create a focused branch.
2. Keep each PR scoped to one change theme.
3. Read the affected `SKILL.md` file before editing it.
4. Make sure the change is useful across research fields, not only for one private project.
5. Do not commit secrets, credentials, personal conversations, unpublished research, or local machine state.
6. If you used AI assistance, review the output carefully and take responsibility for every claim and line changed.

## Local checks

On Windows PowerShell:

```powershell
$env:PYTHONUTF8="1"
python scripts\bootstrap_agent_skills.py --check-only
```

If you modify a script, add or run the relevant self-test. A script that claims to support `--selftest` or an equivalent check should run successfully before the change is submitted.

If you modify a skill, manually inspect the generated client layout when relevant:

```powershell
$env:PYTHONUTF8="1"
python scripts\bootstrap_agent_skills.py --targets agents --mode auto --force
python scripts\bootstrap_agent_skills.py --targets claude --mode auto --force
python scripts\bootstrap_agent_skills.py --targets opencode --mode auto --force
```

## Skill quality rules

Every skill should be:

- **honest**: it must not claim abilities that the instructions or scripts cannot actually support;
- **domain-neutral**: default behavior should work across fields unless a section is explicitly scoped;
- **evidence-aware**: uncertain facts must be verified or marked `unknown`;
- **user-centered**: it should ask the user at meaningful decision points instead of silently pretending to know the correct research direction;
- **reproducible**: paper figures, data figures, and experiment figures should be generated programmatically;
- **portable**: public workflows should not depend on a private database, private memory, or a specific user's local setup;
- **reviewable**: important outputs should leave enough trace for a human to audit them.

## Citation and evidence policy

Light Skills treats citation integrity as a core trust boundary.

- Do not invent papers, authors, DOI values, links, GitHub stars, metrics, or benchmark results.
- If a fact cannot be verified in the current task context, mark it `unknown` or `待核查`.
- Do not cite a source you have not actually inspected.
- Distinguish evidence, inference, and recommendation.
- Do not use popularity as proof of correctness.

## Figure and media policy

- Scientific figures, data charts, and experiment visuals must be generated from code or traceable source data.
- AI-generated images may be used for marketing, illustration, or README branding, but must not be represented as paper figures, data figures, or experiment results.
- Figure workflows should preserve source data, code, labels, units, and reproducibility notes where practical.

## Privacy policy for contributions

Do not include:

- private chat logs;
- unpublished research details;
- user emails or credentials;
- API keys or tokens;
- local database dumps;
- private MCP configuration;
- local project ledgers that are not intended for public release.

If you accidentally commit sensitive information, rotate the credential immediately and open a security report rather than a normal issue.

## Issue reports

When opening an issue, please include:

- what you tried to do;
- which agent client you used, if any;
- your operating system;
- the skill or script involved;
- the expected behavior;
- the actual behavior;
- minimal reproduction steps;
- relevant logs with secrets removed.

## Pull request checklist

Before submitting, confirm:

- [ ] The change is public and domain-neutral, or clearly marked as domain-scoped.
- [ ] No private data, credentials, or unpublished research were added.
- [ ] No unverifiable claims, fake citations, fake DOI values, or fake metrics were added.
- [ ] Any changed script has a relevant runnable check.
- [ ] Any changed skill still matches what the repository can actually do.
- [ ] Documentation was updated when user-facing behavior changed.

## License

By contributing, you agree that your contribution will be licensed under the repository's MIT License.

