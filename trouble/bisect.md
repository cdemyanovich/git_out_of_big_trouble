!SLIDE
# Problem
## Where did a defect first occur?

!SLIDE
# `git bisect`

!SLIDE center
## Binary search
![binary search](images/binary_search.png)

!SLIDE commandline incremental small
## Short Help

    $ git bisect
    Usage: git bisect [help|start|bad|good|skip|next|reset|visualize|replay|log|run]

!SLIDE commandline incremental small
## Long Help

    $ git bisect help
    Usage: git bisect [help|start|bad|good|skip|next|reset|visualize|replay|log|run]

    git bisect help
    	print this long help message.
    git bisect start [--no-checkout] [<bad> [<good>...]] [--] [<pathspec>...]
    	reset bisect state and start bisection.
    git bisect bad [<rev>]
    	mark <rev> a known-bad revision.
    git bisect good [<rev>...]
    	mark <rev>... known-good revisions.
    git bisect skip [(<rev>|<range>)...]
    	mark <rev>... untestable revisions.
    git bisect next
    	find next bisection to test and check it out.
    git bisect reset [<commit>]
    	finish bisection search and go back to commit.
    git bisect visualize
    	show bisect status in gitk.
    git bisect replay <logfile>
    	replay bisection log.
    git bisect log
    	show bisect log.
    git bisect run <cmd>...
    	use <cmd>... to automatically bisect.

    Please use "git help bisect" to get the full man page.

!SLIDE bullets incremental
## Good or bad?

* `git bisect good`
* `git bisect bad`

!SLIDE bullets incremental
## Automation
### `git bisect run <script> <script-arguments>`

* `0` if commit is good
* `1-127` if commit is bad
* `125` if commit cannot be tested

!SLIDE
## Call off the search
### `git bisect reset`

!SLIDE center
![caution](images/caution.png)
### intentionally "bad" commits

!SLIDE
## Demo
### This slide deck
