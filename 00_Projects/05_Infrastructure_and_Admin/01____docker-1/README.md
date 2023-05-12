<center><image src="https://github.com/evgenkarlson/ALL_SCHOOL_42/raw/master/03_Norme____(%D0%9D%D0%BE%D1%80%D0%BC%D1%8B_%D0%B8_%D0%9F%D1%80%D0%B0%D0%B2%D0%B8%D0%BB%D0%B0_%D0%A8%D0%BA%D0%BE%D0%BB%D1%8B)/src/page1image3852832-small-13.png"></center>
</br>
<center><h2>Docker-1</h1></center>
</br>
<center><h2>Теперь вы думаете о контейнерах...</h2></center>
</br>
<center><i>Резюме: Греби, греби, греби на лодке... плавно вниз по течению...</i></center>
</br>
</br>
</br>

# Глава I.

## Предисловие

</br>

Вот что говорит Википедия об Усатом Ките:  

Усатый кит - это фильтрующая система внутри рта усатых китов. Система китового уса работает, когда кит открывает пасть под водой и впитывает воду. Затем кит выталкивает воду, а животные, такие как криль, фильтруются китовым усом и остаются источником пищи для кита. Усатый усат похож на щетину и состоит из кератина, того же вещества, что и человеческие ногти и волосы. Усатый кит - производное кожи. У некоторых китов, например, у гренландского кита, китовый ус длиннее, чем у других. Другие киты, такие как серый кит, используют только одну сторону китового уса. Эти щетинки китового уса расположены пластинами на верхней челюсти кита. Усатый ус часто называют китовым усом, но это название также может относиться к нормальным костям китов, которые часто использовались в качестве материала, особенно в качестве более дешевой замены слоновой кости в резьбе.  

Слово `baleen` происходит от латинского слова `balaena`, связанного с греческим `phalaina` - оба слова означают `Кит`.  

Раньше люди использовали китовый ус (обычно называемый «китовым усом») для изготовления множества предметов, где требовались гибкость и прочность, в том числе скребки для спины, ребра жесткости воротника, кнуты для багги, ребра от зонтиков, нижние юбки из кринолина и корсеты. Его обычно использовали для складывания бумаги; его гибкость не позволяла повредить бумагу. Он также иногда использовался в луках с тросовой подкладкой. В настоящее время для аналогичных целей обычно используются синтетические материалы, особенно пластик и стекловолокно. Не следует путать с китовой костью, означающей кости китов, используемые в резьбе по дереву, для ручек столовых приборов и в других целях для костей различных крупных видов.  


</br>
</br>
</br>

# Глава II. 

## Вступление

Возможно, вы столкнулись с одной из этих неприятных ситуаций:  
- Вы разрабатываете на компьютере, и у вас нет прав администратора для установки зависимости.  
- Вам потребовалось пять часов, чтобы установить последнюю версию вашей любимой БД, но ваш начальник говорит вам, что приложение должно работать с предыдущей версией.  
- Вам потребовалось две недели, чтобы создать идеально чистое приложение... которое работает только на вашем компьютере.  
- `SysOp`, отвечающий за все запуски, ненавидит вас, потому что ваше приложение невозможно развернуть.  

Короче говоря, у вас уже есть или скоро вы потратите в какой-то момент своей жизни столько же времени на настройку своей рабочей среды, сколько на фактическую разработку своего приложения.  

Прямо сейчас вы, вероятно, разрабатываете одноблочное приложение с программным обеспечением и библиотеками, установленными непосредственно в вашей среде разработки или, может быть, в виртуальной среде ... Представьте, что ваше приложение должно быть развернуто по всему миру, и вам нужно повторно разработать его для всех существующих платформ и ОС ...  

Docker был создан для удовлетворения этой потребности в унификации и нормализации: он позволяет разделить приложение на несколько микросервисов, легких, адаптируемых, универсальных и масштабируемых, а также дает системным администраторам большую гибкость для развертывания и масштабирования приложения.  

Этот набор проектов на Docker поможет вам лучше понять этот конкретный инструмент, а также различные аспекты разработки приложений с использованием микросервисов.  

</br>
</br>
</br>

# Глава III. 

## Цели

</br>

### III.1 Прежде чем мы начнем

Цель проекта `Docker-1` - заставить вас работать с `docker` и `docker-машиной`, базами для понимания идеи контейнеризации сервисов. Вы можете рассматривать этот проект как начало. Но прежде чем отправиться в это приключение, важно предупредить вас о нескольких вещах:  

