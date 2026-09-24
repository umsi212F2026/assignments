# Problem Set 2: React App with SQL Backend

## What you are doing

**Design and build a React app of your own choosing, with a server and a SQL database behind
it.** It runs on your laptop. Nothing is deployed and nothing is public. Problem Set 3 deploys
this same app, so build something you are willing to live with for a month.

You pick what the app is. That is the assignment, and it is the part nobody can do for you.

## How big

**At least the size of the app you built in Thursday's lab**, which is a floor rather than a
target. Stated so it can be checked, an app clears the floor when all three of these are true:

1. **Somebody can put data in, change it, and remove it.** All three, not just adding.
2. **Something else in the app reads that data back** and does something with it that is not
   just listing it.
3. **Something the app records about what the user did survives a restart.** Not just the data
   they typed in: something the app itself noticed and wrote down.

The lab app clears it: an editor that adds, changes and deletes acronyms, a learner mode that
shows them one at a time and checks what you type, and scores that are still there tomorrow.
Yours will look nothing like that, and it still has to clear all three.

**Your schema needs at least two tables with a relationship between them.** One table is a list,
and a list does not have a design worth reviewing. Two related tables is where schema decisions
start.

## The stack

React on the front, a Node server in the middle, a SQL database at the back. All three on
localhost.

**Use SQLite unless you have a reason not to.** It is the one the backends topic worked
through, and it is a file, so there is nothing to install and nothing to start. Anything else
is fine if the whole app still comes up with one command.

## The two things that are fixed

Everything else about how you organize this is yours. These two are not, because a program runs
them.

### `npm test` runs your tests, from this folder

Whatever test runner you and your agent pick. The command is what is fixed.

### One of those tests proves the data survives a restart

**The test restarts the server process between writing and reading.** Write something, stop the
server, start it again, read it back, assert it is there.

**It writes and reads through your app's own HTTP API**, not with SQL straight into the database
file. A test that writes with SQL and reads with SQL proves that SQLite works, which nobody
doubted. It tells you nothing about your app.

Both halves matter and the test is worth nothing without either. Without the restart it passes
on an app that saves nothing. Without the API it passes on an app whose server and database work
perfectly and whose React code never talks to them.

You do not need a headless browser for this. It is a Node test making HTTP requests.

### Also, and not checked by a program

`npm start` should bring the whole thing up, server and front end together. Problem Set 3 will
deploy this app and it will start it the same way. Put the command in your `README.md` either
way.

## What you hand in

Everything lives in this folder.

| file                                | what it is                                                          |
| ----------------------------------- | ------------------------------------------------------------------- |
| the app                             | source, organized however you and your agent see fit                 |
| `spec.md`                           | the spec you approved before any code was written                    |
| `README.md`                         | what the app is, how to start it, how to exercise the main features  |
| `REFLECTION.md`                     | five questions, answered by hand. The template is in this folder.    |
| your tests                          | including the restart test above                                     |

**`spec.md` is the spec you approved, not a description written afterwards.** Those read
differently and it is easy to tell them apart. A spec says what the app will do and what was
decided; a write-up says what the app does. Hand in the first one.

## The reflection, and why it is different from last time

Problem Set 1 told you there were no points for process, and meant it. This one marks
`REFLECTION.md`, which looks like a reversal and is not quite one. Those five questions are not
about your process. They are about decisions you made, and the decisions are what the last two
weeks were about.

**Write it by hand. Do not have your agent write it, or draft it, or clean it up.**

Nobody can check how a file got written, and there is no point pretending otherwise. Here is why
it is still worth doing:

**The quiz reads your answers and asks you about them.** Your question is generated from your
own `REFLECTION.md`, so it is yours alone, and you will not have the file in front of you when
it arrives. If you wrote your answers, that question is free. If something else wrote them, you
are being asked to defend a position you have never held.

That is the whole mechanism, and it is aimed at your quiz score rather than at your conscience.

Working through the questions with your agent to figure out *what you think* is fine, the same
as it was for Problem Set 1's `QUESTIONS.md`. Having it produce the answers is the thing that
costs you later.

**There are no marks for length.** A few sentences each. Four of the five ask you to name
something you rejected, something that went wrong, or somewhere you were sloppy, and a long
answer to those is usually an evasive one.

## Grading

Automated, on what you hand in, plus a judge reading your `spec.md`, your schema and your tests.

| criterion                                                                          | share |
| ---------------------------------------------------------------------------------- | ----- |
| `npm test` runs, and the tests pass                                                 | 20%   |
| a test restarts the server and goes through your own API                            | 20%   |
| the app clears all three clauses under **How big**                                  | 25%   |
| schema: two or more related tables, and nothing stored that should be worked out    | 15%   |
| `spec.md` present, and it reads as a spec rather than a write-up                    | 10%   |
| `REFLECTION.md` present, all five answered, answers responsive to what was asked    | 10%   |

**The reflection is marked for being answered, not for what the answer says.** Question 4 asks
where you approved something without reading it. You are not penalized for the answer. You are
penalized for not having one.

**"Nothing stored that should be worked out"** is the one in that table with a trap in it, and
you met the trap on Thursday. A number you can compute from two other numbers should not have a
column. Stored twice means wrong twice, as soon as one copy changes.

## Submitting

Commit as you go, and push. On Canvas, submit the URL of your assignments repository. What gets
graded is whatever is on `main` at the deadline, so work you have not pushed has not been handed
in.

Due **Wed Sep 30, 11:59 PM**.
