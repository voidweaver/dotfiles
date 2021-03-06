# ~/.dotfiles

My personal dotfiles repository, managed by [chezmoi](https://github.com/twpayne/chezmoi).

### Installation
1. Make sure you have [chezmoi](https://github.com/twpayne/chezmoi) installed
    ```shell
    $ which chezmoi
    /usr/bin/chezmoi
    ```

2. Initialize chezmoi using this repository
    ```shell
    $ chezmoi init https://github.com/voidweaver/dotfiles.git
    ```

3. Preview changes that chezmoi would make to your `$HOME`
    ```shell
    $ chezmoi diff
    ```

4. Apply the changes
    ```shell
    $ chezmoi apply
    ```
5. Install [antigen](https://github.com/zsh-users/antigen) and [vim-plug](https://github.com/junegunn/vim-plug) plugin managers
    ```shell
    $ curl -fLo ~/.antigen.zsh git.io/antigen
    $ curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
        https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
    ```
    **Note**: If you have installed antigen using the official command, you might need to symlink, copy, or move your `antigen.zsh` to `~/.antigen.zsh`. Skip this step if you installed antigen using the command above.
    ```shell
    $ ln -s /path/to/antigen.zsh ~/.antigen.zsh
    ```

6. Install vim plugins
    ```shell
    $ vim +PlugInstall +qall
    ```

7. Start a new zsh shell (plugins will be installed automatically by antigen)
    ```shell
    $ zsh
    ```
