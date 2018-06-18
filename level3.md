# Перемещаем труды туда-сюда

## Git Cherry-pick

Это очень простой и прямолинейный способ сказать, что ты хочешь копировать несколько коммитов на место, где сейчас находишься (`HEAD`)

Чтобы пройти этот уровень, просто скопируй изменения из этих трёх веток в мастер.

Решение

  ```
  $ git cherry-pick C3 C4 C7
  ```

## Введение в интерактивный Rebase

После открытия окна интерактивного rebase (с ключом `-i`) есть три варианта для каждого коммита:

  - Можно сменить положение коммита по порядку, переставив строчку с ним в редакторе (у нас в окошке строку с коммитом можно перенести просто мышкой).
  - Можно "выкинуть" коммит из ребейза. Для этого есть pick - переключение его означает, что нужно выкинуть коммит.
  - Наконец, можно соединить коммиты. При помощи этой функции можно объединять изменения двух коммитов.

Решение
  
  ```
  $ git rebase -i HEAD~4
  ```

