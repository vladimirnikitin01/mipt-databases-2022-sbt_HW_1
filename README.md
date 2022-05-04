# mipt-databases-2022-sbt_HW_4
## Отчет домашняя работа №4, Jackrabbit 

В данно домашей задаче нам надо разобраться с данной СУБД и подробно ответить на множество вопросов, которые помогут составить более подробное описание нашей СУБД. Давайте, начнем.

**a)История развития СУБД**

 хранилище содержимого с открытым исходным кодом для платформы Java. Проект Jackrabbit был начат 28 августа 2004 года (но первые идеи были еще в 2002), когда компания Day Software начала разработку реализации API хранилища содержимого для Java (JCR). Jackrabbit также был использован как пример реализации JSR-170 и JSR-283. Проект вышел из «инкубатора» Apache 15 марта 2006 года и сейчас является проектом верхнего уровня в Apache Software Foundation. Надо отметить, что примерно каждые 2 недели появляются новые выпуски, причем некоторые из них являются нестабильными или выпусками дополнительны функций, так что разработчики постоянно занимимаются расширением и улучшением нынешних версий. Последняя стабильная версия вышла 2 марта 2022 г.


[Загрузка и версии Apache Jackrabbit](https://jackrabbit.apache.org/jcr/downloads.html)

**b)Инструменты для взаимодействия с СУБД**

На официальном сайте написано следующее: разработчики используют различные инструменты для помощи в работе, такие как IntelliJ IDEA или Eclipse. Большинство инструментов не требуют указания атрибуции, но некоторые требуют (YourKit Java Profiler). Хотелось бы немного рассказать про каждую из выше перечисленных. [Eclipse](https://www.eclipse.org/) служит в первую очередь платформой для разработки расширений, чем он и завоевал популярность: любой разработчик может расширить Eclipse своими модулями. [IntelliJ IDEA](https://www.jetbrains.com/opensource/idea/) — интегрированная среда разработки программного обеспечения для многих языков программирования, в частности Java, JavaScript, Python, разработанная компанией JetBrains. [YourKit Java Profiler](https://www.yourkit.com/benefits/#:~:text=YourKit%20Java%20Profiler%20is%20the,simply%20unrivaled%20but%20absolutely%20unique.) — это ведущий инструмент профилирования на рынке Java, предоставляющий самые инновационные, мощные и интеллектуальные возможности анализа производительности.

**c)Какой database engine используется в вашей СУБД?**

Приложения контента взаимодействуют через API JSR-170 с реализацией репозитория контента. Существует множество приложений, доступных для репозиториев JSR-170, некоторые из них очень общие (например, сервер WebDAV), другие приложения могут быть очень специфичными и использовать репозиторий контента в качестве хранилища информации, используемой приложениями.Java-приложения могут использовать репозиторий содержимого JSR-170 в качестве замены чего угодно, от файлов свойств, XML-конфигурации, определенных частей функциональности реляционной базы данных до прямой файловой системы или управления большими двоичными объектами.

Репозиторий на основе контента — это иерархическое хранилище контента, в котором собраны структурированный и неструктурированный контент, полнотекстовый поиск, наблюдение за транзакциями управления версиями и многое другое.

![image](https://user-images.githubusercontent.com/58188954/166662155-21b750df-6b9a-4676-b70b-51b1542f27fc.png)

Также давайте более подробно рассмотрим [архитектуру](https://jackrabbit.apache.org/jcr/jackrabbit-architecture.html)

![image](https://user-images.githubusercontent.com/58188954/166662841-8c44eec7-0795-4637-bda4-2a8e0177129c.png)


