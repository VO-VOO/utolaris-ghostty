# utolaris-ghostty

## 桌面效果

![桌面截图](./assets/desktop-screenshot.png)

## 配置内容

- `.zshrc`：Zsh 的 shell 配置，包含 prompt、插件、别名和常用工具默认设置。原始文件中的敏感 `env` 段已排除。
- `ghostty/config`：Ghostty 终端配置，主要包括字体、主题、透明度、窗口行为和输入体验。

## 使用教程

1. 前提条件：你的系统需要是 macOS，并且已经安装 Homebrew。
2. 从 Ghostty 官网下载安装包：<https://ghostty.org/download>
3. 将这个项目链接发给 Codex 或 Claude Code，让它帮你把配置落到本机环境里。
4. 按照仓库里的 `.zshrc` 和 `ghostty/config` 进行同步，必要时先备份你自己的原配置。

## 视觉效果

- 整体是偏克制的深色终端风格，背景半透明、边缘柔和，桌面感比较强。
- Starship prompt 会把路径、分支和状态信息压缩成更易扫读的提示行。
- 语法高亮和自动补全会让输入过程更清楚，终端看起来也更整洁。

## 加载的插件和集成

- Starship prompt
- zsh-syntax-highlighting
- zsh-autosuggestions
- 通过 `fpath` 和 `compinit` 加载的 zsh-completions
- `fzf` shell 集成
- `zoxide`
- `fnm`

## 优势

- 更快定位当前路径、Git 分支和命令状态。
- 更少的手动输入，常用路径和历史命令更容易复用。
- 终端显示更统一，适合长时间使用。
- 既保留效率，也保留一定的视觉层次感。

这个快照不包含密钥或私钥。
