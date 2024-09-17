# Tugas Praktikum 4

# 1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan output standar ke file baru
![so1](https://github.com/user-attachments/assets/52390658-250d-44c7-962d-737f5b2d8665)

Perintah ls -l menampilkan daftar file dan direktori. Simbol > digunakan untuk mengalihkan output ke file baru bernama daftar_direktori.txt. 
Daftar file dan direktori dari direktori aktif akan tersimpan dalam daftar_direktori.txt.

![file baru](https://github.com/user-attachments/assets/6372fbd8-7495-43cb-8cde-48084fa0914c)


# 2. Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
![so2](https://github.com/user-attachments/assets/4bcea3d6-d9b1-464c-836f-07f4eff01539)

Menggunakan >> untuk menambahkan hasil (append) ke file daftar_direktori.txt tanpa menghapus isinya.
Hasil ls -l /etc/passwd ditambahkan ke file daftar_direktori.txt.

# 3. Urutkan file baru dengan cara membelokkan standard input.  
![so3](https://github.com/user-attachments/assets/540c4cc3-9a4c-4c9e-8ac3-74dedae8dde1)

Perintah sort digunakan untuk mengurutkan isi file. Simbol < mengarahkan file daftar_direktori.txt sebagai input untuk sort.

Outputnya :
Isi dari daftar_direktori.txt akan diurutkan dan ditampilkan di layar.

![file urut](https://github.com/user-attachments/assets/9c3e6455-40af-47cd-ae44-2788842268d3)

# 4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut. 
![so4](https://github.com/user-attachments/assets/54312381-1433-4af0-8c9e-95059ff3ddb7)

Perintah ini mengurutkan isi daftar_direktori.txt dan mengarahkan output yang sudah diurutkan ke file baru bernama file_baru.urut.
Isi dari daftar_direktori.txt yang sudah diurutkan akan tersimpan di file_baru.urut.

# 5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.  
![so5](https://github.com/user-attachments/assets/bbc5a956-bb46-46ac-b71f-e5ad87f15f98)

- Perintah mkdir latihan6 digunakan untuk membuat direktori bernama latihan6.
- Karena direktori sudah dibuat pada perintah pertama, ketika mencoba membuat lagi, akan ada error yang dialihkan dengan 2> ke file rmdirerror.txt.
- Pada perintah kedua, 2>> digunakan untuk menambahkan error (append) tanpa menimpa isi file rmdirerror.txt.

# 6. Urutkan kalimat berikut :  
![so6](https://github.com/user-attachments/assets/425090bd-1fd7-44e3-b7ad-2efdded662d0)

Jakarta  
     Bandung  
     Surabaya  
     Padang  
     Palembang  
     Lampung  
     Dengan menggunakan notasi here document (<@@@ …@@@) 
sort <<@@@ memulai notasi here document, yang memungkinkan input multi-baris dimasukkan langsung ke dalam perintah. Setelah kata @@@, perintah akan dijalankan.
Outputnya:
Kalimat-kalimat tersebut akan diurutkan secara alfabetis:
- Bandung
- Jakarta
- Lampung
- Padang
- Palembang
- Surabaya


# 7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru. 
![so7](https://github.com/user-attachments/assets/74ee542d-83f1-4ba8-8220-f2340473463f)

Perintah wc (word count) menghitung jumlah baris, kata, dan karakter dalam file_baru.urut, dan >> menambahkan hasilnya ke file_baru.txt.
Output:
Informasi tentang jumlah baris, kata, dan karakter dari file_baru.urut akan ditambahkan ke file_baru.txt.

# 8. Gunakan perintah di bawah ini dan perhatikan hasilnya. 
![so8](https://github.com/user-attachments/assets/421ff33d-af2b-4dae-b87a-351af2fd51b7)

$ cat /etc/passwd | sort | pr –n | grep tty03  
$ find /etc –print | head  
$ head /etc/passwd | tail –5 | sort 
Penjelasan:      
# $ cat /etc/passwd | sort | pr –n | grep tty03
- cat /etc/passwd menampilkan isi file /etc/passwd.
- sort mengurutkan outputnya.
- pr -n menambahkan nomor baris pada hasil.
- grep tty03 mencari baris yang mengandung kata tty03.

# $ find /etc –print | head
- find /etc –print mencari semua file dan direktori di bawah /etc.
- head menampilkan 10 baris pertama dari hasil pencarian.
Output:
10 file atau direktori pertama yang ditemukan di bawah /etc akan ditampilkan.

# $ head /etc/passwd | tail –5 | sort
- head /etc/passwd mengambil 10 baris pertama dari /etc/passwd.
- tail -5 mengambil 5 baris terakhir dari output head.
- sort mengurutkan baris-baris tersebut.
Output:
5 baris terakhir dari 10 baris pertama dalam file /etc/passwd akan diurutkan secara alfabetis.

# 9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.  
![so9](https://github.com/user-attachments/assets/498dd06e-c080-4efe-ac41-2fc1aacc27fd)

Penjelasam:
-  'who' menampilkan siapa yang sedang login ke sistem.
- Dua kali 'cat' tidak mengubah output apapun.
- 'sort' mengurutkan output dari who.
- 'pr' memformat output menjadi kolom-kolom.
- 'head' mengambil 10 baris pertama dari hasil yang diformat.
- 'cat' | 'tail' mengambil 10 baris terakhir (atau lebih jika diubah) dari output sebelumnya.
