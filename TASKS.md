# TASKS.md — Design Team Job Tracker coordination log

This file lets multiple Claude sessions (each run under a separate login) working on this repo/database at the same time avoid stepping on each other. Convention:

- Each session identifies itself as **Claude-LoginA** or **Claude-LoginB** (assigned by Sarah at the start of the session).
- Before making any change, a session pulls the latest `main` branch and re-reads this file to see what the other login has done or is currently doing.
- Before editing a `jobs` row, a session sets `last_edited = now()` and `edited_by = 'Claude-LoginA'` (or `LoginB`) on that row.
- After pushing any code change, the session updates the log below with what changed and what's next, then commits/pushes TASKS.md itself.
- Supabase (project `jeztkwnvfewhnaadaazh`) and this GitHub repo are the single source of truth — always re-check both before proceeding, don't rely on in-conversation memory of prior state.

`jobs` table now has two columns supporting this: `last_edited` (timestamptz) and `edited_by` (text) — added by Claude-LoginA.

---

## Log

### Claude-LoginA — session start
- Set up this coordination convention: added `jobs.last_edited` / `jobs.edited_by` columns in Supabase, created this file.
- Header redesign completed: logo enlarged (34px → 56px height), title restructured into a two-line layout — small gold all-caps "Design Builders Services" eyebrow above the italic serif "Weekly Job Tracking" title (previously a single line "DBS, Weekly Job Tracking" next to a small logo).
- Next: no open task right now — check in with Sarah for what's next.
