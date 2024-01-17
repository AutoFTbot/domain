# 🤖 Bot Telegram untuk DNS Cloudflare

Bot ini memungkinkan Anda untuk mendaftarkan domain baru dengan IP tertentu di Cloudflare, langsung dari Telegram.

## 📝 Persyaratan

Untuk menjalankan bot ini, Anda akan memerlukan beberapa hal berikut:

- Python 3.8 atau lebih tinggi.
- ID aplikasi dan hash dari [my.telegram.org](https://my.telegram.org).
- Token bot dari [BotFather](https://t.me/botfather).
- ID dan kunci Cloudflare.
- ID admin Anda di Telegram.
- Domain tentunya
## ⚙️ Pengaturan

1. Buka file `var.txt`, dan ganti `<...>` dengan nilai yang sesuai:

    ```
    api_id=<api_id Anda>
    api_hash=<api_hash Anda>
    bot_token=<token bot Anda>
    CF_ID=<ID Cloudflare Anda>
    CF_KEY=<kunci Cloudflare Anda>
    admin_id=<ID admin Anda>
    main_domain=<domain anda>
    ```

2. Jalankan skrip Python dengan perintah berikut:

    ```
    git clone https://github.com/AutoFTbot/domain
    ```
    ```
    cd domain
    ````
    ```
    pip3 install -r requirements.txt
    
    ```
    ```
    python3 domain.py
    ```

## 🔥SERVICE

```
cat >/etc/systemd/system/domain.service << EOF
[Unit]
Description=domain
After=network.target

[Service]
WorkingDirectory=/root/domain
ExecStart=python3 domain.py
Restart=always

[Install]
WantedBy=multi-user.target
EOF
systemctl daemon-reload
systemctl restart domain
systemctl enable domain
systemctl status domain
```

## 🚀 Penggunaan

Untuk menggunakan bot, kirim pesan `/ipadmin` ke bot. Bot akan meminta Anda untuk mengirimkan IP. Setelah Anda mengirimkan IP, bot akan mendaftarkan domain baru dengan IP tersebut di Cloudflare.

Jika Anda tidak merespons dalam waktu 60 detik, bot akan mengirim pesan timeout.

## 💬 Bantuan dan Dukungan

Jika Anda mengalami kesulitan atau memiliki pertanyaan, jangan ragu untuk menghubungi kami melalui Telegram di [@AutoFTbot](https://t.me/AutoFTbot).
