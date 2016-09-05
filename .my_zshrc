## ===== Options ===== ##

setopt autocd                # Allow omit cd while changing directory.

setopt HIST_REDUCE_BLANKS    # Remove extra blanks from each command line being added to history.
setopt HIST_IGNORE_ALL_DUPS  # Prevent history from recording duplicated entries.
setopt HIST_FIND_NO_DUPS     # Don't display duplicates when searching in history.


## ===== History ===== ##

HISTFILE=~/.histfile
HISTSIZE=1000
SAVEHIST=$HISTSIZE


## ===== Load theme ===== ##

source ~/.zsh/arrows.theme.zsh


## ===== Antigen ===== ##

source /usr/share/zsh/scripts/antigen/antigen.zsh

antigen bundle zsh-users/zsh-completions
antigen bundle zsh-users/zsh-autosuggestions
antigen bundle zsh-users/zsh-syntax-highlighting

antigen apply


## ===== Syntax Highlighting ===== ##

ZSH_HIGHLIGHT_STYLES[alias]=none
ZSH_HIGHLIGHT_STYLES[builtin]=none
ZSH_HIGHLIGHT_STYLES[command]=none
ZSH_HIGHLIGHT_STYLES[path]=none
ZSH_HIGHLIGHT_STYLES[path_prefix]=none
ZSH_HIGHLIGHT_STYLES[globbing]=none


## ===== Aliases ===== ##

alias ...='cd ../..'
alias ....='cd ../../..'
alias back='cd $OLDPWD'

alias gaa='git add .'
alias ga='git add'
alias gp='git push'
alias gl='git log'
alias gs='git status'
alias gd='git diff'
alias gcm='git commit -m'
alias gca='git commit --amend'
alias gc='git checkout'
alias gb='git branch'

alias ls='ls --color=auto'
alias la='ls -lhA --color=auto'     # List almost all elements
alias ll='ls -lh --color=auto'      # List all not hidden elements
alias ld='ls -lhd .* --color=auto'  # List only hidden elements

alias szsh='source ~/.zshrc'
alias zshrc='$EDITOR ~/.zshrc'
alias wtf='dmesg'


## ===== Completion ===== ##

autoload -Uz compinit
compinit

# Show completion menu when number of options is at least 2
zstyle ':completion:*' menu select

# Match case-insensitive, partial-word, and then substring completion
zstyle ':completion:*' matcher-list 'm:{a-zA-Z}={A-Za-z}' 'r:|[._-]=* r:|=*' 'l:|=* r:|=*'

# Don't complete unavailable commands.
zstyle ':completion:*:functions' ignored-patterns '(_*|pre(cmd|exec))'


## ===== Bind keyboard ===== ##

# History beginnig search (built-in zsh feature)
bindkey '^[[A' history-beginning-search-backward
bindkey '^[[B' history-beginning-search-forward


# zstyle ':completion:*:default' list-colors ${(s.:.)LS_COLORS}
