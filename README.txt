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

- pdf-to-cbt.html: PDF-to-CBT admin tool. Upload a question PDF and optional answer-key PDF, extract text with PDF.js, optionally OCR scanned pages, review/edit questions/options/answers, then download a generated CBT HTML file.

PDF-TO-CBT NOTES:
1. Open pdf-to-cbt.html from the deployed website. Internet is needed for PDF.js and optional Tesseract OCR.
2. Upload the question PDF and, if separate, the answer-key PDF. Review every extracted question and answer before generating.
3. This tool is a best-effort parser. It cannot guarantee exact extraction for all layouts; diagrams and images are not embedded in the generated CBT. Manually correct missing content and answer keys.
4. Downloaded CBT files are not automatically pushed to GitHub. To make a new test available to all students, upload the downloaded HTML file to the repository, add a link to index.html, and redeploy Vercel. Drafts saved in LocalStorage exist only in that browser.
5. The generated CBT uses the project's configured Supabase project/key for optional cloud result sync after student sign-in. Verify the project is yours and run supabase_setup.sql before use. Never expose a service_role key.
