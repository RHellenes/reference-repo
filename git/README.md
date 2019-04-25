# Light weight version git guide

[_Based on Roger Dudler's version_](http://rogerdudler.github.io/git-guide/)

Ad hoc is added as I go

&nbsp;

## Contents:

- [Light weight version git guide](#light-weight-version-git-guide)
  - [Contents:](#contents)
  - [Create & Clone](#create--clone)
  - [Add & Remove](#add--remove)
  - [Commit & Synchronize](#commit--synchronize)
  - [Branches](#branches)
  - [Merge](#merge)
  - [Tagging](#tagging)
  - [Restore](#restore)
  - [Set Remote Upstream](#set-remote-upstream)
  - [Set alias/ shorthand](#set-alias-shorthand)

&nbsp;

## Create & Clone

- **create new** repository

  ```git
  git init
  ```

- **clone local** repository

  ```git
  git clone /path/to/repository
  ```

- **clone remote** repository

  ```git
  git clone username@host:path/to/repository
  ```

&nbsp;

## Add & Remove

- **Add** changes to INDEX

  ```git
  git add filename.filetype
  ```

  or add whole directory

  ```git
  git add <directory>
  ```

- **Add all** changes to INDEX

  ```git
  git add *
  ```

- **Remove/ delete**

  ```git
  git rm filename.filetype
  ```

  or remove whole directory

  ```git
  git rm <directory>
  ```

&nbsp;

## Commit & Synchronize

- **Commit** changes

  ```git
  git commit -m 'Commit message'
  ```

- **Push** changes to remote repository

  ```git
  git push origin <branch>
  ```

- **Connect** local repository to remote repository

  ```git
  git remote add origin <server>
  ```

- **Update** local repository with remote changes

  ```git
  git pull
  ```

&nbsp;

## Branches

- **Create** new branch

  ```git
  git checkout -b <branch>
  ```

- **Switch** branch

  ```git
  git checkout <branch>
  ```

- **Delete** branch

  ```git
  git branch -d <branch>
  ```

- **Delete** remote branch

  ```git
  git branch --delete <branch>
  ```

- **Push branch** to remote repository

  ```git
  git push <remote> <branch>
  ```

- **List local branches** 

  ```git
  git branch
  ```

- **List remote branches** 

  ```git
  git branch -r
  ```

  If `git branch -r` does not work then try:

  ```git
  git ls-remote --heads <remote-name>
  ```

  e.g.
  ```git
  git ls-remote --heads git@github.com:RHellenes/rhellenes.me.git
  ```



&nbsp;

## Merge

- **Merge changes** from another branch

  ```git
  git merge branchName
  ```

- **View changes** between two branches

  ```git
  git diff sourceBranch -- targetBranch
  ```

  press `return` to end. `Q` also works (?)

&nbsp;

## Tagging

- **Create tag**

  ```git
  git tag tagName commitID
  ```

- **Get commit IDs**

  ```git
  git log
  ```

To end git log press <kbd>Q</kbd> 


&nbsp;

## Restore

- **Replace** working copy with latest from HEAD

  ```git
  git checkout -- fileName
  ```
  
&nbsp;

## Set Remote Upstream

- **Choose default remote branch to push/pull**

  Do this to enable `git pull` instead of having to do `git pull origin dev` when you are on branch: `dev` locally.

  ```git
  git branch --set-upstream-to=<remote>/<branch>
  ```

  **e.g**
  ```git
  git branch --set-upstream-to=origin/dev
  ```

&nbsp;

## Set alias/ shorthand

- **Set alias**


  ```git
  git config --global alias.<shorthand> <gitCommand>
  ```
  
  This will create a git alias, and add an entry to your global `~/.gitconfig` file
  ```git
  [alias]
      <shorthand> = <gitCommand>
  ```

  **e.g**
  ```git
  git config --global alias.co checkout
  ```
  [_Will create this in the_ `~/.gitconfig` _file_]
  ```git
  [alias]
      co = checkout
  ```

  You can also manually update the `.gitconfig` file with a text editor following this syntax:

  ```git
  [alias]
      co = checkout
      brunch = branch
      dinner = push
      etc.
  ```

  **Pro tip:** Type `code ~/.gitconfig` in the terminal to open the file in VSCode from the terminal.