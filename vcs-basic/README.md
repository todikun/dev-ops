# Version Control System

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. [Version Control System](https://github.com/todikun/dev-ops/tree/main/vcs-basic)
  5. [CI/CD with Cloudflare Pages](https://github.com/todikun/dev-ops/tree/main/cicd-with-cloudflare)
  6. [Manage Server with Terminal](https://github.com/todikun/dev-ops/tree/main/manage-server-with-terminal)
  7. [Web Server & Load Balancing](https://github.com/todikun/dev-ops/tree/main/web-server-load-balancing)
---
### Python [Here](https://github.com/todikun/app-python), Golang [Here](https://github.com/todikun/app-golang), dan NodeJS [Here](https://github.com/todikun/app-nodejs).
   - Masuk ke directory project
   - Ketik perintah `git init` agar git dapat menginisiasi project kita
   
   <p align="center">
      <img src="./img/1.png" alt="devops" width="650">
   </p>
   
   - Ketik perintah :
   `git add .`
   `git commit -m "initial commit"`
   - Untuk memastikan bahwa project telah diinisasi ketik perintah berikut `git status`
   
   <p align="center">
      <img src="./img/2.png" alt="devops" width="650">
   </p>
   
   - Selanjut nya agar project dapat di upload ke repository di github, buat sebuah repositroy 
   
   <p align="center">
      <img src="./img/3.png" alt="devops" width="650">
   </p>
   
   - Buat remote
   `git remote add origin git@github.com:todikun/app-python.git`
   
   - Upload repository 
   `git push origin master` 
   
   <p align="center">
      <img src="./img/4.png" alt="devops" width="650">
   </p>
   
   - Buat branch staging
   `git branch staging`
   
   - Pindah branch
   `git checkout staging`
   
   - Untuk memastikan apakah branch sudah berganti ketik perintah berikut
   `git branch -a`
   
   <p align="center">
      <img src="./img/5.png" alt="devops" width="650">
   </p>
   
   - Lakukan pull agar branch staging dapat update commit terbaru dari branch master
   `git pull origin master`
   
   <p align="center">
      <img src="./img/6.png" alt="devops" width="650">
   </p>
   
   - Selanjutnya lakukan push
   `git push -u origin staging`
   
   <p align="center">
      <img src="./img/7.png" alt="devops" width="650">
   </p>   
   
   <p align="center">
      <img src="./img/8.png" alt="devops" width="650">
   </p>   
   
   <p align="center">
      <img src="./img/9.png" alt="devops" width="650">
   </p>
   
   - Buat branch baru dengan nama production
   `git branch production`
   `git checkout production`
      
   <p align="center">
      <img src="./img/10.png" alt="devops" width="650">
   </p>
   
   - Terakhir kita akan menggabungkan branch master ke branch production
   `git merge master`
   - Lakukan push
   `git push origin production`
        
   <p align="center">
      <img src="./img/11.png" alt="devops" width="650">
   </p> 
