##Rangkuman Pertemuan 8 Sistem Keamanan Jaringan
##Latar Belakang 
1.	Snort
2.	Cara Instalasi Snort Pada CentOS

##Snort
Snort adalah sebuaah sistem open source untuk pencegahan penyusupan jaringan yang mampu melakukan analisis lalu lintas jaringan secara real-time dan packet logger pada jaringan IP. Snort juga dapaat melakukan analisis protokol, konten pencarian atau pencocokan dan dapat digunakan untuk mendeteksi berbagai serangan.<br>

##Cara Instalasi Snort Pada CentOS
Sebelum menginstall snort, install dulu beberapa paket yang dibutuhkaan snort untuk berjalan.<br>
- yum install libdnet libdnet-devel pcre pcre-devel gcc make flex byacc bison kernel-devel libxml2-devel wget -y<br>
Selaanjutnya membuat direktori atau folder untuk digunakan sebagai tempat instalasi.<br>
- mkdir /usr/local/src/snort<br>
- cd /usr/local/src/snort<br>
Instaalasi Libpcap.<br>
- wget http://www.tcpdump.org/release/libpcap-1.3.0.tar.gz -O libpcap.tar.gz<br>
- tar zxvf libpcap.tar.gz<br>
- cd libpcap-*<br>
- ./configure && make && make install<br>
- echo “/usr/local/lib” >> /etc/ld.so.conf<br>
- ldconfig -v<br>
Instaalasi DAQ.<br>
- wget https://www.snort.org/downloads/snort/daq-2.0.6.tar.gz -O daq.tar.gz<br>
- tar zxvf daq.tar.gz<br>
- cd daq-*<br>
- ./configure && make && make install<br>
- ldconfig -v<br>
Buaat user dan group untuk snort.<br>
- groupadd snort<br>
- useradd -g snort snort<br>
Maasuk ke folder snort dan instalasi snort.<br>
- cd /usr/local/src/snort<br>
- wget https://www.snort.org/downloads/snort/snort-2.9.9.0.tar.gz -O snort.tar.gz<br>
- tar zxvf snort.tar.gz<br>
- cd snort-2*<br>
- ./configure –prefix /usr/local/snort –enable-sourcefire && make && make install<br>

##Kesimpulan
Jadi, snort adalah sebuah sistem open source untuk pencegahan penyusupan jaringan yang mampu melakukan analisis lalu lintas jaringan secara real-time dan packet logger pada jaringan IP.

##Saran
Untuk memaahami lebih jelasnya alangkah lebih baiknya jika kita mencari di buku-buku yang terpercaya atau melakukan praktikum mandiri.

-------

•	Nama : Entol Achmad Fikry Ilhamy<br>
•	NPM : 1144115
•	Kelas : 3C<br>
•	Prodi : D4 Teknik Informatika
•	Kampus : Politeknik Pos Indonesia<br>

-------

Link Matakuliah : http://kampus.awangga.net/assignments/keamananjaringan2016<br>
Link Github : https://github.com/enfikry25/SistemKeamananJaringan

##Referensi :
•	https://siswandapratama12tkj2.wordpress.com/2014/10/20/firewall-pengertian-fungsi-manfaat-dan-cara-kerja-firewall/

##Scan Plagiarisme :
•	https://drive.google.com/open?id=0B5FSMUsdCMU4Nk5KajE0bkozVkE<br>
•	https://drive.google.com/open?id=0B5FSMUsdCMU4T1d2elFLeFZSTk0
