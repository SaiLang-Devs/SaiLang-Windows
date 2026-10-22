# Building SaiLang for Windows

## Option 1: on GitHub (no installs needed)

1. Put this folder in a GitHub repository (see the steps below).
2. Open the **Actions** tab, choose **build-windows**, then **Run workflow**.
3. When it finishes, download the **SaiLang-windows** artifact. It contains
   `SaiLang-Setup-v1.0.0.exe`, the installer.

## Option 2: on your own Windows computer

1. Install Python 3.12 from python.org.
2. Install NSIS from nsis.sourceforge.io (it provides `makensis`).
3. Open a Command Prompt in this folder and run:
   ```
   python installer/build_installer.py
   ```
4. The programs are written to `dist\windows\`.

Tests: `set PYTHONPATH=src` then `python -m unittest discover -s tests -v`.
