# GRAY_UTS
# uts-algoritma
# project kasir
### NAMA : GRAYVEN CHRIVIO WANGKE
### NIM : 312410435
### KELAS : TI.24.A.3

# Penjelasan mengenai project kasir ini
Mempunyai fitur pada kasir seperti :

a. Menambah barang ke dalam keranjang.

b. Menampilkan daftar barang.

c. Menghitung total harga.

d. Mencetak struk.

# Code Codingan Project Kasir 
```
class Item:
    def __init__(self, nama, harga, jumlah):
        self.nama = nama
        self.harga = harga
        self.jumlah = jumlah

    def total_harga(self):
        return self.harga * self.jumlah


class Keranjang:
    def __init__(self):
        self.barang = []

    def tambah_barang(self, item):
        self.barang.append(item)

    def tampilkan_daftar_barang(self):
        print("Daftar Barang di Keranjang:")
        for i, item in enumerate(self.barang, start=1):
            print(f"{i}. {item.nama} - Harga: {item.harga} - Jumlah: {item.jumlah} - Total: {item.total_harga()}")

    def hitung_total_harga(self):
        return sum(item.total_harga() for item in self.barang)

    def cetak_struk(self):
        print("===== STRUK PEMBELIAN =====")
        self.tampilkan_daftar_barang()
        print(f"Total Harga: {self.hitung_total_harga()}")
        print("===========================")


# Contoh penggunaan
keranjang = Keranjang()

# Menambah barang ke dalam keranjang
keranjang.tambah_barang(Item("Arbal", 50000, 1))
keranjang.tambah_barang(Item("Cipur", 15000, 1))
keranjang.tambah_barang(Item("Tuak", 45000 , 2))

# Menampilkan daftar barang
keranjang.tampilkan_daftar_barang()

# Menghitung total harga
total_harga = keranjang.hitung_total_harga()
print(f"Total Harga: {total_harga}")

# Mencetak struk
keranjang.cetak_struk()

```

# Contoh Hasil Dari Codingan Project
![Screenshot 2024-11-08 091738](https://github.com/user-attachments/assets/bfe8cb6b-3da7-4a2e-a05b-41e744d51472)



# Penjelasan Singkat Mengenai Algoritma Pada Project Kasir 

- Membuat kelas Barang: Kelas Barang menyimpan data tentang barang, termasuk nama, harga satuan, dan jumlah.

- Membuat kelas Keranjang: Kelas Keranjang menyimpan daftar barang yang dibeli dan menyediakan fungsi untuk menambah barang, menampilkan barang, menghitung total harga, dan mencetak struk.

- Menambahkan barang ke keranjang: Program meminta pengguna untuk memasukkan nama barang, harga satuan, dan jumlah, lalu membuat objek Barang baru dengan data tersebut dan menambahkannya ke dalam keranjang.

- Menampilkan daftar barang: Program menampilkan daftar barang yang ada di keranjang, termasuk nama, harga satuan, jumlah, dan total harga per barang.

- Menghitung total harga: Program menghitung total harga semua barang di keranjang.

- Mencetak struk: Program mencetak struk yang berisi daftar barang, total harga, dan ucapan terima kasih.