- Вы будете выполнять упражнения как минимум на `docker 1.12`. Если вы не знаете, какая у вас версия докера, вы можете запустить `docker version`. `Brew` всегда предоставляет последнюю версию докера ... просто говорю.  

- ЧРЕЗВЫЧАЙНО важно, чтобы бинарный файл `docker-машины` был доступен на вашем дампе, прежде чем вы начнете исследовать чудесный мир контейнеров и воспользуетесь бонусами. Прочтите документацию по `docker`, доступную в Интернете, чтобы установить ее при необходимости.  

- Найдите время, чтобы внимательно прочитать документацию. Рано или поздно тебе все равно придется.  

</br>

### III.2 Путеводитель автостопщика по контейнерам

Когда вы работаете над этим проектом, мы НАСТОЯТЕЛЬНО советуем вам иметь под рукой официальную документацию по `docker`, чтобы правильно обрабатывать ваши будущие контейнеры. Вам также следует взглянуть на документацию для официальных контейнеров, которые мы попросим вас реализовать на протяжении всего этого проекта.  
Вы очень скоро поймете, что вам не нужно заново изобретать велосипед каждый раз, когда вы захотите разработать приложение или реализовать конкретный сервис.  

С этой точки зрения вот несколько очень полезных ссылок для вашего проекта:  
- [Отличная официальная документация Docker](https://docs.docker.com)  
- [Публичный реестр Docker](https://hub.docker.com)  
- [Официальный Github Docker со многими предстоящими проектами](https://github.com/docker)  
- [Блог Джесси Фразель, бывшего основного автора Docker](https://blog.jessfraz.com)  
- [Ее Github с множеством хороших идей](https://github.com/jessfraz)  

</br>
</br>
</br>

# Глава IV. 

## Основные инструкции

- Проект будет исправлен людьми  

- Для оценки контейнеры будут размещены на дампе коррекции и локально.  

- Вы не можете исправить свой проект с помощью контейнера, размещенного на удаленном компьютере. Прочтите правило выше, если вы его не понимаете.  

- В вашем репозитории будет 2 папки (+1, если вы сделали бонусы):  
  - 00_how_to_docker  
  - 01_dockerfiles  
  - 02_bonus [BONUS]  

В каждом файле должна быть своя древовидная структура, определенная в соответствующем
главы.  

> По соображениям хранения мы советуем вам переместить папки `.docker` и `VirtualBox VMs` из вашей домашней дериктории в `goinfre` и использовать символические ссылки.  

</br>
</br>
</br>

# Глава V.

## Обязательная часть

</br>

### V.1 Как в Docker

В этой первой части вы познакомитесь с Docker и его основными параметрами. В вашем репозитории создайте папку `00_how_to_docker`, в которую вы будете помещать решения для всех упражнений.  

Если у вас его еще нет, установите `docker`, `docker-machine` и `virtualbox`. `Docker` и `docker-machine` могут быть установлены через `Brew`, а `virtualbox` - через `Managed Software Center`.  

Убедитесь, что `docker version` распечатывает вашу текущую версию докера и что у вас есть докер не ниже `1.12` (Примечание редактора: на момент написания статьи используется новая нотация управления версиями, а самая последняя версия - `17.03.0-ce-mac2`).  

У вас может возникнуть соблазн использовать `Docker for Mac`, и я вам сочувствую. Не волнуйтесь, вы будете использовать его в следующих проектах `Docker`. Но для этого проекта вам нужно будет реализовать кластеризацию локально, и это довольно легко сделать с помощью `docker-machine`!  

Вы поместите свою работу в папку `00_how_to_docker`: по одному файлу на упражнение, названному по номеру упражнения, с командой или командами, запрошенными для этого упражнения.  

```
$> ls 00_how_to_docker
01    02    03    04    06    
[...]
31    32    33    34
$> cat 00_how_to_docker/01
docker-machine [...]
```

</br>

### V.2  Упражнения  

Для каждого упражнения мы попросим вас дать команду(-ы) оболочки для:  

1. Создайте виртуальную машину с `docker-machine`, используя драйвер `virtualbox`, и назовите ее `Char`.  

2. Получите `IP`-адрес виртуальной машины `Char`.  

3. Определите переменные, необходимые вашей виртуальной машине `Char` в общем окружении вашего терминала, чтобы вы могли без ошибок запускать команду `docker ps`. Вы должны исправить все четыре переменные среды с помощью одной команды, и вам не разрешается использовать встроенные функции вашей оболочки для установки этих переменных вручную.  

4. Получите контейнер `hello-world` из `Docker Hub`, где он доступен.  

5. Запустите контейнер `hello-world` и убедитесь, что он печатает приветственное сообщение, а затем покидает его.  

6. Запустите контейнер `nginx`, доступный в `Docker Hub`, в качестве фоновой задачи. Он должен называться `overlord`, иметь возможность перезапускаться самостоятельно, и его порт `80` должен быть подключен к порту `5000` виртуальной машины `Char`. Вы можете проверить правильность работы вашего контейнера, посетив `http://<ip-de-char>:5000` в вашем веб-браузере.  

7. Получить внутренний `IP`-адрес контейнера `overlord` без запуска его оболочки и одной командой.  

8. Запустите оболочку из контейнера `alpine` и убедитесь, что вы можете напрямую взаимодействовать с контейнером через свой терминал, и что контейнер удаляется после завершения выполнения оболочки.  

9. Из оболочки контейнера `debian` установите через диспетчер пакетов контейнера все необходимое для компиляции исходного кода `C` и поместите его в репозиторий `git` (конечно, перед этим убедитесь, что диспетчер пакетов и пакеты уже в контейнере обновляются). В этом упражнении вы должны указать только команды, которые будут запускаться непосредственно в контейнере.  

10. Создайте том с именем `hatchery`.  

11. Перечислите все тома `Docker`, созданные на машине. Помните. ТОМА.  

12. Запустите контейнер `mysql` в качестве фоновой задачи. Он должен иметь возможность перезапускаться самостоятельно в случае ошибки, а `root` пароль, базы данных, должен быть `Kerrigan`. Вы также убедитесь, что база данных хранится в томе `hatchery`, что контейнер напрямую создает базу данных с именем `zerglings`, а сам контейнер называется `spawning-pool`.  

13. Выведите переменные среды контейнера `spawning-pool` за одну команду, чтобы убедиться, что вы правильно настроили свой контейнер.  

14. Запустите контейнер `wordpress` в качестве фоновой задачи, просто для удовольствия. Контейнер должен называться `lair`, его порт `80` должен быть привязан к порту `8080` виртуальной машины, и он должен иметь возможность использовать контейнер `spawning-pool` в качестве службы базы данных. Вы можете попытаться получить доступ к `lair` на своей машине через веб-браузер, указав `IP`-адрес виртуальной машины в качестве `URL`.  
Поздравляем, вы только что развернули работоспособный веб-сайт на Wordpress двумя командами!  

15. Запустите контейнер `phpmyadmin` в качестве фоновой задачи. Он должен называться `roach-warden`, его порт `80` должен быть привязан к порту `8081` виртуальной машины, и он должен иметь возможность исследовать базу данных, хранящуюся в контейнере `spawning-pool`.  

16. Просматривайте журналы контейнера `spawning-pool` в режиме реального времени, не запуская его оболочку.  

17. Отобразите все активные в данный момент контейнеры на виртуальной машине `Char`.  

18. Перезапустите контейнер `overlord`.  

19. Запустите контейнер с именем `Abathur`. Это будет контейнер `Python`, версии`2-slim`, его папка `/root` будет привязана к папке `HOME` на вашем хосте, а его порт `3000` будет привязан к порту `3000` вашей виртуальной машины. Персонализируйте этот контейнер, чтобы иметь возможность использовать микро-фреймворк `Flask` самой последней версии. Убедитесь, что `html`-страница, отображающая `Hello World` с тегами `<h1>`, может обслуживаться `Flask`. Проверьте, что ваш контейнер правильно настроен, обратившись через `curl` или веб-браузер к `IP`-адресу вашей виртуальной машины через порт `3000`. Вы также перечислите все необходимые команды в своем репозитории.  

20. Создайте локальный рой, его менеджером должна быть виртуальная машина `Char`.  

21. Создайте еще одну виртуальную машину с `docker-machine»` используя драйвер `virtualbox`, и назовите ее `Aiur`.  

22. Превратите `Aiur` в подчиненного местного роя, в котором `Char` является лидером (команда взять под контроль `Aiur` не запрашивается).  

23. Создайте внутреннюю сеть  типа `overlay`, которую вы назовете `overmind`.  

24. Запустите СЛУЖБУ `rabbitmq SERVICE`, которая будет называться `orbital-command`. Вы должны определить конкретного пользователя и пароль для службы `RabbitMQ`, они могут быть какими угодно. Эта услуга будет в надразумной сети.  

25. Перечислите все службы местного роя.  

26. Запустите службу `42school/engineering-bay` в двух точках и убедитесь, что служба работает правильно (см. Документацию на сайте `hub.docker.com`). Эта служба будет называться `engineering-bay` и будет находиться в сети `overmind`.  

27. Получайте в реальном времени журналы выполнения одной из задач службы `engineering-bay`.  

28. ... Черт побери, группа зергов атакует `orbital-command`, и отключение службы `engineering-bay` совершенно не поможет ... Вы должны послать отряд морских пехотинцев, чтобы уничтожить злоумышленников. . Запустите `42school/marine-squad` в двух точках и убедитесь, что сервис работает должным образом (см. Документацию на сайте `hub.docker.com`). Этот сервис будет называться ... `marines` и будет находиться в сети `overmind`.  

29. Отображение всех задач службы `marines`.  

30. Увеличьте количество экземпляров службы `marines` до двадцати, потому что `Морских пехотинцев`(marines) никогда не бывает достаточно, чтобы уничтожить `Зергов`. (Не забудьте взглянуть на задачи и журналы службы, вы увидите, это весело.)  

31. Завершить принудительно и удалить все службы в локальном рое одной командой.  

32. Завершить принудительно и удалить все контейнеры (независимо от их статуса) одной командой.  

33. Удалите все образы контейнеров, хранящиеся на виртуальной машине `Char`, также с помощью одной команды.  

34. Удалите виртуальную машину `Aiur` без использования `rm -rf`.  

</br>
</br>
</br>

# Глава VI.

## Dockerfiles


Итак, это было весело, не так ли?  

А теперь пора приступить к делу. `Docker` позволяет создавать СОБСТВЕННЫЕ контейнеры для ваших СОБСТВЕННЫХ приложений! Вот о чем эта глава. К счастью, `Docker` позволяет вам программировать `Dockerfiles` (он же `Makerfile` для `Docker` ... Я думаю, вы уловили нюанс). `Dockerfiles` использует особый синтаксис, который повторно использует базовый образ или существующий контейнер для добавления ваших собственных зависимостей и ваших собственных файлов.  

Вы также заметите, что каждая команда, созданная вашим `Dockerfiles`, генерирует слой, который можно повторно использовать в других `Dockerfile` или других версиях того же `Dockerfile`, чтобы избежать дублирования данных. Классно, правда?
Но прежде чем вы начнете создавать свои собственные контейнеры, убедитесь, что ваша виртуальная машина очищена от всех образов и оставшихся активных контейнеров. Мы начнем с самого начала и будем создавать все более и более сложные приложения.  

Создайте папку `01_dockerfiles`, в которой вы будете хранить все файлы `Dockerfiles`, которые вам понадобятся позже, в отдельных папках (`ex00` / `ex01` ...).  

Перейдите по этой ссылке, чтобы создать высококачественные файлы `Docker`: [Рекомендации по использованию файлов `Docker`](https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/)  

</br>

### VI.1 Упражнение 00: vim/emacs

---------------------------------------------------------------------
> | Упражнение 00: vim/emacs                                        |
> |-----------------------------------------------------------------|
> | Каталог для сдачи: ex00/                                        |
> | Файлы для сдачи : Dockerfile                                    |
> | Допустимые функции: -                                           |
> | Примечания : нет данных                                         |
---------------------------------------------------------------------

Из `Docker` образа `alpine` вы добавите в свой контейнер ваш любимый текстовый редактор, `vim` или `emacs`, который запустится вместе с вашим контейнером.  

</br>

### VI.2 Упражнение 01: BYOTSS

---------------------------------------------------------------------
> | Упражнение 01: BYOTSS                                           |
> |-----------------------------------------------------------------|
> | Каталог для сдачи: ex01/                                        |
> | Файлы для сдачи : Dockerfile + Скрипты (если это применимо)     |
> | Допустимые функции: -                                           |
> | Примечания : нет данных                                         |
---------------------------------------------------------------------

Из образа `debian` вы добавите соответствующие источники для создания сервера `TeamSpeak`, который будет запускаться вместе с вашим контейнером. Он будет считаться действительным, если хотя бы один пользователь сможет подключиться к нему и участвовать в обычном обсуждении (без надуманной настройки), поэтому обязательно создайте свой `Dockerfile` с правильными параметрами. Ваша программа должна получать исходные коды при сборке, их не может быть в вашем репозитории.  

> Для умников использование официального docker-образа `TeamSpeak` строго ЗАПРЕЩЕНО, и вы получите` -42`.  

</br>

### VI.3 Упражнение 02: Dockerfile в Dockerfile... в Dockerfile ?

---------------------------------------------------------------------
> | Exersize 01: Dockerfile в Dockerfile... в Dockerfile ?          |
> |-----------------------------------------------------------------|
> | Каталог для сдачи: ex02/                                        |
> | Файлы для сдачи : Dockerfile                                    |
> | Допустимые функции: -                                           |
> | Примечания : нет данных                                         |
---------------------------------------------------------------------

Вы собираетесь создать свой первый `Dockerfile` для контейнеризации приложений `Rails`. Это особая конфигурация: этот конкретный `Dockerfile` будет общим и вызываться в другом `Dockerfile`, который будет выглядеть примерно так:  

```
FROM        ft-rails:on-build

EXPOSE      3000
CMD         ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]
```  

Ваш общий контейнер должен установить через рубиновый контейнер все необходимые зависимости и драгоценные камни, а затем скопировать ваше приложение `rails` в папку `/opt/app` вашего контейнера. `Docker` должен установить соответствующие драгоценные камни при сборке, но также запустить миграции и заполнение базы данных для вашего приложения. Дочерний `Dockerfile` должен запустить сервер `rails` (см. Пример ниже). Если вы не знаете, какие команды использовать, самое время взглянуть на документацию [Ruby on Rails](http://rubyonrails.org/).  

</br>

### VI.4 Упражнение 03: ... и полоски бекона ... и полоски бекона ...

---------------------------------------------------------------------
> | Exersize 01: ... и полоски бекона ... и полоски бекона ...      |
> |-----------------------------------------------------------------|
> | Каталог для сдачи: ex03/                                        |
> | Файлы для сдачи : Dockerfile                                    |
> | Допустимые функции: -                                           |
> | Примечания : нет данных                                         |
---------------------------------------------------------------------

`Docker` может быть полезен для тестирования приложения, которое все еще разрабатывается, не загрязняя ваши библиотеки. Вам нужно будет создать файл `Dockerfile`, который получит разрабатываемую версию [Gitlab - Community Edition](https://gitlab.com/gitlab-org/gitlab-ce), установит его со всеми зависимостями и необходимыми конфигурациями, и запускает приложение, все как оно строится. Контейнер будет считаться действительным, если вы можете получить доступ к веб-клиенту, создать пользователей и взаимодействовать через `GIT` с этим контейнером (`HTTPS` и `SSH`). Очевидно, вам не разрешено использовать официальный контейнер от `Gitlab`, было бы обидно ...  


</br>
</br>
</br>


# Глава VII.

## Бонусная часть


Теперь, когда вы понимаете все тонкости `Docker`, вы можете наслаждаться бонусами!  

Вы можете создать свою будущую рабочую среду, например:  

- Среда разработки для кодирования в `nodejs`, но с использованием пряжи, а не `npm`.  
- `PAMP` (!) С `docker-compose`, но с использованием `MariaDB`, а не `MySQL`  
- Воссоздать полный `MEAN`-стек  
- Специальные файлы `Dockerfiles` для ваших проектов `C`, `Ruby`, `Go`, `Ocaml`, `Rust` ...  
- И так далее.  


Имейте в виду, что вы еще ничего не видели о всей мощи `Docker`. Например, вы можете:  

- Попробуйте поместить конфигурацию `VPN` в свои контейнеры.  
- Попробуйте сгруппировать несколько машин в разных облачных сервисах с помощью `Docker Swarm`.  
- Начните создание базового образа, создайте свой собственный контейнер `debian` или `archlinux`.  
- Создайте контейнер для сервера вашей любимой игры, например `Minecraft` (?)  
- И так далее.  

Что бы вы ни решили сделать, мы ожидаем, что вы сохраните все, что имеет значение, в папке `02_bonus` вашего репозитория.  

Повеселись!!  


</br>
</br>
</br>


# Глава VIII.

## Сдача и экспертная оценка

Сдавайте свою работу, используя репозиторий `GiT`, как обычно. Во время оценки будет оцениваться только работа, которая находится в вашем репозитории.  


