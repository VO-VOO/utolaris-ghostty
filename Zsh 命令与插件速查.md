---
title: Zsh 命令与插件速查
created: 2026-03-25
tags:
  - zsh
  - terminal
  - obsidian
---

# Zsh 命令与插件速查

这份笔记记录的是我目前这套 Zsh 环境里，常见命令实际变成了什么，以及每个工具负责什么。

## 一、命令映射

| 你输入的命令 | 实际执行的工具                                     | 功能                |
| ------ | ------------------------------------------- | ----------------- |
| `ls`   | `eza --icons --group-directories-first`     | 更好看的目录列表，带图标，目录优先 |
| `ll`   | `eza -la --icons --group-directories-first` | 详细列表，显示隐藏文件       |
| `lt`   | `eza --tree --icons --level=2`              | 树状显示目录结构          |
| `cat`  | `bat`                                       | 带语法高亮和行号的文件查看     |
| `find` | `fd`                                        | 更简单、更快的文件查找       |
| `grep` | `rg`                                        | 更快的全文搜索           |
| `top`  | `btop`                                      | 更直观的系统监控          |
| `lg`   | `lazygit`                                   | 终端里的 Git 图形界面     |

## 二、目录跳转

### `zoxide`

`zoxide` 是增强版 `cd`。它会记住你常去的目录，然后让你用关键词快速跳转。

常用方式：

```zsh
z mimo
z model
z obsidian
```

它的作用：

- 记录历史目录
- 优先匹配你最常访问的路径
- 让目录切换比完整输入路径更快

### `cd`

`cd` 还是标准命令，仍然可用：

```zsh
cd /Users/utolaris/Documents/obsidian
```

## 三、提示符和交互

### `starship`

`starship` 只负责提示符外观，不改变命令语法。

它会显示：

- 用户名
- 当前目录
- Git 分支和状态
- 语言版本
- 时间
- 命令耗时

### `zsh-autosuggestions`

根据历史命令给出灰色建议。

效果：

- 输入一半命令时，会看到补全建议
- 可以减少重复输入

### `zsh-syntax-highlighting`

实时给命令上色，帮助你看出：

- 命令是否存在
- 参数是否写对
- 是否有明显拼写错误

### `zsh-completions`

增强 `Tab` 补全，让更多命令有额外补全规则。

## 四、模糊搜索

### `fzf`

`fzf` 是模糊搜索工具，配合 shell 集成后常见用法是：

- `Ctrl-R`：搜索历史命令
- `Ctrl-T`：搜索并插入文件路径
- `Alt-C`：搜索并切换目录

它的作用：

- 减少你手输路径和历史命令的次数
- 在大量文件和命令里快速筛选

## 五、Node 版本管理

### `fnm`

`fnm` 是 Node 版本管理器，作用类似 `nvm`，但更快。

常用命令：

```zsh
fnm install --lts
fnm use lts-latest
fnm default lts-latest
fnm list
```

它的作用：

- 安装 Node 版本
- 切换当前使用的 Node
- 按项目目录自动切换版本

## 六、历史和补全体验

当前这套 Zsh 还做了这些事：

- 保存更长的命令历史
- 多个终端共享历史
- 命令执行后立即追加到历史
- 让补全和建议更像 fish

## 七、当前这套最常用命令

```zsh
z project
ls
ll
lt
cat README.md
grep "pattern" .
find . -name "*.md"
top
lg
fnm list
Ctrl-R
Ctrl-T
Alt-C
```

