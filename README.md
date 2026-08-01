# Dotfiles

Symlinked by [mise](https://mise.jdx.dev/) `[dotfiles]`. See `mise.toml` and `mise.darwin.toml` for what maps where.

## Setup on a new machine

```bash
brew install mise
git clone git@github.com:raphaelerodellar/dotfiles.git ~/rcode/dotfiles
cd ~/rcode/dotfiles && ./install
```

Ghostty expects the JetBrainsMono Nerd Font: `brew install --cask font-jetbrains-mono-nerd-font`.

## Commands

```bash
./install                    # apply everything
mise bootstrap status        # what is out of sync
```

Files are symlinked, so editing them in the repo is enough.
