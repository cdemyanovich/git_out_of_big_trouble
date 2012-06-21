!SLIDE
# Problem
## You lost a commit
### (or did you?)

!SLIDE
## `git reflog`

!SLIDE
## How do we lose commits?
### Delete them during interactive rebase

`# If you remove a line here THAT COMMIT WILL BE LOST.`

!SLIDE
## How do we lose commits?
### `git reset --hard <commit>`

!SLIDE bullets incremental
## Maintenance

* __manual__ with the `expire` or `delete` subcommands
* __semi-automatic__ with `git gc`
* __automatic__ if garbage collection runs

!SLIDE bullets incremental
## "Emergency fund"

* keeps entries for last __90 days__ if `git gc` runs
* see `git help gc` for options like `gc.reflogExpire`

!SLIDE
## Demo
### Artisan
