---
title: 'Probabilitas Diskrit '

---

---
title: 'Probabilitas Diskrit '

---
# Zakaria Mujur Prasetyo | NIM 24-144
# Probabilitas Diskrit
## Probabilitas Bayesian

Naive Bayes adalah salah satu dari banyak model pengklasifikasi yang ada. Model ini pada dasarnya didasarkan pada Teorema Bayes dan menggunakan asumsi "naif" bahwa semua fitur bersifat independen.

Asumsikan bahwa kita ingin membuat keputusan apakah kita harus pergi ke pantai atau tidak, berdasarkan dua fitur: X₁ (Suhu) dan X₂ (Angin). Fitur X₁ dapat mengasumsikan tiga nilai diskret (rendah, sedang, tinggi), sementara fitur X₂ dapat mengasumsikan tiga nilai diskret yang berbeda (lemah, normal, kuat). Untuk menyederhanakannya, kita akan menggunakan X₁ sebagai singkatan untuk Suhu, dan X₂ untuk Angin. Target Pantai kita akan disingkat menjadi B.

Tabel di bawah ini berisi beberapa catatan fitur X₁ , X₂ , dan target B. Yang terakhir dapat mengasumsikan nilai Boolean benar (pergi ke pantai) atau salah (jangan pergi ke pantai).<br>
![Screenshot 2024-12-08 040609](https://hackmd.io/_uploads/HJokFVMV1g.png)
Sasaran kami adalah, dengan mempertimbangkan sepasang fitur baru (X₁, X₂) , menentukan target B ( benar atau salah ). Tentu saja contoh ini sangat disederhanakan, demi penjelasan. Jadi, kami akan berasumsi bahwa sepasang fitur baru tersebut belum direkam.Secara sederhana, kita dapat mengatakan: jika suhu sedang (tidak tinggi, tidak rendah) dan angin lemah, haruskah kita pergi ke pantai atau tidak? Kita juga berasumsi bahwa kita memiliki skala sendiri untuk suhu dan angin, sehingga kita tahu persis apa arti masing-masing status tersebut Secara Matematika, kita mencari probabilitas tertinggi diantara dua hal berikut: probabilitas bahwa Pantai = benar , dengan asumsi bahwa Suhu = sedang & Angin = lemah ,
$P(B = T \mid X_1 = M, X_2 = W)$
dan kemungkinan bahwa Pantai = salah , mengingat Suhu = sedang & Angin = lemah ,
$P(B = F \mid X_1 = M, X_2 = W)$
Mana pun yang lebih besar akan secara otomatis memberi kita jawaban atas pertanyaan tersebut. Perhatikan bahwa model ini murni berdasarkan probabilitas.

## VARIABEL INDEPENDEN
Langkah terbesar yang akan kita ambil sekarang adalah mengasumsikan bahwa fitur X₁ dan X₂ bersifat independen — maka dari itu dinamakan “Naif” sebagai bagian dari model pengklasifikasi kita (Naive Bayes). Mungkin naif untuk mengasumsikan bahwa variabel-variabel ini memang independen, tetapi itu akan menyederhanakan model kita (dan perhitungan kita) secara signifikan.

Jika kita menggunakan aturan produk untuk probabilitas gabungan , kita dapat menulis ulang probabilitas marginal menjadi P(X) = P(X₁) . P(X₂).

Dengan cara yang sama, kita dapat menulis ulang kemungkinan sebagai P(X₁, X₂ | B) = P(X₁| B) . P(X₂ | B).

Maka persamaan utama kita menjadi:
$P(B \mid X_1, X_2) = \frac{P(X_1 \mid B) \cdot P(X_2 \mid B) \cdot P(B)}{P(X_1) \cdot P(X_2)}$

Sebelum kita menyelami persamaan ini dan mulai memasukkan semua angka, mari kita lihat plot di bawah ini yang merangkum distribusi kelima sampel yang kita miliki dari tabel di atas.<br>
![Screenshot 2024-12-08 050649](https://hackmd.io/_uploads/B1ZXPHGN1g.png)

# Perhitungan Probabilitas
Sekarang kita kembali ke permasalahan kita: diberikan sampel fitur baru ( X₁, X₂ ), kita ingin memprediksi target B. Jika kita tetap menggunakan contoh dimana Suhu = sedang ( X₁ = M ) dan Angin = lemah ( X₂ = W ), kita harus menghitung
$P(B' | T, X_1 = M, X_2 = W) = \frac{P(X_1 = M | B = T) \cdot P(X_2 = W | B = T) \cdot P(B = T)}{P(X_1 = M) \cdot P(X_2 = W)}$
Dan
$P(B' | T, X_1 = M, X_2 = W) = \frac{P(X_1 = M | B = F) \cdot P(X_2 = W | B = F) \cdot P(B = F)}{P(X_1 = M) \cdot P(X_2 = W)}$
untuk mencari yang terbesar dari keduanya. Baiklah, mari kita hitung berdasarkan bagiannya.
## Probabilitas Sebelumnya
Setiap probabilitas sebelumnya harus dihitung secara individual, tetapi perhitungannya mudah: dari semua (5) sampel, berapa banyak yang benar dan berapa banyak yang salah ? Jawabannya masing-masing adalah 3 dan 5. Jadi, P(B = T) = 3/5 = 0,6 dan P(B = F) = 2/5 = 0,4 .

Sekali lagi, ini disebut probabilitas sebelumnya karena merupakan pengetahuan sebelum peristiwa itu sendiri, sehingga dapat dihitung hanya berdasarkan sampel yang telah kita rekam.

2) Kemungkinan

Sama seperti probabilitas sebelumnya, setiap persamaan probabilitas posterior akan mengarah pada kemungkinannya sendiri.

Untuk B = T , kita memiliki:

P(X₁ = M, X₂ = W | B = T ) = P(X₁ = M | B = T ) . P(X₂ = W | B = T ) , di mana P(X₁ = M | B = T ) = 1/3 ≈ 0,33 dan P(X₂ = W | B = T ) = 1/3 ≈ 0,33 .

Hal ini menggambarkan berapa banyak fitur suhu yang sedang dari semua target pantai yang benar , dan berapa banyak fitur angin yang lemah dari semua target pantai yang benar , masing-masing.

Dengan demikian, P(X₁ = M, X₂ = W | B = T) = 1/3 . 1/3 = 1/9 ≈ 0,11 .

Secara analogis, untuk B = F , kita memiliki:

P(X₁ = M, X₂ = W | B = F ) = P(X₁ = M | B = F ) . P(X₂ = W | B = F ) , di mana P(X₁ = M | B = F ) = 1/2 = 0,5 dan P(X₂ = W | B = F ) = 1/2 = 0,5 .

Dengan demikian, P(X₁ = M, X₂ = W | B = F ) = 1/2 . 1/2 = 1/4 = 0,25 .

3) Probabilitas Marjinal

Probabilitas marginalnya sama dalam kedua persamaan yang ingin kita hitung (untuk B = T dan B = F ):

P(X₁ = M, X₂ = W) = P(X₁ = M) . P(X₂ = W) , di mana P(X₁ = M) = 2/5 = 0,4 (dua suhu sedang dari semua lima sampel) dan P(X₂ = W) = 2/5 = 0,4 (dua angin lemah dari semua lima sampel).

Jadi, P(X₁ = M, X₂ = W) = 2/5 . 2/5 = 4/25 = 0,16 .

4) Probabilitas Posterior

Sekarang kita akhirnya dapat memasukkan semua nilai ke dalam dua persamaan utama kita untuk menghitung setiap probabilitas posterior:
$P(B = T | X_1 = M, X_2 = W) = \frac{\frac{1}{9} \cdot \frac{3}{5}}{\frac{4}{25}} = \frac{5}{12} \approx 0.42.$
Dan
$P(B = F | X_1 = M, X_2 = W) = \frac{\frac{1}{4} \cdot \frac{2}{5}}{\frac{4}{25}} = \frac{5}{8} \approx 0.63.$
Karena 0,63 > 0,42 , kita dapat memprediksi bahwa B = F , atau mengatakan bahwa kita tidak boleh pergi ke pantai , mengingat kondisi tersebut.

## Probabilitas Prediksi
Langkah lain yang diambil oleh model Naive Bayes adalah menghitung probabilitas relatif untuk kedua keputusan benar dan salah . Hal ini dilakukan karena probabilitas posterior tidak berjumlah sama dengan unit ( 0,63 > 0,42 = 1,05 ≠ 1 atau, jika Anda ingin lebih tepat, 5/12 + 5/8 = 25/24 ≠ 1 ).

Kita dapat mendefinisikan PT sebagai probabilitas untuk memprediksi benar dan PF sebagai probabilitas untuk memprediksi salah sebagai berikut:
$P_T = \frac{P(B = T | X_1, X_2)}{P(B = T | X_1, X_2) + P(B = F | X_1, X_2)}$
Dan
$P_F = \frac{P(B = F | X_1, X_2)}{P(B = F | X_1, X_2) + P(B = T | X_1, X_2)}$

Perhatikan bahwa kami menghilangkan nilai aktual untuk X₁ dan X₂ demi kesederhanaan. Selain itu, sekarang kami dapat memastikan bahwa PT + PF = 1 .

Keuntungan utama menggunakan probabilitas (yang jumlahnya sama dengan satuan) adalah jika kita menemukan probabilitas pertama lebih besar dari 0,5, kita dapat membuat keputusan tanpa menghitung probabilitas kedua. Atau, jika kita berhadapan dengan lebih dari dua kelas untuk variabel target kita, segera setelah kita menemukan satu probabilitas yang lebih besar dari 0,5, itu sudah menjadi jawaban kita.

Dengan memasukkan probabilitas posterior yang telah kita hitung, kita memperoleh
![P](https://hackmd.io/_uploads/SJHFqBM41e.png)
dan, sekali lagi, kita akan memilih B = F. Namun begitu kita menghitung probabilitas prediksi pertama, PT = 0.4 , karena PT < 0.5 , kita akan secara otomatis memprediksi kelas lainnya (selain T ); yaitu, F — yang, sekali lagi, berarti kita tidak boleh pergi ke pantai .










