# `info-winter-prep.md`

## Setting up Python on Windows

### Use `pyenv` for managing python versions

Go to the [`pyenv` repo](https://github.com/pyenv/pyenv) (macOS or Linux) or the [`pyenv-win` repo](https://github.com/pyenv-win/pyenv-win/) (Windows) and install `pyenv` by following the `README.md`.
I'm ony windows and followed the instructions using `chocolatey` since that seemed to be the least painful way to deal with environmental variables.

### Install Python with `pyenv`

Run

```
pyenv install -l
```

to see a list of available python versions and install the version of your choosing by running

```
pyenv install {version}
```

Then run

```
pyenv global {version}
pyenv rehash
```

to set this version of Python as your global default.

### Setup and test `pyenv` installation with VS Code/Codium

Follow the steps in the video below from `9:59` to `12:02`

[🎥 How to Install and Run Multiple Python Versions on Windows 10/11 | pyenv & virtualenv Setup Tutorial](https://www.youtube.com/watch?v=HTx18uyyHw8&t=9m59s)

The issue I ran into was that the VS Codium terminal didn't seem to detect python, i.e.

```
python --version
```

would return an error that `python` wasn't detected in the VS Codium (PowerShell) terminal but was detected in the stand-alone PowerShell terminal opened outside of VS Codium.

However, following the steps the two minute portion of the video allowed me to run a simple hello world script. So `pyenv` may be functioning as intended and preventing global configs of python from conflicting with "local" environments in VS Codium.

### Install and configure anaconda to not conflict with `pyenv`

Install anaconda by downloading the installer from [here](https://www.anaconda.com/products/individual).

Refer to the instructions and links below to see how to use `pyenv` and `anaconda` without conflicts.

[🥞 Installing anaconda with pyenv, unable to configure virtual environment](https://stackoverflow.com/a/58045984)  
stack overflow answer  
[👤 Simba](https://stackoverflow.com/users/5101148/simba)
