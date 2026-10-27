# NEET 2027 CBT package changes

- Added a live countdown targeting 2 May 2027 (midnight IST) to the homepage.
- Added an AIIMS Rishikesh campus image with Wikimedia Commons attribution.
- Added Student Result History link and `student-dashboard.html`.
- Added mark-for-review and clear-response controls to BTS-01/02/03 CBT pages.
- The exam timer starts only after a student signs in.
- Results save to browser LocalStorage and attempt cloud sync to Supabase.
- Attempt numbers are sequential per student and test; result screen shows previous attempt and mark change where scored.
- BTS-03 does not include a verified answer key in the supplied files, so its marks/correct/wrong counts are intentionally not invented.

## Required before cloud sync works
Run `supabase_setup.sql` in the matching Supabase project's SQL Editor, then test sign-up, email confirmation (if enabled), sign-in, and submission. If the configured project URL/key are not yours, replace them with your own Supabase project URL and publishable/anon key. Never put a service-role key in browser HTML.
