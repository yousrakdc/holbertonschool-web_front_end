# Cookies & Local Storage

> A hands-on exploration of browser storage mechanisms — from HTTP cookies to Web Storage APIs — built as part of the Holberton School Web Front End curriculum.

---

## 🚀 Getting Started

```bash
npm install
npm start
```

Server runs at `http://localhost:8080` with hot module replacement enabled.

### Available Scripts

| Command | Description |
|---|---|
| `npm start` | Dev server with live reload |
| `npm run dev` | Development build |
| `npm run watch` | Auto-recompile on changes |
| `npm run build` | Production build |

---

## 📁 Project Structure

```
Cookies_local_storage/
├── 0-index.html          # Webpack + basic cookies
├── 1-index.html          # Cookie expiration
├── 2-index.html          # Cookie reading & parsing
├── 3-index.html          # Login/logout flow
├── 4-index.html          # js-cookie library
├── 5-index.html          # localStorage cart
├── 6-index.html          # sessionStorage cart
├── 7-index.html          # Advanced cart (full CRUD)
├── src/index.js          # Cookie utility functions
├── dist/bundle.js        # Webpack output
├── webpack.config.js
└── package.json
```

---

## 🎯 Exercises

### 0 — Webpack Setup & Basic Cookies
Configure Webpack 5 and implement `setCookies()` / `showCookies()` with a simple login form.

### 1 — Cookie Expiration
Add 10-day expiration timestamps using the `expires` attribute and `Date.toUTCString()`.

### 2 — Cookie Parsing
Implement `getCookie(name)` to extract specific values from the cookie string.

### 3 — Authentication Flow
Full login/logout system with session persistence, welcome message, and `deleteCookiesAndShowForm()`.

### 4 — js-cookie Integration
Replicate exercise 3 using the `js-cookie` v3.0.5 library via CDN for a cleaner API.

### 5 — localStorage Cart
Persistent shopping cart (Shampoo, Soap, Sponge, Water) using `localStorage` — survives page refresh.

### 6 — sessionStorage Cart
Same cart with `sessionStorage` — data is cleared when the tab is closed.

### 7 — Advanced Cart (CRUD)
Full cart management with JSON-based quantity tracking, individual item removal, and a "Clear cart" option.

---

## 📊 Storage Comparison

| Feature | Cookies | localStorage | sessionStorage |
|---|---|---|---|
| Capacity | ~4KB | ~5–10MB | ~5–10MB |
| Expiration | Configurable | Permanent | Until tab closes |
| Sent to server | ✅ Yes | ❌ No | ❌ No |
| Scope | Domain/path | Domain | Domain + tab |
| Best for | Auth, preferences | User settings | Temporary form data |

---

## 🔒 Security Notes

- Never store passwords or sensitive tokens in plain text
- Use `Secure`, `HttpOnly`, and `SameSite` flags on cookies in production
- Web Storage is accessible via JavaScript — always sanitize inputs to prevent XSS
- Wrap `JSON.parse()` calls in `try-catch`

---

## 🧪 Testing

To manually verify your implementation, open **DevTools → Application → Storage** and inspect Cookies, localStorage, and sessionStorage. For expiration testing, temporarily set cookies to expire in 10 seconds and refresh.

---

*Holberton School — Web Front End Specialization, 2025*