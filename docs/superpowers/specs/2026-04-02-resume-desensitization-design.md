# Resume Desensitization Design

## Goal

For the current HTML resume project, make the minimum necessary changes to:

1. Desensitize personally identifiable and directly attributable content in the existing resume HTML.
2. Add a `README.md` that explains how to edit and export the resume independently.

## Confirmed Scope

The user explicitly confirmed the following:

- Keep the existing HTML structure and current layout direction.
- Do not rewrite project descriptions.
- Do not redesign styling or add visual enhancements.
- Add a `README.md`.

## Files In Scope

- `简历_gpt.html`
- `README.md`

## Desensitization Rules

Replace the following content with `XXXXX` in `简历_gpt.html`:

- Name
- Phone number
- Email address
- School names
- Award names
- Project names

Keep the following content unchanged:

- Technical stack names
- Generic technical concepts
- Existing project responsibility descriptions
- Dates, locations, and layout structure

## HTML Change Strategy

Apply surgical content-only changes:

- Replace visible identifying strings in the title and page body.
- Keep CSS unchanged unless required for content fit after replacement.
- Preserve one-page A4 intent by avoiding structural expansion.

## README Strategy

Create a short operational README that explains:

- What this project is
- Which sections in the HTML are intended for manual edits
- How to replace personal information, education, awards, skills, and projects
- How to open the file locally in a browser
- How to export or print to A4 PDF

Tone should be practical and formal. It should reflect the user's intent that this is an HTML + GPT collaborative resume template and does not depend on Word-style layout editing.

## Non-Goals

- Rewriting project bullets using STAR
- Editing technology descriptions
- Introducing build tools, frameworks, or scripts
- Splitting the resume into multiple files

## Risks

- Some identifying information may remain if not directly visible in the main content.
- Replacing short labels with repeated `XXXXX` can slightly reduce readability, but this is acceptable for the desensitized version.

## Acceptance Criteria

Implementation is complete when:

1. `简历_gpt.html` no longer exposes the user's real name, phone, email, school names, award names, or project names.
2. Technical stack and responsibility text remain intact.
3. `README.md` exists and clearly explains how to edit and export the resume.
4. No unnecessary style or structure changes are introduced.
