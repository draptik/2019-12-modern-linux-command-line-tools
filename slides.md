---
title: ░▒▓ modern linux command line tools ▓▒░
author: patrick @drechsler frank @yooogan / Softwerkskammer 2019-12
patat:
    pandocExtensions:
        - patat_extensions
        - autolink_bare_uris
        - emoji
    incrementalLists: false
    wrap: true
    margins:
        left: 6
        right: 4
    theme:
        header: [bold]
        emph: [vividBlue, onVividBlack, italic]
        strong: [bold, dullMagenta, onVividBlack]
        codeBlock: [dullRed]
    images:
        backend: 'w3m'
        path: '/usr/lib/w3m/w3mimgdisplay'
---

<!--

# Patat demos

## Emojis

- requires `pandocExtensions: emoji`
- use Emoji Shortcodes: https://www.webfx.com/tools/emoji-cheat-sheet/
- Examples: :smiley:, :thumbsup:, :white_check_mark:, :heavy_check_mark:, :ballot_box_with_check:, :collision:

## Ascii art generator

- http://patorjk.com/software/taag/
-->

```text

███╗   ███╗ ██████╗ ██████╗ ███████╗██████╗ ███╗   ██╗
████╗ ████║██╔═══██╗██╔══██╗██╔════╝██╔══██╗████╗  ██║
██╔████╔██║██║   ██║██║  ██║█████╗  ██████╔╝██╔██╗ ██║
██║╚██╔╝██║██║   ██║██║  ██║██╔══╝  ██╔══██╗██║╚██╗██║
██║ ╚═╝ ██║╚██████╔╝██████╔╝███████╗██║  ██║██║ ╚████║
╚═╝     ╚═╝ ╚═════╝ ╚═════╝ ╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝

██╗     ██╗███╗   ██╗██╗   ██╗██╗  ██╗
██║     ██║████╗  ██║██║   ██║╚██╗██╔╝
██║     ██║██╔██╗ ██║██║   ██║ ╚███╔╝
██║     ██║██║╚██╗██║██║   ██║ ██╔██╗
███████╗██║██║ ╚████║╚██████╔╝██╔╝ ██╗
╚══════╝╚═╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝  ╚═╝

 ██████╗██╗     ██╗    ████████╗ ██████╗  ██████╗ ██╗     ███████╗
██╔════╝██║     ██║    ╚══██╔══╝██╔═══██╗██╔═══██╗██║     ██╔════╝
██║     ██║     ██║       ██║   ██║   ██║██║   ██║██║     ███████╗
██║     ██║     ██║       ██║   ██║   ██║██║   ██║██║     ╚════██║
╚██████╗███████╗██║       ██║   ╚██████╔╝╚██████╔╝███████╗███████║
 ╚═════╝╚══════╝╚═╝       ╚═╝    ╚═════╝  ╚═════╝ ╚══════╝╚══════╝
```

---

# "modern" is relative...

**Douglas Adams**

I've come up with a set of rules that describe our reactions to technologies:

> 1. Anything that is in the world **when you're born** is normal and ordinary and is just a natural part of the way the world works.
>
> 2. Anything that's invented **between when you're fifteen and thirty-five** is new and exciting and revolutionary and you can probably get a career in it.
>
> 3. Anything invented **after you're thirty-five** is against the natural order of things.

---

# Target audience

- linux desktop CLI users
- linux admins

