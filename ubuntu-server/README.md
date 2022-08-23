# Instalasi Ubuntu Server di VMware

Sebelum lebih jauh membahas instalasi Ubuntu Server pastikan PC/Laptop kita sudah mendukung teknologi virtualisasi untuk mengecek nya ada beberapa cara : 

1. **Command Prompt** 

    >systeminfo

    Selanjutnya akan tampil informasi **Hyper-V Requirements** seperti gambar berikut

    <p align="center">
        <img src="./img/1.png" alt="devops">
    </p>
    
2. **LeoMoon CPU-V** 

    link download [Here!](https://leomoon.com/downloads/desktop-apps/leomoon-cpu-v/)

    Pastikan AMD-v Supported dan AMD-v Enabled ceklis seperti gambar berikut 
    > Note : INTEL VT (untuk pengguna INTEL)

    <p align="center">
        <img src="./img/2.png" alt="devops">
    </p>
    
    > Jika AMD-v Enabled nya tidak ceklis jangan khawatir itu hanya karena Teknologi Virtualisasinya belum enable.
    > 
    > Tutorial enable Teknologi Virtualisasi [Here!](https://www.leskompi.com/cara-mengaktifkan-virtualization-processor/)
    
---
### Tutorial Instal Ubuntu Server di VMWare
- Buka aplikasi VMware klik Create a New Virtual Machine.    
- Pilih Installer disc image file, dan cari file OS Ubuntu Server

    <p align="center">
        <img src="./img/3.png" alt="devops">
    </p>
    
- Isi Fullname, username dan password
- Buat nama virtual machine dan tentukan lokasi path virtual machine

    <p align="center">
        <img src="./img/4.png" alt="devops">
    </p>
    
    <p align="center">
        <img src="./img/5.png" alt="devops">
    </p>
    
- Isi jumlah kapasitas disk yang diinginkan, dan ceklis **Split virtual disk into multiple files.** maksudnya disk yang kita pakai untuk virtual machine kita nantinya akan dibagi menjadi beberapa bagian 

    <p align="center">
        <img src="./img/6.png" alt="devops">
    </p>
    
-  Klik Customize Hardware klik bagian Network Adapter ubah menjadi **Bridge** 
-  Klik Finish
    
    <p align="center">
        <img src="./img/7.png" alt="devops">
    </p>
    
    <p align="center">
        <img src="./img/8.png" alt="devops">
    </p>
    
- Nanti langsung diarahkan ke proses intalasi

    <p align="center">
        <img src="./img/9.png" alt="devops">
    </p>
    
- Pilih bahasa yang diinginkan **English**

    <p align="center">
        <img src="./img/10.png" alt="devops">
    </p>
    
- Selanjutnya bisa klik done

    <p align="center">
        <img src="./img/11.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/12.png" alt="devops">
    </p>
    
- Ubah konfigurasi DHCPv4 menjadi Static
- Pilih ens33, pada bagian IPv4 Method ubah automatic menjadi manual.
- Masukan detail IP, sesuaikan dengan IP dari koneksi jaringan yang dipakai

    <p align="center">
        <img src="./img/13.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/14.png" alt="devops">
    </p>
    
- Pada tahap selanjutnya bisa skip lagi dengan klik **Done**.

    <p align="center">
        <img src="./img/15.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/16.png" alt="devops">
    </p>
    
- Pilih **Custom storage layout**. Disini kita akan buat 2 partisi untuk **root** dan **swap**
- Pilih free space Klik ADD GPT Partition
- Atur ukuran space untuk swap dan root
- Klik Done.
- Klik Continue ketika muncul notifikasi konfigurasi yang telah dibuat.
    <p align="center">
        <img src="./img/17.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/18.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/19.png" alt="devops">
    </p>

    <p align="center">
        <img src="./img/20.png" alt="devops">
    </p>
    
