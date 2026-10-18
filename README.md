# No Short Skills

A collection of reusable skills for Codex, Claude Code, and other AI agents. Built by Long.

Writing cleanup and evidence-based personal work reports, distributed independently from [No Short Usage](https://github.com/longlonglong173/no-short). No application, local MCP runtime or API key is required by this package. A report needs access to at least one evidence source selected by the user.

## Available skills

| Skill | Purpose |
| --- | --- |
| [no-ai-slop](skills/no-ai-slop/SKILL.md) | Edit writing while preserving facts and personal voice, or audit observable patterns without guessing authorship. |
| [personal-work-report](skills/personal-work-report/SKILL.md) | Create personal standup, weekly, sprint or monthly reports from verified Jira, GitHub or Slack activity. |

## Install

### Skills CLI

```sh
npx skills add longlonglong173/no-short-skills --list
npx skills add longlonglong173/no-short-skills --all
```

Or choose a skill and agents:

```sh
npx skills add longlonglong173/no-short-skills --skill no-ai-slop --agent codex claude-code
npx skills add longlonglong173/no-short-skills --skill personal-work-report --agent codex claude-code
```

### Codex plugin

```sh
codex plugin marketplace add longlonglong173/no-short-skills
codex plugin add no-short-skills@no-short-skills
```

Start a new chat after installation.

### Claude Code plugin

```text
/plugin marketplace add longlonglong173/no-short-skills
/plugin install no-short-skills@no-short-skills
```

Start a new session after installation.

## Moving from no-short

The two skills moved here without changes to their instructions, supporting references or templates. Their related Git history was extracted from `no-short`; version 0.1.0 starts this repository's independent package versioning.

Use the new installation source above for future updates. A cached installation from `no-short` can still contain the old skills. Remove the old skill copies with your installer if they appear twice. If you installed the old Claude skills-only plugin, uninstall `no-short@no-short` after installing this replacement. Codex users who use the Usage panel should keep the `no-short` plugin as well; it now provides Usage only. The separate No Short Usage.app is unaffected.

Existing GitHub releases and public-directory submissions for the old package are historical and are not automatically updated by this migration. This repository does not claim a new directory approval or publication.

## Development

```sh
npm run validate
claude plugin validate .
```

See [CONTRIBUTING.md](CONTRIBUTING.md), [CHANGELOG.md](CHANGELOG.md), [PRIVACY.md](PRIVACY.md) and [LICENSE](LICENSE).

Review each skill and connected-service permissions before use. Skills run within the permissions granted to your agent.
