# Praktikum6
Anggita Risqi Nur Clarita (312210450)

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Latihan|[Click Here](#latihan)|
|2|Praktikum 6|[Click Here](#praktikum-6)|
|3|Flowchart Praktikum 6|[Click Here](#flowchart-praktikum-6)|

## Latihan
* Buat Dictionary daftar kontak (Nama sebagai key, dan nomor sebagai value)
* Tampilkan kontaknya Ari
* Tambah kontak baru dengan nama Riko, nomor 087654544
* Ubah kontak Dina dengan nomor baru 088999776
* Tampilkan semua Nama
* Tampilkan semua Nomor
* Tampilkan daftar Nama dan Nomornya
* Hapus kontak Dina

### Rumusnya
```python
# Latihan
print("Nama : Anggita Risqi Nur Clarita")
print("NIM  : 312210450")

daftarkontak = {"Nama": "Nomer Telepon"}
kontak = {'Ari': '081267888', 'Dina': '087677776'}

# print
print("============================")
print("|   # Nama   |Nomor Telepon|")
print("============================")
print("|   # Ari    |  ", kontak['Ari'], '|')
print("|   # Dina   |  ", kontak['Dina'], '|')
print("============================")
print()

# Tampilkan kontaknya Ari
print("# Tampilkan kontaknya Ari")
print("===========================")
print("|    Ari     | ", kontak['Ari'], '|')
print("===========================")
print()

# Tambah kontak baru dengan nama Riko, nomor 087654544
print("# Tambah kontak baru dengan nama Riko, nomor 087654544")
kontak['Riko'] = '087654544'
print("===========================")
print("|    Riko    | ", kontak['Riko'], '|')
print("===========================")
print()

# Ubah kontak Dina dengan nomor baru 088999776
print("# Ubah kontak Dina dengan nomor baru 088999776")
kontak['Dina'] = '088999776'
print("===========================")
print("|    Dina    | ", kontak['Dina'], '|')
print("===========================")
print()

# Tampilkan semua Nama
print("# Tampilkan semua Nama")
print("==================================")
print(kontak.keys())
print("==================================")
print()

# Tampilkan semua Nomor
print("# Tampilkan semua Nomor")
print("====================================================")
print(kontak.values())
print("====================================================")
print()

# Tampilkan daftar Nama dan nomornya
print("# Tampilkan daftar Nama dan nomornya")
print("================================================================================")
print(kontak.items())
print("================================================================================")
print()

# Menghapus kontak Dina
print("# Hapus kontak Dina")
print("=========================================================")
kontak.pop('Dina')
print(kontak.items())
print("=========================================================")
```

### Programnya
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/1.png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/2.png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/3.png)

### Hasil dari programnya (RUN)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/4.png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/5.png)


## Praktikum 6
Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan
* Program dibuat dengan menggunakan _Dictionary_
* Tampilkan menu pilihan : (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
* Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, uts : 35%, uas : 35%)
* Buat Flowchart dan Penjelasan Programnya pada README.md.
* Commit dan push repository ke github.

### Rumusnya
```python
# Praktikum 6
print("Nama : Anggita Risqi Nur Clarita")
print("NIM  : 312210450")

data = {}
while True :
    print("")
    j = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
# untuk Keluar Dari Program
    if j.lower() == "k":
        print("Keluar Dari Program")
        break
# untuk melihat-lihat
    elif j.lower() == "l":
        if data.items():
            print("Daftar Nilai")
            print()
            print("=============================================================================================");
            print("|  No  |    Nama    |      NIM      |    Tugas    |     UTS     |     UAS     | Nilai Akhir |");
            print("=============================================================================================");
            i = 0
            for x in data.items():
                i+=i
                print("|  1   | {0:9}  |   {1:9}   |  {2:9}  |  {3:9}  |  {4:9}  |  {5:9}  |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
                print("=============================================================================================");
                print("")
        else :
            print("Daftar Nilai")
            print()
            print("=============================================================================================");
            print("|  No  |    Nama    |      NIM      |    Tugas    |     UTS     |     UAS     | Nilai Akhir |");
            print("=============================================================================================");
            print("|                                      TIDAK ADA DATA                                       |");
            print("=============================================================================================");
# Untuk Menambahkan Data
    elif j.lower() == "t":
        print("Tambah Data")
        nama  = input    ("Nama       : ")
        nim   = input    ("NIM        : ")
        tugas = int(input("Nilai Tugas: "))
        uts   = int(input("Nilai UTS  : "))
        uas   = int(input("Nilai UAS  : "))
        nilaiakhir = ((tugas)*30/100+(uts)*35/100+(uas)*35/100)
        data[nama] = [nim, tugas, uts, uas, nilaiakhir]
# Untuk Mengubah data
    elif j.lower() == "u":
        print("Edit Data Nilai Mahasiswa")
        nama  = input    ("Nama       : ")
        if nama in data.keys():
            nim   = input    ("NIM        : ")
            tugas = int(input("Nilai Tugas: "))
            uts   = int(input("Nilai UTS  : "))
            uas   = int(input("Nilai UAS  : "))
            nilaiakhir = ((tugas)*30/100+(uts)*35/100+(uas)*35/100)
            data[nama] = [nim, tugas, uts, uas, nilaiakhir]
        else:
            print("Data nilai{0} tidak ada".format(nama))
# Untuk Menghapus Data
    elif j.lower() == "h":
        print("Hapus Data Nilai Mahasiswa")
        nama  = input    ("Nama       : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data {0} tidak ada".format(nama))
# Untuk Mencari Data
    elif j.lower() == "c":
        print("Cari Data Nilai Mahasiswa")
        nama  = input    ("Nama       : ")
        if nama in data.keys():
            print("")
            print("=====================================================================================");
            print("|   {0}   |   {1}   |".format(nama, data[nama]))
            print("=====================================================================================");
        else:
            print("Datanya {0} tidak ada".format(nama))
    else:
        print()
        print("=====================================================================================");
        print("|  No  |     Nama     |     NIM     |   Tugas   |   UTS   |   UAS   |  Nilai Akhir  |");
        print("=====================================================================================");
        print("|                                   TIDAK ADA DATA                                   ");
        print("=====================================================================================");
else:
    print("Pilih Menu Yang Tersedia")
```

### Programnya
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(1).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(2).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(3).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(4).png)

### Hasil dari programnya (RUN)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(5).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(6).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(7).png)
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/Praktikum6%20(8).png)

