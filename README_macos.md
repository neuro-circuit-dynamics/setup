# Python Set Up
### macOS — Python 3.12

## Overview
This guide walks you through creating a clean, isolated Python environment for lab work. The result is a self-contained environment that does not interfere with the system Python or any other project.

---

## Step 1 — Install Homebrew

Homebrew is a package manager for macOS. If you already have it, skip to Step 2.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

---

## Step 2 — Install Python 3.12

```bash
brew install python@3.12
```

---

## Step 3 — Verify the installation

```bash
python3.12 --version
```

You should see `Python 3.12.x`. If you do, you are ready to continue.

---

## Step 4 — Navigate to your working folder

```bash
cd ~/code
```

You can use any folder you prefer. The environment will be created inside it.

---

## Step 5 — Create the virtual environment

Replace `name_of_environment` with your choice:

```bash
python3.12 -m venv name_of_environment
```

---

## Step 6 — Activate the virtual environment

```bash
source name_of_environment/bin/activate
```

When activated, your terminal prompt will change to show the environment name:

```
(name_of_environment) user@machine:~$
```

This confirms you are working inside the environment.

---

## Step 7 — Install the required packages

```bash
python3.12 -m pip install -r https://raw.githubusercontent.com/neuro-circuit-dynamics/lab-setup/main/requirements.txt
```

---

## Step 8 — Verify the installation

```bash
python3.12 -m pip list
```

---

## Step 9 — Deactivate the environment

When you finish your session:

```bash
deactivate
```

Your terminal returns to the global system environment.
