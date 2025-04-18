- Git add . – добавление файлов в индекс.
- Git status – дает понимание какие файлы были изменены, добавлены или удалены, но они еще не закоммичены.
- git commit -m "Описание коммита" - фиксирует изменения в репозитории. Сохраняет их в историю, в которую можно обратиться.
- Git log – выводит всю историю коммитов, там информация изменений и действий.
- Git show – дает информацию о конкретном коммите. Дата, автор, что изменилось.
- Git diff – разница между текущими изменнениями и последним коммитом. Показывает, что именно изменилось в файлах.
- git restore – омтеняет все изменения в файлах, возвращает к состоянию последнего коммита. 
- git rm - удаление файлов из Git, а также из рабочей папки в случае необходимости.
- git reset - отменяет все коммиты не запушенные и возвращает в проект к более раннему этапу. (git reset --hard HEAD-1).
- git branch - показывает список веток.
    1. git branch "имя ветки" - создаем  новую ветку. 
    2. git branch -d "имя ветки" - удаляем ветку с названия. 
- git pull - переносит актуальные изменения с гита на наш репозиторий. Желательно находиться на главной ветке в момент выполнения.
- git push - отправляет изменения в удаленный репозиторий. Работает только после коммита.
- git help -a -  показывает все доступные команды в git.
- git clone url - скопироать/склонировать удаленный репозиторий.

Тема 1.
# Понятие репозитория и структура проекта.
Репозиторий - хранилище кода, включающее:
1. все файлы и папки проекта. 
2. историю изменений(коммиты).
3. информацию о ветках и настройках.   

Виды репозитория:
1. Локальный - хранится на компьютере разработчика(папка.git).
2. Удаленный (remote) он размещен на сервере (GitHub или GitLab).

# Структура проекта
project/         # Корневая папка
|
|--
|--- .git/       # Скрытая папка с данными Git (история, настройки)
|
|--- src/        # Исходный код (например, main.py, index.js)
|--- docs/       # Документация (README.md, API-описание)
|--- tests/      # Тесты (unit-тесты, интеграционные тесты)
|--- config/     # Файлы конфигурации (настройка сервера, БД)
|--- assets/     # Ресурсы (изображения, шрифты)
|
|___ .gitignore  # Файл, указывабщий, какие файлы Git должен игнорировать 

Основные элементы:
 - .git/ - служебная папка Git (нельзя удалять!).
 - README.md - описание проекта (облако в корне).
 - .gitignore - список файлов, которые Git не отслеживает

 # Жизненый цикл файлов в Git
 1. Неотслеживаемые (Untracked) -- Git о них не знает.
 2. Измененные (Modified) -- файлы, которые уже в репозитории, но были изменены.
 3. Индексированные (Staged) --  файлы, подготовленные к коммиту (git add).
 4. Зафиксированные (Committed) -- изменения сохранены в репозитории (git commit).

 # Важные правила 
 Коммиты должны быть атомарными - каждое изменение логически завершенное.
 - .gitignore обязателен - чтобы не засорять репозиторий ненужными файлами.
 - README.md - лицо проекта - должно содержать описание, установку и использование.