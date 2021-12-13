# `NULL`

An empty repository to aid ZI atclone'' hook.

Use case example: 

```
# The invocation uses https://github.com/z-shell/null repo as a placeholder
# for the atclone'' and atpull'' hooks

zi ice as"program" pick"$ZPFX/sdkman/bin/sdk" id-as'sdkman' run-atpull \
  atclone"wget https://get.sdkman.io -O scr.sh; SDKMAN_DIR=$ZPFX/sdkman bash scr.sh" \
  atpull"SDKMAN_DIR=$ZPFX/sdkman sdk selfupdate" \
  atinit"export SDKMAN_DIR=$ZPFX/sdkman; source $ZPFX/sdkman/bin/sdkman-init.sh"
zi light z-shell/null
```
