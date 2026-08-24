# Repository Context for AI Agents

Read this file before making any changes to this repository. It is the single source of truth for structure, conventions, and current academic status.

---

## What This Repository Is

An academic portfolio for Samuel Stidham's Computer Science education at Southern New Hampshire University (SNHU). It tracks coursework, grades, and reflections across the Bachelor of Science and the planned Master of Science in Computer Science.

**Academic integrity note:** This is a public portfolio. Specific assignment solutions, code submissions, or graded work are never included, in keeping with SNHU's academic integrity policy. Do not add them.

---

## Repository Structure

```text
README.md          ← Landing page / index. Links to both degree program pages.
bachelors.md       ← Full BS program: course list, grades, and schedule.
masters.md         ← MS program placeholder (to be populated starting ~2028).
docs/
  2025/            ← Year 1 completed courses
  2026/            ← Year 2 courses (completed, in-progress, and planned)
  2027/            ← Year 3 courses (all planned, per advisor schedule)
  course-template.md           ← Template for completed courses
  upcoming-course-template.md  ← Template for planned/in-progress courses
.agents/
  core.md          ← This file
```

---

## File Naming Convention

Course files follow a strict sequential numbering scheme reflecting chronological order:

```text
docs/<year>/<##> - <COURSECODE>.md
```

Example: `docs/2026/08 - CS210.md`

- Numbers start at `01` and increment by 1 for each course taken
- Numbers are never reused or skipped
- The next available number is **29**
- The year folder reflects the calendar year the course is taken, not the academic year

---

## Status System (used in bachelors.md and course lists)

| Symbol | Meaning |
| --- | --- |
| ✅ | Completed (final grade received) |
| ⏳ | Upcoming or In Progress |

The `bachelors.md` grade-table Status column uses only these values: "Planned (<term dates>)", "Up Next (<term dates>)" once registration is confirmed, "In Progress (<term dates>)", "Grade Pending", and "Completed".

Back links in all course files use:

```markdown
[← Back to Central Portfolio](../../bachelors.md)
```

---

## Current Degree Status (as of August 2026)

| Field | Value |
| --- | --- |
| Program | Bachelor of Science in Computer Science |
| Concentration | None (dropped to maximize transfer credit application) |
| Minor | Mathematics |
| Overall GPA | 4.000 |
| Credits Applied | 75 / 120 (includes completed, in-progress, and pre-registered) |
| Credits Remaining | 45 |
| Projected Graduation | December 2027 |

---

## Advisor-Confirmed Course Schedule

| Term | Dates | Courses |
| --- | --- | --- |
| 2026 C-3 | May–Jun 2026 | CS-210, PHY-150 *(Completed)* |
| 2026 C-4 | Jun–Aug 2026 | MAT-230, CS-250 *(Completed)* |
| 2026 C-5 | Aug–Oct 2026 | CS-300, DAD-220 *(In Progress)* |
| 2026 C-6 | Oct–Dec 2026 | CS-230, CS-305, MAT-350 |
| 2027 C-1 | Jan–Feb 2027 | CS-255, MAT-299 |
| 2027 C-2 | Mar–Apr 2027 | CS-320, MAT-415 |
| 2027 C-3 | May–Jun 2027 | CS-330, IDS-410 |
| 2027 C-4 | Jun–Aug 2027 | CS-340, MAT-243 |
| 2027 C-5 | Aug–Oct 2027 | CS-465, CS-360 |
| 2027 C-6 | Oct–Dec 2027 | CS-499, CS-370 |

CS-320 → CS-340 → CS-465 → CS-499 are locked prerequisite chains. Do not reorder them.

When a term's courses sit in different states, mark each course in the row individually instead of tagging the whole term.

---

## Content Conventions

- Never name Samuel's employers, past or present, in any file. Refer to roles anonymously, for example "a Senior Software Engineer."
- Write all mathematical notation as inline LaTeX (`$...$`), not Unicode symbols. GitHub renders it natively.
- No peer names or quoted peer content in discussion summaries. Characterize a peer's position only as needed to frame Samuel's response.
- Stub unwritten sections with the exact phrase `*To be documented as the course progresses.*` so stale stubs stay greppable. Write any interim promise sentence to end with "as the course progresses" too, so one grep finds everything.

---

## Course File Formats

The template files in `docs/` are the single source of structure. Do not restate their section lists here.

- **Upcoming courses:** copy `docs/upcoming-course-template.md` and fill in the header table and catalog description.
- **In-progress courses:** keep the upcoming header with Status set to "In Progress". Add the full section scaffold from `docs/course-template.md`, spliced before the closing back link. Stub unwritten parts with the standard placeholder phrase.
- **Completed courses:** follow `docs/course-template.md`. Its header uses `**Term Taken**` and `**Final Grade**` in place of `**Planned Term**` and `**Status**`.

Both templates carry blockquote template notes for conditional structure, such as the math-course discussion rule. Remove every template note when instantiating a real course file. Course files never include actual assignment solutions.

---

## How to Update This Repository

| Event | Action |
| --- | --- |
| Course starts | Set "In Progress" in the course file, the `bachelors.md` table and Next Steps entry, and the schedule table above. Scaffold the course file with the full section structure. |
| Course completes | Swap the file header to Term Taken and Final Grade. Sweep remaining placeholders. Record the grade and set the `bachelors.md` table row to Completed. Flip ⏳ to ✅ in the course lists and mark the Next Steps entry *(Completed)*. Update the schedule table above. Refresh the Current Degree Status table's date and credits. |
| New course registered | Create the file from `upcoming-course-template.md` and assign the next sequential number. Add the course to the `bachelors.md` table, course lists, and Next Steps list, and to the schedule table above. |
| Degree status changes | Update the Current Degree Status table in this file and the Degree Path Overview lines in `bachelors.md`. |
| MS program begins | Populate `masters.md` following the same structure as `bachelors.md`. Add `docs/2028/` (or the relevant year). |
