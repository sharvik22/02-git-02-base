# Домашнее задание к занятию «Основы Git» Шарапат Виктор

## Задание 1. Знакомимся с GitLab и Bitbucket* 

Из-за сложности доступа к Bitbucket в работе достаточно использовать два репозитория: GitHub и GitLab.

Иногда при работе с Git-репозиториями надо настроить свой локальный репозиторий так, чтобы можно было 
отправлять и принимать изменения из нескольких удалённых репозиториев. 

Это может понадобиться при работе над проектом с открытым исходным кодом, если автор проекта не даёт права на запись в основной репозиторий.

Также некоторые распределённые команды используют такой принцип работы, когда каждый разработчик имеет свой репозиторий, а в основной репозиторий пушатся только конечные результаты 
работы над задачами. 

### GitLab

Создадим аккаунт в GitLab, если у вас его ещё нет:

1. GitLab. Для [регистрации](https://gitlab.com/users/sign_up)  можно использовать аккаунт Google, GitHub и другие. 
1. После регистрации или авторизации в GitLab создайте новый проект, нажав на ссылку `Create a projet`. 
Желательно назвать также, как и в GitHub — `devops-netology` и `visibility level`, выбрать `Public`.
1. Галочку `Initialize repository with a README` лучше не ставить, чтобы не пришлось разрешать конфликты.
1. Если вы зарегистрировались при помощи аккаунта в другой системе и не указали пароль, то увидите сообщение:
`You won't be able to pull or push project code via HTTPS until you set a password on your account`. 
Тогда перейдите [по ссылке](https://gitlab.com/profile/password/edit) из этого сообщения и задайте пароль. 
Если вы уже умеете пользоваться SSH-ключами, то воспользуйтесь этой возможностью (подробнее про SSH мы поговорим в следующем учебном блоке).
1. Перейдите на страницу созданного вами репозитория, URL будет примерно такой:
https://gitlab.com/YOUR_LOGIN/devops-netology. Изучите предлагаемые варианты для начала работы в репозитории в секции
`Command line instructions`. 
1. Запомните вывод команды `git remote -v`.
1. Из-за того, что это будет наш дополнительный репозиторий, ни один вариант из перечисленных в инструкции (на странице 
вновь созданного репозитория) нам не подходит. Поэтому добавляем этот репозиторий, как дополнительный `remote`, к созданному
репозиторию в рамках предыдущего домашнего задания:
`git remote add gitlab https://gitlab.com/YOUR_LOGIN/devops-netology.git`.
1. Отправьте изменения в новый удалённый репозиторий `git push -u gitlab main`.
1. Обратите внимание, как изменился результат работы команды `git remote -v`.

#### Как изменить видимость репозитория в  GitLab — сделать его публичным 

* На верхней панели выберите «Меню» -> «Проекты» и найдите свой проект.
* На левой боковой панели выберите «Настройки» -> «Основные».
* Разверните раздел «Видимость» -> «Функции проекта» -> «Разрешения».
* Измените видимость проекта на Public.
* Нажмите «Сохранить изменения».

## Решение 1
1. Регистрация
   
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/0102803a-0f6c-416e-be2c-34b7429800b5)


2. После регистрации или авторизации в GitLab создайте новый проект, нажав на ссылку `Create a projet`. 
Желательно назвать также, как и в GitHub — `devops-netology` и `visibility level`, выбрать `Public`.

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/c8f55f9e-249d-4f79-b71f-8f7e99f0dd77)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/8a2a411d-a3ec-4f5c-b55d-6f2ffd395a77)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/d940b77d-b6e0-4452-a5a9-3f96ca97fe76)

4. Добавиль пароль

5. Перейдите на страницу созданного вами репозитория, URL будет примерно такой: https://gitlab.com/YOUR_LOGIN/devops-netology.
Изучите предлагаемые варианты для начала работы в репозитории в секции Command line instructions.

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/8abd6488-e611-4849-ad03-39a7de99869a)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/0933a01e-f4ab-48ad-a234-89c94f671064)

6. Запомните вывод команды git remote -v

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/85522c76-b4db-4b38-a042-45f03cc679be)

7. Из-за того, что это будет наш дополнительный репозиторий, ни один вариант из перечисленных в инструкции (на странице вновь созданного репозитория) нам не подходит. Поэтому добавляем этот репозиторий, как дополнительный remote,
к созданному репозиторию в рамках предыдущего домашнего задания: git remote add gitlab https://gitlab.com/YOUR_LOGIN/devops-netology.git.

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/3510ffc4-9d59-4bcf-9318-5ea0a39ba7db)

8. Отправьте изменения в новый удалённый репозиторий git push -u gitlab main.

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/a7e9e23a-3c52-4a8c-b4be-ae518a50d3ef)

9. Обратите внимание, как изменился результат работы команды git remote -v.

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/9209169b-2f9e-44c4-8901-08eaf763d1f7)

---

## Задание 2. Теги

Представьте ситуацию, когда в коде была обнаружена ошибка — надо вернуться на предыдущую версию кода,
исправить её и выложить исправленный код в продакшн. Мы никуда не будем выкладывать код, но пометим некоторые коммиты тегами и создадим от них ветки. 

