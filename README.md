:octocat: PROGRAM UNTUK MENGINPUT DATA MAHASISWA :octocat:

FLOWCHART PROGRAM :

![flowchart05](https://user-images.githubusercontent.com/57025775/70371165-4d8df780-1902-11ea-8ca9-cf27741048bb.jpg)

CODE PROGRAM  :

    datamahasiswa={}
    while True:
        print("DAFTAR NILAI MAHASISWA")
        c=input("L)ihat, T)ambah, U)bah, H)apus, C)ari, K)eluar: ")
        if c.lower()=='k':
            break
        elif c.lower()=='l':
            print("DATA MAHASISWA")
            print(57 * "=")
            print("| NO |   NAMA   |    NIM    | TUGAS | UTS | UAS | AKHIR |")
            print(57*"=")
            i=0
            for x in datamahasiswa.items():
                i+=1
                        #no     #nama   #nim   #tugas #uts  #uas    #akhir
                print("|{6:4}|{0:10s}|{1:11}|{2:7d}|{3:5d}|{4:5d}|{5:7.2f}|"
                    .format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
                             #nama  #nim    #tugas   #uts   #uas  #akhir  #no
            print(57*"=")
        elif c.lower()=='t':
            print("silakan masukan data ")
            nama=input("Nama : ")
            nim=input("NIM : ")
            tugas=int(input("Nilai Tugas : "))
            uts=int(input("Nilai Uts : "))
            uas =int(input("Nilai Uas : "))
            persentugas=tugas*30/100
            persenuts=uts*35/100
            persenuas=uas*35/100
            akhir=((tugas)*30/100+(uts)*35/100+(uas)*35/100)
            datamahasiswa[nama]=nim,tugas,uts,uas,akhir
        elif c.lower()=='u':
            print("EDIT DATA")
            nama=input("MASUKAN NAMA YANG INGIN DI RUBAH : ")
            if nama in datamahasiswa.keys():
                nim = input("NIM : ")
                tugas = int(input("Nilai Tugas : "))
                uts = int(input("Nilai Uts : "))
                uas = int(input("Nilai Uas : "))
                datamahasiswa[nama] = nim, tugas, uts, uas, akhir
            else:
                print("Nama {0} tidak ada ".format(nama))
        elif c.lower()=='h':
            print("HAPUS KONTAK")
            nama = input("Nama : ")
            if nama in datamahasiswa.keys():
                del datamahasiswa[nama]
            else:
                print("Nama {0} tidak ada dalam data".format(nama))
        elif c.lower()=='c':
            nama = input("MASUKAN NAMA YANG INGIN DI CARI : ")
            if nama in datamahasiswa.keys():
                print("Data",nama,"adalah :")
                print("|   NIM   | Tugas | Uts | Uas | Akhir |")
                print("{1}".format(nama,datamahasiswa[nama]))
            else:
                print("Nama {0} tidak ada dalam data".format(nama))
        else:
            print("Silakan pilih menu ")


ALUR ALGORITMA PROGRAM :

1. Buat perintah untuk memasukan dictionary kosong, lalu masukan perintah "While true" agar program melakukan perulangan tanpa batas dan masukan perintah untuk menginput menu. 

2. Buat perintah "if" untuk membuat perulangan berhenti (break) ketika input dari menu yang di tampilkan adalah “K”.

3. Lalu buat perintah "elif" dan masukan perintah untuk menampilkan list ketika input menu adalah “L” dan buat perulangan "for" agar bisa menampilkan semua data yang sudah di input. 

4. Buat perintah "elif" untuk membuat perintah input data dari nilai mahasiswa ketika input menu adalah “T” dan buat perhitungan nilai dengan persentasi yang di inginkan untuk menampilkan nilai akhir. 

5. Buat perintah "elif" dan untuk membuat perintah edit data atau mengubah data yang sudah ada ketika input menu adalah “U” lalu buat buat perintah "if" agar kita bisa mencari nama yang ingin di ubah dan "else" jika data tersebut tidak ada. 

6. Buat perintah "elif" untuk menghapus salah satu data nilai dari nama mahasiwa ketika input menu adalah “H” dengan cara menggunakan perintah "if" dan "else" jika nama tersebut tidak ada.

7. Buat perintah "elif" untuk mencari data yang ada ketika input menu adalah “C” dengan menggunkan perintah "if" dan "else" jika nama tersebut tidak ada.

8. Terakhir perintah else jika input menu tidak ada dalam menu.

HASIL PROGRAM :

![5n1](https://user-images.githubusercontent.com/57025775/70382418-778cfb80-198e-11ea-8c4e-213f3d0ad182.jpg)


Demikian program sederhana untuk menginput data mahasiswa, semoga bermanfaat :octocat:

