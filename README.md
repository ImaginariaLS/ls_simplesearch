Simple Search and Auto Completer
================================

Поиск с простой релевантностью (на основе регулярных выражений в запросах к БД) по топикам (заголовок, текст),
комментам, пользователям (логин, имя, страна, город и поле "о себе"), описаниям блогов (заголовок, текст)
и расширенный поиск по тегам, автозаполнение (автокомплитер) по тегам, логинам для формы поиска.
Не требует установки других плагинов для своей работы. Альтернатива сфинксу.


Автор
=====

PSNet

Описание и возможности
======================

*Преимущества перед Сфинксом*

- ищет всегда самую свежую и актуальную информацию, в отличие от Сфинкса, который нужно синхронизировать раз на определенное время чтобы в поиск попали новые топики и комментарии.
- в результаты поиска не попадают топики или комментарии из закрытых блогов или черновиков в отличие от Сфинкса, у которого есть такая ошибка.
- плагин может производить поиск по данным профилей пользователей.
- плагин может производить поиск по описаниям блогов.
- плагин может производить расширенный поиск по тегам (см. ниже).
- Позволяет включить поддержку поиска по топикам, которые созданы другими плагинами и имеют свой тип блога (можно задавать список типов блогов).
- есть пользовательские словари.
- показ ссылок поиска в других ПС по сайту.
- добавлен OpenSearch.
- поиск дополнительно проводится в закрытых блогах, к которым у пользователя есть доступ.
- возможность поиска внутри блога.
- возможность поиска по тегу в блоге.
- позволяет подбирать теги набирая даже их часть.
- возможность поиска по избранному пользователя.

<b>Релевантность выдачи:</b>

Поиск использует выдачу на основе точного совпадения с искомым словом, а потом уже похожих слов и строит на основе этого выдачу, т.е. в выдачу сначала попадают объекты в которых найдено точное совпадение с запросом, потом - похожие. Плагин выполняет поиск по соответствию одного из слов запроса в тексте (ИЛИ).

Наибольший приоритет имеет точное совпадение поискового запроса в заголовке + тексте топика - если в обоих полях найдено точное совпадение - делаем вес релевантности самым большим, потом точный поиск осуществляется по заголовку топика, после - точное совпадение плагин ищет в тексте. Потом производится поиск на не точное совпадение снова в заголовке + тексте топика, потом в заголовке топика и затем в тексте. После этого идет сортировка по рейтингу, а после уже по времени публикации (на самом деле по ИД, но ИД отображает "дальность" публикации т.к. автоматически инкрементируется), самые старые объекты будут в конце поисковой выдачи.

Рассмотрим запрос на украинском языке "<i>їжа kiss</i>": плагин выведет первым топик в котором есть слово <i>kiss </i>с рейтингом <i>+2</i>, потом топик о еде ("<i>їжа</i>") с нулевым рейтингом и потом топик о ежиках ("<i>їжак</i>", "<i>їжаки</i>" и т.п.) тоже с нулевым рейтингом, причем результаты поиска будут определены по группам точное/не точное совпадение в заголовке/тексте.

В плагин включен автокомплитер по тегам для поиска, который раньше был выполнен в виде отдельного плагина.

<b>В плагин добавлена возможность поиска по людям:</b>
Поиск выполняется по логину, имени, стране, городу и поле "о себе". Релевантность при поиске пользователей не используется, на форме есть опция "<i>точный/не точный поиск</i>", которая задает алгоритм поиска.


Существует возможность задавать список типов блогов чтобы производить поиск по топикам от других плагинов (например, блоги с подразделами от aceblogextender, плагин Компании от gran'а).

Можно задать пользовательские словари: для исключения ненужных слов из поиска, для дополнения поискового запроса синонимами. Формат этих словарей полностью совместим с форматом Сфинкса.

Опция показа ссылок поиска в других ПС по сайту если ничего не найдено средствами встроенного поиска (Гугл, Яндекс и Бинг).

Есть OpenSearch - открытая технология, которая позволяет добавлять поиск по сайту как поисковый плагин для браузера.

<b>Добавлен поиск по описаниям и заголовкам блогов</b>

Если пользователь авторизирован, поиск дополнительно проводится в закрытых блогах, к которым у пользователя есть доступ.

<b>Добавлена возможность поиска внутри блога:</b>
В форме поиска можно выбрать блог, в котором нужно искать топики. Также на страницах блогов добавлена форма поиска по этому блогу.

<b>Добавлен расширенный поиск по тегам:</b>
Можно искать даже по части тега, например, середины (интегрирован плагин "Tags like full"), а также возможность поиска по тегу в блоге.

<b>Добавлена возможность поиска по избранному пользователя:</b>
Для топиков, комментариев и расширенного поиска топиков за тегом есть возможность указать поиск в избранном.

Плагин предлагает фасетный поиск по поисковому запросу + блогу или по всем + возможность поиска по избранному.

При выводе результаты поиска выводятся в порядке релевантности: сначала точные результаты, потом похожие. Каждая группа результатов подписана и визуально отделена (точное совпадение в заголовке + тексте, заголовке, тексте и в таком же порядке для неточного совпадения).

Поисковый запрос выделяется в тексте цветом.
Запросы оптимизированы, все результаты поиска кешируются.

<h4><b>В конфиге доступны параметры:</b></h4>

- Минимальная длина поискового запроса (всего)
- Максимальная длина поискового запроса (всего)
- Минимальная длина слова в запросе
- Максимальная длина слова в запросе
- Вырезать ли все теги из поискового запроса, иначе - обработать стандартным парсером ЛС
- Количество результатов поиска на страницу
- Включать ли автозаполнение (автокомплитер) по тегам для формы поиска
- Включить поиск по топикам
- Включить поиск по комментариям
- Включить поиск по людям
- Включить поиск по описаниям блогов
- Включить расширенный поиск по тегам (в блогах)

<i>Секция проверки запроса:</i>
- Символы, которые считаются валидными. Все остальные вырежет парсер. Для добавления других языков сюда нужно будет внести набор символов (регекспа)

<i>Секция выделения результатов поиска в тексте:</i>
- Граница слова, используется при подсветке результатов поиска (регекспа)
- Выделение искомого слова слева (html строка)
- Выделение искомого слова справа (html строка)

<i>Секция поиска по релевантности информации:</i>
- Точный поиск по умолчанию. Например, поиск по слову "Сон" - будет искать точное совпадение (регистр-независимое), иначе найдет "Сонату" и т.п.
- Разрешить НЕ точный поиск ДОПОЛНИТЕЛЬНО и ТОЛЬКО если включен точный поиск. Результаты будут выдаваться на основе релевантности найденной информации - сначала тексты, где найдено точное совпадение с искомым запросом, потом - тексты, где встречаются и похожие слова

<i>Секция сортировки результатов:</i>
- Как выводить топики
- Как выводить комментарии
- Как выводить людей
- Как выводить список блогов

<i>Секция задания списка разрешенных типов блогов:</i>
Позволяет включить поддержку поиска по топикам, которые созданы другими плагинами и имеют свой тип блога.

<i>Секция проверки словарей:</i>
Словари позволяют расширить морфологические возможности плагина. stopwords.txt нужен для исключения ненужных слов из поиска. wordforms.txt нужен для дополнения поискового запроса синонимами. Действие словарей такое же как и у Сфинкса и имеют такую же структуру.

<i>Секция поиска в других ПС:</i>
Можно показывать ссылки для поиска в других поисковых системах по этому же сайту если ничего не найдено средствами встроенного поиска.
