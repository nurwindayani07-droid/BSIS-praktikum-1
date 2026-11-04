# WORKFLOWS BSIS

## 1. Workflow PPDB sampai Santri Aktif

**Aktor:** Pendaftar, Petugas PPDB, Admin.

**Alur proses:**

1. Pendaftar membuat akun atau mengisi formulir pendaftaran.
2. Pendaftar mengirimkan formulir pendaftaran.
3. Petugas PPDB memeriksa data dan dokumen pendaftaran.
4. Pendaftar mengikuti proses seleksi.
5. Petugas PPDB menetapkan keputusan penerimaan.
6. Jika dinyatakan lulus, pendaftar melakukan registrasi ulang.
7. Sistem membuat atau menghubungkan data santri dan wali.
8. Admin menetapkan kelas, asrama, dan tagihan awal.
9. Akun orang tua memperoleh akses sesuai hubungan wali-santri.
10. Santri menjadi santri aktif.

**Hasil akhir:** Data santri baru tercatat dan siap dikelola dalam sistem.

## 2. Workflow Tagihan dan Pembayaran

**Aktor:** Petugas Keuangan, Santri, Orang Tua.

**Alur proses:**

1. Petugas keuangan membuat jenis biaya dan periode pembayaran.
2. Petugas atau sistem membuat tagihan untuk santri.
3. Santri atau orang tua melakukan pembayaran sesuai ketentuan.
4. Pembayaran dicatat secara manual atau simulasi.
5. Jika membutuhkan verifikasi, petugas memeriksa pembayaran.
6. Petugas menerima atau menolak pembayaran.
7. Sistem memperbarui status tagihan berdasarkan pembayaran yang diterima.
8. Sistem menyediakan kuitansi atau riwayat pembayaran.
9. Orang tua dapat melihat status tagihan dan pembayaran.

**Hasil akhir:** Tagihan dan riwayat pembayaran tercatat dalam sistem.

## 3. Workflow Saldo Uang Jajan

**Aktor:** Orang Tua, Petugas Uang Jajan, Santri.

**Alur proses:**

1. Orang tua melakukan atau menyampaikan setoran uang jajan.
2. Petugas mencatat transaksi DEPOSIT.
3. Sistem menambahkan transaksi ke ledger.
4. Ketika santri melakukan pengeluaran, petugas mencatat transaksi EXPENSE.
5. Sistem memeriksa apakah saldo mencukupi.
6. Jika saldo mencukupi, transaksi pengeluaran dicatat.
7. Sistem menghitung ulang saldo berdasarkan seluruh transaksi.
8. Orang tua dapat melihat saldo dan riwayat mutasi.
9. Jika terjadi kesalahan, petugas melakukan koreksi melalui reversal atau adjustment yang meninggalkan jejak.

**Hasil akhir:** Saldo dan riwayat transaksi uang jajan dapat diketahui secara transparan.

## 4. Workflow Informasi Orang Tua

**Aktor:** Orang Tua/Wali.

**Alur proses:**

1. Orang tua melakukan login.
2. Sistem memeriksa role dan hubungan wali-santri.
3. Jika memiliki lebih dari satu anak, orang tua memilih santri yang ingin dilihat.
4. Sistem menampilkan ringkasan profil santri.
5. Orang tua dapat melihat informasi akademik yang diizinkan.
6. Orang tua dapat melihat informasi kepesantrenan yang diizinkan.
7. Orang tua dapat melihat tagihan dan pembayaran.
8. Orang tua dapat melihat saldo serta mutasi uang jajan.
9. Orang tua dapat melihat pengumuman.
10. Sistem menolak akses terhadap data santri yang tidak memiliki hubungan wali-santri.

**Hasil akhir:** Orang tua memperoleh informasi mengenai anaknya secara aman dan sesuai hak akses.

## 5. Catatan
Keempat workflow di atas merupakan alur utama sistem BSIS. Setiap alur harus diperhatikan dalam proses perancangan, implementasi, dan pengujian sistem.
