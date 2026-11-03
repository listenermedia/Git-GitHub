# Build your portfolio step by step

Use **VS Code → Terminal → New Terminal → PowerShell**. Type Git commands in the terminal. Create and edit files manually in VS Code Explorer. Run one stage at a time.

Replace YOUR NAME, YOUR_EMAIL and YOUR_USERNAME wherever they appear. Commands assume a new project.

## Stage 1 — Create and open your project folder · PPT 08–12

1. In Windows File Explorer, create a folder named **my-portfolio** in your usual projects location.
2. In VS Code, choose **File → Open Folder** and open my-portfolio.
3. Choose **Terminal → New Terminal**. The terminal should open inside this folder.
4. Run:

```powershell
git --version
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR_EMAIL"
git init -b main
```

Name/email configuration is needed only if you have not already set it correctly. It sets commit identity, not GitHub sign-in. Use an email appropriate for public commit history.

**What changed:** Git now tracks this folder as a repository on the main branch. No files or commits exist yet. The -b main option sets this repository's initial branch; no global default-branch setting is needed.

## Stage 2 — Create your README manually · PPT 12–13

In VS Code Explorer, click **New File**, name it **README.md**, paste the following and save with **Ctrl+S**:

```markdown
# My Portfolio

My first portfolio website.
```

Run:

```powershell
git status
git add README.md
git commit -m "Create portfolio README"
git log --oneline
```

**What changed:** README.md is recorded in your first commit. Status should now be clean.

## Stage 3 — Edit the README and inspect changes · PPT 14–15

Open README.md. Add this line below the existing text and save:

```markdown
I am learning HTML, CSS, Git and GitHub.
```

Run these first:

```powershell
git status
git diff
```

**Check:** the added line appears with a + in the diff. The file is modified but not yet staged.

Then run:

```powershell
git add README.md
git diff --staged
git commit -m "Add learning goals"
```

**What changed:** your second commit records the learning-goal line. Staging selects what goes into the commit.

## Stage 4 — Build the first portfolio page · portfolio preparation for PPT 28

