# Vim 配置

## 使用方法

将 `vim` 复制到 `$XDG_CONFIG_HOME`

为了让 Vim 遵守 XDG 规范，设置环境变量：

```bash
export VIMINIT='if !has("nvim") | set rtp^=$XDG_CONFIG_HOME/vim | let $MYVIMRC="$XDG_CONFIG_HOME/vim/vimrc" | so $MYVIMRC | endif'
```
