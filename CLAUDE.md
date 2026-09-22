# CLAUDE.md —bubblink

Bubblink turns photographed handwriting —a whiteboard, a window, paper— into a
structured digital form of the writing: overlapping shots go in; the stitched
stroke skeleton comes out, ready to be restyled and rendered. Work is
AI-assisted but hand-driven: Jonatan writes a deliberate prompt, you carry it
out.


## Map

- `CLAUDE.md` —this file; the repo's workflow and conventions.
- `README.md` —the repo's public face; short, and points to the journal.
- `docs/approach.md` —the research journal: the ideas behind the tool, told
  milestone by milestone for the reader who enjoys the solution-telling more
  than the source code.
- `milestones.md` —the evolving milestone list; Jonatan's to maintain. Leave it
  untouched unless he tells you to change it.
- `prompts/` —full session logs, `sessionNNNN.log`, every turn verbatim.
- `datasets/` —the photo sets that drive development; one folder per written
  sentence, shot as a row of overlapping pictures at roughly constant distance.


## Sessions and `prompts/`

A new session begins whenever Jonatan starts a fresh conversation here.

- **First prompt of a session:** after reading this `CLAUDE.md`, open a new
  `prompts/sessionNNNN.log` with the next unused 4-digit counter, counting from 0000.
- **Logging a turn:**
  1. `Jonatan on YYYY-MM-DD at ~HH:MM:` + the **full prompt, verbatim**.
  2. One blank line.
  3. `Claude <model> on YYYY-MM-DD at ~HH:MM:` + the **full final answer,
     verbatim**, where `<model>` is whichever model actually produced the turn.

  Two blank lines between turns; append every later turn of the session to the
  same file. Times are approximate, the date reliable.


## Documentation stays in the present

The repo's memory is git; documents are not to become logs of themselves. Docs
and code comments describe the project **as it is now**: when something
consciously changes, rewrite the passage as if the new way had always been the
way —no "previously", no "this used to", no deprecation trails. Rule of thumb:
a sentence that does not relate to the current state of the project is probably
bloat. The one exception is `docs/approach.md`, whose whole point is to narrate
the path —there, the past is content, not clutter.

The same goes for structure: no files, folders or scaffolding before something
real needs them.


## Git

Versioning is Jonatan's: commits are how he marks development breakpoints. Use
git in **read mode only** (`status`, `diff`, `log`, `show`) —never stage,
commit, branch, revert, or otherwise alter history.


## Installing software

Prompts run with CC in auto mode, so you may install software when a prompt
genuinely needs it —no need to ask first. But install it **system-wide** (on
`PATH`, under a standard prefix), never into a private per-tool location only
you would know to look in. If a system-wide install needs sudo or otherwise
can't be done from here, stop and tell Jonatan the exact command to run it
himself.


## Code style

- Comments express *intent* —short, verb-led statements of what the next code
  does. Use them sparingly; if the code reads itself, leave it alone.
- One-line comments take no trailing period. Inline comments are lightly padded
  from the code, not so much that their line becomes unclear.
- No defensive coding when it hurts readability —prefer loud failure to silent
  guards, unless the guard genuinely reduces security exposure.
- **Em dashes, Jonatan's convention** —it governs everything written for the
  repo (docs, journal, code comments), not chat answers. No space on the inside
  of what the dashes enclose: `word —enclosed— word`, and `word —enclosed. Next
  sentence` where a stop closes the aside instead of a second dash. A spaced em
  dash stays only where nothing is enclosed, as in a range: `2021 — 2025`.
