# Some cool git commands

* Show which files compose commit
    ```
    git log --stat
    ```

* Ammend commit but do not stop for editing  
    ```bash
    git commit --amend --no-edit
    ```

* Remove untracked files 
    ```bash
    git clean -f
    ```

* Delete remote branch/tag
    ```bash
    git push --delete origin <branch/tag>
    ```

* Update origin url 
    ```bash
    git remote set-url origin <new-url>
    ```

* List branchs [not] merged until the current commit
    ```bash
    git branch --no-merged/--merged [commit] 
    ```

* Force push but check if remote has new additions. If yes, do not push
    ```bash
    git push --force-with-lease
    ```

* Import (copy) commit from another branch
    ```bash
    git cherry-pick <commit>
    ```

* How to find the commit that introduced a BUG:
    ```bash
    git bisect start          # start binary search

    git bisect good <commit>  # indicates good start point of code
    git bisect bad <commit>   # indicates bad point of code

    git bisect good/bad       # indicate to git whether the commit it is showing has the bug or not

    # at the end of the algorithm git gives you the bad commit (and checkout to it): "<sha1> is the first bad commit ..."

    git bisect reset          # back to normal
    ```
