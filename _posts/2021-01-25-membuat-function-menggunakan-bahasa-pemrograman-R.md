---
layout: post
title: Membuat function menggunakan bahasa pemrograman R
tags: [R, programming]
---
> R merupakan bahasa pemrograman untuk analisis statistik yang paling
> banyak digunakan, karena dengan menggunakan R memungkinkan kamu untuk 
> melakukan  _import_  data dari berbagai sumber  _database_  dan format
> yang berbeda. R juga memiliki 7000+ packages yang gratis untuk
> digunakan. Packages ini memungkinkan kamu untuk melakukan:
> 
> -   Analisa statistik kompleks
> -   Econometrics
> -   Optimisasi
> -   Pembuatan model machine learning
> -   Dan pembuatan teknik simulasi

*Sumber: [algorit.ma](https://algorit.ma/)*

---
Kali ini kita akan membuat *function* menggunakan bahasa pemrograman R. Di sini saya menggunakan RStudio sebagai IDE untuk menulis code dan menjalankan (*run*) *code* tersebut. 

Sama seperti bahasa pemrograman lain yang bersifat OOP, R juga memiliki struktur yang sama untuk membuat sebuah *function*. Di dalam *function* terdapat *object* sebagai penyimpan *function* dan parameter untuk menyimpan value yang akan diolah.

*Let's take a look in more simple way!*

Misalkan kita punya sebuah formula seperti berikut:

> a + (b^2) / 72

Formula itu merupakan formula sederhana, namun di sini kita tidak akan menggunakan formula tersebut hanya sekali melainkan berkali-kali. Tentu saja akan sangat melelahkan kalau kita perlu terus menerus menuliskan formula tersebut, kan? Maka dari itu kita akan memasukkan formula itu ke dalam *function* sehingga nantinya kita tidak perlu menulis formula tersebut berulang-ulang melainkan hanya perlu memanggil *function*-nya saja.   

Di dalam formula itu ada dua variable, **a** dan **b**. Variable ini akan diisi dengan angka yang tidak tentu, bisa 10, 9, 5, 100, dll. Maka dari itu kita akan membuat variable tersebut sebagai parameter di dalam *function* kita. *Function* dibuat menggunakan sintaks `function` seperti berikut: 

    functionSaya <- function(a, b) {
	    }



Sampai sini kamu sudah berhasil membuat sebuah *function*, tapi tidak ada proses di dalam *function* tersebut karena di dalam tanda kurung kurawal tidak diisi dengan apa-apa. Kita akan memasukkan formula awal kita ke dalam situ.




    functionSaya <- function(a, b) {
			a + (b^2) / 72
        }

Sekarang function kamu sudah jadi.

Tapi, tunggu. Ini belum selesai. Apa yang kurang? 🤔

Setiap *function* itu punya value hasil yang akan dikembalikan (return) ataupun dicetak (print). Dalam hal ini value hasil adalah hasil dari operasi formula ini: `a + (b^2) / 72`. Misalnya saja kita masukkan a = 1, dan b = 1 maka hasil operasi tersebut menghasilkan 1.013889. Value hasil inilah yang harus kita munculkan dari dalam *function* tersebut. Caranya menggunakan return ataupun print, seperti berikut:

    functionSaya <- function(a, b) {
      return(a + (b^2) / 72)
    }

Sekarang hasil dari operasi kita sudah bisa dimunculkan, maka *function* kita sudah benar-benar jadi. 

> **Apa bedanya return dan print dalam *function*?**
> Return mengembalikkan value hasil dari operasi sedangkan print dipakai untuk mencetak hasil. Value hasil yang dikembalikan menggunakan return bisa kita pakai lagi ke dalam operasi di luar *function*. Sedangkan kalau print hanya mencetak saja, tapi kita tidak bisa menggunakan value hasil itu ke operasi di luar *function*. **penjelesan ribet amat*

Di dalam *function* kita bisa membuat condition ataupun loop. Bahkan kita bisa memanggil *function* di dalam *function*. Intinya, *function* itu cara mudah supaya kita bisa menggunakan sebuah formula/script/algoritma berkali-kali tanpa harus menulisnya setiap kali kita mau pake. Tinggal panggil saja *function*-nya, lalu masukkan parameter maka *function* akan mengembalikkan hasil dari operasi.

Cara memanggil *function*:

    functionSaya(2,3)

 

>  ***functionSaya** itu object, sedangkan  **(2,3)** itu parameter*

---
Salah satu contoh *function* untuk menghitung *body mass index* menggunakan *condition*:

 

      bmi <- function(berat,tinggi) {
      tinggiBaru <- tinggi/100
      hasilBMI <- berat/(tinggiBaru^2)
      if (hasilBMI < 18.5) {
        return(hasilBMI)
        return("Underweight")
       } else if (hasilBMI >= 18.5 && hasilBMI <= 24.9) {
        print(hasilBMI)
        print("Normal Weight")
       } else if (hasilBMI >= 25 && hasilBMI <= 29.9) {
        print(hasilBMI)
        print("Overweight")
       } else if (hasilBMI >= 30 && hasilBMI <= 34.9) {
         print(hasilBMI)
         print("Obesity class I")
       } else if (hasilBMI >= 35 && hasilBMI <= 39.9) {
         print(hasilBMI)
         print("Obesity class II")
       } else {
         print(hasilBMI)
         print("Obesity class III") 
       }
    }

