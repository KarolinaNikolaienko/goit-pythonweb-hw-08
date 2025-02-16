# Fullstack Python Web HW08

1. Встановити залежності
```bash
pip install -r requirements.txt
```

2. Запустити команду для контейнера і бази даних за замовчуванням
```bash
docker run --name contacts_app_db -p 5432:5432 -e POSTGRES_PASSWORD=python08 -d postgres
```

3. Створити нову базу даних contacts_app, наприклад за допомогою DBeaver


4. Запустити команду для ініціалізації alembic
```bash
alembic init -t async migrations
```
5. Виконати міграцію та зберегти зміни у бд
```bash
alembic revision --autogenerate -m 'Init'
alembic upgrade head
```
6. Запускаємо програму
```bash
python main.py
```