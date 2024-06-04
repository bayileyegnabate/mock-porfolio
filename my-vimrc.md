"don't try to be vi compatible
set nocompatible
"encoding
set encoding=utf-8
"force plugins to load correctly when it is turned back on below
filetype off
"load plugins here (pathogen or vundle)

"turn on syntax highlighting
syntax on
"for plugins to load correctly
filetype plugin indent on

"pick a leader key

"let mapleader = ","
" Security
set modelines=0
"show line numbers
set number relativenumber
"show file stats
set ruler
"blink cursor on error instead of beeping
set visualbell
"whitespace
set wrap
set textwidth=79
set formatoptions=tcqrn1
set tabstop=2
set shiftwidth=2
set softtabstop=2
set expandtab
set noshiftround
" Cursor motion
set scrolloff=3
set backspace=indent,eol,start
set matchpairs+=<:> " use % to jump between pairs
runtime! macros/matchit.vim
"move up/down editor lines
nnoremap j gj
nnoremap k gk
"allow hidden buffers
set hidden
"rendering
set ttyfast
" Status bar
set laststatus=2
"last line
set showmode
set showcmd
"searching
nnoremap / /\v
vnoremap / /\v
set hlsearch
set incsearch
set ignorecase
set smartcase
set showmatch
"clear search
map <leader><space> :let @/=''<cr>
" Remap help key.
inoremap <F1> <ESC>:set invfullscreen<CR>a
nnoremap <F1> :set invfullscreen<CR>
vnoremap <F1> :set invfullscreen<CR>

" Textmate holdouts

" Formatting
map <leader>q gqip

" Visualize tabs and newlines
set listchars=tab:▸\ ,eol:¬
" Uncomment this to enable by default:
" set list " To enable by default
" Or use your leader key + l to toggle on/off
map <leader>l :set list!<CR> " Toggle tabs and EOL

" Color scheme (terminal)
"set t_Co=256
"set background=dark
"let g:solarized_termcolors=256
"let g:solarized_termtrans=1
" put https://raw.github.com/altercation/vim-colors-solarized/master/colors/solarized.vim
" in ~/.vim/colors/ and uncomment:
" colorscheme solarized
