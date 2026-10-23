# Week 1, core 0: Set up your tools

This page comes before the first notebook, because creating an environment happens in a terminal, before any notebook can run. It is the one page of the course that is not a notebook.

Every notebook in this course runs in one of two places: on your own computer, in the course's `geol522` environment (opened in VS Code or in JupyterLab), or in Google Colab, in your browser. Pick one route for Week 1; you can switch later, and the notebooks are identical everywhere. If anything here fails, post in the Week 1 discussion thread with the exact error message: getting set up is part of Week 1's content, not a prerequisite for it.

## Getting the notebooks

Each week's materials are a folder with the notebooks (`.ipynb` files) and a landing page; the data are **not** in the folder, every notebook downloads what it needs into a `data/` folder beside itself the first time it runs. `[DECIDE: where students get the folders, for example a download button on the course site or the Canvas module for the week.]`

## Route A: Google Colab (about 15 minutes, nothing to install)

1. Go to [colab.research.google.com](https://colab.research.google.com) and sign in with your Illinois Google account.
2. *File → Upload notebook*, and choose the week's notebook file.
3. Run the first cell. On Colab it installs the one package Colab lacks (cartopy); on your own computer the same cell does nothing.
4. *Runtime → Run all* runs the notebook top to bottom, which is also the test that it is correct.
5. Colab has Google's Gemini assistant built in (a chat panel, code suggestions in empty cells, and an "Explain error" button under tracebacks); whether it is enabled depends on your account, and the course's AI policy applies to it like any other assistant.
6. Files the notebook downloads land in Colab's temporary storage and vanish when the session ends; the download cell simply fetches them again next time.
7. To hand in homework, *File → Download → Download .ipynb* and upload that file to Canvas.

Limits: a free Colab session times out after some hours of inactivity and has no GPU unless you ask for one (*Runtime → Change runtime type*); nothing before Week 6 needs a GPU.

## Route B: your own computer (one to two hours the first time)

Two parts: create the course environment once, then pick an editor to open the notebooks in. We recommend VS Code, because it runs notebooks well and is where most AI coding assistants live; JupyterLab is the plain alternative and is what the course text's menu names refer to.

### B1. Create the `geol522` environment (once)

1. Install **Miniforge**, a small conda distribution that uses the conda-forge channel: download the installer for your system from [github.com/conda-forge/miniforge](https://github.com/conda-forge/miniforge) and run it with the default options. On Windows, open the *Miniforge Prompt* from the Start menu afterwards; on macOS and Linux, open a new terminal.
2. Download the course environment file, `environment.yml` `[DECIDE: link]`, into a folder for the course.
3. In the terminal, in that folder:

   ```
   conda env create -f environment.yml
   ```

   This downloads about 2 GB (PyTorch, scikit-learn, cartopy, JupyterLab and the rest) and takes 10–20 minutes. The environment is named `geol522`; every editor below needs only that name.

### B2. VS Code (recommended)

1. Install [VS Code](https://code.visualstudio.com) and, from its Extensions view (the blocks icon in the left bar), the **Python** and **Jupyter** extensions published by Microsoft.
2. *File → Open Folder…* and choose the week's folder (or the whole course folder). Opening the folder, not just a file, is what lets VS Code find the `data/` folder next to each notebook. The first time you open a folder, VS Code asks whether you trust its authors: answer **Yes, I trust the authors**. In the alternative, Restricted Mode, the Python extension does not load, notebooks cannot run, and the kernel list offers nothing but "Install Python" (if you ever see that, click *Restricted Mode* at the bottom left of the window and choose *Trust*).
3. Open the week's first notebook. At the top right of the notebook, click **Select Kernel → Python Environments…** and pick **geol522** (it appears as `Python 3.12 ('geol522')` or similar). VS Code finds Miniforge environments on its own; if the list is empty, restart VS Code after creating the environment.
4. Click **Run All** in the notebook toolbar. The course text says *Restart kernel and run all cells* (JupyterLab's menu wording); in VS Code that is the **Restart** button followed by **Run All**, both in the same toolbar.
5. Every later session: open the folder, open the notebook, and check that the kernel name at the top right still says `geol522`; VS Code remembers it per notebook.
6. For a terminal inside VS Code (*Terminal → New Terminal*), choose the interpreter once with *View → Command Palette → Python: Select Interpreter → geol522*; new terminals then start with the environment activated.

AI assistants in VS Code: GitHub Copilot, Gemini Code Assist, Claude Code and others install as extensions and work inside the notebook editor, which is the most convenient way to use an assistant in this course (at the time of writing, Copilot has a free tier and a free student plan through GitHub Education; check what your account offers). Whatever you install, the course's AI policy is the same: the notebooks say which cells an assistant may write for you and which you write yourself, and every homework ends with a declaration of what you used.

### B3. JupyterLab (the plain alternative)

1. In the terminal, activate the environment and start JupyterLab:

   ```
   conda activate geol522
   jupyter lab
   ```

   A browser tab opens. Use its file browser to open the week's folder and the first notebook.
2. In the notebook, *Kernel → Restart kernel and run all cells*. If it runs to the end, you are set up.
3. Every later session: open the terminal, `conda activate geol522`, `jupyter lab`.

### Troubleshooting

- `conda: command not found` right after installing: close and reopen the terminal (Windows: use the Miniforge Prompt, not PowerShell or cmd).
- The environment creation fails part-way: run the same `conda env create` command again; it resumes.
- VS Code's kernel list shows only "Install Python" although Python is installed: the folder is open in Restricted Mode. Click *Restricted Mode* in the status bar (bottom left) and choose *Trust*; the kernel list fills a few seconds later. If it is still empty, wait a moment and open it again, the environment scan may not have finished.
- VS Code runs the notebook but a cell says a package is missing: the notebook is using the wrong kernel; click the kernel name at the top right and pick `geol522`.
- The first map (Week 1 lab) downloads a small coastline file; it needs an internet connection the first time.
- "Kernel died" on a laptop with little memory: close other programs and run the notebook again; the imagery weeks say at the top when a Colab GPU is the better route.

## Which route?

Colab if you want to start now, or if your computer is old or locked down by your employer. Your own computer if you want your work and data to persist between sessions, if you want an AI assistant inside your editor, or if you expect to use Python for your own projects after the course; VS Code is the editor to learn for that. Many students use both routes.
