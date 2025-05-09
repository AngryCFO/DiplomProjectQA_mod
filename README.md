# Дипломный проект по профессии [«Инженер по тестированию»](https://github.com/netology-code/qamid-diplom/tree/main) - `Александра Бужор`

<br>

## Тестовая документация

- [План](https://github.com/AngryCFO/DiplomProjectQA/documentation/Plan.md) по проверке и автоматизации приложения (`documentation/Plan.md`).

- [Чек-лист](https://docs.google.com/spreadsheets/d/1fixkuUc1HL-9UGBTSnLohiU53TA2FEfQtqdYT4w-u2I/edit?usp=sharing) c отметками о пройденных и не пройденных тестах (`documentation/Check.xlsx`).

- [Тест-кейсы](https://docs.google.com/spreadsheets/d/1SZQpvwa5PksNxRopZcktfAXzVb4jnhh0Fl4UzhrBBLY/edit?usp=sharing) для проверки приложения (`documentation/Cases.xlsx`).

- [Баг-репорты](https://github.com/AngryCFO/DiplomProjectQA/issues) оформленные как (`Issues`).

- [allure-отчет](https://AngryCFO.github.io/DiplomProjectQA_mod/documentation/allure-report) с результатами прогона авто-тестов, а так же запакованный в zip-архив (`documentation/allure-results.zip`).

- [Отчет о тестировании](https://github.com/AngryCFO/DiplomProjectQA/documentation/Result.md) со сравнением ручного и автоматизированного тестирования, затраченного времени, найденные проблемы (`documentation/Result.md`).

<br>

-----

<br>

## Запуск авто-тестов и создание Allure-отчёта в Android Studio
### 1. Условия для запуска авто-тестов
- **Java JDK 11:** Убедитесь, что у вас установлена Java Development Kit версии 11.
- **Android Studio:** Убедитесь, что у вас установлена последняя версия Android Studio с настроенной файловой средой:
    * Добавлен путь до JAVA_HOME в переменные окружения.
    * Настроена переменная ANDROID_HOME, указан путь до SDK Android.
- **Эмулятор Android**: Убедитесь, что у вас установлен и настроен эмулятор Android с версией API 29.

### 2. Клонирование и настройка проекта
- Склонируйте репозиторий проекта: `git clone https://github.com/AngryCFO/DiplomProjectQA`
- Откройте проект в Android Studio.
- Подождите, пока завершится индексация и синхронизация проекта с Gradle.

### 3. Запуск авто-тестов
- В верхней части окна Android Studio, непосредственно над каталогом проекта, выберите вкладку «Project».
- Разверните структуру проекта и перейдите в директорию `app/src/androidTest/java/ru.iteco.fmhandroid.ui/test`.
- Правой кнопкой мыши кликните на папку `test` и выберите опцию «Run 'Tests in iteco.fmhandroid.ui'», чтобы запустить все тесты данного пакета.
- Для запуска отдельных тестов выберите нужный тестовый класс и повторите предыдущий шаг.
    * Начнется процесс сборки и запуска тестов.
    * Прогресс выполнения будет отображаться в окне «Run».

### 4. Формирование Allure-отчёта
- Установите [Allure](https://allurereport.org/docs/install/) на вашем ПК

### 5. Экспорт результатов тестов
- После завершения тестов откройте окно Device Explorer в Android Studio (Это можно сделать через поисковик 🔍).
- Перейдите в директорию `/data/data/ru.iteco.fmhandroid.ui/files/allure-results`.
- Щёлкните правой кнопкой мыши на папке `files` и выберите опцию Save As....
- Сохраните папку `allure-result` в корневую директорию вашего проекта.
    * Если вам нужно сохранить папку `allure-result` в какую-то подпапку внутри вашего проекта, сначала необходимо перейти в эту подпапку, а затем выполнить команду для запуска.

### 6. Генерация отчёта
- Перейдите в терминал и убедитесь, что находитесь в корневой директории проекта.
- Выполните необходимую вам команду:
```bash
   # для быстрого анализа результатов тестирования
   # запускает временный веб-сервер, который динамически генерирует и показывает отчет на основе JSON-данных:
   allure serve

   # для генерации HTML-отчёта:
   allure generate allure-results -o allure-report

   # открывает сгенерированный HTML-отчёт в браузере:
   allure open allure-report
```
- Теперь вы можете просматривать результаты тестов в удобном формате Allure-отчёта.

