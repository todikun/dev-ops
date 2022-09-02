# CI/CD with Cloudflare Pages

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. [Version Control System](https://github.com/todikun/dev-ops/tree/main/vcs-basic)
  5. [CI/CD with Cloudflare Pages](https://github.com/todikun/dev-ops/tree/main/cicd-with-cloudflare)
  6. [Manage Server with Terminal](https://github.com/todikun/dev-ops/tree/main/manage-server-with-terminal)
  7. [Web Server & Load Balancing](https://github.com/todikun/dev-ops/tree/main/web-server-load-balancing)
---
> Repository [Here](https://github.com/todikun/wayshub-frontend), Web Pages [Here](https://dumb-frontend.pages.dev/login)

Ctt : Login [Cloudflare](https://cloudflare.com/), jika belum punya akun silahkan registrasi terlebih dahulu [Cloudflare](https://cloudflare.com/sign-up)

### 1. Cloudflare Pages
   - Masuk kemenu **pages** untuk membuat project baru
   
   <p align="center">
    <img src="./img/1.png" alt="devops" width="650">
   </p>
   
   - Klik **Connect To Github**, agar repository di github dapat terdeteksi di **Cloudflare Pages**
   - Pilih akun github
   
   <p align="center">
    <img src="./img/2.png" alt="devops" width="650">
   </p>
   
   - Pilih **Only select repositories** karena kita akan menghubungkan **Cloudflare Pages** ke salah satu repositories saja
   
   <p align="center">
    <img src="./img/3.png" alt="devops" width="650">
   </p>
   
   - Klik **Begin setup** untuk memulai konfigurasi
   
   <p align="center">
    <img src="./img/4.png" alt="devops" width="650">
   </p>
   
   - Isi nama project dan pilih branch
   
   <p align="center">
    <img src="./img/5.png" alt="devops" width="650">
   </p>
   
   - Pilih **Framework preset**
   
   <p align="center">
    <img src="./img/6.png" alt="devops" width="650">
   </p>
   
   - Selanjutnya klik **Save and deploy**
   - Tunggu proses build sampai selesai
   
   <p align="center">
    <img src="./img/7.png" alt="devops" width="650">
   </p>
   
   <p align="center">
    <img src="./img/8.png" alt="devops" width="650">
   </p>
   
   - Selanjutnya buka url yang ada di sebelah **Domains**
   <p align="center">
    <img src="./img/9.png" alt="devops" width="650">
   </p>
   
### 2. Update code

   - Buka ubuntu server di VMWare
   - Lakukan clone repository `git clone <repository>`
   
   <p align="center">
    <img src="./img/10.png" alt="devops" width="650">
   </p>
   
   - Kita akan mengubah `title` di file **index.html**
   
   <p align="center">
    <img src="./img/11.png" alt="devops" width="650">
   </p>
   
   - Melakukan push repository
   
     `git add . `

     `git commit -m "update index.html"`

     `git push origin main`
   
   <p align="center">
    <img src="./img/12.png" alt="devops" width="650">
   </p>
   
   - Selanjutnya **Cloudflare** akan ke trigger untuk melakukan build ulang ketika ada perubahan yang terjadi pada repository
   
   <p align="center">
    <img src="./img/13.png" alt="devops" width="650">
   </p>
   
   <p align="center">
    <img src="./img/14.png" alt="devops" width="650">
   </p>
   
   - Tunggu proses build nya sampai selesai
   
   <p align="center">
    <img src="./img/15.png" alt="devops" width="650">
   </p>
   
   - **Title** pada web pages telah berubah
   
   <p align="center">
    <img src="./img/16.png" alt="devops" width="650">
   </p>
   
   
   
   
   
   
 
