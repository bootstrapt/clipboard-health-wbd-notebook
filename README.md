# Clipboard Health WBD Practice Problem Notebook
This repo contains files related to the Clipboard Health WBD practice problem I was asked to complete. I opted not to include the raw data file. 

## Installation
This notebook was developed and tested on a MacBook Air running macOS 11.5.1 and python 3.9.5 (using pyenv). Install pyenv and initialize in your current shell.
```
$ brew install pyenv
$ pyenv install 3.9.5
$ pyenv shell
$ git clone git@github.com:bootstrapt/clipboard-health-wbd-notebook.git
```

## Running
To run the notebook yourself, just run `jupyter notebook` after cloning the git project.
```
$ cd clipboard-health-wbd-notebook
$ jupyter notebook
```

## Publishing to Github Pages
To publish this notebook, update `./html/index.html` and push to github. 
```
$ rm -f ./docs/index.html
$ jupyter nbconvert pricing_wbd.ipynb --no-input --no-prompt --to=html --output-dir=docs --output=index.html
$ git commit -am "updated ./docs/index.html with latest notebook output"
$ git push
```
