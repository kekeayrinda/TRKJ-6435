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
| Judul Praktikum   | : | Dasar-Dasar Docker (Docker Image, Container, dan Docker Hub) |
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
- [Analisa](#Analisa)
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
Lab1.1: Docker Image "hello-world" :
Perintah docker version digunakan untuk memastikan Docker telah terinstal dengan benar. Saat menjalankan docker run hello-world, Docker secara otomatis melakukan pull image dari Docker Hub jika belum tersedia di lokal. Hasil pada docker images menunjukkan bahwa image berhasil diunduh dan siap digunakan.
![Docker Version](img/Docker%20Version.png)
![docker run hello-world](img/docker%20run%20hello-world.jpg)
![docker images hello](img/docker%20images%20hello.jpg)



Hasil Lab 1.2 : Shell :
Perintah docker search alpine dan docker pull alpine digunakan untuk mencari dan mengunduh image Alpine. Selanjutnya, docker run -it alpine menjalankan container dalam mode interaktif sehingga dapat digunakan seperti sistem operasi Linux. Perintah seperti id, date, dan hostname menunjukkan bahwa container berjalan dengan baik. Perbedaan docker ps dan docker ps -a menunjukkan container aktif dan riwayat container.
![docker search alpine](img/docker%20search%20alpine.jpg)
![docker pull alpine](img/docker%20pull%20alpine.jpg)
![docker images alpine](img/docker%20images%20alpine.jpg)
![docker pull alpine:latest](img/docker%20pull%20alpinelatest.jpg)
![docker run -it alpine](img/docker%20run%20-it%20alpine.jpg)
![5 in 1 perintah linux](img/1id2date3hostnme4netstat-r5exit.jpg)
![docker ps dan docker ps-a](img/docker%20ps%20docker%20ps-a.jpg)

Hasil Lab 1.3 : Membuat Akun di Docker Hub :
Pembuatan akun Docker Hub berhasil dilakukan sebagai sarana penyimpanan dan distribusi image. Repository yang dibuat dapat digunakan untuk menyimpan image agar dapat diakses kembali atau dibagikan ke pengguna lain.
![dashbor dockker](img/dashbor%20docker.jpg)
![membuat respositories](img/membuat%20respositories.jpg)
![username](img/username.jpg)

Hasil Lab 1.4 : Membuat Image baru dan Menyimpan di Docker
Hub :
Pembuatan file salam.go dan Dockerfile menunjukkan proses pembuatan aplikasi sederhana berbasis Golang. Perintah docker build digunakan untuk membuat image dari Dockerfile. Hasil docker images membuktikan bahwa image berhasil dibuat dan siap untuk dijalankan atau di-push ke Docker Hub.
![Buar folder baru untuk image baru](img/Buar%20folder%20baru%20untuk%20image%20baru.jpg)
![isinya salam](img/isinya%20salam.go.jpg)
![buat file Dockerfile](img/membuat%20file%20Dockerfile.jpg)
![isinya Dockerfile](img/isinya%20docker.jpg)
![build docker image](img/docker%20images%20lab%201.4.jpg)

## F. Kesimpulan
Docker merupakan teknologi container yang sangat berguna untuk menjalankan aplikasi dalam lingkungan yang terisolasi. Docker mempermudah proses instalasi, deployment, dan distribusi aplikasi melalui penggunaan image dan container. Dengan adanya Docker Hub, pengguna juga dapat menyimpan dan membagikan image dengan mudah sehingga proses pengembangan aplikasi menjadi lebih efisien.

## G. Analisa
Docker berhasil digunakan untuk menjalankan image seperti hello-world dan memahami proses pull secara otomatis dari Docker Hub. Penggunaan container berbasis Alpine menunjukkan bahwa container dapat berfungsi seperti sistem operasi yang terisolasi. Selain itu, pembuatan dan penyimpanan image ke Docker Hub membuktikan bahwa Docker memudahkan distribusi aplikasi secara efisien.

## H. Referensi
1. Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.
2. Docker Inc. (2023). Docker Documentation. https://docs.docker.com
3. Node.js. (2023). Node.js Official Documentation. https://nodejs.org
4. Express.js. (2023). Express Framework Documentation. https://expressjs.com


<div align="center">
---

## Lembar Pengesahan


| No. Praktikum     | : | Lab 2 |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | Pembuatan dan Deployment Aplikasi Node.js Menggunakan Docker |
| Tanggal Praktikum | : | 02 April 2026|
| Tanggal Penyerahan| : | 09 April 2026 |
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
- [Analisa](#Analisa)
- [Referensi](#referensi)
---

## A. Tujuan Praktikum
Memahami proses pembuatan dan pengelolaan aplikasi berbasis container menggunakan Docker, khususnya pada proyek Node.js. Mahasiswa diharapkan mampu membuat aplikasi sederhana menggunakan Node.js dan Express, kemudian mengkonfigurasinya ke dalam Dockerfile untuk dijadikan sebuah image. Selain itu, praktikum ini bertujuan agar mahasiswa dapat melakukan build image, menjalankan container dengan pengaturan port dan mode daemon, serta memahami cara menyimpan (push) dan mengambil (pull) image dari Docker Hub. Dengan demikian, mahasiswa dapat mengimplementasikan konsep containerization dalam pengembangan dan distribusi aplikasi secara efektif.

## B. Dasar Teori
Docker merupakan platform containerization yang digunakan untuk mengemas aplikasi beserta seluruh dependensinya ke dalam sebuah container sehingga dapat dijalankan secara konsisten di berbagai lingkungan. Dengan menggunakan Docker, proses pengembangan, pengujian, dan deployment aplikasi menjadi lebih efisien karena tidak bergantung pada konfigurasi sistem host.

Dalam praktikum ini digunakan Node.js sebagai runtime environment untuk menjalankan aplikasi berbasis JavaScript di sisi server. Framework Express digunakan untuk mempermudah pembuatan server web sederhana dengan menangani request dan response. Aplikasi Node.js yang dibuat kemudian dikonfigurasi dalam sebuah file bernama package.json yang berisi informasi proyek dan dependensi yang dibutuhkan.

Untuk mengubah aplikasi menjadi container, digunakan Dockerfile yang berisi serangkaian instruksi seperti menentukan base image (node), menyalin file aplikasi, menginstal dependensi, serta menjalankan aplikasi. Setelah Dockerfile dibuat, image dapat dibangun menggunakan perintah docker build dan dijalankan sebagai container dengan docker run disertai pengaturan port mapping agar aplikasi dapat diakses melalui browser.

Selain itu, Docker juga memungkinkan pengguna untuk menyimpan dan mendistribusikan image melalui Docker Hub. Dengan fitur ini, image yang telah dibuat dapat di-push ke repository dan di-pull kembali oleh pengguna lain, sehingga memudahkan kolaborasi dan distribusi aplikasi secara luas.

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
1. Membuat Direktori Proyek
2. Memastikan Instalasi Node.js dan npm
3. MInisialisasi Proyek Node.js
4. Menambahkan Dependency Express
5. Membuat File Aplikasi
6. Menjalankan Aplikasi Secara Lokal
7. Membuat Dockerfile
8. Membangun Docker Image
9. Menguji Aplikasi di Browser
10. Menyimpan Image ke Docker Hub (Opsional)

## E. Hasil dan Pembahasan
Hasil 5 DockerImage"node_project" :

Membuat direktori dengan perintah mkdir lalu pin
dahkedirektoritersebutdengancd(changedirectory).
mkdir node_project & cd node_project
Digunakan untuk membuat dan masuk ke direktori proyek sebagai tempat pengembangan aplikasi Node.js.
![node_project & cd node_project](img2/node_project.jpg)

npm -v :
Untuk memastikan bahwa Node.js dan npm sudah terinstal dengan baik pada sistem.
![npm-v](img2/npm-v.jpg)

npm init-y :
Digunakan untuk membuat file package.json yang berisi konfigurasi dasar proyek.
![npm init-y](img2/npm%20init.jpg)



npm install express :
Menambahkan framework Express sebagai dependency untuk membuat server web sederhana.
![ npm install express](img2/npm%20install%20express.jpg)


file index.js :
File ini berisi kode program utama untuk menjalankan server Node.js yang menampilkan output saat diakses.
![ file index.js](img2/file%20index.js.jpg)


node index.js :
Digunakan untuk menjalankan aplikasi secara lokal dan memastikan program berjalan dengan baik.
![ Mengaktifkan file index.js](img2/node%20index.js.jpg)


buka di web browser dengan url http://localhost:7000 :
Membuktikan bahwa server berhasil berjalan dan dapat diakses melalui web browser.
![ output di web](img2/output%20di%20web.jpg)


Selanjutnya  membuat Dockerfile menggunakan kode berikut ini:
DockerFile :
Dockerfile berisi instruksi untuk mengemas aplikasi Node.js ke dalam image Docker.
![ DockerFile](img2/Docker%20File.jpg)

docker build & docker tag :
Digunakan untuk membuat image dan memberikan nama serta versi agar mudah dikenali.
![ docekrtag](img2/docker%20tag.jpg)
![ dockertag 2](img2/docker%20tag%20(2).jpg)

## F. Kesimpulan
Docker mempermudah proses pengemasan dan menjalankan aplikasi Node.js ke dalam container sehingga lebih konsisten dan mudah didistribusikan. Melalui pembuatan aplikasi sederhana, pembuatan Dockerfile, hingga menjalankan container, praktikan dapat memahami dasar penggunaan Docker dalam proses deployment aplikasi secara efisien.

## G. Analisa
Pada praktikum ini, aplikasi Node.js berhasil dibuat dan dijalankan menggunakan Express, kemudian dikemas ke dalam Docker menggunakan Dockerfile. Proses build dan run menunjukkan bahwa aplikasi dapat berjalan secara konsisten dalam container serta dapat diakses melalui port yang telah dikonfigurasi. Selain itu, penggunaan Docker Hub memudahkan distribusi image sehingga aplikasi dapat dibagikan dan dijalankan di lingkungan lain dengan lebih efisien.

## H. Referensi
1. Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.
2. Docker Inc. (2023). Docker Documentation. https://docs.docker.com
3. Node.js. (2023). Node.js Official Documentation. https://nodejs.org
4. Express.js. (2023). Express Framework Documentation. https://expressjs.com


<div align="center">
---

## Lembar Pengesahan


| No. Praktikum     | : | Lab 3 |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | Manajemen Penyimpanan Data dengan Docker Volume |
| Tanggal Praktikum | : | 09 April 2026|
| Tanggal Penyerahan| : | 16 April 2026 |
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
- [Analisa](#Analisa)
- [Referensi](#referensi)
---

## A. Tujuan Praktikum
Memahami konsep Docker Volume sebagai media penyimpanan data yang bersifat persisten pada container. Mahasiswa diharapkan mampu membuat dan menggunakan volume, baik yang bersifat anonymous maupun named volume, serta memahami cara berbagi data antar container menggunakan volume. Selain itu, praktikum ini bertujuan agar mahasiswa dapat mengelola penyimpanan data sehingga tetap tersedia meskipun container dihentikan atau dihapus.

## B. Dasar Teori
Docker Volume merupakan mekanisme penyimpanan data pada Docker yang digunakan untuk mengatasi keterbatasan container yang bersifat sementara (ephemeral). Secara default, data yang berada di dalam container akan hilang ketika container dihentikan atau dihapus. Oleh karena itu, Docker Volume digunakan sebagai media penyimpanan persisten yang terhubung langsung dengan sistem host.

Docker menyediakan beberapa jenis volume, yaitu anonymous volume dan named volume. Anonymous volume dibuat secara otomatis oleh Docker dengan nama acak, sedangkan named volume dibuat secara eksplisit oleh pengguna sehingga lebih mudah dikelola dan digunakan kembali. Volume ini memungkinkan data tetap tersimpan meskipun container tidak lagi berjalan.

Selain itu, Docker Volume juga memungkinkan beberapa container untuk berbagi data yang sama. Hal ini sangat berguna dalam pengembangan aplikasi yang membutuhkan pertukaran data antar layanan. Dengan menggunakan volume, efisiensi penyimpanan meningkat karena data tidak perlu diduplikasi pada setiap container.

Dengan demikian, Docker Volume menjadi komponen penting dalam pengelolaan data pada container, terutama untuk aplikasi yang membutuhkan penyimpanan data secara berkelanjutan dan dapat diakses oleh lebih dari satu container.

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
1. Persiapan Awal memastikan tidak ada container yang aktif
2. Membuat Folder Lokal (Bind Volume)
3. Menjalankan Container dengan Bind Volume
4. Membuat File di Dalam Container
5. Memeriksa Data di Host
6. Menggunakan Anonymous Volume
7. Melihat Volume yang Terbentuk
8. Berbagi Volume Antar Container
9. Membuat Named Volume
10. Menggunakan Named Volume di Container

## E. Hasil dan Pembahasan
Hasil : Docker Volume

Berikut perintah untuk melihat environment kerja :

docker info :
Menampilkan informasi detail tentang sistem Docker seperti versi, jumlah container, image, dan konfigurasi yang sedang digunakan.
![docker info](img3/docker%20info.jpg)

docker images :
Menampilkan daftar image yang tersedia di lokal, sehingga dapat diketahui image apa saja yang siap digunakan.
![docker images](img3/docker%20images.jpg)

docker ps :
Digunakan untuk melihat container yang sedang berjalan.
![docker ps](img3/docker%20ps.jpg)

docker volume ls :
Menampilkan daftar volume yang tersedia pada sistem Docker.
![docker volume ls](img3/docker%20volume%20ls.jpg)

docker system prune-a :
Digunakan untuk menghapus seluruh container, image, dan data yang tidak terpakai agar sistem bersih.
![docker system prune-a](img3/docker%20system%20prune-a.jpg)

docker volume prune :
Menghapus volume yang tidak digunakan untuk menghemat penyimpanan.
![docker volume prune](img3/docker%20volume%20prune.jpg)

docker run -it -v "/d/SEMESTER 4/Komputasi Awan (Muhammad Davi)/Komputasi Awan/docker-volume/data:/mydata" --name k1 alpine :
Menjalankan container dengan bind volume, sehingga data pada folder host dapat terhubung dengan container.
![k1 alpine](img3/k1%20alpine.jpg)

docker volume ls :
Menunjukkan adanya volume yang digunakan oleh container.
![docker volume ls](img3/docker%20volume%20ls.jpg)

docker system prune -a k1 :
Membersihkan kembali container dan volume yang sudah tidak digunakan.
![docker system prune -a k1](img3/docker%20system%20prune%20-a%20k1.jpg)

docker volume prune k1 :
Membuat container dengan anonymous volume yang disimpan otomatis oleh Docker.
![docker volume prune k1](img3/docker%20volume%20prune%20k1.jpg)

docker run-it-v /myfolder--name k2 alpine
cd /myfolder
touch f4 f5 56
ls :
Membuat container dengan anonymous volume yang disimpan otomatis oleh Docker.
![k2 alpine](img3/k2%20alpine.jpg)

docker ps k2 :
Menampilkan container aktif dan volume yang terbentuk secara otomatis.
![docker ps k2](img3/docker%20ps%20k2.jpg)

docker volume ls k2 :
Menampilkan container aktif dan volume yang terbentuk secara otomatis.
![docker volume ls k2](img3/docker%20volume%20ls%20k2.jpg)

docker run -it --volumes-from k2 --name k3 alpine
cd /myfolder :
Menggunakan volume dari container k2 ke k3, sehingga data dapat dibagikan antar container.
echo "halo dari k3 by kekeayrinda" > pesan 
cat pesan :
Membuktikan bahwa file dapat dibuat dan dibaca dalam volume yang sama.
![k3 alpine](img3/k3%20alpine.jpg)

docker run -it -v ourdata:/projectdata --name k4 alpine
cd /projectdata
echo "Ini pesan dari k4 oleh kekeayrinda" > pesan :
Menggunakan named volume agar penyimpanan lebih terstruktur dan mudah diakses.
![k4 alpine](img3/k4%20alpine.jpg)

docker run -it -v ourdata:/projectdata --name k5 alpine
k5 alpine
cd /projectdata
echo "Ini pesan dari k5" >> pesan :
Mengakses volume yang sama dari container lain dan menambahkan data.
cat pesan :
Menunjukkan bahwa data dari k4 dan k5 tersimpan dalam volume yang sama (shared data).
![k5 alpine](img3/k5%20alpine.jpg)

## F. Kesimpulan
Docker Volume berfungsi sebagai media penyimpanan data yang bersifat persisten sehingga data tidak hilang meskipun container dihentikan atau dihapus. Penggunaan bind volume, anonymous volume, dan named volume menunjukkan bahwa Docker mampu mengelola serta berbagi data antar container dengan mudah. Dengan demikian, Docker Volume sangat penting dalam mendukung pengelolaan data pada aplikasi berbasis container agar lebih efisien dan terstruktur.

## G. Analisa
Docker Volume berhasil digunakan untuk menyimpan data secara persisten serta memungkinkan berbagi data antar container. Pengujian dengan bind volume, anonymous, dan named volume menunjukkan bahwa data tetap tersimpan meskipun container dihentikan atau dihapus, serta dapat diakses oleh beberapa container. Hal ini membuktikan bahwa Docker Volume sangat membantu dalam menjaga konsistensi data dan meningkatkan efisiensi dalam pengelolaan aplikasi berbasis container.

## H. Referensi
1. Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.
2. Docker Inc. (2023). Docker Documentation. https://docs.docker.com
3. Node.js. (2023). Node.js Official Documentation. https://nodejs.org
4. Express.js. (2023). Express Framework Documentation. https://expressjs.com


<div align="center">
---

## Lembar Pengesahan


| No. Praktikum     | : | Lab 4 |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | Multi Kontainer dengan komposisi docker |
| Tanggal Praktikum | : | 16 April 2026|
| Tanggal Penyerahan| : | 23 April 2026 |
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
- [Analisa](#Analisa)
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
Hasil 5 DockerImage"node_project" :

Membuat direktori dengan perintah mkdir lalu pin
dahkedirektoritersebutdengancd(changedirectory).
mkdir node_project
![node_project & cd node_project](img2/node_project.jpg)

Cekinstalasinpmdenganperintahberikut:
![npm-v](img2/npm-v.jpg)

Selesai instalasi npm, lakukannpm init dan hasilnya sebuah file teks
![npm init-y](img2/npm%20init.jpg)

Periksa file yang terbentuk,dengan:
![ cat package.json](img2/)

Filepackage.jsonakanditambahkanmodul"express"denganperintahberikut: "npm install express"
![ npm install express](img2/npm%20install%20express.jpg)


Selanjutnya membuat sebuah file dengan nama index.js dan isi dengan kode berikut ini:
![ file index.js](img2/file%20index.js.jpg)


Mengaktifkan file index.js
![ Mengaktifkan file index.js](img2/node%20index.js.jpg)



buka di web browser dengan url http://localhost:7000
![ Mengaktifkan file tu kan](img2/output%20di%20web.jpg)


Selanjutnya  membuat Dockerfile menggunakan kode berikut ini:
![ Mengaktifkan file tu kan](img2/Docker%20File.jpg)
![ Mengaktifkan file tu kan](img2/docker%20tag.jpg)
![ Mengaktifkan file tu kan](img2/docker%20tag%20(2)![ Mengaktifkan file tu kan](imge)
)

docker push
docker run & docker ps

Selanjutnya  membuat Dockerfile menggunakan kode berikut ini:

## F. Kesimpulan

## G. Analisa

## H. Referensi
Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.



<div align="center">
---

## Lembar Pengesahan


| No. Praktikum     | : | Lab 5 |
|------------------:|:-:|:--------------|
| Judul Praktikum   | : | Judul |
| Tanggal Praktikum | : | 16 April 2026|
| Tanggal Penyerahan| : | 23 April 2026 |
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
- [Analisa](#Analisa)
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



## F. Kesimpulan

## G. Analisa

## H. Referensi
Muhammad Davi. Modul Praktikum Cloud Computing – Docker. Politeknik Negeri Lhokseumawe, 2024.
