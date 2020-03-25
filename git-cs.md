## Git

#### Save username and password for a repo

````bash
$ git config credential.helper store
$ git push http://example.com/repo.git
````


#### show number of codes per user in a repo
````bash
$ git ls-files | while read f; do git blame --line-porcelain $f | grep '^author '; done | sort -f | uniq -ic | sort -n
````

#### show number of changed lines between commits
````bash
$ git diff --stat HEAD^ HEAD
````

#### show number of changed files between commits
````bash
$ git show --name-only HEAD^..HEAD
````

#### fix .gitignore

````bash
$ git rm -r --cached .
$ git add .gitignore
$ git commit -m "fixing .gitignore"
````
