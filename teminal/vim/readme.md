Vim does not have a plugin manager built-in, it has a package system. Here's how it works.

# Basics
You (or your plugin manager) put your plugins here

´´´
$HOME/.vim/pack/{anyname}/start/{plugin_name}/{same stuff as in $HOME/.vim, "autoload", "after", "plugin", etc.}
´´´
same as above, but only loaded on demand with :packadd {plugin_name}.

´´´
$HOME/.vim/pack/{anyname}/opt/{plugin_name}
´´´

Using this you can have lazy loading. You can also put color schemes under "opt", they will be detected without :packadd

# Example

I have $HOME/.vim/pack/{integrated,local,minpac}

- "minpac" is for plugins installed via minpac plugin manager
- "local" has symlinks to plugins that I planned to publish but didn't come around to it yet
- "integrated" is plugins that I keep as part of the configuration. This directory is under git source control. This is for convenience only. Mostly because I wanted to utilize "autoload" functionality, but did wan't to pollute $HOME/.vim/autoload.

# Details

At the heart of it all is the 'runtimepath' setting. It was present before the new package system. The plugin managers like pathogen used to modify it directly. Now they don't have to, Vim does it automatically.

You can take a look at 'runtimepath' value with :set runtimepath?. It is a list of directories where Vim will source *.vim files from. Each directory has the same structure. It can contain "plugin", "color", "ftdetect", etc. The directories will be processed in the order they appear in 'runtimepath'.

# References

´:h packages´

´:h startup´

´:h runtimepath´



---

# Plugin list
Plugin 'scrooloose/nerdtree'
Plugin 'majutsushi/tagbar'
Plugin 'airblade/vim-gitgutter'
Plugin 'nathanaelkane/vim-indent-guides'
Plugin 'tpope/vim-fugitive'
Plugin 'austintaylor/vim-indentobject'
Plugin 'ctrlpvim/ctrlp.vim'
Plugin 'tpope/vim-rails'
Plugin 'vim-ruby/vim-ruby'


Plugin 'christoomey/vim-tmux-navigator'
Plugin 'juvenn/mustache.vim'
Plugin 'garbas/vim-snipmate'
Plugin 'MarcWeber/vim-addon-mw-utils'
Plugin 'tomtom/tlib_vim'
Plugin 'nono/vim-handlebars'
Plugin 'scrooloose/syntastic'
Plugin 'slim-template/vim-slim'
Plugin 'tpope/vim-bundler'
Plugin 'tpope/vim-commentary'
Plugin 'tpope/vim-cucumber'
Plugin 'tpope/vim-dispatch'
Plugin 'tpope/vim-endwise'
Plugin 'tpope/vim-pastie'
Plugin 'tpope/vim-ragtag'
Plugin 'tpope/vim-repeat'
Plugin 'tpope/vim-surround'
Plugin 'tpope/vim-unimpaired'
Plugin 'tpope/vim-vividchalk'
Plugin 'vim-scripts/Align'
Plugin 'vim-scripts/greplace.vim'
Plugin 'vim-scripts/matchit.zip'


---

https://opensource.com/article/20/2/how-install-vim-plugins

# plugins
https://vimawesome.com/

---
Nerd fonts install
> brew install fontconfig
> brew install --cask font-jetbrains-mono-nerd-font
> brew install --cask font-meslo-lg-nerd-font
> brew install --cask font-noto-nerd-font

colorthemes
https://github.com/NLKNguyen/papercolor-theme from https://vimcolorschemes.com/i/top
https://github.com/morhetz/gruvbox

Icons to plugins
https://github.com/ryanoasis/vim-devicons

Statusline
https://github.com/vim-airline/vim-airline
:helptags ~/.vim/pack/dist/start/vim-airline/doc

https://github.com/vim-airline/vim-airline-themes
https://github.com/vim-airline/vim-airline-themes#vim-airline-themes--
:helptags ~/.vim/pack/dist/start/vim-airline-themes/doc

Git integration
https://github.com/tpope/vim-fugitive
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-fugitive/doc" -c q

gitgutter
https://github.com/airblade/vim-gitgutter
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-gitgutter/doc" -c q

Identation guides
https://github.com/preservim/vim-indent-guides
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-indent-guides/doc" -c q

Full path fuzzy file, buffer, mru, tag, ... finder for Vim.
https://github.com/ctrlpvim/ctrlp.vim
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/ctrlp.vim/doc" -c q

Rails
https://github.com/tpope/vim-rails
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-rails/doc" -c q

Node
https://github.com/moll/vim-node
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-node/doc" -c q

Rake
https://github.com/tpope/vim-rake
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-rake/doc" -c q

Ruby
https://github.com/vim-ruby/vim-ruby
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/vim-ruby/doc" -c q

LSP
https://github.com/yegappan/lsp
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/lsp/doc" -c q
install typescript language server: npm install -g typescript typescript-language-server

Automamting bracketing creation
https://github.com/jiangmiao/auto-pairs
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/auto-pairs/doc" -c q
