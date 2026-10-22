# Resume Match Checker

A private, client-side web app for matching resumes to job descriptions and coaching better bullet points. No installs, no server, no internet needed.

## Run it
Double-click `index.html` (or open it in your browser from VS Code).

## Use it
1. **Upload or paste your resume** on the left and the full job posting on the right:
   - Click **📄 Upload file** to load **PDF**, Word (**`.docx`**), or text files.
   - Or **drag & drop** any file directly into the resume or job description box.
   - Or click **Try a sample** for an instant demo with pre-loaded data.
2. Click **Check my match** (or press `Ctrl + Enter`).
3. **Review your match score and bullet rewrites**:
   - **Bullet Rewrite Suggestions**: Flags weak, passive lines (e.g., *"Responsible for cleaning datasets"*) and generates accomplishment-focused versions (e.g., *"Cleaned and validated datasets to..., with blanks for your results"*). Click **⚡ Apply to resume** to update your resume in one click or **📋 Copy suggestion**.
   - **Keyword Match**: Identifies matching and missing skills from the job description with priority levels (required vs. nice-to-have).
   - **Resume Health Check**: Verifies contact info, section headers, word count, action verbs, and quantifiable metrics.
   - **Highlighted Job Posting**: Visualizes covered vs. missing terms directly on the job description.
4. **Export your report**:
   - **Download PDF report** opens the print window (choose **Save as PDF**).
   - **Copy summary** copies a clean text breakdown to your clipboard.

Test files are included in the folder:
- `sample_resume.pdf`
- `sample_resume.docx`
- `sample_resume.txt`
- `sample_job_description.txt`

## How the score works
- **Keyword match (75%)**: Skills found in the job description (from a built-in dictionary of over 330 skills with aliases, e.g. JS = JavaScript) plus repeated key terms. Skills under "Requirements" or repeated multiple times carry higher weight; "nice to have" skills carry lower weight.
- **Experience (15%)**: Years requested in the job vs. years calculated from work dates on your resume.
- **Education (10%)**: Degree level requested vs. the highest degree found on your resume.

## Bullet Rewrite Coach (The Google XYZ Formula)
The app teaches you to elevate passive task descriptions into quantified achievements using Google's proven formula:
> **Accomplished [X], as measured by [Y], by doing [Z]**

- Upgrades passive starters like *"Responsible for..."*, *"Worked on..."*, or *"Helped with..."* into strong action verbs (*Cleaned*, *Architected*, *Spearheaded*, *Automated*).
- Inserts context-specific placeholders for numbers (percentages, time saved, team size, query latency, revenue).

## Privacy & Offline Use
- **100% In-Browser**: All text parsing, PDF extraction, Word document extraction, and keyword scoring run locally in JavaScript.
- **Offline Ready**: Includes standalone reader libraries in `lib/` (`pdf.min.js`, `pdf.worker.min.js`, `mammoth.browser.min.js`), with CDN fallbacks if moved.
- Your resume and job description never leave your computer and are never saved to any external server.
