---
title: LOGIKA MATEMATIKA

---

### Zakaria Mujur Prasetyo - 240411100144
#### Teknik Informatika
---
# LOGIKA MATEMATIKA
Logika matematika adalah landasan berpikir secara logis untuk menarik kesimpulan dari suatu kondisi tertentu.
## Negasi 
Negasi Adalah penyangkalan atau kebalikan dari suatu pernyataan. Negasi memiliki sifat, yaitu jika sebuah pernyataan bernilai salah maka negasinya bernilai benar, dan sebaliknya.

$\neg, \quad-$, atau $\sim$

 | P |     $\neg P$
| -------- | -------- | 
| B     |     S     |
| S     |     B     |

$\mathrm{P}=$ Sapi merupakan binatang mamalia (pernyataan benar)
$\neg P=$ Sapi bukan binatang mamalia (pernyataan salah)
$\mathrm{Q}=$ bilangan asli terkecil adalah 1
$\neg Q=1$ bukan bilangan asli terkecil

## Konjugsi

Konjungsi adalah gabungan dari dua atau lebih pernyataan tunggal dengan kata hubung dan. Kongjungsi disimbolkan dengan:

$\wedge$

Ada kaidah khusus dalam penulisan pernyataan majemuk ini. Secara matematis, konjungsi dari pernyataan p dan q dapat dituliskan sebagai:

$P \wedge Q$

Dalam pernyataan konjungsi, satu pernyataan saja yang bernilai salah maka pernyataan gabungannya pasti bernilai salah. Untuk memudahkan kita menentukan nilai kebenaran dari pernyataan konjungsi, perhatikan tabel kebenaran konjungsi berikut.


| P | Q | $P \wedge Q$ |
| -------- | -------- | -------- |
| B     | B     | B     |
| B     | S     | S     |
| S     | B     | S     |
| S     | S     | S     |

$P=2$ adalah bilangan genap (BENAR)
$\mathrm{Q}=2$ adalah bilangan prima (BENAR)
$P \wedge Q=2$ adalah bilangan genap dan bilangan prima (BENAR)
$P=$ Persegi panjang memiliki 2 simetri putar (BENAR)
$Q=$ Persegi panjang memiliki 4 simetri lipat (SALAH)
$P \wedge Q=$ Persegi panjang memiliki 2 simetri putar dan 4 simetri lipat (SALAH)
Bagaimana jika konjungsinya berupa ingkaran? Apabila suatu pernyataan konjungsi berupa ingkaran, maka nilai kebenaran yang berlaku yaitu:
$$
\neg(P \wedge Q) \equiv \neg P \vee \neg Q
$$

Contoh negasi konjungsi:
2 adalah bilangan genap dan bilangan prima. (konjungsi)
2 bukan bilangan genap atau bukan bilangan prima. (negasi konjungsi)
## Disjungsi

Disjungsi adalah gabungan dari dua atau lebih pernyataan tunggal dengan kata hubung atau. Disjungsi disimbolkan dengan:

 $\vee$
 
 Bagaimana penulisan pernyataan majemuk yang satu ini? Secara matematis, disjungsi dari pernyataan p dan q dapat dituliskan sebagai:
 
$P \vee Q$

Dalam pernyataan disjungsi, satu pernyataan saja bernilai benar maka pernyataan gabungannya juga bernilai benar. Untuk memudahkan kita menentukan nilai kebenaran dari suatu pernyataan disjungsi, perhatikan tabel kebenaran disjungsi berikut.

| P | Q | $P \vee Q$ |
| -------- | -------- | -------- |
| B     | B     | B     |
| B     | S     | S     |
| S     | B     | S     |
| S     | S     | S     |
 
## Implikasi

Suatu pernyataan majemuk yang menyatakan hubungan sebab akibat dengan bentuk kalimat “jika P maka Q” disebut dengan implikasi atau kondisional. Implikasi disimbolkan dengan:

## Biimplikasi

Suatu pernyataan majemuk yang berbentuk kalimat “P jika dan hanya jika Q” disebut dengan biimplikasi. Sesuai dengan istilahnya, biimplikasi berarti dua pernyataan saling menjadi sebab akibat atau, sederhananya, kalimat implikasi yang bisa dibolak-balik. Biimplikasi disimbolkan dengan:






Buatlah tabel kebenaran untuk~pernyataan berikut $$P\lor(R\to\ Q)$$


$$\begin{array}{c|c|c|c|cc}P&Q&R&\ Q&R\to\ Q&P\lor(R\to\ Q)\\\hline\text{Т}&\text{Т}&\text{Т}&\text{-}&\text{-}&\text{-}\\\text{Т}&\text{Т}&\text{F}&\text{-}&\text{-}&\text{-}\\\text{T}&\text{F}&\text{T}&\text{-}&\text{-}&\text{-}\\\text{T}&\text{F}&\text{F}&\text{-}&\text{-}&\text{-}\\\text{F}&\text{T}&\text{T}&\text{-}&\text{-}&\text{-}\\\text{F}&\text{T}&\text{F}&\text{-}&\text{-}&\text{-}\\\text{F}&\text{F}&\text{T}&\text{-}&\text{-}&\text{-}\\\text{F}&\text{F}&\text{F}&\text{-}&\text{-}&\text{-}&\text{-}\end{array}$$


Jawab :


| \( P \) | \( Q \) | \( R \) | \( R \to Q \) | \( P \lor (R \to Q) \) |
|:-------:|:-------:|:-------:|:-------------:|:---------------------:|
|    T    |    T    |    T    |       T       |           T           |
|    T    |    T    |    F    |       T       |           T           |
|    T    |    F    |    T    |       F       |           T           |
|    T    |    F    |    F    |       T       |           T           |
|    F    |    T    |    T    |       T       |           T           |
|    F    |    T    |    F    |       T       |           T           |
|    F    |    F    |    T    |       F       |           F           |
|    F    |    F    |    F    |       T       |           T           |

