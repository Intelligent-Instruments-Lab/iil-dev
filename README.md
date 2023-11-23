# iil-dev

Development environment for working with [Intelligent Instruments Lab](https://iil.is) tools and repos

## Install

Clone the repository:

```sh
git clone https://github.com/Intelligent-Instruments-Lab/iil-dev.git
cd iil-dev
```

### `conda`

We manage python dependencies with `conda`. If you don't have an anaconda/miniconda python install already, download [the miniconda installer](https://docs.conda.io/en/latest/miniconda.html) or `brew install --cask miniconda` on macOS. Afterwards, verify with `which python` -- it should have `miniconda` in the path.

Now set up the `conda` Python environment:

```sh
conda env create -f environment.yml
conda activate iil-dev
```

This will install all dependencies in a `conda` environment called `iil-dev`, with editable installs of the git submodules in this repo so that you can edit them.

#### Updating `conda` dependencies

Add new dependencies to `environment.yml`, then run:

```sh
conda env update -f environment.yml
```

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
