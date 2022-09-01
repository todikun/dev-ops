# Manage Server With Terminal
Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. [Version Control System](https://github.com/todikun/dev-ops/tree/main/vcs-basic)
  5. [CI/CD with Cloudflare Pages](https://github.com/todikun/dev-ops/tree/main/cicd-with-cloudflare)
  6. [Manage Server with Terminal](https://github.com/todikun/dev-ops/tree/main/manage-server-with-terminal)
  7. *SOON!*
---
## 1. Terminal
Terminal merupakan tools yang sangat penting untuk dipahami, karena pada server berbasis unix/linux tidak ada GUI untuk 
diklik klik dalam menjalankan server.
      
### Text Editor  
Text editor sangat penting dipelajari karena akan membantu kita dalam membuat sebuah konfigurasi tertentu.
  
- **Nano**
          
  - Membuat sebuah file
            
    `nano test.md`
            
    <p align="center">
      <img src="./img/1.png" alt="devops" width="650">
    </p>
            
    <p align="center">
      <img src="./img/2.png" alt="devops" width="650">
    </p>

   - Memilih teks

     `ALT + A`

    <p align="center">
      <img src="./img/3.png" alt="devops" width="650">
    </p>

    - Copy & Paste

      `ALT + 6` untuk mengcopy
      
      `ALT + U` untuk paste

    <p align="center">
      <img src="./img/4.png" alt="devops" width="650">
    </p>

    - Move cursor

      `CTRL + A` pindah cursor ke baris awal
      
      `CTRL + E` pindah cursor ke baris akhir

    <p align="center">
      <img src="./img/5.png" alt="devops" width="650">
    </p>

    <p align="center">
      <img src="./img/6.png" alt="devops" width="650">
    </p>

### Text Manipulation

- **cat**

`cat` sebuah perintah untuk melihat isi dari sebuah file

<p align="center">
  <img src="./img/7.png" alt="devops" width="650">
</p>
    
`cat > (namafile)` untuk membuat sebuah file baru dan memasukkan teks

<p align="center">
  <img src="./img/8.png" alt="devops" width="650">
</p>

- **grep**

Akan mencari dan menghitung kata saya di file test.md 

`grep -c **saya** test.md`

<p align="center">
  <img src="./img/9.png" alt="devops" width="650">
</p>

---
### Monitoring

Monitoring penting karena kita dapat memantau keadaan server, seperti apakah server tersebut resource nya masih aman, atau server tersebut masih bagus atau ada yang down.

`htop`

<p align="center">
  <img src="./img/10.png" alt="devops" width="650">
</p>

Nmon

`sudo apt-get install nmon`

<p align="center">
  <img src="./img/11.png" alt="devops" width="650">
</p>

untuk menjalakankannya

`nmon`

<p align="center">
  <img src="./img/12.png" alt="devops" width="650">
</p>

<p align="center">
  <img src="./img/13.png" alt="devops" width="650">
</p>

### Netwwork Firewall
 
Firewall merupakan garis pertahanan pertama dalam menjaga keamanan jaringan komputer.

- Ufw 
  
  `sudo apt-get install ufw -y`
  
<p align="center">
  <img src="./img/14.png" alt="devops" width="650">
</p>

- Untuk menampilkan aplikasi yang didukung oleh ufw pada server

`sudo ufw app list`
  
<p align="center">
  <img src="./img/15.png" alt="devops" width="650">
</p>

## File bash

- Membuat file bash yang berisi script untuk melakukan update & upgrade system

  `nano update-system.sh`

  <p align="center">
    <img src="./img/16.png" alt="devops" width="650">
  </p>

  - Ketik perintah berikut untuk mengeksekusi

  `bash update-system.sh`

  <p align="center">
    <img src="./img/17.png" alt="devops" width="650">
  </p>

  <p align="center">
    <img src="./img/18.png" alt="devops" width="650">
  </p>

- Membuat file bash untuk membuat firewall port 22, 80 dan 443
  
  - Aktifkan ufw
  
    `sudo ufw enable`
    
  - Ketik perintah `sudo ufw verbose` untuk melihat status ufw
  
  <p align="center">
    <img src="./img/19.png" alt="devops" width="650">
  </p>
  
  - Buat sebuah file bash `nano ufw-port.sh`
  
  <p align="center">
    <img src="./img/20.png" alt="devops" width="650">
  </p>
  
  - Ketik perintah berikut untuk mengeksekusi file bash `bash ufw-port.sh`
  
  <p align="center">
    <img src="./img/21.png" alt="devops" width="650">
  </p>
  
  - Terakhir kita akan membuat file bash untuk mematikan firewall port 22, 80, 443
  
  
  <p align="center">
    <img src="./img/22.png" alt="devops" width="650">
  </p>

  <p align="center">
    <img src="./img/23.png" alt="devops" width="650">
  </p>




        