### Penjelasan programnya
1. Definisikan dictionary terlebih dahulu _data = {}_.
2. Gunakanlah perulangan _While True_ untuk menampilkan data sebanyak banyaknya.
3. Lalu Masukkan perintah _j = input("(T)ambah, (U)bah, (H)apus, (L)ihat,(C)ari, (K)eluar: ")_, untuk mendapatkan perintah Tambah, Ubah, Hapus, Lihat, Cari, dan Keluar.
4. Untuk menambahkan data pilih _"tambah"_ gunakan fungsi _elif_ gunakan perintah _"t"_, lalu masukan nama, nim, tugas, uts, uas, nilaiakhir, nilai akhir didapat dari _= ((tugas)*30/100 + (uts)*35/100 + (uas)*35/100_.
5. Lalu jika ingin memilih "lihat" gunakan fungsi _'elif'_ dan gunakan fungsi _'for x in data.items():'_ untuk melihat data pada tabel data yang kita inputkan, dengan perintah _"l"_. Jika data tidak terdaftar maka akan tampil _"TIDAK ADA DATA"_ atau = 0.
6. Untuk menampilkan pilihan _"hapus"_ gunakan fungsi _'elif'_ kemudian gunakan fungsi _'if nama in data.keys():'_ kemudian fungsi _'del.data[nama]_ jika nama yang kita hapus tidak ada dalam tabel maka gunakan fungsi _'else'_ untuk menampilkan _"TIDAK ADA DATA"_.
7. Lalu untuk menampilan pilihan _"cari"_ gunakan fungsi _'elif'_ kemudian gunakan fungsi _'if nama in data.keys():'_ untuk mencari data nama kemudian gunakan fungsi _'else'_ untuk menampilkan data nama yang kita cari tidak ada.
8. Lalu jika ingin keluar dari program gunakan fungsi _'if'_ kemudian gunakan fungsi _break_ untuk keluar dari data nilai atau menghentikan program.
9. Selesai

### Flowchart Praktikum 6
![image](https://github.com/AnggitaRisqiNC/Praktikum6/blob/main/screenshot/flowchart%20praktikum%206.png)

## Finish