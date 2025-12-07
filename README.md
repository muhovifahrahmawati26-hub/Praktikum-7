<!-- BOOTSTRAP ICONS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">

<h1 align="center">
  <i class="bi bi-journal-code"></i> Praktikum 7 - OOP 
  <br>
<hr>

<h2><i class="bi bi-terminal"></i> Tugas Praktikum </h2>
<p>
Tujuan dari program ini adalah mengaplikasikan konsep Object-Oriented Programming (OOP) dalam Python, khususnya konsep Class dan Instance Class, untuk membuat sistem manajemen data nilai mahasiswa sederhana yang meliputi fungsi CRUD (Create, Read, Update, Delete).
</p>

### 🧩 Flowchart Program
<img width="791" height="951" alt="flowchart7" src="https://github.com/user-attachments/assets/0f6b551a-4eb3-44df-8f1e-11831f9128e8" />

### Penjelasan Flowchart
1. Inisialisasi Program
Alur dimulai dari simbol START. Langkah pertama yang dieksekusi adalah proses inisialisasi, yaitu membuat Instance Class nilai_mahasiswa = DaftarNilai(). Proses ini memanggil constructor __init__ dari DaftarNilai, yang menyiapkan atribut utama, yaitu list kosong self.data_nilai, tempat semua data mahasiswa akan disimpan.

2. Tampilan Menu Utama
Setelah inisialisasi, program masuk ke bagian MENU UTAMA. Pengguna disajikan pilihan fungsi CRUD (1-Tambah, 2-Tampil, 3-Hapus, 4-Ubah, 5-Keluar) dan diminta untuk memasukkan pilihan. Input ini kemudian akan masuk ke blok keputusan (Belah Ketupat) untuk menentukan aksi selanjutnya.

3. Eksekusi Fungsi (Decision Points)
Tergantung pada pilihan pengguna, alur program akan bercabang ke salah satu method yang diimplementasikan dalam class DaftarNilai:

Pilihan 1: Tambah Data (Create)
Jika pengguna memilih 1, program akan memanggil method tambah().
Method ini meminta input berupa nama dan nilai mahasiswa. Setelah validasi dan penyimpanan berhasil ke dalam list self.data_nilai, program menampilkan konfirmasi "data telah disimpan". Alur kemudian diarahkan untuk Kembali ke Menu Utama.

Pilihan 2: Tampilkan Data (Read)
Jika pengguna memilih 2, program memanggil method tampilkan().
Method ini bertugas untuk menampilkan semua data yang ada di dalam list self.data_nilai. Output yang dihasilkan adalah "data ditampilkan" dalam format tabel. Alur kemudian diarahkan untuk Kembali ke Menu Utama.

Pilihan 3: Hapus Data (Delete)
Jika pengguna memilih 3, program memanggil method hapus().
Pengguna diminta untuk memilih nama yang akan dihapus. Method ini mencari dan menghapus data yang sesuai. Setelah berhasil, program menampilkan konfirmasi "data dihapus". Alur kemudian diarahkan untuk Kembali ke Menu Utama.

Pilihan 4: Ubah Data (Update)
Jika pengguna memilih 4, program memanggil method ubah().
Pengguna diminta untuk pilih nama yang akan diubah nilainya. Setelah nama ditemukan, pengguna diminta memasukkan nilai baru. Setelah pembaruan selesai, program menampilkan konfirmasi "data diubah". Alur kemudian diarahkan untuk Kembali ke Menu Utama.

4. Mengakhiri Program (Keluar)
Jika pengguna memilih 5, program akan masuk ke proses pengecekan "apakah data selesai?". Jika pengguna memilih "ya", program menampilkan pesan penutup dan alur berakhir pada simbol END. Jika pengguna memilih "tidak", artinya pengguna ingin membatalkan keluar dan melanjutkan operasi, sehingga alur kembali diarahkan untuk Kembali ke Menu Utama.

### Penjelasan Pemograman (praktikum7.py)
- Konsep OOP yang Digunakan

    1. Class dan Instance Class: Program ini menggunakan Class DaftarNilai , yang berfungsi sebagai blueprint (cetak biru) untuk membuat objek (instance class)  manajemen data. Di program utama, nilai_mahasiswa = DaftarNilai() adalah proses pembuatan instance class.

    2. Atribut dan Method:
        - Atribut (Deklarasi Variabel): Class DaftarNilai memiliki atribut publik self.data_nilai yang diinisialisasi di dalam constructor __init__. Atribut ini adalah list yang digunakan untuk menyimpan data mahasiswa.

        - Method (Fungsi): Class ini memiliki method publik tambah(), tampilkan(), hapus(nama), dan ubah(nama) , yang merupakan behavior (perilaku)  dari objek. Method ini dapat diakses di luar class, contohnya nilai_mahasiswa.tambah().


- Struktur Data
Data mahasiswa disimpan dalam format List of Dictionaries (self.data_nilai). Setiap elemen dalam list adalah sebuah dictionary yang merepresentasikan satu mahasiswa dengan key nama dan nilai.

- Fungsi Method

    - __init__(self): Constructor yang dieksekusi saat objek dibuat, menginisialisasi list self.data_nilai menjadi kosong.

    - tambah(): Menerima input nama dan nilai, memvalidasi nilai harus berupa angka, lalu menambahkan data ke self.data_nilai.

    - tampilkan(): Menampilkan seluruh data dalam format tabel yang rapi.

    - hapus(nama): Mencari data berdasarkan nama (tidak case-sensitive) dan menghapusnya menggunakan list comprehension.

    - ubah(nama): Mencari data berdasarkan nama (tidak case-sensitive) dan meminta input nilai baru untuk diperbarui.

## output
