# statistical_learning_edx
Companion code development for Statistical Learning course @edX

# Environment

## Create dirs
```
MBPdeAlexandre:~ alexandre.c.sousa$ mkdir documents/learning
MBPdeAlexandre:~ alexandre.c.sousa$ mkdir documents/learning/statistical_learning_edx
MBPdeAlexandre:~ alexandre.c.sousa$ cd documents/learning/statistical_learning_edx
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ mkdir .virtualenvs
```

## Clone repo and checkout to a new branch
```
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ git clone https://github.com/alexandredesousa/statistical_learning_edx.git
Cloning into 'statistical_learning_edx'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ cd statistical_learning_edx
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ git checkout -b dev_classes
Switched to a new branch 'dev_classes'
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ git branch -a
* dev_classes
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
```

## Create virtual environments for development
### Python
```
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ python --version
Python 2.7.10
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ python3.7 --version
Python 3.7.9
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ python3.7 -m venv .virtualenvs/sl
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$
```

### R
```
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ mkdir .virtualenvs/sl_r
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ R

> getwd()
[1] "/Users/alexandre.c.sousa/Documents/learning/statistical_learning_edx/statistical_learning_edx"
> setwd(".virtualenvs/sl_r")
> getwd()
[1] "/Users/alexandre.c.sousa/Documents/learning/statistical_learning_edx/statistical_learning_edx/.virtualenvs"

> renv::init(project = getwd(), bare=T, force=F)
* Project '~/Documents/learning/statistical_learning_edx/statistical_learning_edx/.virtualenvs/sl_r' loaded. [renv 0.12.2]
* renv activated -- please restart the R session.
> quit()
Save workspace image? [y/n/c]: n
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ 
```

## Activate and deactivate virtual environment
### Python
Activate 
```
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ . .virtualenvs/sl/bin/activate
(sl) MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ 
```
Deactivate
```
(sl) MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ deactivate
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$
```

### R
Activate
```
> renv::activate(project = ".virtualenvs/sl_r")
* Project '~/Documents/learning/statistical_learning_edx/statistical_learning_edx/.virtualenvs/sl_r' loaded. [renv 0.12.2]
```
Deactivate
```
> renv::deactivate()
* renv deactivated -- please restart the R session.
```

## Instantiate a script from the terminal
Recall to activate the proper environment, previous to run
### Python
```
(sl) MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ python src/py/py_ini.py
Hi, this is awkward
```

### R
```
MBPdeAlexandre:statistical_learning_edx alexandre.c.sousa$ Rscript src/R/r_ini.R
[1] "Hi, this is awkward"
```