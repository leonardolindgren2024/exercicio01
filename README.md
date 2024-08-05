a:
    $echo 01 > arquivo.txt

b: 
    $git add arquivo.txt
    $git status

c:
    $git commit -m "git add example - arquivo.txt"

d:
    $echo 02 > arquivo.txt

e:
    $git diff

f:
    $git add arquivo.txt
    $git status

g:
    $git diff

h:
    $echo 03 > arquivo.txt
    
i:
    $git diff

j:
    $git restore arquivo.txt
    $git status

k:
    $git commit -m "meu segundo commit - arquivo.txt modificado"

l:
    $vi .gitignore

m:
    $echo Olá, CI/CD > novo.txt
    $git status

SAÍDAS DOS COMANDOS:

eonardo.lindgren@DM-002814 MINGW64 /c/mba
$ cd exercicio01/

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ echo 01 > arquivo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git add arquivo.txt 
warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.      

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt


leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git commit -m "git add example - arquivo.txt“
> 
> 
> ^C


leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git commit -m "git add example - arquivo.txt"
[main 6d65583] git add example - arquivo.txt
 Committer: Leonardo Lindgren <leonardo.lindgren@vocedm.com.br>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ echo 02 > arquivo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git diff
warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git add arquivo.txt 
warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git status 
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt


leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git diffin
git: 'diffin' is not a git command. See 'git --help'.

The most similar command is
        diff-index

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git diff

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git diff

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ echo 03 > arquivo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git diff
warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git restore exercicio01
error: pathspec 'exercicio01' did not match any file(s) known to git

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git restore exercicio01
error: pathspec 'exercicio01' did not match any file(s) known to git

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git restore arquivogit .txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt
.txt


leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git commit -m "meu segundo commit - arquivo.txt modificado"
[main 3c39ba8] meu segundo commit - arquivo.txt modificado
 Committer: Leonardo Lindgren <leonardo.lindgren@vocedm.com.br>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ vi .gitignore

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ vi .gitignore

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ echo Olá, CI/CD > novo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        novo.txt

nothing added to commit but untracked files present (use "git add" to track)

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git push
info: please complete authentication in your browser...
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.    
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 581 bytes | 96.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/leonardolindgren2024/exercicio01.git
   4a872a3..3c39ba8  main -> main

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git log
commit 3c39ba8e6601c50b552903cd305692365b9dbe1d (HEAD -> main, origin/main, origin/HEAD)
Author: Leonardo Lindgren <leonardo.lindgren@vocedm.com.br>
Date:   Mon Aug 5 20:02:20 2024 -0300

    meu segundo commit - arquivo.txt modificado

commit 6d6558342d8bb66d6ac8a8449887bace124b228a
Author: Leonardo Lindgren <leonardo.lindgren@vocedm.com.br>
Date:   Mon Aug 5 19:54:43 2024 -0300

    git add example - arquivo.txt

commit 4a872a3be02b155460406ad76973c1703aae7116
Author: leonardolindgren2024 <leonardo.lindgren@aluno.faculdadeimpacta.com.br>
Date:   Mon Aug 5 19:28:39 2024 -0300

    Initial commit

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git add .gitignore 
warning: in the working copy of '.gitignore', LF will be replaced by CRLF the next time Git touches it

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git add novo.txt 
warning: in the working copy of 'novo.txt', LF will be replaced by CRLF the next time Git touches it

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
        new file:   novo.txt


leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git commit -m "encerrando o exercicio e git push"
[main 0aae097] encerrando o exercicio e git push
 Committer: Leonardo Lindgren <leonardo.lindgren@vocedm.com.br>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 2 files changed, 2 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 novo.txt

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 388 bytes | 77.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/leonardolindgren2024/exercicio01.git
   3c39ba8..0aae097  main -> main

leonardo.lindgren@DM-002814 MINGW64 /c/mba/exercicio01 (main)
$