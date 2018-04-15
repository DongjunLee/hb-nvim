
<p align="center">
  <img src="images/logo.png" width=250>
</p>

# hb-nvim: HumanBrain's Neovim Distribution

**hb-nvim** is a distribution of vim plugins and resources for Vim and `Neovim` with `Oh My ZSH`.

## Requirements

- Vim > 7.4, prefer 8.0

## Based on

- [spf13-vim](https://github.com/spf13/spf13-vim)
- [Neovim](https://github.com/neovim/neovim)
- [vim plug](https://github.com/junegunn/vim-plug)
- [Oh My ZSH!](http://ohmyz.sh/)

## Installation

1. Install spf13-vim
  
  ```bash
  curl https://j.mp/spf13-vim3 -L > spf13-vim.sh && sh spf13-vim.sh
  ```
  
  - move `.vimrc` and `.vimrc.bundles` to $HOME path.
  
  ```bash
  mv .vimrc ~/.
  mv .vimrc.bundles ~/.
  ```
  
2. Install or Update Plugins

	```bash
	vim -> :PluginInstall
	vim -> :PluginUpdate
	```

3. Install Neovim (Stable)
  
	```bash
	$ brew install neovim/neovim/neovim
	```

	- Transitioning from Vim

	```bash
	mkdir ~/.config
	ln -s ~/.vim ~/.config/nvim
	ln -s ~/.vimrc ~/.config/nvim/init.vim
	```

4. Install vim-plug (Neovim)

	```bash
	curl -fLo ~/.config/nvim/autoload/plug.vim --create-dirs \
	https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
	```
	
	- install [deoplete](https://github.com/Shougo/deoplete.nvim) requirements
	
	```bash
	pip3 install neovim
	```
	
	- Install or Update Plugs
	
	``` bash
	nvim -> :PlugInstall
	nvim -> :PlugUpgrade
	```
  
5. Install Oh My ZSH!

	```bash
	sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
	```
	
6. Install requirements.txt

	- for Python (autopep8, flake8)
	
	```bash
	pip install -r requirements.txt
	```
  
## Usages

1. **Cursor**

| key | descripton|
| --- | --------- |
| k | 	커서를 위로 움직임 |
| j | 	커서를 아래로 움직임 |
| h | 	커서를 왼쪽으로 움직임 |
| l | 	커서를 오른쪽으로 움직임 |
| - | 	커서를 줄의 처음으로 옮김 |
| e, E | 	다음단어의 끝으로, 문자단위 이동 |
| w, W | 	다음단어의 처음으로, 문자단위 이동 |
| $ | 	줄의 마지막으로 |
| 0 | 	줄의 처음으로 |
| ^ | 	줄의 처음으로(공백이 아닌 처음시작되는 문자) |
| Shift+g | 	문서의 마지막으로 이동한다. |
| gg, 1g | 	문서의 처음으로 이동한다. 1대신 다른 숫자를 입력하면 해당 숫자의 라인으로 이동한다. |
| ), ( | 	다음, 이전 문장의 처음으로 |
| }, { | 	다음, 이전문단의 처음으로 |
| ]], [[ | 	다음, 이전 구절의 처음으로 |

## Plugins

### [Undotree](https://github.com/mbbill/undotree)

### [NERDTree](https://github.com/scrooloose/nerdtree)

### [ctrlp](https://github.com/kien/ctrlp.vim)

### [Surround](https://github.com/tpope/vim-surround)

### [NERDCommenter](https://github.com/scrooloose/nerdcommenter)

### [deoplete](https://github.com/Shougo/deoplete.nvim)

### [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)

### [Syntastic](https://github.com/scrooloose/syntastic)

### [AutoClose](https://github.com/spf13/vim-autoclose)

### [Fugitive](https://github.com/tpope/vim-fugitive)

### [Ack.vim](https://github.com/mileszs/ack.vim)

### [Tabularize](https://github.com/godlygeek/tabular)

### [Tagbar](https://github.com/majutsushi/tagbar)

### [EasyMotion](https://github.com/Lokaltog/vim-easymotion)

### [Airline](https://github.com/bling/vim-airline)

### [Neoformat](https://github.com/sbdchd/neoformat)

```bash
" Use neoformat.
" option - replace : replace the file, instead of updating buffer (default: 0)
let g:neoformat_python_autopep8 = {
        \ 'exe': 'autopep8',
        \ 'args': ['--aggressive', '--max-line-length 120'],
        \ 'replace': 1,
        \ }
let g:neoformat_enabled_python = ['autopep8']
```

## Additional Syntaxes

## Colorscheme

## Git Hooks

- Python (flake8)

```bash
flake8 --install-hook git

" if want prevent commit
git config --bool flake8.strict true
```
