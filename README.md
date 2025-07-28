# 🔐 Simple Free Fire JWT Decoder API

A simple Flask API that decodes and verifies Free Fire JWT tokens.

## 📌 Features

- Decode JWT without verifying signature
- Extract header, payload, and signature
- Check expiration (`exp`) and verify signature (if secret provided)
- Built with **Flask** and **PyJWT**
- Deploy-ready on **Vercel**

---

## 📂 API Endpoints

### ✅ Health Check

```
GET /
```

**Response:**
```json
{
  "message": "API made by @dear_sumi is alive"
}
```

---

### 🔍 Decode JWT Token

```
GET /decode?token={jwt_token}
```
```
https://free-fire-jwt-decoder.vercel.app/dhttps://free-fire-jwt-decoder.vercel.app/decode?token={jwt_token}ecode?token={jwt_token}
```
### Example:
```
https://free-fire-jwt-decoder.vercel.app/decode?token=eyJhbGciOiJIUzI1NiIsInN2ciI6IjMiLCJ0eXAiOiJKV1QifQ.eyJhY2NvdW50X2lkIjoxMTQ5OTU4MjA4Mywibmlja25hbWUiOiJN4bSA4bSiyarhtIXhtLPhtLnhtL8wNyIsIm5vdGlfcmVnaW9uIjoiSU5EIiwibG9ja19yZWdpb24iOiJJTkQiLCJleHRlcm5hbF9pZCI6IjMxNzk2YjhkYWIzMmU0NTRlYmQxZDMyMGUxNDMwOWYyIiwiZXh0ZXJuYWxfdHlwZSI6NCwicGxhdF9pZCI6MSwiY2xpZW50X3ZlcnNpb24iOiIxLjEwOC4zIiwiZW11bGF0b3Jfc2NvcmUiOjEwMCwiaXNfZW11bGF0b3IiOnRydWUsImNvdW50cnlfY29kZSI6IlVTIiwiZXh0ZXJuYWxfdWlkIjozODI0NTg0NjA5LCJyZWdfYXZhdGFyIjoxMDIwMDAwMDcsInNvdXJjZSI6NCwibG9ja19yZWdpb25fdGltZSI6MTc0MjYwNzc4NywiY2xpZW50X3R5cGUiOjIsInNpZ25hdHVyZV9tZDUiOiIiLCJ1c2luZ192ZXJzaW9uIjoxLCJyZWxlYXNlX2NoYW5uZWwiOiIzcmRfcGFydHkiLCJyZWxlYXNlX3ZlcnNpb24iOiJPQjQ5IiwiZXhwIjoxNzUzNzQ0MjYzfQ.e1Z0OTcdsrdv1NtNMVxPZC3hWTKIFWfZH07YPQ7FORQ 
```

**Response Example:**
```json
{
  "expired": false,
  "header": {
    "alg": "HS256",
    "svr": "3",
    "typ": "JWT"
  },
  "payload": {
    "account_id": 11499582083,
    "client_type": 2,
    "client_version": "1.108.3",
    "country_code": "US",
    "emulator_score": 100,
    "exp": 1753744263,
    "external_id": "31796b8dab32e454ebd1d320e14309f2",
    "external_type": 4,
    "external_uid": 3824584609,
    "is_emulator": true,
    "lock_region": "IND",
    "lock_region_time": 1742607787,
    "nickname": "Mᴀᴢɪᴅᴳᴹᴿ07",
    "noti_region": "IND",
    "plat_id": 1,
    "reg_avatar": 102000007,
    "release_channel": "3rd_party",
    "release_version": "OB49",
    "signature_md5": "",
    "source": 4,
    "using_version": 1
  },
  "signature": "e1Z0OTcdsrdv1NtNMVxPZC3hWTKIFWfZH07YPQ7FORQ",
  "signature_valid": false,
  "valid": false
}
```




---

## 🔗 One-Click Deploy to Vercel

> You can deploy instantly using the button below.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/import?s=https://github.com/bisug/FREE-FIRE-JWT-DECODER-API)

> Replace `bisug` with your GitHub username if you fork the repo.

---

## 📁 Folder Structure

```
jwt-decoder-api/
├── app.py
├── requirements.txt
├── vercel.json
└── README.md
```

## 🆘 Need Help?

DM [@dear_sumi](https://t.me/dear_sumi) on Telegram for help or contributions.
