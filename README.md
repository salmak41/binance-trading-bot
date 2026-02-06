# Binance Futures Testnet Trading Bot

A simplified Python-based trading bot that places **Market** and **Limit** orders on the **Binance Futures Testnet (USDT-M)** using a clean, modular, and production-ready project structure.

This project was built as part of a Python Developer application task and demonstrates:

- Structured and reusable code
- CLI-based user interaction
- Proper validation and error handling
- File-based logging of API activity
- Real order execution on Binance Futures **Testnet**

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

### 2. Create virtual environment (recommended)

```bash
python -m venv venv
```

Activate:

**Windows**
```bash
venv\Scripts\activate
```

**Mac/Linux**
```bash
source venv/bin/activate
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure Binance Testnet API Keys

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

## 🛠 Technologies Used

- Python 3.x
- python-binance
- argparse
- logging

---

## 📧 Submission Contents

This repository contains:

- Complete source code
- README with setup & usage
- requirements.txt
- Generated log files
