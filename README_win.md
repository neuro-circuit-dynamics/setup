# Python Set Up
### Windows — Python 3.12

## Overview
This guide walks you through creating a clean, isolated Python environment for lab work. The result is a self-contained environment that does not interfere with the system Python or any other project.

> All commands below should be run in **PowerShell**. Search for it in the Start menu and open it normally (no need to run as administrator).

---

## Step 1 — Install Python 3.12

```powershell
winget install Python.Python.3.12
```

When installation finishes, **close and reopen PowerShell** before continuing.

---

## Step 2 — Verify the installation

```powershell
python --version
```

You should see `Python 3.12.x`. If you do, you are ready to continue.

---

## Step 3 — Navigate to your working folder

```powershell
cd ~\code
```

You can use any folder you prefer. The environment will be created inside it.

---

## Step 4 — Create the virtual environment

Replace `name_of_environment` with your choice:

```powershell
python -m venv name_of_environment
```

---

## Step 5 — Activate the virtual environment

```powershell
name_of_environment\Scripts\activate
```

When activated, your terminal prompt will change to show the environment name:

```
(name_of_environment) PS C:\Users\yourname\code>
```

This confirms you are working inside the environment.

> If you get a permissions error, run this first and then try again:
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

---

## Step 6 — Update pip

Before installing packages, update pip to the latest version:

```powershell
python -m pip install --upgrade pip
```

---

## Step 7 — Install the required packages

```powershell
python -m pip install -r https://raw.githubusercontent.com/neuro-circuit-dynamics/setup/main/requirements.txt
```

---

## Step 8 — Verify the installation

```powershell
python -m pip list
```

---

## Step 9 — Deactivate the environment

When you finish your session:

```powershell
deactivate
```

Your terminal returns to the global system environment.
