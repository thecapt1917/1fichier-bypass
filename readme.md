# 🚀 1Fichier Bypass & Direct Link Generator

✨ Instantly generate direct download links from 1Fichier URLs – skip the waiting, bypass the limits.

![preview](https://i.postimg.cc/XYPZ2NKP/image.png)
![preview](https://i.postimg.cc/Fss7NkDq/image.png)

---

## 🌐 Live App

🔗 [Try it now!](https://thecapt1917.github.io/1fichier-bypass)  

---

## ✨ Features

- 🚫 No ads
- ⚡ **Instant Direct Link Generation** from `1fichier.com`
- 🧾 Shows **filename**, **file size**, **upload date**, and **MIME type**
- ⬇️ Direct **Download** button
- 📋 **Copy to Clipboard** with one click
- 🌍 100% **Frontend-only** – no backend required

---

## 🛠️ How to Use

1. Open the app
2. Paste a `1fichier.com` link like:
https://1fichier.com/?p4j18q797j...
3. Click **Generate Link** 🧙
4. Wait for the file info to appear 📦
5. Click **Download** ⬇️ or **Copy Link** 🔗

---

## 📦 API Reference

This app uses the public my own **1fichier Direct Link API**:

### 🔍 Get File Info

`GET https://1f.stpn.eu.org/api/info/{fileId}`

#### 📥 Path Parameters:

| Param   | Type   | Description                          |
|---------|--------|--------------------------------------|
| fileId  | string | Extracted file ID from 1fichier URL |

#### ✅ Example:

```http
GET https://1f.stpn.eu.org/api/info/p4j18q797j193qhi2f4k
```

#### 📤 Response:

```json
{
  "ok": true,
  "filename": "example.zip",
  "filesize": 12345678,
  "date": "2024-10-18 14:35:21",
  "content_type": "application/zip"
}
```


### ⚡️ Get 1Fichier Direct Link

`GET https://1f.stpn.eu.org/api/dl/{fileId}`

#### 📥 Path Parameters:

| Param   | Type   | Description                          |
|---------|--------|--------------------------------------|
| fileId  | string | Extracted file ID from 1fichier URL |

#### ✅ Example:

```http
GET https://1f.stpn.eu.org/api/dl/p4j18q797j193qhi2f4k
```

#### 📤 Response:

```json
{
  "ok": true,
  "direct_link": "https://a-34.1fichier.com/c1103650933"
}
```

### ✨ Get 1Fichier Direct Link (Proxied)

`GET https://1f.stpn.eu.org/download/{fileId}`

#### 📥 Path Parameters:

| Param   | Type   | Description                          |
|---------|--------|--------------------------------------|
| fileId  | string | Extracted file ID from 1fichier URL |

#### ✅ Example:

```http
GET https://1f.stpn.eu.org/download/p4j18q797j193qhi2f4k
```

---

## 🔐 Supported Links

- ✅ Valid `https://1fichier.com/?...` links
- ❌ Invalid or expired links will show an error 🚫

---

## 🙏 Credits

Built with ❤️ by [@thecapt1917](https://github.com/thecapt1917)

---

## ⚠️ Disclaimer

> This tool is for **educational and personal use only**.  
Please ensure you have permission to download the content.
