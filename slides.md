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
---

# Who am I?

---
layoutClass: gap-16
hideInToc: true
---

# Table of contents

<Toc text-sm minDepth="1" maxDepth="1" />

---
transition: slide-up
---

# Git installation and setup

- [Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- Configuring git

```bash
# Setting up the identity is necessary as it is used within each commit
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

# Checking if the identity has been set up correctly
$ git config --list
```

---
level: 2
---

# Help

```
$ git help <verb>
$ git <verb> --help
```

---

# Initialize git

1. Create a project folder
2. Run git init

---

# Staging

```
git status
git add .
git status
```

---

# Commits

```
git commit -m `initial commit`

```

---
class: px-20
---

# Github

1. Create a GitHub account

---

# Publishing your code

<!--
git push
-->

---

# Branching

<!--
add image explain why this is done create a PR
-->

---

# Merging

---

# Tools & Extensions

---

# What's next?
