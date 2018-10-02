# Essai

```bash
Rudy@Hermes MINGW64 /d/masterCCI/Toto
$ mkdir bob

Rudy@Hermes MINGW64 /d/masterCCI/Toto
$ cd bob

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob
$ git init
Initialized empty Git repository in D:/masterCCI/Toto/bob/.git/

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo "Premier fichier" >> f1.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo "Second fichier" >> f2.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo ls >> liste.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git add f1.txt
warning: LF will be replaced by CRLF in f1.txt.
The file will have its original line endings in your working directory.

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git add f2.txt
warning: LF will be replaced by CRLF in f2.txt.
The file will have its original line endings in your working directory.

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git add liste.txt
warning: LF will be replaced by CRLF in liste.txt.
The file will have its original line endings in your working directory.

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   f1.txt
        new file:   f2.txt
        new file:   liste.txt


Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am "premier commit"
warning: LF will be replaced by CRLF in f1.txt.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in f2.txt.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in liste.txt.
The file will have its original line endings in your working directory.
[master (root-commit) 21c07c2] premier commit
 3 files changed, 3 insertions(+)
 create mode 100644 f1.txt
 create mode 100644 f2.txt
 create mode 100644 liste.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v1

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo "Second fichier version 2" >> f2.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   f2.txt

no changes added to commit (use "git add" and/or "git commit -a")

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "modif de f2"
warning: LF will be replaced by CRLF in f2.txt.
The file will have its original line endings in your working directory.
[master a643457] modif de f2
 1 file changed, 1 insertion(+)

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo "Troisième fichier" >> f3.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git add f3.txt
warning: LF will be replaced by CRLF in f3.txt.
The file will have its original line endings in your working directory.

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   f3.txt


Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "ajout de f3"
[master a317aa4] ajout de f3
 1 file changed, 1 insertion(+)
 create mode 100644 f3.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v2

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git mv f3.txt f4.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        renamed:    f3.txt -> f4.txt


Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "renommage de f3 en f4"
[master 059e0a0] renommage de f3 en f4
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename f3.txt => f4.txt (100%)

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v3

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git rm f2.txt
rm 'f2.txt'

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        deleted:    f2.txt


Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "suppression de f2"
[master 94d98a3] suppression de f2
 1 file changed, 2 deletions(-)
 delete mode 100644 f2.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v4

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git log
commit 94d98a30bc2220e519ea8aa14286adc34e444e32 (HEAD -> master, tag: v4)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:25 2018 +0200

    suppression de f2

commit 059e0a0707668efba55841ad7c33561a764bf146 (tag: v3)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:25 2018 +0200

    renommage de f3 en f4

commit a317aa45c036bb472e52d250e60a10d271b626c2 (tag: v2)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:24 2018 +0200

    ajout de f3

commit a643457c17e7c6cb4d28da55d5eb0a1e2cc1f971
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:23 2018 +0200

    modif de f2

commit 21c07c2be5ce03bd1463e5a91839e7af95e0b330 (tag: v1)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:22 2018 +0200

    premier commit

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git reset v2
Unstaged changes after reset:
D       f2.txt
D       f3.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        deleted:    f2.txt
        deleted:    f3.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        f4.txt

no changes added to commit (use "git add" and/or "git commit -a")

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git reset --hard v3
HEAD is now at 059e0a0 renommage de f3 en f4

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git log
commit 059e0a0707668efba55841ad7c33561a764bf146 (HEAD -> master, tag: v3)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:25 2018 +0200

    renommage de f3 en f4

commit a317aa45c036bb472e52d250e60a10d271b626c2 (tag: v2)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:24 2018 +0200

    ajout de f3

commit a643457c17e7c6cb4d28da55d5eb0a1e2cc1f971
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:23 2018 +0200

    modif de f2

commit 21c07c2be5ce03bd1463e5a91839e7af95e0b330 (tag: v1)
Author: erkah256 <erkah256@gmail.com>
Date:   Tue Oct 2 20:57:22 2018 +0200

    premier commit

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ ^C

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ ^C

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)


```
