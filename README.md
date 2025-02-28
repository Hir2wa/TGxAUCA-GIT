## ADAVANCED GIT EXERCISES 
### Challeng1
```bash 
Kubahos-iMac-2:Advanced-Git gymkubaho$  git add test1.md
Kubahos-iMac-2:Advanced-Git gymkubaho$  git commit -m  "initial file"
[main (root-commit) 47c0bb2] initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
Kubahos-iMac-2:Advanced-Git gymkubaho$  git add test2.md
Kubahos-iMac-2:Advanced-Git gymkubaho$  git   commit -m "create another file"
[main d348975] create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Kubahos-iMac-2:Advanced-Git gymkubaho$  git add test3.md
Kubahos-iMac-2:Advanced-Git gymkubaho$  git commit -m " create third  and  fourth files "
[main c2d09c8]  create third  and  fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git status
On branch main
nothing to commit, working tree clean
Kubahos-iMac-2:Advanced-Git gymkubaho$  git log 
commit c2d09c8959524305cbadaf3a81bfb56fcc072ec9 (HEAD -> main)
Author: Hir2wa <alainfabricehirwa@gmail.com>
Date:   Fri Feb 28 12:30:49 2025 +0200

     create third  and  fourth files

commit d348975b163bc4f39413b75cfa4bf8458cbf90b4
Author: Hir2wa <alainfabricehirwa@gmail.com>
Date:   Fri Feb 28 12:29:54 2025 +0200

    create another file

commit 47c0bb225247528ee8756615b159e2e5d2b68c68
Author: Hir2wa <alainfabricehirwa@gmail.com>
Date:   Fri Feb 28 12:29:05 2025 +0200

    initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ git add test4.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git commit --amend -m "create third and fourth files(added test4.md)"
[main 83bdcd3] create third and fourth files(added test4.md)
 Date: Fri Feb 28 12:30:49 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git status
On branch main
nothing to commit, working tree clean
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --online 
fatal: unrecognized argument: --online
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline 
83bdcd3 (HEAD -> main) create third and fourth files(added test4.md)
d348975 create another file
47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ 
```

####  Challenge 2
```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$  git rebase -i HEAD~2
[detached HEAD 5788fdd] create Second file
 Date: Fri Feb 28 12:29:54 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
Kubahos-iMac-2:Advanced-Git gymkubaho$ 
```
#### challenge 3
```bash 
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~2
interactive rebase in progress; onto 327fb1c
Last commands done (2 commands done):
   pick 1b3fdef initial commit
   squash 4296568 .
No commands remaining.
You are currently rebasing branch 'main' on '327fb1c'.
  (all conflicts fixed: run "git rebase --continue")
  ```


  #### challenge 4
  ```bash 
  Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline
327fb1c (HEAD)  Added README.md file
81dc92f create third and fourth files(added test4.md)
5788fdd create Second file
47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ git reset --soft 5788fdd

Kubahos-iMac-2:Advanced-Git gymkubaho$ git restore --staged test4.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git commit -m "Create third file"
[detached HEAD a3d3de5] Create third file
 2 files changed, 69 insertions(+)
 create mode 100644 README.md
 create mode 100644 test3.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git add test4.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git commit -m "Create fourth file"
[detached HEAD 448531c] Create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase --continue
You must edit all merge conflicts and then
mark them as resolved using git add
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline
448531c (HEAD) Create fourth file
a3d3de5 Create third file
5788fdd create Second file
47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ 


```

#### challenge 5
```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~2
[detached HEAD a871405] Create third and fourth files
 Date: Fri Feb 28 13:46:47 2025 +0200
 3 files changed, 69 insertions(+)
 create mode 100644 README.md
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated detached HEAD.
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline
a871405 (HEAD) Create third and fourth files
5788fdd create Second file
47c0bb2 initial file
```

####  challenge 6

```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ touch unwanted.txt
Kubahos-iMac-2:Advanced-Git gymkubaho$ echo "this is an unwanted commit." >unwanted.txt
Kubahos-iMac-2:Advanced-Git gymkubaho$ git add unwanted.txt
Kubahos-iMac-2:Advanced-Git gymkubaho$ git commit -m "unwanted commit "
[detached HEAD 29b1154] unwanted commit
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt

Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline 
29b1154 (HEAD) unwanted commit
a871405 Create third and fourth files
5788fdd create Second file
47c0bb2 initial file
```

