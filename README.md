## SQL Praktikum 4 

Nama: Alifia Ananda Putri

Nim: 312210168

Kelas: TI.22.A2

## Query Filtering

Query filtering mengacu pada proses memfilter atau membatasi data yang diambil dari database berdasarkan kriteria tertentu. Dalam konteks basis data, query filtering melibatkan penggunaan klausa "WHERE" dalam perintah SQL untuk mengatur kondisi atau kriteria yang harus dipenuhi oleh data yang ingin diambil.

Dengan menggunakan query filtering, Anda dapat menentukan kondisi seperti kesamaan, ketidaksamaan, rentang nilai, atau kombinasi kondisi lainnya untuk memilih subset data yang relevan dari tabel. Ini membantu Anda memfokuskan pada data yang spesifik atau memenuhi persyaratan tertentu.

## Tugas Praktikum 1


![gambar1](ss/tp1.png)


Sebelumnya buatlah tabel pegawai seperti gambar berikut


![gambar2](ss/fi1.png)


1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000!

perintah:

SELECT * FROM pegawai WHERE gaji <> 2000000 AND gaji <> 1250000;

Output:


![gambar3](ss/fi2.png)


2. Tampilkan pegawai yang tunjangannya NUL!

perintah:

SELECT * FROM pegawai WHERE tunjangan IS NULL;


output:


![gambar4](ss/fi3.png)


3. Tampilkan pegawai yang tunjangannya tidak NULL!

Perintah:

SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;

Output:


![gambar5](ss/fi4.png)


4. Tampilkan/hitung jumlah baris/record tabel pegawai!

Perintah:

SELECT COUNT(*) AS jumlah_baris FROM pegawai;

Output:


![gambar6](ss/fi5.png)


5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

Perintah:

SELECT SUM(gaji) AS total_gaji FROM pegawai;

Output:


![gambar7](ss/fi6.png)


6. Tampilkan/hitung jumlah rata-rata gaji pegawai!

Perintah:

SELECT AVG(gaji) AS rata_gaji FROM pegawai

Output:


![gambar8](ss/fi7.png)


7. Tampilkan gaji terkecil!

Perintah:

SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;

Output:


![gambar9](ss/fi8.png)


8. Tampilkan gaji terbesar!

Perintah:

SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;

Output:


![gambar10](ss/fi9.png)


## Tugas Praktikum 2


![gambar11](ss/tp2.png)


Sebelumnya buatlah tabel pegawai seperti gambar berikut


![gambar12](ss/fi10.png)


1. Tampilkan jumlah hewan yang dimiliki setiap owner!

Perintah:

SELECT owner, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY owner;

Output:


![gambar13](ss/fi11.png)


2. Tampilkan jumlah hewan berdasarkan spesies!

Perintah:

SELECT species, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species;

Output:


![gambar14](ss/fi12.png)


3. Tampilkan jumlah hewan berdasarkan jenis kelamin!

Perintah:

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY sex;

Output:


![gambar15](ss/fi13.png)


4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin!

Perintah:

SELECT species,sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species,sex;

Output:


![gambar16](ss/fi14.png)


5. Tampilkan jumlah hewan berdasarkan spesies (cat dan dog saja) dan jenis kelamin!

Perintah:

SELECT species,sex, COUNT(*) AS jumlah_hewan FROM hewan
WHERE species IN('Cat','Dog')
GROUP BY species,sex;

Output:


![gambar17](ss/fi15.png)


6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja!

Perintah:

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan
WHERE sex IN('f','m')
GROUP BY sex;

Output:


![gambar18](ss/fi16.png)


## Evaluasi dan Pertanyaan

. Tulis semua perintah-perintah SQL percobaan di atas besarta outputnya!

. Beri kesimpulan anda!

## Kesimpulan

Query filtering adalah proses menyaring atau memfilter data dari basis data berdasarkan kriteria tertentu menggunakan perintah query dalam bahasa SQL. Tujuan utama dari query filtering adalah membatasi atau mengambil subset data yang sesuai dengan kondisi yang ditentukan.
Dengan menggunakan query filtering, Anda dapat menentukan berbagai jenis kondisi seperti kesamaan (equal), ketidaksamaan (not equal), rentang nilai (range), kondisi logis (AND, OR), atau kombinasi kondisi lainnya. Dengan mengatur kondisi yang sesuai, Anda dapat mengambil hanya data yang relevan atau yang memenuhi persyaratan tertentu.