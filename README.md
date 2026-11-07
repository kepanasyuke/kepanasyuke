# Кристина Панасюк

**Сайт-портфолио:** [kepanasyuke.github.io/portfolio](https://kepanasyuke.github.io/portfolio/) — 19 проектов разом: скриншоты, видео, фильтры по стеку.

**Python-инженер.** Пишу код с 2021 года: данные, автоматизация, локальные AI-системы.
Разбираю задачу от «принесли на словах» до работающего сервиса с тестами и документацией.

**Простыми словами:** я собираю работающие сервисы, могу сделать под них интерфейс. Здесь — примеры под разные
задачи: бэкенд на Python и PHP, мобильное приложение, разбор данных, автоматизация. У каждого проекта есть README,
где написано, что он делает, и как его запустить.

<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="SQL" src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img alt="Linux" src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img alt="C" src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black">
  <img alt="Java" src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white">
  <img alt="PHP" src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white">
  <img alt="PowerShell" src="https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white">
</p>

---

## Главные проекты

### [Mirro](https://github.com/kepanasyuke/Mirro-) — локальная система ответов на вопросы

Полностью локальная система без внешних зависимостей: OpenAI-совместимый HTTP-API,
собственный поиск по знаниям и движок рассуждений.

- Двухуровневый **дисковый RAG-индекс на 4,8 млн записей** + in-memory индекс по 2,8 млн примеров
- **TF-IDF, BM25, TextRank и перцептрон написаны с нуля** — без numpy и сторонних ML-библиотек
- Знаниевый граф: понятия как узлы, связи как рёбра, ассоциативный вывод по цепочкам
- OpenAI-совместимые эндпоинты `/v1/chat/completions`, `/v1/feedback`, `/v1/self-learn`
- Набор тестов на `unittest`, реестр функций в `CODE_MAP.md`, правила линтера в `LINTER.md`

`Python` · `RAG` · `NLP` · `HTTP API` · `unittest`

### [Search Service](https://github.com/kepanasyuke/something-else/tree/main/search-service) — асинхронный полнотекстовый поиск

Проект из репозитория [`something-else`](https://github.com/kepanasyuke/something-else).
Документы живут в **SQLite**, поиск идёт через **Elasticsearch**, FastAPI связывает их и держит оба хранилища в согласованном состоянии.

- Асинхронная работа с базой и индексом (`aiosqlite`), анализатор `russian` в Elasticsearch
- Автозагрузка CSV при старте, пагинация, подсветка найденных слов, экспорт в **XLSX**
- REST API с OpenAPI (`/search`, `/documents/{id}`, `/health`) и веб-интерфейс
- **Docker + docker-compose**: весь стек поднимается одной командой, настройки в `.env`
- **87% покрытие тестами** (pytest + coverage), `make lint`, `format`, `audit`, `test-coverage`
- Правила кода: функции до 30–50 строк, одна точка выхода, без `break`/`continue`

`Python` · `FastAPI` · `Elasticsearch` · `SQLite` · `Docker` · `pytest`

### [bug_python](https://github.com/kepanasyuke/fumiklea/tree/main/bug_python) — ретро-игра про первый баг

Сентябрь 1947 года, Гарвард, вычислительная машина Mark II: в реле №70 находят моль — тот самый
«first actual case of bug being found». Игрок вынимает насекомое латунным пинцетом и переносит
его в журнал отчёта, после чего видит историческую запись.

- Симуляция ЭЛТ-монитора на **pygame**: скан-линии, фосфорное послесвечение, виньетка, глитчи
- Живая моль внутри реле, журнал 1947 года с эффектом печатной машинки
- Звуки реле, пинцета и старого принтера
- `Makefile` с `install-system`, `install-venv`, `install-x11`, `play`

`Python` · `pygame` · `история вычислений`

---

## Остальные репозитории и что внутри

### [something-else](https://github.com/kepanasyuke/something-else)
Несколько независимых проектов в одной папке:

- **search-service** — асинхронный поисковый сервис на FastAPI, Elasticsearch и SQLite (описан выше)
- **VillaOenningerSimulator** — симулятор виллы с разрушением объектов в **Unity на C#**: менеджер разрушения дома, продвинутая камера, разрезание мешей, звук
- **fluid-materials-app** — визуализация материалов на **GLSL**: жидкость, гелий, газ
- **mercury-app** — шейдер ртути на **GLSL**
- **my-stratu-app** — приложение на **React + Vite** со сборкой в `dist`

`C#` · `Unity` · `GLSL` · `React` · `FastAPI`

### [fumiklea](https://github.com/kepanasyuke/fumiklea)
Мой первый репозиторий — двенадцать проектов папками, на четырёх языках. Здесь я училась
работать с тестами, линтерами и `Makefile`, а не «кодом в один файл».

**Python**
- `anime_parser_python` — парсер сайта с тестами и `flake8`, разделение на `src` и `tests`
- `banking_fraud_analytics_with_dataset_phyton` — аналитика банковских транзакций на датасете, фрод-аналитика
- `bug_python` — игра про историю первого бага: Гарвард 1947 года, моль в реле Mark II (описана выше)
- `calc_app_python` — веб-калькулятор на шаблонах и статике
- `currency_converter_python` — конвертер валют
- `christina_python` — игра-прототип по мотивам романа Стивена Кинга "Кристина"

**Java**
- `library_api_java` — API библиотеки: предметные сущности и связи между ними
- `tic_tac_toe_java` — крестики-нолики
- `tuhs_linux_animation_java` — анимация в терминале

**C и JavaScript**
- `decimal_C` — работа с десятичными числами на C
- `cosmos_play_js` — сцена на JavaScript, автотесты через **Playwright**

`Python` · `Java` · `C` · `JavaScript` · `flake8` · `Playwright` · `Makefile`

### [sysadmin-portfolio](https://github.com/kepanasyuke/sysadmin-portfolio)
Инфраструктура как код и автоматизация: курс, рабочие скрипты, плейбуки. Материалы на русском и английском.

`Ansible` · `Docker` · `PowerShell` · `Linux` · `MIT License`

### [projects-for-kids](https://github.com/kepanasyuke/projects-for-kids)
Проекты для школьной практики: сборка в Crazy Machines, ASCII-графика, задания для учеников.

`HTML` · `педагогика`

### [pixel-admin](https://github.com/kepanasyuke/pixel-admin)
Пиксельный платформер-квест по программам системного администратора. Запуск через PowerShell-скрипты.

`HTML` · `JavaScript` · `PowerShell`

### [informatics-site](https://github.com/kepanasyuke/informatics-site)
Онлайн-курс информатики для 3–11 классов и подготовки к ЕГЭ: уроки, презентации, игры «Собери код».
Внутри — свой сервер на Python (`server.py`, папка `_server`), материалы по классам, `sitemap.xml`.

`Python` · `HTML` · `педагогика`

### [cio-loyalty](https://github.com/kepanasyuke/cio-loyalty) — сервис лояльности на Laravel
Приложение, в котором клиенты брендов копят баллы и меняют их на награды, а бренд управляет каталогом в админке.
REST API на Laravel 12, журнал баллов с идемпотентностью, оплата пакетов через ЮKassa, Redis-кеш, очереди и 17 тестов.

`PHP` · `Laravel` · `MySQL` · `Redis` · `PHPUnit` · `OpenAPI`

### [robot-dispatch](https://github.com/kepanasyuke/robot-dispatch) — диспетчеризация парка роботов
Несколько сервисов на Python, из которых складывается одна система: задачи, телеметрия, мост к ROS2, мониторинг
и интеграция с WMS. Потерянные задачи возвращаются в очередь по lease, события идут через transactional outbox и RabbitMQ.

`Python` · `FastAPI` · `RabbitMQ` · `PostgreSQL` · `ROS2` · `gRPC`

### [fieldpulse](https://github.com/kepanasyuke/fieldpulse) — мобильное приложение выездного инженера
Flutter-приложение: заказы приходят по WebSocket, работают офлайн, наряд закрывается камерой, геолокацией и биометрией.
В репозитории — таблица соответствия требованиям вакансии и разбор архитектуры.

`Flutter` · `Dart` · `Bloc` · `Hive` · `Firebase` · `WebSocket`

### [sql](https://github.com/kepanasyuke/sql) — десять инструментов для работы с данными
Понять, откуда взялась цифра в отчёте, сверить источник и приёмник, разобрать логи, сравнить два SQL по скорости,
посмотреть, нет ли в файле персональных данных. Каждый проект запускается одной командой без установки.

`Python` · `SQL` · `PostgreSQL` · `ETL` · `observability`

### [data-reliability-dq](https://github.com/kepanasyuke/data-reliability-dq) — контроль качества хранилища
Контур проверок для аналитического хранилища: 12 SQL-проверок раз в полчаса, журнал инцидентов с приоритетами P1–P3
и SLA, метрики в Prometheus. Отвечает на вопрос «можно ли доверять этой витрине» до того, как это заметит аналитик.

`Python` · `SQL` · `Greenplum` · `Airflow` · `Prometheus`

### [digital-habits-qa](https://github.com/kepanasyuke/digital-habits-qa) — автотесты сервиса привычек
Учебный проект под вакансию тестировщика: сценарии на Gherkin, проверки API, базы и событий Kafka, отчёты Allure
и запуск в Jenkins. Плюс релизный процесс: ветки, теги, чек-лист.

`Java` · `Cucumber` · `Rest Assured` · `PostgreSQL` · `Kafka` · `Allure`

### [structured-programming-labs](https://github.com/kepanasyuke/structured-programming-labs) — 24 проекта по структурному программированию
Восемь программ на PHP, восемь на C# и восемь на C++ по жёстким правилам: одна точка выхода, без `break`/`continue`,
микрофункции, явная передача данных. Правила проверяются скриптом.

`PHP` · `C#` · `C++` · `статический анализ`

---

## Чем занимаюсь

| Направление | Что делаю |
|---|---|
| **Данные** | SQL (джойны, агрегации, CTE), PostgreSQL, обработка и нормализация выгрузок на Python, контроль качества данных |
| **Бэкенд** | HTTP-сервисы на Python и FastAPI; сервисы на Laravel (PHP) с админками и интеграциями платежей; тесты, документация |
| **Мобильная разработка** | Flutter и Dart: offline-first, WebSocket, Firebase, сборка под iOS и Android |
| **AI-системы** | Локальные RAG-системы, поиск по знаниям, OpenAI-совместимые API, знаниевые графы |
| **Автоматизация** | Скрипты на Python и PowerShell, автоматическая отчётность, автотесты интерфейса |
| **Инфраструктура** | Docker, Ansible, развёртывание сервисов на Linux, Git |
| **Документация** | Техническая документация, по которой работает новый человек; ревью кода; наставничество |

## Образование

- НИУ ВШЭ — бизнес-информатика
- НИУ ВШЭ — прикладное искусство
- НГПУ — педагогическое образование

## Прикладное искусство

Второе высшее — НИУ ВШЭ, прикладное искусство. Оттуда привычка к композиции, цвету и постановке
кадра: те же навыки, что нужны в визуализации данных и интерфейсах. Несколько работ со съёмок.

<table>
  <tr>
    <td><img src="photos/photo-01.jpg" width="220" alt="Постановочный кадр 1"></td>
    <td><img src="photos/photo-02.jpg" width="220" alt="Постановочный кадр 2"></td>
    <td><img src="photos/photo-03.jpg" width="220" alt="Постановочный кадр 3"></td>
  </tr>
  <tr>
    <td><img src="photos/photo-04.jpg" width="220" alt="Постановочный кадр 4"></td>
    <td><img src="photos/photo-05.jpg" width="220" alt="Постановочный кадр 5"></td>
    <td><img src="photos/photo-06.jpg" width="220" alt="Постановочный кадр 6"></td>
  </tr>
  <tr>
    <td><img src="photos/photo-07.jpg" width="220" alt="Постановочный кадр 7"></td>
    <td><img src="photos/photo-08.jpg" width="220" alt="Постановочный кадр 8"></td>
    <td><img src="photos/photo-09.jpg" width="220" alt="Постановочный кадр 9"></td>
  </tr>
  <tr>
    <td><img src="photos/photo-10.jpg" width="220" alt="Постановочный кадр 10"></td>
    <td><img src="photos/photo-11.jpg" width="220" alt="Постановочный кадр 11"></td>
    <td><img src="photos/photo-12.jpg" width="220" alt="Постановочный кадр 12"></td>
  </tr>
</table>

## Связаться

Резюме: [cloud.mail.ru](https://cloud.mail.ru/public/ys9R/4Rk5TpzgL)

Открыта к предложениям: Python-разработка, аналитика и инженерия данных, автоматизация тестирования.
