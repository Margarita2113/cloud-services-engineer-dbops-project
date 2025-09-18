# dbops-project
## Описание проекта

В рамках проектной работы мы:

- проанализируем структуру таблиц базы данных интернет-магазина сосисочной;
- оптимизируем схему с помощью нормализации и индексов;
- разработаем Flyway-мigrations для последующей миграции в новую схему.

## Подготовительные работы

1. Убедитесь, что Docker и Docker Compose установлены на вашей машине.
Проверка Docker:
**docker --version**
Проверка Compose:
**docker compose version**
Если отсутсвует -установить. 
2. Запустите локальную PostgreSQL с использованием docker-compose из репозитория.
3. Установите клиент psql для подключения к БД:
**sudo apt-get install -y postgresql-client**
4. Подключитесь к запущенной БД:
**psql "host=<db host> port=5432 dbname=<db> user=<user>"**
5. Заполните базу данных сосисочной данными, запустив insert-data.sh.
6. Подключится к BD и изучить структуру таблиц.

## Команды, которые преадобились:

\dt;
SELECT * FROM имя_таблицы
\d имя_таблицы

## Создание новой БД store и пользовтеля

CREATE DATABASE store;
CREATE USER <пользователь> WITH PASSWORD <пароль>;
GRANT ALL privileges ON DATABASE store TO <пользователь>;
ALTER DATABASE store OWNER TO <пользователь>;

## GitHUB secrets

Создаём и задаём значения для: DB_HOST, DB_PORT, DB_NAME, DB_USER и DB_PASSWORD.




