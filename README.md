# demoServlet

Для того что бы запустить это приложение, необходимо:

1. Сделать Fork данного проекта (приоритет) или клонировать репозиторий

```bash
git clone https://github.com/OKaluzny/demoServlet.git
```

2. Собрать это приложение с помощью maven 

```bash
mvn clean install
```
3. Скачать и установить WildFly. Запустить WildFly. Перейти в каталог /bin и вызвать standalone
   далее задеплоить приложение с помощью команды

```bash
mvn org.wildfly.plugins:wildfly-maven-plugin:2.0.2.Final:deploy
```
4. Скачать и установить клиент запросов Postman
   
5. Скачать и установить базу данных PostgreSQL
```bash
   -- Table: public.users

-- DROP TABLE public.users;

CREATE TABLE public.users
(
id integer NOT NULL DEFAULT nextval('users_id_seq'::regclass),
name character varying COLLATE pg_catalog."default",
email character varying COLLATE pg_catalog."default",
country character varying COLLATE pg_catalog."default",
CONSTRAINT users_pk PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE public.users
OWNER to postgres;
```