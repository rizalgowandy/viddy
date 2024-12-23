# Viddy

<p align="center">
<img src="images/logo.png" width="200" alt="viddy" title="viddy" />
</p>

Modern `watch` command.

Viddy well, gopher. Viddy well.

## Demo

<p align="center">
<img src="images/demo.gif" width="100%" alt="viddy" title="viddy" />
</p>

## Features

* Basic features of original watch command.
    * Execute command periodically, and display the result.
    * color output.
    * diff highlight.
* Time machine mode. 😎
    * Rewind like video.
    * Go to the past, and back to the future.
* Look back history.
    * Save and load history.
* See output in pager.
* Vim like keymaps.
* Search text.
* Suspend and restart execution.
* Support shell alias
    * See detail https://github.com/sachaos/viddy/issues/2#issuecomment-904002053
* Customize keymappings.
* Customize color.

## Install

### Cargo

```shell
cargo install viddy
```

### [Homebrew](https://brew.sh)

```shell
brew install viddy
```

### Linux

```shell
wget -O viddy.tar.gz https://github.com/sachaos/viddy/releases/download/v1.3.0/viddy-v1.3.0-linux-x86_64.tar.gz && tar xvf viddy.tar.gz && mv viddy /usr/local/bin
```

### Other

Download from [release page](https://github.com/sachaos/viddy/releases).

## Install with Other Package Managers (Community-Maintained)

### [MacPorts](https://www.macports.org)

```shell
sudo port install viddy
```

### [Scoop](https://scoop.sh/)

To install Viddy on Windows, first install the Scoop package manager, and then run the commands below.

**NOTE**: The git package is required in order to add additional Scoop "buckets".

```
scoop install git
scoop bucket add extras
scoop install extras/viddy
```

### ArchLinux ( AUR )

```shell
yay -S viddy
```
Alternatively you can use the [AUR Git repo](https://aur.archlinux.org/packages/viddy/) directly

### Alpine Linux

After [enabling the community repository](https://wiki.alpinelinux.org/wiki/Enable_Community_Repository):

```shell
apk add viddy
```

### [asdf version manager](https://asdf-vm.com)

```shell
asdf plugin add viddy
asdf install viddy latest
asdf global viddy latest
```

## Keymaps

| key       |                                            |
|-----------|--------------------------------------------|
| SPACE     | Toggle time machine mode                   |
| s         | Toggle <ins>s</ins>uspend execution                   |
| b         | Toggle ring terminal <ins>b</ins>ell                  |
| d         | Toggle <ins>d</ins>iff                                |
| t         | Toggle header/<ins>t</ins>itle display                      |
| ?         | Toggle help view                           |
| /         | Search text                                |
| j         | Pager: next line                           |
| k         | Pager: previous line                       |
| h         | Pager: move left                           |
| l         | Pager: move right                          |
| Control-F | Pager: page down                           |
| Control-B | Pager: page up                             |
| g         | Pager: go to top of page                   |
| Shift-G   | Pager: go to bottom of page                |
| Shift-J   | (Time machine mode) Go to the past         |
| Shift-K   | (Time machine mode) Back to the future     |
| Shift-F   | (Time machine mode) Go to more past        |
| Shift-B   | (Time machine mode) Back to more future    |
| Shift-O   | (Time machine mode) Go to oldest position  |
| Shift-N   | (Time machine mode) Go to current position |

## Configuration

Viddy can be used without any configuration.
However, if you want to customize the keybindings or default behavior, you can do so.

Install your config file on `$XDG_CONFIG_HOME/viddy.toml`
On macOS, the path is `~/Library/Application\ Support/viddy.toml`.

```toml
[general]
no_shell = false
shell = "zsh"
shell_options = ""
skip_empty_diffs = false
disable_mouse = true

[keymap]
timemachine_go_to_past = "Down"
timemachine_go_to_more_past = "Shift-Down"
timemachine_go_to_future = "Up"
timemachine_go_to_more_future = "Shift-Up"
timemachine_go_to_now = "Ctrl-Shift-Up"
timemachine_go_to_oldest = "Ctrl-Shift-Down"
scroll_left = "h"
scroll_right = "l"
scroll_up = "k"
scroll_down = "j"
scroll_half_page_up = "Ctrl-u"
scroll_half_page_down = "Ctrl-d"
scroll_page_up = "Ctrl-b"
scroll_page_down = "Ctrl-f"
scroll_bottom_of_page = "Shift-g"
scroll_top_of_page = "g g"

[color]
background = "white" # Default value is inherit from terminal color.
```

## What is "viddy" ?

"viddy" is Nadsat word meaning to see.
Nadsat is fictional argot of gangs in the violent book and movie "A Clockwork Orange".

## Credits

The gopher's logo of viddy is licensed under the Creative Commons 3.0 Attributions license.

The original Go gopher was designed by [Renee French](https://reneefrench.blogspot.com/).
