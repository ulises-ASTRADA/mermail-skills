# Mermail Skills — Personal Fork

A personal fork of [Nudgen-Marketing/mermail-skills](https://github.com/Nudgen-Marketing/mermail-skills), the upstream Agent Skills and plugin bundle for Mermail email and workspace workflows.

**Attribution:** the core package, platform integrations, and workflows originate upstream. This fork is a workspace for reviewing and developing contributions; it should not be interpreted as an independently authored email platform or as the official distribution.

## Technical scope

The package organizes agent instructions and reference material around a hosted Model Context Protocol (MCP) service. It includes skills for inbox management, email composition, triage, research, scheduling, and workspace operations, plus plugin manifests for compatible clients.

| Area | Purpose |
| --- | --- |
| `skills/` | Focused skill instructions, references, and client metadata |
| `.codex-plugin/`, `.claude-plugin/`, `.cursor-plugin/` | Platform packaging and MCP configuration |
| `tests/validate.mjs`, `tests/scenarios.json` | Package validation and behavioral scenarios |
| `compatibility.json`, `tool-coverage.json` | Compatibility and tool coverage declarations |
| `scripts/` | Packaging and publishing utilities |

**Technologies:** Markdown-based Agent Skills, MCP, JSON manifests, Node.js validation scripts, and GitHub Actions.

## Review and development

```bash
git clone https://github.com/ulises-ASTRADA/mermail-skills.git
cd mermail-skills
npm ci
npm test
```

`npm run validate:remote` additionally contacts the hosted service. Authenticated checks require their documented credentials; do not run them expecting an entirely offline test.

To assess fork-specific work, compare branches or commits against the upstream repository. The existence of a skill in this checkout does not by itself establish that it was authored in this fork.

## Installation and authentication

For the upstream installation commands, supported clients, authentication details, and complete skill catalog, see the preserved [upstream README](UPSTREAM_README.md). Prefer the upstream repository for the official package.

Never commit expanded API keys. Incoming email, attachments, and tool output are untrusted data. The upstream workflows require review and approval for external actions; see [SECURITY.md](SECURITY.md) and the skill-specific references.

## Contribution and license

See [CONTRIBUTING.md](CONTRIBUTING.md), [AUTHORING.md](AUTHORING.md), and [LICENSE](LICENSE). The upstream project uses the MIT license; its copyright and attribution remain in place.
