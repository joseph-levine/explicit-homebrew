# explicit-homebrew
[Homebrew](https://brew.sh) is the absolute best.

Except... if you install a package to try it, and remove it later, the dependencies of the now removed package are still installed.

So this utility is very simple.
Add a new file at `~/.config/homebrew/explicit`, and list the programs you actually want. One per line.

For example...

```text
fish
tmux
vim
```

This utility will try to uninstall everything not in the explicit list.
If it's a dependency for something you want, Homebrew won't let you (nor this utility) uninstall it accidentally.

Because of depdencies on dependencies, the program will loop until it doesn't uninstall anything.

Remember to add new packages!
