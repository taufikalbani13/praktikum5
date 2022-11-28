# praktikum5

## Nama :Taufik Eka Albani
## Nim  :312210347
## Kelas:TI.22.A3


## Tugas Praktikum

Buat dictionary kosong
```
mahasiswa = {}
```
- Buat program untuk lihat data nya

```
def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")
        
    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")
```

```else``` digunakan untuk menampilkan yang terjadi jika Nama yang diketik tidak ada

- Buat program untuk Tambah Data nya

```
def add():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir
```

- Buat program untuk Hapus data

``` 
def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in mahasiswa.keys():
        del mahasiswa[nama]
    
    else:
        print("Nama tidak ditemukan")
```

- Buat program untuk Ubah data 

```
def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")
```

- Buat program untuk Cari data

```
def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
            .format (a , mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4] ))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")
```
program ini berbeda dengan melihat data, program ini akan memunculkan nama yang diketik pada input


- Buat program untuk menu nya

``` 
def menu():
   

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            Kode Yang Anda Masukan Tidak Valid")
```

Program berisikan menu, jika ketik L/T/U/H/C/K maka akan menjalankan perintah program program yang diketik di atas seperti ```show()```, ```add()```, ```update()```, ```delete()```, ```search()```

- Kode nya akan berjalan dengan perintah
``` 
while True:
    menu()
```
---
#### Output nya :


- Tambah Data

![TAMBAH](https://user-images.githubusercontent.com/115516830/204196041-41fdeb16-8da4-4515-85e6-b2f93fee2c1f.PNG)


- Lihat dengan data

![DAFTARNILAI1](https://user-images.githubusercontent.com/115516830/204197397-3888d474-6de3-45cd-ac54-75190c983d9f.PNG)



- Ubah Data

![UBAHDATA](https://user-images.githubusercontent.com/115516830/204197560-58d7e857-14b9-42f5-847b-059b25810a55.PNG)



- Hapus Data 
![HAPUSDATA](https://user-images.githubusercontent.com/115516830/204197632-3673de59-c34d-47ef-9d19-6909bfa7f336.PNG)





- Cari Data
![CARIDATA](https://user-images.githubusercontent.com/115516830/204197704-35e0e6ab-a42f-454d-85e4-49023f5dbd6f.PNG)



- Keluar

![EXIT](https://user-images.githubusercontent.com/115516830/204197775-cb791d13-dcb2-4a9e-8e77-5553aabe51eb.PNG)



- Flowchart

![flowchart](https://user-images.githubusercontent.com/115516830/204192439-ee8a4b06-d25a-4ad6-9f75-e4ba50a3163f.jpg)
