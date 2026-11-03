# Git & GitHub portfolio workshop — 4 November 2026
Trainer: Muhammed Sanweer KT | Assumed hours: 9:30 AM–5:00 PM

09:30–10:00 Setup, introductions, show finished portfolio; check git --version.
10:00–10:40 Git vs GitHub; working tree, staging, commits. Demonstrate before students repeat.
10:40–10:55 Break.
10:55–11:40 Lab 1: copy starter, initialise, commit, inspect status/diff/log.
11:40–12:30 Lab 2: personalise portfolio; three meaningful commits.
12:30–13:15 Lunch.
13:15–14:00 Lab 3: empty GitHub repository, authentication, first push.
14:00–14:45 Lab 4: feature branch, pull request, partner review, merge.
14:45–15:00 Break.
15:00–15:35 Trainer conflict overview, portfolio checks and questions.
15:35–16:15 Publish portfolio with GitHub Pages; check mobile layout and links.
16:15–16:45 Student demos and peer feedback.
16:45–17:00 Quiz, recap, exit ticket.

## Before class
Install Git and an editor; create and verify GitHub accounts before arrival. Check browser sign-in and internet/projector access. Share STUDENTS.md with every student. It contains all required portfolio code and commands. Use the PowerShell terminal in VS Code for every command in STUDENTS.md. No package installation is needed for the portfolio. Keep a spare local copy and pair students if setup fails. Open index.html and your original PDF before students enter. Students need only STUDENTS.md; no other handout is required.

## Delivery rhythm
Explain for 5 minutes, demonstrate for 5, practise for 15, then check understanding. Ask students to predict status output before running commands. Use pairs: driver types, navigator checks; swap each lab. Show your terminal in large text. Wait for a visible checkpoint before moving on.

## Checkpoints and timing recovery
By lunch: each student has a local portfolio and 3 commits. By 2:45: pushed branch and reviewed PR. By finish: working page or local demo with documented publishing blocker. If behind, shorten optional theory demonstrations and protect portfolio/demo time. With no internet, complete all local labs and defer remote steps.

## Trainer notes
Use your existing PDF for theory and STUDENTS.md for the practical sequence. Git is version control; GitHub is a hosting and collaboration service. A commit records staged content, not every edit. Identity configuration does not authenticate. Do not promise a fixed Pages deployment time. Never ask students to share tokens or passwords. Choose an email suitable for public commits, or GitHub's account-provided no-reply address.

## Assessment (10 points)
Working responsive portfolio 2; clear personal content 1; three meaningful commits 2; branch and PR 2; live URL or documented blocker 1; explains staging and fetch/pull 2.


## Teach from the portfolio sequence

Use STUDENTS.md as the shared step-by-step plan. All files are created or edited manually through VS Code Explorer. The terminal contains Git commands only; there are no Set-Content, Add-Content or printf commands. Do not configure a global default branch: git init -b main already names this project's initial branch.

| Stage | Student action | Evidence to check |
|---|---|---|
| 1 | Create folder in File Explorer, open in VS Code, configure identity and initialise | Terminal is in my-portfolio; main is initial branch |
| 2 | Manually create README and commit | First commit; clean status |
| 3 | Append learning goal manually; inspect and commit | Understands unstaged versus staged diff |
| 4 | Create index.html using the supplied complete code | Starter page opens; third commit |
| 5 | Replace name and introduction | Heading/title/introduction personalised |
| 6 | Replace biography, skills and email | Five commits; personal page ready |
| 7 | Create empty remote and push | Same files and history appear on GitHub |
| 8 | Change first project description on a branch; merge locally | Old text returns on main before merge; new text returns after merge |
| 9 | Add next card on another branch; PR and merge | Three cards; PR history; local main updated |
| 10 | Enable Pages | Successful deployment and live URL |
| 11 | Change tagline and push | New deployment shows the last edit |

The starter code is the baseline. Every later code change has an exact location, example replacement, save/preview instruction, command block and explanation of the result. Students should complete one stage and its checkpoint before continuing.

## Aligning with the PPT

Stages 1–3 cover PPT 08–15; build and personalise the page in Stages 4–6 as an early preview of PPT 28. Stage 7 covers PPT 17–18, Stage 8 covers PPT 19–20, Stage 9 covers PPT 21–23, Stages 10–11 cover PPT 28 and recap 29–31. Use PPT 01–07 for concepts first. Treat clone (11), commit recovery (16), rejected pushes (24), conflicts (25–26) and IDE controls (27) as separate trainer-led explanations rather than interruptions to the main student path.

## Suggested use of the afternoon conflict slot

Discuss why overlapping edits can conflict and show the conflict slides. Let students spend the remaining time checking project content and practicing their demos. The student portfolio sequence deliberately avoids forcing a conflict or rewriting history.

## Before every command block

Confirm the folder and branch. State what should change and what should stay visible in the page. Pause for manual edits and Ctrl+S. Ask students to inspect the diff before committing. If a command fails, diagnose it before allowing them to paste the next block.

## Closing answers

A commit records staged content. Git tracks history; GitHub hosts repositories and collaboration. Fetch downloads remote history; pull also integrates it. A pull request proposes changes for review. Publishing uses the committed files after deployment succeeds.


## Files and sharing

Keep index.html, STUDENTS.md, TEACHER.md and README.md at the repository root. The original PDF stays on the teaching computer and is excluded from Git because it is approximately 95 MB. Share the student guide directly from GitHub. There is one portfolio version, with its full code embedded in the student guide. Students create their own repositories; listenermedia/Git-GitHub is the published classroom reference.
