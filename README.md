# PELICAN RESUME SITE HOW I DID IT AND HOW TO REPLICATE IT 
# Assignment 2 by Iteoluwakisi Oyewusi

## Table of Contents
- [Purpose](#purpose)
- [Prerequisites](#prerequisites)
- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Technical Steps](#technical-steps)
- [Updating and Committing Changes](#updating-and-committing-changes)
- [Frequently Asked Questions](#frequently-asked-questions)
- [My Implementation Of Andrew Etters Book](#my-implementation-of-andrew-etters-book)
- [Credits](#credits)
- [Conclusion](#conclusion)

## Purpose
The purpose of this project was to create a fully functional static resume website using Pelican , a static site generator to present the resume and document it appropriately using a lighthweight markup language like **Markdown** 

## Prerequisites
To be able to do this yourself you will need 
- A computer with inernet access in my case I used a *Windows* device 
- Python installed on that computer 
- `pip` installed 

## Project Overview

**Technologies Used**

- Static Site Generator: `Pelican`
- Programming Language: `Python`
- Markup Language: `Markdown`
- Deployment Platform: `GitHub Pages`
- Version Control Software:`Git`

This README explains the technical steps taken and connects them to principles from Andrew Etter’s *Modern Technical Writing*. a book I have recently read to understand how to make these types of instructions seeing as I have not done this in a while 

---
## Project Structure

After running `pelican-quickstart`, the project directory contains several important folders and files.

- `content/` – Contains Markdown files that will become pages on the site.
- `output/` – Stores the generated static HTML website.
- `pelicanconf.py` – Main configuration file for the site.
- `publishconf.py` – Configuration used when publishing the site online.

The `content/` directory is the most regularly modified part of the project because it stores the pages written in Markdown. During the build process, Pelican reads these files and converts them into HTML pages that are placed in the `output/` directory. These HTML files are what visitors see when they access the website.

## Technical Steps

### 0. Setting up your workspace
- Identify your ideal folder for workflow and name it accordingly
- Set up your folder order and make sure you have a distinct set of folders for each of  the files that will go within your main folder 
- Make sure you have python installed on your device and its reachable via the terminal
- Open up your terminal and the work begins

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
- Linked here is a markdown tutorial that explains basic formatting tools [markdownguide.org](https://www.markdownguide.org/) 

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
  `python -m pelican content -s pelicanconf.py`
- You could also view the site locally in the termianal by running: 
   `python -m pelican.server` 

## Updating and Committing Changes 
While working on my Pelican site , I frequently needed to effect any changes I made to my files locally on my desktop . I took the following steps to ensure safe commissions 

### Checking Project Status
- I made use of of the `git-status` keywords whenever I logged off my pc and wanted to assure the state of my files and folders 
- I also used `git add .` to make sure I have not changed anything without pushing those changes to the github repository 

### Making Changes to the .MD files
- I would have made all my changes to the md files at this point , then post `git add .` , I use `git commit -m "any meaninful phrase" ` to package my changes together for exportation to github 
- Final step would be to move these to the github repo using `git push` to send our packaged changes to the repository 

## Frequently Asked Questions
- How do I add italics to my README.md file ?
   You can do so by adding two asterisk keys one at the start and at the end of the text you want to italicize like so :`*"text"*` and you should end up with this on your actual markdown preview : *Italics*

- How do I make words BOLD in my README.md file ?
   You can handle changing text to Bold by making use of a double asterisk combo before and after the word like so `**"text"**` should end up with this in your actual markdown : **BOLD**

- How do I add Links to my README.md file ?
   You can handle adding links to websites or even to other points in your same markdown file by using a [] then () bracket combination , you should then end up in a setup like so : [Link Name](https://music.youtube.com/watch?v=kNpTKgNQNpI&si=t3BT_0KOauxxFg9r), if you wanted to link sections of your readme , you can add the section name within [] and then within your () add a hashtag before the section name but this time all in lowercase  . It should look like this if implemented appropriately  [FAQs](#frequently-asked-questions)

- Why do I even bother with a markup language over a regular text file ?
   You should bother and even seek out markup languages over regular text files because they make it a lot easier for you to express your opinions and images 

- How do I know if I have installed `pip` ? 
   You can check by running `pip --version` if a number is returned you are fine , if not you would need to install it via `python -m ensurepip --upgrade` , although this will not work all the time so if that does not work for you you can proceed with `python -m pip install --upgrade pip`

## My Implementation Of Andrew Etters Principles for Modern Technical Writing 
- I made thje decision to utilize a lightweight markup language and did so as Andrew argues theyu are the preferred form to handle issues like portability , raw level readability and documentation easy to version control 

- I emphasized version control system like Git and commited as early and as often as possible and also made sure to keep documentation in the same repository as the project 

- I also made use of the concept of localization , since waiting and planning for appropriate translations into as many languages as possible takes an excessive amount of time , I make the decision to use as plane a text as possible to make it easy to translate as well as avoiding meanings being present in complex formatting or images 

## Credits
README was Peer Reviewed by fellow members of my assigned Foomatic team:
Jericho Dinozi and Nobert Siemens.

Made references to and(or) made use of varying resources :
Andrew Etter's Modern Technical Writing to implement appropriate techniques for structuring and creating tangible README files.
Implemented some generative AI tools to clarify some syntax and ensure grammatical accuracy.

## Conclusion
In conclusion , I believe making a README is not just important but necessary for any good project it helps keep information readily available for any audience , provides essential documentation and can be easily customized by multiple parties and taking advantage of this via light weight markup tools as mentioned. Additionally  , the resume and site generated were made easier by looking at documentation that exists because of those who came before me and were willing to take note of their procedures 