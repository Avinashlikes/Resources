<details><summary> GIT commands </summary>

> Git Config.

```
git config --global user.name "Avinash Thakur"
git config --global user.email "avinash_thakur@company.com"
git config --global merge.tool p4merge
git config --global mergetool.p4merge.path "C:\Program Files\Perforce\p4merge.exe"
git config --global mergetool.prompt false
```

> Git clone/delete a branch.

```
git clone <url>
git clone --branch <branch_name> <url>   
git branch <branch-name>
git branch -d <branch-name>
git branch --list
```

> Git Commit.

```
git commit -m "message"
```

> Git Push.

```
git push <remote> <branch-name>  
git push origin <branch_name>
```

> Git amend the code in existing commit.

```
git commit --amend
git commit --amend --no-edit
git push -f origin your_branch
```

> Git Reset last commit that is not pushed.

```
git reset HEAD~1
git reset --hard HEAD~1
```

> Git Pull.

```
git pull <remote>  
git pull <remote>  <master> 
```

> Git diff commit.

```
git diff COMMIT
git diff COMMIT~ COMMIT
```

