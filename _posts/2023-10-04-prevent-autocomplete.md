---
title: "prevent-autocomplete"
date: 2023-10-04
---
To prevent zsh from getting stuck in a loop while auto-completing `apt install`, you can disable the auto-completion feature for the `apt` command. Here's how you can do it:

1. Open your zsh configuration file in a text editor. The default configuration file is usually located at `~/.zshrc`.

2. Search for the line that starts with `autoload -Uz compinit`. This line initializes the zsh completion system.

3. Add the following line after the `autoload -Uz compinit` line to disable auto-completion for the `apt` command:

   ```shell
   zstyle ':completion:*:apt:*' ignored-patterns '*:install'
   ```

   This line tells zsh to ignore auto-completion for any command that ends with `:install` when using the `apt` command.

4. Save the changes and exit the text editor.

5. Restart your zsh shell or run the following command to apply the changes:

   ```shell
   source ~/.zshrc
   ```

Now, when you use the `apt install` command, zsh will not attempt to auto-complete the package names, preventing any potential bugs or loops.
