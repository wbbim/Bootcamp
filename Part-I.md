环境的配置
==========

## vim

### 安装Pathogen.vim

使用它可以轻松地安装各种插件。 
使用 `sudo apt-get install vim` 安装vim.
在shell中拷贝粘贴以下内容:

	mkdir -p ~/.vim/autoload ~/.vim/bundle; \
	curl -Sso ~/.vim/autoload/pathogen.vim \
			https://raw.github.com/tpope/vim-pathogen/master/autoload/pathogen.vim

### 配置vimrc

打开vimrc，添加以下内容:

	execute pathogen#infect()

以后想安装的插件都可以解压到 `~/.vim/bundle` ,便可以使用

*zencoding*是一款快速写HTML的插件。只需执行以下代码:

	git clone http://github.com/mattn/zencoding-vim.git ~/.vim/bundle/zencoding

打开vim，输入 `html:5` , 再按`(Ctrl + y + ',')`，便自动生成html5框架代码。

此外，可以根据自己的需要添加一些配置到vimrc中，这个看个人需要。

## git&git-flow

在shell中输入 `sudo apt-get install git git-flow` 进行安装。

## rvm&ruby

具体内容和使用说明可以上RVM的官方网站[rvm.io](https://rvm.io)进行查阅

安装：

```shell
curl -L https://get.rvm.io | bash -s stable
```

安装完成之后选装安装自己使用的Ruby版本。我安装的是MRI 1.9.3。也就式Matz实现的版本。

```shell
rvm install 1.9.3
```

默认使用1.9.3版本:

```shell
rvm use 1.9.3
```

最后，为了使每次启动都可以使用rvm的命令，可以向 `~/.bashrc` 文件种添加以下代码:

```shell
source ~/.rvm/scripts/rvn
```

至此，环境的配置已经完成。
	
