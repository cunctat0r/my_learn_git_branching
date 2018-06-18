# Rebase over 9000 раз

  ```
  $ git rebase master bugFix
  $ git rebase bugFix C4
  $ git rebase HEAD side
  $ git rebase side another
  $ git branch -f master another
  ```

# Здоровая семья, или несколько родителей

  ```
  $ git checkout master~^2~
  $ git branch bugWork
  $ git checkout master
  ```

# Спутанные ветки

  ```
  $ git checkout one
  $ git cherry-pick C4 C3 C2
  $ git checkout two
  $ git cherry-pick C5 C4 C3 C2
  $ git checkout three
  $ git rebase C2
  ```

