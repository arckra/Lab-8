# Tugas Bahasa Pemrograman Pertemuan ke-11


# DIAGRAM CLASS
![Diagram class](https://github.com/user-attachments/assets/10d783de-09a5-4987-8517-f5acef116fca)


# FLOWCHART


# PENJELASAN CODE

Berikut adalah penjelasan dari kode program Python yang telah dibuat untuk mengelola data mahasiswa, termasuk penjelasan tentang setiap bagian dari kode tersebut:

**1. Import dan Definisi Kelas**


```class Mahasiswa:
    def __init__(self):
        self.daftar_mahasiswa = []
```

- class Mahasiswa: Mendefinisikan kelas Mahasiswa yang akan digunakan untuk mengelola data mahasiswa.
- __init__: Merupakan metode konstruktor yang dipanggil saat objek dari kelas ini dibuat. Di sini, kita menginisialisasi atribut daftar_mahasiswa sebagai list kosong yang akan menyimpan data mahasiswa.


**2. Method tambah**


```def tambah(self, nama, nim, nilai):
    self.daftar_mahasiswa.append({'nama': nama, 'nim': nim, 'nilai': nilai})
    print(f"Data mahasiswa {nama} (NIM: {nim}) berhasil ditambahkan.")
```

- tambah(self, nama, nim, nilai): Method ini digunakan untuk menambahkan data mahasiswa baru ke dalam daftar.
- self.daftar_mahasiswa.append(...): Menambahkan dictionary yang berisi nama, nim, dan nilai mahasiswa ke dalam list daftar_mahasiswa.
- print(...): Menampilkan pesan konfirmasi bahwa data mahasiswa telah berhasil ditambahkan.


**3. Method tampilkan**


```def tampilkan(self):
    if not self.daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
        return
    print("Daftar Mahasiswa:")
    for index, mahasiswa in enumerate(self.daftar_mahasiswa, start=1):
        print(f"{index}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
```
        
- tampilkan(self): Method ini digunakan untuk menampilkan semua data mahasiswa yang ada dalam daftar.
- if not self.daftar_mahasiswa:: Memeriksa apakah daftar mahasiswa kosong. Jika kosong, program akan menampilkan pesan dan keluar dari method.
- enumerate(...): Menggunakan fungsi enumerate untuk mendapatkan indeks dan data mahasiswa saat iterasi. Indeks dimulai dari 1.
- print(...): Menampilkan informasi mahasiswa dalam format yang terstruktur.


**4. Method hapus**


```def hapus(self, nama):
    for mahasiswa in self.daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            self.daftar_mahasiswa.remove(mahasiswa)
            print(f"Data mahasiswa {nama} berhasil dihapus.")
            return
    print(f"Data mahasiswa {nama} tidak ditemukan.")
```
    
- hapus(self, nama): Method ini digunakan untuk menghapus data mahasiswa berdasarkan nama.
- for mahasiswa in self.daftar_mahasiswa:: Melakukan iterasi melalui daftar mahasiswa.
- if mahasiswa['nama'] == nama:: Memeriksa apakah nama mahasiswa yang ingin dihapus ada dalam daftar.
- self.daftar_mahasiswa.remove(mahasiswa): Menghapus mahasiswa dari daftar jika ditemukan.
- print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.


**5. Method ubah**


```def ubah(self, nama, nim_baru, nilai_baru):
    for mahasiswa in self.daftar_mahasiswa:
        if mahasiswa['nama'] == nama:
            mahasiswa['nim'] = nim_baru
            mahasiswa['nilai'] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah menjadi NIM {nim_baru} dan nilai {nilai_baru}.")
            return
    print(f"Data mahasiswa {nama} tidak ditemukan.")
```
    
- ubah(self, nama, nim_baru, nilai_baru): Method ini digunakan untuk mengubah data mahasiswa berdasarkan nama.
- if mahasiswa['nama'] == nama:: Memeriksa apakah nama mahasiswa yang ingin diubah ada dalam daftar.
- mahasiswa['nim'] = nim_baru dan mahasiswa['nilai'] = nilai_baru: Mengubah NIM dan nilai mahasiswa yang ditemukan.
- print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.


**6. Menu Interaktif**


```if __name__ == "__main__":
    mhs = Mahasiswa()
    
    while True:
        print("\nMenu:")
        print("1. Tambah Mahasiswa")
        print("2. Tampilkan Mahasiswa")
        print("3. Ubah Mahasiswa")
        print("4. Hapus Mahasiswa")
        print("5. Keluar")
        
        pilihan = input("Pilih menu (1-5): ")
        
        if pilihan
```


# PENJELASAN DIAGRAM CLASS

# Struktur Kelas

# 1. Kelas Mahasiswa
**Deskripsi**
- Kelas ini adalah inti dari manajemen data mahasiswa, bertanggung jawab untuk mengelola seluruh operasi pada data mahasiswa.

**Atribut**
- `daftar_mahasiswa` (private list): 
  - Menyimpan kumpulan data mahasiswa
  - Bersifat privat untuk melindungi integritas data

**Metode**
1. `__init__()`: 
   - Konstruktor kelas
   - Menginisialisasi list kosong untuk menyimpan data mahasiswa

2. `tambah(nama, nim, nilai)`:
   - Menambahkan mahasiswa baru ke dalam daftar
   - Menerima parameter nama, NIM, dan nilai
   - Membuat entri baru dalam daftar mahasiswa

3. `tampilkan()`:
   - Menampilkan seluruh data mahasiswa yang tersimpan
   - Menangani kasus daftar kosong
   - Menampilkan informasi setiap mahasiswa termasuk nama, NIM, dan nilai

4. `hapus(nama)`:
   - Menghapus data mahasiswa berdasarkan nama
   - Mencari mahasiswa dengan nama tertentu
   - Menghapus entri jika ditemukan
   - Memberikan konfirmasi atau pesan kesalahan

5. `ubah(nama, nim_baru, nilai_baru)`:
   - Mengubah data mahasiswa yang sudah ada
   - Mencari mahasiswa berdasarkan nama
   - Memperbarui NIM dan nilai
   - Memberikan konfirmasi perubahan

# 2. Kelas DataMahasiswa


**Deskripsi**
- Kelas ini merupakan struktur data untuk menyimpan informasi individual setiap mahasiswa.

**Atribut**
- `nama` (string): Nama lengkap mahasiswa
- `nim` (integer): Nomor Induk Mahasiswa 
- `nilai` (integer): Nilai akademik mahasiswa

# 3. Kelas Main


**Deskripsi**
- Kelas yang bertanggung jawab untuk menjalankan program dan berinteraksi dengan pengguna.

**Metode**
1. `main()`:
   - Fungsi utama untuk menjalankan program
   - Membuat instance kelas Mahasiswa
   - Memulai loop utama program

2. `tampilkan_menu()`:
   - Menampilkan pilihan menu kepada pengguna
   - Memudahkan interaksi dan navigasi program

3. `pilih_menu()`:
   - Memproses pilihan menu yang dipilih pengguna
   - Memanggil metode yang sesuai dari kelas Mahasiswa

# Hubungan Antar Kelas

**Komposisi (Mahasiswa  -- 0.. DataMahasiswa)**
- Kelas Mahasiswa mengandung beberapa objek DataMahasiswa
- Hubungan komposisi berarti objek DataMahasiswa tidak dapat eksis tanpa Mahasiswa
- Satu objek Mahasiswa dapat memiliki 0 atau lebih objek DataMahasiswa

**Asosiasi (Main ..> Mahasiswa)**
- Kelas Main menggunakan (uses) kelas Mahasiswa
- Main bergantung pada fungsionalitas Mahasiswa untuk menjalankan program
