# Application in Server

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. *SOON!*
---
1. NodeJs

   - Install engine javascript V8
   `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash`
   - Jalan perintah ini jika nvm belum terdeteksi `exec bash`
   
   <p align="center>
      <img src="./img/1.png" alt="devops" width="650">
   </p>
   
   - Ketik perintah berikut untuk install npm
   `npm install 14`
   - Untuk mengecek versi dari nodejs dan  `node -v` `npm -v`
   - Selanjutnya inisiasi project `npm init -y` 
   
   <p align="center>
      <img src="./img/2.png" alt="devops" width="650">
   </p>
      
   <p align="center>
      <img src="./img/3.png" alt="devops" width="650">
   </p>
   
   - Install framework Express JS sebagai backend 
   `npm install express --save`
      
   <p align="center>
      <img src="./img/4.png" alt="devops" width="650">
   </p>
   
   - Buat sebuah file index.js
   `nano index.js`    
   
   <p align="center>
      <img src="./img/5.png" alt="devops" width="650">
   </p>
   
   - Jalankan program file index.js
   `node index.js`   
   
   <p align="center>
      <img src="./img/6.png" alt="devops" width="650">
   </p>
   
   - Buka browser akses IP dengan port `3000` 
         
   <p align="center>
      <img src="./img/7.png" alt="devops" width="650">
   </p>
---
2. Golang
  - Ketik perintah berikut untuk menginstall golang
  `sudo apt-get install golang-go`
  - Cek versi golang yang telah diinstal      
  
   <p align="center>
      <img src="./img/9.png" alt="devops" width="650">
   </p>
   
   - Buat file index.go
   `nano index.go`
   - Masukan script dibawah
         
   <p align="center>
      <img src="./img/10.png" alt="devops" width="650">
   </p>
   
   - Jalankan dengan perintah berikut
   `go run index.go`   
   
   <p align="center>
      <img src="./img/11.png" alt="devops" width="650">
   </p>
   
   - Jika aplikasi ingin dibuild jalankan perintah berikut
   `go build index.go`
      
   <p align="center>
      <img src="./img/12.png" alt="devops" width="650">
   </p>
   
   - Selanjutnya jalankan perintah berikut
   `./index`
      
   <p align="center>
      <img src="./img/13.png" alt="devops" width="650">
   </p>
---
3. Python
 Python tidak perlu dinstal karena sudah ada secara default
   - Cek versi python
   `python3 -V`
   
   <p align="center>
      <img src="./img/14.png" alt="devops" width="650">
   </p>
   
   - Install package manager dari python
   `sudo apt-get intall python3-pip`
   `pip install flask`
   - Buat file index.py
   `nano index.py`
   - Masukan script berikut
      
   <p align="center>
      <img src="./img/15.png" alt="devops" width="650">
   </p>

   - Run index,py
   `python3 index.py`  
   
   <p align="center>
      <img src="./img/16.png" alt="devops" width="650">
   </p>
   
   - Buka browser menggunakan IP dengan port `5000`
      
   <p align="center>
      <img src="./img/17.png" alt="devops" width="650">
   </p>
---
## PM2 dan Localtunnel untuk menjalankan aplikasi
  - Download pm2
  `npm install pm2@latest -g`
  
  ### NodeJS
  - Jalankan aplikasi NodeJS yang sudah dibuat sebelumnya dengan command berikut
  `pm2 start app-nodejs/index.js`
  
   <p align="center>
      <img src="./img/18.png" alt="devops" width="650">
   </p>
   
  ### Python
  - Jalankan aplikasi Python yang sudah dibuat sebelumnya dengan command berikut
  `pm2 start app-python/python.js`
  
   <p align="center>
      <img src="./img/19.png" alt="devops" width="650">
   </p>
   
   - Ketik perintah ini untuk melihat proses pm2 yang running
   `pm2 list`
   
   <p align="center>
      <img src="./img/20.png" alt="devops" width="650">
   </p>
   
   ### Cek dibrowser
      
   <p align="center>
      <img src="./img/21.png" alt="devops" width="650">
   </p>   
   
   <p align="center>
      <img src="./img/22.png" alt="devops" width="650">
   </p>
   
   - Jalankan localtunnel dengan port `3000` dan `5000`
         
   <p align="center>
      <img src="./img/23.png" alt="devops" width="650">
   </p>   
   
   <p align="center>
      <img src="./img/24.png" alt="devops" width="650">
   </p>
   
   
   
  