1. Создайте легковестный тег `v0.0` на HEAD-коммите и запуште его во все три добавленных на предыдущем этапе `upstream`.
1. Аналогично создайте аннотированный тег `v0.1`.
1. Перейдите на страницу просмотра тегов в GitHab (и в других репозиториях) и посмотрите, чем отличаются созданные теги. 
    * в GitHub — https://github.com/YOUR_ACCOUNT/devops-netology/releases;
    * в GitLab — https://gitlab.com/YOUR_ACCOUNT/devops-netology/-/tags;
    * в Bitbucket — список тегов расположен в выпадающем меню веток на отдельной вкладке.

## Решение 2

### Gitlab

1.Создайте легковестный тег `v0.0`

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/e27a5210-d4ad-4e76-8dc0-65f4964a8559)

2.Аналогично создайте аннотированный тег `v0.1`

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/92c381eb-69cd-43bf-bd4b-40d9e1525e17)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/28cc33b4-bca9-4cfb-9920-f336235d31bc)

пушим теги

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/8ee6a96e-f835-4e15-9f45-2668aeacd9bd)


https://gitlab.com/my8585319/devops-netology/-/tags

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/db536e6f-3c08-432c-93c3-bade805e33c6)

### GitHub

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/f89cdc16-7cb7-41ad-9d7b-462aff0a5b00)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/c7b0454c-fb9a-4d8f-9253-9b7d93395daf)


![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/8c22021e-36c1-4225-8d11-50f27fdfd914)

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/7faeea30-a429-4541-b936-29693ad8ce2c)

https://github.com/sharvik22/devops-netology/tags

Разница в том, что у легковестного тега секция начинается с информации о коммите и нет секции о теги, а у аннотированаго есть секция о теги. Он содержит больше информации (автор, время, комментарий). 

---

## Задание 3. Ветки 

Давайте посмотрим, как будет выглядеть история коммитов при создании веток. 

1. Переключитесь обратно на ветку `main`, которая должна быть связана с веткой `main` репозитория на `github`.
1. Посмотрите лог коммитов и найдите хеш коммита с названием `Prepare to delete and move`, который был создан в пределах предыдущего домашнего задания. 
1. Выполните `git checkout` по хешу найденного коммита. 
1. Создайте новую ветку `fix`, базируясь на этом коммите `git switch -c fix`.
1. Отправьте новую ветку в репозиторий на GitHub `git push -u origin fix`.
1. Посмотрите, как визуально выглядит ваша схема коммитов: https://github.com/YOUR_ACCOUNT/devops-netology/network. 
1. Теперь измените содержание файла `README.md`, добавив новую строчку.
1. Отправьте изменения в репозиторий и посмотрите, как изменится схема на странице https://github.com/YOUR_ACCOUNT/devops-netology/network 
и как изменится вывод команды `git log`.

## Решение 3

Посмотрите лог коммитов и найдите хеш коммита с названием `Prepare to delete and move`, который был создан в пределах предыдущего домашнего задания.
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/9fdc6a26-48ac-44c9-99ed-79af94ad91f1)

Выполните `git checkout` по хешу найденного коммита.
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/a560d2be-52ff-49eb-b3b6-b8b726ecbc81)

Создайте новую ветку `fix`, базируясь на этом коммите `git switch -c fix`
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/ea57093e-eadf-4442-97e4-0ac275ea629d)

Отправьте новую ветку в репозиторий на GitHub `git push -u origin fix`.
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/81b77772-cf03-4933-809f-39488a909827)

Посмотрите, как визуально выглядит ваша схема коммитов: https://github.com/sharvik22/devops-netology/network
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/91e5bc88-a1a7-4c11-b6a4-44cf793a0cb4)

Теперь измените содержание файла `README.md`, добавив новую строчку
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/77bfecb6-787e-4d98-ba1b-54bff779ab47)

Отправьте изменения в репозиторий и посмотрите, как изменится схема на странице https://github.com/sharvik22/devops-netology/network

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/229e92fe-f10c-4040-b9a2-837efe0a5885)

и как изменится вывод команды `git log`.
![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/97d08e36-e601-481d-b7f5-4ce179fbdaf9)

---

## Задание 4. Упрощаем себе жизнь

Попробуем поработь с Git при помощи визуального редактора. 

1. В используемой IDE PyCharm откройте визуальный редактор работы с Git, находящийся в меню View -> Tool Windows -> Git.
1. Измените какой-нибудь файл, и он сразу появится на вкладке `Local Changes`, отсюда можно выполнить коммит, нажав на кнопку внизу этого диалога. 
1. Элементы управления для работы с Git будут выглядеть примерно так:

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/71a131d9-3e57-42f6-84f0-fe0b2bf7284e)

 
1. Попробуйте выполнить пару коммитов, используя IDE. 

[По ссылке](https://www.jetbrains.com/help/pycharm/commit-and-push-changes.html) можно найти справочную информацию по визуальному интерфейсу. 

Если вверху экрана выбрать свою операционную систему, можно посмотреть горячие клавиши для работы с Git. 
Подробней о визуальном интерфейсе мы расскажем на одной из следующих лекций.

## Решение 4

![image](https://github.com/sharvik22/02-git-02-base/assets/136818757/397d2d22-290e-409a-b223-4b0b223e334e)





---

*В качестве результата работы по всем заданиям приложите ссылки на ваши репозитории в GitHub, GitLab и Bitbucket*.  
Bitbucket* (задание со звёздочкой) Это самостоятельное задание, его выполнение необязательно.
 ----




