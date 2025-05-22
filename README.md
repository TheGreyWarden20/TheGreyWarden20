# Trading Bot UI

A web-based user interface for managing and monitoring automated cryptocurrency trading strategies on Binance. Built with Python, FastAPI, and modern web technologies.

![Trading Bot UI Dashboard](https://placeholder-for-screenshot.com/dashboard.png)

## Overview

Trading Bot UI provides a user-friendly interface for the Binance Trading Bot, allowing you to:

- Monitor your trading bot's activities in real-time
- View account balances and active positions
- Start and stop automated trading
- Configure trading parameters and risk settings
- Visualize price charts with technical indicators
- Track performance metrics and trading history

The application extends the existing trading bot functionality with a modern web interface, making it easier to monitor and control your trading strategies without having to use the command line.

## Installation

### Prerequisites

- Python 3.7 or higher
- Binance account with API keys
- Internet connection for accessing Binance API

### Quick Installation

1. Clone the repository:

   ```
   git clone t
   ```

2. Run the start script, which will check for dependencies and install them if needed:

   ```https://github.com/yourusername/trading_bot.git
   cd trading_bo
   python start.py
   ```

### Manual Installation

If you prefer to install dependencies manually:

1. Clone the repository:

   ```
   git clone https://github.com/yourusername/trading_bot.git
   cd trading_bot
   ```

2. Install required packages:

   ```
   pip install -r requirements.txt
   ```

3. Start the application:

   ```
   python start.py
   ```

## Configuration

### Binance API Keys

1. Create a Binance account if you don't have one
2. Generate API keys with trading permissions:
   - For testing, use [Binance Testnet](https://testnet.binance.vision/)
   - For live trading, use [Binance](https://www.binance.com/en/my/settings/api-management)
3. Add your API keys to `api_keys.json`:

   ```json
   {
     "testnet": {
       "api_key": "your_testnet_api_key",
       "api_secret": "your_testnet_api_secret"
     },
     "live": {
       "api_key": "your_live_api_key",
       "api_secret": "your_live_api_secret"
     }
   }
   ```

### Application Settings

You can configure the application settings by:

1. Creating a `.env` file in the root directory with:

   ```
   JWT_SECRET_KEY=your-secure-secret-key
   DEBUG=true
   HOST=0.0.0.0
   PORT=8000
   ```

2. Modifying the trading parameters in the web interface under Settings

## Usage

### Starting the Application

Run the start script:

```
python start.py
```

Access the web interface at `http://localhost:8000`

### Command Line Options

The start script supports several command line options:

- `--host HOST`: Specify the host to bind to (default: 0.0.0.0)
- `--port PORT`: Specify the port to bind to (default: 8000)
- `--no-reload`: Disable auto-reload for development
- `--skip-checks`: Skip dependency and API checks

Example:

```
python start.py --port 5000 --no-reload
```

### Default Login

When you first launch the application, you can log in with:

- Username: `admin`
- Password: `adminpassword`

**Important**: Change the default password immediately after your first login!

## Features

### Dashboard

- Real-time account balance display
- Active trading positions monitoring
- Performance metrics visualization
- Price charts with technical indicators

### Bot Control

- Start/stop trading bot
- Monitor bot status
- View trading signals in real-time

### Trading Configuration

- Configure trading pairs
- Set risk parameters (allocation, stop-loss, take-profit)
- Adjust strategy parameters

### Security

- JWT-based authentication
- Secure API key storage
- User session management

## Security Notes

⚠️ **Important Security Considerations** ⚠️

1. **API Keys**: Never share your Binance API keys. The application stores them in `api_keys.json`.

2. **Testnet Mode**: Always start with Testnet mode to ensure your strategy works as expected before risking real funds.

3. **Default Password**: Change the default admin password immediately after installation.

4. **Production Deployment**: When deploying to production:
   - Use HTTPS for all connections
   - Change the JWT_SECRET_KEY to a strong random value
   - Consider implementing additional security measures like IP restrictions
   - Host behind a reverse proxy like Nginx with proper security headers

5. **Risk Management**: Start with small trade sizes and conservative risk settings. No trading strategy is 100% reliable.

## Development

### Project Structure

```
trading_bot/
├── app/                    # Web application code
│   ├── static/             # Static assets (CSS, JS)
│   ├── templates/          # HTML templates
│   ├── __init__.py
│   ├── main.py             # FastAPI application
│   ├── auth.py             # Authentication
│   ├── config.py           # App configuration
│   └── dependencies.py     # FastAPI dependencies
├── logs/                   # Log files
├── bot.py                  # Trading bot implementation
├── config.py               # Trading configuration
├── start.py                # Starter script
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

### Running in Development Mode

For development with auto-reload:

```
python start.py
```

### Adding New Features

1. **Backend**: Add new endpoints in `app/main.py`
2. **Frontend**:
   - Add HTML templates in `app/templates/`
   - Add static assets in `app/static/`
3. **Bot Functionality**: Extend `bot.py` with new trading capabilities

## License:Ronald DC.Latorilla

0211544(MIT LICENSE)

## Disclaimer

This software is for educational purposes only. Use at your own risk. The developers are not responsible for any financial losses incurred from using this trading bot.

**Cryptocurrency trading involves significant risk. Never invest money you cannot afford to lose.**
