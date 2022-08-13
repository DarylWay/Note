# vim基本操作

## 1. 前置准备

首先用vim编辑vim的配置文件: $HOME/.vimrc

在最后一行添加

```
set number
set relativenumber
```

从而在vim编辑器中可以显示行号以及相对行号

## 2. 基本操作

#### 正常模式

- h, j, k, l: 左, 下, 上, 右
- G - 光标移动到最后
- gg - 光标移动到最顶部
- [num]j - 定位到下方num行
- [num]k - 定位到上方num行
- yy - 复制当前行, yank 
- p - 粘贴复制行
- [num]p - 粘贴复制行num次
- dd - 删除当前行
- . - 重复前次操作
- u - 撤回前次操作, undo
- ctrl+r - 恢复前次操作
- dw - 删除当前单词
- cw - 删改当前单词
- yw - 复制当前单词
- w - 光标移动到下个单词首部
- e - 光标移动到下个单词尾部
- b - 光标移动到上个单词首部
- : - 进入命令行模式
- i - 进入编辑模式, insert光标左侧
- a - 进入编辑模式, append光标右侧
- o - 进入编辑模式. open a new line
- O - 进入编辑模式, open a new line above
- ci - 删除括号里面内容并进入编辑模式, 包括小, 中, 大三种括号, change in
- ctrl+v - 进入视觉模式, 可通过hjkl移动光标以字符为单位选中块, 按d删除
- shift+v - 进入视觉模式, 可通过hjkl移动光标以行为单位选中块, 按d删除

#### 编辑模式

- esc - 返回正常模式 

#### 命令行模式

- 双击esc - 返回正常模式
- :q - 未修改仅退出
- :q! - 已修改不保存强制退出
- :wq - 保存退出
- :/word+回车 - 在文档中搜索word
- :%s/old word/new word/g - 将old word全部替换为new word, g表示global全局替换