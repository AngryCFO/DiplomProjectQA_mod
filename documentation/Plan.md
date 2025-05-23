# План тестирования приложения «Мобильный хоспис»
**Содержание:**
1. [Описание приложения](Plan.md#1-описание-приложения)
2. [Данные для авторизации](Plan.md#2-данные-для-авторизации)
3. [Границы приложения](Plan.md#3-границы-приложения)
4. [Тестовая документация на проекте](Plan.md#4-тестовая-документация-на-проекте)
5. [Критерии начала и окончания тестирования](Plan.md#5-критерии-начала-и-окончания-тестирования)
6. [Виды тестирования](Plan.md#6-виды-тестирования)
7. [Техники тест-дизайна с обоснованием](Plan.md#7-техники-тест-дизайна-с-обоснованием)
8. [Сортировка тест-кейсов по степени автоматизации](Plan.md#8-сортировка-тест-кейсов-по-степени-автоматизации)
9. [Перечень необходимых специалистов для автоматизации](Plan.md#9-перечень-необходимых-специалистов-для-автоматизации)
10. [Перечень используемых инструментов с обоснованием выбора](Plan.md#10-перечень-используемых-инструментов-с-обоснованием-выбора)
11. [Окружение для тестирования](Plan.md#11-окружение-для-тестирования)
12. [Перечень и описание возможных рисков при автоматизации](Plan.md#12-перечень-и-описание-возможных-рисков-при-автоматизации)
13. [Интервальная оценка с учетом рисков в часах](Plan.md#13-интервальная-оценка-с-учетом-рисков-в-часах)
14. [План сдачи работ](Plan.md#14-план-сдачи-работ)

<br>

## 1. Описание приложения
- Приложение даёт функционал по работе с новостями хосписа и включает в себя:
    * информацию о новостях и функционал для работы с ними
    * тематические цитаты
    * информацию о приложении

<br>

## 2. Данные для авторизации
- **Login:** `login2`
- **Password:** `password2`

<br>

## 3. Границы приложения
### Authorization (Страница авторизации в приложении)
- Поле ввода **Login** (Логин).
- Поле ввода **Password** (Пароль).
- Кнопка **SIGN IN** - Аутентифицирует пользователя и предоставляет ему доступ к защищенным функциям после проверки на корректность введенных данных.

### App bar (Меню приложения)
#### `Гамбургер-меню`

- **Main** (Основной) - раздел с главными, опубликованными новостями от хосписа.
    * Гиперссылка **ALL NEWS** переводит в раздел News.
    * Заголовки опубликованных новостей.
    * Кнопка развертывания для управления отображением контента.

- **News** - раздел новостей, который включает в себя страницу с опубликованными новостями и страницу управления новостями.
    * Заголовки опубликованных новостей.
    * Кнопка сортировки от самой старой новости / от самой последней новости.
    * Кнопка **Filter News** используется для поиска новостей по категориям, по промежутку времени.
    * Кнопка с иконкой карандаша открывает стрницу управлениями новостями, редактирование, добавление, удаление новостей.
        * Кнопка сортировки от самой старой новости / от самой последней новости.
        * Кнопка **Filter News** используется для поиска новостей по категориям, по промежутку времени, статусу.
        * Кнопка с иконкой плюса, добавление новости.
        * Заголовки новостей.
        * Кнопка развертывания на каждой новости, для отображения новости.
        * Кнопка редактирования на каждой новости.
        * Кнопка удаления на каждой новости.

- **About** - раздел позволяет получить информацию о версии приложения, условия эксплуатации, политика конфиденциальности.

#### `Love is all` (Иконка бабочки)
* Заголовок и цитат.
* Кнопка развертывания на каждой цитате для отображения контента.
* Список цитат, каких-то высказываний.

#### `Личный кабинет` (Иконка пользователя)
* Кнопка **Log out** выход из учетной записи.

<br>

## 4. Тестовая документация на проекте
- [План](Plan.md#план-тестирования-приложения-мобильный-хоспис) по проверке и автоматизации приложения (`Plan.md`)

- [Чек-лист](Чек-лист_ДипломQA.xlsx) c отметками о пройденных и не пройденных тестах (`Check.xlsx`)

- [Тест-кейсы](Тест-кейсы_ДипломQA.xlsx) для проверки приложения (`Cases.xlsx`)

- [Баг-репорты](https://github.com/AngryCFO/DiplomProjectQA/issues) оформленные как (`Issues`)

- [allure-отчет](allure-results.zip) с результатами прогона авто тестов запакованный в zip-архив (`allure-results.zip`)

- [Отчет о тестировании](Result.md) со сравнением ручного и автоматизированного тестирования, затраченного времени, найденные проблемы (`Result.md`)

<br> 

## 5. Критерии начала и окончания тестирования
### Критерии начала тестирования
- **Наличие необходимых данных**
    * Есть доступ к необходимым входным данным, которые могут включать тестовые данные, учетные записи пользователей.
- **Готовность тестовой среды**
    * Установлено и запущено приложение на эмуляторе (мобильном устройстве).
    * Установлены все необходимые инструменты и зависимости.
- **Документация и спецификации**
    * Наличие четких и понятных тест-кейсов, которые помогут в оценке функциональности продукта.

### Критерии окончания тестирования
- **Покрытие тестами**
    * Все запланированные тест-кейсы были выполнены и покрыли все критические функции.
- **Отсутствие критических и серьезных багов**
    * В процессе тестирования не выявлено критических багов, которые могут препятствовать нормальной работе системы.
- **Ограничение по времени**
    * Ограничение по времени с оценкой воздействия оставшихся рисков на продукт.
- **Отчетность**
    * Подготовлены все необходимые отчеты о тестировании, включая баг-репорты и оценку качества.
- **Отзывы участников команды**
    * Заключительная оценка тестирования со стороны команды, которая включает в себя разработчиков, тестировщиков и других заинтересованных лиц.

<br>

## 6. Виды тестирования
- **Исследовательское тестирование:**
    * В отсутствие чётких требований может быть полезно провести исследовательское тестирование, чтобы лучше понять приложение и его поведение. Это позволит выявить любые неявные требования или ограничения.
- **Функциональное тестирование:**
    * Важно проверить, работают ли все функции (например, авторизация, создание и редактирование новостей, навигация между разделами и т.д.) так, как задумано. Это позволит выявить любые несоответствия между ожидаемыми и фактическими результатами.
- **Тестирование пользовательского интерфейса (UI Testing):**
    * Проверки связанные с удобством использования и отображением интерфейса (например, адаптация под разные размеры экранов, правильное отображение текста и элементов интерфейса). UI тестирование поможет убедиться, что интерфейс интуитивно понятен и доступен для пользователей.
- **Тестирование на удобство использования (Usability Testing):**
    * Этот вид тестирования важен для оценки общего взаимодействия пользователя с приложением. Проверяя удобство навигации и доступность функций, можно сделать выводы о том, насколько приложение соответствует потребностям пользователей и как они реагируют на его интерфейс.
- **Тестирование безопасности:**
    * Проверка на XSS и SQL инъекции требует тестирования на безопасность. Это поможет исключить потенциальные уязвимости в приложении и защитить его от злоумышленников.

<br> 

## 7. Техники тест-дизайна с обоснованием
- **Классические тест-сценарии (Test Case Design):**
    * Это основной подход для создания тестов на основе чек-листа. Каждый сценарий тестируется в соответствии с предопределёнными условиями, что позволяет структурировать процесс тестирования и облегчить анализ результатов.
- **Эквивалентное разбиение (Equivalence Partitioning):**
    * Техника помогает уменьшить количество тестов, разделяя возможные входные данные на эквивалентные классы. Например, для авторизации можно иметь несколько классов для корректных и некорректных вводов.
- **Граничные значения (Boundary Value Analysis):**
    * Тестирование методом граничных значений является важным подходом для выявления ошибок при работе с различными значениями данных, особенно когда речь идет о числовых диапазонах или других границах допустимых значений. Однако, если нет конкретных требований к тестированию, а также отсутствует ограничение на ввод данных, то проведение тестирования методом граничных значений может оказаться менее приоритетным.
- **Состояния и переходы (State Transition Testing):**
    * Это может быть применимо к модулям, связанным с изменением статусов (например, создание и редактирование новостей). Эта техника позволяет проверить все возможные состояния и переходы между ними, чтобы убедиться, что приложение реагирует правильно.
- **Тестирование на основе сценариев пользователя (User Story Testing):**
    * Это позволяет проверить функциональность приложения с точки зрения конечного пользователя, следуя его логике и ожиданиям. Можно использовать чек-лист как руководство для создания сценариев, которые отражают реальные действия пользователей.

<br>

## 8. Сортировка тест-кейсов по степени автоматизации
- **Ручное тестирование:**
    * Ввод не существующей категории в поле "Category" [`TK ID: 24`]
    * Отмена действий в поле выбора даты [`TK ID: 32`]
    * Ввод не существующей категории в поле "Category" при фильтрации новостей [`TK ID: 39`]
    * Фильтр новостей не заполняя категорию и диапазон дат [`TK ID: 42`]
    * Фильтр новостей с выключенными тумблерами [`TK ID: 45`]
    * Фильтровать новости от будующей даты до прошедшей даты [`TK ID: 47`]
    * Отмена действий в поле выбора даты [`TK ID: 48`]
    * Название не существующей категории в поле "Category" в форме создания новости [`TK ID: 50`]
    * Ввод начала текста названия существующей категории в поле "Category" [`TK ID: 51`]
    * Ввод данных в поле "Title" на латинице с использованием спецсимволов и цифр [`TK ID: 52`]
    * Отменить выбор даты публикации, кнопка "CANCEL" [`TK ID: 53`]
    * Отменить выбор времени публикации, кнопка "CANCEL" [`TK ID: 54`]
    * Ввод данных в поле "Description" на латинице с использованием спецсимволов и цифр [`TK ID: 55`]
    * Создание новости с пустой формой [`TK ID: 58`]
    * Сворачивание и разворачивание отдельных новостей [`TK ID: 60`]
    * Ввод начального текста названия категории в форме редактировании новости [`TK ID: 64`]
    * Изменение заголовка  при редактировании в поле "Title" [`TK ID: 65`]
    * Выбор следующего месяца и даты публикации редактируемой новости с последующей отменой [`TK ID: 66`]
    * Выбор времени публикации в окне "Set time" [`TK ID: 67`]
    * Изменение формата выбора времени публикации редактируемой новости, с последующей отменой [`TK ID: 68`]
    * Возвращение к предыдущему выбору формату выбора часов через кнопку "CANCEL" [`TK ID: 69`]
    * Изменение описания в поле "Description [`TK ID: 71`]
    * Отмена внесенных изменений при редактировании новости [`TK ID: 74`]
    * Актуальная информация о политике конфиденциальности приложения [`TK ID: 76`]
    * Актуальная информация об условии эксплуатации приложения [`TK ID: 78`]
    * Взаимодействие приложения с системной кнопкой "Назад" [`TK ID: 86`]
    * Взаимодействие приложения с системной кнопкой "Обзор" [`TK ID: 87`]

- **Автоматизированные тесты:**

    * Авторизация с данными зарегистрированного пользователя [`TK ID: 1`]
    * Авторизация с данными не зарегистрированного пользователя [`TK ID: 2`]
    * Авторизация с пустым полем "Login" [`TK ID: 3`]
    * Авторизация с пустым полем "Password" [`TK ID: 4`]
    * Авторизация пользователя с данными в верхнем регистре [`TK ID: 5`]
    * Авторизация с простой SQL инъекцией в поле "Login" [`TK ID: 6`]
    * Авторизация с простой SQL инъекцией в поле "Password" [`TK ID: 7`]
    * Авторизация с простой SQL инъекцией в поле "Login" и "Password" [`TK ID: 8`]
    * Авторизация с простой XSS инъекцией в поле "Login" [`TK ID: 9`]
    * Авторизация с простой XSS инъекцией в поле "Password" [`TK ID: 10`]
    * Авторизация с простой XSS инъекцией в поле "Login" и "Password" [`TK ID: 11`]
    * Навигация к странице "News" со страницы "Main" [`TK ID: 12`]
    * Навигация к странице "About" со страницы "Main" [`TK ID: 13`]
    * Навигация к странице с тематическими цитатами "Our Mission" со страницы "Main" [`TK ID: 14`]
    * Выход из учетной записи со страницы с "Main" [`TK ID: 15`]
    * Аккордеон выпадающего списка [`TK ID: 16`]
    * Перход по кнопке ссылке "ALL NEWS" на приветствующую страницу "News" [`TK ID: 17`]
    * Навигация к странице "Main" с приветствующей страницы "News" [`TK ID: 18`]
    * Навигация к странице "About" с приветствующей страницы "News" [`TK ID: 19`]
    * Навигация к странице с тематическими цитатами "Our Mission" с приветственной страницы "News" [`TK ID: 20`]
    * Выход из учетной записи с приветствующей страницы "News" [`TK ID: 21`]
    * Выбор каждой категории в поле "Category" при использовании фильтра [`TK ID: 23`]
    * Отмена применения фильтра новостей на приветствующей странице "News" [`TK ID: 26`]
    * Навигация к странице "Main" со страницы управления новостями [`TK ID: 33`]
    * Навигация к странице "About" со страницы управления новостями [`TK ID: 34`]
    * Навигация к странице с тематическими цитатами "Our Mission" со страницы управления новостями [`TK ID: 35`]
    * Выход из учетной записи со страницы управления новостями [`TK ID: 36`]
    * Сортировка новосте на странице управления новостями" [`TK ID: 37`]
    * Выбор каждой категории в списке "Category" при фильтрации новостей [`TK ID: 38`]
    * Фильтрация новостей по категории и промежутку даты [`TK ID: 40`]
    * Отмена применения фильтра новостей [`TK ID: 41`]
    * Поиск через фильт только не активных новостей [`TK ID: 43`]
    * Поиск через фильт только активных новостей [`TK ID: 44`]
    * Фильтр с незаполненны полем "Category" [`TK ID: 46`]
    * Выбор каждой категории в форме создания новости [`TK ID: 49`]
    * Создание новости с валидными данными [`TK ID: 56`]
    * Отмена создания новости [`TK ID: 57`]
    * Возвращение к заполнению формы создания новости после отмены [`TK ID: 59`]
    * Отмена удаления отдельной новости [`TK ID: 61`]
    * Удаление отдельной новости [`TK ID: 62`]
    * Выбор каждой категории в форме редактирования новости [`TK ID: 63`]
    * Изменение статуса публикации редактируемой новости [`TK ID: 70`]
    * Возвращение к редактированию новости [`TK ID: 72`]
    * Публикация редактируемой новости [`TK ID: 73`]
    * Должен открываться URL политики конфиденциальности при нажатии на кнопку "Privacy Policy" [`TK ID: 75`]
    * Должен открываться URL условия эксплуатации при нажатии на кнопку "Terms  of use" [`TK ID: 77`]
    * Кликабельность кнопки назад из раздела "About" [`TK ID: 79`]
    * Навигация к странице "Main" со страницы цитатами [`TK ID: 80`]
    * Навигация к странице "News" со страницы с цитатами [`TK ID: 81`]
    * Навигация к странице "About" со страницы с цитатами [`TK ID: 82`]
    * Выход из учетной записи со страницы с цитатами [`TK ID: 83`]
    * Отображение заголовков свернутых цитат [`TK ID: 84`]
    * Отображение развернутых описаний цитат [`TK ID: 85`]

<br>

## 9. Перечень необходимых специалистов для автоматизации
- **Инженер по автоматизации тестирования** – создание и поддержка автоматических тестов.

<br>

## 10. Перечень используемых инструментов с обоснованием выбора
- **`Android Studio`** - официальная интегрированная среда разработки основана на IntelliJ IDEA для создания приложений на платформе Android, которая предлагает множество инструментов и функций.
- **`Эмулятор Android API 29`** - соответствует Android 10 (Q).
- **`Espresso`** - фреймворк для автоматизированного тестирования пользовательского интерфейса мобильных приложений на платформе Android.
- **`Java JDK 11`** — версия языка программирования Java, которая пользуется широкой популярностью в индустрии для разработки Android-приложений. Для тестировщиков JDK 11 важно тем, что предоставляет обширную экосистему библиотек и фреймворков, которые облегчают процесс тестирования приложений и сказывается на быстродействии тестируемых приложений, а также упрощает их поддержку и масштабирование, что критично для тестирования в условиях изменяющихся требований и новых функциональных возможностей.
- **`JUnit 4`** — тестовый фреймворк для Java, предназначенный для упрощения процесса тестирования программного обеспечения. Он предоставляет инструменты и аннотации, которые позволяют легко писать и выполнять автоматизированные тесты.
- **`Record Espresso Test`** - инструмент, который автоматически записывает действия пользователя для создания тестов.
- **`Layout Inspector`** - мощный инструмент, который позволяет визуально просматривать и анализировать структуру пользовательского интерфейса приложения в реальном времени и помогает изучать, как различные элементы интерфейса (views) расположены и взаимодействуют друг с другом в иерархии представлений (View Hierarchy).
- **`UI Automator`** - фреймворк для автоматизации тестирования пользовательских интерфейсов на Android-устройствах. Он позволяет создавать автоматизированные тесты для приложений, взаимодействуя с их интерфейсом на разных уровнях. Полезен для проверки функциональности, производительности и пользовательского опыта приложения, а также для автоматизации рутинных задач.
- **`GitHub`** - веб-сервис, предоставляющий хостинг для проектов, использующих Git, и создан с целью улучшения совместной разработки и управления проектами.
- **`Allure`** – гибкий инструмент для составления отчетов о тестировании, который показывает понятное представление того, что было протестировано, в форме веб-отчета.

<br>

## 11. Окружение для тестирования
- **Компьютер для разработки**
    * **Модель:** MacBook Pro M1
    * **Процессор:** Apple M1
    * **Операционная система:** macOS версия Sequoia 15.1

- **Эмулятор**
    * **Имя эмулятора:** Pixel 7  API 29
    * **Размер экрана:** 6.31 дюйма
    * **Разрешение:** 1080 x 2400 пикселей
    * **Плотность пикселей:** 420 dpi
    * **Версия Android:** 10
    * **Архитектура:** arm64-v8a

- **Мобильное устройство**
    * **Модель:** Samsung Galaxy Note 9
    * **Объем памяти:** 128 ГБ
    * **Версия Android:** 10
    * **Версия One UI:** One UI 2
    * **Оперативная память:** 6 ГБ
    * **Процессор:** Qualcomm Snapdragon 845
    * **Разрешение экрана:** 2960 x 1440 пикселей (Quad HD+)
    * **Размер экрана:** 6.4 дюйма

- **Описание тестовой среды**
    * Для обеспечения стабильности и предсказуемости тестирования, приложение проверяется на следующих устройствах:
        * **Эмулятор Pixel 7  API 29:** используется для быстрой проверки функциональности на устройствах с характеристиками, близкими к распространенным моделям смартфонов.
        * **Физическое устройство (Samsung Galaxy Note 9):** тестирование на реальном устройстве имеет ключевое значение для оценки пользовательского опыта и производительности приложения. Samsung Galaxy Note 9 позволяет увидеть, как приложение будет работать на устройстве с несколькими характеристиками, включая высокое разрешение.

<br>

## 12. Перечень и описание возможных рисков при автоматизации

- **Отсутствие Требований к тестированию**
    * Описание:
        * Без наличия четких требований к тестированию тестировщики не смогут правильно спроектировать и реализовать автоматизированные тесты. Это приведет к отсутствию целостного подхода к проверке функционала и снижению качества тестирования.
    * Последствия:
        * Невозможность точного определения объема тестирования.
        * Пропуски критически важных проверок.
        * Неверный фокус на второстепенные аспекты.

- **Отсутствие Технического Задания (ТЗ)**
    * Описание:
        * Без четко формализованного технического задания (ТЗ) тестировщики не имеют ясного представления о том, какой функционал нужно тестировать и каких показателей ожидать. Это ведет к созданию неполноценных и некорректных тестовых сценариев.
    * Последствия:
        * Недостаточные или избыточные тесты.
        * Невозможность точно измерять соответствие выходных параметров ожидаемым.
        * Недооценка важности некоторых функциональных областей.

- **Сложности с Кросс-платформенным тестированием**
    * Описание:
        * Автоматизация тестирования мобильных приложений требует учета множества платформ и устройств. Различия в аппаратуре и ПО делают задачу сложной и трудоемкой.
    * Последствия:
        * Приложение может функционировать нормально на одной платформе, но иметь сбои на другой.
        * Неправильное распределение усилий на тестирование разных платформ.
        * Повышенная вероятность пропуска багов, связанных с особенностями конкретной платформы.

- **Отсутствие доступа к базе данных**
    * Описание:
        * Если тестировщики не имеют доступ к необходимой базе данных или данным для тестирования, это сильно ограничивает возможности тестирования.
    * Последствия:
        * Невозможно полноценно протестировать функции, зависящие от данных.
        * Отсутствие возможности провести нагрузочное тестирование с использованием больших объемов данных.
        * Баги, связанные с данными, остаются незамеченными.

- **Трудности с поддержкой и сопровождением**
    * Описание:
        * Поддержка и сопровождение автоматизированных тестов требуют постоянных усилий и ресурсов. Любое изменение в приложении может потребовать обновления тестов.
    * Последствия:
        * Постоянные затраты на поддержание тестов в актуальном состоянии.
        * Рост сложности управления большим количеством тестов.
        * Уменьшение полезности старых тестов из-за их устаревания.

- **Ограниченные ресурсы**
    * Описание:
        * Недостаток ресурсов (человеческих, временных, финансовых) может негативно сказаться на процессе автоматизации тестирования.
    * Последствия:
        * Недостаточно квалифицированные специалисты для создания и поддержания автоматизированных тестов.
        * Ограниченное количество тестов, покрывающих ключевые функции.
        * Снижение общей скорости разработки и тестирования.

<br>

## 13. Интервальная оценка с учетом рисков в часах
- **Общий интервал оценки** `[98, 196]` часов.

    *  **Изучение приложения** `[6, 12]`
    *  **Составление плана тестирования** `[3, 6]`
    *  **Написание чек-листа** `[4, 8]`
    *  **Написание тест-кейсов:** `[10, 20]`
    *  **Проведение ручного тестирования** `[8, 16]`
    *  **Согласование и утверждение** `[1, 2]`
    *  **Написание авто тестов** `[60, 120]`
    *  **Написание баг-репортов** `[3, 6]`
    *  **Составление отчета о тестировании** `[3, 6]`

<br>

## 14. План сдачи работ

Оптимистичный сценарий 4 выходных

- **1-й этап сдачи:** до `06.04.2025`
    * В него входит:
        * Изучение приложения
        * Составление плана тестирования
        * Написание чек-листа
        * Подготовка подробных тест-кейсов на основе чек-листа.
        * Проведение ручного тестирования

- **2-й этап сдачи:** до `20.04.2025`
    * В него входит:
        * Разработка авто тестов
        * Проведение тестирования
        * Составление баг репортов
        * Формирование отчетов
    