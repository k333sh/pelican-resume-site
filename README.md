# PELICAN RESUME SITE AND HOW I DID IT AND HOW TO REPLICATE IT — Assignment 2 by Iteoluwakisi Oyewusi

## Project Overview
A static resume website built using Pelican, a Python-based static site generator. The site includes a homepage and a resume page written in Markdown and converted into HTML during the Pelican build process. The final site is deployed using GitHub Pages.  
This README explains the technical steps taken and connects them to principles from Andrew Etter’s *Modern Technical Writing*. a book I have recently read to understand how to make these types of instructions

---

## Technical Steps

### 0. Setting up your workspace
- Identify your ideal folder for workflow and name it accordingly
- Set up your folder order and make sure you have a distinct set of folders for each of the files that will go within your main folder 
- Make sure you have python installed on your device and its reachable via the terminal
- Open up your terminal and work begins

### 1. Installing Pelican and Initial Setup
- Installed Pelican, Markdown, and ghp-import using pip.
- Ran `pelican-quickstart` to generate the project structure.
- Confirmed that Pelican created configuration files and the `content/` directory.

### 2. Creating Content in Markdown
- Wrote `index.md` for the homepage.
- Wrote `resume.md` transforming the full resume I had on me into a workable ".md" file.
#### Formatting Resumes 
- Copy into md the resume you have on your hands
- Start to seperate into sections the different parts of the resume
- Select and set headings in markdown using "#, ##, ###" to show the level of heading it is 
- [linked here is a markdown tutorial that explains basic formatting tools](https://www.markdownguide.org/) 
###
- Added Pelican metadata (Title, Date, etc.) at the top of each file.
- Used Markdown for clean, portable, version-controlled content.

### 3. Configuring the Site
- You will get prompted on the terminal for configuration , the steps I took are below:
- Updated `pelicanconf.py` with:
  - Site name, author, and URL
  - `PATH = "content"`
  - Timezone and language
  - Navigation links (via `MENUITEMS` or automatic page generation)
- Used the default Pelican theme to keep the system simple and maintainable.

### 4. Generating the Static Site
- After I had confirmed I made whatever change I deemed necessary 
- Ran this is my terminal:
  python -m pelican content -s pelicanconf.py
- You could also view the site locally in the termianal by running: 
   python -m pelican.server 


  