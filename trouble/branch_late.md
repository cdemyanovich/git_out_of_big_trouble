!SLIDE commandline incremental
# Problem
## You are working on `master`

!SLIDE commandline incremental
## `git pull --rebase`

    $ git add -A
    $ git commit -m "Add ability to sign in/out"
    $ git pull --rebase
    $ git push

!SLIDE commandline incremental
## `git checkout -b <new-branch-name>`

    $ git checkout -b <new-branch-name>
    $ git commit -m "Add ability to sign in/out"
    $ git checkout master
    $ git merge <new-branch-name>
    $ git push

