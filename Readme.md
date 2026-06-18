# MiniPortfolio

MiniPortfolio is a Django application for creating and viewing user portfolios, with integration with a Telegram bot.

##  Features
- User registration, login and logout
- Adding your own projects (title, description, image, link)
- Viewing project cards with Bootstrap styling
- Bootstrap-style pagination
- Requests to delete projects
- Integration with the Telegram bot (@mini_portfolio_django_bot):
  - The author receives a notification when a project is created
  - Administrators receive notifications about deletion requests
  - Connection via the `/start` command in the bot


##  Структура
```
mini_portfolio/
├── mini_portfolio/        # головні налаштування Django
├── portfolio/             # додаток із моделями, views, шаблонами
├── telegram_bot/          # логіка Telegram‑бота
├── requirements.txt       # залежності
└── README.md              # документація
```

##  Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mini_portfolio.git
   cd mini_portfolio
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows
   ```

3. Define the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Carry out the migrations:
   ```bash
   python manage.py migrate
   ```

5. Start the server:
   ```bash
   python manage.py runserver
   ```

## Telegram bot
1. Create a bot via [BotFather](https://t.me/BotFather) and obtain a token.  
2. Save the token to the `telegram_bot/telegram_config.py` file:
   ```python
   TELEGRAM_BOT_TOKEN = "your_bot_token_here"
   APP_BASE_URL = "http://127.0.0.1:8000"
   ```
3. Start the bot:
   ```bash
   python telegram_bot/bot.py
   ```
4. Users connect via the `/start` command in @mini_portfolio_django_bot.

## Author
Oleksandr Zabolotnyi

https://github.com/Oleksandr-Zabo