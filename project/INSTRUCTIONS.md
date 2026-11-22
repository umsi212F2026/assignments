# Final Project: Two More Rounds

## What you are doing

**Take something you built this term, or something new, and add two features to it, each with
the method the course taught**: a Superpowers spec, a plan, and an implementation. For each one
you will also say, in your own words, what it added and why it was worth doing next.

The project is deliberately light. It is 15% of the course grade, and the end of the term is
for reviewing the conceptual material. Two honest rounds, written up honestly, should reliably
earn 90%. The last 10% is for inspiration: something that wows the instructor.

**Every project goes into the public class showcase**, so you will end the term with something
you can point to: a running site, or a web page that explains a workflow. There is no demo in
class. The showcase is the audience.

Every project has two parts: **a base, then two rounds.**

## Choosing a project

**Extend one of your problem sets, or build something new.** The base depends on which:

| the project                        | its base                                       | showcase card links to  |
| ---------------------------------- | ---------------------------------------------- | ----------------------- |
| extends PS1, PS2, PS3 or PS4       | the problem set's work, **publicly deployed**  | the running site        |
| extends PS5                        | the PS5 workflow, deployed or on your laptop   | the site, or the report |
| something new, deployed            | a live URL a visitor can open                  | the running site        |
| something new, a workflow          | PS5's core (below)                             | the report              |

**"Publicly deployed" means a URL an anonymous visitor can open that shows the work.** That
applies to PS1 and PS4 too, which did not have to be deployed. For PS1, a Python program that
writes a Markdown report, the report served on GitHub Pages is enough; an interactive page
would be a round, not the base. PS4 is already a web page. **Deploying never counts as a
round**, even where it is new work.

**An extension's base is the problem set as you handed it in**, copied across and, where
required, deployed. It is not graded again. Finishing what it lacked is allowed but earns
nothing. What an extension owes is **two features beyond the original problem set's
requirements**, judged against those requirements rather than against what you handed in.

**A new deployed project's base** is a live URL that an anonymous visitor can open. It needs
sign-in only if the app keeps per-user data.

**A new workflow's base is PS5's core:**

- a BPMN diagram
- at least one step done by an agent following a skill file in the repository, in
  `skills/<name>/SKILL.md`
- at least one step done by a program or by you
- at least ten real inputs it has processed, each saved in `examples/<id>/` as `input.<ext>`
  beside the `output.<ext>` the workflow produced from it. How many runs that took does not
  matter.

PS5's change record is not required. The two rounds take its place.

**A deployed project is graded live.** When the grader runs, the site must be running the work
you submitted, with both rounds' features in it. A free tier that sleeps is fine; one that has
expired is not.

### Negotiated terms

**For a creative project that does not fit these molds, you may propose your own terms.** Email
the instructor by **Wed Dec 2, 11:59 PM** with:

- what you plan to do
- what you think the grading rubric for it should be

Keeping the inspiration 10% in your rubric is a good idea, though you may propose otherwise. The
showcase still applies, in whatever form your terms say. The reply will come by email.

**Without an agreed proposal, the standard terms apply.** If you miss Dec 2, or the instructor
does not agree to your proposal, you are on the standard path.

**Once your terms are agreed**, commit them, with the instructor's reply, as `project/TERMS.md`
in your assignments repository. The grader will read the rubric from there, and the instructor
will grade your project against it. When you start the project, tell your agent the instructor
has agreed negotiated terms.

## Starting it

**Ask your agent to start your final project.** It will ask you, one question at a time, what
your project extends, whether it is a deployed site or a workflow, and where its code should
live. Then it will set up the project's folder and fill in the first three lines of
`project/SUBMIT.md`.

**Where the work lives depends on the kind of project:**

- **A workflow goes in a new public repository.** The public cannot run a workflow on your
  laptop, so they read its code instead.
- **A deployed project may go in a new public repository, or in `project/` here**, in your
  private assignments repository, the same two choices PS3 offered.
- **If your PS3 already lives in a public repository of its own**, and you are extending it,
  you can keep working there.

For an extension, your agent will copy the problem set's folder into the project, leaving out
the course's files and your written answers: `AGENTS.md`, `INSTRUCTIONS.md`, `CHANGES.md`,
`REFLECTION.md`, `QUESTIONS.md`, the `rubrics/` and `tasks/` folders, and any `.env` file. The
copy starts with no git history, which is fine: the base is the "before" that your rounds are
measured against. **Before it creates a public repository, your agent will show you its name
and what will be copied into it, and wait for your yes.** Anything you push there is public for
good.

A new public repository starts with two files from this folder: `AGENTS.md`, which tells your
agent when to offer to record a round, and `ROUNDS.md`, your record.

