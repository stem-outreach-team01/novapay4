# stemtastic

Private admin and delivery material for the NovaPay Workshop. The public
student-facing template lives in [devtest](https://github.com/testingdev-007/devtest);
this repo holds everything that must never reach a student.

## What's here

Four folders, by who the material is for. `index.html` at the root routes to the three hub
pages beside it.

| Folder | For | Holds |
|---|---|---|
| `facilitator/` | Mark and Simon, running the day | Run scripts, timed agendas, troubleshooting cards, the training course, **and the answer keys** |
| `student/` | Students, during the session | Participant guide, both tutorials, test plans, projector screens |
| `setup/` | Whoever sets up a programme | GitHub org and Copilot seat guides, the event operations plan |
| `template/` | Copied into `devtest` | `bank-dashboard.html`, `starter-template.html`, `challenge.js`, `devcontainer.json`, `copilot-instructions.md` — the five files students receive |

Student handouts live in `student/` **in this repo**, not in `devtest`. Only the five files in
`template/` are published to students, via "Use this template". A classification of every file,
and what is being moved into the Staffroom app, is in
[docs/root-file-audit.html](docs/root-file-audit.html).

**Answer keys** — `facilitator/bug-answer-key.html`, `facilitator/printable-bug-cheatsheet.*`
and `facilitator/facilitator-reference.html` spell out every planted bug and its fix. **This
repo must stay private**: these files defeat the entire bug hunt if a student ever sees them.

`live/` is separate from all of the above — the agenda, student feedback and Staffroom app.
See [live/README.md](live/README.md).

## Who's involved

- **Simon and Mark** — administer both repos, using Claude Code for edits.
- **Students** — never see this repo or its facilitator material. They do receive `devtest`'s five template files (`bank-dashboard.html`, `starter-template.html`, `challenge.js`, and the two Codespace/Copilot config files) via "Use this template" — that's the whole point of keeping the two repos separate.

## Branching (GitFlow)

- `main` — released state only.
- `develop` — integration branch.
- `feature/*` — all work branches off `develop` and lands via PR. Nothing gets pushed directly to `main` or `develop`.

This applies to both `stemtastic` and `devtest`.
