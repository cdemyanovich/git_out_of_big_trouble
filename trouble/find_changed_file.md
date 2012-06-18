!SLIDE
# Problem
## You want to know which commits changed a file

!SLIDE
## `git log -- <path>`

!SLIDE commandline incremental

    $ git log -- trouble/bisect.md
    commit 00a439874d7199f49d12068133fcf956c1c675a5
    Author: Craig Demyanovich <cdemyanovich@gmail.com>
    Date:   Sun Jun 17 13:25:41 2012 -0500

        Add note about database to bisect

    commit 06951596948555c32caf3ab16aaf6043cc8b1436
    Author: Craig Demyanovich <cdemyanovich@gmail.com>
    Date:   Sat Jun 16 22:36:52 2012 -0500

        flesh out bisect

    commit f339e7b867c9fb768f8925b1ac9943fb8f2a8f72
    Author: Craig Demyanovich <cdemyanovich@gmail.com>
    Date:   Sat Jun 16 20:08:46 2012 -0500

        Rough draft of bisect

!SLIDE commandline incremental

    $ git log -p -- trouble/bisect.md
    commit 00a439874d7199f49d12068133fcf956c1c675a5
    Author: Craig Demyanovich <cdemyanovich@gmail.com>
    Date:   Sun Jun 17 13:25:41 2012 -0500

        Add note about database to bisect

    diff --git a/trouble/bisect.md b/trouble/bisect.md
    index ce84d0f..c91667d 100644
    --- a/trouble/bisect.md
    +++ b/trouble/bisect.md
    @@ -68,6 +68,10 @@
     ![caution](images/caution.png)
     ### intentionally "bad" commits

    +!SLIDE center
    +![caution](images/caution.png)
    +### What about the database at each checkout?
    +
     !SLIDE
     ## Demo
     ### This slide deck
    ...
