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

## Ruby on Intel Macs

mise has no precompiled Ruby for Intel Macs, and `mise/config.toml` sets `ruby.compile = false`, so link the Intel builds from [rv](https://github.com/spinel-coop/rv-ruby) for each version you need:

```bash
v=4.0.10; d=~/.local/share/rubies/ruby-$v
mkdir -p $d && curl -fsSL https://github.com/spinel-coop/rv-ruby/releases/download/rubies/ruby-$v.ventura.tar.gz | tar xz -C $d --strip-components=2
mise link ruby@$v $d
```

## Commands

```bash
./install                    # apply everything
mise bootstrap status        # what is out of sync
```

Files are symlinked, so editing them in the repo is enough.
