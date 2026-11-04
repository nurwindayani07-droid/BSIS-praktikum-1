# ACCEPTANCE TESTS BSIS

## 1. Tujuan
Dokumen ini berisi kriteria penerimaan untuk memastikan bahwa kebutuhan fungsional utama BoardingSchool Information System (BSIS) dapat berjalan sesuai dengan tujuan yang telah ditentukan.

## 2. Daftar Acceptance Criteria

### AT-01: Login Pengguna
**Requirement:** FR-AUTH-01

- Pengguna dapat memasukkan username/email dan password.
- Jika data login benar, sistem mengarahkan pengguna ke halaman sesuai role.
- Jika data login salah, sistem menampilkan pesan kesalahan.
- Pengguna yang belum login tidak dapat mengakses halaman internal.

**Kriteria keberhasilan:** Pengguna dapat login dengan benar dan hanya mengakses halaman sesuai hak aksesnya.

### AT-02: Pengelolaan Role Pengguna
**Requirement:** FR-AUTH-02

- Admin dapat mengelola akun pengguna.
- Setiap pengguna memiliki role.
- Pengguna tidak dapat menjalankan tindakan yang berada di luar kewenangannya.

**Kriteria keberhasilan:** Hak akses pengguna berjalan sesuai role yang telah ditentukan.

### AT-03: Informasi Website Publik
**Requirement:** FR-PUB-01

- Pengunjung dapat membuka halaman beranda.
- Pengunjung dapat melihat profil pesantren.
- Pengunjung dapat melihat program pendidikan dan fasilitas.
- Pengunjung dapat melihat berita dan informasi PPDB.

**Kriteria keberhasilan:** Informasi publik dapat ditampilkan tanpa mengharuskan pengunjung login.

### AT-04: Pendaftaran Santri Baru
**Requirement:** FR-PPDB-01

- Pendaftar dapat mengisi formulir pendaftaran.
- Sistem memvalidasi data yang wajib diisi.
- Pendaftar dapat mengirimkan formulir.
- Sistem menyimpan data pendaftaran.
- Sistem memberikan informasi bahwa pendaftaran berhasil dikirim.

**Kriteria keberhasilan:** Data pendaftaran yang valid berhasil disimpan dan memiliki status awal.

### AT-05: Verifikasi Pendaftaran
**Requirement:** FR-PPDB-02

- Petugas PPDB dapat melihat daftar pendaftar.
- Petugas dapat memeriksa data dan dokumen pendaftaran.
- Petugas dapat memperbarui status pendaftaran.
- Perubahan status dapat diketahui melalui riwayat status.

**Kriteria keberhasilan:** Petugas dapat memverifikasi dan memperbarui status pendaftaran.

### AT-06: Pengelolaan Data Santri dan Wali
**Requirement:** FR-STU-01

- Admin dapat menambahkan data santri.
- Admin dapat mengubah informasi santri.
- Sistem dapat menghubungkan santri dengan orang tua atau wali.
- Hubungan santri dan wali dapat digunakan untuk menentukan hak akses orang tua.

**Kriteria keberhasilan:** Data santri dan hubungan wali-santri tersimpan dengan benar.

### AT-07: Pengelolaan Tagihan dan Pembayaran
**Requirement:** FR-FIN-01

- Petugas keuangan dapat membuat tagihan santri.
- Petugas dapat mencatat pembayaran.
- Sistem dapat memperbarui status tagihan berdasarkan pembayaran yang diterima.
- Sistem dapat menampilkan riwayat pembayaran.
- Sistem harus mencegah pembayaran melebihi sisa kewajiban tanpa aturan khusus yang disetujui.

**Kriteria keberhasilan:** Tagihan dan pembayaran tercatat dengan benar serta status tagihan sesuai jumlah pembayaran yang diterima.

### AT-08: Pengelolaan Uang Jajan
**Requirement:** FR-ALL-01

- Petugas dapat mencatat setoran uang jajan.
- Petugas dapat mencatat pengeluaran uang jajan.
- Sistem memeriksa kecukupan saldo sebelum mencatat pengeluaran.
- Sistem menghitung saldo berdasarkan seluruh transaksi.
- Koreksi transaksi harus meninggalkan jejak.

**Kriteria keberhasilan:** Saldo uang jajan sesuai dengan catatan DEPOSIT dan EXPENSE.

### AT-09: Portal Orang Tua
**Requirement:** FR-PAR-01

- Orang tua dapat login.
- Orang tua dapat melihat data santri yang memiliki hubungan wali-santri dengannya.
- Orang tua dapat melihat informasi akademik dan kepesantrenan yang diizinkan.
- Orang tua dapat melihat tagihan, pembayaran, dan uang jajan.
- Orang tua tidak dapat melihat data santri yang tidak memiliki hubungan dengannya.

**Kriteria keberhasilan:** Orang tua hanya dapat mengakses informasi anak yang menjadi tanggung jawabnya.

### AT-10: Laporan dan Dashboard
**Requirement:** FR-REP-01

- Pengguna yang memiliki hak akses dapat membuka dashboard.
- Sistem menampilkan ringkasan informasi sesuai kewenangan pengguna.
- Petugas dapat melihat laporan berdasarkan data yang tersedia.
- Informasi yang ditampilkan harus sesuai dengan data yang tersimpan.

**Kriteria keberhasilan:** Dashboard dan laporan menampilkan informasi yang sesuai dengan data sistem dan hak akses pengguna.

## 3. Catatan Pengujian
Setiap acceptance criteria perlu diuji menggunakan data sintetis atau data contoh.

Pengujian minimal harus memperhatikan:
1. Happy path: proses berjalan sesuai kondisi normal.
2. Invalid input: sistem menolak masukan yang tidak valid.
3. Unauthorized access: sistem menolak akses tanpa hak.
4. Not found atau relasi tidak sah: sistem menolak data yang tidak ditemukan atau tidak memiliki hubungan yang sah.
5. Data consistency: data tetap konsisten ketika terjadi kegagalan proses transaksi.

## 4. Kesimpulan
Fitur BSIS dinyatakan memenuhi acceptance criteria apabila perilaku sistem sesuai dengan kriteria yang telah ditentukan dan hasilnya dapat dibuktikan melalui pengujian.
