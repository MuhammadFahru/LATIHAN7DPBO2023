# Latihan 7 Praktikum DPBO

## Janji

Bismillah Saya Muhammad Fahru Rozi [2108927] mengerjakan soal Latihan Praktikum 7 dalam mata kuliah Desain Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Data Diri

- 2108927
- Muhammad Fahru Rozi
- Ilmu Komputer C1'21
- Universitas Pendidikan Indonesia

## Desain Program

Dari code program yang disediakan saya hanya menambahkan satu class yaitu **Target.java** untuk membuat sebuah kotak yang dijadikan target sehingga player bisa hit untuk mendapatkan score.

## Penjelasan Alur

1. Setiap **Player** bergerak, maka Score Move +1 dengan syarat movement sebelumnya tidak boleh sama dengan movement yang akan dilakukan. Contoh: kanan -> kanan +0 score karena bergerak ke arah yang sama berurutan. Dalam code program pada **Controller.java** saya membuat variable integer baru yaitu lastDirection untuk menyimpan tanda arah manakah yang menjadi pergerakan terkahir player. Untuk tanda nya saya set 1 = UP, 2 = LEFT, 3 = DOWN, 4 = RIGHT. Saya juga menambahkan handling jika key ditekan dan dihold maka Score Move akan tetap +1 dengan cara menambah variable boolean baru yaitu keyPressed, variable ini berfungsi sebagai tanda apakah key sudah *released* atau masih dalam keadaan *pressed*.
2. Saya menambahkan class **Target.java** untuk membuat sebuah kotak yang dijadikan target sehingga player bisa hit target tersebut dan mendapatkan Score Hit. Tiap player menabrak/hit target tersebut maka Score Hit +5. Untuk code program nya saya membuatnya kurang lebih sama dengan class **Player.java**, tetapi karena ada object baru ini saya menyesuaikannya di beberapa file yaitu pada **Game.java** pada function *constructor* saya menambahkan untuk spawn Target dengan posisi random. Pada **GameObject.java** saya membuat function baru yaitu *setRandomPos* untuk generate random position yang digunakan pada object Target. Pada class **Handler.java** saya menambahkan function *hit* yang mengembalikan nilai boolean untuk mendeteksi apakah object Player melakukan hit/tabrakan pada object Target, function ini mengecek apakah posisi player dan target sama atau tidak. Saat Player bergerakan untuk melakukan hit/tabrakan pada Target, posisinya kadang tidak benar-benar sama jadi saya memberikan kondisi space perkiraan sekitar 20 an pada pengecekan titik kordinat kedua object tersebut.

## Dokumentasi

https://user-images.githubusercontent.com/59097913/234334742-5ce8cbe1-d678-49af-8cd8-7d45320fad40.mp4

https://user-images.githubusercontent.com/59097913/234334774-e50e2e6f-5aa5-4581-884d-7278afdc9a95.mp4
