!SLIDE
# Problem
## You want to search history for content

!SLIDE
## `git grep`

!SLIDE commandline smaller
## A "few" options

    $ git help grep
    ...
    SYNOPSIS
       git grep [-a | --text] [-I] [-i | --ignore-case] [-w | --word-regexp]
           [-v | --invert-match] [-h|-H] [--full-name]
           [-E | --extended-regexp] [-G | --basic-regexp]
           [-P | --perl-regexp]
           [-F | --fixed-strings] [-n | --line-number]
           [-l | --files-with-matches] [-L | --files-without-match]
           [(-O | --open-files-in-pager) [<pager>]]
           [-z | --null]
           [-c | --count] [--all-match] [-q | --quiet]
           [--max-depth <depth>]
           [--color[=<when>] | --no-color]
           [--break] [--heading] [-p | --show-function]
           [-A <post-context>] [-B <pre-context>] [-C <context>]
           [-W | --function-context]
           [-f <file>] [-e] <pattern>
           [--and|--or|--not|(|)|-e <pattern>...]
           [ [--exclude-standard] [--cached | --no-index | --untracked] | <tree>...]
           [--] [<pathspec>...]
    ...

!SLIDE bullets incremental
## Concise help

* doesn't exist (no `--help`)
* but, fake it with `-h`

!SLIDE commandline incremental small

    $ git grep -h
    usage: git grep [options] [-e] <pattern> [<rev>...] [[--] <path>...]

        --cached              search in index instead of in the work tree
        --no-index            finds in contents not managed by git
        --untracked           search in both tracked and untracked files
        --exclude-standard    search also in ignored files

        ...
        -h                    don't show filenames
        ...

!SLIDE
## A good default

`$ git grep --break --heading --line-number --ignore-case 'bisect'`

(add `--color` if not using `color.ui` in config)

!SLIDE commandline
## Tip
### Assign an alias

    $ git config --list
    ...
    [alias]
        find = grep --break --heading --line-number --ignore-case
    ...

!SLIDE commandline incremental

    $ git find 'bisect'
    trouble/bisect.md
    6:# `git bisect`
    15:    $ git bisect
    16:    Usage: git bisect [help|start|bad|good|skip|next|reset|visualize|replay|log|run]
    ...

    trouble/find_changed_file.md
    10:    $ git log -- trouble/bisect.md
    15:        Add note about database to bisect
    21:        flesh out bisect
    ...

!SLIDE
## Demo
### This slide deck
