# Sifter

Sifter tests VPN configs and connects through the best one. It runs on Linux and Windows.

**Downloads:** see the [latest release](../../releases/latest).

| System | File |
| --- | --- |
| Linux (x64) | `sifter-linux-x64.tar.gz` |
| Windows (x64) | `sifter-windows-x64.zip` |

## What it does

- Add configs by pasting share links, opening files, or giving a subscription URL.
- Supports vmess, vless, trojan, shadowsocks, hysteria2, WireGuard and SOCKS5.
- Tests each config through xray-core: real delay, exit-IP quality (ipdata.co) and download speed.
- Sorts the list by trust (high to low), then delay (low to high), so the best config is first.
- Connects through the config you pick:
  - **System proxy**: browsers and most apps (GNOME on Linux, system settings on Windows).
  - **TUN**: all traffic of the computer (needs administrator rights on Windows, a password prompt on Linux).
  - **Local proxy only**: SOCKS5 `127.0.0.1:10808` and HTTP `127.0.0.1:10809` for apps you set up yourself.
- Tray icon: grey when disconnected, coloured with a green dot when connected.
- Checks for new versions and downloads them from inside the app.

## Install

**Linux**

```
tar -xzf sifter-linux-x64.tar.gz
cd sifter
./sifter
```

Run `./install-desktop.sh` once to add Sifter to your applications menu.

**Windows**

Unzip `sifter-windows-x64.zip` and run `sifter.exe`. For TUN mode, start it as administrator.

## Notes

- The exit-IP quality score needs your own ipdata.co API key. Enter it in Settings; it is stored only on your computer.
- Subscription links that are blocked in your country may need a VPN first. Connect with a config you already have, then add the link.
- Sifter keeps its settings in `~/.config/sifter` (Linux) or `%APPDATA%\sifter` (Windows).

---

# سیفتر (Sifter)

سیفتر کانکشن‌های VPN را تست می‌کند و از بهترینشان وصل می‌شود. روی لینوکس و ویندوز اجرا می‌شود.

**دانلود:** [آخرین نسخه](../../releases/latest)

## امکانات

- افزودن کانکشن با چسباندن لینک، باز کردن فایل یا آدرس سابسکریپشن.
- پشتیبانی از vmess، vless، trojan، shadowsocks، hysteria2، WireGuard و SOCKS5.
- تست تأخیر واقعی، کیفیت IP خروجی (با ipdata.co) و سرعت دانلود.
- مرتب‌سازی بر اساس Trust (نزولی) و بعد Delay (صعودی)؛ بهترین کانکشن اول لیست است.
- اتصال از طریق کانکشن انتخاب‌شده با سه حالت: System proxy، TUN (کل سیستم) و Local proxy only.
- آیکن سینی سیستم: خاکستری در حالت قطع، رنگی با نقطه‌ی سبز در حالت وصل.
- بررسی و دریافت نسخه‌ی جدید از داخل برنامه.

## نصب

**لینوکس:** فایل `sifter-linux-x64.tar.gz` را باز کن، وارد پوشه‌ی `sifter` شو و `./sifter` را اجرا کن. برای افزودن به منوی برنامه‌ها یک بار `./install-desktop.sh` را بزن.

**ویندوز:** فایل `sifter-windows-x64.zip` را از حالت فشرده خارج کن و `sifter.exe` را اجرا کن. برای حالت TUN برنامه را با دسترسی Administrator باز کن.

## نکته‌ها

- برای امتیاز کیفیت IP به کلید API شخصی خودت از ipdata.co نیاز داری. آن را در Settings وارد کن؛ فقط روی کامپیوتر خودت ذخیره می‌شود.
- اگر لینک سابسکریپشن در کشور تو فیلتر است، اول با یک کانکشن موجود وصل شو و بعد لینک را اضافه کن.
