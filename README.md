# Fair & Lovely Studio: BUS 702 G200

This is a separate copy of the original studio. The original GitHub repository is unchanged.

## Studio links

- **[Instructor Studio](https://srabanadg.github.io/fair-lovely-g200/)**
- **[Student Studio](https://srabanadg.github.io/fair-lovely-g200/student.html)**

Both links are published from this repository with GitHub Pages. Share only the **Student Studio** link with students. Instructor controls require authorized Firebase sign-in.

## What's new
- Instructor retains all seven activities. Activities 3–6 default to hidden in the student interface, and instructor can toggle visibility.
- Activity 1: live student word cloud (up to 3 trends, anonymous to instructor).
- Activity 2: before-and-after voting (Yes, No, Undecided) with side-by-side comparison.
- Activity 7: five teams, product formulation fixed, strategy/brand/storyboard, and individual two-dimensional peer ratings. No Zoom instructions.
- Reset buttons require authorized instructor login.

## REQUIRED setup before live use
1. Create a **new GitHub repository** (for example `fair-lovely-g200`) and upload these files to its root; enable Settings > Pages > Deploy from branch > main / root. The URLs will be your repo root (`index.html`, instructor) and `student.html` (students).
2. This copy uses the EXISTING Firebase project but a DIFFERENT session path `gdba-fair-lovely-g200-2026` to keep data separate. Firebase Realtime Database rules are project-wide. **Do not replace your whole existing Firebase rules with this file without merging the existing session rules**, or the online-class version may stop working.
3. In Firebase Authentication > Sign-in method, enable Google and Anonymous providers. In Authentication > Settings > Authorized domains, add your new GitHub Pages hostname.
4. Open the instructor page, click Instructor sign-in, sign in with Google, and copy the UID displayed. Replace `REPLACE_WITH_YOUR_FIREBASE_GOOGLE_UID` in BOTH `config.js` and `database.rules.json` with that same UID, then upload the changed `config.js` to GitHub.
5. Merge the `sessions.gdba-fair-lovely-g200-2026` rules node into your EXISTING Firebase Realtime Database rules (preserving other sessions), then Publish. Do not use a broad rule granting students write permission to the session root.
6. Open the published instructor link and a student link in separate browsers. Use the instructor buttons to open each round; check live updates, both votes, cloud, five team submissions, ratings, visibility, and reset.

## Important
- If you only open the files locally, Firebase authentication may fail; use HTTPS hosting.
- Team submissions use a first-scribe lock: the first person submitting for a team owns subsequent edits from the same browser/account. Instructor can reset all teams. Anonymous auth is not a guarantee of one vote per actual student; use for low-stakes participation only.
- Peer ratings are anonymous to instructor but team choice is self-reported; they are not intended for graded assessment.
- Visibility controls hide activity access; the instructor still has all seven pages. Public student authentication does not prevent visitors with the URL from signing in.
- Notes are saved locally to the instructor's browser, not Firebase. Use Export notes to back them up.
