# Dotfiles

## Install

```
git clone --recursive git@github.com:codepotato/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
script/bootstrap
```

Periodically run `dot`, this will keep your environment updated. You can find the file at `bin/dot`.

Also do not forget to install `oh-my-zsh` if you haven't already, this is based on assumption you have it installed. If not the program does install zsh, but you'll need to run `zsh` in your terminal to see changes.

If not, run `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` and restartyour terminal.

## iTerm2 Settings

1. Preferences > Profiles
2. Under the *Colors* tab *Load Presets* using `~/.dotfiles/iterm2/cobalt2.itermcolors`
3. Under the *Text* tab change the font for each type (*Regular* and *Non-ASCII*) to '**Inconsolata for Powerline**' found under `~/.dotfiles/fonts`.

## components

There's a few special files in the hierarchy.

- **bin/**: Anything in `bin/` will get added to your `$PATH` and be made
  available everywhere.
- **Brewfile**: This is a list of applications for [Homebrew Cask](http://caskroom.io) to install: things like Chrome and 1Password and Adium and stuff. Might want to edit this file before running any initial setup.
- **topic/\*.zsh**: Any files ending in `.zsh` get loaded into your
  environment.
- **topic/path.zsh**: Any file named `path.zsh` is loaded first and is
  expected to setup `$PATH` or similar.
- **topic/completion.zsh**: Any file named `completion.zsh` is loaded
  last and is expected to setup autocomplete.
- **topic/\*.symlink**: Any files ending in `*.symlink` get symlinked into
  your `$HOME`. This is so you can keep all of those versioned in your dotfiles
  but still keep those autoloaded files in your home directory. These get
  symlinked in when you run `script/bootstrap`.

## Credits

Forked from [iWader/dotfiles][fork]:  http://iwader.co.uk
Cobalt2 theme from [wesbos/Cobalt2-iterm][theme]
Completion from [zsh-users/zsh-completions][zsh-completions]

## License

MIT. See [LICENSE][license] file for more info.

[fork]: https://github.com/holman/dotfiles
[theme]: https://github.com/wesbos/Cobalt2-iterm
[zsh-completions]: https://github.com/zsh-users/zsh-completions
[license]: LICENSE.md
