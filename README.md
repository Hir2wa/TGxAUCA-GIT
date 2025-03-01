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

#### Challenge 2

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

#### challenge 6

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

#### challenge 7

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

## Part2:

#### challenge 1:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git branch ft/new-feature
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git branch
  ft/new-feature
* main
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git  switch   ft/new-feature
Switched to branch 'ft/new-feature'
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git  switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

#### challenge 2:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> echo "Implemented core functionality for new feature" > feature.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git add feature.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>   git   commit  -m " added new file "
[ft/new-feature 991d089]  added new file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
```

#### challenge 3:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>   git  switch main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> echo "This is the updated project readme." > readme.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git add readme.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>  git commit -m "added new file on main branch"
[main 956d657] added new file on main branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git log --oneline
956d657 (HEAD -> main) added new file on main branch
2ec3819 (origin/main, origin/HEAD) Done Part1: Advanced Git
ac623f0 Implemented test 5
4296568 .
1b3fdef initial commit
327fb1c  Added README.md file
81dc92f create third and fourth files(added test4.md)
5788fdd create Second file
47c0bb2 initial file
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

#### challenge 4:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>  git remote -v
origin  https://github.com/Hir2wa/TGxAUCA-GIT.git (fetch)
origin  https://github.com/Hir2wa/TGxAUCA-GIT.git (push)
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

#### challenge 5:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git merge ft/new-feature
>>
Merge made by the 'ort' strategy.
 feature.txt | Bin 0 -> 98 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>

(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git add .
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>   git commit -m "Merged from ft/new-feature"
[main acfaf9b] Merged from ft/new-feature
 1 file changed, 122 insertions(+), 36 deletions(-)
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>  git push origin main
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 12 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 1.94 KiB | 397.00 KiB/s, done.
Total 11 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 1 local object.
To https://github.com/Hir2wa/TGxAUCA-GIT.git
   2ec3819..acfaf9b  main -> main
```

#### challenge 5:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git  branch
  ft/new-feature
* main
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git branch -d ft/new-feature
Deleted branch ft/new-feature (was 991d089).

(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git branch
* main
```

#### challenge 6: Creating a Branch from a Commit

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git log --oneline
acfaf9b (HEAD -> main, origin/main, origin/HEAD) Merged from ft/new-feature
cafc1c9 Merge branch 'ft/new-feature'
956d657 added new file on main branch
991d089  added new file
2ec3819 Done Part1: Advanced Git
ac623f0 Implemented test 5
4296568 .
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git checkout -b ft/new-branch-from-commit 956d657
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git stash
Saved working directory and index state WIP on main: acfaf9b Merged from ft/new-feature
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git checkout -b ft/new-branch-from-commit 956d657
Switched to a new branch 'ft/new-branch-from-commit'
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git branch
* ft/new-branch-from-commit
  main
```

#### challenge 7:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git merge ft/new-branch-from-commit
Already up to date.
```

#### challenge 8:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git switch   ft/new-branch-from-commit
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git  stash
Saved working directory and index state WIP on main: acfaf9b Merged from ft/new-feature
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git switch   ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git rebase main
Successfully rebased and updated refs/heads/ft/new-branch-from-commit.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git merge ft/new-branch-from-commit
Already up to date.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

#### challenge 9:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git add README.md
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git commit -m  "updated README.md"
[main c91fb2b] updated README.md
 1 file changed, 92 insertions(+)
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.10 KiB | 1.10 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Hir2wa/TGxAUCA-GIT.git
   acfaf9b..c91fb2b  main -> main
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

#### challenge 10:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git push origin main
To https://github.com/Hir2wa/TGxAUCA-GIT.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Hir2wa/TGxAUCA-GIT.git'
To https://github.com/Hir2wa/TGxAUCA-GIT.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Hir2wa/TGxAUCA-GIT.git'
hint: Updates were rejected because the tip of your current branch is behind
error: failed to push some refs to 'https://github.com/Hir2wa/TGxAUCA-GIT.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git pull origin main
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git pull origin main
From https://github.com/Hir2wa/TGxAUCA-GIT
 * branch            main       -> FETCH_HEAD
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git push  origin main
Everything up-to-date
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT>
```

for pushing and resolving conflict i used texteditor that why i go to push and i see everything is updated

## part3:

#### challenge 1:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git  stash
Saved working directory and index state WIP on main: 62b6e28 Solved 10 challenges of Part2
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git stash  list
stash@{0}: WIP on main: 62b6e28 Solved 10 challenges of Part2
stash@{1}: WIP on main: acfaf9b Merged from ft/new-feature
stash@{2}: WIP on main: acfaf9b Merged from ft/new-feature
```

#### challenge 2:

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git stash apply
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

#### challenge 3:

###### This is a new feature update from ft/conflict-branch.

```bash
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git checkout -b ft/conflict-branch
Switched to a new branch 'ft/conflict-branch'
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git add README.md
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git commit -m "Updated README from ft/conflict-branch"
[ft/conflict-branch 0305aeb] Updated README from ft/conflict-branch
 1 file changed, 37 insertions(+)
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git commit -m "Updated README from main branch"
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

(base) PS C:\Users\Aime\Desktop\TGxAUCA-GIT> git merge ft/conflict-branch
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git commit -m "resolved  conflicts "
[main 0eaca6e] resolved  conflicts
 1 file changed, 25 insertions(+), 3 deletions(-)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
```

#### challenge 4:

```bash
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (ft/conflict-branch)
$ git  commit -m "simulated  conflict"
[ft/conflict-branch d9e8636] simulated  conflict
 1 file changed, 536 deletions(-)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (ft/conflict-branch)
$ echo "Hello from conflict-branch" >> README.md
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (ft/conflict-branch)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (ft/conflict-branch)
$ git commit -m "Updated README in conflict-branch"
[ft/conflict-branch 91079d4] Updated README in conflict-branch
 1 file changed, 1 insertion(+)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (ft/conflict-branch)
$ git switch main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git merge conflict-branch
merge: conflict-branch - not something we can merge
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git mergetool

This message is displayed because 'merge.tool' is not configured.
See 'git mergetool --tool-help' or 'git help config' for more details.
'git mergetool' will now attempt to use one of the following tools:
opendiff kdiff3 tkdiff xxdiff meld tortoisemerge gvimdiff diffuse diffmerge ecmerge p4merge araxis bc codecompare smerge emerge vimdiff nvimdiff
No files need merging
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git config --global merge.tool vscode
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git config --global mergetool.vscode.cmd "code --wait $MERGED"
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git stash apply
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git mergetool
Merging:
README.md

Normal merge conflict for 'README.md':
  {local}: modified file
  {remote}: modified file
node:internal/modules/cjs/loader:1235
  throw err;
  ^

Error: Cannot find module 'C:\Users\Aime\anaconda3\Library\c\Users\Aime\AppData\Local\Programs\Microsoft VS Code\resources\app\out\cli.js'
    at Module._resolveFilename (node:internal/modules/cjs/loader:1232:15)
    at Module._load (node:internal/modules/cjs/loader:1058:27)
    at c._load (node:electron/js2c/node_init:2:16955)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:188:12)
    at node:internal/main/run_main_module:28:49 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []


