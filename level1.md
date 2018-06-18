# Intro

    ```
    $ git commit
    $ git commit
    ```

# Branches

    ```
    $ git branch bugFix
    $ git checkout bugFix
    ```

# Merging

Первый способ объединения изменений, который мы рассмотрим - это git merge - слияние или просто мердж. Слияния в Git создают особый вид коммита, который имеет сразу двух родителей. Коммит с двумя родителями обычно означает, что мы хотим объединить изменения из одного коммита с другим коммитом и всеми их родительскими коммитами.

Чтобы пройти этот уровень, сделай следующее:

  [x] Создай новую ветку под названием bugFix
  [x] Переключись на новую ветку bugFix командой git checkout bugFix
  [x] Сделай один коммит
  [x] Вернись на ветку master при помощи git checkout
  [x] Сделай ещё один коммит
  [x] Слей ветку bugFix с веткой master при помощи git merge

    ```
    $ git checkout -b bugFix
    $ git commit
    $ git checkout master
    $ git commit
    $ git merge bugFix
    ```

# Rebasing

При ребейзе Git по сути копирует набор коммитов и переносит их в другое место.

Несмотря на то, что это звучит достаточно непонятно, преимущество rebase в том, что c его помощью можно делать чистые и красивые линейные последовательности коммитов. История коммитов будет чище, если вы применяете rebase.

    [x] Переключись на ветку bugFix
    [x] Сделай коммит
    [x] Вернись на master и сделай коммит ещё раз
    [x] Переключись на bugFix и сделай rebase на master

    ```
    $ git checkout -b bugFix
    $ git commit
    $ git checkout master
    $ git commit
    $ git checkout bugFix
    $ git rebase master
    ```
