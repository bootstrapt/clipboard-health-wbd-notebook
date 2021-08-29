# Clipboard Health WBD Practice Problem Notebook
This repo contains files related to the Clipboard Health WBD practice problem I was asked to complete. I opted not to include the raw data file. 

## Installation
This notebook was developed and tested on a MacBook Air running macOS 11.5.1 and python 3.9.5 (using pyenv).
##### Install pyenv
```
$ brew install pyenv
$ pyenv install 3.9.5
$ pyenv shell
```
##### Clone project and install dependencies
```
$ git clone git@github.com:bootstrapt/clipboard-health-wbd-notebook.git
$ cd clipboard-health-wbd-notebook
$ pip install notebook pandas numpy scipy seaborn matplotlib
```

## Runtime
To run the notebook yourself, just run `jupyter notebook` after cloning the git project.
```
$ cd clipboard-health-wbd-notebook
$ jupyter notebook
```

## Publishing to Github Pages
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
