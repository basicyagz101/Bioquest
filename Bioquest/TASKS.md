# Bioquest feedback task list

**Implementation status as of November 2026.** A code-level check is not a substitute for a student playtest in a browser. See `TESTING.md`.

| Peer feedback / requirement | Status | Notes |
| --- | --- | --- |
| Game player walks through buildings and water | Implemented in code — browser testing pending | Editable shapes for water, buildings and fountain; paths enforce map boundaries. |
| Player strays off paths | Implemented in code — browser testing pending | Movement constrained to walkable routes. |
| Team HQ won't interact | Implemented in code — browser testing pending | Approach marked entrance, press E to open Team HQ dialogue. |
| Main Research Center doesn't respond | Implemented in code — browser testing pending | Approach marked entrance, press E for research overview dialogue. |
| Map is not centered | Implemented in code — browser testing pending | Replaced incorrectly stretched raster with vector boundary map, centered in responsive canvas. |
| Explain map letter markers | Implemented in code — browser testing pending | Number badges now show matching opportunity counts; legend explains them. |
| Filter selections should be intersection / AND | Implemented in code — browser testing pending | Matches every checkbox selection. Selecting mutually exclusive categories yields no results. |
| Click counties and show opportunities without losing map | Implemented in code — browser testing pending | Interactive 21-county shapes with adjacent results panel. |
| Career/path bar has no function | Partial / verify tester intent | Made the career pathway on result screens a clickable step-by-step display; confirm whether the feedback referred to another UI element. |
| Add imagery and visual details | Partially addressed | Reused campus pixel-art artwork in Home card and improved decoration. No new original illustrations added. |
| CSS and presentation polish | Implemented in code — browser testing pending | Five-color palette, consistent borders/buttons/cards, map layout, mobile stacking and focus styling. |
| Preserve quizzes, Team Builder and music | Checked at source/runtime-stub level | Quizzes are byte-for-byte unchanged; music retains continuity between Game and Map. |

## Team contribution areas (as provided)

- Matthew — game and map
- Leah — style and logo
- Natalie — sprite art
- Aditya — quizzes for the game

This table lists assigned areas, not a claim that any team member individually implemented the changes in this ZIP.

## Pending QA

- Walk every path and entrance in a real browser; fine-tune collision shapes if they don't match the artwork precisely.
- Check the responsive mobile layout in actual browsers/devices.
- Verify any opportunity listing with the organization before describing it as currently open.
- Clarify what the tester meant by “path bar” if it was not the career-pathway result display.
