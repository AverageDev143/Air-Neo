# Getting started

This guide covers the current experimental Air Neo Windows package.

## What you need

- A Windows PC.
- Python 3 installed.
- The Windows Python Launcher (`py`) available in your terminal.
- An internet connection for the first launch, so the launcher can install the required packages.
- Compatible RayNeo AR glasses for device testing. See [Compatibility](compatibility.md).

## Download and extract

1. Open the [latest Air Neo release](https://github.com/AverageDev143/Air-Neo/releases/latest).
2. Download **Air-Neo-0.79-Windows.zip**.
3. Extract the ZIP to a folder you can easily find.
4. Open the extracted Air Neo folder in File Explorer.

## Launch the application

1. Open the extracted folder.
2. Click the File Explorer address bar, type `cmd`, and press Enter. You can also use **Open in Terminal**.
3. Run:

   ```powershell
   py run.py
   ```

On first launch, the launcher creates a local Python virtual environment in the project folder (`.venv`) and installs the packages from `requirements.txt`. Later launches reuse that environment.

## First-launch notes

- Install Python 3 if it is not already installed.
- During installation, enable the Python Launcher and the option to add Python to PATH.
- The first launch needs internet access for pip to download dependencies.
- Core packages are installed by the launcher; you do not need to install them manually.

## Optional camera mode

Camera mode features, including the camera background, hand tracking and virtual keyboard, use optional packages. To install them into the app's environment, run this from the project folder:

```powershell
.venv\Scripts\python -m pip install -r requirements-camera.txt
```

These optional packages are not required for the core application.

## Need help?

If startup fails, see [Troubleshooting](troubleshooting.md). When reporting a problem, include your Windows version, glasses model, the command you ran and the complete error text.
