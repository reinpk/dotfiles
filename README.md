# Dotfiles

My OS X dotfiles.

## Getting started

### Prerequisites

* Git (1.7+)

### Installation

This will create symlinks for most of the files.  The
`.gitconfig` file is copied to the HOME directory so that any private git
configuration taking place in `~/.extra` is not accidentally committed.

```bash
git clone git://github.com/reinpk/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
bash bootstrap.sh
```

N.B. This will overwrite any existing dotfiles in your HOME and `.vim`
directories that have the same names as those found in this repository.

### Updating

This must be done whenever you make a change to `.gitconfig` or pull from the
remote repo.

```bash
cd ~/.dotfiles
bash bootstrap.sh
```


## Custom OS X defaults

When setting up a new Mac, you may want to customise your OS X defaults after
installing the dotfiles.

```bash
bash .osx
```


## Adding local and private configurations

You can create a `~/.bash_profile.local` file to add private and custom
commands without the need to fork this repository. Any commands included in
this file will not be under version control or committed to a public
repository. If `~/.bash_profile.local` exists, it will be sourced for inclusion
in `bash_profile`.

Here is an example `~/.bash_profile.local`:

```bash
# PATH exports
PATH=$PATH:~/.gem/ruby/1.8/bin
export PATH

# Git credentials
# Not under version control to prevent people from
# accidentally committing with your details
GIT_AUTHOR_NAME="Nicolas Gallagher"
GIT_AUTHOR_EMAIL="nicolas@example.com"
GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"
GIT_COMMITTER_EMAIL="$GIT_AUTHOR_EMAIL"
# Set the credentials (modifies ~/.gitconfig)
git config --global user.name "$GIT_AUTHOR_NAME"
git config --global user.email "$GIT_AUTHOR_EMAIL"
```


## Custom bash prompt

I use the  [Solarized theme](https://github.com/altercation/solarized) for the standard OSX terminal.

Screenshot:

![](https://github.com/altercation/solarized/raw/master/img/solarized-vim.png)

## Acknowledgements

Inspiration and code was taken from many sources, including:

* [@mathiasbynens](https://github.com/mathiasbynens) (Mathias Bynens)
  [https://github.com/mathiasbynens/dotfiles](https://github.com/mathiasbynens/dotfiles)
* [@tejr](https://github.com/tejr) (Tom Ryder)
  [https://github.com/tejr/dotfiles](https://github.com/tejr/dotfiles)
* [@gf3](https://github.com/gf3) (Gianni Chiappetta)
  [https://github.com/gf3/dotfiles](https://github.com/gf3/dotfiles)
* [@cowboy](https://github.com/cowboy) (Ben Alman)
  [https://github.com/cowboy/dotfiles](https://github.com/cowboy/dotfiles)
