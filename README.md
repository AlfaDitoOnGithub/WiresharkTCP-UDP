
# JARKOM 2023 Hands-On TCP&UDP

Alfadito Aulia Denova (5025211157 - Teknik Informatika ITS)



## TCP
Hasil jawaban soal menggunakan file yang diberikan yaitu tcp-wireshark-trace1-1

![gambar1](TCPUDPSS/ss(4).png)
1. IP address client adalah 192.168.86.68 dan port TCP adalah 55639
2. IP address gaia.cs.umass.edu adalah 128.119.245.12 dan port penerimaannya adalah 80
3. Seq number untuk TCP SYN adalah 4236649187, terdapat flags 0x002 (SYN) yang menandakan TCP ini sebagai SYN. seharusnya karena terdapat flags, maka bisa melakukan selective
![gambar2](TCPUDPSS/ss(5).png)
4. Seq number di SYN ACK adalah 1068969752, terdapat flag 0x012 (SYN, ACK), ack numbernya 1 dengan rawnya adalah 4236649188,yang merupakan seq number SYN +1.
![gambar3](TCPUDPSS/ss(6).png)
5. sequence number relative 153426, dengan raw 4236801228. ukuran file keseluruhan adalah 153425 bytes. yang terbagi menjadi 106 tcp yang berbeda masing-masing berisi 1448 bytes dan 1385 bytes untuk tcp yang terakhir.
6.  - time untuk HTTP dengan POST adalah 0.147682
    - time untuk ACK pertamanya adalah 0.149626
    - rtt nya adalah 0.001944
    - rtt untuk ack kedua adalah 0.000003
    - Estimated RTT nya adalah 0.1926
7. length totalnya adalah header 32 bytes + payload 1448 bytes = 1480 bytes
8. ukurannya adalah 131712 * 64 = 8429568
9. jika ada checksum yang sama memungkinkan bahwa packet tersebut merupakan retransmitted
10. ukuran yang kurang dari 1500 bytes
![gambar4](TCPUDPSS/ss(7).png)
11. kecepatan transfernya adalah 153425 bytes / 0.123635 detik didapat dari awal mula TCP yang melakukan transfer, frame 4 sampai pada HTTP POST nya frame 153. nilai akhirnya adalah 1,240,951.186961621 bytes/detik
![gambar5](TCPUDPSS/ss(11).png)
![gambar6](TCPUDPSS/ss(12).png)
13. pada beberapa point t, terdapat rangkaian packet yang dikirim bersamaan. terlihat padat dan ter congested. 
14. Periode yang dimiliki oleh pengirim TCP belum dipelajari
15. tidak memakai punya sendiri karena banyaknya noise

## UDP

Sesuai dengan permintaan adalah melakukan nslookup ke sebuah web.
![gambar7](TCPUDPSS/ss(13).png)
![gambar8](TCPUDPSS/ss(14).png)
![gambar9](TCPUDPSS/ss(15).png)
![gambar4](TCPUDPSS/ss(16).png)
1. packet number untuk UDP pertama yang muncul adalah 10. membawa sebuah data 84 bytes yang tampak tidak beraturan. hanya ada field UDP dan juga data yang dibawanya
2. UDP tidak memiliki header fields secara explisit, namun data yang diterima terdapat sebuah payload dan data lainnya (header), untuk yang satu payloadnya 84 bytes dan headernya 42 bytes, dan yang satunya payload 36 bytes dan header 42 bytes. maka header dari UDP berukuran 42 bytes
3. data payload plus sebuah data info
4. kurang dari 128 bytes
5. port yang bisa digunakan 54962 untuk kasus ini
6. 17
7. UDP pertama 10, UDP replynya 11, src port untuk pengirim menjadi dst port pada reply.
