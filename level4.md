# Выберем один коммит

  ```
  $ git checkout master
  $ git cherry-pick C4
  ```

# Жонглируем коммитами

  - [x] Переставить коммит так, чтобы нужный находился наверху при помощи git rebase -i
  - [x] Внести изменения при помощи commit --amend
  - [x] Переставить всё обратно при помощи git rebase -i
  - [x] Переместить master на изменённую часть дерева, чтобы закончить уровень.

Решение:

  ```
  $ git rebase -i HEAD~2
  $ git commit --amend
  $ git rebase -i HEAD~2
  $ git checkout master
  $ git merge caption
  ```

# Жонглируем коммитами №2

  ```
  $ git checkout master
  $ git cherry-pick C2
  $ git checkout -f master HEAD^
  $ git cherry-pick C2
  $ git cherry-pick C3
  ```

# git tag

git предоставляет нам теги, чья основная задача – ссылаться постоянно на конкретный коммит.

Важно, что после создания они никогда не сменят своего положения, так что можно с лёгкостью сделать checkout конкретного момента в истории изменений.

  ```
  $ git tag v0 C1
  $ git tag v1 C2
  $ git checkout v1
  ```

# Git describe

  ```
  $ git describe master
  $ git describe side
  $ git describe bugFix
  $ git commit
  ```

