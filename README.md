# Настройка Git
git config --global user.name "Твоё Имя"           # Установка имени пользователя
git config --global user.email "email@example.com" # Установка email
git config --global core.editor "code --wait"      # Редактор по умолчанию (VS Code)
git config --list                                  # Показать текущие настройки

# Работа с репозиторием
git init                                           # Инициализировать новый репозиторий
git clone URL                                      # Клонировать репозиторий

# Индексация и коммиты
git status                                         # Проверить текущее состояние
git add file.txt                                   # Добавить файл в индекс
git add .                                          # Добавить все изменения
git commit -m "Комментарий"                        # Сделать коммит
git commit -am "Комментарий"                       # Добавить и закоммитить (отслеж. файлы)

# Просмотр истории
git log                                            # Полная история коммитов
git log --oneline                                  # Краткая история
git log --graph --oneline --all                    # История с графом ветвлений

# Работа с ветками
git branch                                         # Показать список веток
git branch feature                                 # Создать новую ветку
git checkout feature                               # Переключиться на ветку
git switch feature                                 # Переключиться (современный способ)
git switch -c feature                              # Создать и переключиться на ветку
git merge feature                                  # Слить ветку в текущую
git branch -d feature                              # Удалить ветку

# Работа с удалёнными репозиториями
git remote -v                                      # Показать удалённые репозитории
git remote add origin URL                          # Добавить удалённый репозиторий
git push origin master                             # Отправить изменения в master
git push -u origin feature                         # Отправить ветку и запомнить её
git pull                                           # Получить и слить изменения
git fetch                                          # Получить изменения без слияния

# Работа с изменениями
git diff                                           # Показать изменения в файлах
git diff --staged                                  # Изменения, подготовленные к коммиту
git restore file.txt                               # Отменить изменения в рабочем файле
git restore --staged file.txt                      # Убрать файл из индекса

# Откаты и сбросы
git reset HEAD~1                                   # Откатить последний коммит (оставить изменения)
git reset --hard HEAD~1                            # Полный откат (безвозвратно)
git revert <hash>                                  # Откатить конкретный коммит (с новым коммитом)

# Работа с тегами
git tag                                            # Показать теги
git tag v1.0                                       # Создать тег
git tag -a v1.0 -m "релиз"                         # Создать аннотированный тег
git push origin v1.0                               # Отправить тег на сервер

# Работа с субмодулями
git submodule add URL path                         # Добавить субмодуль
git submodule update --init --recursive            # Инициализировать и обновить субмодули
