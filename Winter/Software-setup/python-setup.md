# `Python-setup.md`

## Python package managers and virtual environment managers

My workflow will likely be using `pyenv` to manage versions of python (install globally) and using `mamba` to manage virtual environments and download packages from the `conda-forge` channel. The latter can be downloaded in one installation called `mambaforge`.

<details>
<summary>pyenv instructions</summary>

### General `pyenv` installation

If you're using macOS or a Linux OS, go to the [🐙🐱 pyenv repo](https://github.com/pyenv/pyenv#installation) and follow the installation instructions.

If you're Windows, you have two options. To install directly on Windows, you can go to the [🐙🐱 pyenv-win](https://github.com/pyenv-win/pyenv-win#installation) repo and follow the installation instructions there. Otherwise, you can install WSL 2 (e.g. followin this [video](https://www.youtube.com/watch?v=IL7Jd9rjgrM) by David Bombal) and then install `pyenv` on your resulting Linux pseudo-virtual machine via WSL 2.

</details>

<details>
<summary>mambaforge instructions</summary>

### General `mambaforge` installation

Go to the [🐙🐱 miniforge repo](https://github.com/conda-forge/miniforge) and follow the instructions for your operating system to install `mamabaforge`. The installation files are in the [`mambaforge` section](https://github.com/conda-forge/miniforge#mambaforge), but it will make more sense if you at least skim the instructions in the [Install section](https://github.com/conda-forge/miniforge#install).

</details>

### `pyenv` + `mambaforge` usage instructions

Using "vanilla" python virtual environment managers like `venv` or `poety` with `pyenv` as well as `conda`/`mamba` environments can lead to conflicts. See the following link for one potential workflow that avoids those issues.

[🥞 Installing anaconda with pyenv, unable to configure virtual environment](https://stackoverflow.com/a/58045984)  
stack overflow answer  
[👤 Simba](https://stackoverflow.com/users/5101148/simba)

## Recommended VS Code/Codium extensions

<details>

### General extensions

- Python (official MS extension for Python support)
- AREPL for python (real-time output)

Source:
[🎥 Setting Up VSCode For Python Programming](https://www.youtube.com/watch?v=W--_EOzdTHk)  
[👤 Traversy Media](https://www.youtube.com/channel/UC29ju8bIPH5as8OGnQzwJyA)

### Code formatting

For each Python project you do in VS Code, run

```
pip install black isort
```

in your terminal. Create a local `settings.json` file and add the following to it:

```
"editor.formatting.provider": "black",
    "python.formatting.blackArgs": [
        "--line-length=119"
    ],
"python.sortImports.args": [
    "--profile=black",
],
"[python]": {
    "editor.codeActionsOnSave": {
        "source.organizeImports": true
    }
}
```

[🎥 Set up Python Black and isort on Visual Studio Code](https://www.youtube.com/watch?v=cG88P-MsdzQ)  
[👤 Very Academy](https://www.youtube.com/channel/UC1mxuk7tuQT2D0qTMgKji3w)

</details>

## Set up Jupyter with VS Code

<details>

Install the official "Jupyter" extension from Microsoft. More details might have to be added about using Jupyter inside VS Code.

</details>
