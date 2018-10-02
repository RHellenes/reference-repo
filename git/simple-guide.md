# Light weight version git guide

[_Based on Roger Dudler's version_](http://rogerdudler.github.io/git-guide/)

&nbsp;

## Contents:

+ [Light weight version git guide](#light-weight-version-git-guide)
  + [Contents:](#contents)
  + [Create & Clone](#create--clone)
  + [Add & Remove](#add--remove)
  + [Commit & Synchronize](#commit--synchronize)
  + [Branches](#branches)
  + [Merge](#merge)
  + [Tagging](#tagging)
  + [Restore](#restore)

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

- **add** changes to INDEX

  ```git
  git add filename.filetype
  ```

  or add whole directory

  ```git
  git add directoryName
  ```

- **add all** changes to INDEX

  ```git
  git add *
  ```

- **remove/ delete**

  ```git
  git rm filename.filetype
  ```

  or remove whole directory

  ```git
  git rm directoryName
  ```

&nbsp;

## Commit & Synchronize

- **commit** changes

  ```git
  git commit -m 'Commit message'
  ```

- **push** changes to remote repository

  ```git
  git push origin branchName
  ```

- **connect** local repository to remote repository

  ```git
  git remote add origin <server>
  ```

- **update** local repository with remote changes

  ```git
  git pull
  ```

&nbsp;

## Branches

- **create** new branch

  ```git
  git checkout -b branchName
  ```

- **switch** branch

  ```git
  git checkout branchName
  ```

- **delete** branch

  ```git
  git branch -d branchName
  ```

- **push branch** to remote repository

  ```git
  git push origin branchName
  ```

&nbsp;

## Merge

- **merge changes** from another branch

  ```git
  git merge branchName
  ```

- **view changes** between two branches

  ```git
  git diff sourceBranch -- targetBranch
  ```

  press `return` to end. `Q` also works (?)

&nbsp;

## Tagging

- **create tag**

  ```git
  git tag tagName commitID
  ```

- **Get commit IDs**

  ```git
  git log
  ```

&nbsp;

## Restore

- **Replace** working copy with latest from HEAD

  ```git
  git checkout -- fileName
  ```
