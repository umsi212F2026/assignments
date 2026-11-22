# Final project

Instructions for an agent working in the final project. The project folder is the one this file
is in: the root of the student's project repository, or `project/` in their assignments
repository. The student's instructions are `project/INSTRUCTIONS.md` in their assignments
repository.

## After a round's implementation is committed, offer to record it

**Once `ROUNDS.md` names a base**, its `Base:` line followed by a commit hash rather than
`<commit hash>`, then after the commits that implement a Superpowers plan are in, follow
`record-round`:

    <course-materials>/workflows/rounds/skills/record-round/SKILL.md

where `<course-materials>` is the folder `~/.codex/AGENTS.md` names.

A round is a spec in `docs/superpowers/specs/` and a plan in `docs/superpowers/plans/` inside
the project folder, both committed after the base, then the commits that implement them. Offer once the implementation is
committed, not while it is still being built, and not after a commit that only changes a spec or
a plan.

**Commit the spec and the plan on their own, before writing any code that implements them.**
Code committed before its plan's commit can never be part of that round.

Whether to offer is your call. Whether the round goes in the record is the student's:
`record-round` asks them, and you never decide that for them or write its own-words parts
yourself.

**Do not offer the same round twice.** Once the student declines one, it stays out unless they
bring it up. If they ask you to stop offering, stop for the rest of the session. A round you pass
over can still be recorded later with `find-rounds`.

Before the base is named, nothing goes in the record. Do not offer.

## Never edit `ROUNDS.md` by hand

Every read and write of it goes through the tool those skills run, `rounds.mjs`. The student may
edit it; you do not.

**The one exception is the `Base:` line**, which the student sets by hand, naming the commit
where the base is in place. A commit cannot contain its own hash, so it goes in a later commit.
If the student asks you to fill it in, you may edit that one line and nothing else, and only with
a hash the student has confirmed is the right commit.

## Before committing anything under `examples/`

**Remind the student once, before the first such commit in a session**, that the repository may
be public, and that an input with someone's personal details in it (names, email addresses,
anything about a real person) needs a stand-in with the details changed before it is committed.
Public material such as job postings can go in as it is. Then do what they say.

## Where things go

- the record: `ROUNDS.md`, through `rounds.mjs` only
- each round's spec and plan: `docs/superpowers/specs/` and `docs/superpowers/plans/` inside
  the project folder. **For a project kept in `project/`**, that is
  `project/docs/superpowers/specs/` and `project/docs/superpowers/plans/`, not the
  `docs/superpowers/` at the top of the assignments repository where Superpowers would put them:
  when brainstorming and planning, tell Superpowers to write them there. `rounds.mjs` sees only
  specs and plans inside the project folder.
- for a workflow, the report: `docs/index.html`, or `docs/index.md` if the student writes it in
  Markdown, served by GitHub Pages from `/docs` on `main`. The diagram image and the links must be
  in the page as served, not added by a script, because the check reads the served page. GitHub
  Pages runs Jekyll over `docs/`, and a `{{` or `{%` in a plan under `docs/superpowers/` can fail
  the build. For a plain-HTML report, add an empty `docs/.nojekyll`. For a Markdown report, which
  needs Jekyll to render it, add `exclude: [superpowers]` to `docs/_config.yml` instead.
- for a workflow, the diagram as a PNG: `docs/workflow.png`, rendered from the BPMN file with
  `<course-materials>/workflows/diagram/tools/render.mjs`
- for a workflow, skills: `skills/<name>/SKILL.md`
- for a workflow, evidence of runs: `examples/<id>/input.<ext>` and `examples/<id>/output.<ext>`,
  one folder per input
- for a deployed project, `README.md`: what each round added and where to see it in the app,
  naming each round by its title in `ROUNDS.md`