In Explorer, create **index.html** next to README.md. Paste this complete code and save:

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="Muhammed Sanweer KT — a portfolio exploring code, design and learning in public.">
<title>Sanweer — Code & Curiosity</title>
<style>
:root{--paper:#f4f1e9;--ink:#202820;--muted:#596253;--green:#d7ff65;--line:#cdd0c3}*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--paper);color:var(--ink);font:17px/1.65 system-ui,-apple-system,sans-serif}a{color:inherit;text-underline-offset:5px}a:focus-visible{outline:3px solid #697f22;outline-offset:6px}.wrap{width:min(1160px,90%);margin:auto}.skip{position:absolute;left:-9999px}.skip:focus{left:20px;top:20px;background:white;padding:12px;z-index:5}header{border-bottom:1px solid var(--line)}nav{display:flex;justify-content:space-between;align-items:center;gap:24px;padding:25px 0}.brand{font-weight:850;text-decoration:none;letter-spacing:-1px;font-size:24px}.brand span{color:#647d2c}.links{display:flex;gap:28px;font-size:14px}.links a{text-decoration:none}.links a:hover{text-decoration:underline}.hero{display:grid;grid-template-columns:1.5fr 1fr;align-items:center;gap:60px;padding:90px 0 80px}.eyebrow{font:700 12px/1.5 ui-monospace,monospace;text-transform:uppercase;letter-spacing:2px}.eyebrow:before{content:"";display:inline-block;width:8px;height:8px;border-radius:50%;background:#647d2c;margin-right:10px}h1{font-size:clamp(54px,7.6vw,100px);letter-spacing:-.075em;line-height:1.02;margin:24px 0}h1 em{font-family:Georgia,serif;font-weight:normal}.intro{max-width:470px;color:var(--muted);font-size:19px}.actions{display:flex;align-items:center;gap:25px;flex-wrap:wrap;margin-top:32px}.button{display:inline-block;background:var(--ink);color:var(--paper);padding:14px 22px;border-radius:4px;text-decoration:none;font-size:14px;font-weight:700}.button:hover{background:#415034}.textlink{font-size:14px;font-weight:650}.art{background:var(--green);aspect-ratio:1;position:relative;border-radius:50% 50% 4px 4px;display:grid;place-items:center;overflow:hidden}.art:before,.art:after{content:"";position:absolute;border:1px solid #637938;border-radius:50%;width:76%;height:76%}.art:after{width:110%;height:40%;transform:rotate(-35deg)}.symbol{font:700 clamp(60px,9vw,125px)/1 ui-monospace,monospace;z-index:1;transform:rotate(-8deg)}.art-label{position:absolute;bottom:23px;left:24px;font:12px ui-monospace,monospace}.strip{border-block:1px solid var(--line);padding:18px 0;display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;font:12px ui-monospace,monospace;letter-spacing:1px;text-transform:uppercase}section{padding:80px 0;scroll-margin-top:20px}.section-head{display:flex;justify-content:space-between;align-items:end;gap:20px;margin-bottom:32px}h2{font-size:clamp(34px,4vw,52px);line-height:1.12;letter-spacing:-2px;margin:10px 0}h3{font-size:25px;line-height:1.2;letter-spacing:-.7px}.section-head p{color:var(--muted);max-width:330px}.projects{display:grid;grid-template-columns:1fr 1fr;gap:26px}.project{border-top:1px solid var(--ink);padding-top:16px}.project-top{display:flex;justify-content:space-between;font:12px ui-monospace,monospace;margin-bottom:18px}.project-art{min-height:220px;padding:30px;display:flex;align-items:center;justify-content:center;border-radius:5px;background:#e1e5d7}.browser{width:90%;background:var(--paper);border:1px solid #87917e;box-shadow:12px 12px 0 #b6bfaa;padding:20px;transform:rotate(-3deg)}.dots{font-size:11px;letter-spacing:5px;border-bottom:1px solid var(--line);padding-bottom:10px}.browser strong{font-size:32px;line-height:1.1;display:block;margin-top:15px;letter-spacing:-1px}.browser small{font:10px ui-monospace,monospace}.project p{color:var(--muted);max-width:490px}.tags{font:12px ui-monospace,monospace}.project-art.dark{background:#26372b;color:var(--green)}.terminal{font:15px/2 ui-monospace,monospace;width:100%}.terminal span{color:#a0b49c}.about{border-top:1px solid var(--line);display:grid;grid-template-columns:1fr 1.2fr;gap:80px}.about-copy p{color:var(--muted);font-size:19px}.skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:25px}.skills span{border:1px solid #bbc1b1;border-radius:30px;padding:7px 15px;font-size:13px}.note{font:12px ui-monospace,monospace;color:var(--muted);margin-top:25px}.contact{background:var(--green);padding:55px;border-radius:6px;display:flex;align-items:center;justify-content:space-between;gap:30px;margin-bottom:70px}.contact h2{max-width:580px}.contact p{max-width:550px}footer{border-top:1px solid var(--line);padding:24px 0;display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;font:12px ui-monospace,monospace}@media(max-width:760px){.hero{grid-template-columns:1fr;padding:55px 0;gap:40px}.art{max-width:370px;width:100%;justify-self:center}.projects,.about{grid-template-columns:1fr;gap:35px}.section-head{display:block}.contact{display:block;padding:30px}.contact .button{margin-top:15px}.links{gap:15px}section{padding:55px 0}.strip{font-size:10px}h1{font-size:clamp(52px,13vw,85px)}}@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>
<header><nav class="wrap" aria-label="Main navigation"><a class="brand" href="#">sanweer<span>.</span></a><div class="links"><a href="#work">Work</a><a href="#about">About</a><a href="#contact">Connect ↗</a></div></nav></header>
<main id="main" class="wrap">
<div class="hero"><div><p class="eyebrow">Code. Create. Keep learning.</p><h1>Small ideas.<br><em>Thoughtful</em><br>digital things.</h1><p class="intro">Hi, I’m Muhammed Sanweer KT. This is my space to explore the web, share what I build, and keep learning in public.</p><div class="actions"><a class="button" href="#work">Explore my work ↗</a><a class="textlink" href="https://github.com/listenermedia">Find me on GitHub</a></div></div><div class="art" role="img" aria-label="Abstract code brackets on a lime green orbital illustration"><span class="symbol">&lt;/&gt;</span><span class="art-label">MADE OF CODE + CURIOSITY</span></div></div>
<div class="strip"><span>01 / Learn by making</span><span>02 / Improve with feedback</span><span>03 / Share the process</span></div>
<section id="work"><div class="section-head"><div><p class="eyebrow">Selected explorations</p><h2>A little code.<br>A lot of curiosity.</h2></div><p>A working portfolio and a practical learning repository. Simple foundations, built to grow.</p></div><div class="projects">
<article class="project"><div class="project-top"><span>01 / WEB DESIGN</span><span>HTML + CSS</span></div><div class="project-art" aria-hidden="true"><div class="browser"><div class="dots">● ● ●</div><small>MY LITTLE CORNER OF THE WEB</small><strong>Hello, world.<br>Let’s build.</strong></div></div><h3>A personal corner of the web</h3><p>This responsive, single-page portfolio brings together my introduction, projects and GitHub profile. Built without a framework, with readable code and accessible navigation.</p><p class="tags">Responsive layout / Semantic HTML / CSS</p><a class="textlink" href="https://github.com/listenermedia/Git-GitHub/blob/main/index.html">Explore the source ↗</a></article>
<article class="project"><div class="project-top"><span>02 / LEARNING IN PUBLIC</span><span>GIT + GITHUB</span></div><div class="project-art dark" aria-hidden="true"><div class="terminal"><span>$ git switch -c curiosity</span><br>make something small<br><span>$ git add .</span><br><span>$ git commit -m "Keep learning"</span><br>one step forward. ↗</div></div><h3>From first commit to a live page</h3><p>A hands-on workshop repository covering commits, branches, pull requests and publishing. Includes a step-by-step student walkthrough to make the process easier to follow.</p><p class="tags">Version control / Collaboration / Documentation</p><a class="textlink" href="https://github.com/listenermedia/Git-GitHub">Visit the repository ↗</a></article>
</div></section>
<section id="about" class="about"><div><p class="eyebrow">A bit about me</p><h2>Always a work<br>in progress.</h2></div><div class="about-copy"><p>I’m Muhammed Sanweer KT, the creator behind listenermedia on GitHub. I like the idea that a simple file can become something useful on the web.</p><p>This portfolio is part of a Git and GitHub workshop: a place to practise, experiment and turn each new lesson into a small improvement.</p><div class="skills" aria-label="Tools used in this project"><span>HTML</span><span>CSS</span><span>Git</span><span>GitHub</span><span>VS Code</span></div><p class="note">Currently exploring → better web experiences, one commit at a time.</p></div></section>
<section id="contact" class="contact"><div><p class="eyebrow">Keep the conversation going</p><h2>Good things start<br>with a hello.</h2><p>Explore my repositories, follow the learning journey, or share a thought about this project.</p></div><a class="button" href="https://github.com/listenermedia">Say hello on GitHub ↗</a></section>
</main><div class="wrap"><footer><span>Muhammed Sanweer KT / listenermedia</span><span>Built with curiosity. Tracked with Git.</span><a href="#">Back to top ↑</a></footer></div>
</body>
</html>

```

Open index.html from Windows File Explorer in your browser. You should see a cream-and-green portfolio page with the Sanweer introduction, two project cards, About and Connect.

Run:

```powershell
git add index.html
git commit -m "Add portfolio page"
```

**What changed:** the repository now contains a working single-page HTML/CSS website. All later portfolio edits happen inside this same index.html file.

## Stage 5 — Personalise the introduction

In index.html, replace **Muhammed Sanweer KT** everywhere with your own name and **sanweer** in the navigation brand with your short name. Change the hero introduction (the paragraph with class="intro") to describe yourself. Update the browser title in the title element. Save, refresh and inspect:

```powershell
git diff
git add index.html
git commit -m "Personalise name and introduction"
```

**What changed:** the page now introduces you; the design stays the same.

## Stage 6 — Complete About and Connect

Edit the two paragraphs inside the About section (id="about") to tell your story. Replace listenermedia in the GitHub profile links with your username. Update the footer name and the contact paragraph to suit you. Keep project repository links pointing to this workshop until you have your own source repository. Save and refresh.

```powershell
git diff
git add index.html
git commit -m "Update biography and profile links"
git log --oneline
```

**What changed:** your biography and profile links are personalised. You should have five commits.

## Stage 7 — Put your project on GitHub · PPT 17–18

In your browser, sign in to GitHub and create a repository named **my-portfolio**. Choose public for this workshop. Leave the options to add a README, .gitignore and license unchecked; your local project already has files.

Replace YOUR_USERNAME below and run:

```powershell
git remote add origin https://github.com/YOUR_USERNAME/my-portfolio.git
git remote -v
git push -u origin main
```

Follow the sign-in flow if prompted. Refresh the GitHub repository page.

**What changed:** GitHub now holds your committed files and history. Your local files did not change. Repository hosting alone does not yet publish a website.

## Stage 8 — Improve your first project on a branch · PPT 19–20

Run before editing:

```powershell
git switch -c feature/project-description
```

In index.html, find:

```html
<p>This responsive, single-page portfolio brings together my introduction, projects and GitHub profile. Built without a framework, with readable code and accessible navigation.</p>
```

Replace it with a description in your own words, for example:

```html
<p>My first responsive portfolio, built with HTML and CSS and tracked with Git.</p>
```

Save, refresh the browser and run:

```powershell
git diff
git add index.html
git commit -m "Improve portfolio project description"
git switch main
```

**Check now:** refresh the browser. The old project description returns because main does not have the branch's commit yet.

Run:

```powershell
git merge feature/project-description
git push
```

Refresh again.

**What changed:** main now includes the improved description. You created a branch, committed a change and merged it locally.

## Stage 9 — Add your next project through a pull request · PPT 21–23

Run:

```powershell
git switch -c feature/second-project
```

In index.html, find the second project card's closing **</article>**. Immediately after it, and before the surrounding projects container's closing **</div>**, paste:

```html
<article class="project">
  <h3>Study planner</h3>
  <p>A project idea to organise weekly learning goals. My next step is to build a prototype.</p>
</article>
```

Save and refresh. You should see three project cards. Keep this labelled as an idea unless you have actually built it.

Run:

```powershell
git diff
git add index.html
git commit -m "Add next project card"
git push -u origin feature/second-project
```

On GitHub:

1. Open a pull request from **feature/second-project** into **main**.
2. Title it **Add next project card**.
3. Inspect Files changed with a partner.
4. Merge using **Create a merge commit** for this exercise.

Return to the terminal:

```powershell
git switch main
git pull --ff-only
git log --oneline --graph --all
```

**What changed:** the new card reached main through a reviewed pull request. Your local main now matches the merged remote history.

## Stage 10 — Publish the website · PPT 28

On GitHub, open the repository's **Settings → Pages**. Select deployment from a branch, **main**, and **/(root)**, then save. Interface labels may vary.

Wait for the deployment to succeed and open the URL GitHub reports, normally:

https://YOUR_USERNAME.github.io/my-portfolio/

**What changed:** your portfolio is now available as a website. Publishing did not modify your HTML. Deployment may take several minutes.

Check your name, three project cards, About and Connect links, and a narrow-screen layout.

## Stage 11 — Update the live site

In index.html, find **Code. Create. Keep learning.** and change it to your own short tagline. Save and preview locally.

```powershell
git diff
git add index.html
git commit -m "Update portfolio tagline"
git push
```

Wait for the new deployment and refresh the live URL.

**What changed:** a new commit updated the tagline locally, on GitHub and, after deployment, on the live website.

## Final page and history checklist · PPT 29–31

Your final page has your name and introduction, biography and skills, three project cards, profile links and your tagline. The original HTML supplied in Stage 4 plus the explicit edits in Stages 5, 6, 8, 9 and 11 produce this final page.

```powershell
git status
git log --oneline --graph --all
```

Status should be clean. Explain one commit, one branch and your pull request to a partner.

## Optional PPT topics — trainer-led

PPT 11 clone, PPT 16 amend/reset/revert, PPT 24 rejected pushes, PPT 25–26 conflicts and PPT 27 Source Control are separate demonstrations. They are not additional steps to paste into the portfolio sequence. Your trainer will guide these if needed.

## If something goes wrong

- Git not recognised: install Git, restart VS Code and retry.
- Nothing to commit: save the edited file and check git status.
- Not a Git repository: make sure the terminal is inside my-portfolio.
- Authentication failed: check your GitHub account and repository access.
- Push rejected or pull fails: show the trainer git status and the history before trying recovery commands.
- Website 404: check successful Pages deployment, the reported URL and that index.html is at the root of main.

Never share passwords or tokens. Official references: https://git-scm.com/docs and https://docs.github.com/en/pages .

