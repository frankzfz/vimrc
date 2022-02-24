# vimrc
vim configure file 
FAQ:
1. 编译安装vim8.2版本，
   1.1  wget https://ftp.nluug.nl/pub/vim/unix/vim-8.2.tar.bz2 --no-check-certificate
   1.2  ./configure --with-features=huge --enable-multibyte --enable-rubyinterp --enable-python3interp --enable-luainterp --enable-cscope --enable-gui=gtk3  --with-python3-config-dir=/usr/lib/python3.6/config-3.6m-x86_64-linux-gnu/   为了后续python的支撑，配置python3的使能，并安装python的包。 yum install python3 python-devel
   1.3  make && make install 
2. 验证是否安装python
   后续使用Leaderf需要用到python，否则提示：LeaderF requires Vim compiled with python and/or a compatible python version.  错误信息
   使用下面的命令，检查是否安装python支持。 vim --version | grep python
   +cmdline_info      +libcall           -python            +visual
   +comments          +linebreak         +python3           +visualextra
   前面的“-” 表示没有安装，“+”  表示已经安装完成。
3. 配置vimrc文件，
   参考 https://github.com/amix/vimrc.git的配置文件， 在/root/.vim_runtime目录下配置自己的个性化配置。 插件的目录位置：/root/.vim_runtime/sources_non_forked/ack.vim/plugged

4. 插件管理
  参考：https://github.com/junegunn/vim-plug  
5. Leaderf 搜索插件
    yum-config-manager --add-repo=https://copr.fedorainfracloud.org/coprs/carlwgeorge/ripgrep/repo/epel-7/carlwgeorge-ripgrep-epel-7.repo
    yum install ripgrep
 
    
