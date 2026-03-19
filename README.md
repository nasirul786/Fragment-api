# ⭐ Fragment Stars API

Buy Telegram Stars for any user using their username.  
Payment is automatically deducted from your TON wallet.

This API allows you to build a fully automated **Telegram Stars selling bot**.

### [Test Video 🕵️‍♂️🕵️‍♂️](https://t.me/bottercc/469)

---

## 🚀 Features

- Buy Telegram Stars via username
- Automatic TON wallet transaction signing
- Fast and optimized backend
- Fragment user lookup support
- Supports multiple wallet versions

---

## 📦 Base URL

```

https://api.arijitiyan.cc/frgmnt/

```

---

## ⭐ Buy Telegram Stars

Initiate a purchase of Telegram Stars for a specific user.

### **Endpoint**
```

POST https://api.arijitiyan.cc/frgmnt/buy.php

````

### **Request Body**
```json
{
  "recipient": "@arijitiyan",
  "wallet_seed": [
    "word1", "word2", "word3", "word4", "word5", "word6",
    "word7", "word8", "word9", "word10", "word11", "word12",
    "word13", "word14", "word15", "word16", "word17", "word18",
    "word19", "word20", "word21", "word22", "word23", "word24"
  ],
  "amount": 50,
  "wallet_version": "v5r1"
}
````

### **Parameters**

| Field          | Type   | Description                          |
| -------------- | ------ | ------------------------------------ |
| recipient      | string | Telegram username (with `@`)         |
| wallet_seed    | array  | 12 or 24-word TON wallet seed phrase |
| amount         | number | Number of stars (50 to 2500)         |
| wallet_version | string | Wallet version (e.g. `v5r1`)         |

---

### ✅ **Success Response**

```json
{
  "ok": true,
  "message": "Transaction successfully signed and broadcasted.",
  "data": {
    "user": "ɪ ᴀᴍ ᴄᴄ",
    "username": "@arijitiyan",
    "ton_paid": 0.6205,
    "star_purchased": 50
  }
}
```

---

### ❌ **Error Response**

```json
{
  "ok": false,
  "message": "Recipient not found on Fragment. (Check if cookie is expired)"
}
```

---

## 🔍 Search User

Retrieve a Telegram user's Fragment details.

### **Endpoint**

```
POST https://api.arijitiyan.cc/frgmnt/buy.php
```

### **Request Body**

```json
{
  "username": "@mslylia"
}
```

---

### ✅ **Response**

```json
{
  "ok": true,
  "data": {
    "name": "mslylia",
    "username": "@mslylia",
    "photo": "https://cdn5.telesco.pe/file/J9zZgP........jpg",
    "fragment_id": "C2.....ZIpw8ita_Gry2Kq"
  }
}
```

---

## 💡 Notes

* Ensure the wallet has sufficient TON balance before making a purchase.
* Wallet seed must be correct and secure.
* Use username to purchase.

---

## 🚀 Get the Source Code

The backend source code is **paid and highly optimized**.

📩 Contact: [@arijitiyan](https://t.me/arijitiyan)
---

## ⚙️ Backend Architecture

This API is built with a **minimal single-file Node.js architecture** for speed and simplicity.

- The entire backend runs from a single file: node api.js
- Uses **TON blockchain libraries** to:
- Derive wallet from seed phrase
- Sign transactions securely
- Broadcast transactions to the TON network
- Integrates with **TON API / RPC endpoints** for real-time transaction execution
- Handles:
- Fragment user lookup
- Star purchase logic
- Transaction building & submission
- Designed to be **lightweight, fast, and easy to deploy**

> ⚡ No complex framework required — just Node.js + TON SDK
---

Made with ❤️ by **Botter**
Telegram: [https://t.me/bottercc](https://t.me/bottercc)

