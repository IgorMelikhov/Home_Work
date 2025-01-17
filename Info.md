# Инструкция по работе с git

## Что такое git

*__Git__ - это система контроля и управления версиями с распределенной архитектурой*

## Подготовка репозитория

Прописать пользователя
* git config user.name "name"
* git config user.email "email"

Прописать пользователя локально:
* git config --local--

## Создание сохранений
_Редактируем файл, после чего добавляем его для отслеживания командой add и фиксируем командой commit._
## git add
*команда, которая добавляет файлы, которые нужно отслеживать*

Команды:

* git add name_of_file
* git add .

добавляет все файлы репозитория

## git commit
*команда, которая фиксирует изменения в файле*

Команды:

* git commit -m "message"

фиксируем изменения в одном файле и описываем в чем заключаются изменения

*  git commit -a -m "message"

фиксируем изменения во всех файлов репозитория и описываем в сообщении эти изменения

## Перемещение между сохранениями

*перемещение между сохранениями осуществляется при помощи команды:*
* git checkout commit_code (первые 4 цифры достаточно)
commit code - код коммита, который можно получить дав команду git log

## Состояние репозитория

*проверяет состояние репозитория*

*git status

## Журнал изменений
*команда, которая позволяет увидеть разницу между текущими изменениями и теми, что закоммичены*
* git diff

_Показать все наши изменения:_
* git log

_Показать все наши изменения в графическом виде с указанием веток:_
* git log --graph

_показывает изменения, внесенные в последнем коммите_

* git show
## Ветви в git
*создание новой ветки:*
* git branch branch_name

_вывести список всех веток в файле_
* git branch

_переход к другой ветке_
* git checkout branch_name

## Слияние веток и решение конфликтов 

_слияние веток_
* git merge

*При возникновении конфликта при выполнении команды merge необходимо вручную проверить изменения и убрать лишнее. После чего сохранить изменения.*

## Удаление веток
*Удаление веток произодится командой:*
* git branch -d branch_name

## Справка

Модификатор команд, который выведет информацию о той команде, к которой был пременен:
Пример:
* git commit --help
* git status --help

*Далее представлена информация по работе с удаленными репозиториями.*

Для работы с удаленными репозиториями существует сервис *GitHub*, который позволяет загружать свой собственный репозиторий или же скачивать чей-то для совместной работы над ним. 

Пройдя простую регистрацию на данном сервисе создается "личный кабинет", куда Вы сможете загружать свои или скачивать чужие репозитории. Для начала работы с чужим репозиторием необходимо найти его на сервисе GitHub и выбрать его. Далее нажать на вкладку "Code", скопировать ссылку на данный репозиторий. Затем в терминале VSCode в выбранной Вами папке при помощи команды *__git clone__* (ссылка) перенести выбранный репозиторий с удаленного сервиса на Ваш локальный компьютер. Параллельно с данным действием закаченный репозиторий появляется в "личном кабинете" *GitHub*, и таким образом все внесенные и закоммиченные Вами изменения будут происходить в **нем**, а не в репозитории вашего напарника.


Загрузив на свой компьютер репозиторий и начав работу с ним, можно отслеживать изменения локального репозитория по сравнению с удаленным при помощи команды _**git log**_. С вызовом данной команды представляются коммиты, в которых указан последний коммит локального репозитория (*HEAD*) и последний коммит удаленного репозитория (*origin*). 

Для того, чтобы внесенные в локальный репозиторий изменения добавить в удаленный репозиторий, необходимо вызвать команду _**git push**_.

Для того, чтобы наоборот выгрузить изменения из удаленного репозитория на локальный, необходимо вызывать команду _**git pull**_. Данной командой рекомендуется пользоваться, когда работаете с несколькими людьми над одним репозиторием для избежания конфликтов при слиянии изменений (*__git merge__*).

В случае, когда Вы работаете с несколькими удаленными репозиториями, Вам поможет команда _**git remote**_, которая отслеживает все настроенные удаленные репозитории.

Это базовые команды, необходимые для полноценной работы в Git. Для более глубокого изучения данной программы, рекомендуем посетить сайт LearnGitBranching, в котором сможете узнать о новых командах и отработать уже изученные в представленных там упражнениях! 

**Успехов в изучении Git!**