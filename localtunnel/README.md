# Localtunnel

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. [Version COntrol System](https://github.com/todikun/dev-ops/tree/main/vcs-basic)
  5. *SOON!*
---
Sebelum lanjut ke Localtunnel, kita coba ganti IP lama dengan baru karena koneksi yang dipilh sebelumnya pada sesi installasi **Ubuntu Server** static maka perlu di konfigurasi ulang.
  
Caranya:
  - Gunakan perintah berikut
    
    `sudo nano /etc/netplan/00-installer-config.yaml`
    
    <p align="center">
        <img src="./img/1.png" alt="devops" width="650">
    </p>
  
  - Selanjutnya untuk keluar dari teks editor ini bisa menggunakan **ctrl + x** lalu **Y** setelah itu Enter
  - Ketik perintah berikut untuk mengkonfirmasi customisasi dari **IP** yang telah dirubah tadi
    
    `sudo netplan apply`
    
  - Selanjutnya ketik perintah dibawah untuk memastikan terhubung dengan internet
    
    `ping google.com`
    
    <p align="center">
        <img src="./img/2.png" alt="devops" width="650">
    </p>
    
---
Instal localtunnel agar server local dapat diakses secara publik.
  - Install **node.js** dan **nvm**
  
    `sudo apt-get curl`
    
    `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
  
  - exec bash

    `nvm install 14`

    `node -v`

    `npm -v`
    
    <p align="center">
        <img src="./img/3.png" alt="devops" width="650">
    </p>
    
    <p align="center">
        <img src="./img/4.png" alt="devops" width="650">
    </p>
    
  -  Selanjutnya install **Localtunnel** dengan **npm**
  
     `npm install -g localtunnel`
     
     <p align="center">
        <img src="./img/5.png" alt="devops" width="650">
     </p>
    
  - Install **Apache2** 
  
    `sudo apt-get install apache2`
    
    <p align="center">
        <img src="./img/6.png" alt="devops" width="650">
    </p>
    
  - Ketik **Y** jika muncul notifkasi
  
  - Untuk menjalankan localtunel ketik perintah di bawah ini
    
    `lt --port 80`
    
    <p align="center">
        <img src="./img/7.png" alt="devops" width="650">
    </p>
    
  - Selanjutnya akses via web browser
    
    <p align="center">
        <img src="./img/8.png" alt="devops" width="650">
    </p>
    
  - Klik Continue
  - Sekarang aplikasi sudah dapat diakses secara publik.
  
    <p align="center">
        <img src="./img/9.png" alt="devops" width="650">
    </p>
    
    
