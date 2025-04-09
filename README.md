# UKK-Kasir
UKK kasir 2025 - Angkatan 6

isi dalam file main.c adalah program yang berfungsi dalam tugas UKK kasir sederhana pada tahun 2025 - Angkatan 6 

Kamu Bisa Menjadikan kode ini sebagai refrensi pembelajaran


Baiklah, saya akan menjelaskan cara kerja fungsi `bandingkan_produk` dengan contoh sederhana.

Misalkan kamu membeli:
- 2 Buku Tulis
- 5 Pensil
- 3 Penghapus
- 1 Penggaris
- 0 Bujur Sangkar (tidak beli)

Awalnya, daftar ini tersimpan dalam urutan asli (sesuai dengan nomor di menu):
1. Buku Tulis (2 buah)
2. Pensil (5 buah)
3. Penghapus (3 buah)
4. Penggaris (1 buah)
5. Bujur Sangkar (0 buah)

Ketika program memanggil fungsi `qsort` dengan fungsi pembanding `bandingkan_produk`, inilah yang terjadi:

**Langkah 1:** Fungsi `qsort` mulai dengan mengambil pasangan barang dan membandingkannya.

**Langkah 2:** Misalnya membandingkan Buku Tulis (2 buah) dengan Pensil (5 buah)
- `produkA = Buku Tulis (2 buah)`
- `produkB = Pensil (5 buah)`
- Perhitungan: `produkB->jumlah - produkA->jumlah` = `5 - 2` = `3` (hasil positif)
- Karena hasilnya positif, Pensil harus ditempatkan lebih dulu (di atas) Buku Tulis

**Langkah 3:** Fungsi terus membandingkan pasangan-pasangan barang lainnya
- Membandingkan Pensil (5 buah) dengan Penghapus (3 buah): `5 - 3` = `2` (positif), Pensil di atas
- Membandingkan Penghapus (3 buah) dengan Buku Tulis (2 buah): `3 - 2` = `1` (positif), Penghapus di atas
- Dan seterusnya...

**Hasil akhir:** Setelah semua perbandingan selesai, urutan barang menjadi:
1. Pensil (5 buah) - Jumlah terbanyak
2. Penghapus (3 buah)
3. Buku Tulis (2 buah)
4. Penggaris (1 buah)
5. Bujur Sangkar (0 buah) - Jumlah terkecil

Urutan ini kemudian digunakan saat program menampilkan rekap pesanan di layar dan saat menyimpan struk ke file. Jadi pada struk, kamu akan melihat barang yang paling banyak dibeli (Pensil) di bagian atas daftar, dan yang paling sedikit/tidak dibeli (Bujur Sangkar) di bagian bawah atau tidak muncul sama sekali.