Node.js v20.18.1
README.md seems unchanged.
Was the merge successful [y/n]? y
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
```

#### challenge 5:

```bash
$ git  log --oneline
3f46298 (HEAD -> main) solved Challenge 4
7e84267 updated README.md
0eaca6e resolved  conflicts
cc61017 (origin/main, origin/HEAD) Merge branch 'ft/conflict-branch'
6ac9dba Updated README from main branch
0305aeb Updated README from ft/conflict-branch
62b6e28 Solved 10 challenges of Part2
db82d94 Merge branch 'main' of https://github.com/Hir2wa/TGxAUCA-GIT
136e5e4  Resolved conflict from  remote branch
9c3359d  README.md
c91fb2b updated README.md
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git checkout 62b6e28
Note: switching to '62b6e28'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 62b6e28 Solved 10 challenges of Part2
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((62b6e28...))
$ git commit -am "Experimenting in Detached HEAD"
HEAD detached at 62b6e28
nothing to commit, working tree clean
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((62b6e28...))
$ git add README.md
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((62b6e28...))
$ git commit -am "Experimenting in Detached HEAD"
[detached HEAD 2a5fc68] Experimenting in Detached HEAD
 1 file changed, 1 insertion(+), 1 deletion(-)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((2a5fc68...))
$ git log --oneline --graph --decorate
* 2a5fc68 (HEAD) Experimenting in Detached HEAD
* 62b6e28 Solved 10 challenges of Part2
*   db82d94 Merge branch 'main' of https://github.com/Hir2wa/TGxAUCA-GIT
|\
| * 9c3359d  README.md
* | 136e5e4  Resolved conflict from  remote branch
|/
* c91fb2b updated README.md
* acfaf9b (ft/new-branch-from-commit) Merged from ft/new-feature
*   cafc1c9 Merge branch 'ft/new-feature'
|\
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((2a5fc68...))
$ git branch experiment-branch
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT ((2a5fc68...))
$ git checkout main
Previous HEAD position was 2a5fc68 Experimenting in Detached HEAD
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)

```

#### challenge 6:

```bash
//Accidently  deleted the codes  that why i provided  codes  only

touch .gitignore
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git add .gitignore
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git commit -m "Added .gitignore to exclude temporary files"
[main e2f5a3a] Added .gitignore to exclude temporary files
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$
```

#### challenge 7:

```bash
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git tag v1.0
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
$ git push origin v1.0
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 12 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (13/13), 6.09 KiB | 891.00 KiB/s, done.
Total 13 (delta 7), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
To https://github.com/Hir2wa/TGxAUCA-GIT.git
 * [new tag]         v1.0 -> v1.0
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
```

#### challenge 8:

```bash
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git tag v1.1
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git tag
v1.0
v1.1
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git tag -d v1.1
Deleted tag 'v1.1' (was e2f5a3a)
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git tag
v1.0
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
```

#### challenge 9:

```bash
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
$ git push --all origin
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 833 bytes | 277.00 KiB/s, done.
Total 8 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/Hir2wa/TGxAUCA-GIT.git
   cc61017..e2f5a3a  main -> main
 * [new branch]      experiment-branch -> experiment-branch
 * [new branch]      ft/conflict-branch -> ft/conflict-branch
 * [new branch]      ft/new-branch-from-commit -> ft/new-branch-from-commit
←]633;P;Cwd=C:/Users/Aime/anaconda3/Library/c/Users/Aime/Desktop/TGxAUCA-GIT(base)
Aime@Aimeb MINGW64 ~/Desktop/TGxAUCA-GIT (main)
```
// Testing  for 10th challenge
