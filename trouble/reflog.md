!SLIDE
# Problem
## You lost a commit
### (or did you?)

!SLIDE
## `git reflog`

!SLIDE bullets incremental
## How do we lose commits?

* delete a commit during interactive rebase
* `git reset --hard <commit>`

!SLIDE bullets incremental
## reflog Maintenance

* tracks _every_ time the tip of a branch changes
* can be pruned with the `expire` or `delete` subcommands

!SLIDE bullets incremental
## reflog Maintenance
### (continued)

* will be pruned if `git gc` runs
* keeps entries for last 90 days if `git gc` runs
* see `git help gc` for options like `gc.reflogExpire`

!SLIDE
## Demo
### Artisan
