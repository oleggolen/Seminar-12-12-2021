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
## Работа с удаленным репозиторием
Репозитории можно создавать не только на ПК, но и использовать для этого специальные сервисы. Один из самых популярных сервисов *__GitHub__*.

Этот сервис интегрируется с Git, а также его можно связать с VScode. Для этого нужно перейти по ссылке на [GitHub](https://github.com/ "GitHub") и зарегистрироваться на сайте.

На этом сервисе можно как создавать свои репозитории и работать с файлами непосредственно там, так и переносить репозитории с него на свой ПК, работать с файлами, а потом переносить внесенные изменения на сервис. Также там можно увидеть репозитории других людей. 

Подобные сервисы дают широкие возможности для командной работы. Поскольку каждый член команды может вносить свои изменения, а потом все это собирается в один законченный проект прямо на сервисе.

Для того, чтобы перенести удаленный репозиторий на свой ПК нужна команда:

*__git clone <URL-адрес репозитория>__*

Откуда взять *__URL-адрес__*? 

Над названием репозитория вверху справа нажать на *__Code__*, откроется ссылка на репозиторий, выбрать нужно *__HTTPS__*.

![Где взять адрес репо](repo.png)

После того, как репозиторий скачается, необходимо перейти в папку с репозиторием на ПК. Для того, чтобы выбрать нужную папку используют команду:

*__cd <folder_name>__*

*__Folder_name__* - это имя папки с репозиторием.

По умолчанию загружается только главная ветка репозитория, для того чтобы загрузить остальные ветки нужна команда:

*__git checkout <branch_name>__*

Теперь работать можно как в удаленном репозитории, так и в локальном на ПК. Для того, чтобы они могли обмениваться изменениями нужны две команды:

1. Команда, позволяющая скачать все изменения из удаленного репозитория и автоматически слить его с нашей версией репо:

    *__git pull__*

2. Команда, позволяющая отправить нашу версию репозитория на удаленный репозиторий, требующая авторизации на внешнем репозитории:

    *__git push__*

### __Как связать локальный и удаленный репозиторий:__

1. Создать на GitHub новый репозиторий и дать ему имя

2. Использовать команду:

   *__git remote add origin https://github.com <repo_name>__*

   *__Origin__* имя репозитория по умолчанию

3. Задаем название главной ветки

   *__git branch -M main__*

4. Передаем изменения с локального репозитория на главную ветку удаленного


   *__git push -u origin main__*

5. При первой передаче авторизуемся с помощью логина и пароля на *__GitHub__*.

6. В дальнейшем для передачи изменений на удаленный репозиторий достаточно использовать команду:

    *__git push__*

7. В удаленном репозитории мы также можем работать и сохранять изменения с помощью коммитов. Для передачи изменений с удаленного репозитория используем команду

    *__git pull__*

На GitHub бывают как публичные, так закрытые репозитории. К закрытому репозиторию имеют доступ ограниченное число лиц, но если все же человеку со стороны хочется предложить изменения, то пользуются *__pull request__*.

Порядок действий:

1. Необходимо сделать копию чужого репозитория в свой аккаунт, для этого используем кнопку *__fork__* (вилка) в правом верхнем углу.
2. Появляется точна копия чужого репозитория в личном аккаунте.
3. Теперь с этой копией можно работать, клонировав  ее на ПК.
4. Для изменений нужно создать новую ветку
5. Каждое созданное изменение фиксируем (коммитим)
6. Отправляем свою версию проекта на GitHub
7. Нажимаем на сайте *__pull request__*, прелагая свои изменения создателю изначального репозитория.

**The End**

