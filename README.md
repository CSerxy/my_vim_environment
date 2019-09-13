# my_vim_environment
Every time it takes me long to build a new vim environment on a new machine. Decided to put my .vimrc and corresponding operations here to save my time in the future.

-----

1. First of all, copy the whole files in .vimrc and .vim to the home direcotory of your new machine.

2. Ensure that your version of Vim is at least 7.4.1578 and that it has support for Python 2 or Python 3 scripting.

3. **Install YCM** with [Vundle][] (or [Pathogen][], but Vundle is a better
    idea). With Vundle, this would mean adding a `Plugin
    'Valloric/YouCompleteMe'` line to your [vimrc][].

    If you don't install YCM with Vundle, make sure you have run
    `git submodule update --init --recursive` after checking out the YCM
    repository (Vundle will do this for you) to fetch YCM's dependencies.

4. 
