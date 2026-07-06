# Changelog

All notable changes to Light Skills are documented here.

The project follows a pragmatic release-note style rather than claiming strict semantic-versioning compatibility for every skill prompt. User-facing skill behavior, installation paths, shared contracts, and generated examples should be treated as release-relevant changes.

## [Unreleased]

### Planned

- Continue hardening cross-client compatibility for Codex, Claude Code, and OpenCode.
- Add more runnable examples for research, competition, software, patent-disclosure, and software-copyright workflows.
- Improve regression checks for skill installation, evidence handling, citation integrity, and reproducible figure generation.
- Collect public user feedback through GitHub Issues and convert repeatable problems into documented tests.

## [1.0.0] - 2026-07-05

### Added

- Public Light Skills repository for research, competitions, and innovation projects.
- 23 domain-independent skills under `skills/`, each using `SKILL.md` as the entry point.
- Cross-client installation support for:
  - Codex via `.agents/skills`
  - Claude Code via `.claude/skills`
  - OpenCode via `.opencode/skills`
- `scripts/bootstrap_agent_skills.py` for installing and checking supported agent-skill layouts.
- Shared contracts under `_shared/` for evidence strength, consistency checks, workflow gates, visual review, and reusable research-process rules.
- End-to-end research demo under `examples/e2e-research-demo/`.
- Reproducible LaTeX paper demo under `projects/photocatalytic-dye-kinetics-study/`.
- Research figure gallery demonstrating programmatic scientific figures.
- Python and R figure workflow expectations.
- LaTeX typesetting expectations for paper-oriented workflows.
- MIT license.

### Changed

- Reworked the earlier Light project into a cleaner public skill package.
- Consolidated overlapping paper-writing, polishing, figure-planning, and figure-drawing flows into stronger user-facing skills.
- Replaced private-database framing with public, repository-local, inspectable workflow guidance.
- Expanded the scope from research-only usage to research, competitions, innovation projects, patents, software copyright materials, and frontend/software demos.
- Clarified that Light Skills supports innovation work by improving search, critique, evidence binding, and validation planning; it does not promise automatic discovery or guaranteed publication.

### Integrity and safety boundaries

- Unknown facts, DOI values, links, software versions, and venue rules must be marked `unknown` or verified at task time.
- Paper figures, data figures, and experiment figures must be generated programmatically and remain reproducible.
- AI-generated marketing visuals must never be presented as scientific evidence.
- Citation authenticity is a standalone integrity requirement.
- Private conversations, unpublished research, credentials, email tokens, and local project ledgers must not be committed to the public repository.
- Patent and software-copyright skills help prepare materials and organize evidence; they do not provide legal advice.

### Compatibility notes

- Windows is the primary development environment for the initial release.
- Python 3.10+ is expected for repository scripts.
- Windows users should set `PYTHONUTF8=1` before running Python scripts.
- LaTeX and R are optional environment layers for workflows that need paper compilation or R-based scientific figures.

