# 📚 Flask User Management App

Это простое веб-приложение на Flask для управления пользователями с использованием базы данных SQLite.

## 🚀 Установка

1. Клонируйте репозиторий и перейдите в папку проекта:
   ```bash
   git clone https://github.com/your-repo/flask-user-management-app.git
   cd flask-user-management-app
   ```

2. Установите зависимости:
   ```bash
   pip install Flask Flask-SQLAlchemy passlib
   ```

3. Запустите приложение:
   ```bash
   python app.py
   ```

## 💡 Использование

### 🔐 Регистрация пользователя

Отправьте POST запрос на `/register` с JSON телом:

```json
{
  "username": "example_user",
  "password": "password123"
}
```

### 🔑 Аутентификация пользователя

Отправьте POST запрос на `/login` с JSON телом:

```json
{
  "username": "example_user",
  "password": "password123"
}
```

### 📜 Получение списка пользователей

Отправьте GET запрос на `/users`.

### ➕ Добавление нового пользователя

Отправьте POST запрос на `/users` с JSON телом, аналогичным регистрации.

### ✏️ Обновление информации о пользователе

Отправьте PUT запрос на `/users/{user_id}` с JSON телом:

```json
{
  "username": "new_username",
  "password": "new_password"
}
```

### 🗑️ Удаление пользователя

Отправьте DELETE запрос на `/users/{user_id}`.

## 🌐 Маршруты

- `/register` - Регистрация нового пользователя.
- `/login` - Аутентификация пользователя.
- `/users` - Получение списка всех пользователей и добавление новых.
- `/users/{user_id}` - Обновление и удаление пользователя по его ID.

## 🔒 Защита приложения

Приложение защищено от SQL-инъекций с использованием SQLAlchemy ORM и от хэширования паролей с помощью библиотеки passlib.

## ⚙️ Запуск

Запустите приложение командой:

```bash
python app.py
```

Приложение будет доступно по адресу `http://localhost:5000`.

## 📦 Зависимости

- Flask
- Flask-SQLAlchemy
- passlib

---

👨‍💻 Разработано с ❤️ разработчиком.
