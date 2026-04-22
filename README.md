# deeplearning-study-material

Storing my study material for courses completed in deeplearning.ai here.

## Python environment setup

This project has been verified with Python 3.11 in a local virtual environment.

If Python 3.11 is not installed, install it first:

```powershell
winget install Python.Python.3.11
```

Then run these commands from the project root in PowerShell to create the virtual environment and install the required packages:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\python.exe -m pip install --upgrade pip
.\.venv\Scripts\python.exe -m pip install numpy ipywidgets ipykernel
.\.venv\Scripts\python.exe -m ipykernel install --user --name deeplearning-study-material --display-name "Python (.venv)"
```

If `.venv` already exists, you can reuse it and reinstall or update the required packages with:

```powershell
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install numpy ipywidgets ipykernel
python -m ipykernel install --user --name deeplearning-study-material --display-name "Python (.venv)"
```

If PowerShell blocks activation, run this once in the same terminal session and try again:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Before running any Jupyter notebook, make sure the selected kernel is `Python (.venv)` so the notebook uses the packages installed in this project's virtual environment.

## Notes

- The virtual environment uses an already installed Python interpreter. `venv` does not install Python by itself.
- If `py -3.11` is not available after installation, close and reopen PowerShell and try again.
- In VS Code, use the notebook kernel picker in the top-right corner and select `Python (.venv)` before running cells.
- The current notebook imports `numpy`, `ipywidgets`, and a local `quiz` module. If `quiz.py` is missing, the notebook will still need that course helper file to run fully.