**Then get your base working, and name it.** When the base is in place, committed and, where
required, deployed, find that commit's hash (`git log --oneline` shows it, or ask your agent)
and replace the placeholder on the `Base:` line of `ROUNDS.md`, so it reads `Base: <that hash>`.
A commit cannot contain its own hash, so this line will go in a later commit. If you started
work early somewhere else, copy it across first: work done before the base is part of the base.

## Rounds

**A round is a Superpowers spec and plan, committed, then the commits that implement them,
adding a new feature beyond the base.** Superpowers puts the spec in `docs/superpowers/specs/`
and the plan in `docs/superpowers/plans/`, inside the project folder. Both must be committed
after your base, and the implementing commits after the plan.

**If your project is in `project/` here, its specs and plans go in `project/docs/superpowers/`**,
not in `docs/superpowers/` at the top of this repository, where PS2 told you to leave them. Only
specs and plans inside the project folder can be rounds. Your agent will tell Superpowers to
write them there.

**Not a round:**

- a bug fix
- anything needed to reach the base, including, for an extension, anything the original
  problem set required, finished or not
- deploying, or moving to a different host

**There is no size bar on a feature.** The inspiration 10% rewards ambition.

**Your agent will offer to record each round** once `ROUNDS.md` names your base, after the
round's implementation is committed. It will fill in the spec, the plan and the commits from
git. If the round looks like a bug fix, catch-up or deployment, it will tell you so, and that
it would not count. Whether to record it anyway is up to you.

**Two parts of each round are in your own words**, and your agent will ask you for each one. A
tool will copy your answer into `ROUNDS.md` exactly as you typed it.

- **What's new:** the feature the round added, concretely enough to find in the running app or
  the workflow. "Adds a weekly email digest of new postings" is concrete. "Made it better" is
  not.
- **Why next:** why this feature was worth doing next. "I kept missing deadlines buried in long
  postings" gives a reason. "It seemed good" does not.

**If you made a round without recording it**, ask your agent to **find rounds for your
record**. It will list the plans committed since your base that are not in `ROUNDS.md` yet,
with the commits that look like their implementation, and ask which ones you want to add.

## The report

**A project whose showcase card links to a report**, a workflow on your laptop, needs a web page
served by GitHub Pages from its public repository. Put it at `docs/index.html`, or
`docs/index.md` if you write it in Markdown. Its outline is
fixed, so every report reads the same way to a grader and to a visitor:

1. **What the workflow does, and for whom**, in a paragraph.
2. **The diagram, as a PNG**, saved as `docs/workflow.png` and shown on the page. Ask your
   agent to render it from your BPMN file with `workflows/diagram/tools/render.mjs` in your
   `course-materials` folder.
3. **One section per design decision from sessions 18 to 22:** dividing the work into steps
   and who does each, what triggers it, how state is stored, what each part can touch, and how
   failures are handled. Each says what your workflow does and why, with **deep links into the
   repository, pinned to a commit**, to the skill, program or config that does it.
4. **The two rounds:** what each added, linked to its spec, plan and commits.

**A link pinned to a commit names the commit's hash, not a branch:**
`https://github.com/you/your-repo/blob/3f1c2a9/skills/assess/SKILL.md#L12`, never
`.../blob/main/...`. A link to `main` points somewhere else as soon as the file changes. On a
file's page on GitHub, pressing `y` turns the address into one pinned to the current commit.
The commit has to be pushed for the link to work.

How the page is built is up to you and your agent. Plain HTML, or Markdown that GitHub Pages
renders, are both fine. **The diagram image and the links must be in the page itself**, not
added by a script when it loads, because the check reads the page as GitHub Pages serves it.

**To turn on GitHub Pages:** on GitHub, open the repository's **Settings**, then **Pages**.
Under **Build and deployment**, set the source to **Deploy from a branch**, the branch to
`main` and the folder to `/docs`, and save. A minute or two later the report will be at
`https://<your username>.github.io/<repository name>/`. That address is your card's
`projectUrl`.

## For a deployed project, the README

**A deployed project needs no report.** Its card links to the running site, and its `README.md`,
at the top of the project folder, says what each of the two rounds added and where to see it in
the app. Name each round there by its title in `ROUNDS.md`, the words after `## 1.` and `## 2.`.
For a project kept in `project/`, that is `project/README.md`, in place of the paragraph there
now.

## Personal data

**The repository may be public, so anyone can read what you commit.** PS5's rule carries over
unchanged: if an input has someone's personal details in it (names, email addresses, anything
about a real person), replace them with made-up ones before you commit it. A stand-in still
counts as a real input. Public material such as job postings can go in as it is.

If you extend PS5 into a public repository, your agent will ask you to confirm that every input
in `ps5/examples/` is a stand-in or has nothing personal in it before it copies them across.
Your agent will also remind you before it commits anything new under `examples/`.

## The showcase

