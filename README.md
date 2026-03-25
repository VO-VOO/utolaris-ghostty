# utolaris-ghostty

这个仓库包含两份配置快照：

- `.zshrc`：Zsh 的 shell 配置，包含 prompt、插件、别名和常用工具默认设置。原始文件中的敏感 `env` 段已刻意排除。
- `.zshrc` 中声明的 Zsh 相关插件和集成包括：
  - Starship prompt
  - zsh-syntax-highlighting
  - zsh-autosuggestions
  - 通过 `fpath` 和 `compinit` 加载的 zsh-completions
  - `fzf` shell 集成
  - `zoxide`
  - `fnm`
- `ghostty/config`：Ghostty 终端配置，主要包括外观、字体、输入行为和默认终端设置。

这个快照不包含密钥或私钥。
