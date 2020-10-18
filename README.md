
# Laporan Resmi Praktikum Komunikasi Data dan Jaringan Komputer Modul 1  Kelompok T14

## Anggota Kelompok:

1. Hisyam Zulkarnain F – 05311840000019
2. Muhamad Rifaldi - 05311840000022
  
## A. Display Filter  

### Soal No. 1  

Sebutkan webserver yang digunakan ketika mengakses "testing.mekanis.me"!  

### Penyelesaian

1. Gunakan wireshark display filter expression    
  
```
http.host == testing.mekanis.me
```  

![Step 1](./images/No1/t1401.jpg/)

2. Klik kanan pada salah satu paket >> Follow >> TCP Stream

![Step 2](./images/No1/t1401b.jpg/)

### Soal No. 2

Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

### Penyelesaian

1. Gunakan wireshark display filter expression

```
HTTP
```

![Step 1](./images/No2/t1402.jpg/)

2. Pilih menu file >> Export Object >> http

![step 2](https://raw.githubusercontent.com/fvldi/Jarkom_Modul1_Lapres_T14/main/images/No2/t1402be.jpg)

3. Cari file gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg", kemudian Save.

![step 3](./images/No2/t1402c.jpg/)

4. Buka file gambar, maka akan tampil sebagai berikut

![step 4](https://raw.githubusercontent.com/fvldi/Jarkom_Modul1_Lapres_T14/main/images/No2/Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)

### Soal No. 3

Cari username dan password ketika login di "ppid.dpr.go.id"!

### Penyelesaian

1. Gunakan wireshark display filter expression dibawah, kemudian klik kanan pada paket yang tertera >> follow >> TCP Stream

```
http.request.method == POST
```

![Step 1](./images/No3/t1403.jpg/)

![Step 1b](./images/No3/t1403b.jpg/)

### Soal No. 4

Temukan paket dari web-web yang menggunakan basic authentication method!

### Penyelesaian

1. Gunakan wireshark display filter expression

```
http.authbasic
```

![Step 1](./images/No4/t1404.jpg)

### Soal No. 5

Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

### Penyelesaian

1. Gunakan wireshark display filter expression dibawah, kemudian cek credential pada paket nomor 31651. Maka didapat username dan password sebagai berikut

```
http.host=="aku.pengen.pw”
```

![Step 1](./images/No5/t1405.jpg/)

2. Masuk ke website aku.pengen.pw menggunakan username dan password tadi, kemudian jawab soal yang tertera.

![Step 2](./images/No5/t1405b.png/)

### Soal No. 6

Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

### Penyelesaian

1. Gunakan wireshark display filter expreession dibawah, kemudian follow TCP Streams pada paket dengan info "Answer.zip"

```
ftp-data
```

![Step 1](./images/No6/t1406.jpg/)

2. Ubah show and save data as menjadi "Raw", kemudian Save dengan nama Answer.zip

![Step 2](./images/No6/t1406b.jpg/)

3. Lalu follow TCP Stream pada paket dengan info "zipkey.txt", maka akan muncul password sebagai berikut

![Step 3](./images/No6/t1406c.jpg/)

4. Unzip file "Answer.zip" menggunakan password tersebut, kemudian Buka file "Open This.pdf". Maka akan tampil sebagai berikut

![step 4](https://raw.githubusercontent.com/fvldi/Jarkom_Modul1_Lapres_T14/main/images/No6/t1406d.jpg)

### Soal No. 7

Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf".

### Penyelesaian

1. Gunakan wireshark display filter expression dibawah, kemudian follow TCP Sream

```
ftp-data contains "Yes.pdf"
```

![Step 1](./images/No7/t1407.jpg/)

2. Ubah show and save data as menjadi "Raw", kemudian Save dengan extensi .zip

![Step 2](./images/No7/t1407b.jpg/)

3. Unzip file zip tersebut, kemudian buka file "Yes.pdf" didalamnya. Maka akan tampil sebagai berikut

![step 3](https://raw.githubusercontent.com/fvldi/Jarkom_Modul1_Lapres_T14/main/images/No7/t1407c.jpg)

### Soal No. 8

Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

### Penyelesaian

1. Gunakan wireshark display filter expression dibawah, Maka akan mendapatkan paket dari koneksi FTP dengan Microsoft FTP Service

```
ftp contains "Microsoft"
```

![Step 1](./images/No8/t1408.jpg/)

### Soal No. 9

Cari username dan password ketika login FTP pada localhost!

#### Penyelesaian

1. Gunakan wireshark display filter expression `ftp`, kemudian filter menggunakan regular expression : `User`

![step 1](./images/No9/t1409.png/)

2. Kemudian follow TCP stream, didapatlah username dan password nya sebagai berikut

![step 2](https://raw.githubusercontent.com/fvldi/Jarkom_Modul1_Lapres_T14/main/images/No9/t1409b.png)

### Soal No. 10

Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"

### Penyelesaian

1. Gunakan wireshark display filter expression dibawah, cek link yang terdapat pada paket yang tertera. Double click untuk mengunduh file pdf tersebut.

```
http contains ".pdf"
```

![step 1](./images/No10/t1410.jpg/)

2. Maka didapat file pdf dengan nama "1759.pdf" dengan isi tampilan berikut

![step 2](./images/No10/t1410b.jpg/)

## Capture Filter

### Soal No. 11

Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

### Penyelesaian

1. Gunakan wireshark Capture Filter expression 

```
port 21
```

![Step 1](./images/No11/t1411.jpg/)

### Soal No. 12

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

### Penyelesaian

1. Gunakan wireshark Capture Filter expression 

```
src port 21
```

![Step 1](./images/No12/t1412.jpg/)

### Soal No. 13

Filter sehingga wireshark hanya mengambil paket yang menuju  port 443!

### Penyelesaian

1. Gunakan wireshark Capture Filter expression 

```
dst port 443
```

![Step 1](./images/No13/t1413.jpg/)

### Soal No. 14

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

### Penyelesaian

1. Cari IP address menggunakan perintah "ipconfig" pada cmd, kemudian capture menggunakan wireshark capture filter expression 

```
src [ip address]
```

```
src 192.168.100.2
```

![Step 1](./images/No14/t1414.jpg/)

### Soal No. 15

Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

### Penyelesaian

1. Gunakan wireshark Capture filter expression dibawah, kemudian test dengan membuka laman monta.if.its.ac.id

```
dst monta.if.its.ac.id
```

![Step 1](./images/No15/t1415.jpg/)

