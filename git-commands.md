##Usefull git commands

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
