[![GitHub license](https://img.shields.io/github/license/hamelsmu/code_search.svg)](https://github.com/zhenyisx/cheat-sheet/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/hamelsmu/code_search.svg)](https://github.com/zhenyisx/cheat-sheet/issues)

# Cheat Sheet

This repo hosts all cheat sheets I have used. Please feel free to use them and leave feedbacks.


## Git

### Save username and password for a repo

````bash
$ git config credential.helper store
$ git push http://example.com/repo.git
````


### show number of codes per user in a repo
````bash
$ git ls-files | while read f; do git blame --line-porcelain $f | grep '^author '; done | sort -f | uniq -ic | sort -n
````

### show number of changed lines between commits
````bash
$ git diff --stat HEAD^ HEAD
````

### show number of changed files between commits
````bash
$ git show --name-only HEAD^..HEAD
````

### fix .gitignore

````bash
$ git rm -r --cached .
$ git add .gitignore
$ git commit -m "fixing .gitignore"
````

## jupyter notebook

### Access jupyter notebook remotely

#### server side

- start server
```bash
$ jupyter notebook --no-browser --port=XXXX
````
    
- list servers
````bash
$ jupyter notebook list
````

- kill servers
    1. get PID
    ````bash
    $ lsof -n -i4TCP:[port-number]
    ````
    2. kill by PID
    ````bash
    $ kill -9 [PID]
    ````

#### local side
````bash
$ ssh -N -f -L localhost:YYYY:localhost:XXXX serveruser@serverhost
````
start a browser and use `localhost:YYYY` as entry point. please note that one needs to reestablish the connection using above command if there is any break or reconnection or change of local network settings.

#### Reference
https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/
often times overleaf could be used for writing latex papers. The following references are also useful.

## latex

* latex [Symbols](https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols)
[Syntax](https://www.markdownguide.org/cheat-sheet/)

Please note that free version of overleaf doesn't support github. [Example](https://gist.github.com/jnaecker/da8c1846bc414594783978b66b6e8c83)

## create python package on pypi.

build project (note the version in setup.py)
```bash
python setup.py sdist bdist_wheel
```

upload to pypi test
```bash
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

install using pypi test (note the version)
```bash
pip install -i https://test.pypi.org/simple/ pyllama==0.0.4
```

[Working Example](https://towardsdatascience.com/build-your-first-open-source-python-project-53471c9942a7)


[NOT Working Example](https://www.codementor.io/@arpitbhayani/host-your-python-package-using-github-on-pypi-du107t7ku)

## python continuous integration tools

used for packaging and testing and publishing python package. check [this](https://docs.python-guide.org/scenarios/ci/) for some details.

### local
1. tox

### master/worker
1. buildbot
2. pygradle
3. travis ci
4. circleci

## shell

### check shell in use
```bash
$ echo $SHELL
```

### start up files for different shells

bash
* ~/.bashprofile
* ~/.bashrc

zsh
* ~/.zshenv
* ~/.zprofile
* ~/.zshrc
* ~/.zlogin
* ~/.zlogout

### check RHEL version
```bash
$ cat /etc/redhat-release
```

### check Linux kernel version
```bash
$ uname -r
```

### best zsh config 
[Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh)

## VS Code Development

[Remote Dev via SSH](https://code.visualstudio.com/docs/remote/ssh)
