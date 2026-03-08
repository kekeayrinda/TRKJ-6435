[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/J9HR2HBe)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=22982678)
<div align="center">

## LAPORAN CLOUD COMPUTING

![Logo PNL](/img/logo-pnl.png)

### Disusun Oleh:  
Nama               : Keke Ayrinda  
NIM                : 2024903430012  
Kelas              : TRKJ-2A


### Program Studi Teknologi Rekayasa Komputer Jaringan
### Jurusan Teknologi Informasi dan Komputer
### Politeknik Negeri Lhokseumawe
### 2026


---


## Lembar Pengesahan


| No. Praktikum     | : | Lab 1 |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | Cloud Computing Docker |
| Tanggal Praktikum | : | 05 Maret 2026|
| Tanggal Penyerahan| : | 10 Maret 2026 |
| Nama Praktikan    | : | Keke Ayrinda |
| NIM/Kelas Praktikan| : | 2024903430012 / TRKJ-2A |
| Nilai Praktikum   | : | .......................... |
| Dosen Pengampu    | : | Muhammad Davi, S.Kom., M.Cs. |

Mengetahui,  
Dosen Pengampu
<br><br><br><br><br>

Muhammad Davi, S.Kom., M.Cs.
</div>


## Daftar Isi
- [Lembar Pengesahan](#lembar-pengesahan)
- [Daftar Isi](#daftar-isi)
- [Tujuan Praktikum](#tujuan-praktikum)
- [Dasar Teori](#dasar-teori)
- [Alat dan Bahan](#alat-dan-bahan)
- [Langkah Kerja](#langkah-kerja)
- [Hasil dan Pembahasan](#hasil-dan-pembahasan)
- [Kesimpulan](#kesimpulan)
- [Referensi](#referensi)
---

## A. Tujuan Praktikum
Tujuan dari praktikum ini adalah untuk memahami konsep dasar container menggunakan Docker serta cara mengelola image dan container. Selain itu, praktikum ini bertujuan agar mahasiswa mampu menjalankan container sederhana, membuat image Docker sendiri, serta menyimpan image tersebut ke Docker Hub. Mahasiswa juga diharapkan dapat memahami cara menjalankan aplikasi berbasis container menggunakan berbagai konfigurasi seperti volume, multi container, dan docker-compose.

## B. Dasar Teori
Docker merupakan platform containerization yang digunakan untuk membuat, menjalankan, dan mengelola aplikasi di dalam container. Container adalah lingkungan virtual ringan yang berisi semua dependensi yang diperlukan oleh sebuah aplikasi sehingga aplikasi dapat berjalan secara konsisten di berbagai sistem operasi.

Docker menggunakan konsep image dan container. Image merupakan template yang berisi sistem operasi, library, serta aplikasi yang dibutuhkan. Sedangkan container adalah instance yang berjalan dari sebuah image. Dengan menggunakan Docker, proses deployment aplikasi menjadi lebih cepat, ringan, dan konsisten dibandingkan dengan virtual machine.

Docker juga menyediakan layanan Docker Hub, yaitu repository online yang digunakan untuk menyimpan dan membagikan Docker image kepada pengguna lain. Dengan Docker Hub, pengguna dapat melakukan pull atau push image dengan mudah.

Dalam pengembangan aplikasi modern, Docker sering digunakan bersama teknologi lain seperti Node.js, database container, serta docker-compose untuk menjalankan beberapa container sekaligus dalam satu sistem.

## C. Alat dan Bahan
Alat dan bahan yang digunakan dalam praktikum ini adalah sebagai berikut:

1. Laptop atau komputer yang telah terinstal sistem operasi Linux/Windows.

2. Docker Engine yang telah terinstal pada sistem.

3. Akses internet untuk mengunduh Docker image dari Docker Hub.

4. Docker Hub account untuk menyimpan dan membagikan image.

5. Terminal atau command line.

6. Text editor seperti VSCode atau Nano untuk membuat file program dan Dockerfile.

7. Node.js dan npm untuk menjalankan aplikasi berbasis Node.js.

## D. Langkah Kerja
1. Memeriksa instalasi Docker dengan menjalankan perintah:
docker version

2. Memeriksa daftar image yang tersedia pada sistem:
docker images

3. Menjalankan container menggunakan image hello-world:
docker run hello-world

4. Mengunduh image Linux Alpine dari Docker Hub:
docker pull alpine

5. Menjalankan container Alpine dalam mode interaktif:
docker run -it alpine

6. Membuat akun pada Docker Hub dan membuat repository baru.

7. Membuat program sederhana menggunakan bahasa Go dan membuat file Dockerfile.

8. Membangun Docker image menggunakan perintah:
docker build -t username/salam .

9. Login ke Docker Hub dan mengunggah image:
docker login
docker push username/salam

10. Menjalankan image dari Docker Hub menggunakan perintah:
docker run username/salam

## E. Hasil dan Pembahasan
Hasil
Lab1.1: Docker Image "hello-world"
![Docker Version](img/Docker%20Version.png)
![docker run hello-world](img/docker%20run%20hello-world.jpg)
![docker images hello](img/docker%20images%20hello.jpg)



Hasil Lab 1.2 : Shell
![docker search alpine](img/docker%20search%20alpine.jpg)
![docker pull alpine](img/docker%20pull%20alpine.jpg)
![docker images alpine](img/docker%20images%20alpine.jpg)
![docker pull alpine:latest](img/docker%20pull%20alpinelatest.jpg)
![docker run -it alpine](img/docker%20run%20-it%20alpine.jpg)
![5 in 1 perintah linux](img/1id2date3hostnme4netstat-r5exit.jpg)
![docker ps dan docker ps-a](img/docker%20ps%20docker%20ps-a.jpg)

Hasil Lab 1.3 : Membuat Akun di Docker Hub
![dashbor dockker](img/dashbor%20docker.jpg)
![membuat respositories](img/membuat%20respositories.jpg)
![username](img/username.jpg)

Hasil Lab 1.4 : Membuat Image baru dan Menyimpan di Docker
Hub
![Buar folder baru untuk image baru](img/Buar%20folder%20baru%20untuk%20image%20baru.jpg)
![isinya salam](img/isinya%20salam.go.jpg)
![buat file Dockerfile](img/membuat%20file%20Dockerfile.jpg)
![isinya Dockerfile](img/isinya%20docker.jpg)
![build docker image](img/docker%20images%20lab%201.4.jpg)

## F. Kesimpulan
Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa Docker merupakan teknologi container yang sangat berguna untuk menjalankan aplikasi dalam lingkungan yang terisolasi. Docker mempermudah proses instalasi, deployment, dan distribusi aplikasi melalui penggunaan image dan container. Dengan adanya Docker Hub, pengguna juga dapat menyimpan dan membagikan image dengan mudah sehingga proses pengembangan aplikasi menjadi lebih efisien.
## G. Referensi
Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.
