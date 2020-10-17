# Laporan Resmi Praktikum Komunikasi Data dan Jaringan Komputer Modul 1  Kelompok T14

**Anggota Kelompok:**  
1. Hisyam Zulkarnain F – 05311840000019
2. Muhamad Rifaldi - 05311840000022

## I. Soal

A.  Display Filter

1.	Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
    *	Ketik wireshark display filter berikut: http.host=="testing.mekanis.me"
    *	Klik kanan pada paket teratas > Follow > TCP Stream
    *	Maka didapat hasil sebagai berikut:
    
2.	Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
    *	Klik menu File > Export Objects > HTTP… maka akan muncul windows berisi deretan file yang tersedia.
    *	Tuliskan pada Text Filter “Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg”
    *	Maka didapatlah gambar sebagai berikut:
    
3.	Cari username dan password ketika login di "ppid.dpr.go.id"!
    *	Ketik wireshark display filter berikut: http.host=="ppid.dpr.go.id"
    *	Maka akan didapat Informasi sebagai berikut:
    Username: 10pemuda
    Password: guncangdunia

4.	Temukan paket dari web-web yang menggunakan basic authentication method!
    *	Ketik wireshark display filter berikut: http.authbasic
    * Maka akan diketahui web-web yang menggunakan basic aunthentication method : "aku.pengen.pw" dan "testing.mekanis.me"

5.	Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
    *	Ketik wireshark display filter berikut: http.host=="aku.pengen.pw”
    *	Maka didapatlah:
    Username: kakakgamtenk 
    Password: hartatahtabermuda
    * Kemudian berikut isi dari website “aku.pengen.pw” beserta jawaban dari soal yang tertera:
    
6.	Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file     zipkey.txt (passwordnya adalah isi dari file txt tersebut).
   *  Ketik wireshark display filter berikut : ftp-data
   *  Lalu klik pada Answer.zip kemudian follow -> TCP stream
   *  Lalu save as menggunakan raw dan beri nama Answer.zip
   *  Kemudian buka dan extract file Answer.zip dan masukkan password
   *	Ketik wireshark display filter berikut: ftp-data.command contains .txt untuk mengetahui password pada file zipkey.txt

7.	Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
    Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

8.	Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

9.	Cari username dan password ketika login FTP pada localhost!
    *	Ketik display filter: ftp , dan filter menggunakan regular expression : User
    * Kemudian follow -> TCP stream dan didapatkan username dan password nya
    
    
10.	Cari file .pdf di wireshark lalu download dan buka file tersebut!
    clue: "25 50 44 46"
    *	Search dengan kategoti hexa sebagai berikut:
        
B. Capture Filter

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!



    
