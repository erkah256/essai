# essai

## sous titre

![Texte alternatif](index.jpg "texte pour le titre, facultatif")


   

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
[master (root-commit) f20a649] premier commit
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
[master 2323936] modif de f2
 1 file changed, 1 insertion(+)

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ echo "Troisième fichier" >> f3.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git add f3.txt
warning: LF will be replaced by CRLF in f3.txt.
The file will have its original line endings in your working directory.

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ status
bash: status: command not found

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "ajout de f3"
warning: LF will be replaced by CRLF in f3.txt.
The file will have its original line endings in your working directory.
[master a1ddad5] ajout de f3
 1 file changed, 1 insertion(+)
 create mode 100644 f3.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v2

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git mv f3.txt f4.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ status
bash: status: command not found

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git commit -am  "renommage de f3 en f4"
[master 966b22e] renommage de f3 en f4
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
[master df33cb0] suppression de f2
 1 file changed, 2 deletions(-)
 delete mode 100644 f2.txt

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git tag v4

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git log
commit df33cb0c916e424e901795b1aacb9d2f13d40724 (HEAD -> master, tag: v4)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:37 2018 +0200

    suppression de f2

commit 966b22e56eddd44f1d73efc274a61038c906275b (tag: v3)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:36 2018 +0200

    renommage de f3 en f4

commit a1ddad57a7aca4fe2e339277a6490c578cadfd38 (tag: v2)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:35 2018 +0200

    ajout de f3

commit 23239364862793051f98c339a2a0fc986fb909d9
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:35 2018 +0200

    modif de f2

commit f20a64951557b05d7794829d5c485134d5ed884f (tag: v1)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:34 2018 +0200

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
HEAD is now at 966b22e renommage de f3 en f4

Rudy@Hermes MINGW64 /d/masterCCI/Toto/bob (master)
$ git log
commit 966b22e56eddd44f1d73efc274a61038c906275b (HEAD -> master, tag: v3)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:36 2018 +0200

    renommage de f3 en f4

commit a1ddad57a7aca4fe2e339277a6490c578cadfd38 (tag: v2)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:35 2018 +0200

    ajout de f3

commit 23239364862793051f98c339a2a0fc986fb909d9
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:35 2018 +0200

    modif de f2

commit f20a64951557b05d7794829d5c485134d5ed884f (tag: v1)
Author: erkah256 <erkah256@gmail.com>
Date:   Sun Sep 30 20:26:34 2018 +0200

    premier commit

```
