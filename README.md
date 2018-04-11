# workstation-setup

## Git

* [Git for Windows](https://git-scm.com/download/win)
* Merge and diff tool is [DiffMerge](https://sourcegear.com/diffmerge/). You also need to add Diffmerge to the environment variables "Path".

```
git config --global user.name Ryan Vogel
git config --global user.username ryanavogel
git config --global user.email {email}

git config --global merge.tool diffmerge
git config --global mergetool.diffmerge.cmd 'sgdm --merge --result=\"$MERGED\" \"$LOCAL\" \"$(if test -f \"$BASE\"; then echo \"$BASE\"; else echo \"$LOCAL\"; fi)\" \"$REMOTE\"'
git config --global mergetool.diffmerge.trustexitcode true
git config --global mergetool.keepbackup false

git config --global diff.tool diffmerge
git config --global difftool.diffmerge.cmd 'sgdm \"$LOCAL\" \"$REMOTE\"'
```
