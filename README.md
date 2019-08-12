Useful additional Git commands
==============================

Description
-----------

This repository hosts a collection of miscellaneous extra Git commands (in the
form of scripts, mostly building on top of Git plumbing commands) that have
proved useful.

Installation
------------

Those scripts are supposed to be made available to your local Git installation
(either by copying them in a location on the `PATH` or by defining
[Git aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)) in
order to act as invokable custom Git commands.

Commands
--------

### git-disseminate ###

Usage: `git disseminate [A...B]`

**Finds non-merge commits in `A` but not in `B`** (that have not been
cherry-picked from `B`, limited to at most 1,000 commits) that contains
`!disseminate!` in their commit message, **and cherry-picks them to the current
branch.**

The `!disseminate!` tag does not need to be at the beginning of a new line and
can appear anywhere in the commit message body (as well as in the subject).

When `git disseminate` is called with no arguments, `A` defaults to `master`
and `B` to the current branch.

### git-gc-all-ferocious ###

Usage: `git gc-all-ferocious`

Performs a **very** aggressive GC! **Beware of data loss!**

See: <https://stackoverflow.com/a/14728706>

Contributing
------------

We welcome any kinds of positive contribution, mainly in two forms:

* [reporting bugs or issues](#reporting-issues)
* and [submitting patches](#submitting-patches)

### Development pre-requisites ###

Please install the following pre-requisites to contribute to this project.

1. [pre-commit](https://pre-commit.com) ([installation
   instructions](https://pre-commit.com/#install))
2. [ShellCheck](https://www.shellcheck.net) ([installation
   instructions](https://github.com/koalaman/shellcheck#installing))

### Optional tools ###

In addition to the [mandatory pre-requesites](#development-pre-requisites)
listed in the previous section, we found the following tools useful during
development.

#### Visual Studio Code Extensions ####

* [markdownlint](https://github.com/DavidAnson/vscode-markdownlint)
  (`davidanson.vscode-markdownlint`)
* [shellcheck](https://github.com/timonwong/vscode-shellcheck)
  (`timonwong.shellcheck`)

### Getting the source code ###

Considering that this project is a collection of scripts, chances are that if
you're reading this file, you already have a copy of the "source" code. Just
look for files starting by `git-` in the same directory as this `README`.

However, if you want to contribute to this project, you'll have to file a PR
with your changes on GitHub, against the official [Git
repository](https://github.com/xcomponent/git-commands), so it might be a good
idea to start by
[cloning](https://help.github.com/articles/cloning-a-repository) or
[forking](https://help.github.com/articles/fork-a-repo) it.

#### `pre-commit` hook setup ####

If you did not follow the instructions allowing you to [automatically setup the
`pre-commit` hook](https://pre-commit.com/#automatically-enabling-pre-commit-on-repositories)
when cloning a new Git repository, please run the `pre-commit install` command
at least once after cloning (see the
[pre-requisites](#development-pre-requisites) above if you did not install
pre-commit yet).

### Reporting issues ###

TODO

### Submitting patches ###

TODO
