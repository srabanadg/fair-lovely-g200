# Fair & Lovely Studio | Marketing Management (BUS 702 G200)

## Open the Studio

- **[Instructor Studio](https://srabanadg.github.io/fair-lovely-g200/instructor-g200.html)** — for the instructor; use your authorized Firebase email/password login.
- **[Student Studio](https://srabanadg.github.io/fair-lovely-g200/student.html)** — the link to share with students.

These are the **G200** links. The separate [original Fair & Lovely Studio repository](https://github.com/srabanadg/fair-lovely-studio) remains available for the online course.

## What the G200 Studio includes

- **Activity 1:** Live beauty-trends word cloud, with up to three short responses per student.
- **Activity 2:** Before-and-after votes on whether Fair & Lovely should be discontinued.
- **Activities 3–6:** Kept in the instructor interface; hidden from students by default for whiteboard discussion.
- **Activity 7:** Five-team brand repositioning and three-scene storyboard exercise. The product formulation must remain unchanged. Includes class campaign ratings for commercial effectiveness and social responsibility.

The instructor can control student activity access, student visibility, and resets.

## Where to make updates

1. Use the [G200 GitHub repository](https://github.com/srabanadg/fair-lovely-g200) (not the original `fair-lovely-studio` repository).
2. The published instructor page is **`instructor-g200.html`**. It is **not** the repository's default `index.html` page.
3. Upload replacement files into the **root** of the G200 repository on the `main` branch, then **Commit changes**.
4. GitHub Pages serves the site from the `main` branch, `/ (root)`. After a successful deployment, refresh the page to see the changes.

## Firebase notes

- The G200 Studio uses the existing Fair & Lovely Firebase project but a **separate database session path**: `gdba-fair-lovely-g200-2026`. This is an internal identifier, **not a visible course header**, and should not be renamed without updating the application and database rules together.
- Instructor authentication uses **Firebase Email/Password**. The authorized instructor UID is configured in `config.js` and permitted in the Firebase Realtime Database rules.
- Student sessions use anonymous Firebase authentication. Students should only receive the Student Studio link.
- The two courses' database rules are shared within the Firebase project; preserve permissions for the original online course when editing rules.

## Notes

- Team submissions are linked to the first anonymous account to submit for each team until reset.
- Student responses are anonymous to the instructor, but anonymous sign-in does not guarantee one response per person.
- Instructor notes are stored locally in the instructor browser. Use **Export notes** to back them up.
