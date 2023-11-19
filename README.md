Bot Telegram untuk DNS Cloudflare

Bot ini memungkinkan Anda untuk mendaftarkan domain baru dengan IP tertentu di Cloudflare, langsung dari Telegram.

Persyaratan
Anda akan memerlukan beberapa hal berikut untuk menjalankan bot ini:
Python 3.8 atau lebih tinggi.
ID aplikasi dan hash dari my.telegram.org.
Token bot dari BotFather.
ID dan kunci Cloudflare.
ID admin Anda di Telegram.

Pengaturan
Buka file var.txt,dan ganti <...> dengan nilai yang sesuai:
api_id=<api_id Anda>
api_hash=<api_hash Anda>
bot_token=<token bot Anda>
CF_ID=<ID Cloudflare Anda>
CF_KEY=<kunci Cloudflare Anda>
admin_id=<ID admin Anda>

Jalankan skrip Python dengan perintah berikut:
git clone https://github.com/AutoFTbot/domain
cd domain
python3 domain.py

Penggunaan
Untuk menggunakan bot, kirim pesan /ipadmin ke bot. Bot akan meminta Anda untuk mengirimkan IP. Setelah Anda mengirimkan IP, bot akan mendaftarkan domain baru dengan IP tersebut di Cloudflare.

Jika Anda tidak merespons dalam waktu 60 detik, bot akan mengirim pesan timeout.
