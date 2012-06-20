!SLIDE
# Problem
## You want to split in-progress changes into several commits

!SLIDE
## `git add`

!SLIDE bullets
## Two options

* `-i, --interactive`
* `-p, --patch`

!SLIDE code smaller

    $ git add -i
               staged     unstaged path
      1:    unchanged        +1/-1 trouble/add_interactive.md

    *** Commands ***
      1: status	  2: update	  3: revert	  4: add untracked
      5: patch	  6: diff	  7: quit	  8: help
    What now> p
               staged     unstaged path
      1:    unchanged        +1/-1 trouble/add_interactive.md
    Patch update>> 1
               staged     unstaged path
    * 1:    unchanged        +1/-1 trouble/add_interactive.md
    Patch update>>

!SLIDE code smaller

    diff --git a/trouble/add_interactive.md b/trouble/add_interactive.md
    index 43c1717..ea061a2 100644
    --- a/trouble/add_interactive.md
    +++ b/trouble/add_interactive.md
    @@ -6,7 +6,7 @@
     ## `git add`

     !SLIDE bullets
    -## Two options
    +## Two common options

     * `-i, --interactive`
     * `-p, --patch`
    Stage this hunk [y,n,q,a,d,/,e,?]? ?

!SLIDE smaller

    y - stage this hunk
    n - do not stage this hunk
    q - quit; do not stage this hunk nor any of the remaining ones
    a - stage this hunk and all later hunks in the file
    d - do not stage this hunk nor any of the later hunks in the file
    g - select a hunk to go to
    / - search for a hunk matching the given regex
    j - leave this hunk undecided, see next undecided hunk
    J - leave this hunk undecided, see next hunk
    k - leave this hunk undecided, see previous undecided hunk
    K - leave this hunk undecided, see previous hunk
    s - split the current hunk into smaller hunks
    e - manually edit the current hunk
    ? - print help

!SLIDE code smaller

    diff --git a/trouble/add_interactive.md b/trouble/add_interactive.md
    index 43c1717..ea061a2 100644
    --- a/trouble/add_interactive.md
    +++ b/trouble/add_interactive.md
    @@ -6,7 +6,7 @@
     ## `git add`

     !SLIDE bullets
    -## Two options
    +## Two common options

     * `-i, --interactive`
     * `-p, --patch`
    Stage this hunk [y,n,q,a,d,/,e,?]? y

!SLIDE code smaller

    *** Commands ***
      1: status	  2: update	  3: revert	  4: add untracked
      5: patch	  6: diff	  7: quit	  8: help
    What now> q
    Bye.
    $ git status
    # On branch master
    # Changes to be committed:
    #   (use "git reset HEAD <file>..." to unstage)
    #
    #	modified:   trouble/add_interactive.md
    #
