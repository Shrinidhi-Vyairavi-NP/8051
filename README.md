\# Foundations of IoT — 8051 Projects



\## Overview



This repository contains assignments and projects developed for the Foundations of IoT course using the 8051 microcontroller.



Each board family should have its own Git repository. This repository is dedicated to 8051 projects.



\## Repository Structure



```text

8051/

├── .gitignore

├── README.md

└── BLINK\_LED/

&#x20;   ├── LED\_BLINK.uvproj

&#x20;   ├── ledblinkplz.c

&#x20;   ├── STARTUP.A51

&#x20;   ├── Objects/

&#x20;   │   └── generated HEX files

&#x20;   └── Listings/

&#x20;       └── generated listing files

```



The actual project files and folder names may vary between assignments.



\## Tools Required



\- Git for version control.

\- Keil µVision with the compatible Keil C51 compiler for 8051 projects.

\- The appropriate 8051 hardware and programming tools, if the assignment requires physical testing.



\*\*Note:\*\* Keil MDK-ARM is intended for ARM-based microcontrollers and is not a replacement for the Keil C51 toolchain required by these 8051 projects.



\## Files to Include in Git



Include the files needed to understand, modify, and rebuild the project:



\- C source files (`.c`)

\- Required header files (`.h`)

\- Startup assembly files (`.A51`), if used

\- Keil project files (`.uvproj` or `.uvprojx`)

\- Required configuration files

\- HEX firmware files (`.hex`) when required by the assignment

\- This README and the repository's `.gitignore`



Generated object files, listing files, build logs, and personal IDE settings should generally be excluded.



\## Instructions for Students



\### 1. Install the required tools



Install Git and the appropriate Keil software and compiler for the board used in your assignment.



Verify that Git is available by opening Command Prompt and running:



```cmd

git --version

```



\### 2. Organize your project



Create a folder for your assignment and place the required source files and Keil project file inside it.



Keep the original project structure unless you understand which paths and settings need updating.



\### 3. Initialize a local Git repository



Open Command Prompt in the root folder you want Git to track.



For a new repository, run:



```cmd

git init

```



If you are working inside an existing Git repository, do not initialize another one unnecessarily.



\### 4. Create a `.gitignore` file



Create `.gitignore` in the repository root.



For an 8051 project, a starting configuration is:



```gitignore

\*\*/Listings/



\*\*/Objects/\*.obj

\*\*/Objects/\*.lst

\*\*/Objects/\*.m51

\*\*/Objects/\*.abs

\*\*/Objects/\*.omf

\*\*/Objects/\*.lnp

\*\*/Objects/\*.build\_log.htm



\*.uvgui

\*.uvgui.\*

\*.uvopt

\*.uvoptx



Thumbs.db

Desktop.ini

.DS\_Store

```



This configuration deliberately does not ignore `.hex` files.



Review the rules for your particular assignment. Some project settings or generated files may be required by your evaluator.



\### 5. Check which files Git will track



Run:



```cmd

git status

```



For a more detailed list of untracked files, run:



```cmd

git status --short --untracked-files=all

```



Confirm that the required source files, project file, startup files, and required HEX files are included. Ensure that unwanted generated files and personal settings are excluded.



\### 6. Stage and commit your files



Stage the files:



```cmd

git add .

```



Review the staged changes:



```cmd

git status

```



Create a commit:



```cmd

git commit -m "Add 8051 assignment"

```



Staging and committing save a version of your project in the local Git repository. They do not upload it to GitHub.



\### 7. Publish the repository to GitHub (optional)



To make the repository available online:



1\. Sign in to GitHub and create a new, empty repository.

2\. Copy its repository URL.

3\. In Command Prompt, navigate to your local repository root.

4\. Add the GitHub repository as a remote:



```cmd

git remote add origin YOUR-REPOSITORY-URL

```



5\. Verify the remote:



```cmd

git remote -v

```



6\. Push your current branch. If your branch is named `master`, run:



```cmd

git push -u origin master

```



If your branch is named `main`, use `main` instead. Follow GitHub's authentication prompts if required.



For an existing local repository, create the online repository without initializing it with another README, license, or `.gitignore`, to avoid an unnecessary initial-history conflict.



\### 8. Submit future changes



After editing your project, inspect the changes:



```cmd

git status

```



Stage the intended changes:



```cmd

git add .

```



Commit them:



```cmd

git commit -m "Describe your changes"

```



If the repository is connected to GitHub, upload the commit:



```cmd

git push

```



\## Important Notes



\- Never commit passwords, API keys, private keys, or other secrets.

\- A successful Git commit does not prove that the project compiles or works on hardware.

\- Rebuild the project after source changes to generate an updated HEX file.





