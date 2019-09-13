# my_vim_environment
Every time it takes me long to build a new vim environment on a new machine. Decided to put my .vimrc and corresponding operations here to save my time in the future.

-----

1. First of all, copy the whole files in .vimrc and .vim to the home direcotory of your new machine.

2. ** Ensure that your version of Vim is at least 7.4.1578 and that it has support for Python 2 or Python 3 scripting **.

3. **Install YCM** with Vundle. Basically, just launch vim and run :PluginInstall

4. **Install libclang** by conda install -c rapidsai libclang

5. **Compile the `ycm_core` library** that YCM needs. This library
    is the C++ engine that YCM uses to get fast completions.

    We'll create a new folder where build files will be placed. Run the
    following:

        cd ~
        mkdir ycm_build
        cd ycm_build
        cmake -G "Unix Makefiles" . ~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp
        cmake --build . --target ycm_core

