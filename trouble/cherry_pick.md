!SLIDE
# Problem
## You want a commit from another branch

!SLIDE
## `git cherry-pick`

!SLIDE bullets incremental
## Common options

* `-e, --edit`
* `-n, --no-commit`
* `-s, --signoff`

!SLIDE bullets incremental
## Sequencers

* `--continue`
* `--quit`
* `--abort`

!SLIDE
## Example

!SLIDE center
![before cherry-pick](images/18333fig0526-tn.png)

!SLIDE commandline smaller

    $ git cherry-pick e43a6fd3e94888d76779ad79fb568ed180e5fcdf
    Finished one cherry-pick.
    [master]: created a0a41a9: "More friendly message when locking the index fails."
     3 files changed, 17 insertions(+), 3 deletions(-)

!SLIDE center
![after cherry-pick](images/18333fig0527-tn.png)

!SLIDE center
## 5.3 Distributed Git - Maintaining a Project
### http://git-scm.com/book/en/Distributed-Git-Maintaining-a-Project
![Pro Git](images/pro_git.jpg)
