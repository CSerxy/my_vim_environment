# my_vim_environment
Every time it takes me long to build a new vim environment on a new machine. Decided to put my .vimrc and corresponding operations here to save my time in the future.

-----

1. First of all, copy the whole files in .vimrc and .vim to the home direcotory of your new machine.

2. ** Ensure that your version of Vim is at least 7.4.1578 and that it has support for Python 2 or Python 3 scripting **.

3.0 git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/plugin/Vundle.vim

3.1 **Install YCM** with Vundle. Basically, just launch vim and run :PluginInstall

4. **Install libclang** by conda install -c rapidsai libclang

5. **Compile the `ycm_core` library** that YCM needs. This library
    is the C++ engine that YCM uses to get fast completions.

    We'll create a new folder where build files will be placed. Run the
    following:
        
        cd ~/.vim/bundle/
        git clone https://github.com/ycm-core/YouCompleteMe.git
        brew install cmake python go nodejs
        cd YouCompleteMe
        python3 install.py
        cd ~
        mkdir ycm_build
        cd ycm_build
        cmake -G "Unix Makefiles" . ~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp
        cmake --build . --target ycm_core
----
Refer to: 

        https://github.com/ycm-core/YouCompleteMe/blob/master/README.md
        https://github.com/VundleVim/Vundle.vim#about
        https://www.jianshu.com/p/a0b452f8f720
    
to gain more detailed information.
