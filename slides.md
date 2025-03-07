---
theme: dracula
title: Git Workshop
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

# Git Workshop

Hosted by G:URL\*s Coding Club

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
hideInToc: true
---

# What is git?

Version Control System

<!--
give general introduction to git based on an example
add picture showcasing file changes without version control
-->

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

3. Help command

```bash
$ git help <verb>
$ git <verb> --help
```

---

# Initialize a repository

1. Create a project folder
2. Initialize a git repository

```bash
$ git init
```

<br/>

<v-click>

## Do you see any changes?

</v-click>

<!--
What does git init do? 
- Creates a hidden .git directory with a lot of metadata including
HEAD
config
refs (branches, tags etc)
- It makes the repository ready so changes can be tracked

TODO: Add gif
-->

---
layout: two-cols
---

# Recoding Changes

<!-- add image of the flow -->

::right::
<v-click>

## 1. Untracked

</v-click>

<br/>

<v-click>

## 2. Tracked

</v-click>

<br/>

<v-click>

### Modified

```bash
$ git status  # Check what files changed
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

<!--
examples of good git messages and why
-->

</v-click>

<v-click>

### Unmodified

</v-click>

---
layout: two-cols
---

# Git vs Github?

## Git

- Version control system
- Command-line tool
- free and open-source

::right::

## GitHub

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
- Azure DevOps
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
---

# Branching

<!--
add image explain why this is done create a PR
examples: Different branches are used for different versions of the documentation (e.g., v1.0, v2.0).
-->

---
hideInToc: true
---

# Merging

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

---
layout: cover
hideInToc: true
---

# INTERACTIVE DEMO

---
hideInToc: true
src: ./pages/CHANGE-ME.md
---

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
layout: cover
---

# Q&A

## Thank you for your attention