####  challenge 7
```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline 
29b1154 (HEAD) unwanted commit
a871405 Create third and fourth files
5788fdd create Second file
47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~2
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~1
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.
Kubahos-iMac-2:Advanced-Git gymkubaho$ git stash
Saved working directory and index state WIP on (no branch): 29b1154 unwanted commit
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~1
error: nothing to do
Kubahos-iMac-2:Advanced-Git gymkubaho$ git rebase -i HEAD~2
Successfully rebased and updated detached HEAD.
```

#### challenge 8

```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ git  switch main
Switched to branch 'main'
Kubahos-iMac-2:Advanced-Git gymkubaho$ git cherry-pick --abort
error: no cherry-pick or revert in progress
fatal: cherry-pick failed
Kubahos-iMac-2:Advanced-Git gymkubaho$ git cherry-pick fccfe92
[main ac623f0] Implemented test 5
 Date: Fri Feb 28 14:43:58 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --online
fatal: unrecognized argument: --online
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --oneline
ac623f0 (HEAD -> main) Implemented test 5
4296568 .
1b3fdef initial commit
327fb1c  Added README.md file
81dc92f create third and fourth files(added test4.md)
5788fdd create Second file
47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ 
```
#### Challenge 9
```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --graph --oneline --all
* ac623f0 (HEAD -> main) Implemented test 5
* 4296568 .
* 1b3fdef initial commit
* 327fb1c  Added README.md file
* 81dc92f create third and fourth files(added test4.md)
| * d9eadd4 (ft/branch) Implemented test 5
| * fccfe92 Implemented test 5
| * ee55f6b create Second file
| * 7daa906 Create third and fourth files
| | *   2daa42a (refs/stash) WIP on (no branch): a871405 Create third and fourth files
| | |\  
| | | * 8054459 index on (no branch): a871405 Create third and fourth files
| | |/  
| | * a871405 Create third and fourth files
| |/  
|/|   
* | 5788fdd create Second file
|/  
* 47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ git log --graph --oneline --decorate --all
* ac623f0 (HEAD -> main) Implemented test 5
* 4296568 .
* 1b3fdef initial commit
* 327fb1c  Added README.md file
* 81dc92f create third and fourth files(added test4.md)
| * d9eadd4 (ft/branch) Implemented test 5
| * fccfe92 Implemented test 5
| * ee55f6b create Second file
| * 7daa906 Create third and fourth files
| | *   2daa42a (refs/stash) WIP on (no branch): a871405 Create third and fourth files
| | |\  
| | | * 8054459 index on (no branch): a871405 Create third and fourth files
| | |/  
| | * a871405 Create third and fourth files
| |/  
|/|   
* | 5788fdd create Second file
|/  
* 47c0bb2 initial file
Kubahos-iMac-2:Advanced-Git gymkubaho$ 
```
#### Challenge 10
Git's reflog (short for "reference log") is a powerful tool that allows you to track the history of branch references and HEAD (the pointer to the current commit). It records every change made to the tips of branches, whether you made a commit, switched branches, performed a rebase, or any other Git operation that moves the HEAD. Even operations that may seem to be destructive, like git reset, are recorded in the reflog.

```bash
Kubahos-iMac-2:Advanced-Git gymkubaho$ git reflog
ac623f0 (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
4296568 HEAD@{1}: checkout: moving from ft/branch to main
d9eadd4 (ft/branch) HEAD@{2}: commit (cherry-pick): Implemented test 5
fccfe92 HEAD@{3}: checkout: moving from main to ft/branch
4296568 HEAD@{4}: checkout: moving from ft/branch to main
fccfe92 HEAD@{5}: commit: Implemented test 5
ee55f6b HEAD@{6}: checkout: moving from ee55f6b3ea33eec16e583f99fa6ec4063cb4612d to ft/branch
ee55f6b HEAD@{7}: rebase (pick): create Second file
7daa906 HEAD@{8}: rebase (pick): Create third and fourth files
47c0bb2 HEAD@{9}: rebase (start): checkout HEAD~2
a871405 HEAD@{10}: rebase (start): checkout HEAD~2
29b1154 HEAD@{11}: commit: unwanted commit
a871405 HEAD@{12}: rebase (reword): Create third and fourth files
e64dbdc HEAD@{13}: rebase: fast-forward
5788fdd HEAD@{14}: rebase (start): checkout HEAD~2
e64dbdc HEAD@{15}: rebase (squash): Create third file
a3d3de5 HEAD@{16}: rebase (start): checkout HEAD~2
448531c HEAD@{17}: commit: Create fourth file
a3d3de5 HEAD@{18}: commit: Create third file
5788fdd HEAD@{19}: reset: moving to 5788fdd
b7723be HEAD@{20}: commit: Create third file
:
```