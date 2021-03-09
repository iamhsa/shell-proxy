# Shell Proxy oh-my-zsh plugin
Forked from : https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/shell-proxy
Removing SSH auto config and aliases

This a pure user-space program, shell-proxy setter, written Python3 and Bash.

100% only no side-effects, only effect **environment variables**

## Key feature

- Support Ubuntu, Archlinux, etc (Linux)
- Support macOS
- Built-in Auto-complete

## Usage

Method 1:

`$DEFAULT_PROXY` is the proxy URL you will set

Method 2:

Write a program to `$HOME/.config/proxy` in the file.

Example program:

```bash
#!/bin/bash
# The file path: $HOME/.config/proxy
if [[ "$OSTYPE" == "darwin"* ]]; then
  echo "http://127.0.0.1:6152" # Surge Mac
else
  echo "http://127.0.0.1:8123" # polipo
fi
```

Method 3:

The working path of **Method 2** can be changed via `$CONFIG_PROXY`

## The oh-my-zsh plugin (shell-proxy)

Public Domain
