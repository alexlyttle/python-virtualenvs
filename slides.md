---
marp: true
theme: mytheme
paginate: true
_paginate: false
---
<!-- _class: lead -->

# Python Virtual Environments

Alex Lyttle | Skills Session | 14 May 2021

---
<!-- footer: 'Alex Lyttle | Skills Session | 14 May 2021' -->

# Title

This is some `inline code`

```bash
echo this is a code block
```

> This is a blockquote

$$a^2 = b^2 + c^2$$

https://marpit.marp.app/markdown

---

# Introduction

1. Quiz
2. What is a virtual environment?
    - Conda
    - Venv
    - Virtualenv
3. How do I manage different Python versions?
4. Worked example

---
<!-- _class: lead -->

> Help! I updated a Python package and now my code is broken!

---

# Why a virtual environment?

When you install a Python *package* (e.g. `numpy` or `scipy`) it is installed in the `site-packages` directory associated with your Python interpreter. This is how Python accesses the package when you run code.

When you install a package, it may have *dependencies* &mdash; i.e. other required packages. Sometimes dependencies must be a *particular version* in order for a package to work. **Therefore, if you update one package, it could break another.**

---

# What is a virtual environment?

A *virtual environment* is set of environmental variables for running software isolated from your system.

A Python virtual environment has its own self-contained `site-packages` directory and Python path which points to a particular Python interpreter. When you activate a virtual environment, it updates your `PATH` so that when Python looks for a package it looks in the virtual environment, not your system.

---

```bash
conda create --name myenv python=3.6
```

---
<!-- _class: lead -->

> Help! I updated Python and now my code is broken!

---

# <!--fit--> How do I manage different Python versions?
