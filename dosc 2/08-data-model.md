# DATA MODEL BSIS

## 1. Tujuan
Dokumen ini menjelaskan rancangan data konseptual serta hubungan antarentitas yang digunakan dalam BoardingSchool Information System (BSIS).

## 2. Daftar Entitas Utama

| No. | Entitas | Deskripsi |
|---|---|---|
| 1 | Users | Menyimpan informasi akun pengguna sistem. |
| 2 | Roles | Menyimpan jenis peran dan hak akses pengguna. |
| 3 | Applicants | Menyimpan data calon santri. |
| 4 | Applications | Menyimpan informasi pendaftaran calon santri. |
| 5 | Students | Menyimpan data santri yang telah diterima. |
| 6 | Guardians | Menyimpan data orang tua atau wali santri. |
| 7 | Student_Guardian | Menghubungkan data santri dengan orang tua atau wali. |
| 8 | Classes | Menyimpan informasi kelas. |
| 9 | Subjects | Menyimpan informasi mata pelajaran. |
| 10 | Enrollments | Menghubungkan santri dengan kelas atau periode akademik. |
| 11 | Attendances | Menyimpan data kehadiran santri. |
| 12 | Grades | Menyimpan informasi nilai akademik santri. |
| 13 | Dormitories | Menyimpan informasi asrama. |
| 14 | Rooms | Menyimpan informasi kamar asrama. |
| 15 | Room_Assignments | Menyimpan penempatan santri pada kamar. |
| 16 | Fee_Types | Menyimpan jenis biaya yang harus dibayar. |
| 17 | Bills | Menyimpan tagihan yang dimiliki santri. |
| 18 | Bill_Items | Menyimpan rincian komponen tagihan. |
| 19 | Payments | Menyimpan catatan pembayaran. |
| 20 | Payment_Verifications | Menyimpan informasi verifikasi pembayaran. |
| 21 | Allowance_Transactions | Menyimpan transaksi setoran dan pengeluaran uang jajan. |
| 22 | Content | Menyimpan berita, pengumuman, dan informasi publik. |

## 3. Hubungan Antarentitas

### A. Pengguna dan Role
- Satu role dapat dimiliki oleh beberapa pengguna.
- Setiap pengguna memiliki role sesuai kewenangannya.
- Pengguna dapat menjadi pelaku dalam transaksi penting.

### B. PPDB dan Santri
- Satu calon santri dapat memiliki data pendaftaran.
- Setiap pendaftaran memiliki riwayat status.
- Pendaftar yang dinyatakan lulus dan melakukan registrasi ulang dapat menjadi santri.

### C. Santri dan Wali
- Satu santri dapat memiliki satu atau lebih wali.
- Satu wali dapat memiliki hubungan dengan lebih dari satu santri.
- Hubungan tersebut dicatat melalui entitas Student_Guardian.

### D. Akademik
- Santri dapat terdaftar dalam kelas.
- Kelas dapat memiliki beberapa mata pelajaran.
- Data kehadiran dan nilai berhubungan dengan santri dan kegiatan akademik.

### E. Kepesantrenan
- Asrama memiliki beberapa kamar.
- Santri dapat ditempatkan pada kamar tertentu.
- Riwayat penempatan dan catatan kepesantrenan dapat disimpan.

### F. Keuangan
- Santri dapat memiliki beberapa tagihan.
- Tagihan memiliki rincian biaya.
- Satu tagihan dapat memiliki satu atau beberapa catatan pembayaran.
- Pembayaran dapat melalui proses verifikasi.

### G. Uang Jajan
- Santri dapat memiliki banyak transaksi uang jajan.
- Transaksi terdiri atas DEPOSIT dan EXPENSE.
- Saldo dihitung berdasarkan keseluruhan transaksi.
- Koreksi transaksi dilakukan melalui reversal atau adjustment yang dapat ditelusuri.

### H. Konten
- Pengguna yang memiliki kewenangan dapat membuat dan mengelola berita atau pengumuman.

## 4. Aturan Penting dalam Data Model
1. Setiap data santri harus memiliki identitas yang dapat dibedakan.
2. Hubungan santri dan wali harus tercatat dengan jelas.
3. Tagihan dan pembayaran harus terhubung dengan santri yang bersangkutan.
4. Riwayat transaksi keuangan harus tetap dapat ditelusuri.
5. Saldo uang jajan tidak boleh diubah secara langsung tanpa catatan transaksi.
6. Orang tua hanya dapat mengakses data santri yang memiliki hubungan wali-santri dengannya.

## 5. Catatan
Rancangan ini merupakan model data konseptual awal. Nama entitas dan tabel dapat disesuaikan pada tahap implementasi database, setelah melalui proses normalisasi dan peninjauan lebih lanjut.
