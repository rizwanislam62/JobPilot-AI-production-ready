# JobPilot AI - Cloud & DevOps Career Copilot

Single-file web app (`index.html`, no build step) for a job search in Norway and the Netherlands.

## What it does
- Profile and master CV, all editable; unverified metrics stay out of generated documents until ticked as verified.
- Add jobs by pasting the description and URL; duplicate detection by URL and by company plus title.
- Match score (0-100, editable weights) with evidence, gaps, mandatory vs preferred requirements, language and work-authorization checks. A confirmed mandatory barrier caps the score at 49; an unconfirmed one caps it at 74.
- Tailored CV with side-by-side comparison, per-section editing, validation checklist and explicit approval before a version is saved.
- Cover letter, email, LinkedIn message, motivation statement and interview prep, all built from profile facts.
- Application tracker with statuses, filters, follow-up dates, JSON/CSV export and import, .txt/.docx download.

## Limits
- Data is stored in the browser (`localStorage`) only. Use Export regularly.
- No live job search, scheduler or email sending is connected. Nothing is applied for or sent automatically.
- Claude-assisted actions (second opinion, wording polish, translation) appear only when the page runs inside a Claude artifact with the `sample` capability.

## Roadmap
See Settings > Roadmap and integrations inside the app (live discovery, database plus DOCX/PDF backend, scheduler and reminders).

## Importing search results
`data/indeed-shortlist-2026-10-08.json` holds 10 postings found through an Indeed connector search (DevOps, cloud and platform roles in Oslo and Amsterdam/Utrecht). Paste the file into Find Jobs > "Import results from an external search service". Items arrive marked "Imported, unverified" until you confirm each one at its original URL. Several postings were published months ago and may be closed.
