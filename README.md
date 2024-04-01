# Config Types

- **Local** - Current project
- **Global** - All projects on my user system
- **System** - All projects for all users

## How to open?

```shell
  git config --global # | --local | --system / choose the correct config
  git config --global --edit # opens with vim
  git config --global core.editor code # sets vs code as default editor
  git config --global --edit # now opens with vs code
```

## What should I change?

### Push - [push]

- Now in this [push] section you can add:

```shell
followTags = true # git doesnt push custom tags by default
```

- There are two types of tags on git, annotated and lightweight tags, you can create a tag by using git tag version:

  ```shell
  git tag "1.0" # lightweight tag
  git tag -a "1.0.1" -m "1.0.1" # annotated tag
  ```

- You should only push annotated tags as releases, now with the followTags on git config, you will also send your tags to git

### Alias - [alias]

- Now in this [alias] section you can add:

```shell
c = !git add --all && git commit -m # add all modified files and commit them
s = !git status -s # show git status
l = !git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr' # show logs in a prettier way
amend = !git add -all && git commit --amend --no-edit # amend commits
count = !git shortlog -s --grep # count commits by type (feat, refactor, chore)
```
