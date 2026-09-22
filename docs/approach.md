# The approach

*This is bubblink's research journal —the record of a problem being taken
apart, written around the interesting bits: the ideas needed to unlock each
step, and the advances as the tool takes shape. It is meant to be readable
without the technical counterpart, though it will not shy away from the
occasional math idea —those are the stars of the show. Each section
corresponds to a milestone of the project; new sections appear as milestones
fall.*


## 1. A whiteboard too good to erase

Every so often a thinking session leaves my whiteboard in a state I am
reluctant to destroy. The board is full, the session is over, and the only way
to keep working is to erase —which feels like sweeping the dust under the
carpet. I wanted to digitize the board before clearing it, and my phone alone
was not up to it: a single photo far enough to fit the whole board smears the
strokes, while photos close enough to keep them only ever hold a piece. The
natural move is to take a row of overlapping close shots and stitch them. I
tried a couple of open-source stitchers and the results did not motivate a
third attempt —understandably, since a general-purpose stitcher knows nothing
about what makes this scene special. That became the founding observation:
this scene *is* special, and its structure is there to be exploited.

A photographed whiteboard is very nearly a picture of nothing: a background in
one color, and strokes from a handful of pens. That poverty is a gift. It
invites a different ambition than stitching pixels into a larger picture of
pixels —we can aim to extract the *writing itself*. For every word: where it
sits relative to the others, what color it is drawn in, and, the delicate
part, the path the pen took when it was written. The idea the project is named
after lives in that last part: grow circles —bubbles— inside a pen trace, each
as large as the trace allows, each tangent to the one before, and let the
chain of their centers trace out the skeleton of the stroke. A written word
stops being a patch of pixels and becomes a small geometric object —a graph of
linked bubbles.

Once the writing exists in that form, saving the board is only half of what
the tool can do. A skeleton can be re-inked: thickened, recolored, made to
glow, rendered into an SVG —made to look like almost anything while remaining
recognizably *your* handwriting. That second half turns a board-saving chore
into something better: a way to port things written by hand —on a whiteboard,
a window, paper— into digital assets. It is also the half that a longer-running
project of mine has been quietly waiting for.

So here is the plan, and the definition of "stable" I am holding the project
to. Write something on the board. Photograph it in overlapping pieces at
roughly the same distance —a mild restriction on the photographer that buys
the mathematician a lot of containment. Drop the photos in a folder and run a
detecting program that digitizes the writing; there is real computation in
there, so this step is allowed to take its time. Then run a styling program:
the digitized writing on one side, a control box of knobs on the other, and
play until it pleases the eye. Export, done.

The repo opens with three datasets —three sentences that are on my board right
now, each photographed as a row of overlapping shots. They will drive the
early stages. The project will advance through an evolving sequence of
milestones, at whatever pace the final stretch of a PhD allows; I chose this
problem precisely because it breaks into bite-sized pieces, each worth a visit
on its own. This journal grows one section per milestone, and the first
milestone is the humblest of them: set up a repo worth coming back to —the
workflows, the conventions, and this very document. You are reading its
closing act.
