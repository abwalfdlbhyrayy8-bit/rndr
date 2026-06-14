# 🚀 RVG Gateway – codebox

دروازه (Gateway) سریع و مدرن برای تونل‌زنی VLESS روی WebSocket + HTTP Proxy، با داشبورد مدیریتی زیبا و قابلیت ساخت لینک‌های اختصاصی با محدودیت ترافیک.

---

## ✨ ویژگی‌ها

- 🔌 تونل VLESS over WebSocket (TLS 443)
- 🌐 HTTP Proxy داخلی
- 📊 داشبورد مدیریتی کامل (آمار، نمودار ترافیک، اتصالات زنده)
- 🔗 مدیریت لینک‌های نامحدود با محدودیت ترافیک اختصاصی (MB/GB)
- ✅ فعال/غیرفعال‌سازی هر لینک به‌صورت لحظه‌ای
- 📱 خروجی QR Code برای هر لینک
- 🛡️ Fingerprint Spoofing (Chrome)

---

## 1️⃣ Fork روی گیت‌هاب

ابتدا روی دکمه **Fork** کلیک کنید تا این ریپازیتوری را به حساب خود منتقل کنید:

```bash
https://github.com/arvin341az-glitch/RVG/
```

---

## 2️⃣ Deploy روی Render.com (توصیه‌شده)

1. ریپازیتوری را روی GitHub Fork کنید.
2. به [Render.com](https://render.com) بروید و **New Web Service** بسازید.
3. ریپازیتوری GitHub را متصل کنید.
4. تنظیمات زیر را وارد کنید:

   - **Runtime**: Python
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `uvicorn main:app --host 0.0.0.0 --port $PORT`

5. در بخش **Environment Variables** اضافه کنید:
   - `ADMIN_PASSWORD` = رمز دلخواه خود (پیش‌فرض: 123456)
   - `SECRET_KEY` = یک رشته طولانی random (اختیاری)

Render به‌صورت خودکار `RENDER_EXTERNAL_HOSTNAME` را ست می‌کند و HTTPS را مدیریت می‌کند.

---

## 3️⃣ اتصال به کانفیگ‌ها

پس از دیپلوی موفق:

1. به آدرس `https://your-app.onrender.com/dashboard` بروید.
2. در صفحه **داشبورد کلی**، لینک VLESS پیش‌فرض (بدون محدودیت) را مشاهده و کپی کنید.
3. این لینک را در کلاینت دلخواه (v2rayNG، NekoBox، Streisand و...) وارد کنید.
4. برای ساخت لینک‌های جداگانه با محدودیت ترافیک، به بخش **مدیریت لینک‌ها** بروید.

---
|


---


---


---

## ⚠️ نکته مهم

تمام لینک‌ها و آمار مصرف به‌صورت **درون‌حافظه (in-memory)** ذخیره می‌شوند و با هر بار ری‌استارت سرویس (روی Render یا Railway)، ریست خواهند شد. برای ذخیره‌سازی دائمی، اتصال به یک دیتابیس (Redis یا PostgreSQL) پیشنهاد می‌شود.

---

<p align="center">ساخته‌شده با ❤️ توسط <b>codebox</b></p>

---

## 💰 حمایت مالی (Donate)

اگر این پروژه به شما کمک کرد و خواستید از توسعه‌دهنده حمایت کنید:

https://wallets.arvin341az.workers.dev

🙏 از حمایت شما متشکریم!
