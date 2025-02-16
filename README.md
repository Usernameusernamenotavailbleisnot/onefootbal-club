# OneFootball Club BOT

An automation bot for managing multiple OFC accounts with proxy support and 25-hour cycle automation.

## Features

- Multi-wallet management
- Proxy support (required)
- 25-hour auto-cycle timer
- Comprehensive task automation:
  - Daily check-ins
  - Twitter interactions
  - Farcaster tasks
  - Quiz completions
  - External link visits
  - Referral tasks

## Requirements

- Node.js v16 or higher
- Proxies (one per wallet)
- Private keys for wallets

## Installation

1. Clone the repository or download the code
2. Install dependencies:
```bash
npm install axios ethers@5.7.2 https-proxy-agent winston winston-daily-rotate-file
```

## Configuration

### Private Keys (pk.txt)
Create a file named `pk.txt` and add your wallet private keys:
```
privatekey1
privatekey2
privatekey3
```

### Proxies (proxy.txt)
Create a file named `proxy.txt` and add your proxies in this format:
```
ip:port:username:password
ip:port:username:password
ip:port:username:password
```

Note: Number of proxies should match number of private keys.

## Usage

Start the bot:
```bash
node index.js
```

The bot will:
1. Load configurations
2. Run tasks for each wallet
3. Wait 25 hours
4. Repeat automatically

## File Structure
```
├── index.js
├── pk.txt
├── proxy.txt
└── logs/
    ├── error-YYYY-MM-DD.log
    └── combined-YYYY-MM-DD.log
```

## Logs

The bot creates two types of log files:
- `error-YYYY-MM-DD.log`: Error logs only
- `combined-YYYY-MM-DD.log`: All activity logs

Logs are automatically rotated daily.

## Notice

- Always use proxies to prevent IP bans
- Ensure reliable internet connection
- Keep your private keys secure
- Do not share your configuration files

## Disclaimer

This bot is for educational purposes only. Use at your own risk.
