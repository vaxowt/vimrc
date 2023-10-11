# Vim 配置

## 使用方法

将 `vim` 复制到 `$XDG_CONFIG_HOME`

为了让 Vim 遵守 XDG 规范，设置环境变量：

```bash
export GVIMINIT='let $MYGVIMRC = !has("nvim") ? "$XDG_CONFIG_HOME/vim/gvimrc" : "$XDG_CONFIG_HOME/nvim/init.lua" | so $MYGVIMRC'
export VIMINIT='let $MYVIMRC = !has("nvim") ? "$XDG_CONFIG_HOME/vim/vimrc" : "$XDG_CONFIG_HOME/nvim/init.lua" | so $MYVIMRC'
```

安装插件管理器 `vim-plug`：

```bash
curl -fLo "${XDG_CONFIG_HOME}/vim/autoload/plug.vim" --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

打开 `vim`，安装插件：

```vim
:PlugInstall
```
