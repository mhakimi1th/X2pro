# 🚀 x2pro – سیستم مدیریت هوشمند کانفیگ‌های شبکه

> **X2PRO Panel v2.0** — یک پنل خودمیزبان، امن و بدون نیاز به سرور، بر پایه **Cloudflare Workers**  
> مدیریت کانفیگ‌های VLESS, VMess, Trojan, TUIC, Hysteria و ... در یک رابط کاربری فارسی و واکنش‌گرا

![License](https://img.shields.io/badge/license-MIT-blue)
![Version](https://img.shields.io/badge/version-2.0-green)
![Platform](https://img.shields.io/badge/platform-Cloudflare_Worker-orange)




## ✨ ویژگی‌های کلیدی

### 🔐 امنیت و احراز هویت
- ورود با نام کاربری و رمز عبور (احراز هویت ساده ولی امن)
- پشتیبانی از چند ادمین با نقش‌های مختلف (`owner`, `editor`)
- محدودیت تلاش ورود (حداکثر ۵ تلاش قبل از قفل موقت)
- جلسه کاربر با عمر ۳۰ دقیقه (اتمام خودکار)
- لاگ کامل از تمام عملیات (ورود، تغییر تنظیمات، حذف کاربر و ...)

### 🌐 پشتیبانی از تمام پروتکل‌های مدرن
- VLESS + XTLS + Reality
- VMess (AEAD / Legacy)
- Trojan & Trojan-Go
- Shadowsocks / ShadowsocksR
- Hysteria / Hysteria2
- TUIC v5
- Snell v3
- WireGuard
- و بسیاری دیگر!

### 🧩 مدیریت کانفیگ‌ها
- ✅ افزودن دستی یا انبوه کانفیگ (با لینک یا JSON)
- ✅ استخراج خودکار از لینک‌های **GitHub Public**
- ✅ تست سلامت (Health Check) با تشخیص Latency، TLS Handshake و وضعیت IP
- ✅ دسته‌بندی کانفیگ‌ها بر اساس منبع (Source)
- ✅ فعال/غیرفعال، حذف و مرتب‌سازی دسته‌ای

### 👥 مدیریت کاربران
- ایجاد کاربر با UUID، ترافیک، تعداد اتصال و تاریخ انقضا
- تمدید کاربر، تغییر پروتکل‌های مجاز
- QR Code شخصی برای هر کاربر (`/qrcode/{userId}`)
- اشتراک تک کاربره (Subscription URL)

### 🛠️ ابزارهای هوشمند
- مدیریت لینک‌های GitHub برای استخراج خودکار کانفیگ
- اجرا خودکار استخراج هر ۱۲ ساعت (قابل تنظیم)
- اضافه کردن IPهای سالم (IPv4/IPv6) برای پروکسی تلگرام
- پشتیبان‌گیری و بازیابی داده‌ها (Backup & Restore)

### 🎨 رابط کاربری مدرن
- رابط کاملاً فارسی با پشتیبانی از RTL
- تم روشن و تیره
- واکنش‌گرا (موبایل، تبلت، دسکتاپ)
- استفاده از **Tailwind CSS**, **Lucide Icons**, و فونت **Vazirmatn**

---

## 🌐 منابع پیشنهادی کانفیگ
شما می‌توانید از لینک‌های زیر به عنوان منبع خودکار برای استخراج کانفیگ استفاده کنید. این لینک‌ها توسط خود سیستم X2PRO مدیریت می‌شوند و به‌روزرسانی دوره‌ای دارند.

برای اضافه کردن، وارد بخش **ابزارها > مدیریت لینک GitHub** شوید و لینک‌های زیر را با نام مناسب اضافه کنید:

| نام منبع                | لینک Raw                                                               |
|-------------------------|------------------------------------------------------------------------|
| 🔹 کانفیگ‌های VMess     | `https://raw.githubusercontent.com/mhakimi1th/X2pro/main/vmess.txt`     |
| 🔷 کانفیگ‌های VLESS     | `https://raw.githubusercontent.com/mhakimi1th/X2pro/main/vless.txt`     |
| 🟡 کانفیگ‌های Trojan    | `https://raw.githubusercontent.com/mhakimi1th/X2pro/main/trojan.txt`   |
| ⚫ کانفیگ‌های Shadowsocks| `https://raw.githubusercontent.com/mhakimi1th/X2pro/main/ss.txt`       |
| ⚡ کانفیگ‌های Hysteria2 | `https://raw.githubusercontent.com/mhakimi1th/X2pro/main/hysteria2.txt` |

> ✅ پس از اضافه کردن، می‌توانید روی دکمه **"استخراج"** کلیک کنید یا صبر کنید تا سیستم به‌صورت خودکار هر ۱۲ ساعت یکبار آن‌ها را به‌روز کند.


## 📦 نحوه نصب و راه‌اندازی

### 1. پیش‌نیازها
- حساب [Cloudflare](https://dash.cloudflare.com) (رایگان)
- دسترسی به **Workers & KV**
- دانلود کدهای پروژه از گیتهاب

### 2. مراحل نصب

#### مرحله ۱: کلون کردن پروژه
```bash
git clone https://github.com/mhakimi1th/X2pro.git
cd X2pro


## 📸 نمایی از رابط کاربری

در ادامه تصاویری از رابط کاربری X2PRO آورده شده است:

<div align="center">
  <h3>🔐 صفحه ورود</h3>
  <img src="https://github.com/mhakimi1th/X2pro/blob/main/img/login.JPG?raw=true" alt="صفحه ورود" width="800" style="border-radius: 12px; margin-bottom: 24px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);" />
  
  <h3>📊 داشبورد اصلی</h3>
  <img src="https://github.com/mhakimi1th/X2pro/blob/main/img/dash.JPG?raw=true" alt="داشبورد" width="800" style="border-radius: 12px; margin-bottom: 24px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);" />
  
  <h3>👥 مدیریت کاربران</h3>
  <img src="https://github.com/mhakimi1th/X2pro/blob/main/img/user.JPG?raw=true" alt="مدیریت کاربران" width="800" style="border-radius: 12px; margin-bottom: 24px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);" />
  
  <h3>⚙️ مدیریت کانفیگ‌ها</h3>
  <img src="https://github.com/mhakimi1th/X2pro/blob/main/img/conf.JPG?raw=true" alt="کانفیگ‌ها" width="800" style="border-radius: 12px; margin-bottom: 24px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);" />
  
  <h3>🔧 ابزارها و مدیریت GitHub</h3>
  <img src="https://github.com/mhakimi1th/X2pro/blob/main/img/git.JPG?raw=true" alt="ابزارها" width="800" style="border-radius: 12px; margin-bottom: 24px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);" />
---

</div>

---
