# Инструкция по работе с Git и удалёнными репозиториями

## Что такое Git?

Git - одна из реализаций распределённых систем контроля версий, имеющая как лольную версионность, так и версионность на сервере. Git является самой популярной системой контроля версий на сегодняшний день.

## Подготовка репозитория
Для того, чтобы создать репозиторий в указанной папке используется команда *git init*. Для этого достаточно написать команду *git init* в папке с будущем репозиторием

## Создание фиксаций
### Просмотр информации о изменениях

Для того, чтобы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду *git status*. Для этого достаточно использовать *git status* в папке с репозиторием

### Добавление файла к коммиту
Для того, чтобы добавить файл к новому коммиту("сохранению") необходимо использовать команду *git add*. Используется она следующим образом: в папке с репозиторием пишем команду *git add <имя файла>*

### Создание коммитов

Для создания новой фиксации необходимо использовать команду *git commit*. Используется она следующим образом: в папке с репозиторием пишется команда *git commit -m "<сообщение к коммиту>"*. Все файлы коммита должны быть предворительно добавлены с помощью команды *git add*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***

## Перемещение между сохранениями
Для перемещения между коммиитами необходимо использовать команду *git checkout*. Используется она следующим образом в папке с репозиторием: *git checkout <номер комиита>*.

## Журнал изменений
Для просмотра журнала изменений необходимо использовать команду *git log*. Для этого нужно в папке с репозиторием написать *git log*

## Ветки в Git
### Создание веток в Git
Для того, чтобы создать новую ветку необходимо использовать команду *git brnach*. Используется она следующим образом в папке с репозиторием: *git branch <название ветки>*.
### Просмотр списка веток
Для того, чтобы просмотреть список веток необходимо использовать команду *git branch*. Для этого в папке с репозиторием надо набрать команду *git branch*

### Переход между ветками
Для того, чтобы перейти на другую ветку необходимо использовать команду *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <название ветки>*.

## Слияние веток и разрешение конфликтов
### Слияние веток
Для слияния веток необходимо использовать команду *git merge*. Используется она следующим образом: Для начала ***ОБЯЗАТЕЛЬНО*** перейти на ветку, куда мы сливаем изменения, после чего надо воспользоваться командой *git merge <название сливаемой ветке>*. Слияние может произойти автоматически, а может вознить конфликт. Про разрешение конфликтов смотри дальше.

## Удаление веток

## Работа с удаленными репозиториями

### Что такое удаленный репозиторий и для чего он нужен

Для того, чтобы иметь возможность совместно с другими пользователями работать в каком-либо Git-проекте, необходимо использовать удалённые репозитории. Удалённые репозитории представляют собой версии проектов, сохранённых в интернете или ещё где-то в сети.

### Базовая работа с удаленными репозиториями GitHub

#### Просмотр удалённых репозиториев

Для того, чтобы просмотреть список настроенных удалённых репозиториев, необходимо выполнить команду: `git remote`. Если репозиторий был клонирован, то на экране появится как минимум `origin` - имя по умолчанию, которое Git даёт серверу, с которого производилось клонирование (с помощью комманды `git clone <адерс удалённого репозитория>`)

Для того, чтобы чтобы просмотреть адреса для чтения и записи, привязанные к репозиторию необходимо использовать команду: `git remote -v`

    git remote -v
    origin  https://github.com/CovChEGG/Seminar-12-12-2021.git (fetch)
    origin  https://github.com/CovChEGG/Seminar-12-12-2021.git (push)

Где `fetch` - отображает адрес скачивания данных, а `push`- отображает адрес для записи данных, при этом вывод команды не даёт никакой информации о правах доступа (только адрес и назначение).





###### The end
