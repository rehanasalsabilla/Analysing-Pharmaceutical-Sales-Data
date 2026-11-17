# Analysing Pharmaceutical Sales Data

Analisis data penjualan obat harian menggunakan Python, Pandas, dan Matplotlib. Proyek ini merupakan bagian dari latihan Data Analyst di [roadmap.sh](https://roadmap.sh/projects/pharmaceutical-sales-data).

## Ringkasan

Proyek ini menjawab enam pertanyaan bisnis dari data penjualan harian delapan kategori obat (kode ATC). Hasil akhirnya berupa satu Jupyter Notebook yang berisi kode, tabel, grafik, dan kesimpulan untuk setiap pertanyaan.

## Dataset

| Aspek | Keterangan |
|---|---|
| Sumber | [Pharma Sales Data (Kaggle)](https://www.kaggle.com/milanzdravkovic/pharma-sales-data) |
| File yang dipakai | `salesdaily.csv` |
| Jumlah baris | 2.106 hari (2014 sampai 2019) |
| Kolom obat | M01AB, M01AE, N02BA, N02BE, N05B, N05C, R03, R06 |
| Kolom bantu | Year, Month, Hour, Weekday Name |
| Data kosong | Tidak ada |

Dataset hanya memuat kode ATC (klasifikasi obat berdasarkan kelompok kegunaan), bukan nama merek. Dalam analisis ini, setiap kode ATC diperlakukan sebagai satu jenis obat.

## Teknologi

| Alat | Kegunaan |
|---|---|
| Python 3 | Bahasa pemrograman |
| Pandas | Pengolahan dan agregasi data |
| Matplotlib | Visualisasi |
| Kaggle Notebook | Lingkungan kerja |

## Pertanyaan dan Temuan Utama

| No | Pertanyaan | Temuan |
|---|---|---|
| 1 | Total penjualan per kategori ATC | N02BE tertinggi (sekitar 63.005), N05C terendah (sekitar 1.250) |
| 2 | Obat dengan penjualan tertinggi | N02BE di peringkat pertama, disusul N05B dan R03 |
| 3 | Tiga obat terlaris pada Jan 2015, Jul 2016, dan Sep 2017 | N02BE dan N05B selalu di dua teratas. Peringkat ketiga berganti dari R03 ke M01AB pada Juli 2016 |
| 4 | Obat yang paling sering terjual di 2017 | N02BE, baik dari jumlah hari terjual (361 hari) maupun total kuantitas (sekitar 9.259) |
| 5 | Kategori dengan rata-rata penjualan harian tertinggi | N02BE, sekitar 29,9 per hari |
| 6 | Apakah R03 lebih laku di bulan tertentu | Ya. Tertinggi pada Desember (sekitar 7,92 per hari), terendah pada Juli (sekitar 2,96 per hari) |

## Kesimpulan

N02BE mendominasi penjualan pada hampir semua ukuran yang dianalisis. Penjualan obat pernapasan R03 menunjukkan pola musiman yang jelas: tinggi pada Oktober sampai Maret dan rendah pada Juni sampai September. Pola ini bisa menjadi dasar perencanaan stok.

## Keterbatasan

| Keterbatasan | Dampak |
|---|---|
| Tidak ada nama merek | Pertanyaan tentang "merek" dijawab pada tingkat kode ATC |
| Satuan kuantitas tidak dijelaskan di dataset | Angka ditulis sebagai "kuantitas", bukan unit atau tablet |
| Tidak ada informasi lokasi atau penyebab | Penjelasan pola musiman R03 hanya berupa dugaan dan perlu data tambahan untuk dibuktikan |
| Pertanyaan 4 dapat ditafsirkan dua cara | Dihitung dari jumlah hari terjual dan total kuantitas, dan keduanya menunjuk ke kategori yang sama |

## Struktur Repositori

```
Analysing-pharmaceutical-sales-data/
├── data/
│   └── salesdaily.csv
├── analysing-pharmaceutical-sales-data.ipynb
└── README.md
```

## Cara Menjalankan

| Langkah | Yang dilakukan |
|---|---|
| 1 | Unduh `salesdaily.csv` dari Kaggle lalu simpan di folder `data/` |
| 2 | Instal library: `pip install pandas matplotlib jupyter` |
| 3 | Buka notebook dengan `jupyter notebook` |
| 4 | Ubah path pada sel pemuatan data menjadi `data/salesdaily.csv` |
| 5 | Jalankan semua sel dari atas ke bawah (Run All) |

Jika dijalankan di Kaggle, tambahkan dataset melalui **Add Input**, lalu gunakan path dari `/kaggle/input/`.

## Tautan

| Item | Tautan |
|---|---|
| Notebook di Kaggle | [isi tautan notebook Kaggle] |
| Halaman proyek | https://roadmap.sh/projects/pharmaceutical-sales-data |

## Penulis

[Nama kamu] · [tautan GitHub atau LinkedIn]
