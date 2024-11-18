---
title: 240411100144_ZAKARIA MUJUR PRA

---

**240411100144_ZAKARIA MUJUR PRASETYO**
## ANALISA GRAPH    
### Analisis grafik adalah proses untuk menganalisis dan memahami hubungan antara objek yang direpresentasikan dalam grafik.
### Graph adalah struktur data yang terdiri dari kumpulan titik (simpul) yang dihubungkan oleh garis (sisi).
---
### Dalam ilmu komputer, graph merupakan fondasi dari berbagai aplikasi, seperti: Struktur data graph, Pemodelan grafik, Alokasi sumber daya pada sistem operasi, Pencarian rute terpendek pada Google Maps.
---
## **Social Network Analysis** 
### Social Network Analysis merupakan bidang kajian yang mengekplorasitentang hubungan manusia dengan menggunakan teori graf. Implementasi Social Network Analysis dapat menjelaskan relasi atau hubungan antar aktor melalui visualisasi berbentuk graf. Relasi dalam analisis jaringan sosial dapat diproses dalam bentuk perhitungan yang disebut centrality dalam sebuah jaringan sosial sesuai dengan posisi masing-masing aktor di dalam struktur jaringan tersebut.
# Adjacency Matrix

| **Node** | **1** | **2** | **3** | **4** | **5** | **6** | **7** | **8** | **9** |
|----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| **1**    | -      | 1      | 1      | 1      | 0      | 0      | 0      | 0      | 0      |
| **2**    | 1      | -      | 1      | 0      | 0      | 0      | 0      | 0      | 0      |
| **3**    | 1      | 1      | -      | 1      | 0      | 0      | 0      | 0      | 0      |
| **4**    | 1      | 0      | 1      | -      | 1      | 1      | 0      | 0      | 0      |
| **5**    | 0      | 0      | 0      | 1      | -      | 1      | 1      | 0      | 0      |
| **6**    | 0      | 0      | 0      | 1      | 1      | -      | 1      | 1      | 0      |
| **7**    | 0      | 0      | 0      | 0      | 1      | 1      | -      | 1      | 1      |
| **8**    | 0      | 0      | 0      | 0      | 0      | 1      | 1      | -      | 1      |
| **9**    | 0      | 0      | 0      | 0      | 0      | 0      | 1      | 1      | -      |

![image](https://hackmd.io/_uploads/B1daJEOMkl.png)
### Centrality adalah penentuan aktor menggunakan ukuran pada Social Network Centrality dalam teori graf dan social network .Dibagi menjadi empat jenis, 
### - DEGREE CENTRALITY, 
### - BETWENESS CENTRALITY, 
### - closeness CENTRALITY 
### - eigenvector CENTRALITY
---
## DEGREE CENTRALITY
### Degree centrality adalah jumlah edge yang terkoneksi pada suatu node yang mewakili interaksi.
#### INI ADALAH DEGREE CENTRALITY & NORMALISASI DEGREE CENTRALITY
![image](https://hackmd.io/_uploads/H1ASWVuzkx.png)
#### CONTOH KODE DEGREE CENTRALITY
```
import networkx as nx
G = nx.Graph([(0, 1), (0, 2), (0, 3),(1, 2),(1,3),(1,4)])
nx.degree_centrality(G)
pos = nx.spring_layout(G)
```
`nx.draw_networkx(G, pos = pos, with_labels=True,node_size=300)`
![image](https://hackmd.io/_uploads/rknxd8PzJl.png)

## **BETWENESS CENTRALITY**
### Menghitung jumlah lintasan terpendek yang melewati suatu node Node dengan  betweenness  tinggi  adalah  penting dalam komunikasi dan penyebaran informasi

### ![image](https://hackmd.io/_uploads/HyLcUIdGJg.png)
## σst(4)/σst

| **t**   | **s = 1** | **s = 2** | **s = 3** |
|---------|-----------|-----------|-----------|
| t = 5   | 1/1       | 2/2       | 1/1       |
| t = 6   | 1/1       | 2/2       | 1/1       |
| t = 7   | 2/2       | 4/4       | 2/2       |
| t = 8   | 2/2       | 4/4       | 2/2       |
| t = 9   | 2/2       | 4/4       | 2/2       |

## **closeness** **CENTRALITY** 
### Closenes centrality adalah nilai kedekatan antara satu node dengan node lain dalam jaringan dengan menghitung rata-rata dari jarak relasi node-node
**Average Distance:**
**Closeness Centrality:**
![image](https://hackmd.io/_uploads/BysnYUdzyl.png)
