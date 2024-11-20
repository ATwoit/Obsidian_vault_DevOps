Ссылка на полный курс по Git - https://www.youtube.com/playlist?list=PLDyvV36pndZFHXjXuwA_NywNrVQO0aQqb

Игра по Git - https://learngitbranching.js.org/?locale=ru_RU&demo=

Ссылка на курс 2 - https://gitimmersion.com/lab_01.html


## 1.1 Git - Введение - Что такое Git ?

Git - это система контроля версий. Хранилище, базы данных 
- Хранилтище истории разроботки 
- Обмен историей разроботки 
- Распределенная система 
- Надежная система 

==Установка Git==

- На Linux
```bash
apt-get install git
yum install git
```
- Mac
```mac
Terminal / iTerm
- git
```
 > Homebrew / Macports

## 2.1 Git - Основы - Конфигурация

![[Screenshot 2024-10-14 094827.png]]

Для поиска и работы команды пишем так:
```
git help <команда которая нам нужна>
```
Так же для поиска можно использовать `/`, `n` это поиск вперед, `shift n` поиск назад. 

==Основные команды Git==

| Команда                                                   | Описание                                                                |
| --------------------------------------------------------- | ----------------------------------------------------------------------- |
| `git init`                                                | Создает новый репозиторий Git в текущей директории.                     |
| `git clone <URL>`                                         | Клонирует удалённый репозиторий на ваш компьютер.                       |
| `git status`                                              | Показывает текущее состояние рабочего каталога и индекса.               |
| `git add <file>`                                          | Добавляет указанный файл в индекс (подготовка к коммиту).               |
| `git add .`                                               | Добавляет все изменения в индекс.                                       |
| `git commit -m "Your commit message"`                     | Сохраняет изменения в репозитории с сообщением о коммите.               |
| `git log`                                                 | Показывает историю коммитов в текущей ветке.                            |
| `git checkout <branch-name>`                              | Переключает на указанную ветку.                                         |
| `git checkout -b <new-branch-name>`                       | Создает новую ветку и сразу переключается на неё.                       |
| `git branch <new-branch-name>`                            | Создает новую ветку, но не переключает на неё.                          |
| `git merge <branch-name>`                                 | Сливает указанную ветку с текущей.                                      |
| `git branch -d <branch-name>`                             | Удаляет указанную ветку.                                                |
| `git push origin <branch-name>`                           | Отправляет ваши изменения на удалённый репозиторий.                     |
| `git pull`                                                | Получает и сливает изменения из удалённого репозитория в текущую ветку. |
| `git diff`                                                | Показывает изменения между рабочим каталогом и индексом.                |
| `git checkout -- <file>`                                  | Отменяет изменения в указанном файле.                                   |
| `git reset <file>`                                        | Удаляет файл из индекса (не из рабочего каталога).                      |
| `git config --global user.name "Your Name"`               | Настраивает имя пользователя для всех репозиториев.                     |
| `git config --global user.email "your_email@example.com"` | Настраивает email пользователя.                                         |
| `git config --list`                                       | Показывает текущие настройки конфигурации Git.                          |

## Git show, кто такие автор и коммиттер

```git
git show --pretty=fuller
```
![[Screenshot 2024-11-13 102522.png]]

## Commit  "Без Add"

- git commit -a
- git commit `<paths>`
- alias.commitall '!git add .; git commit'
	- alias.commitall '!git add -A; git commit'

## Удаление и переименование файлов

