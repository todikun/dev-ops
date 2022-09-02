# Web Server and Load Balancing

Daftar Isi :
  1. [Ubuntu Server](https://github.com/todikun/dev-ops/tree/main/ubuntu-server)
  2. [Localtunnel](https://github.com/todikun/dev-ops/tree/main/localtunnel)
  3. [Simple Application in Server](https://github.com/todikun/dev-ops/tree/main/application-in-server)
  4. [Version Control System](https://github.com/todikun/dev-ops/tree/main/vcs-basic)
  5. [CI/CD with Cloudflare Pages](https://github.com/todikun/dev-ops/tree/main/cicd-with-cloudflare)
  6. [Manage Server with Terminal](https://github.com/todikun/dev-ops/tree/main/manage-server-with-terminal)
  7. [Web Server & Load Balancing](https://github.com/todikun/dev-ops/tree/main/web-server-load-balancing)
---
## Install nginx

Ketik perintah berikut untuk install **nginx**
```
sudo apt-get install nginx
```

<p align="center">
  <img src="./img/1.png" alt="devops" width="650">
</p>

Aktifkan nginx
```
sudo systemctl enable nginx
```

<p align="center">
  <img src="./img/2.png" alt="devops" width="650">
</p>

```
sudo systemctl start nginx
```
Cek status nginx
```
sudo systemctl status nginx
```

<p align="center">
  <img src="./img/3.png" alt="devops" width="650">
</p>

## UFW
Buat script bash yang akan membuka port 20, 80, dan 443.
> script bash optional

<p align="center">
  <img src="./img/4.png" alt="devops" width="650">
</p>

Eksekusi file bash
```
bash <nama-file.sh>
```

<p align="center">
  <img src="./img/5.png" alt="devops" width="650">
</p>

---

## Konfigurasi Reverse Proxy dan Load Balancer dengan 2 server
Aplikasi **node js** sudah berjalan di port **3000**

<p align="center">
  <img src="./img/6.png" alt="devops" width="650">
</p>

1. Buka directory **/etc/nginx** 
2. Buat 2 file **.conf**

<p align="center">
  <img src="./img/7.png" alt="devops" width="650">
</p>

3. Isikan file **reverseproxy.conf** dengan script berikut
```
server {
    server_name dumbways.xyz;
    location / {
        proxy_pass http://10.0.2.15:3000;
    }
} 
```
<p align="center">
  <img src="./img/8.png" alt="devops" width="650">
</p>

4. Isikan file **loadbalance.conf** dengan script berikut
```
upstream loadbalance {
    server 10.0.2.15:3000;
}

server {
    server_name test.dumbways.xyz;
    location / {
        proxy_pass http://loadbalance;
    }
}
```
<p align="center">
  <img src="./img/9.png" alt="devops" width="650">
</p>

5. Buka file **/etc/nginx/nginx.conf** lalu tambahkan line berikut

<p align="center">
  <img src="./img/10.png" alt="devops" width="650">
</p>

6. Cek konfigurasi nginx

<p align="center">
  <img src="./img/11.png" alt="devops" width="650">
</p>

7. Restart nginx
```
sudo systemctl restart nginx
```

<p align="center">
  <img src="./img/12.png" alt="devops" width="650">
</p>

8. Tambahkan line berikut file **/etc/hosts** di client. Jika diwindows tambahkan difile **C:\Windows\System32\drivers\etc\hosts**
```
10.0.2.15 dumbways.xyz
10.0.2.15 test.dumbways.xyz
```

<p align="center">
  <img src="./img/13.png" alt="devops" width="650">
</p>

