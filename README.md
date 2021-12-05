# Labspy5
Modul praktikum 5 ini berisikan latihan menggunakan dictionary pada python, dan juga praktikum membuat Program Daftar Nilai Mahasiswa menggunakan dictionary dan juga menampilkan pilihan menu antara lain: Ubah, Tambah, Hapus, Cari, Lihat!

# Latihan 


### Latihan yang pertama adalah membuat daftar kontak dengan menggunakan dictionary pada python
- berikut gambaran source code nya:
![Screenshot (107)](https://user-images.githubusercontent.com/92356397/144733979-6fca0264-986a-4678-bc57-928efd4ffc9b.png)
![Screenshot (108)](https://user-images.githubusercontent.com/92356397/144734014-b931e98f-1daf-4383-9992-1fcbaf46b771.png)


Dengan penjelasan source code sebagai berikut:
- Dibawah ini adalah untuk menampung data dari dictionary

```python
daftarkontak = {"Nama":"Nomor Telepon"}
kontak = {'Ari':'081267888', 'Dina':'087677776'}
```

- Sedangkan code dibawah adalah untuk mengakses atau menampilkan kontak yang telah ditampung dalam data dictionary tersebut

```python
print("="*30)
print("   Nama     |    Nomor Telepon   ")
print("="*30)
print(" # Ari   |   ",kontak['Ari'])
print(" # Dina  |   ",kontak['Dina'])
print("="*30)
```

- berikut hasil programnya:

![Screenshot (115)](https://user-images.githubusercontent.com/92356397/144736423-5d3789cb-1cde-4a6f-8a7b-7fd8a1bb778c.png)

- Code dibawah ini adalah untuk menampilkan salah satu dari daftar kontak yang ada, dibawah yang akan di tampilkan adalah daftar kontak Ari

```python
print("Menampilkan kontak Ari")
print("="*30)
print(" # Ari   |   ",kontak['Ari'])
print("="*30)
```

- berikut hasil programnya:

![Screenshot (116)](https://user-images.githubusercontent.com/92356397/144736463-c4261578-93d9-415f-a8db-cbceb3b74200.png)

- Code dibawah ini untuk menambahkan kontak dengan nama Riko dan nomor 087654544

```python
print("Menambah kontak dengan dana Riko dan Nomor Telepon 087654544")
kontak['Riko']='087654544'
print("="*30)
print("  Riko   |   ",kontak['Riko'])
print("="*30)
```

- berikut hasil programnya:

![Screenshot (118)](https://user-images.githubusercontent.com/92356397/144736658-2946dd12-5568-460a-92f8-7b054a9a8f23.png)

- Code dibawah untuk mengubah kontak Dina dengan nomor baru 0889999776

```python
print("Mengubah kontak Dina dengan nomor baru 0889999776")
kontak['Dina']='0889999776'
print("="*30)
print(" # Dina  |   ",kontak['Dina'])
print("="*30)
```

- berikut hasil programnya:

![Screenshot (117)](https://user-images.githubusercontent.com/92356397/144736809-6bf854de-3e7f-4d6e-9f90-766143090931.png)

- Code dibawah untuk menampilkan semua nama yang ada dalam daftar kontak

```python
print("Menampilkan semua nama")
print("="*30)
print(kontak.keys())
print("="*30)
```

- berikut hasil programnya:

![screenshot](https://user-images.githubusercontent.com/92356397/144736889-2331e715-e1e7-4b25-ad05-079725fd02a1.jpeg)

 Code berikut untuk menampilkan semua nomor yang ada dalam daftar kontak

```python
print("Menampilkan semua nomor")
print("="*30)
print(kontak.values())
print("="*30)
```

- berikut hasil programnya:

![WhatsApp Image 2021-12-05 at 13 30 40](https://user-images.githubusercontent.com/92356397/144737088-95dd8000-df98-4e5c-bce6-cc27a01c833f.jpeg)

- Code berikut untuk menampilkan semua daftar kontak beserta nama dan nomornya

```python
print("Menampilkan daftar nama dan nomor")
print("="*30)
print(kontak.items())
print("="*30)
```

- berikut hasil programnya:

![Screenshot (119)](https://user-images.githubusercontent.com/92356397/144737183-d93d36b5-e42d-4e85-b6b3-8a142b2a7bde.png)

- Code dibawah untuk menghapus kontak Dina yang tersimpan dalam daftar kontak

```python
print("Hapus kontak Dina")
kontak.pop('Dina')
print("="*30)
print(kontak.items())
print("="*30)
```

- berikut hasil programnya:

![Screenshot (120)](https://user-images.githubusercontent.com/92356397/144737198-a34ae5a0-4eaa-44bd-892b-a1b43819988d.png)


# Praktikum

### Dibawah ini adalah program sederhana untuk membuat daftar nilai mahasiswa dengan menggunakan dictionary, dan menampilkan pilihan menu tambah, ubah, cari, hapus, dan lihat

- berikut gambaran code source nya:

![Screenshot (108)](https://user-images.githubusercontent.com/92356397/144737334-006bfef1-4f01-436f-a067-cfd92adb2c31.png)

- berikut dengan flowchart programnya:

![flowchart_daftar_nilai_mahasiswa](https://user-images.githubusercontent.com/92356397/144738336-a8cc7309-b888-4eca-adb5-0cad023e44fd.png)

Dengan penjelasan source code sebagai berikut:
- Code dibawah ini untuk membuat dictionary kosong, untuk menampung dictionary dengan menggunakan tuple

```python
a = {}
```

- Code dibawah ini untuk perulangan while, dan juga untuk menginisialkan penambahan menu pilihan Tambah, Ubah, Hapus, Cari, Lihat dan Keluar:

```python
while True:
    x = input("(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")
```

- Code dibawah adalah untuk syntax penambahan data, dengan ketentuan jika kita mengetikkan 't' pada keyboard, maka akan melakukan penambahan data dan ditampung kedalam dictionary 'a' yang telah kita buat, dengan nama sebagai keys, dan yang lainnya sebagai values

```python
    if x.lower() == 't':
        print("Tambah Data")
        nama = input("Nama           : ")
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        n_akhir = tugas * 0.30 + uts * 0.35 + uas * 0.35
        a[nama] = nim, uts, uas, tugas, n_akhir
```

- Code dibawah adalah untuk syntax mengubah data, dengan ketentuan jika kita mengetikkan 'u' pada keyboard, maka akan melakukan perubahan data yang telah di tampung ke dalam dictionary 'a' yang telah kita buat, tetapi data yang dapat diubah hanya data yang berupa values nya saja

```python
    elif x.lower() == 'u':
        print("Ubah Data")
        nama = input("Masukkan Nama   : ")
        if nama in a.keys():
            nim = int(input("NIM            : "))
            uts = int(input("Nilai UTS      : "))
            uas = int(input("Nilai UAS      : "))
            tugas = int(input("Nilai Tugas    : "))
            n_akhir = tugas*0.30 + uts*0.35 + uas*0.35
            a[nama] = nim, uts, uas, tugas, n_akhir
        else:
            print("Nama{0} Tidak Ditemukan".format(nama))
```

- Code dibawah adalah untuk syntax penghapusan data, dengan ketentuan jika kita mengetikkan 'h' pada keyboard, maka akan melakukan penghapusan data yang telah kita masukkan kedalam dictionary 'a' yang telah kita buat dengan statemen ```del a[nama]```

```python
    elif x.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in a.keys():
            del a[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

- Code dibawah adalah untuk syntax pencarian data, dengan ketentuan jika kita mengetikkan 'c' pada keyboard, maka akan melakukan pencarian data dengan memasukkan keys dari data yang telah kita masukkan kedalam dictionary 'a' yang telah kita buat

```python
    elif x.lower() == 'c':
        print("Cari Data")
        nama = input("Masukkan Nama : ")
        if nama in a.keys():
            print("=" * 73)
            print("|                             Daftar Mahasiswa                          |")
            print("=" * 73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("=" * 73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, n_akhir))
            print("=" * 73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

- Code dibawah adalah untuk syntax melihat data, dengan ketentuan jika kita mengetikkan 'l' pada keyboard, maka akan menampilkan keseluruhan dari data yang telah kita masukkan dan ditampung ke dalam dictionary 'a' yang telah kita buat

```python
    elif x.lower() == 'l':
        if a.items():
            print("=" * 78)
            print("|                               Daftar Mahasiswa                             |")
            print("=" * 78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("=" * 78)
            i = 0
            for y in a.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(y[0][:13], y[1][0], y[1][1], y[1][2], y[1][3], y[1][4], no=i))
                print("=" * 78)
```

- Code dibawah adalah untuk menampilkan 'TIDAK ADA DATA', jika kita belum pernah memasukkan data kedalam dictionary 'a'

```python
        else:
            print("=" * 78)
            print("|                               Daftar Mahasiswa                             |")
            print("=" * 78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("=" * 78)
            print("|                                TIDAK ADA DATA                              |")
            print("=" * 78)
```

- sedangkan code dibawah adalah untuk syntax keluar dari program, untuk menghentikan program, dengan ketentuan jika kita mengetikkan 'k' pada keyboard, maka akan keluar dari program tersebut

```python
    elif x.lower() == 'k':
        break
```

- Dan code yang terakhir adalah untuk syntax jika kita mengetikkan pada keyboard selain dari huruf yang telah di definisikan di atas seperti 't', 'u', 'h', 'c', 'l', dan 'k', maka akan menampilkan Pilih Menu Yang Tersedia

```python
    else:
        print("Pilih Menu Yang Tersedia")
```
### Berikut hasil program praktikum, jika programnya di jalankan

- Menambahkan Data dengan syntax 't' dan melihat data dengan syntax 'l'

![Screenshot (109)](https://user-images.githubusercontent.com/92356397/144738270-854d0017-b87d-4324-abcc-a8cf3c1b382d.png)

![Screenshot (110)](https://user-images.githubusercontent.com/92356397/144738943-a42ec07c-53ba-4323-b15e-a88b7c79ad35.png)

- Mengubah data dengan syntax 'u', dan melihat data dengan syntax 'l'

![Screenshot (111)](https://user-images.githubusercontent.com/92356397/144738987-9b4b7c57-0541-4a6c-a303-61181afe1d12.png)

- Mencari data dengan syntax 'c', dan melihat data dengan syntax 'l'

![Screenshot (112)](https://user-images.githubusercontent.com/92356397/144739348-48bcab5a-f975-4e7c-87c6-d81dae86356f.png)

- Menghapus data dengan syntax 'h' dan melihat data dengan syntax 'l'

![Screenshot (113)](https://user-images.githubusercontent.com/92356397/144739387-74798e71-6334-4546-aead-4bd30641b798.png)

- Keluar dari program dengan syntax 'k'

![screenshot(114)](https://user-images.githubusercontent.com/92356397/144739462-9e136170-c0a5-422e-8de6-8755d93f6005.png)



#### Sekian praktikum modul 5  
##### Terima Kasih
