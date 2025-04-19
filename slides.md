---
theme: dracula
title: Git Started – An Introduction to Git
info: |
  ## Workshop hosted by G:URL*s Coding Club Vienna
# apply unocss classes to the current slide
class: text-center
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
hideInToc: true
---

# An Introduction to Git

Hosted by G:URL\*s Coding Club

---
layout: cover
hideInToc: true
---

<section class="flex items-center flex-1 h-auto justify-center">
<img class="h-72 w-72" src="/slides.svg"/>
</section>


---
transition: fade-out
hideInToc: true
layout: image-left
image: /profile-picture.jpg
---

# Who am I?

- 👩‍💻 Fullstack Software Engineer @ Elevantiq
- 🛠️ Javascript/Typescript
- 💜 Org. member @ G:URL\*s Coding Club since June 2024
- 🧗 Bouldering & Eating & Running

---
transition: slide-up
hideInToc: true
---

# What is git?

`Version Control System`

> "...is a system that records changes to a file or set of files over time so that you can recall specific versions later."

<br/>
<v-click>

### Raise your hand if you ever...

</v-click>

<ol>
  <li v-click>Wanted to share your code, or let other people work on your code?</li>
  <li v-click>Made a change to code, realized it was a mistake and wanted to revert back?</li>
  <li v-click>Lost code or had a backup that was too old?</li>
  <li v-click>Wanted to prove that a particular change broke or fixed a piece of code?</li>
</ol>

---
layoutClass: gap-16
hideInToc: true
---

# Table of contents

<Toc text-sm minDepth="1" maxDepth="1" />

---
transition: slide-up
hideInToc: true
---

# Installation and setup