Add your project to [the class showcase](https://umsi212f2026.github.io/student-showcase/) with a
pull request to `umsi212F2026/student-showcase`, as in PS3. Its
[README](https://github.com/umsi212F2026/student-showcase#readme) has the steps.

- **Your card is `<your username>-project.json`**, with `assignment` set to `"Final Project"`.
- **Its `projectUrl` is the running site**, or for a workflow, the report on GitHub Pages.
- **For a workflow, set `projectType` to `"Workflow"`.**
- **Its `githubUrl` is your public repository's URL**, the same one on the `Work:` line of
  `SUBMIT.md`. If your code is in `project/` here, leave `githubUrl` out: this repository is
  private, so anyone following the link would get a 404.
- **If you extended PS3, your project replaces your PS3 card**: the same pull request deletes
  `<your username>-ps3.json` and adds the new card. If you would rather keep both cards, you may.
  Any other project adds a card.

**The pull request runs checks, and they have to pass.** If one fails, read its log, fix it, and
push to the same branch. Do not open a second pull request.

**The showcase is public.** Use whatever name you are comfortable having on the public internet.

## Check it yourself before you hand it in

**Ask your agent whether your final project is ready to submit.** It will check everything a
program can check, some of it as a stranger on the web sees it, without your sign-in: that a
workflow's repository is public, that your site or report answers, that the report has its
diagram and pinned links, and that the showcase pull request has its fields right. It will also
check that `ROUNDS.md` names a base and has two rounds, that `SUBMIT.md` is filled in, and that
everything is committed and pushed in both repositories.

Then it will show you each own-words part of `ROUNDS.md` and ask whether you wrote it yourself.
A yes is recorded in `ROUNDS.md` with the date. If you say no, rewrite that part in your own
words, and it will ask you again. It will also warn you about an own-words part that might lose
credit, and about a round that looks like a bug fix or catch-up. Whether to change either is up
to you.

## What you hand in

| what                                                  | where                                              |
| ----------------------------------------------------- | -------------------------------------------------- |
| where your work is, and your showcase pull request    | `project/SUBMIT.md` in this repository             |
| the project, with its base and both rounds            | your public repository, or `project/` here          |
| the record                                            | `ROUNDS.md` at the top of the project              |
| each round's spec and plan                            | `docs/superpowers/specs/` and `docs/superpowers/plans/` |
| for a workflow, the report and its diagram            | `docs/index.html` (or `docs/index.md`) and `docs/workflow.png`, on GitHub Pages |
| for a deployed project, the README                    | `README.md` at the top of the project              |
| the running site, for a deployed project              | at your card's `projectUrl`                        |
| the showcase pull request                             | open or merged on `umsi212F2026/student-showcase`  |
| for negotiated terms, the agreed terms                | `project/TERMS.md` in this repository              |

`SUBMIT.md` has four lines. Your agent will fill in the first three when you start; you add the
last when you open the showcase pull request:

- `Kind:` `deployed`, `workflow` or `negotiated`
- `Extends:` `PS1` to `PS5`, or `new`
- `Work:` your public repository's URL, such as `https://github.com/you/your-repo`, or
  `project/` if the code is here
- `Showcase:` your showcase pull request's URL

## Grading

| criterion                                                                                      | share |
| ---------------------------------------------------------------------------------------------- | ----- |
| the base is in place at the commit `ROUNDS.md` names: for an extension, the problem set's work copied and deployed where required; for a new project, the base bar above | 20%   |
| `SUBMIT.md`, a public repository for a workflow, and the showcase pull request with its fields right | 10%   |
| round 1: spec and plan committed after the base, implementing commits, a new feature that counts | 20%   |
| round 2: the same                                                                              | 20%   |
| each round's own-words parts are concrete and attested                                         | 10%   |
| the report, or for a deployed project the README, says what each round added and where to see it; a report also covers the five design decisions with pinned deep links | 10%   |
| **inspiration:** something that wows the instructor                                            | 10%   |

**"Counts" is judged against the original problem set's requirements**, or the base for a new
project, read beside the round's changes. A round that is a bug fix, catch-up or deployment
earns nothing for its row.

**Not graded:** feature size, code quality, and how well the own-words parts or the report are
written. "Concrete" is the only bar on the own-words parts: "adds a weekly email digest of new
postings" meets it; "made it better" does not. "Why next" is judged generously.

**Inspiration is a holistic call, with no rubric.** Ambition, polish, a genuinely useful tool or
a surprising idea might earn it, but none of them is a promise. The other 90% does not depend on
it.

## Submitting

Commit as you go, in both repositories. Push both to GitHub before you submit on Canvas. On
Canvas, submit the URL of your assignments repository. The grader will grade whatever is on
`main` in both repositories when it runs, and for a deployed project, the site as it is then.

Due **Wed Dec 9, 11:59 PM**.
