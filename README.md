# kottans-frontend
# Конспект stage0
1. [Git & GitHub](#git)
2. [Linux CLI, and HTTP](#linux-cli-and-http)
  2.1 [Linux CLI](#linux-cli)
  2.2 [HTTP](#http)

----

## GIT

**GIT** - специальная программа, позволяющая контролировать изменения файлов.

#### Основные возможности:

* Возврат к любой версии кода из прошлого
* Просмотр истории изменений и восстановление любых данных
* Совместная работа разработчиков без боязни потерять данные или затереть чужую работу

> Git в современном мире стал универсальным инструментом, с которого начинается практически любой проект в разработке. Вся существующая экосистема инструментов построена именно вокруг git (git интегрирован во все редакторы кода) и онлайн-сервисов, которые с ним интегрированы, например, https://github.com или https://gitlab.com. Как правило, код проектов хранится именно на этих сайтах, обеспечивая команду и совместным доступом, и копией на случай поломки компьютеров.

****

## Linux CLI, and HTTP

### Linux CLI

![Image alt text](./task_linux_cli/progress.gif)

***Интерфейс командной строки Линукс aka командная строка*** - универсальный интерфейс управления операционными системами на основе Linux, и некоторыми другими POSIX системами. Кстати, терминал и командный интерпретатор (CLI) - разные понятия. Терминал - программа которая эмулирует поведение *железного* терминала.
CLI - программа для управления ОС.

От реализации к реализации команды интерпретатора могут отличаться, но принцип одинаков для всех.

> *Освой один - освоишь все*.

Опишу самые популярные консольные команды:

* **pwd, cd, ls**. Текущая директория, смена директории и список файлов - навигация по файловой системе.

* **mkdir, touch**. Создание директории и создание файла(сама по себе команда **touch** меняет дату последнего изменения файла, побочный эффект этой команды - создание файла. Одна из тех команд, которые используются ради своего побочного действия, а не основного).

* **cat**. Быстрый способ посмотреть содержимое файла. Если передать второй аргумент, cat конкатенирует содержимое этих файлов.

* **grep**. Поиск по файлу или файлам определенного типа. Позволяет *гуглить* по файловой системе. Удобно.

etc. ***Тысячи их.***

### HTTP

***HHTP*** протокол передачи гипертекста. Один из столпов всея **web**. Обмен сообщениями с сервером построен по схеме **запрос-ответ**. Клиент начинает соединение отправляя сообщение запроса HTTP, сервер отвечает сообщением ответа HTTP. Текущая версия HTTP 1.1, имеет преимущества перед HTTP 1.0. Ждем HTTP 2.0.

####Методы запроса:

* **GET:** для получения существующего ресурса.  В URL-адресе содержится вся необходимая информация для определения местонахождения и возвращения ресурса сервером.
* **HEAD:** подобен GET, однако не передается тело сообщения. Он используется для получения заголовков определенного ресурса с сервера, обычно чтобы проверить при помощи временной отметки, не изменился ли ресурс.
* **POST** для создания нового ресурса. Запросы по методу POST обычно содержат данные для создания нового ресурса.
* **PUT:** для обновления существующего ресурса. В содержимом могут находиться обновленные данные для ресурса.
* **DELETE:** для удаления существующего ресурса.

####Коды состояния:

* **200 OK** запрос успешно обработан, все ок.
* **301** объект перемещен на новый url(указывается)
* **400 Bad request** обнаружена ошибка
* **404 Not Found**  объект не найден.

####Заголовки

> Заголовки должны быть отделены пустой строкой. Две пустых строки - конец сообщения.

Заголовки содержат информацию о куках, коде ответа, длине тела ответа/запроса и тд.

****