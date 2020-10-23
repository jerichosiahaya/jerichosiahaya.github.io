---
layout: post
title: Praktek MySQL Untuk Pemula
share-img: https://logos-download.com/wp-content/uploads/2016/05/MySQL_logo_logotype.png
tags: [mysql, database]
---

MySQL adalah salah satu aplikasi **RDBMS (Relational Database Management System)** atau sistem manajemen basis data yang menggunakan prinsip relasional (setiap tabel saling terhubung dan memiliki relasi). 

Pada praktek kali ini kita akan menggunakan Laragon sebagai *local development enviroment*. Teman-teman juga bisa menggunakan XAMPP, WampServer ataupun aplikasi pengembangan *web server* lainnya yang mendukung basis data MySQL.

### Instalasi Laragon

Aplikasi Laragon dapat diunduh di sini: https://laragon.org/download/index.html. Instalasi Laragon cukup mudah, setelah selesai diunduh teman-teman bisa langsung menjalankan aplikasi Laragon. Setelah itu akan muncul setup seperti demikian:

![0_1513170555874_setup 01.png](https://i.imgur.com/4OyDDhK.png)

Teman-teman bisa memilih direktori instalasi (defaultnya di C):

![0_1513170575695_02-location.png](https://i.imgur.com/sJK59DC.png)

![0_1513170587611_03-options.png](https://i.imgur.com/8oZ4N8E.png)

Next, next, next, kemudian selanjutnya Laragon siap digunakan.

### Latihan Praktikum

1. Buatlah sebuah database dengan format nama database DB_NIM_NAMA 
2. Buatlah sebuah tabel pada database Anda dengan tabel bernama TABEL_NILAI 
3. Pada tabel TABEL_NILAI buatlah fields sebagai berikut : 
	- NIM ‐> Varchar(11) 
	- NAMA ‐> Varchar(50) 
	- TUGAS ‐> integer 
	- UTS ‐> integer 
	- UAS ‐> integer 
	- Nilai_akhir ‐> integer 
	- Nilai_akhir adalah hasil perhitungan dari 30%*TUGAS + 30%*UTS + 40%*UAS

Pertama-tama, buka Aplikasi Laragon, lalu klik *Start All*.

![FOTO](assets/img/mysql1.jpg)

Pastikan status Apache dan MySQL berjalan dengan lancar.

![FOTO](assets/img/mysql2.jpg)

Setelah itu, klik *Terminal*. Laragon sudah menyediakan cmd khusus jadi kita tidak perlu membuka cmd yang ada di komputer kita.

![FOTO](assets/img/mysql3.jpg)

Tampilan awal terminal Laragon akan terlihat seperti ini.

![FOTO](assets/img/mysql4.jpg)

Untuk melakukan login ke dalam MySQL kita menggunakan *script*:
```mysql
mysql -u root -h localhost
```
Setelah itu akan muncul teks seperti ini:

![FOTO](assets/img/mysql5.jpg)

#### Membuat Database

Setelah itu kita akan membuat database baru menggunakan perintah **CREATE DATABASE** seperti ini:
```
create database DB_32932_Jericho;
```
*Catatan: selalu gunakan semicolon (titik-koma) untuk mengakhiri sebuah perintah/script*
#### Menggunakan Database
Sebelum membuat tabel ataupun memodifikasi database yang telah dibuat, kita perlu memilih database tersebut, menggunakan perintah **USE** seperti ini:
```
use DB_32932_Jericho;
```

#### Membuat Tabel
Setelah database telah dibuat, kemudian kita akan membuat tabel di dalam database tersebut menggunakan perintah **CREATE TABLE** seperti ini:
```
create table tabel_nilai (nim varchar(11), nama varchar(50), tugas int, uts int, uas int, nilai_akhir int);
```
#### Memasukkan Data
Setelah tabel dibuat, lalu kita akan memasukkan data pada tabel sesuai ketentuan yang telah kita buat pada field-fieldnya (varchar, int, dll). Untuk memasukkan data kita menggunakan perintah **INSERT INTO [nama tabel] VALUES [data]** seperti ini:
```
insert into tabel_nilai values ('32666','Ricky Ng',90,85,80,(tugas*0.3+uts*0.3+uas*0.4));
```
Pada perintah di atas kita memasukkan data mengikuti urutan field yang telah kita buat  sebelumnya. Kita juga bisa memasukkan data sesuai urutan field yang kita mau, seperti ini:
```
insert into tabel_nilai (nama, nim, uas, uts, tugas, nilai_akhir) values ('Dicky Sanjaya','32000',80,85,90,(tugas*0.3+uts*0.3+uas*0.4));
```
Hasil dari proses di atas adalah sebagai berikut:

![FOTO](assets/img/mysql6.jpg)

### Perintah MySQL Lainnya

#### Melihat Seluruh Database
```
show databases;
```
#### Melihat Seluruh Tabel Pada Sebuah Database
```
show tables;
```
#### Melihat Seluruh Data Pada Sebuah Tabel
```
select * from [nama_tabel];
```
#### Melihat Beberapa Data Pada Sebuah Tabel
```
select (nama_field_A,nama_field_B,nama_field_C) from [nama_tabel];
```
*Catatan: field = nama kolom*
#### Mengubah Data
```
update [nama_tabel] set [nama_field_B] = nilai yang diinginkan where [nama_field_A] = masukkan parameter di sini;
```
#### Menghapus Data
```
delete from [nama_tabel] where [nama_field] = masukkan parameter di sini;
```
Untuk lebih lengkapnya dapat dicek pada dokumentasi di situs resmi MySQL di sini: https://dev.mysql.com/doc/refman/8.0/en/sql-statements.html
