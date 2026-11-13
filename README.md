# Air Neo

**A software-first spatial display experience for RayNeo AR glasses.**

Air Neo is a free PC application exploring how to bring features such as 3DoF-style spatial viewing, virtual screens, and 3D content to RayNeo glasses—without requiring an expensive external processing accessory.

The long-term goal is to make a flexible, approachable experience inspired by products such as InAir OS, while keeping the software free and running on a PC.

> **Project vision:** Make spatial displays more accessible through software, better window management, and useful customization.

## Documentation

Read the [Air Neo Wiki](https://averagedev143.github.io/Air-Neo/wiki/) for installation, compatibility, troubleshooting, and development guides.

## Why Air Neo?

RayNeo glasses provide a capable display, but getting a more immersive desktop experience can involve additional hardware or third-party software. Existing options can be useful, but they may involve trade-offs in price, usability, workflow, or customization.

Air Neo is an attempt to explore a better approach: a PC-based experience designed around how people actually use their desktop.

## Existing alternatives

These are the alternatives that motivated the project. The notes below reflect the project's author's experience and are not intended as a comprehensive review.

### Airpin

Airpin can provide a shifted 2D display, but in the author's experience it does not provide the spatial 3DoF experience they were looking for and offers fewer features than some alternatives.

### Parallel

Parallel offers spatial 3DoF support and multiple windows. However, the author's experience highlighted a few workflow and comfort issues:

- During setup, the display can be split into sections, with a central blind spot until windows are configured.
- Some desktop elements, such as dock items, can feel awkwardly positioned.
- Opening additional applications from within the workspace can interrupt the workflow.

### InAir Pod

The InAir Pod offers a more complete hardware-based experience, including remote PC access and additional display customization such as window size and distance.

The drawback for this project is the extra hardware and its cost, which can be a significant addition to the price of the glasses themselves.

## Project goals

Air Neo aims to build toward the following capabilities:

- **Spatial viewing:** Explore practical 3DoF-style display positioning where supported by the glasses and available hardware/software interfaces.
- **Virtual screens:** Make it easier to work with multiple desktop windows.
- **Window customization:** Adjust window size, distance, and placement.
- **Usable multitasking:** Open and manage applications without constantly leaving the workspace.
- **Clean interface:** Keep controls intuitive and the desktop experience uncluttered.
- **Software-first approach:** Avoid requiring a dedicated external processing accessory for the core PC experience.

These are project goals, not a claim that every feature is currently implemented or supported on every RayNeo model.

## Compatibility

Air Neo is intended for use with RayNeo AR glasses and a Windows PC. Exact compatibility depends on the glasses model, its available interfaces, and the state of the relevant software support.

The **RayNeo Air 3S Pro** is one of the devices considered during the project's development. Do not assume that every feature works on every model.

## Running on Windows

1. Download the project ZIP from GitHub.
2. Extract the ZIP to a folder on your PC.
3. Open the extracted **Air Neo** folder.
4. Open a terminal in that folder. In File Explorer, you can click the address bar, type `cmd`, and press Enter, or use **Open in Terminal**.
5. Run:

   ```powershell
   py run.py
   ```

On the first launch, the launcher creates a local Python virtual environment in the project folder (the `.venv` folder) and installs the packages listed in `requirements.txt`. It then starts the application. Later launches reuse that environment.

**First-launch notes:**
- Install Python 3 before running the command. The Windows Python Launcher (`py`) must be available in your terminal.
- An internet connection is needed on the first launch so pip can download the required packages.
- If `py` is not recognized, reinstall Python from [python.org](https://www.python.org/downloads/) and enable the option to add Python to PATH / install the Python Launcher.

## Python requirements

The Windows launcher installs the core dependencies automatically from `requirements.txt`:

| Package | Minimum version | Purpose |
|---|---:|---|
| Python 3 | — | Runs the application and its launcher |
| PySide6 | 6.6 | Application interface |
| PyOpenGL | 3.1.7 | OpenGL rendering |
| NumPy | 1.24 | Numerical and image data processing |
| mss | 9.0 | Desktop/window screen capture |

You do **not** need to install the Python packages manually when using `py run.py`; the launcher handles the core requirements in its private `.venv`.

### Optional camera mode

Camera mode (camera background, hand tracking, and the virtual keyboard) uses additional packages that are kept separate from the core install:

- `opencv-python-headless>=4.8`
- `mediapipe>=0.10.14`

To install these optional packages into the app's virtual environment on Windows, run:

```powershell
.venv\Scripts\python -m pip install -r requirements-camera.txt
```

The core application does not require these optional camera packages.

## Development

Air Neo is an evolving project. Features, compatibility, and setup instructions may change as development progresses. Check the repository's source and commit history for the latest implementation details.

## Contributing

Ideas, bug reports, and contributions are welcome. When reporting an issue, include:

- Your RayNeo glasses model
- Your Windows version
- What you were trying to do
- What happened and what you expected
- Any relevant error messages or screenshots

## Disclaimer

Air Neo is an independent community project and is not affiliated with, endorsed by, or officially supported by RayNeo or InAir. Product and company names are used only to identify compatible devices and related software.

## Testing status and known issues

Air Neo has been tested successfully on **Windows with the RayNeo Air 3S Pro**.

The following issues are currently known:

- **Virtual window clicks do not work:** Clicking on virtual windows is currently not functional.
- **Aspect ratio:** Aspect-ratio handling is currently unreliable and may not display content at the correct proportions.

These issues are known limitations and may be addressed in future updates. This testing result does not guarantee compatibility with other glasses models or PC configurations.

---

*Air Neo — bringing a more flexible spatial desktop experience to your glasses.*
