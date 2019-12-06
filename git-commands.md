##Usefull git commands

# How to merge 2 repos into existing one

Add second repo to existing one
```
git remote add second-repo https://github.com/user/second-repo.git
git pull --allow-unrelated-histories second-repo master
```
Merge conflicts if exists

Commit merge

Remove second repo origin
```
git remote -v
git remote remove second-repo
```

Push all changes to existing repo origin
```
git push
```

Profit! :)

---



**merge new existing repo**
```
git remote add origin [repo]
git pull origin master --allow-unrelated-histories
```

**windows long path support**
```
git config --system core.longpaths true
```

**clean all stagged files**
```
git rm -r --cached .
git add .
```

**clone single branch**
```
git clone <url> --branch <branch> --single-branch
```

**delete branch locally and remotelly**
```
git branch -d <branch_name>
git push -d origin <branch_name>
```

**amend commit**
```
git commit --amend -m "New commit text"
```

**force push**
```
git push origin <your_branch_name> -f
```
