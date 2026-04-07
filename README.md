# Darwin College DCSA Website — Contributor Guide

This website is built with [Jekyll](https://jekyllrb.com/) and hosted via GitHub Pages. 
The source files live in this repository and any changes pushed to the `master` branch 
are automatically published to the live website within a few minutes.

## Who to contact

This repository was created by at the end of 2019 by Michael Schneider and is now maintained by DCSA student volunteers. If you need help or access:

- **Kilian Bartsch** (kpb30) — first point of contact
- **Andy Jenkins** (adj35) — first point of contact
- **Espen Koht** (ehk20, Darwin College IT Manager) — has admin access as a backup if student 
  maintainers are unavailable

## How GitHub works — a quick primer

If you haven't used GitHub before, here is what you need to know:

- **Repository**: this is where all the website's files are stored, like a shared folder 
  with version history.
- **Commit**: a saved change to one or more files. Every commit has a message describing 
  what was changed and is logged permanently, so nothing is ever truly lost.
- **Branch**: a separate copy of the files where you can make changes safely without 
  affecting the live website. The live website is served from the `master` branch.
- **Pull Request (PR)**: a way to propose changes from your branch into `master`. It 
  allows others to review and discuss your changes before they go live. You can open a PR 
  entirely through the GitHub website without installing anything.
- **Merge**: once a PR is approved, it is merged into `master` and the changes go live.

For simple edits (text changes, image swaps), you can do everything through the GitHub 
website without any technical setup — see below.

## Roles and access levels

- **Owners / Admins**: can merge pull requests, manage access, and change settings. 
  Currently Kilian (kpb30), Andy (adj35), and Espen (ehk20) as backup.
- **Contributors**: can propose changes via pull requests but cannot merge them without 
  review. If you would like contributor access, contact one of the people above.

If you are a new DCSA executive committee officer and need access 
to update the website, please get in touch with Kilian or Andy in the first instance.

## Making changes

### Using AI tools/chatbots (recommended for beginners)
If you are unfamiliar with HTML or Markdown, tools like Github Copilot, ChatGPT or Claude can be very 
helpful. You can paste in the contents of a file and ask the chatbot to make specific changes 
for you, then copy the result back into GitHub. Always ask someone to review your PR 
before merging if you are unsure.

### Updating text
The main content files are Markdown (`.md`) files in the `content/` directory. You can 
edit these directly in the GitHub web interface:
1. Navigate to the file you want to edit
2. Click the pencil (edit) icon in the top right
3. Make your changes
4. At the bottom, write a short description of what you changed and click 
   **"Propose changes"**
5. On the next screen, click **"Create pull request"**
6. Ask an admin to review and merge it

### Updating images
- Images must be **under 1MB** in size
- Images should have a **4:3 aspect ratio** (height:width)
- Do not change existing image filenames
- Images can be uploaded via the GitHub web interface

## Local testing (optional, for advanced users)

You do not need to test locally for simple text or image changes — the preview on a PR 
is sufficient. Local testing is useful if you are making structural changes and want to 
see the result before opening a PR.

### With Jekyll directly
- Install dependencies — see the [slate theme](https://github.com/pages-themes/slate)
- Run `bundle exec jekyll serve`
- See also: [GitHub's guide to local Jekyll testing](https://help.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll)

### With Docker
- Install [Docker](https://www.docker.com/)
- Build the image: `docker build -t test .`
- Run the image: `docker run -d -p 4000:4000 --name beautiful-jekyll -v "$PWD":/srv/jekyll test`
- The site will be available at `http://localhost:4000`
