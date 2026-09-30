# Orders On Table

Program ini merupakan **tugas mini project** pemrograman C++ berupa sistem pemesanan makanan dan minuman langsung dari meja restoran.

## Anggota Tim

1. Dhama Shidqi Putra
2. Alfian Putra Hidayat

## Deskripsi Singkat

Pelanggan memasukkan nomor meja, memilih menu yang tersedia, lalu membayar menggunakan QRIS atau Cash. Setelah pembayaran divalidasi, program menampilkan nota pembayaran.

## Fitur

- Input nomor meja (1-20). Meja 1-10 berada di area **Indoor**, meja 11-20 di area **Outdoor**.
- Daftar menu lengkap dengan harga dan **stok**. Stok berkurang setiap ada pesanan, dan menu yang stoknya habis tidak bisa dipesan.
- Pesan lebih dari satu menu (pilihan "Pesan lagi?").
- Pembayaran dengan **QRIS** atau **Cash** (untuk Cash, kembalian dihitung otomatis).
- Animasi loading validasi pembayaran.
- Nota pembayaran berisi waktu, nomor meja, daftar pesanan, total, dan metode bayar.

## Alur Program

```
Input No Meja -> Tampil Menu + Stok -> Pilih Menu & Jumlah -> Pesan Lagi?
      -> Pilih Metode Bayar (QRIS / Cash) -> Loading Validasi -> Nota
```

## Materi yang Digunakan

| Materi | Penerapan |
|---|---|
| Struct | `Menu` dan `Pesanan` |
| Array | `daftarMenu[]` dan `pesanan[]` |
| Loop | `for` dan `while` (tampil menu, validasi input, pesan lagi) |
| Input | `cin` (nomor meja, menu, jumlah, metode bayar, uang) |
| Output | `cout` (menu, pesan, dan nota) |
| Percabangan | `if / else` (area meja, stok habis, metode pembayaran) |
| Function | `tampilkanMenu()`, `hitungTotal()`, `loading()`, `cetakStruk()` |

## Cara Menjalankan

Pastikan compiler g++ sudah terpasang, lalu jalankan perintah berikut di terminal (PowerShell):

```
g++ orders_on_table.cpp -o orders_on_table.exe
.\orders_on_table.exe
```

## Contoh Nota

```
======================================
            NOTA PEMBAYARAN
======================================
Waktu : Wed Sep 30 07:37:52 2026
Meja  : 4 (Indoor)
--------------------------------------
Menu            Qty     Subtotal
Nasi Goreng     2       Rp 50000
--------------------------------------
TOTAL                   Rp 50000
Metode                  QRIS
Status                  LUNAS
======================================
   Terima kasih, selamat menikmati!
```
