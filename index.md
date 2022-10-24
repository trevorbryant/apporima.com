#!/bin/bash

# To get the latest dotfiles, run the following in your shell:
# source <(curl -sLo- https://dotfiles.apporima.com)

function dotfile-update {
    pushd $HOME &>/dev/null
    if [ -d .rcfiles ]; then
      mv .rcfiles .rcfiles-old
    fi
    curl -sLo- https://git.jharmison.com/trevor/dotfiles/archive/master.tar.gz | \
      tar xvzf - \
        --xform=s/dotfiles/./ \
        --exclude=.gitignore \
        --exclude=README.md \
        --exclude=LICENSE \
        --exclude=dconf \
        && \
      rm -rf .rcfiles-old || \
      { mv .rcfiles-old .rcfiles ; return 1 ; }
      . .bashrc
      popd &>/dev/null
}

