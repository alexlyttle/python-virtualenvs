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
    - `conda`
    - `venv`
    - `virtualenv`
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

A Python virtual environment has its own self-contained `site-packages` directory and Python path which points to a particular Python interpreter. When you run Python in a virtual environment, it updates your `sys.path` so that Python looks for packages installed within the environment only.

---

# How do I make a virtual environment?

![bg blur:1px right:33%](assets/images/terminal-code.png)

- Depends on how you installed Python
  - Anaconda uses `conda` to manage environments
  - `venv` comes with Python 3
  - Or, the `virtualenv` package

---

# Virtual environments with `conda`

![width:200px](assets/images/anaconda-logo.png) If familiar, you can use Anaconda  Navigator.

Alternatively, open your Terminal or Anaconda Prompt and use the `conda create` command to setup an empty virtual environment. For example,

```bash
conda create --name myenv python=3.6
```

where `python=3.6` specifies the Python version you want for the environment.

---

# Virtual environments with `conda`

To *activate* the environment at any time,

```bash
conda activate myenv
```

You can then install packages (e.g. `conda install scipy`).

To *deactivate* the environment,

```bash
conda deactivate
```

---

# Aside: `PATH`

What happens when we type `python` into the Terminal?

- The console searches your system `PATH` for the first script named `python`.

---

# Virtual environments with `venv`

- The simplest way to get started without `conda`
- Only works with Python 3



---
<!-- _class: lead -->

> Help! I updated Python and now my code is broken!

---

# <!--fit--> How do I manage different Python versions?
