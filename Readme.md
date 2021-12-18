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

Пример:

Мы сделали слияние ветки Prepare_Repository 

>PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00">  git </font>  merge Prepare_Repository  
Auto-merging Instructions for working with GIT.md  
Merge made by the 'ort' strategy.  
 Instructions for working with GIT.md | 10 <font color="#00FF00"> ++++++++++  </font>  
 1 file changed, 10 insertions(+)  
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT>

Здесь мы видим, что всё прошло успешно.

<font color="#7FFFD4">

### Разрешение конфликтов
</font>

Может произойти при слиянии конфликт. То есть атоматическое слияние не понимает, что с чем сделать слияние и предагает нам варианты его разрешения

>PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00"> git  </font> merge Creating_Fixations  
Auto-merging Instructions for working with GIT.md  
CONFLICT (content): Merge conflict in Instructions for working with GIT.md  
Automatic merge failed; fix conflicts and then commit the result. <p></p> 
Далее выбираем подходящий нам вариант и делаем коммит.  <p></p>
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00" >git  </font>  add <font color="#00CED1">'.\Instructions for working with GIT.md'  </font>
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00"> git </font> commit -m <font color="#00CED1"> "Разрешили конфликт" </font>  
[master d5b4fd7] Разрешили конфликт  
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT>

## Удаление веток

Для того чтобы удалить ветку можем использоать команду <***`git branch -d <имя ветки>`***>.
Ветка которую мы хотим удалить должна быть слита.

Пример:  

Для начала вводим команду <***`git branch`***>.  
Потом выбираем ветку которую хотим удалить  <***`git  branch -d Prepare_Repository`***>.



>PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00">  git </font> branch  
  Branches_in_Git  
  Change_Log  
  Conclusion  
  Creating_Fixations  
  Merging_branches_and_resolving_conflicts  
  Move_Between_Saves  
  Prepare_Repository  - эту ветку будем удалять 
  Removing_Branches  
\*<font color="#00FF00"> master </font>  
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00"> git </font>  branch -d Prepare_Repository   
Deleted branch Prepare_Repository (was 86b9d8d).  a870839). - Git гоорит, что ветка успешна удалена.    
Далее проеряем, что этой ветки нет  
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> <font color="#FFFF00">  git </font> branch  
  Branches_in_Git  
  Change_Log  
  Conclusion  
  Creating_Fixations  
  Merging_branches_and_resolving_conflicts  
  Move_Between_Saves  
  Removing_Branches  
\* <font color="#00FF00"> master  </font>  
PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT

## Работа с удаленными репозиториями
Команды для работы c репозиториями
Команда <git clone <сетеой адрес>> Эта команда позволяет склонировать внешний репозиторий на наш ПК

PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> git clone https://github.com/Alexandr-Galaktionov/Seminar-12-12-2021.git

Команда <git pull>
Эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией

PS C:\Основы GIT\Домашка\ДЗ_2_Истркуция по работе с GIT> git pull

Команда <git pash> эта команда позволяет отправить нашу версию репозитория на внешний репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ на внешнем репозитории

Как сделать pull request
Делаем fork репозитория
Делаем clone СВОЕЙ версии репозитория
Создаем новую ветку и в НЕЕ вносим свои изменения
Фиксируем изменения ( делаем коммиты )
Отправляем свою версию в свой GitHub
На сайте GitHub нажимаем кнопку pull request

###### The end
