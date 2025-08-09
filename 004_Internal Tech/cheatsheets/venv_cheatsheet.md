## 🐍 .venv Cheatsheet – SIVERSE Edition

A quick-reference for managing Python virtual environments on your dev machine or during collaborative SIVIO development.

---

### 📦 Create a New Virtual Environment

```bash
python3 -m venv .venv
```

Creates a `.venv` folder in the current directory with an isolated Python environment.

---

### 🚀 Activate the Environment

**Linux/macOS**:

```bash
source .venv/bin/activate
```

**Windows (CMD)**:

```cmd
.venv\Scripts\activate.bat
```

**Windows (PowerShell)**:

```powershell
.venv\Scripts\Activate.ps1
```

---

### 🛑 Deactivate the Environment

```bash
deactivate
```

Returns to system Python.

---

### 📜 Install Dependencies from File

```bash
pip install -r requirements.txt
```

---

### 📦 Freeze Current Dependencies

```bash
pip freeze > requirements.txt
```

Captures a reproducible environment snapshot.

---

### 🔄 Auto-Activate with direnv (Optional)

Install direnv:

```bash
sudo apt install direnv
```

Add to `.envrc`:

```bash
layout python3
```

Enable it:

```bash
direnv allow
```

---

### 🔧 Helpful Commands

| Task                        | Command                                 |
| --------------------------- | --------------------------------------- |
| Show current Python path    | `which python`                          |
| Confirm pip is from `.venv` | `which pip` (should be `.venv/bin/pip`) |
| List installed packages     | `pip list`                              |
| Upgrade pip                 | `pip install --upgrade pip`             |
| Add `.venv/` to gitignore   | `echo .venv/ >> .gitignore`             |

---

### 🧠 Why Use `.venv`?

- Keeps dependencies **isolated per project**
- Avoids polluting **system Python**
- Simplifies **collaboration and deployment**
- Required for reproducible agent behaviors in **SIVERSE workflows**

---

### 📍 Troubleshooting

- ❗If `.venv/bin/activate` is missing, recreate with:
  ```bash
  python3 -m venv .venv
  ```
- 🌀 If things break, `rm -rf .venv` and start fresh
- ✅ Use `python -m pip install ...` to be explicit if needed

---

🧵 *A properly prepped **`.venv`** is the uniform of every professional dev. Suit up.* — Prof. Spaghetti

