## Git

:camel:#### Save username and password for a project

```bash
$ git config credential.helper store
$ git push http://example.com/repo.git
```


#### show number of codes per user in a repo

    $ git ls-files | while read f; do git blame --line-porcelain $f | grep '^author '; done | sort -f | uniq -ic | sort -n
    
#### fix .gitignore

```bash
$ git rm -r --cached .
$ git add .gitignore
$ git commit -m "fixing .gitignore"
```
