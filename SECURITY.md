# Security Policy

Light Skills is a public AI workflow skill package. Its main security concerns are not only code vulnerabilities, but also accidental disclosure of private research, credentials, local memory, unpublished data, and misleading AI-generated claims.

## Supported versions

| Version | Supported |
| --- | --- |
| `main` / `master` | Yes |
| `v1.x` releases | Yes |
| Older private or pre-release local copies | No |

## Reporting a vulnerability

Please do not open a public GitHub Issue for sensitive reports.

Preferred reporting route:

- Email: `1833058953@qq.com`
- Subject prefix: `[Light Skills Security]`

Please include:

- repository URL and affected file path;
- a concise description of the issue;
- minimal reproduction steps, if applicable;
- whether any credential, unpublished data, or private memory may have been exposed;
- your recommended severity, if you have one.

If GitHub Security Advisories are enabled for the repository, you may also use a private security advisory.

## What counts as a security issue?

Examples include:

- exposed API keys, tokens, credentials, cookies, or private email configuration;
- committed private conversations, unpublished research, local project ledgers, or database dumps;
- scripts that unexpectedly read, upload, delete, or publish user files outside the intended workspace;
- instructions that encourage users to paste secrets into chat;
- supply-chain risks in installation scripts;
- unsafe defaults that could overwrite user work;
- prompt or workflow patterns that cause fabricated citations, fake DOI values, or fake links to be presented as verified facts;
- any workflow that silently sends private research materials to external services without user awareness.

## What is usually not a security issue?

Please use normal GitHub Issues for:

- unclear documentation;
- installation problems without data exposure;
- feature requests;
- normal skill-quality improvements;
- typos or formatting issues;
- disagreements about research workflow design.

## Maintainer response

The maintainer will try to:

- acknowledge security reports within 7 days;
- confirm scope and severity after reproduction;
- prioritize fixes that protect credentials, private research, or user files;
- publish a short public note after a fix when disclosure is safe and useful.

Response times are best-effort for a volunteer-maintained open-source project.

## User safety guidance

When using Light Skills:

- do not commit API keys, credentials, private data, or unpublished research;
- review generated citations, DOI values, links, venue rules, and software versions;
- treat `unknown` / `待核查` as a required verification marker, not a failure;
- keep paper figures, data figures, and experiment figures reproducible from code or source data;
- do not present AI-generated marketing images as scientific evidence;
- confirm before installing optional system tools such as LaTeX or R packages.

## Scope of responsibility

Light Skills can help organize research, code, figures, papers, patent-disclosure drafts, and software-copyright materials. It does not replace:

- legal counsel;
- institutional security review;
- research ethics review;
- human verification of citations and claims;
- final publication, patent, or software-copyright decisions.

