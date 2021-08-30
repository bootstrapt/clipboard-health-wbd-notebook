# Clipboard Health WBD Practice Problem Notebook
This repo contains files related to the Clipboard Health WBD practice problem I was asked to complete. Does not include raw data file. 

## Installation
This notebook was developed and tested on a MacBook Air running macOS 11.5.1.
##### Install pyenv and pipenv
```
$ brew install pyenv
$ pyenv install 3.9.5
$ pyenv shell 3.9.5
$ pip install --user --upgrade pipenv
```
##### Clone project and install dependencies
```
$ git clone git@github.com:bootstrapt/clipboard-health-wbd-notebook.git
$ cd clipboard-health-wbd-notebook
$ export SYSTEM_VERSION_COMPAT=1
$ pipenv install notebook pandas numpy scipy seaborn matplotlib
```
_Note: see references re: SYSTEM_VERSION_COMPAT_

## Run Notebook
From project root:
```
$ pipenv shell
$ jupyter notebook
```

## Publish to Github Pages
To publish this notebook, update `./html/index.html` and push to github. 
##### Scripted
```
$ sudo chmod +x ./publish_to_github_pages.sh
$ ./publish_to_github_pages.sh
```
##### Manually
```
$ jupyter nbconvert pricing_wbd.ipynb --no-input --no-prompt --to=html --output-dir=docs --output=index.html
$ git commit -am "updated ./docs/index.html with latest notebook output"
$ git push
```

## References
- [Note on SYSTEM_VERSION_COMPAT](https://github.com/pypa/pipenv/issues/4564#issuecomment-756625303)
