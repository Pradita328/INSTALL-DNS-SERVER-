# INSTALL-DNS-SERVER-

1.	Login ke debian dengan menggunakan user root dan setelah itu kita setting IP untuk server terlebih dahulu dengan mengetikkan perintah nano /etc/network/interfaces
2.	Jika sudah, restart IP dengan perintah /etc/init.d/networking restart. Dan cek konfigurasi IP sudah berhasil atau belum dengan perintah ip a.
3.	Jika berhasil, maka langkah selanjutnya masukkan DVD 2 dan install bind9, dengan perintah apt-get install bind9. Jika ada pertanyaan [y/n] klik Y kemudian enter
4.	Jika terjadi error seperti gambar dibawah ini, jangan panik. Kita ketikkan perintah apt --fix-broken install. Tetapi jika tidak ada berarti instalasi berhasil.
Kemudian ada perintah untuk memasukkan DVD binary 1 seperti gambar dibawah ini, masukkan DVD binary 1 kemudian enter.
6.	 Untuk memastikan instalasi sudah berhasil atau belum kita ketikkan ulang perintah apt-get insatll bind9. Jika ada keterangan 0 upgrade, 0 newly installed, 0 to remove and 0 not upgraded. Seperti gambar dibawah ini berarti instalasi telah berhasil.
7.	Kemudian masuk ke directory bind dengan perintah cd /etc/bind. 
Berikut file-file penting yang akan kita konfigurasi dalam DNS Server
a.	File forward
b.	File reverse
c.	named.conf.options
d.	named.conf.local
e.	/etc/resolv.confl
8.	Membuat file forward, dengan cara copy file db.local dengan perintah cp db.local db.tkj. kemudian konfigurasi file db.tkj dengan perintah nano db.tkj. Lakukan konfigurasi seperti gambar dibawah ini.
File forward berfungsi untuk konversi dari DNS menjadi IP Address. Misalnya www.tkj.com melalui Web Browser, maka akan muncul website dari server debian.
