# Dotfiles

Symlinked by [mise](https://mise.jdx.dev/) `[dotfiles]`. See `mise.toml` and `mise.darwin.toml` for what maps where.

## Setup on a new machine

```bash
curl https://mise.run | sh
git clone git@github.com:raphaelerodellar/dotfiles.git ~/rcode/dotfiles
cd ~/rcode/dotfiles && ./install
```

Ghostty expects the JetBrainsMono Nerd Font. Download it from [nerdfonts.com](https://www.nerdfonts.com/font-downloads) and open the `.ttf` files to install them.

System packages such as ffmpeg, ghostscript and vips come from [MacPorts](https://www.macports.org/install.php). `zsh/zprofile` puts `/opt/local/bin` first in `PATH`.

## Commands

```bash
./install                    # apply everything
mise bootstrap status        # what is out of sync
```

Files are symlinked, so editing them in the repo is enough.
