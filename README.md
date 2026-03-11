# 🤖 Universal Posts Bot — Инструкция по запуску

## ШАГ 1 — Загрузи код на GitHub

1. Зайди на https://github.com и зарегистрируйся (если нет аккаунта)
2. Нажми зелёную кнопку **"New"** → создай репозиторий с именем `posts-bot`
3. Нажми **"uploading an existing file"**
4. Перетащи ВСЕ файлы из папки бота в браузер
5. Нажми **"Commit changes"**

---

## ШАГ 2 — Получи ключи GigaChat

1. Зайди на https://developers.sber.ru/portal/products/gigachat
2. Нажми **"Подключить"** → войди через Сбер ID
3. Создай проект → скопируй **Client ID** и **Client Secret**

---

## ШАГ 3 — Узнай свой Telegram ID

1. Напиши боту @userinfobot в Telegram
2. Он пришлёт твой ID (число) — сохрани его

---

## ШАГ 4 — Задеплой на Railway

1. Зайди на https://railway.app
2. Нажми **"Start a New Project"**
3. Выбери **"Deploy from GitHub repo"**
4. Авторизуйся через GitHub → выбери репозиторий `posts-bot`
5. Railway автоматически начнёт сборку

---

## ШАГ 5 — Добавь переменные окружения

В Railway открой свой проект → вкладка **"Variables"** → добавь:

| Переменная | Значение |
|---|---|
| `BOT_TOKEN` | Токен от @BotFather |
| `GIGACHAT_CLIENT_ID` | Client ID от GigaChat |
| `GIGACHAT_CLIENT_SECRET` | Client Secret от GigaChat |
| `ADMIN_CHAT_ID` | Твой Telegram ID (число) |
| `ADMIN_USERNAME` | Твой username без @ |

После добавления нажми **"Deploy"** — бот запустится!

---

## ШАГ 6 — Проверь

Напиши своему боту `/start` — он должен ответить приветствием.

---

## Если что-то не работает

- Проверь вкладку **"Logs"** в Railway — там будет ошибка
- Самые частые проблемы:
  - Неправильный `BOT_TOKEN` — перепроверь у @BotFather
  - Неправильные ключи GigaChat — проверь в личном кабинете Сбера

---

## Команды бота

| Команда | Что делает |
|---|---|
| `/start` | Начать диалог |
| `/balance` | Показать баланс |
| `/withdraw` | Вывести деньги |
| `/admin` | Статистика (только для тебя) |
| `/help` | Список команд |
