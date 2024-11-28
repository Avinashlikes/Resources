## Git Commandds

<details><summary> Git Config. </summary>

> Git Config.

```
git config --global user.name "Avinash Thakur"
git config --global user.email "avinash_thakur@company.com"
git config --global merge.tool p4merge
git config --global mergetool.p4merge.path "C:\Program Files\Perforce\p4merge.exe"
git config --global mergetool.prompt false
```
</details>
  
<details><summary> Git clone/delete a branch.</summary>
 
  > Git clone/delete a branch.

```
git clone <url>
git clone --branch <branch_name> <url>   
git branch <branch-name>
git branch -d <branch-name>
git branch --list
```
</details>

<details><summary> Git Commit.</summary>

  > Git Commit.

```
git commit -m "message"
```
</details>

<details><summary>  Git Push.</summary>

  > Git Push.

```
git push <remote> <branch-name>  
git push origin <branch_name>
```
</details>

<details><summary> Git amend the code in existing commit.</summary>

  > Git amend the code in existing commit.

```
git commit --amend
git commit --amend --no-edit
git push -f origin your_branch
```
</details>

<details><summary> Git Reset last commit that is not pushed.</summary>

  > Git Reset last commit that is not pushed.

```
git reset HEAD~1
git reset --hard HEAD~1
```
</details>

<details><summary> Git Pull.</summary>

  > Git Pull.

```
git pull <remote>  
git pull <remote>  <master> 
```
</details>
<details><summary> Git diff commit.</summary>

  > Git diff commit.

```
git diff COMMIT
git diff COMMIT~ COMMIT
```
</details>

