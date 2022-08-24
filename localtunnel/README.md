# Localtunnel

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
---
Sebelum lanjut ke Localtunnel, kita coba ganti IP lama dengan baru karena koneksi yang dipilh sebelumnya pada sesi installasi **Ubuntu Server** static maka perlu di konfigurasi ulang.
  
Caranya:
  - Gunakan perintah berikut
    
    `sudo nano /etc/netplan/00-installer-config.yaml`
    
    img 1
  
  - Selanjutnya untuk keluar dari teks editor ini bisa menggunakan **ctrl + x** lalu **Y** setelah itu Enter
  - Ketik perintah berikut untuk mengkonfirmasi customisasi dari **IP** yang telah dirubah tadi
    
    `sudo netplan apply`
    
  - Selanjutnya ketik perintah dibawah untuk memastikan terhubung dengan internet
    
    `ping google.com`
    
    img 2
---
Instal localtunnel agar server local dapat diakses secara publik.
  - Install **node.js** dan **nvm**
  
    `sudo apt-get curl`
    
    `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
  
  - exec bash

    `nvm install 14`

    `node -v`

    `npm -v`
    
    img 3
    
    img 4
    
  -  Selanjutnya install **Localtunnel** dengan **npm**
    
    img 5
    
  - Install **Apache2** 
  
    `sudo apt-get install apache2`
    
    img 6
    
  - Ketik **Y** jika muncul notifkasi
  
  - Untuk menjalankan localtunel ketik perintah di bawah ini
    
    `lt --port 80`
    
    img 7
    
  - Selanjutnya akses via web browser
    
    img 8
    
  - Klik Continue
  - Sekarang aplikasi sudah dapat diakses secara publik.
  
    img 9
    
