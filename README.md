# myvim
---

## 安装

	git clone https://github.com/AlexWoo/vim.git
	cd vim
	./install

## 插件管理

### 按键说明

- <SP\> 空格
- <CR\> 回车
- <Ctl\> Ctrl 键
- <Alt\> Alt 键
- <Lead\> , 键

### Vundle 插件操作命令

	:BundleInstall     安装配置的插件
	:BundleUpdate      更新配置的插件
	:BundleClean       删除本地无用插件

### 窗口管理

#### 总体

打开 nerdtree

	<Ctl> + n
	:NERDTreeToggle

打开 tagbar

	<Ctl> + t
	:TagbarToggle

光标 focus 左侧树形目录

	<Ctl> + w + h

光标 focus 右侧文件显示窗口

	<Ctl> + w + l

光标自动在左右侧窗口切换

	<Ctl> + w + w

增加窗口高度

	w=

降低窗口高度

	w-

增加窗口宽度

	w]

减少串口宽度

	w[

#### 已打开的文件

**常用操作**

打开文件 (**在 minibufexpl 中操作**)

	<CR>
	o

关闭文件 (**在 minibufexpl 中操作**)

	d

上下分屏

	s

左右分屏

	v

#### 导航栏

**自动打开配置**

Skeleton 已配置自动打开

	autocmd StdinReadPre * let s:std_in=1
	autocmd VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif

**常用操作**

查看帮助 (**在 nerdtree 中操作**)

	?

关闭 nerdtree (**在 nerdtree 中操作**)

	q

最大化 nerdtree (**在 nerdtree 中操作**)

	A

**文件操作**

打开文件，游标跳到打开的文件 (**在 nerdtree 中操作，二选一**)

	o
	<CR>

打开文件，游标留在 needtree (**在 nerdtree 中操作**)

	go

打开文件，在主窗口中水平分割，游标跳到打开的文件 (**在 nerdtree 中操作**)

	i

打开文件，在主窗口中水平分割，游标留在 needtree (**在 nerdtree 中操作**)

	gi

打开文件，在主窗口中水平分割，游标跳到打开的文件 (**在 nerdtree 中操作**)

	s

打开文件，在主窗口中水平分割，游标留在 needtree (**在 nerdtree 中操作**)

	gs

**目录操作**

目录操作有 x 和 X，用得不多

展开或折叠当前目录 (**在 nerdtree 中操作，二选一**)

	o
	<CR>

展开当前目录及其子目录 (**在 nerdtree 中操作**)

	O

在新窗口查看当前目录下的内容 (**在 nerdtree 中操作**)

	e

**游标跳转**

跳到根目录

	P

跳到上层目录

	p

跳到第一个兄弟

	K

跳到最后一个兄弟

	J

跳到下一个兄弟

	<Ctl> + k

跳到上一个兄弟

	<Ctl> + j

#### 标签栏

**自动打开配置**

Skeleton 未配置自动打开

vim 打开时自动打开 tagbar，tagbar 需要文件类型支持，不建议使用这种方式

	autocmd VimEnter * nested :TagbarOpen

打开支持 tagbar 的文件时才自动打开 tagbar

	autocmd VimEnter * nested :call tagbar#autoopen(1)

按照文件类型打开 tagbar

	autocmd FileType c,cpp nested :TagbarOpen

**常用操作**

查看帮助 (**在 tagbar 中操作**)

	?

跳到选中 tag 定义的位置 (**在 tagbar 中操作**)

	<CR>

查看选中 tag 原型 (**在 tagbar 中操作**)

	<SP>

跳到下一个 tag-fold (**在 tagbar 中操作**)

	<Ctl> + n

跳到上一个 tag-fold (**在 tagbar 中操作**)

	<Ctl> + p

展开选中 tag-fold (**在 tagbar 中操作**)

	+

折叠选中 tag-fold (**在 tagbar 中操作**)

	-


展开所有 tag-fold (**在 tagbar 中操作**)

	*

折叠所有 tag-fold (**在 tagbar 中操作**)

	=

### 其它

将 tab 替换为空格

	:tt

## 配置
