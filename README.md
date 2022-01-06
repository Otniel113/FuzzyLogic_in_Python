# FuzzyLogic_in_Python
Implementasi mencari restoran terbaik berdasarkan nilai/rating pelayanan dan makanan

## Input Output Program
Program menerima input Dataset berupa file Ms. Excel bernama 'restoran.xlsx' dan mengeluarkan output 10 pelanggan terbaik dalam Ms. Excel berupa kolom ID bernama 'peringkat.xlsx'. Untuk itu diperlukan library <img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" />

## Dataset
Dataset berupa Ms. Excel dengan ukuran 101x3 dengan keterangan kolom sebagai berikut
id --> id pelanggan dari angka 1-100
pelayanan --> nilai pelayanan dengan rentang nilai 1-100
makanan --> nilai makanan dengan rentang nilai 1-10

## Hal yang Diobservasi
### 1. Jumlah dan Nama Linguistik Input
Pelayanan dan Makanan memiliki jumlah linguistik masing-masing 3 dengan nama sebagai berikut
| Parameter | Nama Linguistik |
| -- | -- |
| Pelayanan | Buruk |
| | Sedang |
| | Baik |
| Makanan | Tidak Enak
| | Biasa |
| | Enak |

### 2. Batas dan Fungsi Keanggotaan
Batasnya dapat dilihat sebagai berikut
| Parameter | Nama Linguistik | Batas dan Fungsi |
| -- | -- | -- |
| Pelayanan | Buruk | x <= 40 |
| | Sedang | 40 < x < 70 |
| | Baik | x >= 70 |
| Makanan | Tidak Enak | x <= 4 |
| | Biasa | 5 <= x <= 7 |
| | Enak | x >= 8 |
<br>

Dan fungsi keangotaan berupa linier dengan gambar sebagai berikut:
![image](https://user-images.githubusercontent.com/57952404/148388941-182d7a82-26c4-4feb-b78d-f4355d83bafe.png)
![image](https://user-images.githubusercontent.com/57952404/148388981-4f6d9a22-7c3e-4a2d-a979-99c24816209d.png)

### 3. Aturan Inferensi
Dengan masing-masing jumlah linguistik 3, maka didapatkan aturan inferensi 3x3=9 dan memiliki nilai Output sebanyak 3, yaitu Mengecewakan, OK, dan Puas.
| Pelayanan | Makanan | Output |
| -- | -- | -- |
| Buruk | Tidak Enak | Mengecewakan |
| Buruk | Biasa | Mengecewakan |
| Buruk | Enak | Mengecewakan |
| Sedang | Tidak Enak | Mengecewakan |
| Sedang | Biasa | OK |
| Sedang | Enak | Puas |
| Baik | Tidak Enak | OK |
| Baik | Biasa | Puas |
| Baik | Baik | Puas |

### 4. Metode Defuzzifikasi
Dengan menggunakan Sugeno <br>
![image](https://user-images.githubusercontent.com/57952404/148390830-c6375fff-76fa-45f9-8e97-bd5f25c68d1c.png)

### 5. Bentuk dan Batas Fungsi Keanggotaan Output
Nilai Konstan Ci sebagai berikut: <br>
![image](https://user-images.githubusercontent.com/57952404/148391082-069bafac-1076-41f2-bb52-8b7c39d6916b.png)

## Hasil Akhir
Menghasilkan file 'peringkat.xlsx' berisi id pelanggan sebagai berikut <br>
![image](https://user-images.githubusercontent.com/57952404/148391303-7023f02c-2b5f-43d1-b6d0-128dfffb6c66.png)

## Lebih Lanjut
Informasi lengkap ada di Laporan PDF dan Slide PPT

## Video Presentasi
[Klik untuk melihat video presentasi](https://drive.google.com/file/d/1PG9sHg4BqUaPysBnjusfmOiAvgfuseic/view?usp=sharing)

