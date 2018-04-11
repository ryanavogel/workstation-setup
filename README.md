# workstation-setup

## Git

```
git config --global merge.tool=diffmerge
git config --global mergetool.diffmerge.cmd=diffmerge --merge --result="$MERGED" "$LOCAL" "$(if test -f "$BASE"; then echo "$BASE"; else echo "$LOCAL"; fi)" "$REMOTE"
git config --global mergetool.diffmerge.trustexitcode=true
git config --global mergetool.keepbackup=false

git config --global diff.tool=diffmerge
git config --global difftool.diffmerge.cmd=diffmerge "$LOCAL" "$REMOTE"
```
