# Binance Futures Testnet Trading Bot

A Python-based CLI trading bot that places **Market** and **Limit** orders on the **Binance Futures Testnet (USDT-M)** with proper structure, logging, and error handling.

---

## Objective

Build a simplified but production-style trading bot that:

- Places MARKET and LIMIT orders  
- Supports BUY and SELL sides  
- Accepts validated CLI input  
- Logs API requests, responses, and errors  
- Provides clean modular code structure  

---

## Tech Stack

- Python 3.x  
- python-binance  
- argparse (CLI handling)  
- logging  

---

## 🚀 Features

- Place **MARKET** and **LIMIT** orders
- Supports **BUY** and **SELL**
- CLI input using arguments
- Clear terminal output:
  - Order summary
  - Order response details
  - Success / failure status
- Structured architecture:
  - Client layer
  - Order logic
  - Validators
  - Logging configuration
  - CLI entry point
- Logs API requests, responses, and errors to file

---

## 🏗 Project Structure

```
trading_bot/
│
├── bot/
│   ├── __init__.py
│   ├── client.py          # Binance client wrapper
│   ├── orders.py          # Order placement logic
│   ├── validators.py      # Input validation
│   ├── logging_config.py  # Logging setup
│
├── cli.py                 # CLI entry point
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone or download the project

```bash
git clone <your-repo-link>
cd trading_bot
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Configure Binance Testnet API Keys

1. Open Binance Futures Testnet  
   https://testnet.binancefuture.com

2. Generate **API Key** and **Secret Key**

3. Set them as environment variables:

**Windows**
```bash
set BINANCE_API_KEY=your_api_key
set BINANCE_API_SECRET=your_api_secret
```

**Mac/Linux**
```bash
export BINANCE_API_KEY=your_api_key
export BINANCE_API_SECRET=your_api_secret
```

---

## ▶️ How to Run

### Market Order Example

```bash
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

---

### Limit Order Example

```bash
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.001 --price 50000
```

---

## 🧾 Output Includes

- Order request summary
- Binance order response:
  - orderId
  - status
  - executedQty
  - avgPrice (if available)
- Success or error message

---

## 📂 Logs

All API activity is stored in log files, including:

- Requests
- Responses
- Errors

Example logs generated for:

- One **MARKET** order
- One **LIMIT** order

---

## ⚠️ Assumptions

- Uses **Binance Futures Testnet**, not real funds
- API keys must have **Futures trading enabled**
- Quantity and price must follow Binance symbol rules
- Internet connection required for API calls

---

## 📧 Submission Contents

This repository contains:

- Complete source code
- README with setup & usage
- requirements.txt
- Generated log files

