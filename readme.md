# Latihan1

Pada tutorial Git yang kedua, kita sudah membuat repositori kosong. Belum ada apa-apa di sana.

Sekarang coba tambahkan sebuah file baru.

Sebagai contoh, saya akan menambahkan tiga file HTML kosong.

Project 01 - repository Git

Setalah ditambahkan, coba ketik perintah git status untuk melihat status repositorinya.

Git status

Berdasarkan keterangan di atas, saat ini kita berada cabang (branch) master dan ada tiga file yang belum ditambahkan ke Git.


 
Tiga Kelompok Kondisi File dalam Git
Sebelum kita membuat revisi, kita akan berkenalan dulu dengan tiga kondisi file dalam Git.

1. Modified
Modified adalah kondisi dimana revisi atau perubahan sudah dilakukan, tetapi belum ditandai dan belum disimpan di version control. Contohnya pada gambar di atas, ada tiga file HTML yang dalam kondisi modified.

2. Staged
Staged adalah kondisi dimana revisi sudah ditandai, tetapi belum disimpan di version control. Untuk mengubah kondisi file dari modified ke staged gunakan perintah git add nama_file. Contoh:

git add index.html
3. Commited
Commited adalah kondisi dimana revisi sudah disimpan di version control. perintah untuk mengubah kondisi file dari staged ke commited adalah git commit.

Membuat Revisi Pertama
Baiklah, sekarang kita akan sudah tahu kondisi-kondisi file dalam Git. Selanjutnya, silahkan ubah kondisi tiga file HTML tadi menjadi staged dengan perintah git add.

git add index.html
git add about.html
git add contact.html
Atau kita bisa melakukannya seperti ini:

git add index.html about.html contect.html
atau:

git add *.html
Atau seperti ini (semua file dan direktori):

git add .
Setelah itu, cobalah ketik perintah git status lagi. Kondisi filenya sekarang akan menjadi staged.

Kondisi file staged di Git

Setelah itu, ubah kondisi file tersebut ke commited agar semua perubahan disimpan oleh Git.

git commit -m "Commit pertama"
Setelah itu, coba cek dengan perintah git status lagi.

Commit pertama git

Selamat, revisi pertama sudah kita buat. Selanjutnya cobalah untuk membuat revisi kedua.

Membuat Revisi kedua
Ceritanya ada perubahan yang akan kita lakukan pada file index.html. Silahkan modifikasi isi file index.html. Sebagai contoh saya mengisinya seperti ini.

<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Belajar Git - Project 01</title>
    </head>
    <body>
        <p>Hello Semua, Saya sedang belajar Git</p>
    </body>
</html>
Setelah itu ketik lagi perintah git status.

Git status revisi kedua

Terilhat di sana, file index.html sudah dimodifikasi. Kondisinya skarang berada dalam modified. Lakukan commit lagi seperti revisi pertama.

git add index.html
git commit -m "ditambahkan isi"
Dengan demikian, revisi kedua sudah disipan oleh Git. Mungkin anda belum tahu maksud dari argumen -m, argumen tersebut untuk menambahkan pesan setiap menyimpan revisi.

Timeline dua revisi

Sekarang Git sudah mencatat dua revisi yang sudah kita lakukan. Kita bisa ibaratkan revisi-revisi ini sebagai checkpoint pada Game. Apabila nanti ada kesalahan, kita bisa kembali ke checkpoint ini.