```text
  __________________________________________
 / This is the year of linux on the desktop \
|                                            |
|          ...Windows10 has WSL ;-)          |
 \                                          /
  ------------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

---

# Linux tooling philosophy

- **do one thing (and only one thing!) well**

- **chaining**

- _sound familiar? (hint: functional programming...)_

---

# Why? Improvements to...

- **productivity**

- **optics**
    - "unix porn" (`PS1`, `ls`, ...)

---

# Learn the basics

- have knowledge of the **editor war** 
    - https://en.wikipedia.org/wiki/Editor_war
    - (`spacemacs` http://spacemacs.org/)

- `emacs` and `vim` keybindings
    - learn navigation, copy & paste, (and how to exit :thumbsup:)
    - pick one and become fluent

- `cat`, `less`, `find`, `grep`, `sed`, `tail`, `awk`, `dd`, `rsync`, ...

---

# shells

**...there is no "best shell"...**

- `bash`

- `zsh`

- `fish`

---

# What is the difference between **terminal** and **shell**?

## terminal
  
- **colors** (16 or more)
- **fonts** (utf8, ligatures, ...)
- **interactions**
    - keyboard shortcuts
    - mouse interaction (copy & paste, scrolling, selection, ...)
    - image support

## shell

- **everything else** (f.ex. **`PS1`**, scripting language)

---

# What is the best terminal?

- use your default

## Unicode, Emojis, Fonts

- but think about enriching your output!

- Emojis: :thumbsup: :ballot_box_with_check: :collision: :v: :poop: :speech_balloon: :zap: €

(...this presentation is running in a terminal (`kitty`), not a browser...)

---

# **fish**: The new kid on the block

- https://fishshell.com

- package manager
    - fisher (4k stars) https://github.com/jorgebucaran/fisher
    - oh-my-fish (5.5k stars) https://github.com/oh-my-fish/oh-my-fish

- category: shell

---

# **zsh**

- https://www.zsh.org/

- package manager
    - oh-my-zsh (99k stars) https://ohmyz.sh

- category: shell

---

# **bash**

- https://www.gnu.org/software/bash/

- package manager

    - bash-it (10k stars) https://github.com/Bash-it/bash-it
    - oh-my-bash (0.5k stars) https://ohmybash.github.io

- category: shell

---

# PS1: **liquidprompt**

- available for `zsh`, `bash`, etc

- https://github.com/nojhan/liquidprompt

- category: unix-porn

---

# PS1: **Powerline**

- started as fancy statusline for `vim`...

- available for `zsh`, `bash`, etc

- https://github.com/powerline/powerline

- category: unix-porn

---

# **byobu**

- http://byobu.co/

- `tmux`-wrapper for non-vim users

    - `tmux` https://github.com/tmux/tmux/wiki

- Keybindings `F1` - `F12`

- Sensible defaults (layout, info line)

- category: productivity

---

# **Ranger**

- https://ranger.github.io

- file explorer

- 2 layout options
    - miller columns
    - multipane (similar to Midnight commander)

- key bindings: see `~/.config/ranger/rc.conf` starting at line 300...

- with image support for certain terminals
    - `iterms2`
    - `urxvt`
    - `kitty`
    - not `gnome-terminal` (!)

- category: navigation, file system

<!--
    Demo

- navigation
- rename
- copy & paste
- sorting
- open shell
- image preview (only in `kitty` or `urxvt` terminal)
-->

---

# **bat**

- https://github.com/sharkdp/bat

- `cat` & `less` with syntax highlighting

- From the docs:

    _bat looks good on a dark background by default. However, if your terminal uses a light background, some themes like GitHub or OneHalfLight will work better for you._

- category: read / file display

---

# **fzf**

- https://github.com/junegunn/fzf

- fuzzy search
- `find * -type f | fzf`
- see `locate` for a static indexer
- category: search

<!--

    DEMO

    - TODO

-->

---

# **fd**

- https://github.com/sharkdp/fd

- simpler alternative to `find`
    - The command name is 50% shorter* than find :-).
    - Convenient syntax: fd PATTERN instead of `find -iname '*PATTERN*'`.
    - Colorized terminal output (similar to `ls`)
    - Smart case: the search is case-insensitive by default. It switches to case-sensitive if the pattern contains an uppercase character*.
    - Ignores hidden directories and files, by default.
    - Ignores patterns from your `.gitignore`, by default.
    - Regular expressions.
    - Unicode-awareness.

- category: search

<!--
## Demo

- TODO
-->

---

# **progress**

- https://github.com/Xfennec/progress

- attach to any kind of copy
- category: monitoring

---

# **Ultimate Plumber (up)**

- https://github.com/akavel/up

- interactive piping
- instant live preview

- category: search, file manipulation, interactive

---

# **lolcat**

- https://github.com/busyloop/lolcat

- Rainbows and unicorns

- category: fun, unix porn

---

# **ttyd**

- https://tsl0922.github.io/ttyd/

- share your terminal over the web

- category: network, dangerous

---

# **no-more-secrets**

- https://github.com/bartobri/no-more-secrets

- when the tv team comes in your office

- category: fun, unix porn

---

# **thefuck**

- https://github.com/nvbn/thefuck

- fix common typos / mistakes

- category: productivity

---

# **patat**

- https://github.com/jaspervdj/patat

- nerdy slides in your shell
- runs in a terminal (similar to `revealJs` for the browser)
- Pandoc syntax (f. ex. markdown)
- syntax highlighting

```javascript
let foo = "bar";
```

- emojis: :thumbsup:, :white_check_mark:, :ballot_box_with_check:, :collision:

- next slide: experimental image support in some terminals (same as for `ranger`)
    - `iterm2`, `urxvt`, `kitty`

- category: presentation, slides, unix porn

---

![softwerkskammer-logo](images/Softwerkskammer.png)

---

# **colorls**

- https://github.com/athityakumar/colorls

- pimp the `ls` command
- NerdFonts: https://github.com/ryanoasis/nerd-fonts
- icons

- category: unix porn

---

# END

- did I miss your favorite tool?
