# Tmux: A Professional Guide

This guide will help you set up and use `tmux`, a powerful terminal multiplexer, to manage multiple terminal sessions efficiently.

## 1. Install tmux

Install `tmux` on your system if it's not already installed. For Linux, use the following command:

```bash
sudo apt-get update
sudo apt-get install tmux
```

## 2. Start a new tmux session

Create a new `tmux` session with a custom name:

```bash
tmux new-session -s my-session
```

## 3. Navigate between panes and windows

To navigate between panes and windows, use the following key bindings:

- Split the window horizontally: `Ctrl-b %`
- Split the window vertically: `Ctrl-b "`
- Switch to the next pane: `Ctrl-b o`
- Switch to the previous pane: `Ctrl-b ;`
- Close the current pane: `Ctrl-b x`

## 4. Customize tmux

You can customize `tmux` by creating a configuration file called `.tmux.conf` in your home directory. For example, you can change the default prefix key from `Ctrl-b` to `Ctrl-a` by adding the following line to your `.tmux.conf` file:

```
set-option -g prefix C-a
```

To apply your customizations, run `tmux source-file ~/.tmux.conf` from within `tmux`.

## 5. Enhance tmux with plugins

Use the `tmux` plugin manager (tpm) to install and manage plugins. To install tpm, run:

```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Add the following snippet to your `.tmux.conf` file to configure tpm:

```
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Add more plugins below this line

run '~/.tmux/plugins/tpm/tpm'
```

To install a new plugin, add the plugin name after the `# Add more plugins below this line` comment, and then press `Prefix + Shift + I` to install the plugin.

## 6. Share tmux sessions

To share a `tmux` session with others, they need to SSH into the same system and attach to the `tmux` session you created:

```bash
tmux attach-session -t my-session
```

If your SSH connection drops, the `tmux` session will continue running in the background, and you can reattach to it later.

For more information on using `tmux`, refer to the following resources:

- [A quick and easy guide to tmux](https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)
- [Jaime's Guide to Tmux](https://www.barbarianmeetscoding.com/blog/jaimes-guide-to-tmux-the-most-awesome-tool-you-didnt-know-you-needed/)
- [Tmux Beginner's Guide and Cheat Sheet](https://www.hostinger.com/tutorials/tmux-beginners-guide-and-cheat-sheet/)
- [Tmux Keybindings and Customization](https://www.ocf.berkeley.edu/~ckuehl/tmux/)