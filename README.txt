NEET 2027 CBT + STUDENT HISTORY UPDATE PACKAGE

Files:
- index.html: homepage, AIIMS Rishikesh photo, live countdown to 2 May 2027, existing test/question-bank links, Student Result History link.
- BTS-01_NEET_2027_CBT.html / BTS-02_NEET_2027_CBT.html / BTS-03_NEET_2027_CBT.html: CBT pages with timer, palette, clear response, mark for review, auto-submit, per-student attempt numbering, LocalStorage history, Supabase sync attempt, and result comparison panel.
- student-dashboard.html: sign-in page and cross-attempt result history/comparison dashboard.
- supabase_setup.sql: table and row-level security setup for Supabase.
- NEET_Question_Bank_Generator_25901.html + questions.json: existing question bank generator and question data.
- NEET_40K_Custom_Question_Bank_Generator.html: existing 40K generator entry page.

IMPORTANT SETUP:
1. Open supabase_setup.sql and run it once in Supabase Dashboard > SQL Editor for the same Supabase project configured in the BTS files.
2. Confirm the Supabase project URL and publishable/anon key in the CBT files belong to your own project. Never put a service_role key in browser code.
3. Supabase Auth email sign-up/sign-in must be enabled. If email confirmation is enabled, students must confirm their email before signing in.
4. Supabase saves cloud history only after the SQL schema and RLS policies are installed. LocalStorage saves on the same browser/device even if cloud sync fails.
5. BTS-03 has no answer key in the supplied source, so it records attempt/answer details but deliberately does not invent correct/wrong counts or a score for that paper. Add a verified key before scoring BTS-03.
6. The countdown target is 2 May 2027 at 00:00 IST. This is the target date supplied by the project owner; check official NTA notices for the final exam schedule.
7. The campus image is loaded from Wikimedia Commons and includes attribution; internet is needed for that image.
8. This package is not deployed to Vercel. Upload/extract the full folder to the correct GitHub repository, then redeploy. Test sign-up, submission, local history and Supabase history before sharing the site.
