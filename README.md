# Dotfiles

Dotfile management using [Dotbot][dotbot].
Structure of this repository is strongly inspired by [vsund][vsund].

Dependencies
------------

* bash
* git
* tmux
* vim
    * `fzf`
* xorg
* zsh
    * `nodejs`

Installation
------------

```bash
$ git clone --recursive https://github.com/vbrandl/dotfiles /path/to/install/location
```

For installing a predefined profile:

```bash
$ ./install-profile <profile> [<configs...>]
# see meta/profiles/ for available profiles
```

For installing single configurations:

```bash
$ ./install-standalone <configs...>
# see meta/configs/ for available configurations
```

The install script is idempotent - running it multiple times has no effect.

Making Local Customizations
---------------------------

You can make local customizations for some programs by editing these files:

* `git` : `~/.gitconfig_local`
* `tmux` : `~/.tmux_local.conf`
* `vim` : `~/.vimrc_local`
* `zsh` : `~/.zsh/zsh_zstyle` run before `.zshrc`, sets `zstyles`
* `zsh` : `~/.zsh/zsh_local` run after `.zshrc`, contains aliases and custom settings
* `zsh` : `~/.zsh/zsh_functions` run after `.zshrc`, contains only functions
* `zsh` : `~/.zsh/zsh_private` run after `.zshrc`, contains secrets

License
-------

This software is hereby released into the public domain. That means you can do
whatever you want with it without restriction. See [LICENSE][license] for details.

[dotbot]: https://github.com/anishathalye/dotbot
[dotfiles]: https://github.com/simgunz/dotfiles
[license]: LICENSE
[vsund]: https://github.com/vsund/dotfiles
