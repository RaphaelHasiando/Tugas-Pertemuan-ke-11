# Tugas-Pertemuan-ke-11
![image](https://user-images.githubusercontent.com/61907877/145710800-4d0370cd-aea8-467d-bc75-00cb2bcde8d3.png)
## ==========================================================
1 - Buatlah variable dictionary untuk menyimpan nilai data (dalam pasangan kunci:nilai)
###
    Data = {
      "Rahmat": 80
    }
2 - 4 function untuk menambahkan, menampilkan, menghapus, dan mengubah
###
    def function (parameter) :
        function code
## def tambah()
3 - Buatlah variable untuk meng-input Nama dan Nilai baru
###
    def tambah():
      Name = input("Masukkan Nama anda : ")
      Value = input("Masukkan Nilai anda : ")
4 - Gunakan if else statement untuk memeriksa apabila Nama-nama di dalam Data sama dengan Nama yang Anda masukkan. Jika Nama itu tidak sama, maka Nama dan nilai yang dimasukkan akan disimpan ke dalam Data
###
    def tambah():
      Name = input("Masukkan Nama anda : ")
      if Name in list(Data):
        print("Nama yang anda masukkan sudah terdaftar")
      else:
        Value = input("Masukkan Nilai anda : ")
        Data[Name] = int(Value)
## def tampilkan()
5 - Pada tahap ini, data yang berisi akan ditampilkan. Dengan itu, Gunakan for loop pada setiap Data yang diisi
###
    def tampilkan():
      print("============ Data Universal ============")
      for i in range(len(Data)):
        print(f"Nama : {list(Data.keys())[i]} | Nilai : {Data[list(Data.keys())[i]]}")
      print("========================================")
## def hapus(nama)
6 - Gunakan if else statement untuk menghapus Data berdasarkan nama. Setelah itu, Gunakan parameter (diikuti dengan tanda kurung). Contoh berikut memiliki function dengan satu argumen (name).
###
    def hapus(nama):
      if nama in list(Data):
        del Data[nama]
      else:
        print("Nama yang Anda masukkan tidak ditemukan")
Saat function dipanggil, akan mejalankan 'del Data [nama]', yang digunakan di dalam fungsi untuk menghapus Nama dan nilai
## def ubah(nama)
7 - Gunakan perulangan (while loop) dan 'try,except' untuk mengulang jika data yang diisi mendapatkan nilai yang error.
###
    def ubah(nama):
      while True:
        try:
          Data[nama] = int(input(f"Nilai {nama} = "))
          break
        except:
          print("Pengisian harus dalam bentuk angka!")
Ketika terjadi kesalahan, atau pengecualian, function tersebut akan berhenti dan menghasilkan pesan kesalahan.
###
8 - Buatlah perulangan (while loop) dan variable input() untuk menampilkan menu pilihan
###
    while True:
      Pilih = input("T(tambah) | P(Tampil) | (H)Hapus | U(ubah) | K(Keluar) : ")
9 - Ketika nilai itu (Pilih) adalah T, Menambahkan Data baru dengan memanggil fungsi 'tambah()'. Dan ketika nilai itu adalah P, fungsi tersebut akan menampilkan data yang terisi dengan nama dan nilai jika memanggilkan fungsi 'tampilkan()'
###
    while True:
      Pilih = input("T(tambah) | P(Tampil) | (H)Hapus | U(ubah) | K(Keluar) : ")
      if Pilih == "T" or Pilih == "t":
        tambah()

      elif Pilih == "P" or Pilih == "p":
        tampilkan()
10- Hapus -> Gunakan for loop untuk menampilkan beberapa Nama yang terdaftar dalam Data. Setelah itu, dengan memanggil fungsi 'hapus()', Gunakan fungsi input ke dalam parameter hapus()
###
      elif Pilih == "H" or Pilih == "h":
        for m in range(len(Data)):
          print(f'{m + 1}. {list(Data.keys())[m]}')
        hapus(input("Pilih dan Ketik Nama ingin dihapus : "))
Fungsi input itu dikategorikan sebagai argumen untuk fungsi hapus()
11- Ubah -> Gunakan for loop untuk menampilkan beberapa Nama yang terdaftar dalam Data. Lalu, buatlah variable baru (mengambil nilai input) dan gunakan if else statement.
###
    elif Pilih == "U" or Pilih == "u":
      for m in range(len(Data)):
        print(f'{m + 1}. {list(Data.keys())[m]}')
      change = input("Pilih dan Ketik Nama ingin diubah : ")
      if change in list(Data.keys()):
        ubah(change)
      else:
        print("Nama yang Anda masukkan tidak ditemukan")
12- Terakhir, Gunakan fungsi 'break' untuk mengakhiri program / perulangan (while loop)
###
      elif Pilih == "K" or Pilih == "k":
        break
![Untitled Diagram drawio (1)](https://user-images.githubusercontent.com/61907877/145726384-caa8060e-5dd4-491b-9411-63dadf1e12ea.png)
![image](https://user-images.githubusercontent.com/61907877/145756262-bfaed51b-3052-4a70-9bb2-376c14a55d9c.png)
![image](https://user-images.githubusercontent.com/61907877/145756594-5088c071-ac4c-4dab-a573-d5a4bb55aafb.png)
![image](https://user-images.githubusercontent.com/61907877/145756764-e186fad8-c3e7-410f-b611-06d08287d685.png)
