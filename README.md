# bubblink

Write something —on a whiteboard, a window, a sheet of paper. Photograph it in
overlapping pieces. Bubblink stitches the pieces together, detects the strokes,
and hands your writing back as a structured digital object: not a flat scan,
but the skeleton of what you wrote —placement, color, and the path the pen
took— ready to be restyled and rendered into whatever visual you are after.

The name folds the ingredients together: a Babel-sounding wink, the *bubbles*
the detection method grows inside each pen trace, the *link*s that chain them
into a skeleton, and the *ink* it all comes from.


## How it will work

Two programs, chained:

1. **Detect** —point it at a folder of photos taken at roughly the same
   distance; it finds the pen strokes in each shot, matches the overlaps, and
   composes the full writing into bubblink's text form: each word's relative
   placement, its color, and its bubble skeleton.
2. **Style** —load a digitized writing next to a control box of knobs; play
   until it pleases the eye, then export the result (image, SVG, …).


## Status

Early days. The repo holds the founding datasets —three sentences from the
original whiteboard, each shot as a row of overlapping photos— and the
project's working documents. Code comes next.


## The journal

The interesting part of this project is not the code but the ideas —how an
innocent-looking problem gets broken into pieces, and what it takes to defeat
each piece. That story is told, milestone by milestone, in
[docs/approach.md](docs/approach.md): an informal research journal, written to
be readable without the technical counterpart, and unafraid of the occasional
math idea —those are the stars of the show.


## Layout

- `datasets/` —photo sets driving development, one folder per written sentence.
- `docs/approach.md` —the research journal.
- `milestones.md` —where the project is headed next.
- `prompts/` —verbatim logs of the AI-assisted sessions that build the repo.


## License

[MIT](LICENSE).
