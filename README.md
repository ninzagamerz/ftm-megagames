
### `README.md`

```markdown
# FTM MegaGames Telegram Bot

Welcome to the **FTM MegaGames Telegram Bot**, a high-tech and advanced solution for interactive gaming directly within Telegram! This bot provides a range of engaging games, including Tic Tac Toe, Tetris, and Rock Paper Scissors.

## Features

- **Games**: Play Tic Tac Toe, Tetris, Rock Paper Scissors, and more!
- **Subscription Management**: Check and manage your subscription plans.
- **YouTube Downloader**: Download videos from YouTube.
- **Additional Commands**: `/about`, `/id`, `/myplan`, `/plans`, and more.
## Technology

- Python 3.11: The bot is built using Python for robustness and performance.
- Telegram API: Seamlessly integrated with Telegram for a smooth user experience.
- Docker: Containerized for easy deployment and scaling.
- Railway: Deployed on Railway for reliable and scalable hosting.
```
## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ninzagamerz/ftm-megagames
   cd ftm-megagames-bot
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables**:
   - Create a `.env` file in the root directory with your Telegram bot token:
     plaintext
     TELEGRAM_API_TOKEN=your-telegram-bot-token
     

4. **Run the Bot**:
   ```bash
   python megabot.py
   ```

5. **Deploy with Docker** (optional):
   ```bash
   docker build -t ftm-megagames-bot .
   docker run -e TELEGRAM_API_TOKEN=your-telegram-bot-token ftm-megagames-bot
   ```

## Deployment

**Before deploying, please fork this repository and give it a star to support the project.**

### Deploy to Railway
1. Sign up or log in to [Railway](https://railway.app/).
2. Create a new project and connect your GitHub repository.
3. Configure environment variables in the Railway dashboard.
4. Railway will automatically build and deploy your application.
[![Deploy](https://img.shields.io/badge/Deploy%20to%20Railway-blue)](https://railway.app/template/https://github.com/ninzagamerz/ftm-megagames)


### Deploy to Koyeb
1. Sign up or log in to [Koyeb](https://www.koyeb.com/).
2. Create a new service and link your GitHub repository.
3. Configure the deployment settings and environment variables.
4. Koyeb will handle the build and deployment process.
[![Deploy](https://img.shields.io/badge/Deploy%20to%20Koyeb-blue)](https://koyeb.com/deploy?repo=https://github.com/ninzagamerz/ftm-megagames)

### Deploy to Heroku
1. Sign up or log in to [Heroku](https://www.heroku.com/).
2. Create a new app and link your GitHub repository.
3. Configure environment variables in the Heroku dashboard.
4. Heroku will automatically build and deploy your application.
[![Deploy](https://img.shields.io/badge/Deploy%20to%20Heroku-blue)](https://heroku.com/deploy?template=https://github.com/ninzagamerz/ftm-megagames)


### Deploy to Render
1. Sign up or log in to [Render](https://render.com/).
2. Create a new web service and connect your GitHub repository.
3. Configure environment variables in the Render dashboard.
4. Render will automatically build and deploy your application.
[![Deploy](https://img.shields.io/badge/Deploy%20to%20Render-blue)](https://render.com/deploy?repo=https://github.com/ninzagamerz/ftm-megagames)

### Deploy to Netlify
1. Sign up or log in to [Netlify](https://www.netlify.com/).
2. Create a new site from Git and link your repository.
3. Configure build settings and environment variables.
4. Netlify will build and deploy your site automatically.
[![Deploy](https://img.shields.io/badge/Deploy%20to%20Netlify-blue)](https://app.netlify.com/start/deploy?repository=https://github.com/ninzagamerz/ftm-megagames)

### Deploy to VPS
1. **Prepare the VPS**:
   - Install Docker on your VPS.
2. **Upload Files**:
   - Transfer your project files to the VPS.
3. **Build and Run Docker Container**:
   ```bash
   docker build -t ftm-megagames-bot .
   docker run -e TELEGRAM_API_TOKEN=your-telegram-bot-token ftm-megagames-bot
   ```
### Bot Commands

| Command      | Description                                              |
|--------------|----------------------------------------------------------|
| `/start`     | Starts the bot and provides a welcome message.            |
| `/help`      | Provides help and instructions on how to use the bot.     |
| `/ftmgame1`  | Play **Tic Tac Toe** directly within Telegram.            |
| `/ftmgame2`  | Play **Tetris** directly within Telegram.                 |
| `/ftmgame3`  | Play **Rock Paper Scissors** directly within Telegram.    |
| `/ftmcast`   | Broadcasts a message to all users who have started the bot (Admin only). |
| `/ftmmegagame` | Access the **MegaGames Web Blog** featuring over 100+ games. |

## Some Additional Commands 
- `/add_premium <user_id> <plan>` - Add a user to a premium plan (Admin only).
- `/remove_premium <user_id>` - Remove a user from premium status (Admin only).
- `/premium_status` - Check your premium status.
- `/myplan` - Check your current plan.
- `/plans` - Display available plans.
- `/about` - Get information about the bot.
- `/id` - Get your Telegram ID.
- `/youtube <url>` - Download a YouTube video from the provided URL.
---

## Environment Variables

The bot uses the following environment variables to function properly. These variables can be set in a `.env` file or directly in your server environment.

### Required Variables:
1. **TOKEN**:  
   Your Telegram bot token. You can get this from the BotFather on Telegram.  
   Example:  
   ```
   TOKEN=123456:ABCDEF
   ```

2. **OWNER_ID**:  
   The Telegram ID of the bot's owner. This is the person with full control of the bot.  
   Example:  
   ```
   OWNER_ID=123456789
   ```

3. **LOG_CHANNEL**:  
   The ID of the Telegram channel where logs will be sent. This is useful for tracking bot events and errors.  
   Example:  
   ```
   LOG_CHANNEL=-1001234567890
   ```

### Optional Variables:
1. **ADMINS**:  
   A list of Telegram IDs for additional bot administrators who can use admin-level commands.  
   Example:  
   ```
   ADMINS=[987654321, 123456789]
   ```

2. **premium_users**:  
   A dictionary for premium users. This will automatically be populated when users subscribe to premium plans.

### Subscription Plans (Defined in Code):
The following plans are available for users:
- **Free Plan**: Basic access to the bot features.
- **Basic Plan**: Additional features and priority support.
- **Premium Plan**: Full access to all bot features and exclusive content.

For any inquiries, join us on [Telegram Support](https://t.me/ftmbotzsupport) or email at funtoonsmultimedia@gmail.com.

### How to Use the Commands:
1. **Start the bot**: Type `/start` to initiate.
2. **Get help**: If you're unsure of any functionality, type `/help`.
3. **Play games**: Use the specific game commands to play:
   - `/ftmgame1` for Tic Tac Toe.
   - `/ftmgame2` for Tetris.
   - `/ftmgame3` for Rock Paper Scissors.
4. **Broadcast**: The `/ftmcast` command is restricted to admins and can be used to send a message to all users.
5. **Access the MegaGames Web Blog**: Use `/ftmmegagame` to access the games blog directly from the bot.

## Contact Us

For any inquiries or support, join us on Telegram [@ftmbotzsupport](https://t.me/ftmbotzsupport) or email us at funtoonsmultimedia@gmail.com.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```
