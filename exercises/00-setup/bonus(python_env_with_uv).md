# Setting up a Python environment with uv

## What is uv?

uv is a simple and fast way to manage Python environments. It is significantly faster than conda and it is easier to use. The installation process is over the terminal but it is generally easier than installing conda. 

The main advantage of conda over uv is that conda can also manage things beyond Python packages — for example, NVIDIA graphics card drivers, which become important in advanced machine learning work.

You don't need to install uv to follow this course. Conda is perfectly sufficient. We wanted to include an intro into uv, since it is growing in popularity and will become more importante every year.

## Installing uv

Follow the installation instructions on the [official uv website](https://docs.astral.sh/uv/getting-started/installation/) based on the operating system that you are using.

## Creating a virtual environment

Open your terminal, navigate to your project folder, and run:

```bash
uv venv --python 3.12
```

This creates a `.venv` folder in your current directory. uv will automatically download Python 3.12 if it is not already installed on your system.

## Activating the environment

On **Mac / Linux**:
```bash
source .venv/bin/activate
```

On **Windows**:
```powershell
.venv\Scripts\activate
```

Your terminal prompt will show `(.venv)` to confirm the environment is active.

## Installing packages

```bash
uv pip install jupyter jupyterlab numpy scipy pandas matplotlib seaborn plotly scikit-learn ipywidgets tqdm
```

## Launching Jupyter Lab

```bash
jupyter lab
```

Shut it down with **Ctrl+C** in the terminal when you are done.

## Re-opening JupyterLab in future sessions

Each time you open a new terminal, reactivate your environment before launching Jupyter:

```bash
cd path/to/your/project
source .venv/bin/activate        # Mac / Linux
# or: .venv\Scripts\activate     # Windows
jupyter lab
```
