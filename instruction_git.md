# **Инструкция по работе с системой контроля версий Git**

![логотип](git.png)

## Что такое Git?

Git - система управления версиямии с распределенной архитектурой, что позволяет хранить историю изменений а полном объеме.

## Создание репозитория 

Чтобы создать новвый репозиторий (инициализировать) используют команду: 

    git init

## Проверка состояния репозитория

Для того чтобы проверить текущее состояние репозитория: актуальна ли информация и нет ли чего-то нового, используют команду:

    git status

## Добавление/сохранение изменений

Для того чтобы добавить/сохранить изменения необходимо сохранить изменения через "файл-сохранить" или "cmd + s" (***Данное действие необходимо выполнять каждый раз перед введением любой команды***)

Далее ввести команду добавления текущего файла в терминал:

    git add <file_name>

Где *file_name* - имя текущего файла.

И записать все изменения через команду:

    git commit

Для того, чтобы было удобно читать файл и перемещаться по нему, необходимо все записи проименовывать, т.е. присвавать "сообщение" (Message). Имена действиям лучше давать исходя из самого действия. Например, добавили заголовок файла и в команду *git commit* вводим "Добавление заголовка".

Для ввода данного действия используют команду:

    git commit -m

Также, для более оперативной и продуктивной работы мы можем команды *git add* и *git commit* вписать в одну команду:

    git commit -am

И далее проименовать действие, которое мы хотим закомитить.

## Просмотр истории коммитов

Для того чтобы просмотреть всю историю изменений используют команду:

    git log

Для облегчения просмотра и вывода макисмально минимальной информации о комитах можно использовать команду:

    git log --oneline

Что позволит нам вывести всю информацию о каждом коммите в своей строчке.

В случае возврата к предыдущим сохранениям (см.ниже) в терминале после команды *git log* могут отображаться не все коммиты. Чтобы отобарзить все коммиты необходимо ввести команду:

    git log --all

*или*

    git log --oneline --all


## Просмотр изменений

Перед тем как закомитить информацию можно посмотреть были ли сделаны изменения в файле. Для этого используют команду:

    git diff

 С помощью этой команды можно посмотреть изменения с конкретного коммита. Для этого необходимо ввести команду и адрес коммита (достаточно первые 4-5 символов), с которого мы хотим посмотреть изменения. Например:

    git diff 43169 

Также мы можем посмотреть изменения указав промежуток от одного коммита до другого. Для этого необходимо ввести команду и адреса коммитов от какого до какого мы хотим посмотреть изменения. Например:

    git diff d020c e2588

## Возврат к предыдущим сохранениям

Для того чтобы вернуться к предыдущим сохранениям необходимо ввести команду:

    git checkout

После ввода команды необходимо указать к какому сохранению мы хотим вернуться. Для этого после команды необходимо ввести адрес коммита с которого мы хотим продолжить работу. Например:

    git checkout ecb31

Чтобы вернуться к самому актуальному сохранению после команды нужно ввести:

    git checkout master/main

## Ветвление

Ветвление - это создание дополнительных "веток" (версий) файла в самом файле, для более детальной проработки.

### Просмотр существующих веток

Для того чтобы посмотреть какие ветки созданы используется команда:

    git branch

Где активная ветка (в которой сейчас происходит работа) будет подсвечена контрастным цветом.

### Создание новой ветки

Для создания новой ветки необходимо ввести команду:

    git branch name_branch

Где _new_branch_ название новой ветки.

Для перехода из одной ветки в другую, необходимо ввести команду:

    git checkout name_branch

## Слияние веток

Для слияния веток используется команда:

    git merge name_branch

Слияние веток будет проходить в ту ветку, в которой вы работаете в данный момент

## Удаление ветки

Для того, чтобы удалить неиспользуемую ветку необходимо ввести команду:

    git branch -d name_branch

## Удаленные репозитории

### Связывание локального репозитория с удаленным


    
