Hriddhix Studio Website
This package contains the full static website (`index.html` + `assets/`).
It's a single-page site — just open `index.html` in a browser, or upload
the whole folder to any static host.
Folder structure
```
index.html          → the entire site (HTML, CSS, and JS in one file)
assets/images/       → logos, photos, icons
assets/videos/       → portfolio video clips
assets/fonts/        → custom typefaces used across the site
```
Latest round: production repositioning
Overview, scrolling ticker (7 production terms, seamless loop), About Us, Why Hriddhix, Our Process (5 steps) and Contact copy updated for a creative production studio.
What We Do now has three cards: Pre-Production, Production, Post-Production.
Portfolio now shows a single category, "Post Production" (the motion poster, motion graphics and video editing videos, with their credits). The old tabs (All, Design and Branding, Video Editing & Motion Graphics, Print), sub-tabs and their content/scripts were removed.
Testimonials: logos, quotes, names and roles replaced with LOREM IPSUM placeholders (all 10 cards, including the loop duplicates); marquee, hover-pause and card design unchanged.
Post Production: all videos, thumbnails and credit lines removed (heading only remains); unused client-logo, video and thumbnail files deleted from /assets.
Section order, links, Clients Trusted By and portfolio items unchanged.
Changes made in this round
1. Portfolio credits visibility (proper layout/container fix)
Some projects were only showing the first credit line (`CREATED BY`),
with `WORKED FOR`/`CLIENT`, `PROJECT`, and `ROLE` hidden or clipped.
Root fix, at the container level:
Every project's credits now live inside a `.pc-inner` wrapper, and
the collapsible panel around it is a CSS grid that animates between
`grid-template-rows: 0fr` (closed) and `1fr` (open) instead of a
JS-measured pixel `max-height`.
A `1fr` row in a single-row grid sizes itself to its real content
height automatically, on every reflow (image loading, font
swapping, window resizing) — nothing is ever measured-and-frozen,
so nothing can get cut off.
The old JS scroll-height measuring, resize listeners, and
image/font "re-measure" workarounds are gone — no longer needed,
since layout now keeps every panel sized correctly on its own.
Added a small bottom padding inside the panel as extra breathing
room below the final `ROLE` line.
Verified against every project's credits block (Poster Design, Brand
Identity, Motion Poster, Motion Graphics, Video Editing, Backdrop
Design, Ticket Design, Newspaper Ads Design, Brochure Design) — all
four lines, ending in `ROLE: PROJECT HEAD`, are fully present with no
clipping, masking, or truncation, on both category panels and their
subsections, on desktop and mobile. Nothing else was changed.
Housekeeping done on this package
Videos compressed — the 9 portfolio video clips were re-encoded
(downscaled, lower bitrate) to shrink the overall download size.
Quality is slightly reduced from the original source videos.
Unused files removed — 28 image files that weren't referenced
anywhere in the site were deleted (leftover duplicate logo exports
and a couple of unused client logos). Nothing that appears on the
live site was touched.
Still open
Portfolio page logo (Item 2, earlier round): still has a visual
issue — the Lettermark currently renders faint against the
Portfolio bar's background instead of a crisp dark mark. Needs a
follow-up fix — not touched in this round.
