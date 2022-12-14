# Домашнее задание к занятию "`10.3 Pacemaker`" - `Овчинников Дмитрий`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

`Опишите основные функции и назначение Pacemaker `

Pacemaker - это центр управления всем кластером высокой доступности, используемый для управления поведением состояния ресурсов всего кластера, а клиент настраивает, управляет и отслеживает рабочий статус всего кластера


Основные функции:

    *Отслеживайте и восстанавливайте сбои узлов и уровней обслуживания.*
    **Хранилище не имеет ничего общего, и нет необходимости в общем хранилище.*
    **Ресурсу нечего делать, любой ресурс, которым можно управлять с помощью скрипта, можно использовать как службу кластера.*
    *Поддержка функции узла STONITH для обеспечения целостности данных кластера и предотвращения разделения мозга кластера.*
    *Поддержка больших или малых кластеров.*
    *Поддерживает механизм кворума и кластеры, управляемые ресурсами.*
    *Поддерживается практически любая конфигурация с резервированием.*
    *Автоматически синхронизировать файлы конфигурации каждого узла.*
    *Вы можете установить ограничения, такие как порядок, размещение и запрет на размещение в кластере.*
    *Поддержка расширенных типов услуг, таких как:*
    Функция клонирования, то есть те службы, которые должны запускаться на нескольких узлах, могут быть реализованы с помощью функции клонирования, а функция клонирования запускает одну и ту же службу на нескольких узлах;
    Функция с несколькими состояниями, то есть те службы, которые должны запускаться в нескольких состояниях, могут быть реализованы с помощью нескольких состояний. Среди служб кластера высокой доступности многие службы будут работать с разными состояниями высокой доступности. Режим, например: активный / активный режим или активный / пассивный режим и т. Д., И эти службы могут переключаться между активным и резервным (пассивным).
    *Иметь унифицированный инструмент управления кластером со скриптами.*

---

### Задание 2

'Опишите основные функции и назначения Corosync'

Приведите ответ в свободной форме

Corosyns- это программный продукт, позволяющий реализовать кластер серверов. Его основное назначение — знать и передавать состояние всех участников кластера.

В основе работы заложены следующие функции:

    *Отслеживание состояния приложений.*
    *Оповещение приложений о смене активной ноды кластера.*
    *Отправка одинаковых сообщений процессам на всех узлах кластера.*
    *Предоставление доступа к базе данных с конфигурацией и статистикой, а также отправка уведомлений о ее изменениях.*


---

### Задание 3

`Соберите модель, состоящую из двух виртуальных машин. Установите pacemaker, corosync, pcs. Настройте HA кластер.

Пришлите конфигурации сервисов для каждой ноды, конфигурационный файл corosync и бэкап конфигурации pacemaker при помощи команды pcs config backup filename.`

![node1_corosync](https://github.com/dmitri13/10_3/blob/main/img/coro_node1.png)
![node1_status](https://github.com/dmitri13/10_3/blob/main/img/node1_status.png)
![filename1](https://github.com/dmitri13/10_3/blob/main/img/filename1.tar.bz2)

![node2_corosync](https://github.com/dmitri13/10_3/blob/main/img/coro_node2.png)
![node2_status](https://github.com/dmitri13/10_3/blob/main/img/node2_status.png)
![filename2](https://github.com/dmitri13/10_3/blob/main/img/filename2.tar.bz2)

### Задание 4

'Установите и настройте DRBD сервис для настроенного кластера.`

Пришлите конфигурацию DRBD сервиса - .res ресурсов для каждой ноды.

---