1. [Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

```bash
# Checking git version
$ git -v
```

2. Configuration

```bash
# Setting up the identity is necessary as it is used within each commit
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

# Checking if the identity has been set up correctly
$ git config --list
```

<!--
3. Help command

```bash
$ git help <verb>
$ git <verb> --help
```
-->

---
layout: two-cols
---

# Initialize a repository

1. Create a project folder

```bash
$ mkdir my-project # creates a new folder
$ cd my-project    # navigates to the folder
```

2. Initialize a git repository

```bash
$ git init # creates a .git folder
```

<br/>

<v-click>

## Do you see any changes?

<!--
1. Navigate to the project folder
2. Run `ls -a` to see hidden files


What does git init do?
- Creates a hidden .git directory with a lot of metadata including
HEAD
config
refs (branches, tags etc)
- It makes the repository ready so changes can be tracked
-->
</v-click>

<br/>

<v-click>

<img src="/gitinit.gif" alt=""/>

</v-click>

::right::

<v-click>

## Let's create our first file

```bash
$ touch README.md # creates a new file
```

</v-click>

---
layout: two-cols
---

# Recording Changes

<v-click>

## 1. Untracked

- Ignored files within .gitignore
- New files that have not been there in the previous changes

</v-click>

::right::

<v-click>

## 2. Tracked

Changes git knows about

</v-click>

<v-click>

### Modified

```bash
$ git status  # Check which files changed
```

</v-click>

<v-click>

### Staged

```bash
$ git add <file>  # Stage specific file
$ git add .       # Stage all changes
$ git status      # Check staged files
```

</v-click>

<v-click>

### Committed

```bash
$ git commit -m "descriptive message"
$ git log         # View commit history
```

</v-click>

<v-click>

### Unmodified

</v-click>

<!--
# .gitignore examples: 
- .env (secrets, local configs)

# Tracked & Unstaged:
- You started working on a feature
- You are trying to find an error by using console logs


# Staging
- You might have fixed and issue and adopted documentation 
- staged files = ready to be committed



# Commit
- added to the git history
- adds all staged files
-->

---
layout: two-cols
---

# Git

- Version control system
- Command-line tool
- free and open-source

::right::

# GitHub

- Host for git repositories
- Additional collaboration features:
  - Pull Requests
  - Issues
  - Actions
  - Discussions
  - Forks
- Extensive free plan

<!--
Note: Other Git hosting platforms exist:
- GitLab
- Bitbucket
-->

---
layout: two-cols
---

# Publishing your code

## Create a GitHub account

1. Open https://github.com
2. Click `Sign Up` in the right top corner
3. Fill in the required information

## Create a repository

1. Navigate to your profile
2. Click on `Repositories`
3. Click on `New`
4. Define the repository name and make the repository `public`
5. Click `Create repository`

::right::

## Push your work to GitHub

```shell
# Add the remote repository origin
$ git remote add origin https://github.com/<OWNER>/<REPOSITORY_NAME>.git

# Rename the default branch to main
$ git branch -M main  # -M flag forces the rename even if destination exists

# Push the changes to the remote repository
$ git push -u origin main

```

<br/>

## Fetching changes

```shell
$ git pull # Pull the changes from the remote repository
```

<!--
Note:
- Historically, Git used 'master' as the default branch name
- GitHub and other platforms now use 'main' as the default
- The -M flag is a combination of:
  - -m: move/rename a branch
  - -M: move/rename even if target exists
-->

---
hideInToc: true
layout: two-cols
---

# Branching

<section v-click="3">

- Branches are used to develop features isolated from each other
- Use cases:
  - Different versions of documentation (e.g., v1.0, v2.0)
  - Different environments (e.g., development, production)
  - Different features (e.g., login, registration)

```shell
# Create a new branch
$ git checkout -b feature-branch
# push the branch to the remote repository
$ git push origin feature-branch
```

</section>
::right::

<div  class="p-6 pt-12 flex flex-col gap-6">

<img v-click="1" src="/main-branch.svg" alt=""/>
<img v-click="2" src="/feature-branch.svg" alt=""/>
</div>

<!--
examples: Different branches are used for different versions of the documentation (e.g., v1.0, v2.0).
-->

---
hideInToc: true
layout: two-cols
---

# Merging (basics)

- Combining changes from different branches
- Merge Conflicts

<br/>

## Let's merge

- git

```shell
# Switch to the main branch
$ git checkout main
# Merge the feature-branch into main
$ git merge feature-branch
```

- GitHub

  - Create a pull request
  - Merge the pull request

::right::

  <img src="/merge-branch.svg" alt=""/>

<!--
There are times where its easy to merge branches, and there are times where it can be a bit tricky because conflicts can arise.
Conflicts occur when two branches have changed the same part of the same file, and Git doesn't know which version to use.
add image and mention that this might be for another more deep dive session
-->

---
layout: two-cols
---

# Sharing your code with others

## `git clone`

- Download a copy of the repo
- Points to the original repository
- Direct team collaboration (write access)

```shell
# Clone a repository
$ git clone https://github.com/ORIGINAL-OWNER/REPO-NAME
```

::right::

## Fork (GitHub feature)

- Download a copy of the repo under your account
- Open source contribution (without write access)

```shell
# After forking on GitHub, clone your fork
$ git clone https://github.com/YOUR-USERNAME/REPO-NAME
# Add original repository as upstream
$ git remote add upstream https://github.com/ORIGINAL-OWNER/REPO-NAME
```

<!--
## Clone
- makes a copy to your machine


## Forking
- makes a copy of the project to you github account (not local)
- when missing permissions
-->

---
layout: cover
hideInToc: true
---

# OPEN SOURCE

> Open source software is code that is designed to be publicly accessible—anyone can see, modify, and distribute the code as they see fit.



---
hideInToc: true
layout: two-cols
---

# INTERACTIVE DEMO

1. Fork these slides to your account
2. Clone the repository to your local machine

```shell
$ git clone https://github.com/YOUR-USERNAME/REPO-NAME
```

3. Create a new branch

```shell
$ git checkout -b feature-branch
```

4. Make a change to .pages/CHANGE-ME.md (e.g., add your nickname)

5. Commit the change

```shell
$ git add .
$ git commit -m "Add my nickname"
```

::right::

6. Push the branch to your fork

```shell
$ git push origin feature-branch
```

7. Create a pull request

---
hideInToc: true
src: ./pages/CHANGE-ME.md
---


---
hideInToc: true
---

# Summary Cheatsheet

- `git init` - Initialize a new repository
- `git clone <repo>` - Clone a repository
- `git status` - Check the status of the repository
- `git add <file>` - Stage a file
- `git commit -m "<message>"` - Commit changes
- `git push` - Push changes to the remote repository
- `git pull` - Pull changes from the remote repository
- `git checkout <branch>` - Switch to a branch
- `git checkout -b <branch>` - Create a new branch
- `git merge <branch>` - Merge a branch into the current branch

---

# Setting Up Git for Success: A Developer’s Checklist


✅ Using `.gitignore`

✅ Write descriptive commit messages

✅ Use feature branches

✅ Integrations/Tools

<!--
# .gitignore
sensitive data

# feature branches
conflicts

# integrations/tools
make your life easier
-->

---

# Tools

## IDE

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - Git extension for VS Code
- [IntelliJ IDEA](https://www.jetbrains.com/idea/)

<br/>

## Git GUI

- [GitHub Desktop](https://desktop.github.com/)
- [GitKraken](https://www.gitkraken.com/)
- [GitButler](https://gitbutler.com/)

---
layout: two-cols
hideInToc: true
---

# What's next?

## Official Documentation

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Documentation](https://git-scm.com/doc)

<br/>

## Interactive Learning

- [GitHub Skills](https://skills.github.com/)
- [Oh My Git!](https://ohmygit.org/) - An open-source game for learning Git
- [Learn Git Branching](https://learngitbranching.js.org/) - Interactive Git visualization tool

<br/>

## Video Courses

- [Git and GitHub for Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk) - freeCodeCamp
- [GitHub Training & Guides](https://www.youtube.com/githubguides)

::right::

## Tools

- [GitKraken](https://www.gitkraken.com/) - Git GUI Client
- [GitHub Desktop](https://desktop.github.com/) - Simplified Git GUI

- [GitLens for VS Code](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

---
hideInToc: true
---

# Feedback

<section class="flex items-center mt-12 flex-1 h-auto justify-center">
<img class="h-72 w-72" src="/feedback.svg"/>

</section>

---
layout: cover
---

# Q&A

## Thank you for your attention

<!--
TODO: for each section add a real world scenario from work
-->

<!--
Look into resources: 

https://github.com/git-guides/git-add
https://github.blog/developer-skills/github/write-better-commits-build-better-projects/
-->
