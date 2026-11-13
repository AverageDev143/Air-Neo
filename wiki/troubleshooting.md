# Troubleshooting

This page covers known setup notes for the current experimental build.

## `py` is not recognized

The Windows Python Launcher may not be installed or available on PATH.

1. Install Python 3 from [python.org](https://www.python.org/downloads/).
2. In the installer, enable the Python Launcher and add Python to PATH.
3. Close and reopen your terminal.
4. Try `py --version`, then `py run.py` from the Air Neo folder.

## First launch cannot install dependencies

The first launch uses pip to install packages from `requirements.txt` into the local `.venv` environment.

- Check that your PC is connected to the internet.
- Check whether a firewall or network policy is blocking Python or pip.
- Retry `py run.py` from the project folder.
- Include the full terminal error if it continues.

## Optional camera features are unavailable

Camera mode dependencies are separate from the core install. From the project folder, run:

```powershell
.venv\Scripts\python -m pip install -r requirements-camera.txt
```

## Known application limitations

The project README currently records these known issues:

- **Virtual window clicks:** Clicking on virtual windows is not currently functional.
- **Aspect ratio:** Aspect-ratio handling is unreliable and content may not display at the correct proportions.

These are known limitations, not necessarily problems with your PC or glasses.

## Reporting a bug

Open the [GitHub Issues](https://github.com/AverageDev143/Air-Neo/issues) page and include:

1. Glasses model.
2. Windows version.
3. Exact steps to reproduce the problem.
4. What you expected and what happened.
5. Full error text and screenshots, if relevant.

Do not include passwords, access tokens or other private information in an issue.
