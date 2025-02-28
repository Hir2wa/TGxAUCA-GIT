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