---

title: uv
date: 2025-10-05
tags: ["package manager", "python", "uv"]
description: An extremely fast Python package and project manager, written in Rust.

---

## Important Info

- [uv Official Link](https://docs.astral.sh/uv/)

## Download & Install

### macOS and Linux

- Installation Command: `curl -LsSf https://astral.sh.uv/install.sh | sh`
  - curl: downloads the install.sh script from astral website.

## How to

### Create Virtual Environment

1. Basic: `uv venv`
   1. creates virtual environment with default python and everything.
   2. creates a .venv directory in current directory.
2. With custom env directory name: `uv venv my_env`
   1. Specify a different directory directory name by it as an argument, like my_env in this case.
3. 