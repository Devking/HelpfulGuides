Use [`pyenv`](https://github.com/pyenv/pyenv) for easy Python version management.

```
# Install pyenv
brew upgrade
brew install pyenv

# Print the current version of Python being used
pyenv version

# List the versions of Python you can use
pyenv versions

# Set local version of Python to 3.8.2
pyenv local 3.8.2

# List available Python versions to install
pyenv install --list

# Install desired Python version
pyenv install 3.8.2
```

[Other pyenv commands](https://github.com/pyenv/pyenv/blob/master/COMMANDS.md).

Create a virtual environment using [`venv`](https://docs.python.org/3/library/venv.html). In Python 3, `venv` is included in the standard library.

```
# Creates a folder for the virtual environment
python -m venv venv

# Activate the virtual environment
. venv/bin/activate
```

Install the necessary packages using `pip`.

```
# Upgrade pip
pip install -U pip

# Install the Python library Flask
pip install Flask

# Save the dependencies of this project in requirements.txt
pip freeze > requirements.txt

# Install all the dependencies listed in requirements.txt
pip install -r requirements.txt
```

For `.gitignore`:

```
__pycache__/
venv/
```
