# Документація API

## GET /item/<string:name>

Отримати елемент за його ім'ям.

- **Параметри**: `name` (рядок) - ім'я елемента, який потрібно отримати.
- **Відповідь**:
  - 200 OK: якщо елемент знайдено, повертає об'єкт елемента.
  - 404 Not Found: якщо елемент не знайдено.

## POST /item/<string:name>

Додати новий елемент.

- **Параметри**: `name` (рядок) - ім'я нового елемента.
- **Тіло запиту**: JSON-об'єкт з полем `price` (число).
- **Відповідь**:
  - 201 Created: якщо елемент успішно додано, повертає об'єкт елемента.
  - 400 Bad Request: якщо відсутнє поле `price`.

## PUT /item/<string:name>

Оновити існуючий елемент.

- **Параметри**: `name` (рядок) - ім'я елемента, який потрібно оновити.
- **Тіло запиту**: JSON-об'єкт з полем `price` (число).
- **Відповідь**:
  - 200 OK: якщо елемент успішно оновлено, повертає об'єкт елемента.
  - 404 Not Found: якщо елемент не знайдено.

## DELETE /item/<string:name>

Видалити елемент за його ім'ям.

- **Параметри**: `name` (рядок) - ім'я елемента, який потрібно видалити.
- **Відповідь**:
  - 200 OK: якщо елемент успішно видалено, повертає повідомлення про успіх.
  - 404 Not Found: якщо елемент не знайдено.
