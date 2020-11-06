---
layout: post
title: Praktek Web Dasar (HTML & CSS)
share-img: https://cdn.mos.cms.futurecdn.net/hFm4iWXhbw4c4rdcMH8tUD.jpg
tags: [html, css]
---
**HTML** adalah singkatan dari HyperText Markup Languange yang merupakan bahasa pemrograman web atau *markup* internet yang berasal dari kombinasi antara teks dan informasi berupa simbol atau kode yang akan dimasukan ke dalam suatu file guna membuat suatu halaman situs web.  

Sedangkan, **CSS** adalah bahasa Cascading Style Sheet dan biasanya digunakan untuk mengatur tampilan elemen yang tertulis dalam [bahasa *markup*](https://techterms.com/definition/markup_language), seperti HTML, XML, KML, MathML. CSS berfungsi untuk memisahkan konten dari tampilan visualnya di situs.

Pada praktek kali ini, diperlukan sebuah text editor, teman-teman bisa menggunakan Visual Studio Code, Sublime Text, Notepad++, Atom atau yang lainnya. Jika ingin text editor yang lebih ringan, teman-teman bisa menggunakan Notepad++ atau Sublime Text. Namun kalau ingin lebih advanced, bisa menggunakan Visual Studio Code ataupun Atom.

Saya memilih untuk menggunakan Visual Studio Code. (Untuk link download bisa dicari di Google)

## Praktikum
1. Buatlah judul dari halaman tersebut dengan nama “LATIHAN [NIM] [NAMA]” 

2. Buatlah isi seperti pada gambar dengan pengaturan seperti berikut: 	
a. **Lebar TABLE sebesar 500px, ukuran teks dalam tabel sebesar 20pt.** 
b. **“Tabel Mahasiswa NIM NAMA” : h1 , teks berwarna hijau, jenis huruf consolas.** 
c. **Judul tabel memiliki warna teks biru dan warna background hijau muda (kalian bisa mencari warna dengan mengakses w3school.com)**
d. **Isilah tabel minimal 10 anggota teman sekelas Anda! Dan ubahlah background warna dari isi tabel menjadi warna biru muda seperti pada gambar!**

3. Buatlah konten berita sederhana (hanya berupa teks sederhana saja, jika ingin masukkan gambar lebih bagus) dengan konfigurasi berikut! 
a. **JUDUL BERITA : bisa ditekan dan mempunyai link, jika diklik akan mendirect website berita yang anda pilih** 
b. **ISI BERITA : buatlah teks singkat mengenai berita tersebut. Ceritakanlah kembali isi dari berita (bukan copy paste)**

Pertama, buka text editor kalian lalu buat file baru. Kita akan menggunakan HTML versi 5, maka kita perlu menambahkan sintaks `<!DOCTYPE html>` di awalan dokumen. Sintaks ini akan memberi tahu browser bahwa file HTML kita menggunakan HTML 5.

Selanjutnya, untuk membuat judul website kita menggunakan sintaks `<title> judulwebdisini </title>`. Setelah itu kita akan memasukkan sebuah teks ke dalam website tersebut, kita bisa menggunkaan sintaks `<h1> teksdisini </h1>`. Kira-kira script kita sudah jadi seperti ini:
```html
<!DOCTYPE  html>
<head>
	<title>latihanjericho32932</title>
</head>
<body>
	<h1>Tabel Mahasiswa 32932 Jericho</h1>
</body>
```
`<head>` digunakan untuk memberitahu bahwa di bagian ini merupakan tempat judul dari website, sedangkan `<body>` digunakan untuk memberitahu bahwa ini bagian isi dari website.

Untuk melihat tampilan website, simpan file tersebut dengan format `.html` lalu coba buka dengan browsermu. Hasilnya kira-kira akan seperti ini:

![gini tampilan awal](/assets/img/tampilanawal.gif)

Sekarang kita akan membuat sebuah tabel. Pada dasarnya tabel terdiri atas 3 komponen, yaitu kolom, baris dan data. Pertama kita akan membuat kolom atau bisa disebut sebagai *table head*, kita bisa menggunakan sintaks `<thead>`. Penggunaanya seperti ini:
```html
<table>
	<thead>
		<tr>
			<th>NIM</th>
			<th>Nama</th>
		</tr>
	</thead>
</table>
```
Sintaks `<table>` merupakan sintaks yang mendefine tabel kita, lalu di dalamnya terdapat sintaks `<thead>` untuk memberitahu bahwa ini merupakan bagian kepala tabel/kolom/row paling atas. Lalu di dalamnya ada sintaks `<tr>` untuk memberitahu bahwa ini merupakan baris lalu ada `<th>` untuk memastikan bahwa baris ini merupakan kepala dari tabel ini/row paling atas/judul kolomnya.

Sebenarnya sintaks untuk membuat judul kolom di atas bisa dipersingkat seperti ini:
```html
<table>
	<thead>
		<th>NIM</th>
		<th>Nama</th>
	</thead>
<table>
``` 
Ataupun seperti ini:
```html
<table>
	<tr>
		<th>NIM</th>
		<th>Nama</th>
	</tr>
</table>
```
Namun di sini kita akan mengikuti cara yang sudah tertera dalam modul ISIT. Selanjutnya kita akan membuat row di bawah judul kolom yang sudah kita buat sebelumnya dan memasukkan data ke dalamnya. Kita akan menggunakan sintaks `<tr>` untuk membuat row dan `<td>` untuk memasukkan data, seperti ini (script ini masih jadi satu dengan sintaks `<table>`:
```html
<table>
	<thead>
		<tr>
			<th>NIM</th>
			<th>Nama</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>32932</td>
			<td>Jericho Siahaya</td>
		</tr>
	</tbody>
</table>
```
Setelah itu, kita akan membuat sebuah berita dengan judul dan paragraf. Untuk membuat judulnya kita akan memasukkan link sehingga teksnya dapat diklik, kita bisa menggunakan sintaks `<a href="">` seperti ini:
```html
<a  href="namawebsitenyadisini.com"><h2>Judul Berita</h2></a>
```
Setelah itu kita akan membuat paragrafnya menggunakan sintaks `p` seperti ini:
```html
<p> Di sini buat isi paragraf </p>
```
Setelah berhasil membuat berita serta tabel maka bentuk keseluruhan script kita akan jadi seperti ini:
```html
<!DOCTYPE  html>
<head>
	<title>latihanjericho32932</title>
</head>
<body>
<h1>Tabel Mahasiswa 32932 Jericho</h1>
<table>
	<thead>
		<tr>
			<th>NIM</th>
			<th>Nama</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>32932</td>
			<td>Jericho Siahaya</td>
		</tr>
	</tbody>
</table>
<a  href="namawebsitenyadisini.com"><h2>Judul Berita</h2></a>
<p> Di sini buat isi paragraf </p>
</body>
```
Tampilan website akan seperti ini:

![tampilan website jadi seperti ini](/assets/img/tampilanwebsiteakanjadisepertiini.jpg)


Tahap selanjutnya kita akan memberi visualisasi atau *style* pada website yang sebelumnya sudah kita buat menggunakan CSS. Perlu diketahui, pemberian *style* menggunakan CSS bisa memakai teknik [external, inline dan internal CSS](https://www.hostinger.co.id/tutorial/perbedaan-inline-css-external-css-dan-internal-css/). 

Di sini kita akan mencoba menggunakan internal CSS, sehingga kita perlu menambahkan sintaks `<style>` di dalam bagian sintaks `<head>` yang sebelumnya sudah dibuat, seperti ini:  
```html
<!DOCTYPE  HTML>
<head>
	<title>latihanjericho32932</title>
<style>

</style>
</head>
```

Pertama kita akan menambahkan garis pada tabel dan mengubah lebar tabel menjadi 500px lalu mengubah seluruh ukuran teks yang berada di dalam tabel menjadi 20pt. Di dalam sintaks `<style>` kita taruh script CSS berikut ini:
```html
table {
	width: 500px;
	border: 3px  dashed  black;
	font-size: 20pt;
	}

td {
	border: 1px  dashed  black;
	}

th {
	border: 2px  dashed  black;
	background-color: #99ffff;
	}

tr {
	background-color: #ccff99;
	}
```
Di sini kita tidak menggunakan class, tapi teman-teman bisa mencoba menggunakan class dengan cara memberi tambahan perintah `class="namaclass"` pada salah satu sintaks yang ingin diberi *style*. 

Langkah selanjutnya kita akan memberi warna biru dan mengubah font menjadi Consolas pada teks judul kolom. Kita bisa menambahkan perintah `color: blue;` dan `font-family: Consolas;` pada *style* `th` yang sudah kita buat sebelumnya, sehingga jadi seperti ini:
```html
th {
	border: 2px  dashed  black;
	background-color: #99ffff;
	color: blue;
	font-family: Consolas;
}
```
Sampai di sini, tabel kita sudah selesai dibuat. Mungkin untuk lebih rapi, kita bisa membuat teks dalam tabel agar rata tengah dengan menambahkan perintah `text-align: center;` pada *style* `table`.

Terakhir kita akan mengubah font dan warna pada judul teks paling atas. Kita akan coba menggunakan class, pertama kita tambahkan perintah `class="namaclass"` pada sintaks `<h1>` yang sudah kita buat sebelumnya sehingga menjadi seperti ini:
```html
<h1 class="judul">Tabel Mahasiswa 32932 Jericho</h1>
```
Setelah itu kita panggil nama class tersebut di dalam bagian sintaks `<style>` kita, seperti ini:
```html
.judul {
	font-family: Consolas;
	color: green;
}
```
*Note: kita menggunakan awalan titik untuk memanggil nama class dalam style*

Maka keseluruhan *style* kita akan jadi seperti ini:
```html
table {
	width: 500px;
	border: 3px  dashed  black;
	font-size: 20pt;
	text-align: center;
	}

td {
	border: 1px  dashed  black;
	}

th {
	border: 2px  dashed  black;
	background-color: #99ffff;
	color: blue;
	font-family: Consolas;
	}

tr {
	background-color: #ccff99;
	}
	
.judul {
	font-family: Consolas;
	color: green;
	}
```
Sampai di sini website kita sudah diberi visualisasi dan sudah jadi. Keseluruhan script akan terlihat seperti ini:
```html
<!DOCTYPE  html>
<head>
	<title>latihanjericho32932</title>
	<style>
	table {
	width: 500px;
	border: 3px  dashed  black;
	font-size: 20pt;
	text-align: center;
	}

	td {
	border: 1px  dashed  black;
	}

	th {
	border: 2px  dashed  black;
	background-color: #99ffff;
	color: blue;
	font-family: Consolas;
	}

	tr {
	background-color: #ccff99;
	}
	
	.judul {
	font-family: Consolas;
	color: green;
	}
	</style>
</head>
<body>
<h1 class="judul">Tabel Mahasiswa 32932 Jericho</h1>
<table>
	<thead>
		<tr>
			<th>NIM</th>
			<th>Nama</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>32932</td>
			<td>Jericho Siahaya</td>
		</tr>
	</tbody>
</table>
<a  href="namawebsitenyadisini.com"><h2>Judul Berita</h2></a>
<p> Di sini buat isi paragraf </p>
</body>
</html>
```
![foto website](/assets/img/hasilakhir.jpg)

### Need To Know

 - Indensasi/spasi/tab pada HTML ataupun CSS tidak berpengaruh terhadap outputnya, ini dilakukan hanya untuk mempermudah membaca kodingan.
 - `thead` dan `tbody` bisa digunakan, bisa juga tidak digunakan, tergantung keperluan.
 - Pemberian CSS bisa menggunakan teknik inline, internal, dan external. Inline lebih memerlukan banyak waktu dikarenakan harus menulis perintah satu-satu di setiap sintaks.

Sekian.

![oke, ngerti kan](https://i.imgur.com/tqH5lLX.gif)
