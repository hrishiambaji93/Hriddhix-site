# Hriddhix Studio Website

This package contains the full static website (`index.html` + `assets/`).
It's a single-page site — just open `index.html` in a browser, or upload
the whole folder to any static host.

## Folder structure

```
index.html          → the entire site (HTML, CSS, and JS in one file)
assets/images/       → logos, photos, icons
assets/videos/       → portfolio video clips
assets/fonts/        → custom typefaces used across the site
```

## Changes made in this round

**1. Review/testimonial card hover**
Fixed a clipping bug where the top border and corners of a "Trusted By"
review card got cut off as it lifted on hover. The card now has enough
room to lift smoothly with its border fully visible — the hover
animation itself is unchanged.

**2. Portfolio page logo**
On the Portfolio page, the wide Wordmark logo (top-left) was replaced
with the compact Lettermark (the "H" icon), matching how the main
header handles its logo.
⚠️ Note: this still has a visual issue — the mark currently renders
faint against the Portfolio bar's background instead of a crisp dark
mark. It needs one more fix before it matches the main header exactly.

**3. Category hover color**
On the Services section, hovering over a service card (Design &
Branding, Video Editing & Motion Graphics, Social Media Marketing,
Print Design, Video Production) used to turn its icon patch white.
It now turns the brand cream color (`#E5DAD1`) instead.

## Housekeeping done on this package

- **Videos compressed** — the 9 portfolio video clips were re-encoded
  (downscaled, lower bitrate) to shrink the overall download size.
  Quality is slightly reduced from the original source videos.
- **Unused files removed** — 28 image files that weren't referenced
  anywhere in the site were deleted (leftover duplicate logo exports
  and a couple of unused client logos). Nothing that appears on the
  live site was touched.

## Still open

- Item 2 above (Portfolio Lettermark contrast) needs a follow-up fix.
