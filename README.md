# Laporan Resmi Praktikum Komunikasi Data dan Jaringan Komputer Modul 1  Kelompok T14

**Anggota Kelompok:**  
1. Hisyam Zulkarnain F – 05311840000019
2. Muhamad Rifaldi - 05311840000022

## I. Soal

A.  Display Filter

1.	Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
    *	Ketik wireshark display filter berikut: http.host=="testing.mekanis.me"
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/1a.PNG)
    *	Klik kanan pada paket teratas > Follow > TCP Stream
    *	Maka didapat hasil sebagai berikut:
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/1b.PNG)
    
2.	Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
    *	Klik menu File > Export Objects > HTTP… maka akan muncul windows berisi deretan file yang tersedia.
    *	Tuliskan pada Text Filter “Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg”
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/2a.PNG)
    *	Maka didapatlah gambar sebagai berikut:
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/2b.PNG)
    
3.	Cari username dan password ketika login di "ppid.dpr.go.id"!
    *	Ketik wireshark display filter berikut: http.host=="ppid.dpr.go.id"
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/3a.PNG)
    *	Maka akan didapat Informasi sebagai berikut:
    Username: 10pemuda
    Password: guncangdunia

4.	Temukan paket dari web-web yang menggunakan basic authentication method!
    *	Ketik wireshark display filter berikut: http.authbasic
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/4a.PNG)
    * Maka akan diketahui web-web yang menggunakan basic aunthentication method : "aku.pengen.pw" dan "testing.mekanis.me"
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/4b.PNG)

5.	Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
    *	Ketik wireshark display filter berikut: http.host=="aku.pengen.pw”
    *	Maka didapatlah:
    Username: kakakgamtenk 
    Password: hartatahtabermuda
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/5a.PNG)
    * Kemudian berikut isi dari website “aku.pengen.pw” beserta jawaban dari soal yang tertera:
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/5b.PNG)
    
6.	Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file     zipkey.txt (passwordnya adalah isi dari file txt tersebut).
   *  Ketik wireshark display filter berikut : ftp-data
   *  Lalu klik pada Answer.zip kemudian follow -> TCP stream
   ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/6a.PNG)
   *  Lalu save as menggunakan raw dan beri nama Answer.zip
   ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/6b.PNG)
   *	Ketik wireshark display filter berikut: ftp-data.command contains .txt untuk mengetahui password pada file zipkey.txt
   ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/6c.PNG)
   *  Kemudian buka dan extract file Answer.zip dan masukkan password dan pdf terbuka
   *	Ketik wireshark display filter berikut: ftp-data.command contains .txt untuk mengetahui password pada file zipkey.txt
   ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/6d.PNG)

7.	Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
    Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

8.	Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
   * Ketik display filter : ftp contains "Microsoft"
   * Maka akan mendapatkan paket dari koneksi FTP dengan Microsoft FTP Service
   ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/8a.PNG)

9.	Cari username dan password ketika login FTP pada localhost!
    *	Ketik display filter: ftp , dan filter menggunakan regular expression : User
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/9a.PNG)
    * Kemudian follow -> TCP stream dan didapatkan username dan password nya
    ![](https://github.com/fvldi/Jarkom_Modul1_Lapres_T14/blob/main/Gambar/9b.PNG)
    
    
10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
    clue: "25 50 44 46"
    *	Search dengan kategoti hexa sebagai berikut:
        
B. Capture Filter

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!



    
