# iil-dev

Development environment for working with [Intelligent Instruments Lab](https://iil.is) tools and repos

## Install

Clone the repository:

```sh
git clone https://github.com/Intelligent-Instruments-Lab/iil-dev.git
cd iil-dev
```

### `conda`

We manage Python versions, non-python dependencies and environments with `conda`. If you don't have an anaconda/miniconda/miniforge python install already, download [a miniforge installer](https://github.com/conda-forge/miniforge) and run it in a terminal. Afterwards, verify with `which python` -- it should have `miniforge` in the path.

Now set up the `conda` Python environment:

```sh
conda env create -f environment.yml
conda activate iil-dev-env
```

This will create a `conda` environment called `iil-dev` with the `poetry` tool installed.

You can make with editable installs of the git submodules in this repo by running `poetry install` inside of each project, e.g.

```sh
cd iil-dev/anguilla
git checkout main
poetry install
```

Each project is included as a git submodule. This means each project has its own separate git repo and history. You can also make commits to `iil-dev` which track *which commit* of each submodule is currently checked out. When you commit to `iil-dev`, you aren't committing your work on any of the projects -- you are committing a record of their current state *in git*.

So, always remember to commit your changes within each submodule. If you want to pin dev versions of several projects together, make a commit to `iil-dev` on your own branch. If you want to change this README or `environment.yml`, then commit to `main` of `iil-dev`.

#### Updating dependencies

We use `poetry` to manage other dependencies. To add a new dependency to a project, `cd` into the project (e.g., `anguilla`, `tolvera`) and use `poetry add`, or edit `pyproject.toml`, then use `poetry install`.

## Test

In a project directory, run `pytest`.

## Release

If you are an owner of a project on PyPI, to make a release:

1. within the project submodule, make a branch for the release, e.g. `git checkout -b v0.1.2`
2. edit `pyproject.toml` to change any path dependencies to normal pypi dependencies, and update the version number
3. use `poetry build` to make sure the project builds
4. add your PyPI API key to poetry using `poetry config pypi-token.pypi <token>`
5. double check the current version number and use `poetry publish --build`


## Contact

Developed by the [Intelligent Instruments Lab](https://iil.is/about). Get in touch to [collaborate](https://iil.is/collaborate):

 ◦ <a href="https://iil.is" target="_blank" rel="noopener" title="Intelligent Instrumets Lab">iil.is</a> ◦ 
<a href="https://facebook.com/intelligentinstrumentslab" target="_blank" rel="noopener" title="facebook.com">Facebook</a> ◦ 
<a href="https://instagram.com/intelligentinstruments" target="_blank" rel="noopener" title="instagram.com">Instagram</a> ◦ 
<a href="https://x.com/_iil_is" target="_blank" rel="noopener" title="x.com">X (Twitter)</a> ◦ 
<a href="https://youtube.com/@IntelligentInstruments" target="_blank" rel="noopener" title="youtube.com">YouTube</a> ◦ 
<a href="https://discord.gg/fY9GYMebtJ" target="_blank" rel="noopener" title="discord.gg">Discord</a> ◦ 
<a href="https://github.com/intelligent-instruments-lab" target="_blank" rel="noopener" title="github.com">GitHub</a> ◦ 
<a href="https://www.linkedin.com/company/intelligent-instruments-lab" target="_blank" rel="noopener" title="www.linkedin.com">LinkedIn</a> ◦ 
<a href="mailto:iil@lhi.is" target="_blank" rel="noopener" title="">Email</a> ◦ 

## Funding

The Intelligent Instruments project (INTENT) is funded by the European Research Council (ERC) under the European Union’s Horizon 2020 research and innovation programme (Grant agreement No. 101001848).
