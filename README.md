# Frego x402 AI Shipping Agent

AI-powered shipping label service with crypto payments. Describe what you're shipping in natural language, pay with USDC, and get the best shipping rates instantly.

## 🚀 Quick Start

### Web UI (Easiest)

1. Start the server:
```bash
npm install
npm run dev:server
```

2. Open browser: `http://localhost:3000`

3. Connect wallet, describe your item, and get quotes!

### CLI

```bash
npm run dev:cli
```

### API Integration

For programmatic access, see **[API_DOCUMENTATION.md](./API_DOCUMENTATION.md)**

---

## ✨ Features

- 🤖 **AI-Powered Analysis** - Describe items in natural language
- 💰 **x402 Crypto Payments** - Pay $0.001 USDC per request
- 📦 **Real Shipping Rates** - USPS, UPS, FedEx, DHL via Shippo
- 🎯 **Smart Recommendations** - AI picks the best option for your item
- 🏷️ **Instant Labels** - Get trackable shipping labels immediately
- 🌐 **Web UI + CLI + API** - Use however you prefer

---

## 🛠️ Setup

1. **Clone and install:**
```bash
git clone <repo-url>
npm install
```

2. **Configure environment:**
```bash
cp .env.example .env
```

Edit `.env` with:
- `PAYMENT_ADDRESS` - Your Ethereum address (receives payments)
- `SHIPPO_API_TOKEN` - Get from https://goshippo.com
- `ANTHROPIC_API_KEY` - Get from https://console.anthropic.com
- `WALLET_PRIVATE_KEY` - (CLI only) Your wallet for making payments

3. **Run:**
```bash
npm run dev:server
```

---

## 💡 How It Works

1. **Describe item:** "A fragile laptop, about 3 pounds, worth $800"
2. **AI extracts details:** Weight, dimensions, category, fragility
3. **Get rates:** Real-time quotes from major carriers
4. **AI recommends:** Best option based on item characteristics
5. **Pay:** $0.001 USDC via x402 protocol
6. **Ship:** Download label and tracking number

## 🔌 API Endpoints

```
GET  /health                    - Health check (free)
GET  /                          - Web UI
POST /api/shipping/quote        - Get quotes (requires $0.001 USDC)
POST /api/shipping/label        - Purchase label (requires $0.001 USDC)
POST /api/web/shipping/quote    - Web UI endpoint
POST /api/web/shipping/label    - Web UI label purchase
```

See **[API_DOCUMENTATION.md](./API_DOCUMENTATION.md)** for detailed API reference.

---

## 🤖 AI Agent Integration

This API is designed to be called by AI agents. Example use cases:

- **E-commerce chatbots** - "Ship this laptop to the customer"
- **Workflow automation** - Automatically generate labels for orders
- **MCP Servers** - Claude integration for shipping tasks
- **Langchain tools** - Add shipping capabilities to your agent

See API docs for integration examples.

---

## 🌐 Tech Stack

- **Backend:** Node.js + TypeScript + Express
- **Payments:** x402 protocol (USDC on Base Sepolia)
- **AI:** Anthropic Claude
- **Shipping:** GoShippo API
- **Blockchain:** Viem + Base

---

## 📦 What You Can Ship

The AI understands natural language descriptions:

- "A laptop, 3 pounds, valuable"
- "Fragile antique vase, small box"
- "Books, about 5 pounds"
- "iPhone in original packaging"
- "Large winter coat, not fragile"

The AI extracts weight, dimensions, value, category, and fragility automatically.

---

## 🎯 Use Cases

1. **E-commerce sellers** - Quick shipping labels for sales
2. **Marketplaces** - Integrate into your platform
3. **AI agents** - Enable shipping capabilities
4. **Developers** - Build shipping apps with x402 payments
5. **Hackathon projects** - Demonstrate x402 protocol

---

## 🔐 Security

- ✅ `.env` is gitignored (API keys not committed)
- ✅ x402 payments verified on-chain
- ✅ No personal data stored
- ✅ Testnet by default (Base Sepolia)

**For production:** Change to Base mainnet and use real USDC.

---
