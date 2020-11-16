---
layout: post
title: Cara Membuat Virtual Environtment Python
tags: [python]
---
Akhir-akhir ini saya lagi sering menggunakan Python untuk mengerjakan proyek machine learning. Akhir-akhir ini juga, saya baru *ngeh* dengan pentingnya menggunakan virtual environtment saat mengerjakan sebuah proyek di Python. 

![Drake's Meme](https://i.imgflip.com/4miuom.jpg)

Iya, saya berdosa, selama ini saya tidak pernah menggunakan virtual environtment saat mengerjakan sebuah proyek. 😓 #KesalahanPemula

Sebelum saya menjelaskan betapa pentingnya virtual environtment, saya akan langsung menunjukkan bagaimana cara setting virtual environtmentnya (biar gak banyak basa-basi).

## Cara Setting Virtual Environtment Python
Di sini saya menggunakan OS Windows dan Anaconda Distribution untuk menginstall Python dan packages defaultnya.

1. Buka Anaconda Prompt ataupun PowerShell (cmd). Setelah itu ketik `conda create -n namaenvirontmentnya python=3.7`.

![Step 1](https://i.ibb.co/NZ6f1Df/1605494548898.jpg)
> *namaenvirontmentnya* diganti sesuai nama environtment yang kamu inginkan

3. Setelah itu conda akan memproses untuk membuat virtual environtment baru. Pilih `y` kalau ada perintah `Proceed ([y]/n)?`

![Step 2](https://i.ibb.co/jTYLC4v/1605494596869.jpg)

4. Kalau tidak ada pesan error, berarti virtual environtment sudah berhasil dibuat. Coba aktifkan virtual environtment tersebut dengan mengetik `conda activate namaenvirontmentnya`.

![Step 3](https://i.ibb.co/FJ3bkTY/1605494666661.jpg)

5. Untuk melihat keseluruhan packages yang terinstall di dalam virtual environtment tersebut, ketik `conda list`.

![Step 4](https://i.ibb.co/MsxKL43/1605494690118.jpg)

> Packages yang terinstall hanya default packages dari Python.

5. Kalau sudah selesai menggunakan virtual environtment, ketik `conda deactivate`.

Sampai tahap ini kamu sudah berhasil membuat dan mencoba menggunakan virtual environtment di Python.

#### Mengapa virtual environtment di Python sangatlah penting?

Begini, coba bayangkan kamu ingin membuat sebuah aplikasi web berbasis Python menggunakan `Flask 1.0.2` lalu dikemudian hari kamu ingin mendeploy sebuah model machine learning ke dalam aplikasi web menggunakan Flask juga tapi dengan versi yang terbaru, `Flask 1.1.2`.

Kamu punya dua pilihan, yaitu yang pertama update `Flask 1.1.2` untuk mendeploy proyek machine learning, lalu kalau dibutuhkan kamu bisa downgrade ke `Flask 1.0.2` lagi kalau ingin melanjutkan pengerjaan aplikasi web yang sebelumnya.

Apakah cara pertama ini efisien? Tentu saja tidak.

Virtual environtment menawarkan sistem di mana kita bisa mempunyai environtment khusus untuk setiap proyek yang sedang kita kerjakan sehingga kita bisa punya dua atau lebih versi packages tanpa mengganggu packages untuk proyek yang lainnya.

Jadi kamu tidak perlu downgrade-upgrade packages setiap ingin bekerja dengan versi packages yang berbeda.

##### Issues
> Jika kamu menggunakan Anaconda Distribution, biasanya kamu akan menemukan masalah ketika ingin switching environtment. Solusinya adalah kamu bisa menginstall `nb_conda` sebagai ekstensi tambahan untuk switching antar environtment di Jupyter Notebook.
