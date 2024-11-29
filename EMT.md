# Pendahuluan dan Pengenalan Cara Kerja EMT
Selamat datang! Ini adalah pengantar pertama ke Euler Math Toolbox
(disingkat EMT atau Euler). EMT adalah sistem terintegrasi yang
merupakan perpaduan kernel numerik Euler dan program komputer aljabar
Maxima.


* 
Bagian numerik, GUI, dan komunikasi dengan Maxima telah dikembangkan
* oleh R. Grothmann, seorang profesor matematika di Universitas
* Eichstätt, Jerman. Banyak algoritma numerik dan pustaka software open
* source yang digunakan di dalamnya.


* 
Maxima adalah program open source yang matang dan sangat kaya untuk
* perhitungan simbolik dan aritmatika tak terbatas. Software ini
* dikelola oleh sekelompok pengembang di internet.


* 
Beberapa program lain (LaTeX, Povray, Tiny C Compiler, Python) dapat
* digunakan di Euler untuk memungkinkan perhitungan yang lebih cepat
* maupun tampilan atau grafik yang lebih baik.


Yang sedang Anda baca (jika dibaca di EMT) ini adalah berkas notebook
di EMT. Notebook aslinya bawaan EMT (dalam bahasa Inggris) dapat
dibuka melalui menu File, kemudian pilih "Open Tutorias and Example",
lalu pilih file "00 First Steps.en". Perhatikan, file notebook EMT
memiliki ekstensi ".en". Melalui notebook ini Anda akan belajar
menggunakan software Euler untuk menyelesaikan berbagai masalah
matematika.


Panduan ini ditulis dengan Euler dalam bentuk notebook Euler, yang
berisi teks (deskriptif), baris-baris perintah, tampilan hasil
perintah (numerik, ekspresi matematika, atau gambar/plot), dan gambar
yang disisipkan dari file gambar.


Untuk menambah jendela EMT, Anda dapat menekan [F11]. EMT akan
menampilkan jendela grafik di layar desktop Anda. Tekan [F11] lagi
untuk kembali ke tata letak favorit Anda. Tata letak disimpan untuk
sesi berikutnya.


Anda juga dapat menggunakan [Ctrl]+[G] untuk menyembunyikan jendela
grafik. Selanjutnya Anda dapat beralih antara grafik dan teks dengan
tombol [TAB].


Seperti yang Anda baca, notebook ini berisi tulisan (teks) berwarna
hijau, yang dapat Anda edit dengan mengklik kanan teks atau tekan menu
Edit -&gt; Edit Comment atau tekan [F5], dan juga baris perintah EMT yang
ditandai dengan "&gt;" dan berwarna merah. Anda dapat menyisipkan baris
perintah baru dengan cara menekan tiga tombol bersamaan:
[Shift]+[Ctrl]+[Enter].


## Komentar (Teks Uraian)

Komentar atau teks penjelasan dapat berisi beberapa "markup" dengan
sintaks sebagai berikut.


   - * Judul  
   - ** Sub-Judul  
   - latex: F (x) = \int_a^x f (t) \, dt  
   - mathjax: \frac{x^2-1}{x-1} = x + 1  
   - maxima: 'integrate(x^3,x) = integrate(x^3,x) + C  
   - http://www.euler-math-toolbox.de  
   - See: http://www.google.de | Google  
   - image: merah.png  
   - ---  

Hasil sintaks-sintaks di atas (tanpa diawali tanda strip) adalah
sebagai berikut.


# Judul

## Sub-Judul

$$F(x) = \int_a^x f(t) \, dt$$$$\frac{x^2-1}{x-1} = x + 1$$
$$\int {x^3}{\;dx}=C+\frac{x^4}{4}$$  <a href="http://www.euler-math-toolbox.de">http://www.euler-math-toolbox.de</a>  

  <a href="http://www.google.de">Google</a>  

![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Pekan%202-004.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Pekan%202-004.png)

---

Gambar diambil dari folder images di tempat file notebook berada dan
tidak dapat dibaca dari Web. Untuk "See:", tautan (URL)web lokal dapat
digunakan.


Paragraf terdiri atas satu baris panjang di editor. Pergantian baris
akan memulai baris baru. Paragraf harus dipisahkan dengan baris
kosong.


\>// baris perintah diawali dengan \>, komentar (keterangan) diawali dengan //


# Baris Perintah

Mari kita tunjukkan cara menggunakan EMT sebagai kalkulator yang sangat
canggih.


EMT berorientasi pada baris perintah. Anda dapat menuliskan satu atau lebih
perintah dalam satu baris perintah. Setiap perintah harus diakhiri dengan koma
atau titik koma.


* 
Titik koma menyembunyikan output (hasil) dari perintah.

* 
Sebuah koma mencetak hasilnya.

* 
Setelah perintah terakhir, koma diasumsikan secara otomatis (boleh tidak
* ditulis).


Dalam contoh berikut, kita mendefinisikan variabel r yang diberi nilai 1,25.
Output dari definisi ini adalah nilai variabel. Tetapi karena tanda titik koma,
nilai ini tidak ditampilkan. Pada kedua perintah di belakangnya, hasil kedua
perhitungan tersebut ditampilkan.


\>r=1.25; pi\*r^2, 2\*pi\*r 


    4.90873852123
    7.85398163397

## Latihan untuk Anda

* 
Sisipkan beberapa baris perintah baru

* 
Tulis perintah-perintah baru untuk melakukan suatu perhitungan yang Anda
* inginkan, boleh menggunakan variabel, boleh tanpa variabel.
* ---
* Beberapa catatan yang harus Anda perhatikan tentang penulisan sintaks perintah
* EMT.


* 
Pastikan untuk menggunakan titik desimal, bukan koma desimal untuk bilangan!

* 
Gunakan * untuk perkalian dan ^ untuk eksponen (pangkat).

* 
Seperti biasa, * dan / bersifat lebih kuat daripada + atau -.

* 
^ mengikat lebih kuat dari *, sehingga pi * r ^ 2 merupakan rumus luas
* lingkaran.

* 
Jika perlu, Anda harus menambahkan tanda kurung, seperti pada 2 ^ (2 ^ 3).


Perintah r = 1.25 adalah menyimpan nilai ke variabel di EMT. Anda juga dapat
menulis r: = 1.25 jika mau. Anda dapat menggunakan spasi sesuka Anda.


Anda juga dapat mengakhiri baris perintah dengan komentar yang diawali dengan dua
garis miring (//).


\>r := 1.25 // Komentar: Menggunakan  := sebagai ganti =


    1.25

Argumen atau input untuk fungsi ditulis di dalam tanda kurung.


\>sin(45°), cos(pi), log(sqrt(E))


    0.707106781187
    -1
    0.5

Seperti yang Anda lihat, fungsi trigonometri bekerja dengan radian, dan derajat
dapat diubah dengan °. Jika keyboard Anda tidak memiliki karakter derajat tekan
[F7], atau gunakan fungsi deg() untuk mengonversi.


EMT menyediakan banyak sekali fungsi dan operator matematika.Hampir semua fungsi
matematika sudah tersedia di EMT. Anda dapat melihat daftar lengkap fungsi-fungsi
matematika di EMT pada berkas Referensi (klik menu Help -&gt; Reference)


Untuk membuat rangkaian komputasi lebih mudah, Anda dapat merujuk ke hasil
sebelumnya dengan "%". Cara ini sebaiknya hanya digunakan untuk merujuk hasil
perhitungan dalam baris perintah yang sama.


\>(sqrt(5)+1)/2, %^2-%+1 // Memeriksa solusi x^2-x+1=0


    1.61803398875
    2

## Latihan untuk Anda

* 
Buka berkas Reference dan baca fungsi-fungsi matematika yang tersedia di EMT.

* 
Sisipkan beberapa baris perintah baru.

* 
Lakukan contoh-contoh perhitungan menggunakan fungsi-fungsi matematika di EMT.
* ---


# Satuan

EMT dapat mengubah unit satuan menjadi sistem standar internasional (SI).
Tambahkan satuan di belakang angka untuk konversi sederhana.


\>1miles  // 1 mil = 1609,344 m


    1609.344

Beberapa satuan yang sudah dikenal di dalam EMT adalah sebagai
berikut. Semua unit diakhiri dengan tanda dolar ($), namun boleh tidak
perlu ditulis dengan mengaktifkan easyunits. 


kilometer$:=1000;


km$:=kilometer$;


cm$:=0.01;


mm$:=0.001;


minute$:=60;


min$:=minute$;


minutes$:=minute$;


hour$:=60*minute$;


h$:=hour$;


hours$:=hour$;


day$:=24*hour$;


days$:=day$;


d$:=day$;


year$:=365.2425*day$;


years$:=year$;


y$:=year$;


inch$:=0.0254;


in$:=inch$;


feet$:=12*inch$;


foot$:=feet$;


ft$:=feet$;


yard$:=3*feet$;


yards$:=yard$;


yd$:=yard$;


mile$:=1760*yard$;


miles$:=mile$;


kg$:=1;


sec$:=1;


ha$:=10000;


Ar$:=100;


Tagwerk$:=3408;


Acre$:=4046.8564224;


pt$:=0.376mm;


Untuk konversi ke dan antar unit, EMT menggunakan operator khusus,
yakni -&gt;.


\>4km -\> miles, 4inch -\> " mm"


    2.48548476895
    101.6 mm

# Format Tampilan Nilai

Akurasi internal untuk nilai bilangan di EMT adalah standar IEEE,
sekitar 16 digit desimal. Aslinya, EMT tidak mencetak semua digit
suatu bilangan. Ini untuk menghemat tempat dan agar terlihat lebih
baik. Untuk mengatrtamilan satu bilangan, operator berikut dapat
digunakan.


\>pi


    3.14159265359

\>longest pi


          3.141592653589793 

\>long pi


    3.14159265359

\>short pi


    3.1416

\>shortest pi


       3.1 

\>fraction pi


    312689/99532

\>short 1200\*1.03^10, long E, longest pi


    1612.7
    2.71828182846
          3.141592653589793 

Format aslinya untuk menampilkan nilai menggunakan sekitar 10 digit.
Format tampilan nilai dapat diatur secara global atau hanya untuk satu
nilai.


Anda dapat mengganti format tampilan bilangan untuk semua perintah
selanjutnya. Untuk mengembalikan ke format aslinya dapat digunakan
perintah "defformat" atau "reset".


\>longestformat; pi, defformat; pi


    3.141592653589793
    3.14159265359

Kernel numerik EMT bekerja dengan bilangan titik mengambang (floating point)
dalam presisi ganda IEEE (berbeda dengan bagian simbolik EMT). Hasil numerik
dapat ditampilkan dalam bentuk pecahan.


\>1/7+1/4, fraction %


    0.392857142857
    11/28

# Perintah Multibaris

Perintah multi-baris membentang di beberapa baris yang terhubung
dengan "..." di setiap akhir baris, kecuali baris terakhir. Untuk
menghasilkan tanda pindah baris tersebut, gunakan tombol
[Ctrl]+[Enter]. Ini akan menyambung perintah ke baris berikutnya dan
menambahkan "..." di akhir baris sebelumnya. Untuk menggabungkan suatu
baris ke baris sebelumnya, gunakan [Ctrl]+[Backspace].


Contoh perintah multi-baris berikut dapat dijalankan setiap kali
kursor berada di salah satu barisnya. Ini juga menunjukkan bahwa ...
harus berada di akhir suatu baris meskipun baris tersebut memuat
komentar.


\>a=4; b=15; c=2; // menyelesaikan a\*x^2+b\*x+c=0 secara manual ...  
\>   D=sqrt(b^2/(a^2\*4)-c/a); ...  
\>   -b/(2\*a) + D, ...  
\>   -b/(2\*a) - D


    -0.138444501319
    -3.61155549868

# Menampilkan Daftar Variabe

Untuk menampilkan semua variabel yang sudah pernah Anda definisikan
sebelumnya (dan dapat dilihat kembali nilainya), gunakan perintah
"listvar".


\>listvar


    r                   1.25
    a                   4
    b                   15
    c                   2
    D                   1.73655549868123

Perintah listvar hanya menampilkan variabel buatan pengguna.
Dimungkinkan untuk menampilkan variabel lain, dengan menambahkan
string  termuat di dalam nama variabel yang diinginkan.


Perlu Anda perhatikan, bahwa EMT membedakan huruf besar dan huruf
kecil. Jadi variabel "d" berbeda dengan variabel "D".


Contoh berikut ini menampilkan semua unit yang diakhiri dengan "m"
dengan mencari semua variabel yang berisi "m$".


\>listvar m$


    km$                 1000
    cm$                 0.01
    mm$                 0.001
    nm$                 1853.24496
    gram$               0.001
    m$                  1
    hquantum$           6.62606957e-34
    atm$                101325

Untuk menghapus variabel tanpa harus memulai ulang EMT gunakan
perintah "remvalue".


\>remvalue a,b,c,D

\>D


    Variable D not found!
    Error in:
    D ...
     ^

# Menampilkan Panduan

Untuk mendapatkan panduan tentang penggunaan perintah atau fungsi di EMT, buka
jendela panduan dengan menekan [F1] dan cari fungsinya. Anda juga dapat
mengklik dua kali pada fungsi yang tertulis di baris perintah atau di teks
untuk membuka jendela panduan.


Coba klik dua kali pada perintah "intrandom" berikut ini!


\>intrandom(10,6)


    [4,  2,  6,  2,  4,  2,  3,  2,  2,  6]

Di jendela panduan, Anda dapat mengklik kata apa saja untuk menemukan
referensi atau fungsi.


Misalnya, coba klik kata "random" di jendela panduan. Kata tersebut
boleh ada dalam teks atau di bagian "See:" pada panduan. Anda akan
menemukan penjelasan fungsi "random", untuk menghasilkan bilangan acak
berdistribusi uniform antara 0,0 dan 1,0. Dari panduan untuk "random"
Anda dapat menampilkan panduan untuk fungsi "normal", dll.


\>random(10)


    [0.270906,  0.704419,  0.217693,  0.445363,  0.308411,  0.914541,
    0.193585,  0.463387,  0.095153,  0.595017]

\>normal(10)


    [-0.495418,  1.6463,  -0.390056,  -1.98151,  3.44132,  0.308178,
    -0.733427,  -0.526167,  1.10018,  0.108453]

# Matriks dan Vektor

EMT merupakan suatu aplikasi matematika yang mengerti "bahasa matriks". Artinya,
EMT menggunakan vektor dan matriks untuk perhitungan-perhitungan tingkat lanjut.
Suatu vektor atau matriks dapat didefinisikan dengan tanda kurung siku.
Elemen-elemennya dituliskan di dalam tanda kurung siku, antar elemen dalam satu
baris dipisahkan oleh koma(,), antar baris dipisahkan oleh titik koma (;).


Vektor dan matriks dapat diberi nama seperti variabel biasa.


\>v=[4,5,6,3,2,1]


    [4,  5,  6,  3,  2,  1]

\>A=[1,2,3;4,5,6;7,8,9]


                1             2             3 
                4             5             6 
                7             8             9 

Karena EMT mengerti bahasa matriks, EMT memiliki kemampuan yang sangat canggih
untuk melakukan perhitungan matematis untuk masalah-masalah aljabar linier,
statistika, dan optimisasi.


Vektor juga dapat didefinisikan dengan menggunakan rentang nilai dengan interval
tertentu menggunakan tanda titik dua (:),seperti contoh berikut ini.


\>c=1:5


    [1,  2,  3,  4,  5]

\>w=0:0.1:1


    [0,  0.1,  0.2,  0.3,  0.4,  0.5,  0.6,  0.7,  0.8,  0.9,  1]

\>mean(w^2)


    0.35

# Bilangan Kompleks

EMT juga dapat menggunakan bilangan kompleks. Tersedia banyak fungsi untuk
bilangan kompleks di EMT. Bilangan imaginer


dituliskan dengan huruf I (huruf besar I), namun akan ditampilkan dengan huruf i
(i kecil).


  re(x) : bagian riil pada bilangan kompleks x.  
  im(x) : bagian imaginer pada bilangan kompleks x.  
  complex(x) : mengubah bilangan riil x menjadi bilangan kompleks.  
  conj(x) : Konjugat untuk bilangan bilangan komplkes x.  
  arg(x) : argumen (sudut dalam radian) bilangan kompleks x.  
  real(x) : mengubah x menjadi bilangan riil.  

Apabila bagian imaginer x terlalu besar, hasilnya akan menampilkan pesan
kesalahan.


  &gt;sqrt(-1) // Error!  
  &gt;sqrt(complex(-1))  

\>z=2+3\*I, re(z), im(z), conj(z), arg(z), deg(arg(z)), deg(arctan(3/2))


    2+3i
    2
    3
    2-3i
    0.982793723247
    56.309932474
    56.309932474

\>deg(arg(I)) // 90°


    90

\>sqrt(-1)


    Floating point error!
    Error in sqrt
    Error in:
    sqrt(-1) ...
            ^

\>sqrt(complex(-1))


    0+1i

EMT selalu menganggap semua hasil perhitungan berupa bilangan riil dan tidak
akan secara otomatis mengubah ke bilangan kompleks.


Jadi akar kuadrat -1 akan menghasilkan kesalahan, tetapi akar kuadrat kompleks
didefinisikan untuk bidang koordinat dengan cara seperti biasa. Untuk mengubah
bilangan riil menjadi kompleks, Anda dapat menambahkan 0i atau menggunakan
fungsi "complex".


\>complex(-1), sqrt(%)


    -1+0i 
    0+1i

# Matematika Simbolik

EMT dapat melakukan perhitungan matematika simbolis (eksak) dengan bantuan
software Maxima. Software Maxima otomatis sudah terpasang di komputer Anda ketika
Anda memasang EMT. Meskipun demikian, Anda dapat juga memasang software Maxima
tersendiri (yang terpisah dengan instalasi Maxima di EMT).


Pengguna Maxima yang sudah mahir harus memperhatikan bahwa terdapat sedikit
perbedaan dalam sintaks antara sintaks asli Maxima dan sintaks ekspresi simbolik
di EMT.


Untuk melakukan perhitungan matematika simbolis di EMT, awali perintah Maxima
dengan tanda "&amp;". Setiap ekspresi yang dimulai dengan "&amp;" adalah ekspresi
simbolis dan dikerjakan oleh Maxima.


\>&(a+b)^2


    
                                          2
                                   (b + a)
    

\>&expand((a+b)^2), &factor(x^2+5\*x+6)


    
                                2            2
                               b  + 2 a b + a
    
    
                               (x + 2) (x + 3)
    

\>&solve(a\*x^2+b\*x+c,x) // rumus abc


    
                         2                         2
                 - sqrt(b  - 4 a c) - b      sqrt(b  - 4 a c) - b
            [x = ----------------------, x = --------------------]
                          2 a                        2 a
    

\>&(a^2-b^2)/(a+b), &ratsimp(%) // ratsimp menyederhanakan bentuk pecahan


    
                                    2    2
                                   a  - b
                                   -------
                                    b + a
    
    
                                    a - b
    

\>10! // nilai faktorial (modus EMT)


    3628800

\>&10! //nilai faktorial (simbolik dengan Maxima)


    
                                   3628800
    

Untuk menggunakan perintah Maxima secara langsung (seperti perintah pada layar
Maxima) awali perintahnya dengan tanda "::" pada baris perintah EMT. Sintaks
Maxima disesuaikan dengan sintaks EMT (disebut "modus kompatibilitas").


\>factor(1000) // mencari semua faktor 1000 (EMT)


    [2,  2,  2,  5,  5,  5]

\>:: factor(1000) // faktorisasi prima 1000 (dengan Maxima) 


    
                                     3  3
                                    2  5
    

\>:: factor(20!)


    
                            18  8  4  2
                           2   3  5  7  11 13 17 19
    

Jika Anda sudah mahir menggunakan Maxima, Anda dapat menggunakan sintaks asli
perintah Maxima dengan menggunakan tanda ":::" untuk mengawali setiap perintah
Maxima di EMT. Perhatikan, harus ada spasi antara ":::" dan perintahnya.


\>::: binomial(5,2); // nilai C(5,2)


    
                                      10
    

\>::: binomial(m,4); // C(m,4)=m!/(4!(m-4)!)


    
                          (m - 3) (m - 2) (m - 1) m
                          -------------------------
                                     24
    

\>::: trigexpand(cos(x+y)); // rumus cos(x+y)=cos(x) cos(y)-sin(x)sin(y) 


    
                        cos(x) cos(y) - sin(x) sin(y)
    

\>::: trigexpand(sin(x+y));


    
                        cos(x) sin(y) + sin(x) cos(y)
    

\>::: trigsimp(((1-sin(x)^2)\*cos(x))/cos(x)^2+tan(x)\*sec(x)^2) //menyederhanakan fungsi trigonometri


    
                                           4
                               sin(x) + cos (x)
                               ----------------
                                      3
                                   cos (x)
    

Untuk menyimpan ekspresi simbolik ke dalam suatu variabel digunakan tanda "&amp;=".


\>p1 &= (x^3+1)/(x+1)


    
                                     3
                                    x  + 1
                                    ------
                                    x + 1
    

\>&ratsimp(p1)


    
                                   2
                                  x  - x + 1
    

Untuk mensubstitusikan suatu nilai ke dalam variabel dapat digunakan perintah
"with".


\>&p1 with x=3 // (3^3+1)/(3+1)


    
                                      7
    

\>&p1 with x=a+b, &ratsimp(%) //substitusi dengan variabel baru


    
                                        3
                                 (b + a)  + 1
                                 ------------
                                  b + a + 1
    
    
                         2                  2
                        b  + (2 a - 1) b + a  - a + 1
    

\>&diff(p1,x) //turunan p1 terhadap x


    
                                  2      3
                               3 x      x  + 1
                               ----- - --------
                               x + 1          2
                                       (x + 1)
    

\>&integrate(p1,x) // integral p1 terhadap x


    
                                 3      2
                              2 x  - 3 x  + 6 x
                              -----------------
                                      6
    

# Tampilan Matematika Simbolik dengan LaTeX

Anda dapat menampilkan hasil perhitunagn simbolik secara lebih bagus
menggunakan LaTeX. Untuk melakukan hal ini, tambahkan tanda dolar ($)
di depan tanda &amp; pada setiap perintah Maxima.


Perhatikan, hal ini hanya dapat menghasilkan tampilan yang diinginkan
apabila komputer Anda sudah terpasang software LaTeX.


\>$&(a+b)^2


$$\left(b+a\right)^2$$\>$&expand((a+b)^2), $&factor(x^2+5\*x+6)


$$b^2+2\,a\,b+a^2$$$$\left(x+2\right)\,\left(x+3\right)$$\>$&solve(a\*x^2+b\*x+c,x) // rumus abc


$$\left[ x=\frac{-\sqrt{b^2-4\,a\,c}-b}{2\,a} , x=\frac{\sqrt{b^2-4\,
 a\,c}-b}{2\,a} \right] $$\>$&(a^2-b^2)/(a+b), $&ratsimp(%)


$$\frac{a^2-b^2}{b+a}$$$$a-b$$# Selamat Belajar dan Berlatih!

Baik, itulah sekilas pengantar penggunaan software EMT. Masih banyak kemampuan
EMT yang akan Anda pelajari dan praktikkan.


Sebagai latihan untuk memperlancar penggunaan perintah-perintah EMT yang sudah
dijelaskan di atas, silakan Anda lakukan hal-hal sebagai berikut.


* 
Carilah soal-soal matematika dari buku-buku Matematika.

* 
Tambahkan beberapa baris perintah EMT pada notebook ini.

* 
Selesaikan soal-soal matematika tersebut dengan menggunakan EMT.
* Pilih soal-soal yang sesuai dengan perintah-perintah yang sudah dijelaskan dan
* dicontohkan di atas.


\>4!


    24

% Soal 1: Hitunglah nilai dari integral berikut:


$$\int_0^1 (2x^3 + 3x^2 + x + 5) \, dx$$$$\int {2\,x^3+3\,x^2+x+5}{\;dx}=\frac{x^4}{2}+x^3+\frac{x^2}{2}+5\,x
 +c$$\>$expand((x + 2)\*(x - 3))


$$x^2-x-6$$\>$solve(x^2 - 5\*x + 6 = 0, x)


$$\left[ x=3 , x=2 \right] $$\>k=4


    4

\>p=5


    5

\>k+p


    9

\>k\*p


    20

\>pi\*k


    12.5663706144

\>c := k^2 + p^2


    41

\>k\*p/k \* sin(45°)


    3.53553390593

\>pi\*k^2


    50.2654824574




# EMT untuk Perhitungan Aljabar

Pada notebook ini Anda belajar menggunakan EMT untuk melakukan
berbagai perhitungan terkait dengan materi atau topik dalam Aljabar.
Kegiatan yang harus Anda lakukan adalah sebagai berikut:


* 
Membaca secara cermat dan teliti notebook ini;

* 
Menerjemahkan teks bahasa Inggris ke bahasa Indonesia;

* 
Mencoba contoh-contoh perhitungan (perintah EMT) dengan cara
* meng-ENTER setiap perintah EMT yang ada (pindahkan kursor ke baris
* perintah)

* 
Jika perlu Anda dapat memodifikasi perintah yang ada dan memberikan
* keterangan/penjelasan tambahan terkait hasilnya.

* 
Menyisipkan baris-baris perintah baru untuk mengerjakan soal-soal
* Aljabar dari file PDF yang saya berikan;

* 
Memberi catatan hasilnya.

* 
Jika perlu tuliskan soalnya pada teks notebook (menggunakan format
* LaTeX).

* 
Gunakan tampilan hasil semua perhitungan yang eksak atau simbolik
* dengan format LaTeX. (Seperti contoh-contoh pada notebook ini.)


## Contoh pertama

Menyederhanakan bentuk aljabar:


$$6x^{-3}y^5\times -7x^2y^{-9}$$\>$&6\*x^(-3)\*y^5\*-7\*x^2\*y^(-9)


$$-\frac{42}{x\,y^4}$$Menjabarkan:


\>$&showev('expand((6\*x^(-3)+y^5)\*(-7\*x^2-y^(-9))))


$${\it expand}\left(\left(-\frac{1}{y^9}-7\,x^2\right)\,\left(y^5+  \frac{6}{x^3}\right)\right)=-7\,x^2\,y^5-\frac{1}{y^4}-\frac{6}{x^3  \,y^9}-\frac{42}{x}$$## Baris Perintah

Baris perintah Euler terdiri dari satu atau beberapa perintah Euler
yang diikuti dengan titik koma “;” atau koma “,”. Titik koma mencegah
pencetakan hasil. Koma setelah perintah terakhir dapat dihilangkan.


Baris perintah berikut ini hanya akan mencetak hasil dari ekspresi,
bukan penugasan atau perintah format.


\>r:=2; h:=4; pi\*r^2\*h/3


    16.7551608191

Perintah harus dipisahkan dengan tanda kosong. Baris perintah berikut
ini mencetak dua hasilnya.


\>pi\*2\*r\*h, %+2\*pi\*r\*h // Ingat tanda % menyatakan hasil perhitungan terakhir sebelumnya


    50.2654824574
    100.530964915

Baris perintah dieksekusi sesuai urutan pengguna menekan tombol
return. Jadi, Anda mendapatkan nilai baru setiap kali Anda
mengeksekusi baris kedua.


\>x := 1;

\>x := cos(x) // nilai cosinus (x dalam radian)


    0.540302305868

\>x := cos(x)


    0.857553215846

Jika dua baris dihubungkan dengan “...”, kedua baris tersebut akan
selalu dieksekusi secara bersamaan.


\>x := 1.5; ...  
\>   x := (x+2/x)/2, x := (x+2/x)/2, x := (x+2/x)/2, 


    1.41666666667
    1.41421568627
    1.41421356237

Ini juga merupakan cara yang baik untuk membagi perintah yang panjang
menjadi dua baris atau lebih. Anda dapat menekan Ctrl+Return untuk
membagi baris menjadi dua pada posisi kursor saat ini, atau Ctlr+Back
untuk menggabungkan kedua baris.


Untuk melipat semua multi-baris, tekan Ctrl+L. Kemudian garis-garis
berikutnya hanya akan terlihat, jika salah satu dari mereka memiliki
fokus. Untuk melipat satu baris multi-baris, mulai baris pertama
dengan “%+ ”.


\>%+ x=4+5; ...  
\>    // This line will not be visible once the cursor is off the line


Garis yang dimulai dengan %% tidak akan terlihat sama sekali.


    81

Euler mendukung perulangan dalam baris perintah, selama perulangan
tersebut masuk ke dalam satu baris tunggal atau beberapa baris. Dalam
program, tentu saja pembatasan ini tidak berlaku. Untuk informasi
lebih lanjut, baca pengantar berikut ini.


\>x=1; for i=1 to 5; x := (x+2/x)/2, end; // menghitung akar 2


    1.5
    1.41666666667
    1.41421568627
    1.41421356237
    1.41421356237

Tidak masalah untuk menggunakan multi-baris. Pastikan baris diakhiri
dengan “...”.


\>x := 1.5; // comments go here before the ...  
\>   repeat xnew:=(x+2/x)/2; until xnew~=x; ...  
\>      x := xnew; ...  
\>   end; ...  
\>   x,


    1.41421356237

Struktur bersyarat juga bisa digunakan.


\>if E^pi\>pi^E; then "Thought so!", endif;


    Thought so!

Ketika Anda menjalankan perintah, kursor dapat berada di posisi mana
pun dalam baris perintah. Anda dapat kembali ke perintah sebelumnya
atau melompat ke perintah berikutnya dengan tombol panah. Atau Anda
dapat mengklik bagian komentar di atas perintah untuk membuka perintah
tersebut.


Ketika Anda menggerakkan kursor di sepanjang baris, pasangan tanda
kurung atau tanda kurung pembuka dan penutup akan disorot. Juga,
perhatikan baris status. Setelah tanda kurung pembuka dari fungsi
sqrt(), baris status akan menampilkan teks bantuan untuk fungsi
tersebut. Jalankan perintah dengan tombol return.


\>sqrt(sin(10°)/cos(20°))


    0.429875017772

Untuk melihat bantuan untuk perintah terbaru, buka jendela bantuan
dengan F1. Di sana, Anda dapat memasukkan teks yang akan dicari. Pada
baris kosong, bantuan untuk jendela bantuan akan ditampilkan. Anda
dapat menekan escape untuk mengosongkan baris, atau menutup jendela
bantuan.


Anda dapat mengklik dua kali pada perintah apa pun untuk membuka
bantuan untuk perintah ini. Coba klik dua kali perintah exp di bawah
ini pada baris perintah.


\>exp(log(2.5))


    2.5

Anda juga dapat menyalin dan menempel di Euler. Gunakan Ctrl-C dan
Ctrl-V untuk ini. Untuk menandai teks, seret mouse atau gunakan shift
bersamaan dengan tombol kursor. Selain itu, Anda dapat menyalin tanda
kurung yang disorot.


## Sintaksis Dasar

Euler mengetahui fungsi matematika yang biasa. Seperti yang telah Anda
lihat di atas, fungsi trigonometri bekerja dalam radian atau derajat.
Untuk mengonversi ke derajat, tambahkan simbol derajat (dengan tombol
F7) ke nilai, atau gunakan fungsi rad(x). Fungsi akar kuadrat disebut
sqrt dalam Euler. Tentu saja, x^(1/2) juga dapat digunakan.


Untuk mengatur variabel, gunakan “=” atau “:=”. Demi kejelasan,
pengantar ini menggunakan bentuk yang terakhir. Spasi tidak menjadi
masalah. Tetapi spasi antar perintah diharapkan.


Beberapa perintah dalam satu baris dipisahkan dengan “,” atau “;”.
Titik koma menekan output dari perintah. Pada akhir baris perintah,
“,” diasumsikan, jika “;” tidak ada.


\>g:=9.81; t:=2.5; 1/2\*g\*t^2


    30.65625

EMT menggunakan sintaks pemrograman untuk ekspresi. Untuk memasukkan


$$e^2 \cdot \left( \frac{1}{3+4 \log(0.6)}+\frac{1}{7} \right)$$Anda harus mengatur tanda kurung yang benar dan menggunakan / untuk
pecahan. Perhatikan tanda kurung yang disorot untuk mendapatkan
bantuan. Perhatikan bahwa konstanta Euler e diberi nama E dalam EMT.


\>E^2\*(1/(3+4\*log(0.6))+1/7)


    8.77908249441

Untuk menghitung ekspresi yang rumit seperti


$$\left(\frac{\frac17 + \frac18 + 2}{\frac13 + \frac12}\right)^2 \pi$$Anda harus memasukkannya dalam bentuk baris.


\>((1/7 + 1/8 + 2) / (1/3 + 1/2))^2 \* pi


    23.2671801626

Letakkan tanda kurung di sekitar sub-ekspresi yang perlu dihitung
terlebih dahulu. EMT membantu Anda dengan menyorot ekspresi yang
diselesaikan oleh tanda kurung penutup. Anda juga harus memasukkan
nama “pi” untuk huruf Yunani pi.


Hasil dari perhitungan ini adalah angka floating point. Secara default
dicetak dengan akurasi sekitar 12 digit. Pada baris perintah berikut,
kita juga belajar bagaimana kita dapat merujuk ke hasil sebelumnya
dalam baris yang sama.


\>1/3+1/7, fraction %


    0.47619047619
    10/21

Perintah Euler dapat berupa ekspresi atau perintah primitif. Ekspresi
terbuat dari operator dan fungsi. Jika perlu, ekspresi tersebut harus
mengandung tanda kurung untuk memaksa urutan eksekusi yang benar. Jika
ragu, mengatur tanda kurung adalah ide yang bagus. Perhatikan bahwa
EMT menampilkan tanda kurung pembuka dan penutup saat mengedit baris
perintah.


\>(cos(pi/4)+1)^3\*(sin(pi/4)+1)^2


    14.4978445072

Operator numerik Euler meliputi


 + unary atau operator plus  
 - unary atau operator minus  
 *, /  
 . produk matriks  
 pangkat a^b untuk a positif atau bilangan bulat b (a**b juga bisa  

digunakan)


 n! operator faktorial


dan masih banyak lagi.


Berikut adalah beberapa fungsi yang mungkin Anda perlukan. Masih
banyak lagi.


 sin, cos, tan, atan, asin, acos, rad, deg  
 log, exp, log10, sqrt, logbase  
 bin, logbin, logfac, mod, floor, ceil, round, abs, sign  
 conj,re,im,arg,conj,real,complex  
 beta,betai,gamma,complexgamma,ellrf,ellf,ellrd,elle  
 bitand, bitor, bitxor, bitnot  

Beberapa perintah memiliki alias, misalnya ln untuk log.


\>ln(E^2), arctan(tan(0.5))


    2
    0.5

\>sin(30°)


    0.5

Pastikan untuk menggunakan tanda kurung (tanda kurung bulat), apabila
ada keraguan tentang urutan eksekusi! Berikut ini tidak sama dengan
(2^3)^4, yang merupakan default untuk 2^3^4 di EMT (beberapa sistem
numerik melakukannya dengan cara lain).


\>2^3^4, (2^3)^4, 2^(3^4)


    2.41785163923e+24
    4096
    2.41785163923e+24

## Bilangan Real

Tipe data utama dalam Euler adalah bilangan real. Bilangan real
direpresentasikan dalam format IEEE dengan akurasi sekitar 16 digit
desimal.


\>longest 1/3


         0.3333333333333333 

Representasi ganda internal membutuhkan 8 byte.


\>printdual(1/3)


    1.0101010101010101010101010101010101010101010101010101*2^-2

\>printhex(1/3)


    5.5555555555554*16^-1

## String

String dalam Euler didefinisikan dengan “...”.


\>"A string can contain anything."


    A string can contain anything.

String dapat digabungkan dengan | atau dengan +. Ini juga berfungsi
dengan angka, yang dikonversi menjadi string dalam kasus tersebut.


\>"The area of the circle with radius " + 2 + " cm is " + pi\*4 + " cm^2."


    The area of the circle with radius 2 cm is 12.5663706144 cm^2.

Fungsi cetak juga mengonversi angka ke string. Fungsi ini dapat
mengambil sejumlah digit dan sejumlah tempat (0 untuk output padat),
dan secara optimal satu unit.


\>"Golden Ratio : " + print((1+sqrt(5))/2,5,0)


    Golden Ratio : 1.61803

Ada string khusus tidak ada, yang tidak mencetak. Dikembalikan oleh
beberapa fungsi, ketika hasilnya tidak penting. (Dikembalikan secara
otomatis, jika fungsi tidak memiliki pernyataan pengembalian).


\>none


Untuk mengonversi string menjadi angka, cukup evaluasi string
tersebut. Ini juga berlaku untuk ekspresi (lihat di bawah).


\>"1234.5"()


    1234.5

Untuk mendefinisikan vektor string, gunakan notasi vektor [...].


\>v:=["affe","charlie","bravo"]


    affe
    charlie
    bravo

Vektor string kosong dilambangkan dengan [none]. Vektor string dapat
digabungkan.


\>w:=[none]; w|v|v


    affe
    charlie
    bravo
    affe
    charlie
    bravo

String dapat berisi karakter Unicode. Secara internal, string ini
berisi kode UTF-8. Untuk membuat string seperti itu, gunakan u“...”
dan salah satu entitas HTML.


String Unicode dapat digabungkan seperti string lainnya.


\>u"&alpha; = " + 45 + u"&deg;" // pdfLaTeX mungkin gagal menampilkan secara benar


    α = 45°

I


Ada beberapa fungsi untuk membuat atau menganalisis string unicode.
Fungsi strtochar() akan mengenali string Unicode, dan menerjemahkannya
dengan benar.


Ada beberapa fungsi untuk membuat atau menganalisis string unicode.
Fungsi strtochar() akan mengenali string Unicode, dan menerjemahkannya
dengan benar.


\>v=strtochar(u"&Auml; is a German letter")


    [196,  32,  105,  115,  32,  97,  32,  71,  101,  114,  109,  97,  110,
    32,  108,  101,  116,  116,  101,  114]

Hasilnya adalah sebuah vektor angka Unicode. Fungsi kebalikannya
adalah chartoutf().


\>v[1]=strtochar(u"&Uuml;")[1]; chartoutf(v)


    Ü is a German letter

Fungsi utf() dapat menerjemahkan sebuah string dengan entitas dalam
sebuah variabel menjadi sebuah string Unicode.


\>s="We have &alpha;=&beta;."; utf(s) // pdfLaTeX mungkin gagal menampilkan secara benar


    We have α=β.

Dimungkinkan juga untuk menggunakan entitas numerik.


\>u"&#196;hnliches"


    Ähnliches

## Nilai Boolean

Nilai Boolean direpresentasikan dengan 1 = benar atau 0 = salah dalam
Euler. String dapat dibandingkan, seperti halnya angka.


\>2<1, "apel"<"banana"


    0
    1

“dan” adalah operator ‘&amp;&amp;’ dan ‘atau’ adalah operator ‘||’, seperti
dalam bahasa C. (Kata “dan” dan “atau” hanya dapat digunakan dalam
kondisi “jika”).


\>2<E && E<3


    1

Operator Boolean mematuhi aturan bahasa matriks.


\>(1:10)\>5, nonzeros(%)


    [0,  0,  0,  0,  0,  1,  1,  1,  1,  1]
    [6,  7,  8,  9,  10]

Anda dapat menggunakan fungsi nonzeros() untuk mengekstrak elemen
tertentu dari sebuah vektor. Pada contoh, kita menggunakan kondisional
isprime(n).


\>N=2|3:2:99 // N berisi elemen 2 dan bilangan2 ganjil dari 3 s.d. 99


    [2,  3,  5,  7,  9,  11,  13,  15,  17,  19,  21,  23,  25,  27,  29,
    31,  33,  35,  37,  39,  41,  43,  45,  47,  49,  51,  53,  55,  57,
    59,  61,  63,  65,  67,  69,  71,  73,  75,  77,  79,  81,  83,  85,
    87,  89,  91,  93,  95,  97,  99]

\>N[nonzeros(isprime(N))] //pilih anggota2 N yang prima


    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47,
    53,  59,  61,  67,  71,  73,  79,  83,  89,  97]

## Format Keluaran

Format output default EMT mencetak 12 digit. Untuk memastikan bahwa
kita melihat format default, kita atur ulang formatnya.


\>defformat; pi


    3.14159265359

Secara internal, EMT menggunakan standar IEEE untuk angka ganda dengan
sekitar 16 digit desimal. Untuk melihat jumlah digit penuh, gunakan
perintah “longestformat”, atau kami menggunakan operator “longest”
untuk menampilkan hasil dalam format terpanjang.


\>longest pi


          3.141592653589793 

Berikut ini adalah representasi heksadesimal internal dari angka
ganda.


\>printhex(pi)


    3.243F6A8885A30*16^0

Format output dapat diubah secara permanen dengan perintah format.


\>format(12,5); 1/3, pi, sin(1)


        0.33333 
        3.14159 
        0.84147 

Standarnya adalah format(12)


\>format(12); 1/3


    0.333333333333

Fungsi seperti “shortestformat”, “shortformat”, “longformat” bekerja
untuk vektor dengan cara berikut.


\>shortestformat; random(3,8)


      0.66    0.2   0.89   0.28   0.53   0.31   0.44    0.3 
      0.28   0.88   0.27    0.7   0.22   0.45   0.31   0.91 
      0.19   0.46  0.095    0.6   0.43   0.73   0.47   0.32 

Format default untuk skalar adalah format(12). Tetapi ini dapat
diubah.


\>setscalarformat(5); pi


    3.1416

Fungsi “longestformat” juga menetapkan format skalar.


\>longestformat; pi


    3.141592653589793

Sebagai referensi, berikut ini adalah daftar format output yang paling
penting.


 format terpendek format terpendek format panjang, format terpanjang  
 format (panjang, digit) goodformat (panjang)  
 format pecahan (panjang)  
 defformat  

Akurasi internal EMT adalah sekitar 16 tempat desimal, yang merupakan
standar IEEE. Angka disimpan dalam format internal ini.


Tetapi format keluaran EMT dapat diatur dengan cara yang fleksibel.


\>longestformat; pi,


    3.141592653589793

\>format(10,5); pi


      3.14159 

Standarnya adalah defformat().


\>defformat; // default


Ada operator pendek yang hanya mencetak satu nilai. Operator
“terpanjang” akan mencetak semua digit angka yang valid.


\>longest pi^2/2


          4.934802200544679 

Ada juga operator singkat untuk mencetak hasil dalam format pecahan.
Kami sudah menggunakannya di atas.


\>fraction 1+1/2+1/3+1/4


    25/12

Karena format internal menggunakan cara biner untuk menyimpan angka,
maka nilai 0,1 tidak akan terwakili dengan tepat. Kesalahan bertambah
sedikit, seperti yang Anda lihat dalam perhitungan berikut ini.


\>longest 0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1


     -1.110223024625157e-16 

Tetapi, dengan “longformat” default, Anda tidak akan melihat hal ini.
Untuk kenyamanan, output angka yang sangat kecil adalah 0.


\>0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1


    0

# Ekspresi

String atau nama dapat digunakan untuk menyimpan ekspresi matematika,
yang dapat dievaluasi oleh EMT. Untuk ini, gunakan tanda kurung
setelah ekspresi. Jika Anda bermaksud menggunakan string sebagai
ekspresi, gunakan konvensi untuk menamainya “fx” atau “fxy”, dll.
Ekspresi lebih diutamakan daripada fungsi.


Variabel global dapat digunakan dalam evaluasi.


\>r:=2; fx:="pi\*r^2"; longest fx()


          12.56637061435917 

Parameter ditetapkan ke x, y, dan z dalam urutan tersebut. Parameter
tambahan dapat ditambahkan dengan menggunakan parameter yang
ditetapkan.


\>fx:="a\*sin(x)^2"; fx(5,a=-1)


    -0.919535764538

Perhatikan bahwa ekspresi akan selalu menggunakan variabel global,
meskipun ada variabel dalam fungsi dengan nama yang sama. (Jika tidak,
evaluasi ekspresi dalam fungsi dapat memberikan hasil yang sangat
membingungkan bagi pengguna yang memanggil fungsi tersebut).


\>at:=4; function f(expr,x,at) := expr(x); ...  
\>   f("at\*x^2",3,5) // computes 4\*3^2 not 5\*3^2


    36

Jika Anda ingin menggunakan nilai lain untuk “at” selain nilai global,
Anda perlu menambahkan “at=value”.


\>at:=4; function f(expr,x,a) := expr(x,at=a); ...  
\>   f("at\*x^2",3,5)


    45

Sebagai referensi, kami menyatakan bahwa koleksi panggilan (dibahas di
tempat lain) dapat berisi ekspresi. Jadi kita dapat membuat contoh di
atas sebagai berikut.


\>at:=4; function f(expr,x) := expr(x); ...  
\>   f({{"at\*x^2",at=5}},3)


    45

Ekspresi dalam x sering digunakan seperti halnya fungsi.


Perhatikan bahwa mendefinisikan fungsi dengan nama yang sama seperti
ekspresi simbolik global akan menghapus variabel ini untuk menghindari
kebingungan antara ekspresi simbolik dan fungsi.


\>f &= 5\*x;

\>function f(x) := 6\*x;

\>f(2)


    12

Sesuai dengan konvensi, ekspresi simbolik atau numerik harus diberi
nama fx, fxy, dll. Skema penamaan ini tidak boleh digunakan untuk
fungsi.


\>fx &= diff(x^x,x); $&fx


$$x^{x}\,\left(\log x+1\right)$$Bentuk khusus dari sebuah ekspresi memungkinkan variabel apa pun
sebagai parameter tanpa nama untuk evaluasi ekspresi, bukan hanya “x”,
“y”, dll. Untuk ini, mulailah ekspresi dengan “@(variabel)...”.


\>"@(a,b) a^2+b^2", %(4,5)


    @(a,b) a^2+b^2
    41

Hal ini memungkinkan untuk memanipulasi ekspresi dalam variabel lain
untuk fungsi EMT yang membutuhkan ekspresi dalam “x”.


Cara paling dasar untuk mendefinisikan fungsi sederhana adalah dengan
menyimpan rumusnya dalam ekspresi simbolik atau numerik. Jika variabel
utamanya adalah x, ekspresi tersebut dapat dievaluasi seperti halnya
sebuah fungsi.


Seperti yang Anda lihat pada contoh berikut, variabel global terlihat
selama evaluasi.


\>fx &= x^3-a\*x;  ...  
\>   a=1.2; fx(0.5)


    -0.475

Semua variabel lain dalam ekspresi dapat ditentukan dalam evaluasi
menggunakan parameter yang ditetapkan.


\>fx(0.5,a=1.1)


    -0.425

Sebuah ekspresi tidak perlu berbentuk simbolik. Hal ini diperlukan,
jika ekspresi mengandung fungsi-fungsi, yang hanya dikenal di kernel
numerik, bukan di Maxima.


# Matematika Simbolik

EMT melakukan matematika simbolik dengan bantuan Maxima. Untuk
detailnya, mulailah dengan tutorial berikut ini, atau telusuri
referensi untuk Maxima. Para ahli dalam Maxima harus memperhatikan
bahwa ada perbedaan dalam sintaks antara sintaks asli Maxima dan
sintaks default dari ekspresi simbolik dalam EMT.


Matematika simbolik diintegrasikan secara mulus ke dalam Euler dengan
&amp;. Ekspresi apapun yang dimulai dengan &amp; adalah sebuah ekspresi
simbolik. Ekspresi ini dievaluasi dan dicetak oleh Maxima.


Pertama-tama, Maxima memiliki aritmatika “tak terbatas” yang dapat
menangani angka yang sangat besar.


\>$&44!


$$2658271574788448768043625811014615890319638528000000000$$Dengan cara ini, Anda dapat menghitung hasil yang besar secara tepat.
Mari kita hitung


$$C(44,10) = \frac{44!}{34! \cdot 10!}$$\>$& 44!/(34!\*10!) // nilai C(44,10)


$$2481256778$$Tentu saja, Maxima memiliki fungsi yang lebih efisien untuk hal ini
(seperti halnya bagian numerik EMT).


\>$binomial(44,10) //menghitung C(44,10) menggunakan fungsi binomial()


$$2481256778$$Untuk mempelajari lebih lanjut tentang fungsi tertentu, klik dua kali
pada fungsi tersebut. Sebagai contoh, coba klik dua kali pada
“&amp;binomial” di baris perintah sebelumnya. Ini akan membuka dokumentasi
Maxima yang disediakan oleh pembuat program tersebut.


Anda akan mengetahui bahwa perintah-perintah berikut ini juga dapat
digunakan.


$$C(x,3)=\frac{x!}{(x-3)!3!}=\frac{(x-2)(x-1)x}{6}$$\>$binomial(x,3) // C(x,3)


$$\frac{\left(x-2\right)\,\left(x-1\right)\,x}{6}$$Jika Anda ingin mengganti x dengan nilai tertentu, gunakan “with”.


\>$&binomial(x,3) with x=10 // substitusi x=10 ke C(x,3)


$$120$$Dengan begitu, Anda dapat menggunakan solusi dari sebuah persamaan
dalam persamaan lain.


Ekspresi simbolik dicetak oleh Maxima dalam bentuk 2D. Alasannya
adalah sebuah bendera simbolik khusus dalam string.


Seperti yang telah Anda lihat pada contoh sebelumnya dan contoh
berikut, jika Anda telah menginstal LaTeX, Anda dapat mencetak
ekspresi simbolik dengan Latex. Jika tidak, perintah berikut ini akan
mengeluarkan pesan kesalahan.


Untuk mencetak ekspresi simbolik dengan LaTeX, gunakan $ di depan &amp;
(atau Anda dapat menghilangkan &amp;) sebelum perintah. Jangan jalankan
perintah Maxima dengan $, jika Anda tidak memiliki LaTeX.


\>$(3+x)/(x^2+1)


$$\frac{x+3}{x^2+1}$$Ekspresi simbolik diuraikan oleh Euler. Jika Anda membutuhkan sintaks
yang kompleks dalam satu ekspresi, Anda dapat mengapit ekspresi dalam
“...”. Menggunakan lebih dari satu ekspresi sederhana dimungkinkan,
tetapi sangat tidak disarankan.


\>&"v := 5; v^2"


    
                                      25
    

Untuk kelengkapan, kami menyatakan bahwa ekspresi simbolik dapat
digunakan dalam program, tetapi harus diapit dengan tanda kutip.
Selain itu, akan jauh lebih efektif untuk memanggil Maxima pada saat
kompilasi jika memungkinkan.


\>$&expand((1+x)^4), $&factor(diff(%,x)) // diff: turunan, factor: faktor


$$4\,\left(x+1\right)^3$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-016.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-016.png)

Sekali lagi, % mengacu pada hasil sebelumnya.


Untuk mempermudah, kita menyimpan solusi ke dalam sebuah variabel
simbolik. Variabel simbolik didefinisikan dengan “&amp;=”.


\>fx &= (x+1)/(x^4+1); $&fx


$$\frac{x+1}{x^4+1}$$Ekspresi simbolik dapat digunakan dalam ekspresi simbolik lainnya.


\>$&factor(diff(fx,x))


$$\frac{-3\,x^4-4\,x^3+1}{\left(x^4+1\right)^2}$$Masukan langsung dari perintah Maxima juga tersedia. Mulai baris
perintah dengan “::”. Sintaks Maxima disesuaikan dengan sintaks EMT
(disebut “mode kompatibilitas”).


\>&factor(20!)


    
                             2432902008176640000
    

\>::: factor(10!)


    
                                   8  4  2
                                  2  3  5  7
    

\>:: factor(20!)


    
                            18  8  4  2
                           2   3  5  7  11 13 17 19
    

Jika Anda adalah seorang ahli dalam Maxima, Anda mungkin ingin
menggunakan sintaks asli Maxima. Anda dapat melakukan ini dengan
“:::”.


\>::: av:g$ av^2;


    
                                       2
                                      g
    

\>fx &= x^3\*exp(x), $fx


    
                                     3  x
                                    x  E
    

$$x^3\,e^{x}$$Variabel tersebut dapat digunakan dalam ekspresi simbolik lainnya.
Perhatikan, bahwa pada perintah berikut ini, sisi kanan dari &amp;=
dievaluasi sebelum penugasan ke Fx.


\>&(fx with x=5), $%, &float(%)


    
                                         5
                                    125 E
    

$$125\,e^5$$    
                              18551.64488782208
    

\>fx(5)


    18551.6448878

Untuk mengevaluasi ekspresi dengan nilai variabel tertentu, Anda dapat
menggunakan operator “with”.


Baris perintah berikut ini juga mendemonstrasikan bahwa Maxima dapat
mengevaluasi sebuah ekspresi secara numerik dengan float().


\>&(fx with x=10)-(fx with x=5), &float(%)


    
                                    10        5
                              1000 E   - 125 E
    
    
                             2.20079141499189e+7
    

\>$factor(diff(fx,x,2))


$$x\,\left(x^2+6\,x+6\right)\,e^{x}$$Untuk mendapatkan kode Latex untuk sebuah ekspresi, Anda dapat
menggunakan perintah tex.


\>tex(fx)


    x^3\,e^{x}

Ekspresi simbolik dapat dievaluasi seperti halnya ekspresi numerik.


\>fx(0.5)


    0.206090158838

Dalam ekspresi simbolik, hal ini tidak dapat dilakukan, karena Maxima
tidak mendukungnya. Sebagai gantinya, gunakan sintaks “with” (bentuk
yang lebih baik dari perintah at(...) pada Maxima).


\>$&fx with x=1/2


$$\frac{\sqrt{e}}{8}$$Penugasan ini juga bisa bersifat simbolis.


\>$&fx with x=1+t


$$\left(t+1\right)^3\,e^{t+1}$$Perintah solve menyelesaikan ekspresi simbolik untuk sebuah variabel
di Maxima. Hasilnya adalah sebuah vektor solusi.


\>$&solve(x^2+x=4,x)


$$\left[ x=\frac{-\sqrt{17}-1}{2} , x=\frac{\sqrt{17}-1}{2} \right] $$Bandingkan dengan perintah “solve” numerik di Euler, yang membutuhkan
nilai awal, dan secara opsional nilai target.


\>solve("x^2+x",1,y=4)


    1.56155281281

Nilai numerik dari solusi simbolik dapat dihitung dengan evaluasi
hasil simbolik. Euler akan membaca penugasan x= dst. Jika Anda tidak
membutuhkan hasil numerik untuk perhitungan lebih lanjut, Anda juga
bisa membiarkan Maxima menemukan nilai numeriknya.


\>sol &= solve(x^2+2\*x=4,x); $&sol, sol(), $&float(sol)


$$\left[ x=-\sqrt{5}-1 , x=\sqrt{5}-1 \right] $$    [-3.23607,  1.23607]

$$\left[ x=-3.23606797749979 , x=1.23606797749979 \right] $$Untuk mendapatkan solusi simbolik yang spesifik, seseorang dapat
menggunakan “dengan” dan indeks.


\>$&solve(x^2+x=1,x), x2 &= x with %[2]; $&x2


$$\frac{\sqrt{5}-1}{2}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-028.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-028.png)

Untuk menyelesaikan sistem persamaan, gunakan vektor persamaan.
Hasilnya adalah vektor solusi.


\>sol &= solve([x+y=3,x^2+y^2=5],[x,y]); $&sol, $&x\*y with sol[1]


$$2$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-030.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-030.png)

Ekspresi simbolik dapat memiliki bendera, yang menunjukkan perlakuan
khusus di Maxima. Beberapa flag dapat digunakan sebagai perintah juga,
namun ada juga yang tidak. Bendera ditambahkan dengan “|” (bentuk yang
lebih baik dari “ev(...,flags)”)


\>$& diff((x^3-1)/(x+1),x) //turunan bentuk pecahan


$$\frac{3\,x^2}{x+1}-\frac{x^3-1}{\left(x+1\right)^2}$$\>$& diff((x^3-1)/(x+1),x) | ratsimp //menyederhanakan pecahan


$$\frac{2\,x^3+3\,x^2+1}{x^2+2\,x+1}$$\>$&factor(%)


$$\frac{2\,x^3+3\,x^2+1}{\left(x+1\right)^2}$$# Fungsi

Dalam EMT, fungsi adalah program yang ditentukan dengan perintah
“function”. Fungsi dapat berupa fungsi satu baris atau fungsi
multibaris.


Fungsi satu baris dapat berupa numerik atau simbolik. Fungsi satu
baris numerik didefinisikan dengan “:=”.


\>function f(x) := x\*sqrt(x^2+1)


Sebagai gambaran umum, kami menunjukkan semua definisi yang mungkin
untuk fungsi satu baris. Sebuah fungsi dapat dievaluasi seperti halnya
fungsi Euler bawaan.


\>f(2)


    4.472135955

Fungsi ini juga dapat digunakan untuk vektor, mengikuti bahasa matriks
Euler, karena ekspresi yang digunakan dalam fungsi ini adalah vektor.


\>f(0:0.1:1)


    [0,  0.100499,  0.203961,  0.313209,  0.430813,  0.559017,  0.699714,
    0.854459,  1.0245,  1.21083,  1.41421]

Fungsi dapat diplot. Alih-alih ekspresi, kita hanya perlu memberikan
nama fungsi.


Berbeda dengan ekspresi simbolik atau numerik, nama fungsi harus
disediakan dalam bentuk string.


\>solve("f",1,y=1)


    0.786151377757

Secara default, jika Anda perlu menimpa fungsi built-in, Anda harus
menambahkan kata kunci “overwrite”. Menimpa fungsi bawaan berbahaya
dan dapat menyebabkan masalah bagi fungsi lain yang bergantung pada
fungsi tersebut.


Anda masih dapat memanggil fungsi bawaan sebagai “_...”, jika fungsi
tersebut merupakan fungsi dalam inti Euler.


\>function overwrite sin (x) := \_sin(x°) // redine sine in degrees

\>sin(45)


    0.707106781187

Sebaiknya kita hilangkan definisi ulang tentang sin ini.


\>forget sin; sin(pi/4)


    0.707106781187

## Parameter Default

Fungsi numerik dapat memiliki parameter default.


\>function f(x,a=1) := a\*x^2


Menghilangkan parameter ini menggunakan nilai default.


\>f(4)


    16

Menetapkannya akan menimpa nilai default.


\>f(4,5)


    80

Parameter yang ditetapkan juga menimpanya. Ini digunakan oleh banyak
fungsi Euler seperti plot2d, plot3d.


\>f(4,a=1)


    16

Jika sebuah variabel bukan parameter, maka variabel tersebut harus
bersifat global. Fungsi satu baris dapat melihat variabel global.


\>function f(x) := a\*x^2

\>a=6; f(2)


    24

Tetapi parameter yang ditetapkan akan menggantikan nilai global.


Jika argumen tidak ada dalam daftar parameter yang telah ditetapkan
sebelumnya, argumen tersebut harus dideklarasikan dengan “:=”!


\>f(2,a:=5)


    20

Fungsi simbolik didefinisikan dengan “&amp;=”. Fungsi-fungsi ini
didefinisikan dalam Euler dan Maxima, dan dapat digunakan di kedua
bahasa tersebut. Ekspresi pendefinisian dijalankan melalui Maxima
sebelum definisi.


\>function g(x) &= x^3-x\*exp(-x); $&g(x)


$$x^3-x\,e^ {- x }$$Fungsi simbolis dapat digunakan dalam ekspresi simbolis.


\>$&diff(g(x),x), $&% with x=4/3


$$\frac{e^ {- \frac{4}{3} }}{3}+\frac{16}{3}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-036.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-036.png)

Fungsi ini juga dapat digunakan dalam ekspresi numerik. Tentu saja,
ini hanya akan berfungsi jika EMT dapat menginterpretasikan semua yang
ada di dalam fungsi.


\>g(5+g(1))


    178.635099908

Mereka dapat digunakan untuk mendefinisikan fungsi atau ekspresi
simbolis lainnya.


\>function G(x) &= factor(integrate(g(x),x)); $&G(c) // integrate: mengintegralkan


$$\frac{e^ {- c }\,\left(c^4\,e^{c}+4\,c+4\right)}{4}$$\>solve(&g(x),0.5)


    0.703467422498

Hal berikut ini juga dapat digunakan, karena Euler menggunakan
ekspresi simbolik dalam fungsi g, jika tidak menemukan variabel
simbolik g, dan jika ada fungsi simbolik g.


\>solve(&g,0.5)


    0.703467422498

\>function P(x,n) &= (2\*x-1)^n; $&P(x,n)


$$\left(2\,x-1\right)^{n}$$\>function Q(x,n) &= (x+2)^n; $&Q(x,n)


$$\left(x+2\right)^{n}$$\>$&P(x,4), $&expand(%)


$$16\,x^4-32\,x^3+24\,x^2-8\,x+1$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-041.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-041.png)

\>P(3,4)


    625

\>$&P(x,4)+ Q(x,3), $&expand(%)


$$16\,x^4-31\,x^3+30\,x^2+4\,x+9$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-043.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-043.png)

\>$&P(x,4)-Q(x,3), $&expand(%), $&factor(%)


$$16\,x^4-33\,x^3+18\,x^2-20\,x-7$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-045.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-045.png)

![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-046.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-046.png)

\>$&P(x,4)\*Q(x,3), $&expand(%), $&factor(%)


$$\left(x+2\right)^3\,\left(2\,x-1\right)^4$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-048.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-048.png)

![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-049.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-049.png)

\>$&P(x,4)/Q(x,1), $&expand(%), $&factor(%)


$$\frac{\left(2\,x-1\right)^4}{x+2}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-051.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-051.png)

![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-052.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-052.png)

\>function f(x) &= x^3-x; $&f(x)


$$x^3-x$$Dengan &amp;=, fungsi ini bersifat simbolis, dan dapat digunakan dalam
ekspresi simbolis lainnya.


\>$&integrate(f(x),x)


$$\frac{x^4}{4}-\frac{x^2}{2}$$Dengan := fungsi tersebut berupa angka. Contoh yang baik adalah
integral pasti seperti


$$f(x) = \int_1^x t^t \, dt,$$yang tidak dapat dievaluasi secara simbolik.


Jika kita mendefinisikan ulang fungsi tersebut dengan kata kunci
“map”, maka fungsi tersebut dapat digunakan untuk vektor x. Secara
internal, fungsi tersebut dipanggil untuk semua nilai x satu kali, dan
hasilnya disimpan dalam sebuah vektor.


\>function map f(x) := integrate("x^x",1,x)

\>f(0:0.5:2)


    [-0.783431,  -0.410816,  0,  0.676863,  2.05045]

Fungsi dapat memiliki nilai default untuk parameter.


\>function mylog (x,base=10) := ln(x)/ln(base);


Sekarang, fungsi ini dapat dipanggil dengan atau tanpa parameter
“base”.


\>mylog(100), mylog(2^6.7,2)


    2
    6.7

Selain itu, dimungkinkan untuk menggunakan parameter yang ditetapkan.


\>mylog(E^2,base=E)


    2

Sering kali, kita ingin menggunakan fungsi untuk vektor di satu
tempat, dan untuk masing-masing elemen di tempat lain. Hal ini
dimungkinkan dengan parameter vektor.


\>function f([a,b]) &= a^2+b^2-a\*b+b; $&f(a,b), $&f(x,y)


$$y^2-x\,y+y+x^2$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-057.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-057.png)

Fungsi simbolik seperti itu dapat digunakan untuk variabel simbolik.


Tetapi fungsi ini juga dapat digunakan untuk vektor numerik.


\>v=[3,4]; f(v)


    17

Ada juga fungsi yang murni simbolis, yang tidak dapat digunakan secara
numerik.


\>function lapl(expr,x,y) &&= diff(expr,x,2)+diff(expr,y,2)//turunan parsial kedua


    
                     diff(expr, y, 2) + diff(expr, x, 2)
    

\>$&realpart((x+I\*y)^4), $&lapl(%,x,y)


$$0$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-059.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-059.png)

Tetapi tentu saja, semua itu bisa digunakan dalam ekspresi simbolis
atau dalam definisi fungsi simbolis.


\>function f(x,y) &= factor(lapl((x+y^2)^5,x,y)); $&f(x,y)


$$10\,\left(y^2+x\right)^3\,\left(9\,y^2+x+2\right)$$Untuk meringkas


* 
&amp;= mendefinisikan fungsi simbolik,

* 
:= mendefinisikan fungsi numerik,

* 
&amp;&amp;= mendefinisikan fungsi simbolik murni.


# Memecahkan Ekspresi

Ekspresi dapat diselesaikan secara numerik dan simbolik.


Untuk menyelesaikan ekspresi sederhana dari satu variabel, kita dapat
menggunakan fungsi solve(). Fungsi ini membutuhkan nilai awal untuk
memulai pencarian. Secara internal, solve() menggunakan metode secant.


\>solve("x^2-2",1)


    1.41421356237

Hal ini juga bisa digunakan untuk ekspresi simbolis. Perhatikan fungsi
berikut ini.


\>$&solve(x^2=2,x)


$$\left[ x=-\sqrt{2} , x=\sqrt{2} \right] $$\>$&solve(x^2-2,x)


$$\left[ x=-\sqrt{2} , x=\sqrt{2} \right] $$\>$&solve(a\*x^2+b\*x+c=0,x)


$$\left[ x=\frac{-\sqrt{b^2-4\,a\,c}-b}{2\,a} , x=\frac{\sqrt{b^2-4\,  a\,c}-b}{2\,a} \right] $$\>$&solve([a\*x+b\*y=c,d\*x+e\*y=f],[x,y])


$$\left[ \left[ x=-\frac{c\,e}{b\,\left(d-5\right)-a\,e} , y=\frac{c  \,\left(d-5\right)}{b\,\left(d-5\right)-a\,e} \right]  \right] $$\>px &= 4\*x^8+x^7-x^4-x; $&px


$$4\,x^8+x^7-x^4-x$$Sekarang kita mencari titik, di mana polinomialnya adalah 2. Dalam
solve(), nilai target default y=0 dapat diubah dengan variabel yang
ditetapkan.


Kami menggunakan y=2 dan mengeceknya dengan mengevaluasi polinomial
pada hasil sebelumnya.


\>solve(px,1,y=2), px(%)


    0.966715594851
    2

Memecahkan sebuah ekspresi simbolik dalam bentuk simbolik
mengembalikan sebuah daftar solusi. Kami menggunakan pemecah simbolik
solve() yang disediakan oleh Maxima.


\>sol &= solve(x^2-x-1,x); $&sol


$$\left[ x=\frac{1-\sqrt{5}}{2} , x=\frac{\sqrt{5}+1}{2} \right] $$Cara termudah untuk mendapatkan nilai numerik adalah dengan
mengevaluasi solusi secara numerik seperti sebuah ekspresi.


\>longest sol()


        -0.6180339887498949       1.618033988749895 

Untuk menggunakan solusi secara simbolis dalam ekspresi lain, cara
termudah adalah “dengan”.


\>$&x^2 with sol[1], $&expand(x^2-x-1 with sol[2])


$$0$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-068.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-068.png)

Menyelesaikan sistem persamaan secara simbolik dapat dilakukan dengan
vektor persamaan dan pemecah simbolik solve(). Jawabannya adalah
sebuah daftar daftar persamaan.


\>$&solve([x+y=2,x^3+2\*y+x=4],[x,y])


$$\left[ \left[ x=-1 , y=3 \right]  , \left[ x=1 , y=1 \right]  ,   \left[ x=0 , y=2 \right]  \right] $$Fungsi f() dapat melihat variabel global. Tetapi seringkali kita ingin
menggunakan parameter lokal.


$$a^x-x^a = 0.1$$dengan a = 3.


\>function f(x,a) := x^a-a^x;


Salah satu cara untuk mengoper parameter tambahan ke f() adalah dengan
menggunakan sebuah daftar yang berisi nama fungsi dan parameternya
(cara lainnya adalah dengan menggunakan parameter titik koma).


\>solve({{"f",3}},2,y=0.1)


    2.54116291558

Hal ini juga dapat dilakukan dengan ekspresi. Namun, elemen daftar
bernama harus digunakan. (Lebih lanjut tentang daftar dalam tutorial
tentang sintaks EMT).


\>solve({{"x^a-a^x",a=3}},2,y=0.1)


    2.54116291558

# Menyelesaikan Pertidaksamaan

Untuk menyelesaikan pertidaksamaan, EMT tidak akan dapat melakukannya,
melainkan dengan bantuan Maxima, artinya secara eksak (simbolik).
Perintah Maxima yang digunakan adalah fourier_elim(), yang harus
dipanggil dengan perintah "load(fourier_elim)" terlebih dahulu.


\>&load(fourier\_elim)


    
            C:/Program Files/Euler x64/maxima/share/maxima/5.35.1/share/f\
    ourier_elim/fourier_elim.lisp
    

\>$&fourier\_elim([x^2 - 1\>0],[x]) // x^2-1 \> 0


$$\left[ 1<x \right] \lor \left[ x<-1 \right] $$\>$&fourier\_elim([x^2 - 1<0],[x]) // x^2-1 < 0


$$\left[ -1<x , x<1 \right] $$\>$&fourier\_elim([x^2 - 1 # 0],[x]) // x^-1 <\> 0


$$\left[ -1<x , x<1 \right] \lor \left[ 1<x \right] \lor \left[ x<-1   \right] $$\>$&fourier\_elim([x # 6],[x])


$$\left[ x<6 \right] \lor \left[ 6<x \right] $$\>$&fourier\_elim([x < 1, x \> 1],[x]) // tidak memiliki penyelesaian


$${\it emptyset}$$\>$&fourier\_elim([minf < x, x < inf],[x]) // solusinya R


$${\it universalset}$$\>$&fourier\_elim([x^3 - 1 \> 0],[x])


$$\left[ 1<x , x^2+x+1>0 \right] \lor \left[ x<1 , -x^2-x-1>0   \right] $$\>$&fourier\_elim([cos(x) < 1/2],[x]) // ??? gagal


$$\left[ 1-2\,\cos x>0 \right] $$\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[x,y]) // sistem pertidaksamaan


$$\left[ y-5<x , x<y+7 , 10<y \right] $$\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[y,x])


$$\left[ {\it max}\left(10 , x-7\right)<y , y<x+5 , 5<x \right] $$\>$&fourier\_elim((x + y < 5) and (x - y \>8),[x,y])


$$\left[ y+8<x , x<5-y , y<-\frac{3}{2} \right] $$\>$&fourier\_elim(((x + y < 5) and x < 1) or  (x - y \>8),[x,y])


$$\left[ y+8<x \right] \lor \left[ x<{\it min}\left(1 , 5-y\right)   \right] $$\>&fourier\_elim([max(x,y) \> 6, x # 8, abs(y-1) \> 12],[x,y])


    
            [6 &lt; x, x &lt; 8, y &lt; - 11] or [8 &lt; x, y &lt; - 11]
     or [x &lt; 8, 13 &lt; y] or [x = y, 13 &lt; y] or [8 &lt; x, x &lt; y, 13 &lt; y]
     or [y &lt; x, 13 &lt; y]
    

\>$&fourier\_elim([(x+6)/(x-9) <= 6],[x])


$$\left[ x=12 \right] \lor \left[ 12<x \right] \lor \left[ x<9   \right] $$# Bahasa Matriks

Dokumentasi inti EMT berisi diskusi terperinci tentang bahasa matriks
Euler.


Vektor dan matriks dimasukkan dengan tanda kurung siku, elemen
dipisahkan dengan koma, baris dipisahkan dengan titik koma.


\>A=[1,2;3,4]


                1             2 
                3             4 

Hasil kali matriks dilambangkan dengan sebuah titik.


\>b=[3;4]


                3 
                4 

\>b' // transpose b


    [3,  4]

\>inv(A) //inverse A


               -2             1 
              1.5          -0.5 

\>A.b //perkalian matriks


               11 
               25 

\>A.inv(A)


                1             0 
                0             1 

Poin utama dari bahasa matriks adalah bahwa semua fungsi dan operator
bekerja elemen demi elemen.


\>A.A


                7            10 
               15            22 

\>A^2 //perpangkatan elemen2 A


                1             4 
                9            16 

\>A.A.A


               37            54 
               81           118 

\>power(A,3) //perpangkatan matriks


               37            54 
               81           118 

\>A/A //pembagian elemen-elemen matriks yang seletak


                1             1 
                1             1 

\>A/b //pembagian elemen2 A oleh elemen2 b kolom demi kolom (karena b vektor kolom)


         0.333333      0.666667 
             0.75             1 

\>A\\b // hasilkali invers A dan b, A^(-1)b 


               -2 
              2.5 

\>inv(A).b


               -2 
              2.5 

\>A\\A   //A^(-1)A


                1             0 
                0             1 

\>inv(A).A


                1             0 
                0             1 

\>A\*A //perkalin elemen-elemen matriks seletak


                1             4 
                9            16 

Ini bukan hasil kali matriks, tetapi perkalian elemen demi elemen. Hal
yang sama berlaku untuk vektor.


\>b^2 // perpangkatan elemen-elemen matriks/vektor


                9 
               16 

Jika salah satu operan adalah vektor atau skalar, maka operan tersebut
akan diperluas dengan cara alami.


\>2\*A


                2             4 
                6             8 

Misalnya, jika operan adalah vektor kolom, elemen-elemennya diterapkan
ke semua baris A.


\>[1,2]\*A


                1             4 
                3             8 

Jika ini adalah vektor baris, vektor ini diterapkan ke semua kolom A.


\>A\*[2,3]


                2             6 
                6            12 

Kita dapat membayangkan perkalian ini seolah-olah vektor baris v telah
diduplikasi untuk membentuk matriks dengan ukuran yang sama dengan A.


\>dup([1,2],2) // dup: menduplikasi/menggandakan vektor [1,2] sebanyak 2 kali (baris)


                1             2 
                1             2 

\>A\*dup([1,2],2) 


                1             4 
                3             8 

Hal ini juga berlaku untuk dua vektor di mana satu vektor adalah
vektor baris dan yang lainnya adalah vektor kolom. Kami menghitung i*j
untuk i, j dari 1 sampai 5. Caranya adalah dengan mengalikan 1:5
dengan transposenya. Bahasa matriks Euler secara otomatis menghasilkan
sebuah tabel nilai.


\>(1:5)\*(1:5)' // hasilkali elemen-elemen vektor baris dan vektor kolom


                1             2             3             4             5 
                2             4             6             8            10 
                3             6             9            12            15 
                4             8            12            16            20 
                5            10            15            20            25 

Sekali lagi, ingatlah bahwa ini bukan produk matriks!


\>(1:5).(1:5)' // hasilkali vektor baris dan vektor kolom


    55

\>sum((1:5)\*(1:5)) // sama hasilnya


    55

Bahkan operator seperti &lt; atau == bekerja dengan cara yang sama.


\>(1:10)<6 // menguji elemen-elemen yang kurang dari 6


    [1,  1,  1,  1,  1,  0,  0,  0,  0,  0]

Sebagai contoh, kita dapat menghitung jumlah elemen yang memenuhi
kondisi tertentu dengan fungsi sum().


\>sum((1:10)<6) // banyak elemen yang kurang dari 6


    5

Euler memiliki operator perbandingan, seperti “==”, yang memeriksa
kesetaraan.


Kita mendapatkan vektor 0 dan 1, di mana 1 berarti benar.


\>t=(1:10)^2; t==25 //menguji elemen2 t yang sama dengan 25 (hanya ada 1)


    [0,  0,  0,  0,  1,  0,  0,  0,  0,  0]

Dari vektor seperti itu, “nonzeros” memilih elemen bukan nol.


Dalam hal ini, kita mendapatkan indeks semua elemen yang lebih besar
dari 50.


\>nonzeros(t\>50) //indeks elemen2 t yang lebih besar daripada 50


    [8,  9,  10]

Tentu saja, kita dapat menggunakan vektor indeks ini untuk mendapatkan
nilai yang sesuai dalam t.


\>t[nonzeros(t\>50)] //elemen2 t yang lebih besar daripada 50


    [64,  81,  100]

Sebagai contoh, mari kita cari semua kuadrat dari angka 1 sampai 1000,
yaitu 5 modulo 11 dan 3 modulo 13.


\>t=1:1000; nonzeros(mod(t^2,11)==5 && mod(t^2,13)==3)


    [4,  48,  95,  139,  147,  191,  238,  282,  290,  334,  381,  425,
    433,  477,  524,  568,  576,  620,  667,  711,  719,  763,  810,  854,
    862,  906,  953,  997]

EMT tidak sepenuhnya efektif untuk komputasi bilangan bulat. EMT
menggunakan floating point presisi ganda secara internal. Akan tetapi,
hal ini sering kali sangat berguna.


Kita dapat memeriksa bilangan prima. Mari kita cari tahu, berapa
banyak kuadrat ditambah 1 yang merupakan bilangan prima.


\>t=1:1000; length(nonzeros(isprime(t^2+1)))


    112

Fungsi nonzeros() hanya bekerja untuk vektor. Untuk matriks, ada
mnonzeros().


\>seed(2); A=random(3,4)


         0.765761      0.401188      0.406347      0.267829 
          0.13673      0.390567      0.495975      0.952814 
         0.548138      0.006085      0.444255      0.539246 

Ini mengembalikan indeks elemen, yang bukan nol.


\>k=mnonzeros(A<0.4) //indeks elemen2 A yang kurang dari 0,4


                1             4 
                2             1 
                2             2 
                3             2 

Indeks ini dapat digunakan untuk menetapkan elemen ke suatu nilai.


\>mset(A,k,0) //mengganti elemen2 suatu matriks pada indeks tertentu


         0.765761      0.401188      0.406347             0 
                0             0      0.495975      0.952814 
         0.548138             0      0.444255      0.539246 

Fungsi mset() juga dapat mengatur elemen-elemen pada indeks ke
entri-entri matriks lain.


\>mset(A,k,-random(size(A)))


         0.765761      0.401188      0.406347     -0.126917 
        -0.122404     -0.691673      0.495975      0.952814 
         0.548138     -0.483902      0.444255      0.539246 

Dan dimungkinkan untuk mendapatkan elemen-elemen dalam vektor.


\>mget(A,k)


    [0.267829,  0.13673,  0.390567,  0.006085]

Fungsi lain yang berguna adalah extrema, yang mengembalikan nilai
minimal dan maksimal di setiap baris matriks dan posisinya.


\>ex=extrema(A)


         0.267829             4      0.765761             1 
          0.13673             1      0.952814             4 
         0.006085             2      0.548138             1 

Kita bisa menggunakan ini untuk mengekstrak nilai maksimal dalam
setiap baris.


\>ex[,3]'


    [0.765761,  0.952814,  0.548138]

Ini tentu saja, sama dengan fungsi max().


\>max(A)'


    [0.765761,  0.952814,  0.548138]

Tetapi dengan mget(), kita dapat mengekstrak indeks dan menggunakan
informasi ini untuk mengekstrak elemen-elemen pada posisi yang sama
dari matriks yang lain.


\>j=(1:rows(A))'|ex[,4], mget(-A,j)


                1             1 
                2             4 
                3             1 
    [-0.765761,  -0.952814,  -0.548138]

# Fungsi Matriks Lainnya (Membangun Matriks)

Untuk membangun sebuah matriks, kita dapat menumpuk satu matriks di
atas matriks lainnya. Jika keduanya tidak memiliki jumlah kolom yang
sama, kolom yang lebih pendek akan diisi dengan 0.


\>v=1:3; v\_v


                1             2             3 
                1             2             3 

Demikian juga, kita dapat melampirkan matriks ke matriks lain secara
berdampingan, jika keduanya memiliki jumlah baris yang sama.


\>A=random(3,4); A|v'


         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             2 
        0.0257573      0.658585      0.629832      0.770895             3 

Jika keduanya tidak memiliki jumlah baris yang sama, matriks yang
lebih pendek diisi dengan 0.


Ada pengecualian untuk aturan ini. Bilangan real yang dilampirkan pada
sebuah matriks akan digunakan sebagai kolom yang diisi dengan bilangan
real tersebut.


\>A|1


         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             1 
        0.0257573      0.658585      0.629832      0.770895             1 

Dimungkinkan untuk membuat matriks vektor baris dan kolom.


\>[v;v]


                1             2             3 
                1             2             3 

\>[v',v']


                1             1 
                2             2 
                3             3 

Tujuan utama dari hal ini adalah untuk menginterpretasikan vektor
ekspresi untuk vektor kolom.


\>"[x,x^2]"(v')


                1             1 
                2             4 
                3             9 

Untuk mendapatkan ukuran A, kita dapat menggunakan fungsi berikut ini.


\>C=zeros(2,4); rows(C), cols(C), size(C), length(C)


    2
    4
    [2,  4]
    4

Untuk vektor, ada length().


\>length(2:10)


    9

Ada banyak fungsi lain yang menghasilkan matriks.


\>ones(2,2)


                1             1 
                1             1 

Ini juga dapat digunakan dengan satu parameter. Untuk mendapatkan
vektor dengan angka selain 1, gunakan yang berikut ini.


\>ones(5)\*6


    [6,  6,  6,  6,  6]

Matriks angka acak juga dapat dibuat dengan acak (distribusi seragam)
atau normal (distribusi Gauß).


\>random(2,2)


          0.66566      0.831835 
            0.977      0.544258 

Berikut ini adalah fungsi lain yang berguna, yang merestrukturisasi
elemen-elemen matriks menjadi matriks lain.


\>redim(1:9,3,3) // menyusun elemen2 1, 2, 3, ..., 9 ke bentuk matriks 3x3


                1             2             3 
                4             5             6 
                7             8             9 

Dengan fungsi berikut, kita dapat menggunakan fungsi ini dan fungsi
dup untuk menulis fungsi rep(), yang mengulang sebuah vektor sebanyak
n kali.


\>function rep(v,n) := redim(dup(v,n),1,n\*cols(v))


Mari kita coba


\>rep(1:3,5)


    [1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3]

Fungsi multdup() menduplikasi elemen-elemen sebuah vektor.


\>multdup(1:3,5), multdup(1:3,[2,3,2])


    [1,  1,  1,  1,  1,  2,  2,  2,  2,  2,  3,  3,  3,  3,  3]
    [1,  1,  2,  2,  2,  3,  3]

Fungsi flipx() dan flipy() membalik urutan baris atau kolom dari
sebuah matriks. Misalnya, fungsi flipx() membalik secara horizontal.


\>flipx(1:5) //membalik elemen2 vektor baris


    [5,  4,  3,  2,  1]

Untuk rotasi, Euler memiliki rotleft() dan rotright().


\>rotleft(1:5) // memutar elemen2 vektor baris


    [2,  3,  4,  5,  1]

Fungsi khusus adalah drop(v,i), yang menghapus elemen dengan indeks di
i dari vektor v.


\>drop(10:20,3)


    [10,  11,  13,  14,  15,  16,  17,  18,  19,  20]

Perhatikan bahwa vektor i dalam drop(v,i) merujuk pada indeks elemen
dalam v, bukan nilai elemen. Jika Anda ingin menghapus elemen, Anda
harus menemukan elemen-elemen tersebut terlebih dahulu. Fungsi
indexof(v,x) dapat digunakan untuk menemukan elemen x dalam vektor
terurut v.


\>v=primes(50), i=indexof(v,10:20), drop(v,i)


    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47]
    [0,  5,  0,  6,  0,  0,  0,  7,  0,  8,  0]
    [2,  3,  5,  7,  23,  29,  31,  37,  41,  43,  47]

Seperti yang Anda lihat, tidak ada salahnya menyertakan indeks di luar
jangkauan (seperti 0), indeks ganda, atau indeks yang tidak diurutkan.


\>drop(1:10,shuffle([0,0,5,5,7,12,12]))


    [1,  2,  3,  4,  6,  8,  9,  10]

Ada beberapa fungsi khusus untuk mengatur diagonal atau menghasilkan
matriks diagonal.


Kita mulai dengan matriks identitas.


\>A=id(5) // matriks identitas 5x5


                1             0             0             0             0 
                0             1             0             0             0 
                0             0             1             0             0 
                0             0             0             1             0 
                0             0             0             0             1 

Kemudian, kami menetapkan diagonal bawah (-1) ke 1:4.


\>setdiag(A,-1,1:4) //mengganti diagonal di bawah diagonal utama


                1             0             0             0             0 
                1             1             0             0             0 
                0             2             1             0             0 
                0             0             3             1             0 
                0             0             0             4             1 

Perhatikan bahwa kita tidak mengubah matriks A. Kita mendapatkan
sebuah matriks baru sebagai hasil dari setdiag().


Berikut adalah sebuah fungsi yang mengembalikan sebuah matriks
tri-diagonal.


\>function tridiag (n,a,b,c) := setdiag(setdiag(b\*id(n),1,c),-1,a); ...  
\>   tridiag(5,1,2,3)


                2             3             0             0             0 
                1             2             3             0             0 
                0             1             2             3             0 
                0             0             1             2             3 
                0             0             0             1             2 

Diagonal sebuah matriks juga dapat diekstrak dari matriks. Untuk
mendemonstrasikan hal ini, kami merestrukturisasi vektor 1:9 menjadi
matriks 3x3.


\>A=redim(1:9,3,3)


                1             2             3 
                4             5             6 
                7             8             9 

Sekarang kita bisa mengekstrak diagonal.


\>d=getdiag(A,0)


    [1,  5,  9]

Contoh: Kita dapat membagi matriks dengan diagonalnya. Bahasa matriks
memperhatikan bahwa vektor kolom d diterapkan ke matriks baris demi
baris.


\>fraction A/d'


            1         2         3 
          4/5         1       6/5 
          7/9       8/9         1 

# Vektorisasi

Hampir semua fungsi di Euler juga dapat digunakan untuk input matriks
dan vektor, jika hal ini masuk akal.


Sebagai contoh, fungsi sqrt() menghitung akar kuadrat dari semua
elemen vektor atau matriks.


\>sqrt(1:3)


    [1,  1.41421,  1.73205]

Jadi, Anda dapat dengan mudah membuat tabel nilai. Ini adalah salah
satu cara untuk memplot sebuah fungsi (alternatif lainnya menggunakan
ekspresi).


\>x=1:0.01:5; y=log(x)/x^2; // terlalu panjang untuk ditampikan


Dengan ini dan operator titik dua a:delta:b, vektor nilai fungsi dapat
dihasilkan dengan mudah.


Pada contoh berikut, kita membuat vektor nilai t[i] dengan jarak 0.1
dari -1 hingga 1. Kemudian kita membuat vektor nilai dari fungsi


lateks: s = t^3-t


\>t=-1:0.1:1; s=t^3-t


    [0,  0.171,  0.288,  0.357,  0.384,  0.375,  0.336,  0.273,  0.192,
    0.099,  0,  -0.099,  -0.192,  -0.273,  -0.336,  -0.375,  -0.384,
    -0.357,  -0.288,  -0.171,  0]

EMT memperluas operator untuk skalar, vektor, dan matriks dengan cara
yang jelas.


Misalnya, vektor kolom dikalikan vektor baris diperluas menjadi
matriks, jika operator diterapkan. Berikut ini, v' adalah vektor yang
ditransposisikan (vektor kolom).


\>shortest (1:5)\*(1:5)'


         1      2      3      4      5 
         2      4      6      8     10 
         3      6      9     12     15 
         4      8     12     16     20 
         5     10     15     20     25 

Perhatikan, bahwa ini sangat berbeda dengan hasil kali matriks. Hasil
kali matriks dilambangkan dengan sebuah titik “.” dalam EMT.


\>(1:5).(1:5)'


    55

Secara default, vektor baris dicetak dalam format ringkas.


\>[1,2,3,4]


    [1,  2,  3,  4]

Untuk matriks, operator khusus . menyatakan perkalian matriks, dan A'
menyatakan transposisi. Matriks 1x1 dapat digunakan seperti halnya
bilangan real.


\>v:=[1,2]; v.v', %^2


    5
    25

Untuk mentransposisikan matriks, kita menggunakan apostrof.


\>v=1:4; v'


                1 
                2 
                3 
                4 

Jadi kita dapat menghitung matriks A dikali vektor b.


\>A=[1,2,3,4;5,6,7,8]; A.v'


               30 
               70 

Perhatikan bahwa v masih merupakan vektor baris. Jadi v'.v berbeda
dengan v.v'.


\>v'.v


                1             2             3             4 
                2             4             6             8 
                3             6             9            12 
                4             8            12            16 

v.v' menghitung norma v kuadrat untuk vektor baris v. Hasilnya adalah
vektor 1x1, yang berfungsi seperti bilangan real.


\>v.v'


    30

There is also the function norm (along with many other function of
Linear Algebra).


\>norm(v)^2


    30

Operator dan fungsi mematuhi bahasa matriks Euler.


Berikut ini adalah ringkasan aturannya.


* 
Sebuah fungsi yang diterapkan pada vektor atau matriks diterapkan
* pada setiap elemen.


* 
Operator yang beroperasi pada dua matriks dengan ukuran yang sama
* diterapkan secara berpasangan pada elemen-elemen matriks.


* 
Jika dua matriks memiliki dimensi yang berbeda, keduanya diperluas
* dengan cara yang masuk akal, sehingga memiliki ukuran yang sama.


Misalnya, nilai skalar dikalikan vektor mengalikan nilai tersebut
dengan setiap elemen vektor. Atau matriks dikali vektor (dengan *,
bukan .) memperluas vektor ke ukuran matriks dengan menduplikasinya.


Berikut ini adalah kasus sederhana dengan operator ^.


\>[1,2,3]^2


    [1,  4,  9]

Ini adalah kasus yang lebih rumit. Vektor baris dikalikan vektor kolom
memperluas keduanya dengan menduplikasi.


\>v:=[1,2,3]; v\*v'


                1             2             3 
                2             4             6 
                3             6             9 

Perhatikan bahwa hasil kali skalar menggunakan hasil kali matriks,
bukan tanda *!


\>v.v'


    14

Ada banyak fungsi untuk matriks. Kami memberikan daftar singkat. Anda
harus membaca dokumentasi untuk informasi lebih lanjut mengenai
perintah-perintah ini.


  sum,prod menghitung jumlah dan hasil kali dari baris-baris  
  cumsum,cumprod melakukan hal yang sama secara kumulatif  
  menghitung nilai ekstrem dari setiap baris  
  extrema mengembalikan vektor dengan informasi ekstrem  
  diag(A,i) mengembalikan diagonal ke-i  
  setdiag(A,i,v) menetapkan diagonal ke-i  
  id(n) matriks identitas  
  det(A) determinan  
  charpoly(A) polinomial karakteristik  
  eigenvalues(A) nilai eigen  

\>v\*v, sum(v\*v), cumsum(v\*v)


    [1,  4,  9]
    14
    [1,  5,  14]

Operator : menghasilkan vektor baris dengan spasi yang sama, opsional
dengan ukuran langkah.


\>1:4, 1:2:10


    [1,  2,  3,  4]
    [1,  3,  5,  7,  9]

Untuk menggabungkan matriks dan vektor, terdapat operator “|” dan “_”.


\>[1,2,3]|[4,5], [1,2,3]\_1


    [1,  2,  3,  4,  5]
                1             2             3 
                1             1             1 

Elemen-elemen dari sebuah matriks disebut dengan “A[i,j]”.


\>A:=[1,2,3;4,5,6;7,8,9]; A[2,3]


    6

Untuk vektor baris atau kolom, v[i] adalah elemen ke-i dari vektor
tersebut. Untuk matriks, ini mengembalikan baris ke-i dari matriks.


\>v:=[2,4,6,8]; v[3], A[3]


    6
    [7,  8,  9]

Indeks juga dapat berupa vektor baris dari indeks. : menunjukkan semua
indeks.


\>v[1:2], A[:,2]


    [2,  4]
                2 
                5 
                8 

Bentuk singkat untuk : adalah menghilangkan indeks sepenuhnya.


\>\\A[,2:3]


    Syntax error in expression, or unfinished expression!
    Error in:
    \A[,2:3] ...
    ^

Untuk tujuan vektorisasi, elemen-elemen matriks dapat diakses
seolah-olah mereka adalah vektor.


\>A{4}


    4

Sebuah matriks juga dapat diratakan, dengan menggunakan fungsi
redim(). Hal ini diimplementasikan dalam fungsi flatten().


\>redim(A,1,prod(size(A))), flatten(A)


    [1,  2,  3,  4,  5,  6,  7,  8,  9]
    [1,  2,  3,  4,  5,  6,  7,  8,  9]

Untuk menggunakan matriks untuk tabel, mari kita atur ulang ke format
default, dan menghitung tabel nilai sinus dan kosinus. Perhatikan
bahwa sudut dalam radian secara default.


\>defformat; w=0°:45°:360°; w=w'; deg(w)


                0 
               45 
               90 
              135 
              180 
              225 
              270 
              315 
              360 

Sekarang kita append matriksnya


\>M = deg(w)|w|cos(w)|sin(w)


                0             0             1             0 
               45      0.785398      0.707107      0.707107 
               90        1.5708             0             1 
              135       2.35619     -0.707107      0.707107 
              180       3.14159            -1             0 
              225       3.92699     -0.707107     -0.707107 
              270       4.71239             0            -1 
              315       5.49779      0.707107     -0.707107 
              360       6.28319             1             0 

Dengan menggunakan bahasa matriks, kita dapat membuat beberapa tabel
dari beberapa fungsi sekaligus.


Pada contoh berikut, kita menghitung t[j]^i untuk i dari 1 hingga n.
Kita mendapatkan sebuah matriks, di mana setiap baris adalah tabel t^i
untuk satu i. Dengan kata lain, matriks tersebut memiliki
elemen-elemen


$$a_{i,j} = t_j^i, \quad 1 \le j \le 101, \quad 1 \le i \le n$$Sebuah fungsi yang tidak bekerja untuk input vektor harus
“divektorkan”. Hal ini dapat dicapai dengan kata kunci “map” dalam
definisi fungsi. Kemudian fungsi akan dievaluasi untuk setiap elemen
parameter vektor.


Integrasi numerik integrate() hanya bekerja untuk batas interval
skalar. Jadi kita perlu membuat vektornya.


\>function map f(x) := integrate("x^x",1,x)


Kata kunci “map” membuat vektor fungsi. Fungsi ini sekarang akan
bekerja


untuk vektor angka.


\>f([1:5])


    [0,  2.05045,  13.7251,  113.336,  1241.03]

# Sub-Matriks dan Elemen Matriks

Untuk mengakses elemen matriks, gunakan notasi kurung.


\>A=[1,2,3;4,5,6;7,8,9], A[2,2]


                1             2             3 
                4             5             6 
                7             8             9 
    5

Kita dapat mengakses baris lengkap dari sebuah matriks.


\>A[2]


    [4,  5,  6]

Untuk vektor baris atau kolom, ini mengembalikan elemen vektor.


\>v=1:3; v[2]


    2

Jika indeks adalah vektor indeks, Euler akan mengembalikan baris-baris
yang sesuai dari matriks.


Di sini kita menginginkan baris pertama dan kedua dari A.


\>A[2,]


    [4,  5,  6]

Jika indeks adalah vektor indeks, Euler akan mengembalikan baris-baris
yang sesuai dari matriks.


Di sini kita menginginkan baris pertama dan kedua dari A.


\>A[[1,2]]


                1             2             3 
                4             5             6 

Kita bahkan dapat menyusun ulang A menggunakan vektor indeks.
Tepatnya, kita tidak mengubah A di sini, tetapi menghitung versi
susunan ulang dari A.


\>A[[3,2,1]]


                7             8             9 
                4             5             6 
                1             2             3 

Trik indeks juga bekerja dengan kolom.


Contoh ini memilih semua baris A dan kolom kedua dan ketiga.


\>A[1:3,2:3]


                2             3 
                5             6 
                8             9 

Untuk singkatan “:” menunjukkan semua indeks baris atau kolom.


\>A[:,3]


                3 
                6 
                9 

Sebagai alternatif, biarkan indeks pertama kosong.


\>A[,2:3]


                2             3 
                5             6 
                8             9 

Kita juga bisa mendapatkan baris terakhir A.


\>A[-1]


    [7,  8,  9]

Now let us change elements of A by assigning a submatrix of A to some
value. This does in fact change the stored matrix A.


\>A[1,1]=4


                4             2             3 
                4             5             6 
                7             8             9 

Kita juga dapat menetapkan nilai pada deretan A.


\>A[1]=[-1,-1,-1]


               -1            -1            -1 
                4             5             6 
                7             8             9 

Kami bahkan dapat menetapkan ke sub-matriks jika memiliki ukuran yang
tepat.


\>A[1:2,1:2]=[5,6;7,8]


                5             6            -1 
                7             8             6 
                7             8             9 

Selain itu, beberapa jalan pintas diperbolehkan.


\>A[1:2,1:2]=0


                0             0            -1 
                0             0             6 
                7             8             9 

Peringatan: Indeks di luar batas akan mengembalikan matriks kosong,
atau pesan kesalahan, tergantung pada pengaturan sistem. Standarnya
adalah pesan kesalahan. Namun, ingatlah bahwa indeks negatif dapat
digunakan untuk mengakses elemen-elemen matriks yang dihitung dari
akhir.


\>A[4]


    Row index 4 out of bounds!
    Error in:
    A[4] ...
        ^

# Pengurutan dan Pengocokan

Fungsi mengurutkan() mengurutkan vektor baris.


\>sort([5,6,4,8,1,9])


    [1,  4,  5,  6,  8,  9]

Sering kali diperlukan untuk mengetahui indeks vektor yang diurutkan
dalam vektor aslinya. Hal ini dapat digunakan untuk menyusun ulang
vektor lain dengan cara yang sama.


Mari kita mengacak sebuah vektor.


\>v=shuffle(1:10)


    [5,  7,  2,  6,  3,  9,  1,  8,  10,  4]

Indeks berisi urutan v yang tepat.


\>{vs,ind}=sort(v); v[ind]


    [1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Hal ini juga berlaku untuk vektor string.


\>s=["a","d","e","a","aa","e"]


    a
    d
    e
    a
    aa
    e

\>{ss,ind}=sort(s); ss


    a
    a
    aa
    d
    e
    e

Seperti yang Anda lihat, posisi entri ganda agak acak.


\>ind


    [4,  1,  5,  2,  6,  3]

Fungsi unique mengembalikan daftar terurut dari elemen unik sebuah
vektor.


\>intrandom(1,10,10), unique(%)


    [1,  4,  2,  5,  8,  5,  2,  7,  10,  4]
    [1,  2,  4,  5,  7,  8,  10]

Ini juga berlaku untuk string vektor juga.


\>unique(s)


    a
    aa
    d
    e

# Aljabar Linier

EMT memiliki banyak fungsi untuk menyelesaikan sistem linier, sistem
jarang, atau masalah regresi.


Untuk sistem linier Ax=b, Anda dapat menggunakan algoritma Gauss,
matriks invers, atau kecocokan linier. Operator A\b menggunakan versi
algoritma Gauss.


\>A=[1,2;3,4]; b=[5;6]; A\\b


               -4 
              4.5 

Sebagai contoh lain, kita membuat matriks 200x200 dan jumlah barisnya.
Kemudian kita selesaikan Ax = b dengan menggunakan matriks
kebalikannya. Kita mengukur kesalahan sebagai deviasi maksimal dari
semua elemen dari 1, yang tentu saja merupakan solusi yang benar.


\>A=normal(200,200); b=sum(A); longest totalmax(abs(inv(A).b-1))


      3.579359031391505e-13 

Jika sistem tidak memiliki solusi, kecocokan linier meminimalkan norma
kesalahan Ax-b.


\>A=[1,2,3;4,5,6;7,8,9]


                1             2             3 
                4             5             6 
                7             8             9 

Determinan matrisk tersebut adalah 0


\>det(A)


    0

# Matriks Simbolik

Maxima memiliki matriks simbolik. Tentu saja, Maxima dapat digunakan
untuk masalah aljabar linier sederhana. Kita bisa mendefinisikan
matriks untuk Euler dan Maxima dengan &amp;:=, dan kemudian menggunakannya
dalam ekspresi simbolik. Bentuk [...] yang biasa untuk mendefinisikan
matriks dapat digunakan dalam Euler untuk mendefinisikan matriks
simbolik.


\>A &= [a,1,1;1,a,1;1,1,a]; $A


$$\begin{pmatrix}a & 1 & 1 \\ 1 & a & 1 \\ 1 & 1 & a \\ \end{pmatrix}$$\>$&det(A), $&factor(%)


$$\left(a-1\right)^2\,\left(a+2\right)$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-087.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-087.png)

\>$&invert(A) with a=0


$$\begin{pmatrix}-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\ \frac{1  }{2} & -\frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2} & -  \frac{1}{2} \\ \end{pmatrix}$$\>A &= [1,a;b,2]; $A


$$\begin{pmatrix}1 & a \\ b & 2 \\ \end{pmatrix}$$Seperti semua variabel simbolik, matriks ini dapat digunakan dalam
ekspresi simbolik lainnya.


\>$&det(A-x\*ident(2)), $&solve(%,x)


$$\left[ x=\frac{3-\sqrt{4\,a\,b+1}}{2} , x=\frac{\sqrt{4\,a\,b+1}+3  }{2} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-091.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-091.png)

Nilai eigen juga dapat dihitung secara otomatis. Hasilnya adalah
sebuah vektor dengan dua vektor nilai eigen dan kelipatannya.


\>$&eigenvalues([a,1;1,a])


$$\left[ \left[ a-1 , a+1 \right]  , \left[ 1 , 1 \right]  \right] $$Untuk mengekstrak vektor eigen tertentu, diperlukan pengindeksan yang
cermat.


\>$&eigenvectors([a,1;1,a]), &%[2][1][1]


$$\left[ \left[ \left[ a-1 , a+1 \right]  , \left[ 1 , 1 \right]    \right]  , \left[ \left[ \left[ 1 , -1 \right]  \right]  , \left[   \left[ 1 , 1 \right]  \right]  \right]  \right] $$    
                                   [1, - 1]
    

Matriks simbolik dapat dievaluasi dalam Euler secara numerik seperti
halnya ekspresi simbolik lainnya.


\>A(a=4,b=5)


                1             4 
                5             2 

Dalam ekspresi simbolis, gunakan dengan.


\>$&A with [a=4,b=5]


$$\begin{pmatrix}1 & 4 \\ 5 & 2 \\ \end{pmatrix}$$Akses ke baris matriks simbolik bekerja seperti halnya matriks
numerik.


\>$&A[1]


$$\left[ 1 , a \right] $$Ekspresi simbolik dapat berisi sebuah penugasan. Dan itu mengubah
matriks A.


\>&A[1,1]:=t+1; $&A


$$\begin{pmatrix}t+1 & a \\ b & 2 \\ \end{pmatrix}$$Terdapat fungsi-fungsi simbolik dalam Maxima untuk membuat vektor dan
matriks. Untuk hal ini, lihat dokumentasi Maxima atau tutorial tentang
Maxima di EMT.


\>v &= makelist(1/(i+j),i,1,3); $v


$$\left[ \frac{1}{j+1} , \frac{1}{j+2} , \frac{1}{j+3} \right] $$\>B &:= [1,2;3,4]; $B, $&invert(B)


$$\begin{pmatrix}-2 & 1 \\ \frac{3}{2} & -\frac{1}{2} \\   \end{pmatrix}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-099.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-099.png)

Hasilnya dapat dievaluasi secara numerik dalam Euler. Untuk informasi
lebih lanjut tentang Maxima, lihat pengantar Maxima.


\>$&invert(B)()


               -2             1 
              1.5          -0.5 

Euler juga memiliki sebuah fungsi yang kuat xinv(), yang melakukan
usaha yang lebih besar dan mendapatkan hasil yang lebih tepat.


Perhatikan, bahwa dengan &amp;:= matriks B telah didefinisikan sebagai
simbolik dalam ekspresi simbolik dan sebagai numerik dalam ekspresi
numerik. Jadi kita dapat menggunakannya di sini.


\>longest B.xinv(B)


                          1                       0 
                          0                       1 

Misalnya, nilai eigen dari A dapat dihitung secara numerik.


\>A=[1,2,3;4,5,6;7,8,9]; real(eigenvalues(A))


    [16.1168,  -1.11684,  0]

Atau secara simbolis. Lihat tutorial tentang Maxima untuk mengetahui
detailnya.


\>$&eigenvalues(@A)


$$\left[ \left[ \frac{15-3\,\sqrt{33}}{2} , \frac{3\,\sqrt{33}+15}{2}   , 0 \right]  , \left[ 1 , 1 , 1 \right]  \right] $$# Nilai Numerik dalam Ekspresi simbolik

Ekspresi simbolik hanyalah sebuah string yang berisi ekspresi. Jika
kita ingin mendefinisikan nilai baik untuk ekspresi simbolik maupun
ekspresi numerik, kita harus menggunakan “&amp;:=”.


\>A &:= [1,pi;4,5]


                1       3.14159 
                4             5 

Masih ada perbedaan antara bentuk numerik dan bentuk simbolik. Ketika
mentransfer matriks ke bentuk simbolik, perkiraan pecahan untuk
bilangan real akan digunakan.


\>$&A


$$\begin{pmatrix}1 & \frac{1146408}{364913} \\ 4 & 5 \\ \end{pmatrix}$$Untuk menghindari hal ini, ada fungsi “mxmset(variable)”.


\>mxmset(A); $&A


$$\begin{pmatrix}1 & 3.141592653589793 \\ 4 & 5 \\ \end{pmatrix}$$Maxima juga dapat menghitung dengan angka floating point, dan bahkan
dengan angka mengambang yang besar dengan 32 digit. Namun, evaluasinya
jauh lebih lambat.


\>$&bfloat(sqrt(2)), $&float(sqrt(2))


$$1.414213562373095$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-104.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-104.png)

Ketepatan angka floating point yang besar dapat diubah.


\>&fpprec:=100; &bfloat(pi)


    
            3.14159265358979323846264338327950288419716939937510582097494\
    4592307816406286208998628034825342117068b0
    

Variabel numerik dapat digunakan dalam ekspresi simbolik apa pun
dengan menggunakan “@var”.


Perhatikan bahwa ini hanya diperlukan, jika variabel telah
didefinisikan dengan “:=” atau “=” sebagai variabel numerik.


\>B:=[1,pi;3,4]; $&det(@B)


$$-5.424777960769379$$# Demo - Suku Bunga

Di bawah ini, kami menggunakan Euler Math Toolbox (EMT) untuk
menghitung suku bunga. Kami melakukannya secara numerik dan simbolis
untuk menunjukkan kepada Anda bagaimana Euler dapat digunakan untuk
memecahkan masalah kehidupan nyata.


Asumsikan Anda memiliki modal awal sebesar 5000 (katakanlah dalam
dolar).


\>K=5000


    5000

Sekarang kita asumsikan suku bunga 3% per tahun. Mari kita tambahkan
satu suku bunga sederhana dan hitung hasilnya.


\>K\*1.03


    5150

Euler juga akan memahami sintaks berikut ini.


\>K+K\*3%


    5150

Tetapi lebih mudah untuk menggunakan faktor


\>q=1+3%, K\*q


    1.03
    5150

Untuk 10 tahun, kita cukup mengalikan faktor-faktor tersebut dan
mendapatkan nilai akhir dengan suku bunga majemuk.


\>K\*q^10


    6719.58189672

Untuk tujuan kita, kita bisa mengatur formatnya menjadi 2 digit
setelah titik desimal.


\>format(12,2); K\*q^10


        6719.58 

Mari kita cetak angka yang dibulatkan menjadi 2 digit dalam kalimat
lengkap.


\>"Starting from " + K + "$ you get " + round(K\*q^10,2) + "$."


    Starting from 5000$ you get 6719.58$.

Bagaimana jika kita ingin mengetahui hasil antara dari tahun ke-1
hingga tahun ke-9? Untuk hal ini, bahasa matriks Euler sangat
membantu. Anda tidak perlu menulis perulangan, tetapi cukup masukkan


\>K\*q^(0:10)


    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Bagaimana keajaiban ini bekerja? Pertama, ekspresi 0:10 mengembalikan
sebuah vektor bilangan bulat.


\>short 0:10


    [0,  1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Kemudian semua operator dan fungsi dalam Euler dapat diterapkan pada
vektor elemen demi elemen. Jadi


\>short q^(0:10)


    [1,  1.03,  1.0609,  1.0927,  1.1255,  1.1593,  1.1941,  1.2299,
    1.2668,  1.3048,  1.3439]

adalah vektor faktor q^0 hingga q^10. Ini dikalikan dengan K, dan kita
mendapatkan vektor nilai.


\>VK=K\*q^(0:10);


Tentu saja, cara yang realistis untuk menghitung suku bunga ini adalah
dengan membulatkan ke sen terdekat setelah setiap tahun. Mari kita
tambahkan fungsi untuk ini.


\>function oneyear (K) := round(K\*q,2)


Mari kita bandingkan kedua hasil tersebut, dengan dan tanpa
pembulatan.


\>longest oneyear(1234.57), longest 1234.57\*q


                    1271.61 
                  1271.6071 

Sekarang tidak ada rumus sederhana untuk tahun ke-n, dan kita harus
mengulang selama bertahun-tahun. Euler menyediakan banyak solusi untuk
ini.


Cara termudah adalah iterasi fungsi, yang mengulang fungsi yang
diberikan beberapa kali.


\>VKr=iterate("oneyear",5000,10)


    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Kita bisa mencetaknya dengan cara yang bersahabat, menggunakan format
kami dengan angka desimal yang tetap.


\>VKr'


        5000.00 
        5150.00 
        5304.50 
        5463.64 
        5627.55 
        5796.38 
        5970.27 
        6149.38 
        6333.86 
        6523.88 
        6719.60 

Untuk mendapatkan elemen tertentu dari vektor, kita menggunakan indeks
dalam tanda kurung siku.


\>VKr[2], VKr[1:3]


        5150.00 
        5000.00     5150.00     5304.50 

Yang mengejutkan, kita juga dapat menggunakan vektor indeks. Ingatlah
bahwa 1:3 menghasilkan vektor [1,2,3].


Mari kita bandingkan elemen terakhir dari nilai yang dibulatkan dengan
nilai penuh.


\>VKr[-1], VK[-1]


        6719.60 
        6719.58 

Perbedaannya sangat kecil.


# Menyelesaikan Persamaan

Sekarang kita ambil fungsi yang lebih maju, yang menambahkan tingkat
uang tertentu setiap tahun.


\>function onepay (K) := K\*q+R


Kita tidak perlu menentukan q atau R untuk definisi fungsi. Hanya jika
kita menjalankan perintah, kita harus mendefinisikan nilai-nilai ini.
Kami memilih R = 200.


\>R=200; iterate("onepay",5000,10)


    Real 1 x 11 matrix
    
        5000.00     5350.00     5710.50     6081.82     ...

Bagaimana jika kita menghapus jumlah yang sama setiap tahun?


\>R=-200; iterate("onepay",5000,10)


    Real 1 x 11 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Kami melihat bahwa uangnya berkurang. Jelas, jika kita hanya
mendapatkan 150 bunga di tahun pertama, tetapi menghapus 200, kita
kehilangan uang setiap tahun.


Bagaimana kita dapat menentukan berapa tahun uang itu akan bertahan?
Kita harus menulis perulangan untuk ini. Cara termudah adalah dengan
melakukan perulangan yang cukup lama.


\>VKR=iterate("onepay",5000,50)


    Real 1 x 51 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Dengan menggunakan bahasa matriks, kita dapat menentukan nilai negatif
pertama dengan cara berikut.


\>min(nonzeros(VKR<0))


          48.00 

Alasannya adalah karena nonzeros(VKR&lt;0) mengembalikan vektor dengan
indeks i, di mana VKR[i]&lt;0, dan min menghitung indeks minimal.


Karena vektor selalu dimulai dengan indeks 1, maka jawabannya adalah
47 tahun.


Fungsi iterate() memiliki satu trik lagi. Fungsi ini dapat menerima
kondisi akhir sebagai argumen. Kemudian fungsi ini akan mengembalikan
nilai dan jumlah iterasi.


\>{x,n}=iterate("onepay",5000,till="x<0"); x, n,


         -19.83 
          47.00 

Mari kita coba menjawab pertanyaan yang lebih ambigu. Anggaplah kita
tahu bahwa nilainya adalah 0 setelah 50 tahun. Berapakah tingkat suku
bunganya?


Ini adalah pertanyaan yang hanya bisa dijawab secara numerik. Di bawah
ini, kami akan menurunkan rumus yang diperlukan. Kemudian Anda akan
melihat bahwa tidak ada rumus yang mudah untuk suku bunga. Namun untuk
saat ini, kita akan mencari solusi numerik.


Langkah pertama adalah mendefinisikan sebuah fungsi yang melakukan
iterasi sebanyak n kali. Kita tambahkan semua parameter ke fungsi ini.


\>function f(K,R,P,n) := iterate("x\*(1+P/100)+R",K,n;P,R)[-1]


Perulangannya sama seperti di atas


$$x_{n+1} = x_n \cdot \left(1+ \frac{P}{100}\right) + R$$Tetapi kita tidak lagi menggunakan nilai global R dalam ekspresi kita.
Fungsi-fungsi seperti iterate() memiliki trik khusus dalam Euler. Anda
bisa mengoper nilai variabel dalam ekspresi sebagai parameter titik
koma. Dalam hal ini P dan R.


Selain itu, kita hanya tertarik pada nilai terakhir. Jadi kita
mengambil indeks [-1].


Mari kita coba sebuah tes.


\>f(5000,-200,3,47)


         -19.83 

Sekarang kita bisa menyelesaikan masalah kita.


\>solve("f(5000,-200,x,50)",3)


           3.15 

Rutin penyelesaian menyelesaikan ekspresi = 0 untuk variabel x.
Jawabannya adalah 3,15% per tahun. Kita mengambil nilai awal 3% untuk
algoritma ini. Fungsi solve() selalu membutuhkan nilai awal.


Kita dapat menggunakan fungsi yang sama untuk menyelesaikan pertanyaan
berikut: Berapa banyak yang dapat kita hapus per tahun sehingga modal
awal habis setelah 20 tahun dengan asumsi tingkat bunga 3% per tahun.


\>solve("f(5000,x,3,20)",-200)


        -336.08 

Perhatikan bahwa Anda tidak dapat menyelesaikan jumlah tahun, karena
fungsi kita mengasumsikan n sebagai nilai bilangan bulat.


## Solusi Simbolik untuk Masalah Suku Bunga

Kita dapat menggunakan bagian simbolik dari Euler untuk mempelajari
masalah ini. Pertama, kita mendefinisikan fungsi onepay() secara
simbolik.


\>function op(K) &= K\*q+R; $&op(K)


$$R+q\,K$$Sekarang kita bisa mengulangi hal ini.


\>$&op(op(op(op(K)))), $&expand(%)


$$q^3\,R+q^2\,R+q\,R+R+q^4\,K$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-109.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Aljabar%20Materi-109.png)

Kita melihat sebuah pola. Setelah n periode, kita memiliki


$$K_n = q^n K + R (1+q+\ldots+q^{n-1}) = q^n K + \frac{q^n-1}{q-1} R$$Rumus tersebut adalah rumus untuk jumlah geometris, yang dikenal
dengan Maxima.


\>&sum(q^k,k,0,n-1); $& % = ev(%,simpsum)


$$\sum_{k=0}^{n-1}{q^{k}}=\frac{q^{n}-1}{q-1}$$Ini sedikit rumit. Penjumlahan dievaluasi dengan flag “simpsum” untuk
menguranginya menjadi hasil bagi.


Mari kita buat sebuah fungsi untuk ini.


\>function fs(K,R,P,n) &= (1+P/100)^n\*K + ((1+P/100)^n-1)/(P/100)\*R; $&fs(K,R,P,n)


$$\frac{100\,\left(\left(\frac{P}{100}+1\right)^{n}-1\right)\,R}{P}+K  \,\left(\frac{P}{100}+1\right)^{n}$$Fungsi ini melakukan hal yang sama seperti fungsi f kita sebelumnya.
Tetapi fungsi ini lebih efektif.


\>longest f(5000,-200,3,47), longest fs(5000,-200,3,47)


         -19.82504734650985 
         -19.82504734652684 

Sekarang kita dapat menggunakannya untuk menanyakan waktu n. Kapan
modal kita habis? Perkiraan awal kita adalah 30 tahun.


\>solve("fs(5000,-330,3,x)",30)


          20.51 

Jawaban ini mengatakan bahwa nilai tersebut akan menjadi negatif
setelah 21 tahun.


Kita juga bisa menggunakan sisi simbolis dari Euler untuk menghitung
rumus pembayaran.


Asumsikan kita mendapatkan pinjaman sebesar K, dan membayar n kali
pembayaran sebesar R (dimulai setelah tahun pertama) sehingga
menyisakan sisa utang sebesar Kn (pada saat pembayaran terakhir).
Rumus untuk hal ini adalah sebagai berikut


\>equ &= fs(K,R,P,n)=Kn; $&equ


$$\frac{100\,\left(\left(\frac{P}{100}+1\right)^{n}-1\right)\,R}{P}+K  \,\left(\frac{P}{100}+1\right)^{n}={\it Kn}$$Biasanya rumus ini diberikan dalam bentuk


$$i = \frac{P}{100}$$\>equ &= (equ with P=100\*i); $&equ


$$\frac{\left(\left(i+1\right)^{n}-1\right)\,R}{i}+\left(i+1\right)^{  n}\,K={\it Kn}$$Kita dapat menyelesaikan laju R secara simbolis.


\>$&solve(equ,R)


$$\left[ R=\frac{i\,{\it Kn}-i\,\left(i+1\right)^{n}\,K}{\left(i+1  \right)^{n}-1} \right] $$Seperti yang dapat Anda lihat dari rumusnya, fungsi ini mengembalikan
kesalahan floating point untuk i = 0. Euler tetap memplotnya.


Tentu saja, kita memiliki batas berikut.


\>$&limit(R(5000,0,x,10),x,0)


$$\lim_{x\rightarrow 0}{R\left(5000 , 0 , x , 10\right)}$$Jelasnya, tanpa bunga kita harus membayar kembali 10 suku bunga 500.


Persamaan ini juga dapat diselesaikan untuk n. Akan terlihat lebih
baik jika kita menerapkan beberapa penyederhanaan.


\>fn &= solve(equ,n) | ratsimp; $&fn


$$\left[ n=\frac{\log \left(\frac{R+i\,{\it Kn}}{R+i\,K}\right)}{  \log \left(i+1\right)} \right] $$

Soal latihan EMT materi aljabar disertai latex


# R.2

No 50


Sederhanakan


$$\left(\frac{{125p^{12}q^{-14}r^{22}}}{{25p^8q^6r^{-15}}}\right)^{-4}$$\>$&(((125\*p^12\*q^-14\*r^22)/(25\*p^8\*q^6\*r^-15))^-4)


$$\frac{q^{80}}{625\,p^{16}\,r^{148}}$$dapat kita peroleh hasil yang lebih sederhana setelah kita operasiakan


No 90


Hitung


$$\frac{2^6 \cdot 2^{-3}}{2^{10} \cdot 2^{-8}}$$\>$&((2^6\*2^-3)/2^10/2^-8)


$$2$$dengan operasi penyelesaian sifat pangkat dapat kita peroleh hasilnya
2


No 91


Hitung


$$\frac{4(8 - 6)^2 - 4 \cdot 3 + 2 \cdot 8}{3^1 + 19^0}$$\>$&((4\*(8-6)^2-4\*3+2\*8)/3^1+10^0)


$$\frac{23}{3}$$kita bisa memperoleh bentuk sederhana setelah mengoperasikannya


No 104


Sederhanakan


$$\left( m^{x - b} \cdot n^{x + b} \right)^x \left( m^b \cdot n^{-b} \right)^x$$\>$&(m^x-b\*n^x+b)^x(m^b\*n^-b)^x


$$\left(-b\,n^{x}+m^{x}+b\right)^{x^{x}\left(\frac{m^{b}}{n^{b}}  \right)}$$kita bisa memperoleh bentuk sederhana setelah mengoperasikannya


No 105


Sederhanakan


$$\left[\frac{{(3x^a y^b)^3}}{{(-3x^a y^b)^2}}\right]^2$$\>$&(((3\*x^a\*y^b)^3)/(((-3\*x^a\*y^b)^2)^2))


$$\frac{1}{3\,x^{a}\,y^{b}}$$kita bisa memperoleh bentuk sederhana setelah mengoperasikannya


# R.3 No 20

$$\left(z-1\right)\left(z-2\right)$$

jabarkan


\>$&expand((z-1)\*(z-2))


$$z^2-3\,z+2$$Kita bisa melihat bentuk expand yang lebih sederhana


No 21


$$\left(x+6\right)\left(x+3\right)$$

jabarkan


\>$&expand((x+6)\*(x+3))


$$x^2+9\,x+18$$Kita bisa melihat bentuk expand yang lebih sederhana


No 22


$$\left(a-8\right)\left(a-1\right)$$

jabarkan


\>$&expand((a-8)\*(a-1))


$$a^2-9\,a+8$$Kita bisa melihat bentuk expand yang lebih sederhana


No 23


$$\left(2a+3\right)\left(a+5\right)$$

jabarkan


\>$&expand((2\*a+3)\*(a+5))


$$2\,a^2+13\,a+15$$Kita bisa melihat bentuk expand yang lebih sederhana


No 24


$$\left(3b+1\right)\left(b-2\right)$$

jabarkan


\>$&expand((3\*b+1)\*(b-2))


$$3\,b^2-5\,b-2$$Kita bisa melihat bentuk expand yang lebih sederhana


No 25


$$\left(2x+3y\right)\left(2x+y\right)$$

jabarkan


\>$&expand((2\*x+3\*y)\*(2\*x+y))


$$3\,y^2+8\,x\,y+4\,x^2$$Kita bisa melihat bentuk expand yang lebih sederhana


# R.4

No 47


$$z^2-81$$faktorkan


\>$&factor(z^2-81)


$$\left(z-9\right)\,\left(z+9\right)$$Kita bisa melihat bentuk pemfaktoran yang lebih sederhana


N0 81


$$8x^2-32$$faktorkan


\>$&factor(8\*x^2-32)


$$8\,\left(x-2\right)\,\left(x+2\right)$$Kita bisa melihat bentuk pemfaktoran yang lebih sederhana


No 82


$$6y^2-6$$faktorkan


\>$&factor(6\*y^2-6)


$$6\,\left(y-1\right)\,\left(y+1\right)$$Kita bisa melihat bentuk pemfaktoran yang lebih sederhana


No 90


$$x^2-4x-21$$faktorkan


\>$&factor(x^2-4\*x-21)


$$\left(x-7\right)\,\left(x+3\right)$$Kita bisa melihat bentuk pemfaktoran yang lebih sederhana


No 91


$$2a^2 +9a +4$$faktorkan


\>$&factor(2\*a^2+9\*a+4)


$$\left(a+4\right)\,\left(2\,a+1\right)$$Kita bisa melihat bentuk pemfaktoran yang lebih sederhana


# R.5

No 47


$$12z^2 + z = 6$$temukan z


\>$&solve(12\*z^2+z=6)


$$\left[ z=-\frac{3}{4} , z=\frac{2}{3} \right] $$kita bisa menemukan variabel dengan operasi aljabar yang ada


No 53


$$x^2-36=0$$temukan x


\>$&solve(x^2-36=0)


$$\left[ x=-6 , x=6 \right] $$kita bisa menemukan variabel dengan operasi aljabar yang ada


No 54


$$y^2-81=0$$temukan y


\>$&solve(y^2-81=0)


$$\left[ y=-9 , y=9 \right] $$kita bisa menemukan variabel dengan operasi aljabar yang ada


No 60


$$5x^2 -75$$temukan x


\>$&solve(5\*x^2-75=0)


$$\left[ x=-\sqrt{15} , x=\sqrt{15} \right] $$kita bisa menemukan variabel dengan operasi aljabar yang ada


No 86


$$\left(3x^2+7x-20\right)\left(x^2-4x\right)$$temukan x


\>$&solve((3\*x^2+7\*x-20)\*(x^2-4\*x))


$$\left[ x=\frac{5}{3} , x=-4 , x=0 , x=4 \right] $$kita bisa menemukan variabel dengan operasi aljabar yang ada


# R.6

No 9


Simplify


$$\frac{x^2-4}{x^2-4x+4}$$$$\frac{(x+2)(x-2)}{(x-2)^2}$$\>$&((x+2)\*(x-2))/(x-2)^2


$$\frac{x+2}{x-2}$$Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


No 11


Simplify


$$\frac{x^3-6x^2+9x}{x^3-3x^2}$$$$\frac{(x-3)^2 \cdot x}{(x-3) \cdot x^2}$$\>$&((x-3)^2 \* x)/((x-3) \* x^2)


$$\frac{x-3}{x}$$Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


No 17


$$\frac{r-s}{r+s} \cdot \frac{r^2-s^2}{(r-s)^2}$$\>$&(r^2-s^2)/(r-s)\*(s+r), $&ratsimp(%)


$$s^2+2\,r\,s+r^2$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-051.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-051.png)

Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


No 28


Simplify


$$\frac{(c^3+8)}{(c^2-4)} : \frac{(c^2-2c+4)}{(c^2-4c+4)}$$\>$&ratsimp((c^3+8)/(c^2-4))/((c^2-2\*c+4)/(c^2-4\*c+4)), $&ratsimp(%)


$$c-2$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-054.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-054.png)

Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


No 40


$$\frac{6}{y^2+6y+9} - \frac{5}{y-3}$$\>$&expand(6/y^2+6\*y+9)-(5/y-3), $&ratsimp(%)


$$\frac{6\,y^3+12\,y^2-5\,y+6}{y^2}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-057.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-057.png)

Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


No 62


Simplify


$$\frac{\frac{a^2}{b}+\frac{b^2}{a}}{{a^2-ab+b^2}}$$

Penyelesaian:


\>$&factor((a^2/b)+(b^2/a))/(a^2-a\*b+b^2)


$$\frac{b+a}{a\,b}$$Dengan penyederhanaan kita bisa memperoleh hasil yang lebih simpel


# Review Exercice

No 70


$$(x^n + 10)(x^n -4)$$\>$&expand((x^n + 10)\*(x^n - 4))


$$x^{2\,n}+6\,x^{n}-40$$Kita bisa melihat bentuk expand yang lebih sederhana 


No 71


$$(a^n - b^n)^3$$\>$&expand((t^a + t^(-a))^2)


$$t^{2\,a}+\frac{1}{t^{2\,a}}+2$$Kita bisa melihat bentuk expand yang lebih sederhana


 No 72  

$$(y^z - z^c)(y^b + z^c)$$\>$&expand((y^z - z^c)\*(y^b + z^c))


$$-z^{2\,c}+y^{z}\,z^{c}-y^{b}\,z^{c}+y^{z+b}$$Kita bisa melihat bentuk expand yang lebih sederhana


No 73


$$(a^n - b^n)^3$$\>$&showev('expand((a^n - b^n)^3)), $&expand((a^n - b^n)^3)


$$-b^{3\,n}+3\,a^{n}\,b^{2\,n}-3\,a^{2\,n}\,b^{n}+a^{3\,n}$$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-068.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-068.png)

Kita bisa melihat bentuk expand yang lebih sederhana 


No 76


$$(m^6-m^3)$$\>$&factor(m^6-m^3)


$$\left(m-1\right)\,m^3\,\left(m^2+m+1\right)$$Kita bisa melihat bentuk expand yang lebih sederhana


## 2.3 Exercise Set

Given that


$$f(x) = 3x + 1$$$$g(x) = x^2 - 2x -6$$$$h(x) = x^3$$

Find each of the following


Menyimpan semua nilai fx, gx, dan hx.


\>fx &= 3\*x + 1


    
                                   3 x + 1
    

\>gx &= x^2 - 2\*x - 6


    
                                  2
                                 x  - 2 x - 6
    

\>hx &= x^3


    
                                       3
                                      x
    

No 1


mencari nilai


$$(f \circ g)(-1)$$

Penyelesaian:


fungsi komposisi di atas juga dapat ditulis sebagai :


$$(f(g(-1))$$mencari nilai g(-1)


\>fx(gx(-1))


    -8

didapatkan nilai fungsi komposisi dengan operasi aljabar


No 2


mencari nilai g(f(-2)


\>gx(fx(-2))


    29

didapatkan nilai fungsi komposisi dengan operasi aljabar


No 3


mencari nilai h(f(1)


\>hx(fx(1))


    64

didapatkan nilai fungsi komposisi dengan operasi aljabar


No 5


mencari nilai g(f(5)


\>gx(fx(5))


    218

didapatkan nilai fungsi komposisi dengan operasi aljabar


No 8


mencari nilai h(g(3)


\>hx(gx(3))


    -27

didapatkan nilai fungsi komposisi dengan operasi aljabar


# Exercise 3.1

NO 11


Simplify


$$(-5+3i) + (7+8i)$$\>bilangan1 = -5 + 3\*I, bilangan2 = 7 + 8\*I, bilangan1 + bilangan2


    -5+3i
    7+8i
    2+11i

Didapatkan hasil operasi string 


NO 12


Simplify


$$(-6-5i) + (9+2i)$$\>bilangan1 = -6 - 5\*I, bilangan2 = 9 + 2\*I, bilangan1 + bilangan2


    -6-5i
    9+2i
    3-3i

Didapatkan hasil operasi string 


NO 13


Simplify


$$(4-9i) + (1-4i)$$\>bilangan1 = 4 - 9\*I, bilangan2 = 1 -4\*I, bilangan1 + bilangan2


    4-9i
    1-4i
    5-13i

NO 14


Simplify


$$(7-2i) + (4-5i)$$\>bilangan1 = 7 - 2\*I, bilangan2 = 4 -5\*I, bilangan1 + bilangan2


    7-2i
    4-5i
    11-7i

Didapatkan hasil operasi string 


NO 15


Simplify


$$(12+3i) + (-8+5i)$$\>bilangan1 = 12+3\*I, bilangan2 = -8+5\*I, bilangan1 + bilangan2


    12+3i
    -8+5i
    4+8i

Didapatkan hasil operasi string


# 3.4 

No 1


 Solve


 latex: \frac{1}{4} + \frac{1}{5} = \frac{1}{t}


\>$&(1/4+1/5=1/t), $&solve(1/4+1/5=1/t)


$$\left[ t=\frac{20}{9} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-082.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-082.png)

Penyelesaian aljabar dapat kita peroleh nilai variabel


No 2


Solve


$$\frac{1}{3} + \frac{5}{6} = \frac{1}{x}$$\>$&(1/3-5/6=1/x), $&solve(1/3-5/6=1/x)


$$\left[ x=-2 \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-085.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-085.png)

Penyelesaian aljabar dapat kita peroleh nilai variabel


No 3


Solve


$$\frac{x+2}{4} - \frac{x-1}{5} = 15$$\>$&solve(((x+2)/4)-((x-1)/5)=15)


$$\left[ x=286 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 4


Solve


$$\frac{t+1}{3} - \frac{t-1}{2} = 1$$\>$&solve(((t+1)/3)-((t-1)/2))


$$\left[ t=5 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 5


Solve


$$\frac{1}{2} + \frac{2}{x} = \frac{1}{3} +\frac{3}{x}$$\>$&solve(1/2+2/x=1/3+3/x)


$$\left[ x=6 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


# 3.5

No 23


Solve


$$\left| x+3 \right|-2 = 8$$\>$&solve(abs(x+3)-2=8, x)


$$\left[ \left| x+3\right| =10 \right] $$\>$&solve((x+3)=10)


$$\left[ x=7 \right] $$dapat kita peroleh nilai variabel dari operasi nilai mutlak


No 24


Solve


$$\left| x-4 \right|+3 = 9$$\>$&solve(abs(x-4)+3=9, x)


$$\left[ \left| x-4\right| =6 \right] $$\>$&solve((x-4)=6)


$$\left[ x=10 \right] $$dapat kita peroleh nilai variabel dari operasi nilai mutlak


No 25


$$\left| 3x-4 \right|-4 = -1$$\>$&solve(abs(3\*x-4)-4=-1, x)


$$\left[ \left| 3\,x-4\right| =3 \right] $$\>$&solve((3\*x-4)=3)


$$\left[ x=\frac{7}{3} \right] $$dapat kita peroleh nilai variabel dari operasi nilai mutlak


No 26


$$\left| 2x-1 \right|-5= -3$$\>$&solve(abs(2\*x-1)-5=-3, x)


$$\left[ \left| 2\,x-1\right| =2 \right] $$\>$&solve((2\*x-1)=2)


$$\left[ x=\frac{3}{2} \right] $$dapat kita peroleh nilai variabel dari operasi nilai mutlak


No 27


$$\left| 4x-3 \right|+1= 7$$\>$&solve(abs(4\*x-3)+1=7, x)


$$\left[ \left| 4\,x-3\right| =6 \right] $$\>$&solve((4\*x-3)=6)


$$\left[ x=\frac{9}{4} \right] $$dapat kita peroleh nilai variabel dari operasi nilai mutlak


# Chapter 3 Test

No 9


Solve


$$\sqrt{x+4}-2=1$$\>$&solve(((x+4)^1/2)-2=1)


$$\left[ x=2 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 10


Solve


$$\sqrt{x+4}-\sqrt{x-4}=2$$\>$&solve(((x+4)^1/2)-((x-4)^1/2=2))


$$\left[ x=8 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 11


$$\left| x+4 \right| = 7$$\>$&solve((x+4)=7)


$$\left[ x=3 \right] $$Penyelesaian aljabar dapat kira peroleh nilai variabel


No 12


$$\left| 4y-3 \right| = 5$$\>$&solve((4\*y-3)=5)


$$\left[ y=2 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 13


Selesaikan dan tulis notasi interval untuk kumpulan solusi.


kemudian grafik set solusi


$$\left|x+3\right|\leq4$$\>&load(fourier\_elim)


    
            C:/Program Files/Euler x64/maxima/share/maxima/5.35.1/share/f\
    ourier_elim/fourier_elim.lisp
    

\>$&fourier\_elim([abs(x+3)<=4], [x])


$$\left[ x=1 \right] \lor \left[ x=-7 \right] \lor \left[ -7<x , x<1   \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


# 4.1

No 36


Temukan nol dari fungsi polinomial dan nyatakan keragaman
masing-masing


$$f(x) = (x^2-5x+6)^2$$\>$&solve((x^2-5\*x+6)^2)


$$\left[ x=3 , x=2 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 37


Temukan nol dari fungsi polinomial dan nyatakan keragaman
masing-masing


$$f(x) = x^4-4x^2+3$$\>$&solve(x^4-4\*x^2+3)


$$\left[ x=-1 , x=1 , x=-\sqrt{3} , x=\sqrt{3} \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 38


Temukan nol dari fungsi polinomial dan nyatakan keragaman
masing-masing


$$f(x) = x^4-10x^2+9$$\>$&solve(x^4-10\*x^2+9)


$$\left[ x=-1 , x=1 , x=-3 , x=3 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 39


Temukan nol dari fungsi polinomial dan nyatakan keragaman
masing-masing


$$f(x) = x^3-3x^2-x-3$$\>$&solve(x^3-3\*x^2-x-3)


$$\left[ x=\frac{4\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)}{3  \,\left(\frac{\sqrt{179}}{3^{\frac{3}{2}}}+3\right)^{\frac{1}{3}}}+  \left(\frac{\sqrt{179}}{3^{\frac{3}{2}}}+3\right)^{\frac{1}{3}}\,  \left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)+1 , x=\left(\frac{  \sqrt{179}}{3^{\frac{3}{2}}}+3\right)^{\frac{1}{3}}\,\left(\frac{  \sqrt{3}\,i}{2}-\frac{1}{2}\right)+\frac{4\,\left(-\frac{\sqrt{3}\,i  }{2}-\frac{1}{2}\right)}{3\,\left(\frac{\sqrt{179}}{3^{\frac{3}{2}}}  +3\right)^{\frac{1}{3}}}+1 , x=\left(\frac{\sqrt{179}}{3^{\frac{3}{2  }}}+3\right)^{\frac{1}{3}}+\frac{4}{3\,\left(\frac{\sqrt{179}}{3^{  \frac{3}{2}}}+3\right)^{\frac{1}{3}}}+1 \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 40


Temukan nol dari fungsi polinomial dan nyatakan keragaman
masing-masing


$$f(x) = x^3-x^2-2x+2$$\>$&solve(x^3-x^2-2\*x+2)


$$\left[ x=-\sqrt{2} , x=\sqrt{2} , x=1 \right] $$Penyelesaian aljabar dapat kira peroleh nilai variabel


# 4.1

Nomor 11-15


Gunakan pembagian sintetis untuk menemukan hasil bagi dan sisa.


No 11


$$\frac{2x^4 + 7x^3 + x - 12}{x + 3}$$\>$&((2\*x^4+7\*x^3+x-12)/(x+3)), $&solve((2\*x^4+7\*x^3+x-12)/(x+3))


$$\left[ x=-\frac{\sqrt{\frac{125\,3^{\frac{3}{2}}\,\left(\frac{5\,  \sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{6}}  }{8\,\sqrt{48\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-  \frac{293}{8}\right)^{\frac{2}{3}}+147\,\left(\frac{5\,\sqrt{68213}  }{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}-412}}-  \left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}  \right)^{\frac{1}{3}}+\frac{103}{12\,\left(\frac{5\,\sqrt{68213}}{2  \,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}}+\frac{49}{8}}  }{2}-\frac{\sqrt{48\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}  }-\frac{293}{8}\right)^{\frac{2}{3}}+147\,\left(\frac{5\,\sqrt{68213  }}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}-412}}{8\,  \sqrt{3}\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293  }{8}\right)^{\frac{1}{6}}}-\frac{7}{8} , x=\frac{\sqrt{\frac{125\,3  ^{\frac{3}{2}}\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-  \frac{293}{8}\right)^{\frac{1}{6}}}{8\,\sqrt{48\,\left(\frac{5\,  \sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{2}{3}}  +147\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}  \right)^{\frac{1}{3}}-412}}-\left(\frac{5\,\sqrt{68213}}{2\,6^{  \frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}+\frac{103}{12\,  \left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}  \right)^{\frac{1}{3}}}+\frac{49}{8}}}{2}-\frac{\sqrt{48\,\left(  \frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{  \frac{2}{3}}+147\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-  \frac{293}{8}\right)^{\frac{1}{3}}-412}}{8\,\sqrt{3}\,\left(\frac{5  \,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{6  }}}-\frac{7}{8} , x=-\frac{\sqrt{-\frac{125\,3^{\frac{3}{2}}\,\left(  \frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{  \frac{1}{6}}}{8\,\sqrt{48\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{  3}{2}}}-\frac{293}{8}\right)^{\frac{2}{3}}+147\,\left(\frac{5\,  \sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}  -412}}-\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8  }\right)^{\frac{1}{3}}+\frac{103}{12\,\left(\frac{5\,\sqrt{68213}}{2  \,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}}+\frac{49}{8}}  }{2}+\frac{\sqrt{48\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}  }-\frac{293}{8}\right)^{\frac{2}{3}}+147\,\left(\frac{5\,\sqrt{68213  }}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}-412}}{8\,  \sqrt{3}\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293  }{8}\right)^{\frac{1}{6}}}-\frac{7}{8} , x=\frac{\sqrt{-\frac{125\,3  ^{\frac{3}{2}}\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-  \frac{293}{8}\right)^{\frac{1}{6}}}{8\,\sqrt{48\,\left(\frac{5\,  \sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{2}{3}}  +147\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}  \right)^{\frac{1}{3}}-412}}-\left(\frac{5\,\sqrt{68213}}{2\,6^{  \frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{3}}+\frac{103}{12\,  \left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}  \right)^{\frac{1}{3}}}+\frac{49}{8}}}{2}+\frac{\sqrt{48\,\left(  \frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{  \frac{2}{3}}+147\,\left(\frac{5\,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-  \frac{293}{8}\right)^{\frac{1}{3}}-412}}{8\,\sqrt{3}\,\left(\frac{5  \,\sqrt{68213}}{2\,6^{\frac{3}{2}}}-\frac{293}{8}\right)^{\frac{1}{6  }}}-\frac{7}{8} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-129.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-129.png)

EMT operasi aljabar dapat membantu untuk menghitung operasi yang
kompleks


No 12


$$\frac{x^3 - 7x^2 + 13x + 3}{x - 2}$$\>$&((x^3-7\*x^2+13\*x+3)/(x-2)), $&solve((x^3-7\*x^2+13\*x+3)/(x-2))


$$\left[ x=\frac{10\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)}{  9\,\left(\frac{\sqrt{43}}{\sqrt{3}}-\frac{107}{27}\right)^{\frac{1}{  3}}}+\left(\frac{\sqrt{43}}{\sqrt{3}}-\frac{107}{27}\right)^{\frac{1  }{3}}\,\left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)+\frac{7}{3}   , x=\left(\frac{\sqrt{43}}{\sqrt{3}}-\frac{107}{27}\right)^{\frac{1  }{3}}\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)+\frac{10\,  \left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)}{9\,\left(\frac{  \sqrt{43}}{\sqrt{3}}-\frac{107}{27}\right)^{\frac{1}{3}}}+\frac{7}{3  } , x=\left(\frac{\sqrt{43}}{\sqrt{3}}-\frac{107}{27}\right)^{\frac{  1}{3}}+\frac{10}{9\,\left(\frac{\sqrt{43}}{\sqrt{3}}-\frac{107}{27}  \right)^{\frac{1}{3}}}+\frac{7}{3} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-132.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-132.png)

EMT operasi aljabar dapat membantu untuk menghitung operasi yang
kompleks


No 13


$$\frac{x^3 - 2x^2 - 8}{x + 2}$$\>$&((x^3-2\*x^2-8)/(x+2)), $&solve((x^3-2\*x^2-8)/(x+2))


$$\left[ x=\frac{4\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)}{9  \,\left(\frac{4\,\sqrt{31}}{3^{\frac{3}{2}}}+\frac{116}{27}\right)^{  \frac{1}{3}}}+\left(\frac{4\,\sqrt{31}}{3^{\frac{3}{2}}}+\frac{116}{  27}\right)^{\frac{1}{3}}\,\left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}  \right)+\frac{2}{3} , x=\left(\frac{4\,\sqrt{31}}{3^{\frac{3}{2}}}+  \frac{116}{27}\right)^{\frac{1}{3}}\,\left(\frac{\sqrt{3}\,i}{2}-  \frac{1}{2}\right)+\frac{4\,\left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}  \right)}{9\,\left(\frac{4\,\sqrt{31}}{3^{\frac{3}{2}}}+\frac{116}{27  }\right)^{\frac{1}{3}}}+\frac{2}{3} , x=\left(\frac{4\,\sqrt{31}}{3  ^{\frac{3}{2}}}+\frac{116}{27}\right)^{\frac{1}{3}}+\frac{4}{9\,  \left(\frac{4\,\sqrt{31}}{3^{\frac{3}{2}}}+\frac{116}{27}\right)^{  \frac{1}{3}}}+\frac{2}{3} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-135.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-135.png)

EMT operasi aljabar dapat membantu untuk menghitung operasi yang
kompleks


No 14


$$\frac{x^3 - 3x + 10}{x - 2}$$\>$&((x^3-3\*x+10)/(x-2)), $&solve((x^3-3\*x+10)/(x-2))


$$\left[ x=\frac{\frac{\sqrt{3}\,i}{2}-\frac{1}{2}}{\left(2\,\sqrt{6}  -5\right)^{\frac{1}{3}}}+\left(2\,\sqrt{6}-5\right)^{\frac{1}{3}}\,  \left(-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right) , x=\left(2\,\sqrt{6  }-5\right)^{\frac{1}{3}}\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}  \right)+\frac{-\frac{\sqrt{3}\,i}{2}-\frac{1}{2}}{\left(2\,\sqrt{6}-  5\right)^{\frac{1}{3}}} , x=\left(2\,\sqrt{6}-5\right)^{\frac{1}{3}}  +\frac{1}{\left(2\,\sqrt{6}-5\right)^{\frac{1}{3}}} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-138.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-138.png)

EMT operasi aljabar dapat membantu untuk menghitung operasi yang
kompleks


No 15


$$\frac{3x^3 - x^2 + 4x - 10}{x + 1}$$\>$&((3\*x^3-x^2+4\*x-10)/(x+1)), $&solve((3\*x^3-x^2+4\*x-10)/(x+1))


$$\left[ x=-\frac{35\,\left(\frac{\sqrt{3}\,i}{2}-\frac{1}{2}\right)  }{81\,\left(\frac{7\,\sqrt{13}}{3^{\frac{5}{2}}}+\frac{1162}{729}  \right)^{\frac{1}{3}}}+\left(\frac{7\,\sqrt{13}}{3^{\frac{5}{2}}}+  \frac{1162}{729}\right)^{\frac{1}{3}}\,\left(-\frac{\sqrt{3}\,i}{2}-  \frac{1}{2}\right)+\frac{1}{9} , x=\left(\frac{7\,\sqrt{13}}{3^{  \frac{5}{2}}}+\frac{1162}{729}\right)^{\frac{1}{3}}\,\left(\frac{  \sqrt{3}\,i}{2}-\frac{1}{2}\right)-\frac{35\,\left(-\frac{\sqrt{3}\,  i}{2}-\frac{1}{2}\right)}{81\,\left(\frac{7\,\sqrt{13}}{3^{\frac{5}{  2}}}+\frac{1162}{729}\right)^{\frac{1}{3}}}+\frac{1}{9} , x=\left(  \frac{7\,\sqrt{13}}{3^{\frac{5}{2}}}+\frac{1162}{729}\right)^{\frac{  1}{3}}-\frac{35}{81\,\left(\frac{7\,\sqrt{13}}{3^{\frac{5}{2}}}+  \frac{1162}{729}\right)^{\frac{1}{3}}}+\frac{1}{9} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-141.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-141.png)

EMT operasi aljabar dapat membantu untuk menghitung operasi yang
kompleks


# Mid-Chapter Mixed Review

Nomor 16-17


Gunakan pembagian sintetis untuk menemukan hasil bagi dan sisanya


No 16


$$\frac{(3x^4-x^3 + 2x^2-6x+6)}{(x-2)}$$\>$&solve((3\*x^4-x^3 + 2\*x^2-6\*x+6)/(x-2))


$$\left[ x=-\frac{\sqrt{-\frac{409}{6\,\sqrt{\frac{324\,\left(\frac{  \sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{2}{3}}-135\,  \left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3  }}+808}{\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{  \frac{1}{3}}}}}-\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}  \right)^{\frac{1}{3}}-\frac{202}{81\,\left(\frac{\sqrt{101279}\,i}{  81}+\frac{197}{729}\right)^{\frac{1}{3}}}-\frac{5}{6}}}{2}-\frac{  \sqrt{\frac{324\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}  \right)^{\frac{2}{3}}-135\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{  197}{729}\right)^{\frac{1}{3}}+808}{\left(\frac{\sqrt{101279}\,i}{81  }+\frac{197}{729}\right)^{\frac{1}{3}}}}}{36}+\frac{1}{12} , x=  \frac{\sqrt{-\frac{409}{6\,\sqrt{\frac{324\,\left(\frac{\sqrt{101279  }\,i}{81}+\frac{197}{729}\right)^{\frac{2}{3}}-135\,\left(\frac{  \sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}+808}{  \left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3  }}}}}-\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{  \frac{1}{3}}-\frac{202}{81\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{  197}{729}\right)^{\frac{1}{3}}}-\frac{5}{6}}}{2}-\frac{\sqrt{\frac{  324\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{  \frac{2}{3}}-135\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}  \right)^{\frac{1}{3}}+808}{\left(\frac{\sqrt{101279}\,i}{81}+\frac{  197}{729}\right)^{\frac{1}{3}}}}}{36}+\frac{1}{12} , x=-\frac{\sqrt{  \frac{409}{6\,\sqrt{\frac{324\,\left(\frac{\sqrt{101279}\,i}{81}+  \frac{197}{729}\right)^{\frac{2}{3}}-135\,\left(\frac{\sqrt{101279}  \,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}+808}{\left(\frac{  \sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}}}}-\left(  \frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}-  \frac{202}{81\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}  \right)^{\frac{1}{3}}}-\frac{5}{6}}}{2}+\frac{\sqrt{\frac{324\,  \left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{2}{3  }}-135\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{  \frac{1}{3}}+808}{\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}  \right)^{\frac{1}{3}}}}}{36}+\frac{1}{12} , x=\frac{\sqrt{\frac{409  }{6\,\sqrt{\frac{324\,\left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{  729}\right)^{\frac{2}{3}}-135\,\left(\frac{\sqrt{101279}\,i}{81}+  \frac{197}{729}\right)^{\frac{1}{3}}+808}{\left(\frac{\sqrt{101279}  \,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}}}}-\left(\frac{\sqrt{  101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}-\frac{202}{81\,  \left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3  }}}-\frac{5}{6}}}{2}+\frac{\sqrt{\frac{324\,\left(\frac{\sqrt{101279  }\,i}{81}+\frac{197}{729}\right)^{\frac{2}{3}}-135\,\left(\frac{  \sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3}}+808}{  \left(\frac{\sqrt{101279}\,i}{81}+\frac{197}{729}\right)^{\frac{1}{3  }}}}}{36}+\frac{1}{12} \right] $$Penyelesaian aljabar dapat kita peroleh nilai variabel


No 17


$$\frac{x^5-5}{x+1}$$\>$&expand((x^5-5)/(x+1)), $&solve((x^5-5)/(x+1))


$$\left[ x=5^{\frac{1}{5}}\,e^{\frac{2\,i\,\pi}{5}} , x=5^{\frac{1}{5  }}\,e^{\frac{4\,i\,\pi}{5}} , x=5^{\frac{1}{5}}\,e^ {- \frac{4\,i\,  \pi}{5} } , x=5^{\frac{1}{5}}\,e^ {- \frac{2\,i\,\pi}{5} } , x=5^{  \frac{1}{5}} \right] $$![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-146.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_Exercise-146.png)

Penyelesaian aljabar dapat kita peroleh nilai variabel


No 18


Gunakan pembagian sintetis untuk menemukan nilai fungsi


$$f(x)=x^3-9x^2+4x-10;$$$$f(-5)$$\>function f(x) :=(x^3-9\*x^2+4\*x-10)

\>f(-5)


    -380

No 19


$$f(x)=20x^2-40x;$$$$f(\frac{1}{2})$$\>function f(x) :=(20\*x^2-40\*x)

\>f(1/2)


    -15

kita dapat menemukan nilai fungsi sesuai yang dicari


No 20


$$f(x) = 5x^4+x^3-x;$$$$f(-\sqrt{2})$$\>fx &= 5\*x^4 + x^3 - x; fx(-sqrt(2))


    18.5857864376

kita dapat menemukan nilai fungsi sesuai yang dicari




# Menggambar Grafik 2D dengan EMT

Buku ini menjelaskan tentang cara menggambar berbagai macam kurva dan
grafik 2D dengan software EMT. EMT menyediakan fungsi plot2d() untuk
menggambar berbagai kurva dan grafik dua dimensi (2D).


## Plot Dasar

Ada beberapa fungsi yang sangat mendasar dari plot. Ada koordinat
layar, yang selalu berkisar antara 0 hingga 1024 di setiap sumbu,
tidak peduli apakah layarnya persegi atau tidak. Terdapat koordinat
plot, yang dapat diatur dengan setplot(). Pemetaan antara koordinat
tergantung pada jendela plot saat ini. Sebagai contoh, default
shrinkwindow() menyisakan ruang untuk label sumbu dan judul plot.


Pada contoh, kita hanya menggambar beberapa garis acak dalam berbagai
warna. Untuk detail mengenai fungsi-fungsi ini, pelajari fungsi-fungsi
inti dari EMT.


\>clg; // clear screen

\>window(0,0,1024,1024); // use all of the window

\>setplot(0,1,0,1); // set plot coordinates

\>hold on; // start overwrite mode

\>n=100; X=random(n,2); Y=random(n,2);  // get random points

\>colors=rgb(random(n),random(n),random(n)); // get random colors

\>loop 1 to n; color(colors[#]); plot(X[#],Y[#]); end; // plot

\>hold off; // end overwrite mode

\>insimg; // insert to notebook


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-001.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-001.png)

\>reset;


Anda harus menahan grafik, karena perintah plot() akan menghapus
jendela plot.


Untuk menghapus semua yang telah kita lakukan, kita gunakan reset().


Untuk menampilkan gambar hasil plot di layar notebook, perintah
plot2d() dapat diakhiri dengan titik dua (:). Cara lain adalah
perintah plot2d() diakhiri dengan titik koma (;), kemudian gunakan
perintah insimg() untuk menampilkan gambar hasil plot.


Sebagai contoh lain, kita menggambar sebuah plot sebagai inset pada
plot yang lain. Hal ini dilakukan dengan mendefinisikan jendela plot
yang lebih kecil. Perhatikan bahwa jendela ini tidak menyediakan ruang
untuk label sumbu di luar jendela plot. Kita harus menambahkan
beberapa margin untuk hal ini sesuai kebutuhan. Perhatikan bahwa kita
menyimpan dan mengembalikan jendela penuh, dan menahan plot saat ini
ketika kita membuat inset.


\>plot2d("x^3-x");

\>xw=200; yw=100; ww=300; hw=300;

\>ow=window();

\>window(xw,yw,xw+ww,yw+hw);

\>hold on;

\>barclear(xw-50,yw-10,ww+60,ww+60);

\>plot2d("x^4-x",grid=6):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-002.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-002.png)

\>hold off;

\>window(ow);


Plot dengan beberapa angka dicapai dengan cara yang sama. Ada fungsi
utility figure() untuk ini.


## Aspek Plot

Plot default menggunakan jendela plot persegi. Anda dapat mengubahnya
dengan fungsi aspect(). Jangan lupa untuk mengatur ulang aspeknya
nanti. Anda juga dapat mengubah default ini di menu dengan “Set
Aspect” ke rasio aspek tertentu atau ke ukuran jendela grafik saat
ini.


Tetapi Anda juga dapat mengubahnya untuk satu plot. Untuk ini, ukuran
area plot saat ini diubah, dan jendela diatur sedemikian rupa sehingga
label memiliki ruang yang cukup.


\>aspect(2); // rasio panjang dan lebar 2:1

\>plot2d(["sin(x)","cos(x)"],0,2pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-003.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-003.png)

\>aspect();

\>reset;


Fungsi reset () mengembalikan default plot, termasuk rasio aspek.


# Plot 2D di Euler

EMT Math Toolbox memiliki plot dalam bentuk 2D, baik untuk data maupun
fungsi. EMT menggunakan fungsi plot2d. Fungsi ini dapat memplot fungsi
dan data.


Dimungkinkan untuk memplot di Maxima menggunakan Gnuplot atau di
Python menggunakan Math Plot Lib.


Euler dapat memplot plot 2D dari


* 
ekspresi

* 
fungsi, variabel, atau kurva berparameter,

* 
vektor nilai x-y,

* 
awan titik-titik di bidang,

* 
kurva implisit dengan level atau wilayah level.

* 
Fungsi yang kompleks


Gaya plot mencakup berbagai gaya untuk garis dan titik, plot batang,
dan plot berbayang.


# Plot Ekspresi atau Variabel

Ekspresi tunggal dalam “x” (misalnya “4*x^2”) atau nama fungsi
(misalnya “f”) menghasilkan grafik fungsi.


Berikut ini adalah contoh paling dasar, yang menggunakan rentang
default dan menetapkan rentang y yang tepat agar sesuai dengan plot
fungsi.


Catatan: Jika Anda mengakhiri baris perintah dengan tanda titik dua
“:”, plot akan disisipkan ke dalam jendela teks. Jika tidak, tekan TAB
untuk melihat plot jika jendela plot tertutup.


\>plot2d("x^2"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-004.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-004.png)

\>aspect(1.5); plot2d("x^3-x"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-005.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-005.png)

\>a:=5.6; plot2d("exp(-a\*x^2)/a"); insimg(30); // menampilkan gambar hasil plot setinggi 25 baris


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-006.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-006.png)

Dari beberapa contoh sebelumnya Anda dapat melihat bahwa aslinya
gambar plot menggunakan sumbu X dengan rentang nilai dari -2 sampai
dengan 2. Untuk mengubah rentang nilai X dan Y, Anda dapat menambahkan
nilai-nilai batas X (dan Y) di belakang ekspresi yang digambar.


The plot range is set with the following assigned parameters


* 
a,b: x-range (default -2,2)

* 
c,d: y-range (default: scale with values)

* 
r: alternative radius lingakaran di tengah plor

* 
cx,cy:koordinat plot di tengah (default 0,0)


\>plot2d("x^3-x",-1,2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-007.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-007.png)

\>plot2d("sin(x)",-2\*pi,2\*pi): // plot sin(x) pada interval [-2pi, 2pi]


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-008.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-008.png)

\>plot2d("cos(x)","sin(3\*x)",xmin=0,xmax=2pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-009.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-009.png)

Alternatif untuk tanda titik dua adalah perintah insimg(lines), yang
menyisipkan plot yang menempati sejumlah baris teks tertentu.


Dalam opsi, plot dapat diatur untuk muncul


* 
di jendela terpisah yang dapat diubah ukurannya,

* 
di jendela buku catatan.


Lebih banyak gaya yang dapat dicapai dengan perintah plot tertentu.


Dalam hal apa pun, tekan tombol tabulator untuk melihat plot, jika
disembunyikan.


Untuk membagi jendela menjadi beberapa plot, gunakan perintah
figure(). Pada contoh, kita memplot x^1 sampai x^4 ke dalam 4 bagian
jendela. figure(0) akan mereset jendela default.


\>reset;

\>figure(2,2); ...  
\>   for n=1 to 4; figure(n); plot2d("x^"+n); end; ...  
\>   figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-010.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-010.png)

Pada plot2d(), terdapat beberapa gaya alternatif yang tersedia dengan
grid=x. Sebagai gambaran umum, kami menampilkan berbagai gaya grid
dalam satu gambar (lihat di bawah ini untuk perintah figure()). Gaya
grid=0 tidak disertakan. Gaya ini tidak menampilkan grid dan frame.


\>figure(3,3); ...  
\>   for k=1:9; figure(k); plot2d("x^3-x",-2,1,grid=k); end; ...  
\>   figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-011.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-011.png)

Jika argumen untuk plot2d() adalah sebuah ekspresi yang diikuti oleh
empat angka, angka-angka ini adalah rentang x dan y untuk plot.


Atau, a, b, c, d dapat ditentukan sebagai parameter yang ditetapkan
sebagai a=... dst.


Pada contoh berikut, kita mengubah gaya grid, menambahkan label, dan
menggunakan label vertikal untuk sumbu y.


\>aspect(1.5); plot2d("sin(x)",0,2pi,-1.2,1.2,grid=3,xl="x",yl="sin(x)"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-012.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-012.png)

\>plot2d("sin(x)+cos(2\*x)",0,4pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-013.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-013.png)

Gambar yang dihasilkan dengan menyisipkan plot ke dalam jendela teks
disimpan dalam direktori yang sama dengan notebook, secara default
dalam subdirektori bernama “images”. Gambar-gambar tersebut juga
digunakan oleh ekspor HTML.


Anda cukup menandai gambar mana saja dan menyalinnya ke clipboard
dengan Ctrl-C. Tentu saja, Anda juga dapat mengekspor grafik saat ini
dengan fungsi-fungsi pada menu File.


Fungsi atau ekspresi dalam plot2d dievaluasi secara adaptif. Untuk
kecepatan yang lebih tinggi, matikan plot adaptif dengan &lt;adaptive dan
tentukan jumlah subinterval dengan n=... Hal ini hanya diperlukan pada
kasus-kasus yang jarang terjadi.


\>plot2d("sign(x)\*exp(-x^2)",-1,1,<adaptive,n=10000):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-014.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-014.png)

\>plot2d("x^x",r=1.2,cx=1,cy=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-015.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-015.png)

Perhatikan bahwa x^x tidak didefinisikan untuk x&lt;=0. Fungsi plot2d
menangkap kesalahan ini, dan mulai memplot segera setelah fungsi
didefinisikan. Hal ini berlaku untuk semua fungsi yang mengembalikan
NAN di luar jangkauan definisinya.


\>plot2d("log(x)",-0.1,2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-016.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-016.png)

Parameter square=true (atau &gt;square) memilih rentang y secara otomatis
sehingga hasilnya adalah jendela plot persegi. Perhatikan bahwa secara
default, Euler menggunakan ruang persegi di dalam jendela plot.


\>plot2d("x^3-x",\>square):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-017.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-017.png)

\>plot2d(''integrate("sin(x)\*exp(-x^2)",0,x)'',0,2): // plot integral


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-018.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-018.png)

Jika Anda membutuhkan lebih banyak ruang untuk label-y, panggil
shrinkwindow() dengan parameter lebih kecil, atau tetapkan nilai
positif untuk “lebih kecil” pada plot2d().


\>plot2d("gamma(x)",1,10,yl="y-values",smaller=6,<vertical):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-019.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-019.png)

Ekspresi simbolik juga dapat digunakan, karena disimpan sebagai
ekspresi string sederhana.


\>x=linspace(0,2pi,1000); plot2d(sin(5x),cos(7x)):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-020.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-020.png)

\>a:=5.6; expr &= exp(-a\*x^2)/a; // define expression

\>plot2d(expr,-2,2): // plot from -2 to 2


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-021.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-021.png)

\>plot2d(expr,r=1,thickness=2): // plot in a square around (0,0)


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-022.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-022.png)

\>plot2d(&diff(expr,x),\>add,style="--",color=red): // add another plot


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-023.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-023.png)

\>plot2d(&diff(expr,x,2),a=-2,b=2,c=-2,d=1): // plot in rectangle


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-024.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-024.png)

\>plot2d(&diff(expr,x),a=-2,b=2,\>square): // keep plot square


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-025.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-025.png)

\>plot2d("x^2",0,1,steps=1,color=red,n=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-026.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-026.png)

\>plot2d("x^2",\>add,steps=2,color=blue,n=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-027.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-027.png)

# Fungsi dalam satu Parameter

Fungsi plot yang paling penting untuk plot planar adalah plot2d().
Fungsi ini diimplementasikan dalam bahasa Euler dalam file “plot.e”,
yang dimuat pada awal program.


Berikut adalah beberapa contoh penggunaan fungsi. Seperti biasa dalam
EMT, fungsi yang bekerja untuk fungsi atau ekspresi lain, Anda dapat
mengoper parameter tambahan (selain x) yang bukan variabel global ke
fungsi dengan parameter titik koma atau dengan koleksi panggilan.


\>function f(x,a) := x^2/a+a\*x^2-x; // define a function

\>a=0.3; plot2d("f",0,1;a): // plot with a=0.3


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-028.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-028.png)

\>plot2d("f",0,1;0.4): // plot with a=0.4


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-029.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-029.png)

\>plot2d({{"f",0.2}},0,1): // plot with a=0.2


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-030.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-030.png)

\>plot2d({{"f(x,b)",b=0.1}},0,1): // plot with 0.1


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-031.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-031.png)

\>function f(x) := x^3-x; ...  
\>   plot2d("f",r=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-032.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-032.png)

Berikut ini adalah ringkasan dari fungsi yang diterima


* 
ekspresi atau ekspresi simbolik dalam x

* 
fungsi atau fungsi simbolik dengan nama sebagai “f”

* 
fungsi-fungsi simbolik hanya dengan nama f


Fungsi plot2d() juga menerima fungsi simbolik. Untuk fungsi simbolik,
nama saja sudah cukup.


\>function f(x) &= diff(x^x,x)


    
                                x
                               x  (log(x) + 1)
    

\>plot2d(f,0,2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-033.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-033.png)

Tentu saja, untuk ekspresi atau ungkapan simbolik, nama variabel sudah
cukup untuk memplotnya.


\>expr &= sin(x)\*exp(-x)


    
                                  - x
                                 E    sin(x)
    

\>plot2d(expr,0,3pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-034.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-034.png)

\>function f(x) &= x^x;

\>plot2d(f,r=1,cx=1,cy=1,color=blue,thickness=2);

\>plot2d(&diff(f(x),x),\>add,color=red,style="-.-"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-035.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-035.png)

Untuk gaya garis, ada berbagai pilihan.


* 
style = “...”. Pilih dari “-”, “--”, “-.”, “.”, “.-.”, “-.-”.

* 
color: Lihat di bawah untuk warna.

* 
ketebalan: Default adalah 1.


Warna dapat dipilih sebagai salah satu warna default, atau sebagai
warna RGB.


* 
0..15: indeks warna default.

* 
konstanta warna: putih, hitam, merah, hijau, biru, cyan, zaitun,
* abu-abu muda, abu-abu, abu-abu tua, oranye, hijau muda, pirus, biru
* muda, oranye muda, kuning

* 
rgb (merah, hijau, biru): parameter adalah real dalam [0,1].


\>plot2d("exp(-x^2)",r=2,color=red,thickness=3,style="--"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-036.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-036.png)

Berikut ini adalah pemandangan warna EMT yang sudah ditetapkan
sebelumnya.


\>aspect(2); columnsplot(ones(1,16),lab=0:15,grid=0,color=0:15):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-037.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-037.png)

Tapi kamu bisa menggunakan warna lain.


\>columnsplot(ones(1,16),grid=0,color=rgb(0,0,linspace(0,1,15))):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-038.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-038.png)

# Menggambar beberapa kurva pada bidang koordinat yang sama

Memplot lebih dari satu fungsi (beberapa fungsi) ke dalam satu jendela
dapat dilakukan dengan berbagai cara. Salah satu caranya adalah dengan
menggunakan &gt;add untuk beberapa pemanggilan ke plot2d secara
bersamaan, kecuali pemanggilan pertama. Kita telah menggunakan fitur
ini pada contoh di atas.


\>aspect(); plot2d("cos(x)",r=2,grid=6); plot2d("x",style=".",\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-039.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-039.png)

\>aspect(1.5); plot2d("sin(x)",0,2pi); plot2d("cos(x)",color=blue,style="--",\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-040.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-040.png)

Salah satu kegunaan &gt;add adalah untuk menambahkan titik pada kurva.


\>plot2d("sin(x)",0,pi); plot2d(2,sin(2),\>points,\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-041.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-041.png)

Kami menambahkan titik perpotongan dengan label (pada posisi “cl”
untuk kiri tengah), dan menyisipkan hasilnya ke dalam buku catatan.
Kami juga menambahkan judul ke plot.


\>plot2d(["cos(x)","x"],r=1.1,cx=0.5,cy=0.5, ...  
\>     color=[black,blue],style=["-","."], ...  
\>     grid=1);

\>x0=solve("cos(x)-x",1);  ...  
\>     plot2d(x0,x0,\>points,\>add,title="Intersection Demo");  ...  
\>     label("cos(x) = x",x0,x0,pos="cl",offset=20):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-042.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-042.png)

Dalam demo berikut ini, kami memplot fungsi sinc(x)=sin(x)/x dan
ekspansi Taylor ke-8 dan ke-16. Kami menghitung ekspansi ini
menggunakan Maxima melalui ekspresi simbolik.


Plot ini dilakukan dalam perintah multi-baris berikut dengan tiga
pemanggilan plot2d(). Perintah kedua dan ketiga memiliki set flag
&gt;add, yang membuat plot menggunakan rentang sebelumnya.


Kami menambahkan sebuah kotak label yang menjelaskan fungsi-fungsi
tersebut.


\>$taylor(sin(x)/x,x,0,4)


$$\frac{x^4}{120}-\frac{x^2}{6}+1$$\>plot2d("sinc(x)",0,4pi,color=green,thickness=2); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,8),\>add,color=blue,style="--"); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,16),\>add,color=red,style="-.-"); ...  
\>     labelbox(["sinc","T8","T16"],styles=["-","--","-.-"], ...  
\>       colors=[black,blue,red]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-044.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-044.png)

Pada contoh berikut, kami menghasilkan Polinomial Bernstein.


$$B_i(x) = \binom{n}{i} x^i (1-x)^{n-i}$$\>plot2d("(1-x)^10",0,1); // plot first function

\>for i=1 to 10; plot2d("bin(10,i)\*x^i\*(1-x)^(10-i)",\>add); end;

\>insimg;


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-046.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-046.png)

Metode kedua menggunakan sepasang matriks nilai x dan matriks nilai y
dengan ukuran yang sama.


Kita membuat sebuah matriks nilai dengan satu Polinomial Bernstein di
setiap baris. Untuk ini, kita cukup menggunakan vektor kolom i.
Lihatlah pengantar tentang bahasa matriks untuk mempelajari lebih
lanjut.


\>x=linspace(0,1,500);

\>n=10; k=(0:n)'; // n is row vector, k is column vector

\>y=bin(n,k)\*x^k\*(1-x)^(n-k); // y is a matrix then

\>plot2d(x,y):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-047.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-047.png)

Perhatikan bahwa parameter warna dapat berupa vektor. Kemudian setiap
warna digunakan untuk setiap baris matriks.


\>x=linspace(0,1,200); y=x^(1:10)'; plot2d(x,y,color=1:10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-048.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-048.png)

Metode lain adalah menggunakan vektor ekspresi (string). Anda kemudian
dapat menggunakan larik warna, larik gaya, dan larik ketebalan dengan
panjang yang sama.


\>plot2d(["sin(x)","cos(x)"],0,2pi,color=4:5): 


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-049.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-049.png)

\>plot2d(["sin(x)","cos(x)"],0,2pi): // plot vector of expressions


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-050.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-050.png)

Kita bisa mendapatkan vektor seperti itu dari Maxima dengan
menggunakan makelist() dan mxm2str().


\>v &= makelist(binomial(10,i)\*x^i\*(1-x)^(10-i),i,0,10) // make list


    
                   10            9              8  2             7  3
           [(1 - x)  , 10 (1 - x)  x, 45 (1 - x)  x , 120 (1 - x)  x , 
               6  4             5  5             4  6             3  7
    210 (1 - x)  x , 252 (1 - x)  x , 210 (1 - x)  x , 120 (1 - x)  x , 
              2  8              9   10
    45 (1 - x)  x , 10 (1 - x) x , x  ]
    

\>mxm2str(v) // get a vector of strings from the symbolic vector


    (1-x)^10
    10*(1-x)^9*x
    45*(1-x)^8*x^2
    120*(1-x)^7*x^3
    210*(1-x)^6*x^4
    252*(1-x)^5*x^5
    210*(1-x)^4*x^6
    120*(1-x)^3*x^7
    45*(1-x)^2*x^8
    10*(1-x)*x^9
    x^10

\>plot2d(mxm2str(v),0,1): // plot functions


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-051.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-051.png)

Alternatif lain adalah dengan menggunakan bahasa matriks Euler.


Jika sebuah ekspresi menghasilkan sebuah matriks fungsi, dengan satu
fungsi di setiap baris, semua fungsi ini akan diplot ke dalam satu
plot.


Untuk ini, gunakan vektor parameter dalam bentuk vektor kolom. Jika
sebuah larik warna ditambahkan, maka akan digunakan untuk setiap baris
plot.


\>n=(1:10)'; plot2d("x^n",0,1,color=1:10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-052.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-052.png)

Ekspresi dan fungsi satu baris dapat melihat variabel global.


Jika Anda tidak dapat menggunakan variabel global, Anda perlu
menggunakan fungsi dengan parameter tambahan, dan memberikan parameter
ini sebagai parameter titik koma.


Berhati-hatilah untuk meletakkan semua parameter yang diberikan di
akhir perintah plot2d. Pada contoh ini kita mengoper a=5 ke fungsi f,
yang kita plot dari -10 ke 10.


\>function f(x,a) := 1/a\*exp(-x^2/a); ...  
\>   plot2d("f",-10,10;5,thickness=2,title="a=5"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-053.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-053.png)

Atau, gunakan koleksi dengan nama fungsi dan semua parameter tambahan.
Daftar khusus ini disebut koleksi panggilan, dan itu adalah cara yang
lebih disukai untuk mengoper argumen ke fungsi yang dengan sendirinya
dioper sebagai argumen ke fungsi lain.


Pada contoh berikut, kita menggunakan perulangan untuk memplot
beberapa fungsi (lihat tutorial tentang pemrograman perulangan).


\>plot2d({{"f",1}},-10,10); ...  
\>   for a=2:10; plot2d({{"f",a}},\>add); end:


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-054.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-054.png)

Kita dapat mencapai hasil yang sama dengan cara berikut menggunakan
bahasa matriks EMT. Setiap baris dari matriks f(x,a) adalah satu
fungsi. Selain itu, kita dapat mengatur warna untuk setiap baris
matriks. Klik dua kali pada fungsi getspectral() untuk penjelasannya.


\>x=-10:0.01:10; a=(1:10)'; plot2d(x,f(x,a),color=getspectral(a/10)):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-055.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-055.png)

## Label Teks

Dekorasi sederhana dapat berupa


* 
sebuah judul dengan title=”...”

* 
label x dan y dengan xl=“...”, yl=”...”

* 
label teks lain dengan label(“...”,x,y)


Perintah label akan memplotkan ke dalam plot saat ini pada koordinat
plot (x,y). Perintah ini dapat menerima sebuah argumen posisi.


\>plot2d("x^3-x",-1,2,title="y=x^3-x",yl="y",xl="x"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-056.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-056.png)

\>expr := "log(x)/x"; ...  
\>     plot2d(expr,0.5,5,title="y="+expr,xl="x",yl="y"); ...  
\>     label("(1,0)",1,0); label("Max",E,expr(E),pos="lc"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-057.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-057.png)

Ada juga fungsi labelbox(), yang dapat menampilkan fungsi dan teks.
Fungsi ini membutuhkan vektor string dan warna, satu item untuk setiap
fungsi.


\>function f(x) &= x^2\*exp(-x^2);  ...  
\>   plot2d(&f(x),a=-3,b=3,c=-1,d=1);  ...  
\>   plot2d(&diff(f(x),x),\>add,color=blue,style="--"); ...  
\>   labelbox(["function","derivative"],styles=["-","--"], ...  
\>      colors=[black,blue],w=0.4):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-058.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-058.png)

Kotak tersebut berlabuh di kanan atas secara default, tetapi &gt;kiri
menambatkannya di kiri atas. Anda dapat memindahkannya ke tempat mana
pun yang Anda suka. Posisi jangkar adalah sudut kanan atas kotak, dan
angkanya adalah pecahan dari ukuran jendela grafik. Lebarnya otomatis.


Untuk plot titik, kotak label juga dapat digunakan. Tambahkan
parameter &gt;titik, atau vektor bendera, satu untuk setiap label.


Pada contoh berikut, hanya ada satu fungsi. Jadi kita dapat
menggunakan string sebagai pengganti vektor string. Kita mengatur
warna teks menjadi hitam untuk contoh ini.


\>n=10; plot2d(0:n,bin(n,0:n),\>addpoints); ...  
\>   labelbox("Binomials",styles="[]",\>points,x=0.1,y=0.1, ...  
\>   tcolor=black,\>left):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-059.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-059.png)

Gaya plot ini juga tersedia di statplot(). Seperti pada plot2d() warna
dapat diatur untuk setiap baris plot. Terdapat lebih banyak plot
khusus untuk keperluan statistik (lihat tutorial tentang statistik).


\>statplot(1:10,random(2,10),color=[red,blue]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-060.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-060.png)

Fitur yang serupa adalah fungsi textbox().


Lebarnya secara default adalah lebar maksimal baris teks. Tetapi bisa
juga diatur oleh pengguna.


\>function f(x) &= exp(-x)\*sin(2\*pi\*x); ...  
\>   plot2d("f(x)",0,2pi); ...  
\>   textbox(latex("\\text{Example of a damped oscillation}\\ f(x)=e^{-x}sin(2\\pi x)"),w=0.85):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-061.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-061.png)

Label teks, judul, kotak label, dan teks lainnya dapat berisi string
Unicode (lihat sintaks EMT untuk mengetahui lebih lanjut tentang
string Unicode).


\>plot2d("x^3-x",title=u"x &rarr; x&sup3; - x"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-062.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-062.png)

Label pada sumbu x dan y bisa vertikal, begitu juga dengan sumbu.


\>plot2d("sinc(x)",0,2pi,xl="x",yl=u"x &rarr; sinc(x)",\>vertical):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-063.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-063.png)

## LaTeX

Anda juga dapat memplot formula LaTeX jika Anda telah menginstal
sistem LaTeX. Saya merekomendasikan MiKTeX. Jalur ke binari “lateks”
dan “dvipng” harus berada di jalur sistem, atau Anda harus mengatur
LaTeX di menu opsi.


Perhatikan, bahwa penguraian LaTeX berjalan lambat. Jika Anda ingin
menggunakan LaTeX dalam plot animasi, Anda harus memanggil latex()
sebelum perulangan satu kali dan menggunakan hasilnya (gambar dalam
matriks RGB).


Pada plot berikut ini, kita menggunakan LaTeX untuk label x dan y,
sebuah label, kotak label dan judul plot.


\>plot2d("exp(-x)\*sin(x)/x",a=0,b=2pi,c=0,d=1,grid=6,color=blue, ...  
\>     title=latex("\\text{Function $\\Phi$}"), ...  
\>     xl=latex("\\phi"),yl=latex("\\Phi(\\phi)")); ...  
\>   textbox( ...  
\>     latex("\\Phi(\\phi) = e^{-\\phi} \\frac{\\sin(\\phi)}{\\phi}"),x=0.8,y=0.5); ...  
\>   label(latex("\\Phi",color=blue),1,0.4):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-064.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-064.png)

Seringkali, kita menginginkan spasi dan label teks yang tidak sesuai
pada sumbu x. Kita dapat menggunakan xaxis() dan yaxis() seperti yang
akan kita tunjukkan nanti.


Cara termudah adalah dengan membuat plot kosong dengan sebuah frame
menggunakan grid=4, dan kemudian menambahkan grid dengan ygrid() dan
xgrid(). Pada contoh berikut, kita menggunakan tiga buah string LaTeX
untuk label pada sumbu x dengan xtick().


\>plot2d("sinc(x)",0,2pi,grid=4,<ticks); ...  
\>   ygrid(-2:0.5:2,grid=6); ...  
\>   xgrid([0:2]\*pi,<ticks,grid=6);  ...  
\>   xtick([0,pi,2pi],["0","\\pi","2\\pi"],\>latex):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-065.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-065.png)

Tentu, fungsi tersebut bisa digunakan


\>function map f(x) ...


    if x>0 then return x^4
    else return x^2
    endif
    endfunction
</pre>
Parameter “map” membantu menggunakan fungsi untuk vektor. Untuk


plot, hal ini tidak diperlukan. Tetapi untuk mendemonstrasikan bahwa
vektorisasi


berguna, kami menambahkan beberapa titik kunci pada plot pada x=-1,
x=0 dan x=1.


Pada plot berikut, kita juga memasukkan beberapa kode LaTeX. Kita
menggunakannya untuk


dua label dan sebuah kotak teks. Tentu saja, Anda hanya dapat
menggunakan


LaTeX jika Anda telah menginstal LaTeX dengan benar.


\>plot2d("f",-1,1,xl="x",yl="f(x)",grid=6);  ...  
\>   plot2d([-1,0,1],f([-1,0,1]),\>points,\>add); ...  
\>   label(latex("x^3"),0.72,f(0.72)); ...  
\>   label(latex("x^2"),-0.52,f(-0.52),pos="ll"); ...  
\>   textbox( ...  
\>     latex("f(x)=\\begin{cases} x^3 & x\>0 \\\\ x^2 & x \\le 0\\end{cases}"), ...  
\>     x=0.7,y=0.2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-066.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-066.png)

## Interaksi Pengguna

Ketika memplot fungsi atau ekspresi, parameter &gt;user memungkinkan
pengguna untuk memperbesar dan menggeser plot dengan tombol kursor
atau mouse. Pengguna dapat


* 
memperbesar dengan + atau -

* 
memindahkan plot dengan tombol kursor

* 
memilih jendela plot dengan mouse

* 
mengatur ulang tampilan dengan spasi

* 
keluar dengan return


Tombol spasi akan mengatur ulang plot ke jendela plot awal.


Ketika memplot data, bendera &gt;user hanya akan menunggu penekanan
tombol.


\>plot2d({{"x^3-a\*x",a=1}},\>user,title="Press any key!"):


    Interrupt with Escape key!
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        k1=_mouse("Press return, cursor key, +/-, space, click with m ...

\>plot2d("exp(x)\*sin(x)",user=true, ...  
\>     title="+/- or cursor keys (return to exit)"):


    Interrupt with Escape key!
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        k1=_mouse("Press return, cursor key, +/-, space, click with m ...

Berikut ini menunjukkan cara interaksi pengguna tingkat lanjut (lihat
tutorial tentang pemrograman untuk detailnya).


Fungsi bawaan mousedrag() menunggu peristiwa mouse atau keyboard.
Fungsi ini melaporkan mouse ke bawah, mouse bergerak atau mouse ke
atas, dan penekanan tombol. Fungsi dragpoints() memanfaatkan hal ini,
dan mengizinkan pengguna untuk menyeret titik manapun di dalam plot.


Kita membutuhkan fungsi plot terlebih dahulu. Sebagai contoh, kita
melakukan interpolasi pada 5 titik dengan sebuah polinomial. Fungsi
ini harus memplot ke dalam area plot yang tetap.


\>function plotf(xp,yp,select) ...


      d=interp(xp,yp);
      plot2d("interpval(xp,d,x)";d,xp,r=2);
      plot2d(xp,yp,>points,>add);
      if select>0 then
        plot2d(xp[select],yp[select],color=red,>points,>add);
      endif;
      title("Drag one point, or press space or return!");
    endfunction
</pre>
Perhatikan parameter titik koma pada plot2d (d dan xp), yang
diteruskan ke evaluasi fungsi interp(). Tanpa ini, kita harus menulis
fungsi plotinterp() terlebih dahulu, untuk mengakses nilai secara
global.


Sekarang kita menghasilkan beberapa nilai acak, dan membiarkan
pengguna menyeret titik-titiknya.


\>t=-1:0.5:1; dragpoints("plotf",t,random(size(t))-0.5):


    Interrupt with Escape key!
    Try "trace errors" to inspect local variables after errors.
    dragpoints:
        {flag,m,t}=mousedrag(status);

Ada juga fungsi yang memplot fungsi lain tergantung pada vektor
parameter, dan memungkinkan pengguna menyesuaikan parameter ini.


Pertama, kita memerlukan fungsi plot.


\>function plotf([a,b]) := plot2d("exp(a\*x)\*cos(2pi\*b\*x)",0,2pi;a,b);


Kemudian kita membutuhkan nama untuk parameter, nilai awal dan matriks
rentang nx2, dan secara opsional, sebuah garis judul.


Terdapat slider interaktif, yang dapat mengatur nilai oleh pengguna.
Fungsi dragvalues() menyediakan ini.


\>dragvalues("plotf",["a","b"],[-1,2],[[-2,2];[1,10]], ...  
\>     heading="Drag these values:",hcolor=black):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-067.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-067.png)

Anda dapat membatasi nilai yang diseret menjadi bilangan bulat.
Sebagai contoh, kita menulis fungsi plot, yang memplot polinomial
Taylor dengan derajat n ke fungsi kosinus.


\>function plotf(n) ...


    plot2d("cos(x)",0,2pi,>square,grid=6);
    plot2d(&"taylor(cos(x),x,0,@n)",color=blue,>add);
    textbox("Taylor polynomial of degree "+n,0.1,0.02,style="t",>left);
    endfunction
</pre>
Sekarang kita membiarkan derajat n bervariasi dari 0 sampai 20 dalam
20 stop. Hasil dari dragvalues() digunakan untuk memplot sketsa dengan
n ini, dan untuk menyisipkan plot ke dalam buku catatan.


\>nd=dragvalues("plotf","degree",2,[0,20],20,y=0.8, ...  
\>      heading="Drag the value:"); ...  
\>   plotf(nd):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-068.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-068.png)

Berikut ini adalah peragaan sederhana dari fungsi ini. Pengguna dapat
menggambar di atas jendela plot, meninggalkan jejak titik.


\>function dragtest ...


      plot2d(none,r=1,title="Drag with the mouse, or press any key!");
      start=0;
      repeat
        {flag,m,time}=mousedrag();
        if flag==0 then return; endif;
        if flag==2 then
          hold on; mark(m[1],m[2]); hold off;
        endif;
      end
    endfunction
</pre>
\>dragtest // lihat hasilnya dan cobalah lakukan!


## Gaya Plot 2D

Secara default, EMT menghitung tanda sumbu otomatis dan menambahkan
label pada setiap tanda. Hal ini dapat diubah dengan parameter grid.
Gaya default sumbu dan label dapat dimodifikasi. Selain itu, label dan
judul dapat ditambahkan secara manual. Untuk mengatur ulang ke gaya
default, gunakan reset().


\>aspect();

\>figure(3,4); ...  
\>    figure(1); plot2d("x^3-x",grid=0); ... // no grid, frame or axis

\> figure(2); plot2d("x^3-x",grid=1); ... // x-y-axis

\> figure(3); plot2d("x^3-x",grid=2); ... // default ticks

\> figure(4); plot2d("x^3-x",grid=3); ... // x-y- axis with labels inside

\> figure(5); plot2d("x^3-x",grid=4); ... // no ticks, only labels

\> figure(6); plot2d("x^3-x",grid=5); ... // default, but no margin

\> figure(7); plot2d("x^3-x",grid=6); ... // axes only

\> figure(8); plot2d("x^3-x",grid=7); ... // axes only, ticks at axis

\> figure(9); plot2d("x^3-x",grid=8); ... // axes only, finer ticks at axis

\> figure(10); plot2d("x^3-x",grid=9); ... // default, small ticks inside

\> figure(11); plot2d("x^3-x",grid=10); ...// no ticks, axes only

\> figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-069.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-069.png)

Parameter &lt;frame mematikan bingkai, dan framecolor=blue menetapkan
bingkai ke warna biru.


Jika Anda menginginkan tanda centang Anda sendiri, Anda dapat
menggunakan style=0, dan menambahkan semuanya nanti.


\>aspect(1.5); 

\>plot2d("x^3-x",grid=0); // plot

\>frame; xgrid([-1,0,1]); ygrid(0): // add frame and grid


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-070.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-070.png)

Untuk judul plot dan label sumbu, lihat contoh berikut.


\>plot2d("exp(x)",-1,1);

\>textcolor(black); // set the text color to black

\>title(latex("y=e^x")); // title above the plot

\>xlabel(latex("x")); // "x" for x-axis

\>ylabel(latex("y"),\>vertical); // vertical "y" for y-axis

\>label(latex("(0,1)"),0,1,color=blue): // label a point


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-071.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-071.png)

Sumbu dapat digambar secara terpisah dengan sumbu x() dan sumbu y().


\>plot2d("x^3-x",<grid,<frame);

\>xaxis(0,xx=-2:1,style="-\>"); yaxis(0,yy=-5:5,style="-\>"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-072.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-072.png)

Teks pada plot dapat diatur dengan label(). Pada contoh berikut ini,
“lc” berarti lower center. Ini mengatur posisi label relatif terhadap
koordinat plot.


\>function f(x) &= x^3-x


    
                                     3
                                    x  - x
    

\>plot2d(f,-1,1,\>square);

\>x0=fmin(f,0,1); // compute point of minimum

\>label("Rel. Min.",x0,f(x0),pos="lc"): // add a label there


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-073.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-073.png)

Disana juga termasuk kotak teks.


\>plot2d(&f(x),-1,1,-2,2); // function

\>plot2d(&diff(f(x),x),\>add,style="--",color=red); // derivative

\>labelbox(["f","f'"],["-","--"],[black,red]): // label box


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-074.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-074.png)

\>plot2d(["exp(x)","1+x"],color=[black,blue],style=["-","-.-"]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-075.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-075.png)

\>gridstyle("-\>",color=gray,textcolor=gray,framecolor=gray);  ...  
\>    plot2d("x^3-x",grid=1);   ...  
\>    settitle("y=x^3-x",color=black); ...  
\>    label("x",2,0,pos="bc",color=gray);  ...  
\>    label("y",0,6,pos="cl",color=gray); ...  
\>    reset():


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-076.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-076.png)

Untuk kontrol yang lebih besar lagi, sumbu x dan sumbu y dapat
dilakukan secara manual.


Perintah fullwindow() akan memperluas jendela plot karena kita tidak
lagi membutuhkan tempat untuk label di luar jendela plot. Gunakan
shrinkwindow() atau reset() untuk mengatur ulang ke default.


\>fullwindow; ...  
\>    gridstyle(color=darkgray,textcolor=darkgray); ...  
\>    plot2d(["2^x","1","2^(-x)"],a=-2,b=2,c=0,d=4,<grid,color=4:6,<frame); ...  
\>    xaxis(0,-2:1,style="-\>"); xaxis(0,2,"x",<axis); ...  
\>    yaxis(0,4,"y",style="-\>"); ...  
\>    yaxis(-2,1:4,\>left); ...  
\>    yaxis(2,2^(-2:2),style=".",<left); ...  
\>    labelbox(["2^x","1","2^-x"],colors=4:6,x=0.8,y=0.2); ...  
\>    reset:


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-077.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-077.png)

Berikut ini adalah contoh lain, di mana string Unicode digunakan dan
sumbu di luar area plot.


\>aspect(1.5); 

\>plot2d(["sin(x)","cos(x)"],0,2pi,color=[red,green],<grid,<frame); ...  
\>    xaxis(-1.1,(0:2)\*pi,xt=["0",u"&pi;",u"2&pi;"],style="-",\>ticks,\>zero);  ...  
\>    xgrid((0:0.5:2)\*pi,<ticks); ...  
\>    yaxis(-0.1\*pi,-1:0.2:1,style="-",\>zero,\>grid); ...  
\>    labelbox(["sin","cos"],colors=[red,green],x=0.5,y=0.2,\>left); ...  
\>    xlabel(u"&phi;"); ylabel(u"f(&phi;)"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-078.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-078.png)

# Memplot Data 2D

Jika x dan y adalah vektor data, data ini akan digunakan sebagai
koordinat x dan y dari sebuah kurva. Dalam hal ini, a, b, c, dan d,
atau radius r dapat ditentukan, atau jendela plot akan menyesuaikan
secara otomatis dengan data. Sebagai alternatif, &gt;square dapat diatur
untuk mempertahankan rasio aspek persegi.


Memplot ekspresi hanyalah singkatan untuk plot data. Untuk plot data,
Anda memerlukan satu atau beberapa baris nilai x, dan satu atau
beberapa baris nilai y. Dari rentang dan nilai x, fungsi plot2d akan
menghitung data untuk diplot, secara default dengan evaluasi adaptif
dari fungsi tersebut. Untuk plot titik, gunakan “&gt;points”, untuk garis
dan titik campuran gunakan “&gt;addpoints”.


Namun Anda dapat memasukkan data secara langsung.


* 
Gunakan vektor baris untuk x dan y untuk satu fungsi.

* 
Matriks untuk x dan y diplot baris demi baris.


Berikut adalah contoh dengan satu baris untuk x dan y.


\>x=-10:0.1:10; y=exp(-x^2)\*x; plot2d(x,y):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-079.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-079.png)

Data juga dapat diplot sebagai titik. Gunakan poin=true untuk ini.
Plot ini bekerja seperti poligon, namun hanya menggambar
sudut-sudutnya saja.


* 
style = “...”: Pilih dari “[]”, “&lt;&gt;”, “o”, “.”, “..”, “+”, “*”, “[]
* #”, “&lt;&gt;#”, “o#”, “..#”, “#”, “|”.


Untuk memplot kumpulan titik, gunakan &gt;titik. Jika warna adalah sebuah
vektor warna, setiap titik


mendapatkan warna yang berbeda. Untuk sebuah matriks koordinat dan
vektor kolom, warna berlaku pada baris-baris matriks.


Parameter &gt;addpoints menambahkan titik-titik pada segmen garis untuk
plot data.


\>xdata=[1,1.5,2.5,3,4]; ydata=[3,3.1,2.8,2.9,2.7]; // data

\>plot2d(xdata,ydata,a=0.5,b=4.5,c=2.5,d=3.5,style="."); // lines

\>plot2d(xdata,ydata,\>points,\>add,style="o"): // add points


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-080.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-080.png)

\>p=polyfit(xdata,ydata,1); // get regression line

\>plot2d("polyval(p,x)",\>add,color=red): // add plot of line


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-081.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-081.png)

# Menggambar Daerah Yang Dibatasi Kurva

Plot data sebenarnya adalah poligon. Kita juga dapat memplot kurva
atau kurva yang terisi.


* 
filled=true mengisi plot.

* 
style = “...”: Pilih dari “#”, “/”, “\”, “\/”.

* 
fillcolor: Lihat di atas untuk warna yang tersedia.


Warna isian ditentukan oleh argumen “fillcolor”, dan pada pilihan
&lt;outline mencegah menggambar batas untuk semua gaya kecuali gaya
default.


\>t=linspace(0,2pi,1000); // parameter for curve

\>x=sin(t)\*exp(t/pi); y=cos(t)\*exp(t/pi); // x(t) and y(t)

\>figure(1,2); aspect(16/9)

\>figure(1); plot2d(x,y,r=10); // plot curve

\>figure(2); plot2d(x,y,r=10,\>filled,style="/",fillcolor=red); // fill curve

\>figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-082.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-082.png)

Pada contoh berikut ini, kami memplot elips terisi dan dua segi enam
terisi menggunakan kurva tertutup dengan 6 titik dengan gaya isian
yang berbeda.


\>x=linspace(0,2pi,1000); plot2d(sin(x),cos(x)\*0.5,r=1,\>filled,style="/"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-083.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-083.png)

\>t=linspace(0,2pi,6); ...  
\>   plot2d(cos(t),sin(t),\>filled,style="/",fillcolor=red,r=1.2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-084.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-084.png)

\>t=linspace(0,2pi,6); plot2d(cos(t),sin(t),\>filled,style="#"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-085.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-085.png)

Contoh lainnya adalah septagon, yang kita buat dengan 7 titik pada
lingkaran satuan.


\>t=linspace(0,2pi,7);  ...  
\>    plot2d(cos(t),sin(t),r=1,\>filled,style="/",fillcolor=red):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-086.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-086.png)

Berikut ini adalah himpunan nilai maksimal dari empat kondisi linier
yang kurang dari atau sama dengan 3. Ini adalah A[k].v&lt;=3 untuk semua
barisan A. Untuk mendapatkan sudut-sudut yang bagus, kita menggunakan
n yang relatif besar.


\>A=[2,1;1,2;-1,0;0,-1];

\>function f(x,y) := max([x,y].A');

\>plot2d("f",r=4,level=[0;3],color=green,n=111):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-087.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-087.png)

Poin utama dari bahasa matriks adalah bahwa bahasa ini memungkinkan
untuk menghasilkan tabel fungsi dengan mudah.


\>t=linspace(0,2pi,1000); x=cos(3\*t); y=sin(4\*t);


Kita sekarang memiliki vektor nilai x dan y. plot2d() dapat memplot
nilai-nilai ini


sebagai sebuah kurva yang menghubungkan titik-titik. Plot dapat diisi.
Dalam kasus ini


ini memberikan hasil yang bagus karena aturan penggulungan, yang
digunakan untuk


pengisian.


\>plot2d(x,y,<grid,<frame,\>filled):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-088.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-088.png)

Vektor interval diplot terhadap nilai x sebagai wilayah yang terisi


antara nilai bawah dan atas interval.


Hal ini dapat berguna untuk memplot kesalahan perhitungan. Tapi itu
bisa


juga dapat digunakan untuk memplot kesalahan statistik.


\>t=0:0.1:1; ...  
\>    plot2d(t,interval(t-random(size(t)),t+random(size(t))),style="|");  ...  
\>    plot2d(t,t,add=true):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-089.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-089.png)

Jika x adalah vektor yang diurutkan, dan y adalah vektor interval,
maka plot2d akan memplot rentang interval yang terisi pada bidang,
gaya isian sama dengan gaya poligon.


\>t=-1:0.01:1; x=~t-0.01,t+0.01~; y=x^3-x;

\>plot2d(t,y):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-090.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-090.png)

Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk


ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah


dan baris kedua berisi batas atas.


\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)

\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-091.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-091.png)

Kita juga dapat mengisi rentang nilai seperti


$$-1 \le (x^2+y^2)^2-x^2+y^2 \le 0.$$\>plot2d("(x^2+y^2)^2-x^2+y^2",r=1.2,level=[-1;0],style="/"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-093.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-093.png)

\>plot2d("cos(x)","sin(x)^3",xmin=0,xmax=2pi,\>filled,style="/"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-094.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-094.png)

# Grafik Fungsi Parametrik

Nilai x tidak perlu diurutkan. (x,y) hanya menggambarkan sebuah kurva.
Jika x diurutkan, kurva tersebut adalah grafik fungsi.


Pada contoh berikut, kita memplot spiral


$$\gamma(t) = t \cdot (\cos(2\pi t),\sin(2\pi t))$$Kita mungkin perlu menggunakan sangat banyak titik untuk tampilan yang
halus atau fungsi adaptive() untuk mengevaluasi ekspresi (lihat fungsi
adaptive() untuk lebih jelasnya).


\>t=linspace(0,1,1000); ...  
\>   plot2d(t\*cos(2\*pi\*t),t\*sin(2\*pi\*t),r=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-096.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-096.png)

Sebagai alternatif, Anda dapat menggunakan dua ekspresi untuk kurva.
Berikut ini memplot kurva yang sama seperti di atas.


\>plot2d("x\*cos(2\*pi\*x)","x\*sin(2\*pi\*x)",xmin=0,xmax=1,r=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-097.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-097.png)

\>t=linspace(0,1,1000); r=exp(-t); x=r\*cos(2pi\*t); y=r\*sin(2pi\*t);

\>plot2d(x,y,r=1):


Dalam contoh berikut, kami memplot kurva


$$\gamma(t) = (r(t) \cos(t), r(t) \sin(t))$$dengan


$$r(t) = 1 + \dfrac{\sin(3t)}{2}.$$\>t=linspace(0,2pi,1000); r=1+sin(3\*t)/2; x=r\*cos(t); y=r\*sin(t); ...  
\>   plot2d(x,y,\>filled,fillcolor=red,style="/",r=1.5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-100.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-100.png)

# Menggambar Grafik Bilangan Kompleks

Sebuah deretan bilangan kompleks juga dapat diplot. Kemudian
titik-titik kisi akan dihubungkan. Jika sejumlah garis kisi ditentukan
(atau vektor 1x2 garis kisi) pada argumen cgrid, hanya garis-garis
kisi tersebut yang akan terlihat.


Matriks bilangan kompleks akan secara otomatis diplot sebagai sebuah
grid pada bidang kompleks.


Pada contoh berikut, kita memplot gambar lingkaran satuan di bawah
fungsi eksponensial. Parameter cgrid menyembunyikan beberapa kurva
grid.


\>aspect(); r=linspace(0,1,50); a=linspace(0,2pi,80)'; z=r\*exp(I\*a);...  
\>   plot2d(z,a=-1.25,b=1.25,c=-1.25,d=1.25,cgrid=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-101.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-101.png)

\>aspect(1.25); r=linspace(0,1,50); a=linspace(0,2pi,200)'; z=r\*exp(I\*a);

\>plot2d(exp(z),cgrid=[40,10]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-102.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-102.png)

\>r=linspace(0,1,10); a=linspace(0,2pi,40)'; z=r\*exp(I\*a);

\>plot2d(exp(z),\>points,\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-103.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-103.png)

Vektor bilangan kompleks secara otomatis diplot sebagai kurva pada
bidang kompleks dengan bagian nyata dan bagian imajiner.


Pada contoh, kami memplot lingkaran satuan dengan


lateks: \gamma(t) = e^{it}


\>t=linspace(0,2pi,1000); ...  
\>   plot2d(exp(I\*t)+exp(4\*I\*t),r=2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-104.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-104.png)

# Plot Statistik

Terdapat banyak fungsi yang dikhususkan untuk plot statistik. Salah
satu plot yang sering digunakan adalah plot kolom.


Jumlah kumulatif dari nilai berdistribusi normal 0-1 menghasilkan
jalan acak.


\>plot2d(cumsum(randnormal(1,1000))):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-105.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-105.png)

Dengan menggunakan dua baris, ini menunjukkan jalan kaki dalam dua
dimensi.


\>X=cumsum(randnormal(2,1000)); plot2d(X[1],X[2]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-106.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-106.png)

\>columnsplot(cumsum(random(10)),style="/",color=blue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-107.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-107.png)

Ini juga dapat menampilkan string sebagai label.


\>months=["Jan","Feb","Mar","Apr","May","Jun", ...  
\>     "Jul","Aug","Sep","Oct","Nov","Dec"];

\>values=[10,12,12,18,22,28,30,26,22,18,12,8];

\>columnsplot(values,lab=months,color=red,style="-");

\>title("Temperature"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-108.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-108.png)

\>k=0:10;

\>plot2d(k,bin(10,k),\>bar):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-109.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-109.png)

\>plot2d(k,bin(10,k)); plot2d(k,bin(10,k),\>points,\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-110.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-110.png)

\>plot2d(normal(1000),normal(1000),\>points,grid=6,style=".."):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-111.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-111.png)

\>plot2d(normal(1,1000),\>distribution,style="O"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-112.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-112.png)

\>plot2d("qnormal",0,5;2.5,0.5,\>filled):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-113.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-113.png)

Untuk memplot distribusi statistik eksperimental, Anda dapat
menggunakan distribution=n dengan plot2d.


\>w=randexponential(1,1000); // exponential distribution

\>plot2d(w,\>distribution): // or distribution=n with n intervals


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-114.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-114.png)

Atau Anda dapat menghitung distribusi dari data dan memplot hasilnya
dengan &gt;bar di plot3d, atau dengan plot kolom.


\>w=normal(1000); // 0-1-normal distribution

\>{x,y}=histo(w,10,v=[-6,-4,-2,-1,0,1,2,4,6]); // interval bounds v

\>plot2d(x,y,\>bar):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-115.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-115.png)

Fungsi statplot() menetapkan gaya dengan string sederhana.


\>statplot(1:10,cumsum(random(10)),"b"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-116.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-116.png)

\>n=10; i=0:n; ...  
\>   plot2d(i,bin(n,i)/2^n,a=0,b=10,c=0,d=0.3); ...  
\>   plot2d(i,bin(n,i)/2^n,points=true,style="ow",add=true,color=blue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-117.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-117.png)

Selain itu, data dapat diplot sebagai batang. Dalam hal ini, x harus
diurutkan dan satu elemen lebih panjang dari y. Batang akan memanjang
dari x[i] ke x[i+1] dengan nilai y[i]. Jika x memiliki ukuran yang
sama dengan y, maka x akan diperpanjang satu elemen dengan jarak
terakhir.


Gaya isian dapat digunakan seperti di atas.


\>n=10; k=bin(n,0:n); ...  
\>   plot2d(-0.5:n+0.5,k,bar=true,fillcolor=lightgray):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-118.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-118.png)

Data untuk plot batang (batang = 1) dan histogram (histogram = 1)
dapat diberikan secara eksplisit dalam xv dan yv, atau dapat dihitung
dari distribusi empiris dalam xv dengan &gt;distribusi (atau distribusi =
n). Histogram dari nilai xv akan dihitung secara otomatis dengan
&gt;histogram. Jika &gt;even ditentukan, nilai xv akan dihitung dalam
interval bilangan bulat.


\>plot2d(normal(10000),distribution=50):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-119.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-119.png)

\>k=0:10; m=bin(10,k); x=(0:11)-0.5; plot2d(x,m,\>bar):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-120.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-120.png)

\>columnsplot(m,k):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-121.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-121.png)

\>plot2d(random(600)\*6,histogram=6):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-122.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-122.png)

Untuk distribusi, ada parameter distribution=n, yang menghitung nilai
secara otomatis dan mencetak distribusi relatif dengan n sub-interval.


\>plot2d(normal(1,1000),distribution=10,style="\\/"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-123.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-123.png)

Dengan parameter even=true, ini akan menggunakan interval bilangan
bulat.


\>plot2d(intrandom(1,1000,10),distribution=10,even=true):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-124.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-124.png)

Perhatikan bahwa ada banyak plot statistik yang mungkin berguna.
Lihatlah tutorial tentang statistik.


\>columnsplot(getmultiplicities(1:6,intrandom(1,6000,6))):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-125.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-125.png)

\>plot2d(normal(1,1000),\>distribution); ...  
\>     plot2d("qnormal(x)",color=red,thickness=2,\>add):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-126.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-126.png)

Ada juga banyak plot khusus untuk statistik. Boxplot menunjukkan
kuartil dari distribusi ini dan banyak pencilan. Menurut definisi,
pencilan dalam boxplot adalah data yang melebihi 1,5 kali kisaran 50%
tengah plot.


\>M=normal(5,1000); boxplot(quartiles(M)):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-127.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-127.png)

# Fungsi Implisit

Plot implisit menunjukkan garis level yang menyelesaikan f(x,y)=level,
di mana “level” dapat berupa nilai tunggal atau vektor nilai. Jika
level = “auto”, akan ada nc garis level, yang akan menyebar di antara
minimum dan maksimum fungsi secara merata. Warna yang lebih gelap atau
lebih terang dapat ditambahkan dengan &gt;hue untuk mengindikasikan nilai
fungsi. Untuk fungsi implisit, xv haruslah sebuah fungsi atau ekspresi
dari parameter x dan y, atau, sebagai alternatif, xv dapat berupa
matriks nilai.


Euler dapat menandai garis level


$$f(x,y) = c$$dari fungsi apa pun.


Untuk menggambar himpunan f(x,y) = c untuk satu atau lebih konstanta
c, Anda bisa menggunakan plot2d() dengan plot implisitnya pada bidang.
Parameter untuk c adalah level = c, di mana c dapat berupa vektor
garis level. Sebagai tambahan, sebuah skema warna dapat digambar pada
latar belakang untuk mengindikasikan nilai fungsi untuk setiap titik
pada plot. Parameter “n” menentukan kehalusan plot.


\>aspect(1.5); 

\>plot2d("x^2+y^2-x\*y-x",r=1.5,level=0,contourcolor=red):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-129.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-129.png)

\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)

\>plot2d(expr,level=0): // Solutions of f(x,y)=0


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-130.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-130.png)

\>plot2d(expr,level=0:0.5:20,\>hue,contourcolor=white,n=200): // nice


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-131.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-131.png)

\>plot2d(expr,level=0:0.5:20,\>hue,\>spectral,n=200,grid=4): // nicer


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-132.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-132.png)

Hal ini juga berlaku untuk plot data. Tetapi Anda harus menentukan
rentang


untuk label sumbu.


\>x=-2:0.05:1; y=x'; z=expr(x,y);

\>plot2d(z,level=0,a=-1,b=2,c=-2,d=1,\>hue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-133.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-133.png)

\>plot2d("x^3-y^2",\>contour,\>hue,\>spectral):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-134.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-134.png)

\>plot2d("x^3-y^2",level=0,contourwidth=3,\>add,contourcolor=red):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-135.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-135.png)

\>z=z+normal(size(z))\*0.2;

\>plot2d(z,level=0.5,a=-1,b=2,c=-2,d=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-136.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-136.png)

\>plot2d(expr,level=[0:0.2:5;0.05:0.2:5.05],color=lightgray):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-137.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-137.png)

\>plot2d("x^2+y^3+x\*y",level=1,r=4,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-138.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-138.png)

\>plot2d("x^2+2\*y^2-x\*y",level=0:0.1:10,n=100,contourcolor=white,\>hue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-139.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-139.png)

Dimungkinkan juga untuk mengisi set


$$a \le f(x,y) \le b$$dengan rentang level.


Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk
ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah
dan baris kedua berisi batas atas.


\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-141.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-141.png)

Plot implisit juga dapat menunjukkan rentang level. Maka level harus
berupa matriks 2xn interval level, di mana baris pertama berisi awal
dan baris kedua adalah akhir dari setiap interval. Sebagai alternatif,
vektor baris sederhana dapat digunakan untuk level, dan parameter dl
memperluas nilai level ke interval.


\>plot2d("x^4+y^4",r=1.5,level=[0;1],color=blue,style="/"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-142.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-142.png)

\>plot2d("x^2+y^3+x\*y",level=[0,2,4;1,3,5],style="/",r=2,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-143.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-143.png)

\>plot2d("x^2+y^3+x\*y",level=-10:20,r=2,style="-",dl=0.1,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-144.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-144.png)

\>plot2d("sin(x)\*cos(y)",r=pi,\>hue,\>levels,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-145.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-145.png)

Anda juga dapat menandai suatu wilayah


$$a \le f(x,y) \le b.$$Hal ini dilakukan dengan menambahkan level dengan dua baris.


\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>     style="#",color=red,<outline, ...  
\>     level=[-2;0],n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-147.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-147.png)

Dimungkinkan untuk menentukan level tertentu. Sebagai contoh, kita
dapat memplot solusi dari persamaan seperti


$$x^3-xy+x^2y^2=6$$\>plot2d("x^3-x\*y+x^2\*y^2",r=6,level=1,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-149.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-149.png)

\>function starplot1 (v, style="/", color=green, lab=none) ...


      if !holding() then clg; endif;
      w=window(); window(0,0,1024,1024);
      h=holding(1);
      r=max(abs(v))*1.2;
      setplot(-r,r,-r,r);
      n=cols(v); t=linspace(0,2pi,n);
      v=v|v[1]; c=v*cos(t); s=v*sin(t);
      cl=barcolor(color); st=barstyle(style);
      loop 1 to n
        polygon([0,c[#],c[#+1]],[0,s[#],s[#+1]],1);
        if lab!=none then
          rlab=v[#]+r*0.1;
          {col,row}=toscreen(cos(t[#])*rlab,sin(t[#])*rlab);
          ctext(""+lab[#],col,row-textheight()/2);
        endif;
      end;
      barcolor(cl); barstyle(st);
      holding(h);
      window(w);
    endfunction
</pre>
Tidak ada kisi-kisi atau kutu sumbu di sini. Selain itu, kami
menggunakan jendela penuh untuk plot.


Kami memanggil reset sebelum kami menguji plot ini untuk mengembalikan
default grafis. Hal ini tidak perlu dilakukan, jika Anda yakin bahwa
plot Anda berfungsi.


\>reset; starplot1(normal(1,10)+5,color=red,lab=1:10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-150.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-150.png)

Terkadang, Anda mungkin ingin memplot sesuatu yang tidak dapat
dilakukan oleh plot2d, tetapi hampir.


Pada fungsi berikut ini, kita akan membuat plot impuls logaritmik.
plot2d dapat membuat plot logaritmik, tetapi tidak untuk batang
impuls.


\>function logimpulseplot1 (x,y) ...


      {x0,y0}=makeimpulse(x,log(y)/log(10));
      plot2d(x0,y0,>bar,grid=0);
      h=holding(1);
      frame();
      xgrid(ticks(x));
      p=plot();
      for i=-10 to 10;
        if i<=p[4] and i>=p[3] then
           ygrid(i,yt="10^"+i);
        endif;
      end;
      holding(h);
    endfunction
</pre>
Let us test it with exponentially distributed values.


\>aspect(1.5); x=1:10; y=-log(random(size(x)))\*200; ...  
\>   logimpulseplot1(x,y):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-151.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-151.png)

Mari kita menghidupkan kurva 2D dengan menggunakan plot langsung.
Perintah plot(x,y) hanya memplot kurva ke dalam jendela plot.
setplot(a,b,c,d) mengatur jendela ini.


Fungsi wait(0) memaksa plot untuk muncul pada jendela grafik. Jika
tidak, penggambaran ulang akan dilakukan dalam interval waktu yang
jarang.


\>function animliss (n,m) ...


    t=linspace(0,2pi,500);
    f=0;
    c=framecolor(0);
    l=linewidth(2);
    setplot(-1,1,-1,1);
    repeat
      clg;
      plot(sin(n*t),cos(m*t+f));
      wait(0);
      if testkey() then break; endif;
      f=f+0.02;
    end;
    framecolor(c);
    linewidth(l);
    endfunction
</pre>
Tekan sembarang tombol untuk menghentikan animasi ini.


\>animliss(2,3); // lihat hasilnya, jika sudah puas, tekan ENTER


# Plot Logaritmik

EMT menggunakan parameter “logplot” untuk skala logaritmik.


Plot logaritmik dapat diplot menggunakan skala logaritmik dalam y
dengan logplot = 1, atau menggunakan skala logaritmik dalam x dan y
dengan logplot = 2, atau dalam x dengan logplot = 3.


 - logplot = 1: y-logaritmik  
 - logplot=2: x-y-logaritmik  
 - logplot=3: x-logaritmik  

\>plot2d("exp(x^3-x)\*x^2",1,5,logplot=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-152.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-152.png)

\>plot2d("exp(x+sin(x))",0,100,logplot=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-153.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-153.png)

\>plot2d("exp(x+sin(x))",10,100,logplot=2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-154.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-154.png)

\>plot2d("gamma(x)",1,10,logplot=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-155.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-155.png)

\>plot2d("log(x\*(2+sin(x/100)))",10,1000,logplot=3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-156.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-156.png)

Hal ini juga bisa dilakukan dengan plot data.


\>x=10^(1:20); y=x^2-x;

\>plot2d(x,y,logplot=2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-157.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Materi%20plot%202d-157.png)

# Rujukan Lengkap Fungsi plot2d()

  function plot2d (xv, yv, btest, a, b, c, d, xmin, xmax, r, n,  ..  
  logplot, grid, frame, framecolor, square, color, thickness, style, ..  
  auto, add, user, delta, points, addpoints, pointstyle, bar, histogram,  ..  
  distribution, even, steps, own, adaptive, hue, level, contour,  ..  
  nc, filled, fillcolor, outline, title, xl, yl, maps, contourcolor, ..  
  contourwidth, ticks, margin, clipping, cx, cy, insimg, spectral,  ..  
  cgrid, vertical, smaller, dl, niveau, levels)  

Multipurpose plot function for plots in the plane (2D plots). This function can do
plots of functions of one variables, data plots, curves in the plane, bar plots, grids
of complex numbers, and implicit plots of functions of two variables.


Parameters




x,y       : equations, functions or data vectors


a,b,c,d   : Plot area (default a=-2,b=2)


r         : if r is set, then a=cx-r, b=cx+r, c=cy-r, d=cy+r


            r can be a vector [rx,ry] or a vector [rx1,rx2,ry1,ry2].


xmin,xmax : range of the parameter for curves


auto      : Determine y-range automatically (default)


square    : if true, try to keep square x-y-ranges


n         : number of intervals (default is adaptive)


grid      : 0 = no grid and labels,


            1 = axis only,


            2 = normal grid (see below for the number of grid lines)


            3 = inside axis


            4 = no grid


            5 = full grid including margin


            6 = ticks at the frame


            7 = axis only


            8 = axis only, sub-ticks


frame     : 0 = no frame


framecolor: color of the frame and the grid


margin    : number between 0 and 0.4 for the margin around the plot


color     : Color of curves. If this is a vector of colors,


            it will be used for each row of a matrix of plots. In the case of


            point plots, it should be a column vector. If a row vector or a


            full matrix of colors is used for point plots, it will be used for


            each data point.


thickness : line thickness for curves


            This value can be smaller than 1 for very thin lines.


style     : Plot style for lines, markers, and fills.


            For points use


            "[]", "&lt;&gt;", ".", "..", "...",


            "*", "+", "|", "-", "o"


            "[]#", "&lt;&gt;#", "o#" (filled shapes)


            "[]w", "&lt;&gt;w", "ow" (non-transparent)


            For lines use


            "-", "--", "-.", ".", ".-.", "-.-", "-&gt;"


            For filled polygons or bar plots use


            "#", "#O", "O", "/", "\", "\/",


            "+", "|", "-", "t"


points    : plot single points instead of line segments


addpoints : if true, plots line segments and points


add       : add the plot to the existing plot


user      : enable user interaction for functions


delta     : step size for user interaction


bar       : bar plot (x are the interval bounds, y the interval values)


histogram : plots the frequencies of x in n subintervals


distribution=n : plots the distribution of x with n subintervals


even      : use inter values for automatic histograms.


steps     : plots the function as a step function (steps=1,2)


adaptive  : use adaptive plots (n is the minimal number of steps)


level     : plot level lines of an implicit function of two variables


outline   : draws boundary of level ranges.




If the level value is a 2xn matrix, ranges of levels will be drawn


in the color using the given fill style. If outline is true, it


will be drawn in the contour color. Using this feature, regions of


f(x,y) between limits can be marked.




hue       : add hue color to the level plot to indicate the function


            value


contour   : Use level plot with automatic levels


nc        : number of automatic level lines


title     : plot title (default "")


xl, yl    : labels for the x- and y-axis


smaller   : if &gt;0, there will be more space to the left for labels.


vertical  :


  Turns vertical labels on or off. This changes the global variable


  verticallabels locally for one plot. The value 1 sets only vertical


  text, the value 2 uses vertical numerical labels on the y axis.


filled    : fill the plot of a curve


fillcolor : fill color for bar and filled curves


outline   : boundary for filled polygons


logplot   : set logarithmic plots


            1 = logplot in y,


            2 = logplot in xy,


            3 = logplot in x


own       :


  A string, which points to an own plot routine. With &gt;user, you get


  the same user interaction as in plot2d. The range will be set


  before each call to your function.


maps      : map expressions (0 is faster), functions are always mapped.


contourcolor : color of contour lines


contourwidth : width of contour lines


clipping  : toggles the clipping (default is true)


title     :


  This can be used to describe the plot. The title will appear above


  the plot. Moreover, a label for the x and y axis can be added with


  xl="string" or yl="string". Other labels can be added with the


  functions label() or labelbox(). The title can be a unicode


  string or an image of a Latex formula.


cgrid     :


  Determines the number of grid lines for plots of complex grids.


  Should be a divisor of the the matrix size minus 1 (number of


  subintervals). cgrid can be a vector [cx,cy].


Overview


The function can plot


* 
expressions, call collections or functions of one variable,

* 
parametric curves,

* 
x data against y data,

* 
implicit functions,

* 
bar plots,

* 
complex grids,

* 
polygons.


If a function or expression for xv is given, plot2d() will compute


values in the given range using the function or expression. The


expression must be an expression in the variable x. The range must


be defined in the parameters a and b unless the default range


[-2,2] should be used. The y-range will be computed automatically,


unless c and d are specified, or a radius r, which yields the range


[-r,r] for x and y. For plots of functions, plot2d will use an


adaptive evaluation of the function by default. To speed up the


plot for complicated functions, switch this off with &lt;adaptive, and


optionally decrease the number of intervals n. Moreover, plot2d()


will by default use mapping. I.e., it will compute the plot element


for element. If your expression or your functions can handle a


vector x, you can switch that off with &lt;maps for faster evaluation.


Note that adaptive plots are always computed element for element. 


If functions or expressions for both xv and for yv are specified,


plot2d() will compute a curve with the xv values as x-coordinates


and the yv values as y-coordinates. In this case, a range should be


defined for the parameter using xmin, xmax. Expressions contained


in strings must always be expressions in the parameter variable x.



## Contoh soal Plot 2d

# Menggambar Grafik Fungsi Satu Variabel dalam Bentuk Ekspresi

Langsung


\>plot2d("x^2 - 4\*x + 3"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-001.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-001.png)

Ekspresi tunggal dalam “x” (misalnya “x^2 - 4*x + 3 pada soal) atau
nama fungsi (misalnya “f”) menghasilkan grafik fungsi.


# Menggambar Grafik Fungsi Satu Variabel yang Rumusnya Disimpan dalam

Variabel Ekspresi


\>function f(x):= sin(x);

\> plot2d("f", 0, 2pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-002.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-002.png)

Menyimpan suatu perintah lalu dipanggil kembali saat menggunakannya
seperti memanggil fungsi yang ada untuk dijadikan suatu plot


# Menggambar Grafik Fungsi Satu Variabel yang Fungsinya Didefinisikan

sebagai Fungsi Numerik


\>function f(x) := 1/x

\>plot2d("f"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-003.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-003.png)

Disini tampak fungsi yang ada terdapat variabel yang bersifat numerik
karena terdapat operasi hitung pada variabel


# Menggambar Grafik Fungsi Satu Variabel yang Fungsinya Didefinisikan

sebagai Fungsi Simbolik


\>function g(x) := exp(x); 

\>plot2d("g"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-004.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-004.png)

disini kita memberikan suatu simbol untuk suatu fungsi yang berisi
perintah fungsi, nantinya akan bisa dipanggil layaknya fungsi biasa


# Menggambar Beberapa Kurva Sekaligus

\>plot2d("cos(x)", "sin(x)", [0, 2\*pi]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-005.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-005.png)

Kita juga bisa menggambarkan beberapa fungsi sekaligus dengan cara
memberikan koma dan "..." pada fungsi yang akan kita gunakan


# Menggambar Beberapa Kurva dalam Satu Bidang Koordinat

\>plot2d("x^2", "x^3", [-2, 2]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-006.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-006.png)

sama halnya ini juga menggambarkan beberapa kurva dengan ".." dan koma
sebagai pemisah dengan batasan yang ada


# Menuliskan Label Sumbu Koordinat, Label Kurva, dan Keterangan Kurva

(Legend)


\>plot2d("exp(x)",-1,1);

\>textcolor(black); // set the text color to black

\>title(latex("y=e^x")); // title above the plot

\>xlabel(latex("x")); // "x" for x-axis

\>ylabel(latex("y"),\>vertical); // vertical "y" for y-axis

\>label(latex("(0,1)"),0,1,color=blue): // label a point


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-007.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-007.png)

kita juga bisa memberikan nama pada grafik kita dengan 


&gt;textcolor() untuk memberikan warna teks


&gt;title() untuk memberikan judul grafik


&gt;xlabel() untuk memberikan teks pada ordinat


&gt;ylabel() untuk memberikan teks pada absis


&gt;label(latex("(x,y)"),color=...) untuk memberikan garis perpotongan


# Mengatur Ukuran Gambar, Format (Style), dan Warna Kurva

\>plot2d("log(x)", color=[red]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-008.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-008.png)

kita juga memberikan bentuk lain garis dengan style"..." atau warna
yang diinginkan


# Menggambar Sekumpulan Kurva dengan Satu Perintah plot2d

\>aspect();

\>figure(3,3); ...  
\>    figure(1); plot2d("x^2-x",grid=0); ... // no grid, frame or axis

\> figure(2); plot2d("x",grid=1); ... // x-y-axis

\> figure(3); plot2d("x^3",grid=2); ... // default ticks

\>figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-009.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-009.png)

untuk memberikan beberapa grafik sekaligus kita bisa menggunakan
figure() untuk ukurannya dan urutan 1 hingga n untuk setiap grafik


# Membuat Gambar Kurva yang Bersifat Interaktif

\>plot2d({{"x^2-a\*x",a=1}},\>user,title="Press any key!"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-010.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-010.png)

penggunaan user bisa dilakukan untuk memberikan pengguna bisa
berinteraksi secara langsung pada grafik yang dibuat


# Menggambar Kurva Fungsi Parametrik

\>t=linspace(0,1,1000); ...  
\>   plot2d(t\*cos(8\*pi\*t),t\*sin(4\*pi\*t),r=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-011.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-011.png)

Grafik parametrik juga bisa untuk memberikan gambaran dalam rentang
suatu grafik dengan t parametrik


# Menggambar Kurva Fungsi Implisit

\>aspect(2);

\>plot2d("x^3+y^2\*y-x",r=2,level=0,contourcolor=red):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-012.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-012.png)

\>t=linspace(0,2pi,1000); ...  
\>   plot2d(exp(I\*t)+exp(8\*I\*t),r=4):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-013.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-013.png)

Kita juga bisa membuat grafik implisit dengan beberapa variabel di
dalamnya


# Menggambar Daerah Yang Dibatasi Kurva

\>t=linspace(0,2pi,6); ...  
\>   plot2d(sec(t),sin(t),\>filled,style="/",fillcolor=red,r=1.2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-014.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_soal%20plot%202d-014.png)

Untuk memberikan daerah luasan kita bisa memberikan isi pada kurva
yang dibuat juga


<pre class="udf">    
</pre>



# Menggambar Plot 3D dengan EMT

Ini adalah pengenalan plot 3D di Euler. Kita memerlukan plot 3D untuk
memvisualisasikan fungsi dua variabel.


Euler menggambar fungsi tersebut menggunakan algoritma pengurutan
untuk menyembunyikan bagian-bagian di latar belakang. Secara umum,
Euler menggunakan proyeksi pusat. Standarnya adalah dari kuadran x-y
positif ke arah titik asal x=y=z=0, tetapi sudut=0° terlihat dari arah
sumbu y. Sudut pandang dan ketinggian dapat diubah.


Euler dapat memetakan


* 
permukaan dengan bayangan dan garis level atau rentang level,

* 
awan titik-titik,

* 
kurva parametrik,

* 
permukaan implisit.


Plot 3D dari sebuah fungsi menggunakan plot3d. Cara termudah adalah
memplot ekspresi dalam x dan y. Parameter r mengatur rentang plot di
sekitar (0,0).


\>aspect(1.5); plot3d("x^2+sin(y)",-5,5,0,6\*pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-001.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-001.png)

\>plot3d("x^2+x\*sin(y)",-5,5,0,6\*pi):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-002.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-002.png)

Silakan lakukan modifikasi agar gambar "talang bergelombang" tersebut tidak lurus melainkan melengkung/melingkar, baik
melingkar secara mendatar maupun melingkar turun/naik (seperti papan peluncur pada kolam renang. Temukan rumusnya.


# Fungsi dari dua Variabel

Untuk grafik sebuah fungsi, gunakan


* 
ekspresi sederhana dalam x dan y,

* 
nama fungsi dari dua variabell

* 
atau matriks data.


Standarnya adalah kisi-kisi kawat yang terisi dengan warna yang
berbeda di kedua sisi. Perhatikan bahwa jumlah default interval grid
adalah 10, namun plot menggunakan jumlah default 40x40 persegi panjang
untuk membangun permukaan. Hal ini dapat diubah.


* 
n=40, n=[40,40]: jumlah garis kisi di setiap arah

* 
grid=10, grid=[10,10]: jumlah garis grid di setiap arah.


Kami menggunakan default n=40 dan grid=10.


\>plot3d("x^2+y^2"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-003.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-003.png)

Interaksi pengguna dapat dilakukan dengan parameter &gt;user. Pengguna
dapat menekan tombol berikut ini.


* 
kiri, kanan, atas, bawah: memutar sudut pandang

* 
+,-: memperbesar atau memperkecil

* 
a: menghasilkan anaglyph (lihat di bawah)

* 
l: beralih memutar sumber cahaya (lihat di bawah)

* 
spasi: mengatur ulang ke default

* 
kembali: mengakhiri interaksi


\>plot3d("exp(-x^2+y^2)",\>user, ...  
\>     title="Turn with the vector keys (press return to finish)"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-004.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-004.png)

Rentang plot untuk fungsi dapat ditentukan dengan


* 
a, b: rentang x

* 
c, d: rentang y

* 
r: bujur sangkar simetris di sekitar (0,0).

* 
n: jumlah subinterval untuk plot.


Terdapat beberapa parameter untuk menskalakan fungsi atau mengubah
tampilan grafik.


fscale: skala untuk nilai fungsi (standarnya adalah &lt;fscale).


scale: angka atau vektor 1x2 untuk menskalakan ke arah x dan y.


frame: jenis bingkai (default 1).


\>plot3d("exp(-(x^2+y^2)/5)",r=10,n=80,fscale=4,scale=1.2,frame=3,\>user):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-005.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-005.png)

Tampilan dapat diubah dengan berbagai cara.


* 
jarak: jarak pandang ke plot.

* 
zoom: nilai zoom.

* 
angle: sudut ke sumbu y negatif dalam radian.

* 
height: ketinggian tampilan dalam radian.


Nilai default dapat diperiksa atau diubah dengan fungsi view(). Fungsi
ini mengembalikan parameter dalam urutan di atas.


\>view


    [5,  2.6,  2,  0.4]

Jarak yang lebih dekat membutuhkan zoom yang lebih sedikit. Efeknya
lebih seperti lensa sudut lebar.


Dalam contoh berikut ini, sudut = 0 dan tinggi = 0 terlihat dari sumbu
y negatif. Label sumbu untuk y disembunyikan dalam kasus ini.


\>plot3d("x^2+y",distance=3,zoom=1,angle=pi/2,height=0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-006.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-006.png)

Plot terlihat selalu ke bagian tengah kubus plot. Anda dapat
memindahkan bagian tengah dengan parameter center.


\>plot3d("x^4+y^2",a=0,b=1,c=-1,d=1,angle=-20°,height=20°, ...  
\>     center=[0.4,0,0],zoom=5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-007.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-007.png)

Plot diskalakan agar sesuai dengan kubus satuan untuk dilihat. Jadi,
tidak perlu mengubah jarak atau melakukan zoom, tergantung pada ukuran
plot. Namun demikian, label mengacu ke ukuran yang sesungguhnya.


Jika Anda menonaktifkannya dengan scale=false, Anda harus berhati-hati
agar plot tetap muat di dalam jendela plotting, dengan mengubah jarak
tampilan atau zoom, dan memindahkan bagian tengahnya.


\>plot3d("5\*exp(-x^2-y^2)",r=2,<fscale,<scale,distance=13,height=50°, ...  
\>     center=[0,0,-2],frame=3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-008.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-008.png)

Plot polar juga tersedia. Parameter polar=true menggambar plot polar.
Fungsi harus tetap merupakan fungsi dari x dan y. Parameter “fscale”
menskalakan fungsi dengan skala sendiri. Jika tidak, fungsi akan
diskalakan agar sesuai dengan kubus.


\>plot3d("1/(x^2+y^2+1)",r=5,\>polar, ...  
\>   fscale=2,\>hue,n=100,zoom=4,\>contour,color=blue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-009.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-009.png)

\>function f(r) := exp(-r/2)\*cos(r); ...  
\>   plot3d("f(x^2+y^2)",\>polar,scale=[1,1,0.4],r=pi,frame=3,zoom=4):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-010.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-010.png)

Parameter rotate memutar fungsi dalam x di sekitar sumbu x.


* 
rotate = 1: Menggunakan sumbu x

* 
rotate=2: Menggunakan sumbu z


\>plot3d("x^2+1",a=-1,b=1,rotate=true,grid=5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-011.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-011.png)

\>plot3d("x^2+1",a=-1,b=1,rotate=2,grid=5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-012.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-012.png)

\>plot3d("sqrt(25-x^2)",a=0,b=5,rotate=1):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-013.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-013.png)

\>plot3d("x\*sin(x)",a=0,b=6pi,rotate=2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-014.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-014.png)

Berikut ini adalah plot dengan tiga fungsi.


\>plot3d("x","x^2+y^2","y",r=2,zoom=3.5,frame=3):


# Plot Kontur

Untuk plot, Euler menambahkan garis kisi-kisi. Sebagai gantinya,
dimungkinkan untuk menggunakan garis level dan rona satu warna atau
rona berwarna spektral. Euler dapat menggambar ketinggian fungsi pada
plot dengan bayangan. Pada semua plot 3D, Euler dapat menghasilkan
anaglyph merah/cyan.


* 
Rona: Mengaktifkan bayangan cahaya, bukan kabel.

* 
&gt;contour: Memplot garis kontur otomatis pada plot.

* 
level=... (atau level): Vektor nilai untuk garis kontur.


Defaultnya adalah level=“auto”, yang menghitung beberapa garis level
secara otomatis. Seperti yang Anda lihat di plot, level sebenarnya
adalah rentang level.


Gaya default dapat diubah. Untuk plot kontur berikut ini, kami
menggunakan grid yang lebih halus untuk titik 100x100, skala fungsi
dan plot, dan menggunakan sudut pandang yang berbeda.


\>plot3d("exp(-x^2-y^2)",r=2,n=100,level="thin", ...  
\>    \>contour,\>spectral,fscale=1,scale=1.1,angle=45°,height=20°):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-015.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-015.png)

\>plot3d("exp(x\*y)",angle=100°,\>contour,color=green):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-016.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-016.png)

Bayangan default menggunakan warna abu-abu. Tetapi, kisaran warna
spektral juga tersedia.


* 
&gt;spektral: Menggunakan skema spektral default

* 
color =...: Menggunakan warna khusus atau skema spektral


Untuk plot berikut ini, kami menggunakan skema spektral default dan
menambah jumlah titik untuk mendapatkan tampilan yang sangat mulus.


\>plot3d("x^2+y^2",\>spectral,\>contour,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-017.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-017.png)

Alih-alih garis level otomatis, kita juga dapat menetapkan nilai garis
level. Hal ini akan menghasilkan garis level yang tipis, alih-alih
rentang level.


\>plot3d("x^2-y^2",0,5,0,5,level=-1:0.1:1,color=redgreen):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-018.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-018.png)

Pada plot berikut ini, kami menggunakan dua pita level yang sangat
luas dari -0,1 hingga 1, dan dari 0,9 hingga 1. Ini dimasukkan sebagai
matriks dengan batas-batas level sebagai kolom.


Selain itu, kami menghamparkan grid dengan 10 interval di setiap arah.


\>plot3d("x^2+y^3",level=[-0.1,0.9;0,1], ...  
\>     \>spectral,angle=30°,grid=10,contourcolor=gray):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-019.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-019.png)

Pada contoh berikut, kami memplot himpunan, di mana


$$f(x,y) = x^y-y^x = 0$$Kita menggunakan satu garis tipis untuk garis level.


\>plot3d("x^y-y^x",level=0,a=0,b=6,c=0,d=6,contourcolor=red,n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-021.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-021.png)

Dimungkinkan untuk menampilkan bidang kontur di bawah plot. Warna dan
jarak ke plot dapat ditentukan.


\>plot3d("x^2+y^4",\>cp,cpcolor=green,cpdelta=0.2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-022.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-022.png)

Berikut ini beberapa gaya lainnya. Kami selalu mematikan bingkai, dan
menggunakan berbagai skema warna untuk plot dan kisi-kisi.


\>figure(2,2); ...  
\>   expr="y^3-x^2"; ...  
\>   figure(1);  ...  
\>     plot3d(expr,<frame,\>cp,cpcolor=spectral); ...  
\>   figure(2);  ...  
\>     plot3d(expr,<frame,\>spectral,grid=10,cp=2); ...  
\>   figure(3);  ...  
\>     plot3d(expr,<frame,\>contour,color=gray,nc=5,cp=3,cpcolor=greenred); ...  
\>   figure(4);  ...  
\>     plot3d(expr,<frame,\>hue,grid=10,\>transparent,\>cp,cpcolor=gray); ...  
\>   figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-023.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-023.png)

Ada beberapa skema spektral lainnya, yang diberi nomor dari 1 hingga
9. Tetapi Anda juga dapat menggunakan color=value, di mana value


* 
spektral: untuk rentang dari biru ke merah

* 
putih: untuk rentang yang lebih redup

* 
kuningbiru, ungu-hijau, biru-kuning, hijau-merah

* 
biru-kuning, hijau-ungu, kuning-biru, merah-hijau


\>figure(3,3); ...  
\>   for i=1:9;  ...  
\>     figure(i); plot3d("x^2+y^2",spectral=i,\>contour,\>cp,<frame,zoom=4);  ...  
\>   end; ...  
\>   figure(0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-024.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-024.png)

Sumber cahaya dapat diubah dengan l dan tombol kursor selama interaksi
pengguna. Ini juga dapat ditetapkan dengan parameter.


* 
light: arah cahaya

* 
amb: cahaya sekitar antara 0 dan 1


Perhatikan, bahwa program ini tidak membuat perbedaan di antara
sisi-sisi plot. Tidak ada bayangan. Untuk ini Anda akan membutuhkan
Povray.


\>plot3d("-x^2-y^2", ...  
\>     hue=true,light=[0,1,1],amb=0,user=true, ...  
\>     title="Press l and cursor keys (return to exit)"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-025.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-025.png)

Parameter warna mengubah warna permukaan. Warna garis level juga dapat
diubah.


\>plot3d("-x^2-y^2",color=rgb(0.2,0.2,0),hue=true,frame=false, ...  
\>     zoom=3,contourcolor=red,level=-2:0.1:1,dl=0.01):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-026.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-026.png)

Warna 0 memberikan efek pelangi yang istimewa.


\>plot3d("x^2/(x^2+y^2+1)",color=0,hue=true,grid=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-027.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-027.png)

Permukaannya juga bisa transparan.


\>plot3d("x^2+y^2",\>transparent,grid=10,wirecolor=red):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-028.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-028.png)

# Plot Implisit

Ada juga plot implisit dalam tiga dimensi. Euler menghasilkan potongan
melalui objek. Fitur plot3d termasuk plot implisit. Plot-plot ini
menunjukkan himpunan nol dari sebuah fungsi dalam tiga variabel.


Solusi dari


$$f(x,y,z) = 0$$dapat divisualisasikan dalam potongan yang sejajar dengan bidang x-y,
bidang x-z, dan bidang y-z.


* 
implisit = 1: potong sejajar dengan bidang-y-z

* 
implicit = 2: memotong sejajar dengan bidang x-z

* 
implicit=4: memotong sejajar dengan bidang x-y


Tambahkan nilai-nilai ini, jika Anda mau. Pada contoh, kami memplot


$$M = \{ (x,y,z) : x^2+y^3+zy=1 \}$$\>plot3d("x^2+y^3+z\*y-1",r=5,implicit=3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-031.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-031.png)

\>c=1; d=1;

\>plot3d("((x^2+y^2-c^2)^2+(z^2-1)^2)\*((y^2+z^2-c^2)^2+(x^2-1)^2)\*((z^2+x^2-c^2)^2+(y^2-1)^2)-d",r=2,<frame,\>implicit,\>user): 


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-032.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-032.png)

\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-033.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-033.png)

# Memplot Data 3D

Sama seperti plot2d, plot3d menerima data. Untuk objek 3D, Anda perlu
menyediakan matriks nilai x, y, dan z, atau tiga fungsi atau ekspresi
fx(x,y), fy(x,y), fz(x,y).


$$\gamma(t,s) = (x(t,s),y(t,s),z(t,s))$$Karena x,y,z adalah matriks, kita mengasumsikan bahwa (t,s) berjalan
melalui kotak persegi. Hasilnya, Anda dapat memplot gambar persegi
panjang dalam ruang.


Anda dapat menggunakan bahasa matriks Euler untuk menghasilkan
koordinat secara efektif.


Pada contoh berikut, kita menggunakan vektor nilai t dan vektor kolom
nilai s untuk memparameterkan permukaan bola. Pada gambar kita dapat
menandai daerah, dalam kasus kita daerah kutub.


\>t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)'; ...  
\>   x=cos(s)\*cos(t); y=cos(s)\*sin(t); z=sin(s); ...  
\>   plot3d(x,y,z,\>hue, ...  
\>   color=blue,<frame,grid=[10,20], ...  
\>   values=s,contourcolor=red,level=[90°-24°;90°-22°], ...  
\>   scale=1.4,height=50°):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-035.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-035.png)

Berikut ini adalah contoh, yang merupakan grafik suatu fungsi.


\>t=-1:0.1:1; s=(-1:0.1:1)'; plot3d(t,s,t\*s,grid=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-036.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-036.png)

Namun demikian, kita bisa membuat segala macam permukaan. Berikut ini
adalah permukaan yang sama dengan fungsi


$$x = y \, z$$\>plot3d(t\*s,t,s,angle=180°,grid=10):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-038.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-038.png)

Dengan lebih banyak upaya, kita bisa menghasilkan banyak permukaan.


Dalam contoh berikut ini, kami membuat tampilan berbayang dari bola
yang terdistorsi. Koordinat yang biasa digunakan untuk bola adalah


$$\gamma(t,s) = (\cos(t)\cos(s),\sin(t)\sin(s),\cos(s))$$dengan


$$0 \le t \le 2\pi, \quad \frac{-\pi}{2} \le s \le \frac{\pi}{2}.$$Kami mengubahnya dengan sebuah faktor


$$d(t,s) = \frac{\cos(4t)+\cos(8s)}{4}.$$\>t=linspace(0,2pi,320); s=linspace(-pi/2,pi/2,160)'; ...  
\>   d=1+0.2\*(cos(4\*t)+cos(8\*s)); ...  
\>   plot3d(cos(t)\*cos(s)\*d,sin(t)\*cos(s)\*d,sin(s)\*d,hue=1, ...  
\>     light=[1,0,1],frame=0,zoom=5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-042.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-042.png)

Tentu saja, awan titik juga dimungkinkan. Untuk memplot data titik
dalam ruang, kita membutuhkan tiga vektor untuk koordinat titik.


Gaya-gayanya sama seperti pada plot2d dengan points=true;


\>n=500;  ...  
\>     plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="."):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-043.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-043.png)

Anda juga dapat memplot kurva dalam bentuk 3D. Dalam hal ini, akan
lebih mudah untuk menghitung titik-titik kurva. Untuk kurva pada
bidang, kami menggunakan urutan koordinat dan parameter wire = true.


\>t=linspace(0,8pi,500); ...  
\>   plot3d(sin(t),cos(t),t/10,\>wire,zoom=3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-044.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-044.png)

\>t=linspace(0,4pi,1000); plot3d(cos(t),sin(t),t/2pi,\>wire, ...  
\>   linewidth=3,wirecolor=blue):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-045.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-045.png)

\>X=cumsum(normal(3,100)); ...  
\>    plot3d(X[1],X[2],X[3],\>anaglyph,\>wire):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-046.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-046.png)

EMT juga dapat membuat plot dalam mode anaglyph. Untuk melihat plot
semacam itu, Anda memerlukan kacamata merah/cyan.


\> plot3d("x^2+y^3",\>anaglyph,\>contour,angle=30°):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-047.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-047.png)

Sering kali, skema warna spektral digunakan untuk plot. Hal ini
menekankan ketinggian fungsi.


\>plot3d("x^2\*y^3-y",\>spectral,\>contour,zoom=3.2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-048.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-048.png)

Euler juga dapat memplot permukaan yang diparameterkan, ketika
parameternya adalah nilai x, y, dan z dari sebuah gambar kisi-kisi
persegi panjang di dalam ruang.


Untuk demo berikut ini, kami menyiapkan parameter u dan v, dan
menghasilkan koordinat ruang dari parameter ini.


\>u=linspace(-1,1,10); v=linspace(0,2\*pi,50)'; ...  
\>   X=(3+u\*cos(v/2))\*cos(v); Y=(3+u\*cos(v/2))\*sin(v); Z=u\*sin(v/2); ...  
\>   plot3d(X,Y,Z,\>anaglyph,<frame,\>wire,scale=2.3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-049.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-049.png)

Berikut ini contoh yang lebih rumit, yang tampak megah dengan kacamata
merah/cyan.


\>u:=linspace(-pi,pi,160); v:=linspace(-pi,pi,400)';  ...  
\>   x:=(4\*(1+.25\*sin(3\*v))+cos(u))\*cos(2\*v); ...  
\>   y:=(4\*(1+.25\*sin(3\*v))+cos(u))\*sin(2\*v); ...  
\>    z=sin(u)+2\*cos(3\*v); ...  
\>   plot3d(x,y,z,frame=0,scale=1.5,hue=1,light=[1,0,-1],zoom=2.8,\>anaglyph):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-050.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-050.png)

# Plot Statistik

Plot batang juga dapat digunakan. Untuk ini, kita harus menyediakan


* 
x: vektor baris dengan n+1 elemen

* 
y: vektor kolom dengan n+1 elemen

* 
z: matriks nilai berukuran nxn.


z dapat lebih besar, tetapi hanya nilai nxn yang akan digunakan.


Pada contoh, pertama-tama kita menghitung nilainya. Kemudian kita
sesuaikan x dan y, sehingga vektor berada di tengah-tengah nilai yang
digunakan.


\>x=-1:0.1:1; y=x'; z=x^2+y^2; ...  
\>   xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05; ...  
\>   plot3d(xa,ya,z,bar=true):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-051.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-051.png)

Dimungkinkan untuk membagi plot permukaan menjadi dua bagian atau
lebih.


\>x=-1:0.1:1; y=x'; z=x+y; d=zeros(size(x)); ...  
\>   plot3d(x,y,z,disconnect=2:2:20):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-052.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-052.png)

Jika memuat atau menghasilkan matriks data M dari file dan perlu
memplotnya dalam 3D, Anda dapat menskalakan matriks ke [-1,1] dengan
scale(M), atau menskalakan matriks dengan &gt;zscale. Hal ini dapat
dikombinasikan dengan faktor penskalaan individual yang diterapkan
sebagai tambahan.


\>i=1:20; j=i'; ...  
\>   plot3d(i\*j^2+100\*normal(20,20),\>zscale,scale=[1,1,1.5],angle=-40°,zoom=1.8):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-053.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-053.png)

\>Z=intrandom(5,100,6); v=zeros(5,6); ...  
\>   loop 1 to 5; v[#]=getmultiplicities(1:6,Z[#]); end; ...  
\>   columnsplot3d(v',scols=1:5,ccols=[1:5]):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-054.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-054.png)

# Permukaan Benda Putar

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>   style="#",color=red,<outline, ...  
\>   level=[-2;0],n=100):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-055.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-055.png)

\>ekspresi &= (x^2+y^2-1)^3-x^2\*y^3; $ekspresi


$$\left(y^2+x^2-1\right)^3-x^2\,y^3$$Kami ingin memutar kurva jantung di sekitar sumbu y. Berikut ini
adalah ekspresi yang mendefinisikan jantung:


$$f(x,y)=(x^2+y^2-1)^3-x^2.y^3.$$Selanjutnya kita atur


$$x=r.cos(a),\quad y=r.sin(a).$$\>function fr(r,a) &= ekspresi with [x=r\*cos(a),y=r\*sin(a)] | trigreduce; $fr(r,a)


$$\left(r^2-1\right)^3+\frac{\left(\sin \left(5\,a\right)-\sin \left(  3\,a\right)-2\,\sin a\right)\,r^5}{16}$$Hal ini memungkinkan untuk mendefinisikan fungsi numerik, yang
menyelesaikan untuk r, jika a diberikan. Dengan fungsi tersebut kita
dapat memplotkan jantung yang diputar sebagai permukaan parametrik.


\>function map f(a) := bisect("fr",0,2;a); ...  
\>   t=linspace(-pi/2,pi/2,100); r=f(t);  ...  
\>   s=linspace(pi,2pi,100)'; ...  
\>   plot3d(r\*cos(t)\*sin(s),r\*cos(t)\*cos(s),r\*sin(t), ...  
\>   \>hue,<frame,color=red,zoom=4,amb=0,max=0.7,grid=12,height=50°):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-060.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-060.png)

Berikut ini adalah plot 3D dari gambar di atas yang diputar
mengelilingi sumbu-z. Kami mendefinisikan fungsi, yang menggambarkan
objek.


\>function f(x,y,z) ...


    r=x^2+y^2;
    return (r+z^2-1)^3-r*z^3;
     endfunction
</pre>
\>plot3d("f(x,y,z)", ...  
\>   xmin=0,xmax=1.2,ymin=-1.2,ymax=1.2,zmin=-1.2,zmax=1.4, ...  
\>   implicit=1,angle=-30°,zoom=2.5,n=[10,100,60],\>anaglyph):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-061.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-061.png)

# Plot 3D Khusus

Fungsi plot3d memang bagus untuk dimiliki, tetapi tidak memenuhi semua
kebutuhan. Selain rutinitas yang lebih mendasar, Anda juga bisa
mendapatkan plot berbingkai dari objek apa pun yang Anda sukai.


Meskipun Euler bukan program 3D, namun dapat menggabungkan beberapa
objek dasar. Kami mencoba memvisualisasikan parabola dan garis
singgungnya.


\>function myplot ...


      y=-1:0.01:1; x=(-1:0.01:1)';
      plot3d(x,y,0.2*(x-0.1)/2,<scale,<frame,>hue, ..
        hues=0.5,>contour,color=orange);
      h=holding(1);
      plot3d(x,y,(x^2+y^2)/2,<scale,<frame,>contour,>hue);
      holding(h);
    endfunction
</pre>
Sekarang framedplot() menyediakan frame, dan mengatur tampilan.


\>framedplot("myplot",[-1,1,-1,1,0,1],height=0,angle=-30°, ...  
\>     center=[0,0,-0.7],zoom=3):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-062.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-062.png)

Dengan cara yang sama, Anda dapat memplot bidang kontur secara manual.
Perhatikan bahwa plot3d() mengatur jendela ke fullwindow() secara
default, namun plotcontourplane() mengasumsikannya.


\>x=-1:0.02:1.1; y=x'; z=x^2-y^4;

\>function myplot (x,y,z) ...  
\>  
<pre class="udf">      zoom(2);
      wi=fullwindow();
      plotcontourplane(x,y,z,level="auto",<scale);
      plot3d(x,y,z,>hue,<scale,>add,color=white,level="thin");
      window(wi);
      reset();
    endfunction
</pre>
\>myplot(x,y,z):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-063.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-063.png)

# Animasi

Euler dapat menggunakan frame untuk melakukan pra-komputasi animasi.


Salah satu fungsi yang memanfaatkan teknik ini adalah rotate. Fungsi
ini dapat mengubah sudut pandang dan menggambar ulang plot 3D. Fungsi
ini memanggil addpage() untuk setiap plot baru. Akhirnya fungsi ini
menganimasikan plot tersebut.


Silakan pelajari sumber dari rotate untuk melihat lebih detail.


\>function testplot () := plot3d("x^2+y^3"); ...  
\>   rotate("testplot"); testplot():


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-064.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-064.png)

# Menggambar Povray

Dengan bantuan file Euler povray.e, Euler dapat menghasilkan file
Povray. Hasilnya sangat bagus untuk dilihat.


Anda perlu menginstal Povray (32bit atau 64bit) dari
  <a href="http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.">http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.</a>


Antarmuka Povray dari Euler menghasilkan file Povray di direktori home
pengguna, dan memanggil Povray untuk mengurai file-file ini. Nama file
default adalah current.pov, dan direktori defaultnya adalah
eulerhome(), biasanya c:\Users\Username\Euler. Povray menghasilkan
sebuah file PNG, yang dapat dimuat oleh Euler ke dalam notebook. Untuk
membersihkan berkas-berkas ini, gunakan povclear().


Fungsi pov3d memiliki semangat yang sama dengan plot3d. Fungsi ini
dapat menghasilkan grafik dari sebuah fungsi f(x,y), atau sebuah
permukaan dengan koordinat X,Y,Z dalam bentuk matriks, termasuk
garis-garis level yang bersifat opsional. Fungsi ini memulai raytracer
secara otomatis, dan memuat adegan ke dalam notebook Euler.


Selain pov3d(), ada banyak fungsi yang menghasilkan objek Povray.
Fungsi-fungsi ini mengembalikan string, yang berisi kode Povray untuk
objek. Untuk menggunakan fungsi-fungsi ini, mulai file Povray dengan
povstart(). Kemudian gunakan writeln(...) untuk menulis objek ke file
scene. Terakhir, akhiri file dengan povend(). Secara default,
raytracer akan dimulai, dan PNG akan dimasukkan ke dalam buku catatan
Euler.


Fungsi objek memiliki parameter yang disebut “look”, yang membutuhkan
string dengan kode povray untuk tekstur dan hasil akhir objek. Fungsi
povlook() dapat digunakan untuk menghasilkan string ini. Fungsi ini
memiliki parameter untuk warna, transparansi, Phong Shading, dll.


Perhatikan bahwa Povray universe memiliki sistem koordinat lain.
Antarmuka ini menerjemahkan semua koordinat ke sistem Povray. Jadi
Anda dapat tetap berpikir dalam sistem koordinat Euler dengan z yang
mengarah vertikal ke atas, dan sumbu x, y, z di tangan kanan.


Anda perlu memuat file povray.


\>load povray;


Pastikan direktori bin povray berada di dalam path. Jika tidak, edit
variabel berikut sehingga berisi jalur ke povray yang dapat
dieksekusi.


\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"


    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

Untuk kesan pertama, kita plot sebuah fungsi sederhana. Perintah
berikut ini menghasilkan file povray di direktori pengguna Anda, dan
menjalankan Povray untuk melacak sinar pada file ini.


Jika Anda memulai perintah berikut, GUI Povray akan terbuka,
menjalankan file, dan menutup secara otomatis. Karena alasan keamanan,
Anda akan ditanya, apakah Anda ingin mengizinkan file exe dijalankan.
Anda dapat menekan cancel untuk menghentikan pertanyaan lebih lanjut.
Anda mungkin harus menekan OK pada jendela Povray untuk mengetahui
dialog awal Povray.


\>plot3d("x^2+y^2",zoom=2):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-065.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-065.png)

\>pov3d("x^2+y^2",zoom=3);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-066.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-066.png)

Kita dapat membuat fungsi menjadi transparan dan menambahkan hasil
akhir lainnya. Kita juga dapat menambahkan garis level ke plot fungsi.


\>pov3d("x^2+y^3",axiscolor=red,angle=-45°,\>anaglyph, ...  
\>     look=povlook(cyan,0.2),level=-1:0.5:1,zoom=3.8);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-067.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-067.png)

Kadang-kadang perlu untuk mencegah penskalaan fungsi, dan menskalakan
fungsi dengan tangan.


Kami memplot kumpulan titik pada bidang kompleks, di mana hasil kali
jarak ke 1 dan -1 sama dengan 1.


\>pov3d("((x-1)^2+y^2)\*((x+1)^2+y^2)/40",r=2, ...  
\>     angle=-120°,level=1/40,dlevel=0.005,light=[-1,1,1],height=10°,n=50, ...  
\>     <fscale,zoom=3.8);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-068.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-068.png)

# Merencanakan dengan Koordinat

Sebagai pengganti fungsi, kita dapat membuat plot dengan koordinat.
Seperti pada plot3d, kita membutuhkan tiga matriks untuk
mendefinisikan objek.


Pada contoh, kita memutar sebuah fungsi pada sumbu z.


\>function f(x) := x^3-x+1; ...  
\>   x=-1:0.01:1; t=linspace(0,2pi,50)'; ...  
\>   Z=x; X=cos(t)\*f(x); Y=sin(t)\*f(x); ...  
\>   pov3d(X,Y,Z,angle=40°,look=povlook(red,0.1),height=50°,axis=0,zoom=4,light=[10,5,15]);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-069.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-069.png)

Pada contoh berikut, kami memplot gelombang teredam. Kami menghasilkan
gelombang dengan bahasa matriks Euler.


Kami juga menunjukkan, bagaimana objek tambahan dapat ditambahkan ke
adegan pov3d. Untuk pembuatan objek, lihat contoh berikut. Perhatikan
bahwa plot3d menskalakan plot, sehingga sesuai dengan kubus satuan.


\>r=linspace(0,1,80); phi=linspace(0,2pi,80)'; ...  
\>   x=r\*cos(phi); y=r\*sin(phi); z=exp(-5\*r)\*cos(8\*pi\*r)/3;  ...  
\>   pov3d(x,y,z,zoom=6,axis=0,height=30°,add=povsphere([0.5,0,0.25],0.15,povlook(red)), ...  
\>     w=500,h=300);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-070.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-070.png)

Dengan metode bayangan canggih Povray, hanya sedikit titik yang bisa
menghasilkan permukaan yang sangat halus. Hanya pada batas-batas dan
bayangan, trik ini bisa terlihat jelas.


Untuk itu, kita perlu menambahkan vektor normal di setiap titik
matriks.


\>Z &= x^2\*y^3


    
                                     2  3
                                    x  y
    

Persamaan permukaannya adalah [x,y,Z]. Kami menghitung dua turunan
terhadap x dan y dari persamaan ini dan mengambil hasil perkalian
silang sebagai normal.


\>dx &= diff([x,y,Z],x); dy &= diff([x,y,Z],y);


Kami mendefinisikan normal sebagai hasil kali silang dari turunan ini,
dan mendefinisikan fungsi koordinat.


\>N &= crossproduct(dx,dy); NX &= N[1]; NY &= N[2]; NZ &= N[3]; N,


    
                                   3       2  2
                           [- 2 x y , - 3 x  y , 1]
    

Kita hanya menggunakan 25 point.


\>x=-1:0.5:1; y=x';

\>pov3d(x,y,Z(x,y),angle=10°, ...  
\>     xv=NX(x,y),yv=NY(x,y),zv=NZ(x,y),<shadow);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-071.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-071.png)

Berikut ini adalah simpul Trefoil yang dibuat oleh A. Busser di
Povray. Ada versi yang lebih baik dari ini dalam contoh.


  <a href="Examples\Trefoil Knot.html">Trefoil Knot</a>  

Untuk tampilan yang bagus dengan tidak terlalu banyak titik, kita
tambahkan vektor normal di sini. Kita menggunakan Maxima untuk
menghitung normal untuk kita. Pertama, tiga fungsi untuk koordinat
sebagai ekspresi simbolik.


\>X &= ((4+sin(3\*y))+cos(x))\*cos(2\*y); ...  
\>   Y &= ((4+sin(3\*y))+cos(x))\*sin(2\*y); ...  
\>   Z &= sin(x)+2\*cos(3\*y);


Kemudian dua vektor turunan terhadap x dan y.


\>dx &= diff([X,Y,Z],x); dy &= diff([X,Y,Z],y);


Sekarang yang normal, yang merupakan produk silang dari dua turunan.


\>dn &= crossproduct(dx,dy);


Kami sekarang mengevaluasi semua ini secara numerik.


\>x:=linspace(-%pi,%pi,40); y:=linspace(-%pi,%pi,100)';


Vektor normal adalah evaluasi dari ekspresi simbolik dn[i] untuk
i=1,2,3. Sintaks untuk ini adalah &amp;“ekspresi”(parameter). Ini adalah
sebuah alternatif dari metode pada contoh sebelumnya, di mana kita
mendefinisikan ekspresi simbolik NX, NY, NZ terlebih dahulu.


\>pov3d(X(x,y),Y(x,y),Z(x,y),\>anaglyph,axis=0,zoom=5,w=450,h=350, ...  
\>     <shadow,look=povlook(blue), ...  
\>     xv=&"dn[1]"(x,y), yv=&"dn[2]"(x,y), zv=&"dn[3]"(x,y));


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-072.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-072.png)

Kami juga dapat menghasilkan kisi-kisi dalam bentuk 3D.


\>povstart(zoom=4); ...  
\>   x=-1:0.5:1; r=1-(x+1)^2/6; ...  
\>   t=(0°:30°:360°)'; y=r\*cos(t); z=r\*sin(t); ...  
\>   writeln(povgrid(x,y,z,d=0.02,dballs=0.05)); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-073.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-073.png)

Dengan povgrid(), kurva dapat dibuat.


\>povstart(center=[0,0,1],zoom=3.6); ...  
\>   t=linspace(0,2,1000); r=exp(-t); ...  
\>   x=cos(2\*pi\*10\*t)\*r; y=sin(2\*pi\*10\*t)\*r; z=t; ...  
\>   writeln(povgrid(x,y,z,povlook(red))); ...  
\>   writeAxis(0,2,axis=3); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-074.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-074.png)

# Objek Povray

Di atas, kami menggunakan pov3d untuk memplot permukaan. Antarmuka
povray di Euler juga dapat menghasilkan objek Povray. Objek-objek ini
disimpan sebagai string di Euler, dan perlu ditulis ke file Povray.


Kita memulai output dengan povstart().


\>povstart(zoom=4);


Pertama, kita mendefinisikan tiga silinder, dan menyimpannya dalam
bentuk string di Euler.


Fungsi povx() dll. hanya mengembalikan vektor [1,0,0], yang dapat
digunakan sebagai gantinya.


\>c1=povcylinder(-povx,povx,1,povlook(red)); ...  
\>   c2=povcylinder(-povy,povy,1,povlook(yellow)); ...  
\>   c3=povcylinder(-povz,povz,1,povlook(blue)); ...  
\>  
String berisi kode Povray, yang tidak perlu kita pahami pada saat itu.


\>c2


    cylinder { &lt;0,0,-1&gt;, &lt;0,0,1&gt;, 1
     texture { pigment { color rgb &lt;0.941176,0.941176,0.392157&gt; }  } 
     finish { ambient 0.2 } 
     }

Seperti yang Anda lihat, kami menambahkan tekstur ke objek dalam tiga
warna berbeda.


Hal ini dilakukan dengan povlook(), yang mengembalikan sebuah string
dengan kode Povray yang relevan. Kita dapat menggunakan warna default
Euler, atau menentukan warna kita sendiri. Kita juga dapat menambahkan
transparansi, atau mengubah cahaya sekitar.


\>povlook(rgb(0.1,0.2,0.3),0.1,0.5)


     texture { pigment { color rgbf &lt;0.101961,0.2,0.301961,0.1&gt; }  } 
     finish { ambient 0.5 } 
    

Sekarang kita mendefinisikan objek perpotongan, dan menulis hasilnya
ke file.


\>writeln(povintersection([c1,c2,c3]));


Perpotongan tiga silinder sulit untuk divisualisasikan, jika Anda
belum pernah melihatnya.


\>povend;


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-075.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-075.png)

Fungsi-fungsi berikut ini menghasilkan fraktal secara rekursif.


Fungsi pertama menunjukkan, bagaimana Euler menangani objek Povray
sederhana. Fungsi povbox() mengembalikan sebuah string, yang berisi
koordinat kotak, tekstur dan hasil akhir.


\>function onebox(x,y,z,d) := povbox([x,y,z],[x+d,y+d,z+d],povlook());

\>function fractal (x,y,z,h,n) ...  
\>  
<pre class="udf">     if n==1 then writeln(onebox(x,y,z,h));
     else
       h=h/3;
       fractal(x,y,z,h,n-1);
       fractal(x+2*h,y,z,h,n-1);
       fractal(x,y+2*h,z,h,n-1);
       fractal(x,y,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z,h,n-1);
       fractal(x+2*h,y,z+2*h,h,n-1);
       fractal(x,y+2*h,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z+2*h,h,n-1);
       fractal(x+h,y+h,z+h,h,n-1);
     endif;
    endfunction
</pre>
\>povstart(fade=10,<shadow);

\>fractal(-1,-1,-1,2,4);

\>povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-076.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-076.png)

Perbedaan memungkinkan pemotongan satu objek dari objek lainnya.
Seperti persimpangan, ada bagian dari objek CSG Povray.


\>povstart(light=[5,-5,5],fade=10);


Untuk demonstrasi ini, kita akan mendefinisikan sebuah objek di
Povray, alih-alih menggunakan sebuah string di Euler. Definisi akan
langsung dituliskan ke file.


Koordinat kotak -1 berarti [-1,-1,-1].


\>povdefine("mycube",povbox(-1,1));


Kita dapat menggunakan objek ini dalam povobject(), yang mengembalikan
sebuah string seperti biasa.


\>c1=povobject("mycube",povlook(red));


Kami menghasilkan kubus kedua, dan memutar serta menskalakannya
sedikit.


\>c2=povobject("mycube",povlook(yellow),translate=[1,1,1], ...  
\>     rotate=xrotate(10°)+yrotate(10°), scale=1.2);


Kemudian kita ambil selisih dari kedua objek tersebut.


\>writeln(povdifference(c1,c2));


Sekarang tambahkan tiga sumbu.


\>writeAxis(-1.2,1.2,axis=1); ...  
\>   writeAxis(-1.2,1.2,axis=2); ...  
\>   writeAxis(-1.2,1.2,axis=4); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-077.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-077.png)

# Fungsi Implisit

Povray dapat memplot himpunan di mana f(x,y,z)=0, seperti parameter
implisit di plot3d. Namun, hasilnya terlihat jauh lebih baik.


Sintaks untuk fungsi-fungsi ini sedikit berbeda. Anda tidak dapat
menggunakan output dari ekspresi Maxima atau Euler.


$$((x^2+y^2-c^2)^2+(z^2-1)^2)*((y^2+z^2-c^2)^2+(x^2-1)^2)*((z^2+x^2-c^2)^2+(y^2-1)^2)=d$$\>povstart(angle=70°,height=50°,zoom=4);

\>c=0.1; d=0.1; ...  
\>   writeln(povsurface("(pow(pow(x,2)+pow(y,2)-pow(c,2),2)+pow(pow(z,2)-1,2))\*(pow(pow(y,2)+pow(z,2)-pow(c,2),2)+pow(pow(x,2)-1,2))\*(pow(pow(z,2)+pow(x,2)-pow(c,2),2)+pow(pow(y,2)-1,2))-d",povlook(red))); ...  
\>   povend();


    Error : Povray error!
    
    Error generated by error() command
    
    povray:
        error("Povray error!");
    Try "trace errors" to inspect local variables after errors.
    povend:
        povray(file,w,h,aspect,exit); 

\>povstart(angle=25°,height=10°); 

\>writeln(povsurface("pow(x,2)+pow(y,2)\*pow(z,2)-1",povlook(blue),povbox(-2,2,"")));

\>povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-079.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-079.png)

\>povstart(angle=70°,height=50°,zoom=4);


Membuat permukaan implisit. Perhatikan sintaks yang berbeda dalam
ekspresi.


\>writeln(povsurface("pow(x,2)\*y-pow(y,3)-pow(z,2)",povlook(green))); ...  
\>   writeAxes(); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-080.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-080.png)

# Objek Jaring

Pada contoh ini, kami menunjukkan cara membuat objek mesh, dan
menggambarnya dengan informasi tambahan.


Kami ingin memaksimalkan xy di bawah kondisi x+y = 1 dan
mendemonstrasikan sentuhan tangensial dari garis level.


\>povstart(angle=-10°,center=[0.5,0.5,0.5],zoom=7);


Kita tidak dapat menyimpan objek dalam sebuah string seperti
sebelumnya, karena ukurannya terlalu besar. Jadi kita mendefinisikan
objek dalam file Povray menggunakan #declare. Fungsi povtriangle()
melakukan hal ini secara otomatis. Fungsi ini dapat menerima vektor
normal seperti halnya pov3d().


Berikut ini mendefinisikan objek mesh, dan menuliskannya langsung ke
dalam file.


\>x=0:0.02:1; y=x'; z=x\*y; vx=-y; vy=-x; vz=1;

\>mesh=povtriangles(x,y,z,"",vx,vy,vz);


Sekarang kita tentukan dua cakram, yang akan berpotongan dengan
permukaan.


\>cl=povdisc([0.5,0.5,0],[1,1,0],2); ...  
\>   ll=povdisc([0,0,1/4],[0,0,1],2);


Tuliskan permukaan dikurangi kedua cakram.


\>writeln(povdifference(mesh,povunion([cl,ll]),povlook(green)));


Tuliskan kedua perpotongan tersebut.


\>writeln(povintersection([mesh,cl],povlook(red))); ...  
\>   writeln(povintersection([mesh,ll],povlook(gray)));


Tulislah satu titik secara maksimal.


\>writeln(povpoint([1/2,1/2,1/4],povlook(gray),size=2\*defaultpointsize));


Tambahkan sumbu dan selesaikan.


\>writeAxes(0,1,0,1,0,1,d=0.015); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-081.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-081.png)

# Anaglyph dalam Povray

Untuk menghasilkan anaglyph untuk kacamata merah/cyan, Povray harus
dijalankan dua kali dari posisi kamera yang berbeda. Ini menghasilkan
dua file Povray dan dua file PNG, yang dimuat dengan fungsi
loadanaglyph().


Tentu saja, Anda membutuhkan kacamata merah/cyan untuk melihat contoh
berikut dengan benar.


Fungsi pov3d() memiliki tombol sederhana untuk menghasilkan anaglyph.


\>pov3d("-exp(-x^2-y^2)/2",r=2,height=45°,\>anaglyph, ...  
\>     center=[0,0,0.5],zoom=3.5);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-082.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-082.png)

Jika Anda membuat scene dengan objek, Anda harus menempatkan pembuatan
scene ke dalam suatu fungsi, dan menjalankannya dua kali dengan nilai
yang berbeda untuk parameter anaglyph.


\>function myscene ...


      s=povsphere(povc,1);
      cl=povcylinder(-povz,povz,0.5);
      clx=povobject(cl,rotate=xrotate(90°));
      cly=povobject(cl,rotate=yrotate(90°));
      c=povbox([-1,-1,0],1);
      un=povunion([cl,clx,cly,c]);
      obj=povdifference(s,un,povlook(red));
      writeln(obj);
      writeAxes();
    endfunction
</pre>
Fungsi povanaglyph() melakukan semua ini. Parameter-parameternya
seperti pada povstart() dan povend() yang digabungkan.


\>povanaglyph("myscene",zoom=4.5);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-083.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-083.png)

# Mendefinisikan Objek sendiri

Antarmuka povray Euler berisi banyak objek. Namun Anda tidak dibatasi
pada objek-objek tersebut. Anda dapat membuat objek sendiri, yang
menggabungkan objek-objek lain, atau objek yang benar-benar baru.


Kami mendemonstrasikan sebuah torus. Perintah Povray untuk ini adalah
“torus”. Jadi kita mengembalikan sebuah string dengan perintah ini dan
parameternya. Perhatikan bahwa torus selalu berpusat pada titik asal.


\>function povdonat (r1,r2,look="") ...


      return "torus {"+r1+","+r2+look+"}";
    endfunction
</pre>
Inilah torus pertama kami.


\>t1=povdonat(0.8,0.2)


    torus {0.8,0.2}

Mari kita gunakan objek ini untuk membuat torus kedua, ditranslasikan
dan diputar.


\>t2=povobject(t1,rotate=xrotate(90°),translate=[0.8,0,0])


    object { torus {0.8,0.2}
     rotate 90 *x 
     translate &lt;0.8,0,0&gt;
     }

Sekarang, kita tempatkan semua benda ini ke dalam suatu pemandangan.
Untuk tampilannya, kami menggunakan Phong Shading.


\>povstart(center=[0.4,0,0],angle=0°,zoom=3.8,aspect=1.5); ...  
\>   writeln(povobject(t1,povlook(green,phong=1))); ...  
\>   writeln(povobject(t2,povlook(green,phong=1))); ...  
\>  
 &gt;povend();  

calls the Povray program. However, in case of errors, it does not
display the error. You should therefore use


 &gt;povend(&lt;exit);  

if anything did not work. This will leave the Povray window open.


\>povend(h=320,w=480);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-084.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-084.png)

Berikut adalah contoh yang lebih rumit. Kami menyelesaikan


lateks: Ax \le b, \quad x \ge 0, \quad c.x \to \text{Max.}latex: Ax
\le b, \quad x \ge 0, \quad c.x \to \text{Max.}


dan menunjukkan titik-titik yang layak dan optimal dalam plot 3D.


\>A=[10,8,4;5,6,8;6,3,2;9,5,6];

\>b=[10,10,10,10]';

\>c=[1,1,1];


Pertama, mari kita periksa, apakah contoh ini memiliki solusi atau
tidak.


\>x=simplex(A,b,c,\>max,\>check)'


    [0,  1,  0.5]

Ya, benar.


Selanjutnya kita mendefinisikan dua objek. Yang pertama adalah pesawat


$$a \cdot x \le b$$\>function oneplane (a,b,look="") ...


      return povplane(a,b,look)
    endfunction
</pre>
Kemudian kita tentukan perpotongan semua setengah ruang dan kubus.


\>function adm (A, b, r, look="") ...


      ol=[];
      loop 1 to rows(A); ol=ol|oneplane(A[#],b[#]); end;
      ol=ol|povbox([0,0,0],[r,r,r]);
      return povintersection(ol,look);
    endfunction
</pre>
Sekarang, kita bisa merencanakan adegan tersebut.


\>povstart(angle=120°,center=[0.5,0.5,0.5],zoom=3.5); ...  
\>   writeln(adm(A,b,2,povlook(green,0.4))); ...  
\>   writeAxes(0,1.3,0,1.6,0,1.5); ...  
\>  
Berikut ini adalah lingkaran di sekeliling optimal.


\>writeln(povintersection([povsphere(x,0.5),povplane(c,c.x')], ...  
\>     povlook(red,0.9)));


Dan kesalahan pada arah yang optimal.


\>writeln(povarrow(x,c\*0.5,povlook(red)));


Kami menambahkan teks ke layar. Teks hanyalah sebuah objek 3D. Kita
perlu menempatkan dan memutarnya sesuai dengan pandangan kita.


\>writeln(povtext("Linear Problem",[0,0.2,1.3],size=0.05,rotate=5°)); ...  
\>   povend();


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-086.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Plot%203D-086.png)

# Contoh Lainnya

Anda dapat menemukan beberapa contoh lain untuk Povray di Euler dalam
file-file berikut.


  <a href="Examples/Dandelin Spheres.html">Examples/Dandelin Spheres</a>  

  <a href="Examples/Donat Math.html">Examples/Donat Math</a>  

  <a href="Examples/Trefoil Knot.html">Examples/Trefoil Knot</a>  

  <a href="Examples/Optimization by Affine Scaling.html">Examples/Optimization by Affine Scaling</a>  



# Soal plot 3D 1. Grafik dengan ekspresi langsung 

$$x^3+2y$$\>plot3d("x^3+2\*y",distance=3,zoom=1,angle=pi/2,height=0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-002.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-002.png)

plot 3d dengan ekspresi


$$x^3+2y$$

akan membentuk grafik tersebut dengan jarak 3, pembesaran 1 kali,
kemiringan pi/2, dan ketinggian 0


# Grafik dengan menyimpan variabel 

$$f(x)=x^2+3y$$\>function f(x,y):= x^2+3\*y

\>x=3; plot3d("f",0,1,0,distance=3,zoom=2,angle=pi,height=0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-005.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-005.png)

plot 3d dengan ekspresi


$$x^2+3y$$

akan membentuk grafik tersebut dengan jarak 3, pembesaran 2 kali,
kemiringan pi, dan ketinggian 0


# Grafik dengan numerik

$$g(x)= x^2+y^2$$\>function g(x, y) := x^2 + y^2 

\>plot3d("g", -10, 10, -10, 10, distance=3, zoom=1, angle=pi/4, height=0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-008.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-008.png)

plot 3d dengan ekspresi


$$x^2+y^2$$

akan membentuk grafik tersebut skala sumbu -10, 10, -10, 10 dengan
jarak 3, pembesaran 1 kali, kemiringan pi/4, dan ketinggian 0


# Grafik dengan simbolik

$$h(x)=xsin(x) + cos(y)$$\>function h(x,y):= x\*sin(x)+cos(y)

\>plot3d("h", -10, 10, -10, 10, distance=3, zoom=1, angle=pi, height=0):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-011.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-011.png)

plot 3d dengan ekspresi


$$h(x)=xsin(x) + cos(y)$$akan membentuk grafik tersebut skala sumbu -10, 10, -10, 10 dengan
jarak 3, pembesaran 1 kali, kemiringan pi, dan ketinggian 0


# Menggambar Data x, y, z ruang 3D dengan menggambar titik di dalamnya

\>n=500; ...  
\>    plot3d(normal(2,n),normal(2,n),normal(2,n),points=true,style="+"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-013.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-013.png)

Fungsi ini menghasilkan vektor dari 500 titik acak yang diambil dari
distribusi normal dengan rata-rata 0 dan standar deviasi 1. Distribusi
normal menghasilkan angka acak yang tersebar dalam bentuk lonceng
(bell curve) dengan sebagian besar angka mendekati nol, tetapi
beberapa angka bisa lebih besar atau lebih kecil.


# Grafik interaktif 

$$x^4+6y^3$$\>plot3d("exp(-x^4+6\*y^3)",\>user, ...  
\>    title="Turn with the vector keys (press return to finish)"):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-015.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-015.png)

plot interaktif menggunakan user untuk bisa mengubah sudut pandang
yang ada sesuai keinginan sehingga tekan enter untuk mengimport
gambarnya


# Grafik Implisit

\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-016.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-016.png)

$$x^2+y^2+4xz^3$$

Grafik implisit dengan 3 variabel ditambahankan "implisit" dengan
skala grafik 2 dan pembesaran 2.5 kali


# Menggambar tampilan, warna dan sudut pandang serta kontur

\>plot3d("exp(x^2\*y)",angle=100°,\>contour,color=green):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-018.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-018.png)

$$x^2y$$Kita bisa mengatur sudut pandang dengan angle contohnya 100, serta
diberi kontur yang isinya warna hijau


# Grafik anaglitif

$$2x^6+2y^2$$\> plot3d("2\*x^6+2\*y^2",\>anaglyph,\>contour,angle=30°):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-021.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-021.png)

EMT dapat memunculkan anaglitif juga yang bisa dilihat dengan kacamata
merah/cyan


# Membuat grafik batang

\>x=-1:0.1:1; y=x'; z=x^2+y^2;

\>xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05;


\>plot3d(xa,ya,z,bar=true):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-022.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-022.png)

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>  
kita tentukan dulu bentuk grafiknya dengan nilai x y z dan berikan
skala yang ada


# Permukaan benda putar

\>style=".",color=blue,<outline, ...  
\>   level=[-1;0],n=250):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-023.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-023.png)

style . dengan warna biru dan di beri outline


level=[-1;0]: Menunjukkan bahwa plot akan menampilkan nilai dalam
rentang dari -1 hingga 0, kemungkinan merujuk pada nilai z atau
tingkat ketinggian dari objek yang diplot dalam ruang 3D.


# Grafik Povray

\>load povray;

\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"


    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

\>pov3d("-x^4+2\*y^2",zoom=3,angle=pi/2);


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-024.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-024.png)

povray akan menghasilkan bentuk yang lebih bagus seperti 3d nyata
dengan memasukkan load povray yang harus di install terlebih dahulu
dengan rumus 


$$-x^4+2y^2$$pembesaran 3 kali dan kemiringan pi/2


<pre class="udf">    
    
    
    endfunction
</pre>
    Wrong argument.
    Cannot use a string here.
    
    f3dimplicit:
        solidhuecontour((W-xm)*ff,(y-ym)*ff,(z'-zm)*ff,0,(x[#]-xm)*ff ...
    Try "trace errors" to inspect local variables after errors.
    plot3d:
        =contourcolor,=contourwidth);

    Commands must be separated by semicolon or comma!
    Found: ’; plot3d(r*cos(t)*sin(s),r*cos(t)*cos(s),r*sin(t), &gt;hue,&lt;frame,color=red,zoom=4,amb=0,max=0.7,grid=12,height=50°): (character -110)
    You can disable this in the Options menu.
    Error in:
    ... e(-pi/2,pi/2,100); r=f(t); s=linspace(pi,2pi,100)’; plot3d(r*c ...
                                                         ^

    Commands must be separated by semicolon or comma!
    Found: ’; x=cos(s)*cos(t); y=cos(s)*sin(t); z=sin(s); plot3d(x,y,z,&gt;hue, color=blue,&lt;frame,grid=[10,20], values=s,contourcolor=red,level=[90°-24°;90°-22°], scale=1.4,height=50°): (character -110)
    You can disable this in the Options menu.
    Error in:
    t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)’; x=cos(s)*co ...
                                                    ^

\>t=-1:0.1:1; s=(-1:0.1:1)’; plot3d(t,s,t\*s,grid=10):


    Commands must be separated by semicolon or comma!
    Found: ’; plot3d(t,s,t*s,grid=10): (character -110)
    You can disable this in the Options menu.
    Error in:
    t=-1:0.1:1; s=(-1:0.1:1)’; plot3d(t,s,t*s,grid=10): ...
                            ^

\>n=500; ...  
\>    plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="."):


![images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-026.png](images/23030630058_Nur%20Muhammad%20Al%20Fahamiey_Soal%20Plot%203D-026.png)



# Kalkulus dengan EMT

Materi Kalkulus mencakup di antaranya:


1. Fungsi(fungsi aljabar, trigonometri, eksponensial, logaritma,
komposisi fungsi)


2. Limit Fungsi


3. Turunan Fungsi


4. Integral Tak Tentu


5. Integral Tentu


6. Barisan dan Deret


7. Fungsi multivariabel


EMT (bersama Maxima) dapat digunakan untuk melakukan semua perhitungan
di dalam kalkulus, baik secara numerik maupun analitik (eksak).


# 1. Fungsi

Fungsi adalah suatu relasi yang menghubungkan setiap anggota dari
suatu himpunan (domain) dengan tepat satu anggota himpunan lain
(kodomain). Secara sederhana, fungsi dapat dipandang sebagai mesin
yang menerima input (nilai x) dan menghasilkan output (nilai y).


$$f: A \to B$$## Sifat-sifat Fungsi

1. Injektif (satu-satu)


Fungsi injektif adalah fungsi degan tiap elemen kondomain tidak
memiliki lebih dari satu elemen domain. Fungsi injektif disebut juga
dengan "fungsi satu-satu" karena tiap elemen kodomain hanya boleh
berelasi satu kali.


2. Surjektif


Fungsi surjektif adalah fungsi dengan semua elemen kodomain berelasi
dengan elemen domain. Fungsi surjektif juga disebut fungsi "on-to".


3. Bijektif


Fungsi bijektif adalah fungsi yang memenuhi sifat injektif dan
surjektif. Fungsi bijektif juga disebut fungsi korespondensi
satu-satu, karena elemen domain dan kodomain semuanya berelasi
satu-satu.


## Jenis Fungsi yang akan Dielajari

1. Fungsi Aljabar


Fungsi aljabar adalah jenis fungsi matematika yang dibentuk dengan
menggunakan operasi-operasi aljabar seperti penjumlahan, pengurangan,
perkalian, pembagian, dan pangkat. Secara umum, fungsi aljabar
merupakan fungsi yang dapat dinyatakan dengan ekspresi aljabar yang
melibatkan variabel dan konstanta. Fungsi ini termasuk di dalam
kategori fungsi elementer karena bisa dinyatakan dalam bentuk dasar.


2. Fungsi Trigonometri


Fungsi trigonometri adalah fungsi yang menghubungkan sudut suatu
segitiga siku-siku dengan rasio panjang sisi-sisinya. Fungsi ini
sangat penting dalam matematika, khususnya dalam geometri, analisis,
dan aplikasi di bidang fisika, teknik, dan astronomi. Fungsi-fungsi
trigonometri yang paling umum adalah sinus, kosinus, tangen, serta
turunan dan kebalikannya seperti secan, kosekan, dan kotangen.


3. Fungsi Eksponensial


Fungsi eksponensial adalah fungsi matematika di mana variabel
independen (biasanya dilambangkan dengan x) berada di eksponen. Bentuk
umum fungsi eksponensial adalah:


$$f(x)=a^x$$* 
a adalah bilangan positif (basis) dan tidak sama dengan 1

* 
x adalah variabel eksponen


Fungsi eksponensial yang paling umum adalah fungsi eksponensial alami
dengan basis bilangan euler (e = 2.718). Fungsi ini sering digunakan
dalam berbagai aplikasi ilmiah yang dinyatakan sebagai:


$$f(x)=e^x$$4. Fungsi Logaritma


Fungsi logaritma adalah kebalikan atau invers dari fungsi
eksponensial. Fungsi logaritma dinyatakan sebagai:


$$f(x)= \log a(x)$$5. Komposisi Fungsi


Komposisi fungsi adalah operasi matematika di mana dua fungsi
digabungkan sehingga output dari satu fungsi menjadi input dari fungsi
yang lain.


Misal, diketahui f dan g dua fungsi sebarang maka fungsi komposisi f
dan g ditulis


$$g o f$$

didefinisikan sebagai:


$$(g o f)(x) = g(f(x))$$sehingga fungsi f dikerjakan terlebih dahulu daripada g.


## Mendefinisikan Fungsi

Terdapat beberapa cara mendefinisikan fungsi pada EMT, yakni:


* 
Menggunakan format nama_fungsi := rumus fungsi (fungsi numerik),

* 
Menggunakan format nama_fungsi &amp;= rumus fungsi (fungsi simbolik,
* namun dapat dihitung secara numerik),

* 
Menggunakan format nama_fungsi &amp;&amp;= rumus fungsi(fungsi simbolik
* murni, tidak dapat dihitung langsung),

* 
Fungsi sebagai program EMT (Mendefinisikan fungsi yang lebih
* kompleks dengan beberapa langkah atau percabangan)


Setiap format harus diawali dengan perintah function (bukan sebagai
ekspresi).


Berikut adalah adalah beberapa contoh cara mendefinisikan fungsi:


$$f(x)=2x^2+e^{\sin(x)}.$$\>function f(x) := 2\*x^2+exp(sin(x)) // fungsi numerik 


fungsi ini mendefinisikan nilai dari f(x) dan untuk fungsi exp(cox(x))
merupakan dua fungsi dimana:


cos(x)  digunakan untuk menghitung nilai cos di sudut x dan exp()
digunakan untuk mendefinisikan fungsi eksponensial (e pangkat)


\>f(0), f(1), f(pi)


    1
    4.31977682472
    20.7392088022

\>f(a) // tidak dapat dihitung nilainya karena bukan fungsi numerik


    Wrong argument.
    Cannot use a string here.
    
    Error in ^
    Try "trace errors" to inspect local variables after errors.
    f:
        useglobal; return 2*x^2+exp(sin(x))  
    Error in:
    f(a) // tidak dapat dihitung nilainya karena bukan fungsi nume ...
        ^

\>function f(x) := 3\*x^3+exp(cos(x))  

\>f(1)


    4.71652569955

\>f(2)


    24.6595834124

\>f(-2:2)


    [-23.3404,  -1.28347,  2.71828,  4.71653,  24.6596]

\>f(-2)-f(2)


    -48

\>plot2d("f(x)",-2,2):


plot2d : fungsi ini digunakan untuk printah membuat plot dua dimensi


"f(x)" : memanggil fungsi f(x)


-2,2   : grafik akan ditampilkan pada sb x dari rentang -2 sampai 2


Berikutnya kita definisikan fungsi:


$$g(x)=\frac{\sqrt{x^2-3x}}{x+1}$$\>function g(x) := sqrt(x^2-3\*x)/(x+1)

\>g(5)


    0.527046276695

\>g(20)


    0.878051853076

\>g(21)


    0.883737367965

\>g(20:25)


    [0.878052,  0.883737,  0.888915,  0.89365,  0.897998,  0.902003]

Silakan Anda plot grafik fungsi di atas!


\>aspect(1.5); plot2d("g(x)",20,25):

\>f(g(5)) // komposisi fungsi


    2.81254111152

f(g(5)) adalah notasi yang menunjukkan komposisi fungsi.


Ini berarti kita akan melakukan dua langkah perhitungan:


Hitung g(5): Pertama, kita mencari nilai dari fungsi g ketika x = 5.


Hasilnya akan kita sebut sebagai a.


Hitung f(a): Selanjutnya, kita masukkan nilai a yang kita dapatkan
dari langkah 1 ke dalam fungsi f.


Hasil akhir dari perhitungan ini adalah nilai dari f(g(5)).


\>g(f(5))


    0.993366510057

\>function h(x) := f(g(x)) // definisi komposisi fungsi 

\>h(5) // sama dengan f(g(5))


    2.81254111152

Silakan Anda plot kurva fungsi komposisi fungsi f dan g:


$$h(x)=f(g(x))$$dan


$$u(x)=g(f(x))$$bersama-sama kurva fungsi f dan g dalam satu bidang koordinat.


\>f(0:10) // nilai-nilai f(0), f(1), f(2), ..., f(10)


    [2.71828,  4.71653,  24.6596,  81.3716,  192.52,  376.328,  650.612,
    1031.13,  1536.86,  2187.4,  3000.43]

\>fmap(0:10) // sama dengan f(0:10), berlaku untuk semua fungsi


    [2.71828,  4.71653,  24.6596,  81.3716,  192.52,  376.328,  650.612,
    1031.13,  1536.86,  2187.4,  3000.43]

\>gmap(20:25)


    [0.878052,  0.883737,  0.888915,  0.89365,  0.897998,  0.902003]

Misalkan kita akan mendefinisikan fungsi


$$f(x) = \begin{cases} x^3 & x>0 \\ x^2 & x\le 0. \end{cases}$$Fungsi tersebut tidak dapat didefinisikan sebagai fungsi numerik
secara "inline" menggunakan format :=, melainkan didefinisikan sebagai
program. Perhatikan, kata "map" digunakan agar fungsi dapat menerima
vektor sebagai input, dan hasilnya berupa vektor. Jika tanpa kata
"map" fungsinya hanya dapat menerima input satu nilai.


\>function map f(x)


      if x>0 then return x^3
      else return x^2
      endif;
    endfunction
</pre>
\>f(4)


    64

\>f(-2)


    4

\>f(-5:5)


    [25,  16,  9,  4,  1,  0,  1,  8,  27,  64,  125]

\>aspect(1.5); plot2d("f(x)",-5,5):


![images/EMTKalkulus_kelompok%204-012.png](images/EMTKalkulus_kelompok%204-012.png)

\>function f(x) &= 2\*E^x; // fungsi simbolik

\>$f(a) // nilai fungsi secara simbolik


$$2\,e^{a}$$\>function a:=12

\>f(a)


    325509.582838

\>f(E) // nilai fungsi berupa bilangan desimal


    30.308524483

\>function g(x) &= 3\*x+1


    
                                   3 x + 1
    

\>g(50)


    151

\>function h(x) &= f(g(x)) // komposisi fungsi


    
                                     3 x + 1
                                  2 E
    

\>plot2d("h(x)",-1,1):


![images/EMTKalkulus_kelompok%204-014.png](images/EMTKalkulus_kelompok%204-014.png)

## Contoh Fungsi Aljabar

1.Diberikan fungsi:


$$f(x) = 6x^3+12\sqrt x$$Tentukan nilai f(1) dan f(4) kemudian cari nilai f(4)-2f(1)


Gambarkan juga grafiknya di f(1:4)!


\>function f(x) := 6\*x^3+12\*sqrt(x)

\>f(1)


    18

\>f(4)


    408

\>f(4)-2\*f(1)


    372

\>aspect(1.5); plot2d("f",1,4):


2. Diberikan fungsi:


$$k(x,y)= 12x^3+4y^2-3x+2$$Tentukan nilai k(1,1)+k(2,3)!


\>function k(x,y):= 12\*x^3+4\*y^2-3\*x+2

\>k(1,1)


    15

\>k(2,3)


    128

\>k(1,1)+k(2,3)


    143

3. Diketahui suatu fungsi f(x,y,z) diddefinisikan sebagai betrikut


$$f(x,y,z)=(3x-1)+\sqrt{x^3-y^2-z+6}$$Tentukan nilai f(3,4,5)!


\>function f(x,y,z):= (3\*x-1)+ sqrt(x^3-y^2-z+6)

\>f(3,4,5)


    11.4641016151

## Contoh Fungsi Trigonometri

1. Suatu fungsi trigonometri didefinisikan sebagai:


$$f(x)=\frac{tan(x)}{2x+3x^2}$$Tentukan nilai dari f(6)-f(7)!


\>function f(x):= tan(x)/2\*x+3\*x^2

\>f(6)-f(7)


    -42.9230865137

2. Diberikan fungsi:


$$f(x,y)=\frac{x^2+sin(y)}{xy}$$

Tentukan nilai f(4)!


\>function f(x,y) := x^2+sin(x)/x\*y

\>f(4,2)


    15.6215987523

\>plot3d("f",-4,4):


3. Diberikan suatu fungsi


$$f(x,y,z)=\frac{sin(x)}{cos(z)+sin(x)}+tan(y)$$tentukan nilai f(x,y,z) bila x=1, y=2, dan z=-3!


\>function f(x,y,z)&= sin(x)/(sin(x)+cos(z))+tan(y)

\>f(1,2,-3)


    -7.85069041214

## Contoh Fungsi Eksponensial

1. Diberikan sebuah fungsi f(x) sebagai berikut:


$$f(x)=3^x$$Tentukan nilai f(x+1)-f(x)!


\>function f(x)&= 3^x;

\>$f(x+1)


$$3^{x+1}$$\>$f(x)


$$3^{x}$$\>$f(x+1)-f(x)


$$2\,3^{x}$$2. Fungsi f(m) didefinisikan sebagai:


$$f(m)=27+8^m$$Tentukan nilai dari f(3), 2f(5), dan f(3)/2f(5)


\>function f(m)&=27+8^m;

\>$f(3)


$$539$$\>$2\*f(5)


$$65590$$\>$f(3)/(2\*f(5))


$$\frac{77}{9370}$$3. Diketahui nilai y dari fungsi di bawah ini adalah 1


$$f(x)=2^{4x-12y}$$Tentukan nilai f(3), f(8), dan buat grafiknya di f(3:5)!


\>function f(x):=2^(4\*x-12\*y)

\>function y:=1

\>f(8)


    1048576

\>f(3)


    1

\>f(3:5)


    [1,  16,  256]

\>aspect(1.3); plot2d("f",3,5):


## Contoh Fungsi Logaritma

1. Diberikan fungsi di bawah ini:


$$f(x)=e^2 \cdot \left( \frac{1}{3+4 \log(x)}+\frac{1}{7} \right)$$Tentukan nilai f(0.6)!


\>function f(x):= E^2\*(1/(3+4\*log(x))+1/7)

\>f(0.6)


    8.77908249441

\>plot2d("f",-0.6,0.6):


![images/EMTKalkulus_kelompok%204-031.png](images/EMTKalkulus_kelompok%204-031.png)

## Contoh Komposisi Fungsi

1. Untuk fungsi:


$$f(x) = x^2-3x+2$$$$g(x)=3x+5$$cari nilai


$$fog(-2), gof(0)$$\>function f(x) :=  x^2-3\*x+2; $f(x)

\>function g(x) := 3\*x+5; $g(x)

\>f(g(-2)), g(f(0))


    6
    11

\>plot2d("(3\*x+5)^2-3\*(3\*x+5)+2",-2,2):


![images/EMTKalkulus_kelompok%204-035.png](images/EMTKalkulus_kelompok%204-035.png)

# Latihan

Bukalah buku Kalkulus. Cari dan pilih beberapa (paling sedikit 5
fungsi berbeda tipe/bentuk/jenis) fungsi dari buku tersebut, kemudian
definisikan fungsi-fungsi tersebut dan komposisinya di EMT pada
baris-baris perintah berikut (jika perlu tambahkan lagi). Untuk setiap
fungsi, hitung beberapa nilainya, baik untuk satu nilai maupun vektor.
Gambar grafik fungsi-fungsi tersebut dan komposisi-komposisi 2 fungsi.


Juga, carilah fungsi beberapa (dua) variabel. Lakukan hal sama seperti
di atas.


1. Diberikan fungsi:


$$b(x)= \frac{12x^3}{7x^2-3x}$$Cari nilai b(1), vektor b(1:4), dan buatkan grafiknya!


\> 


\> 


2. Diketahui suatu fungsi f(x) sebagai berikut:


$$f(x,y)=\frac{3(x-1)(y-2)}{2}+\frac{(y-2)(x-3)}{2}-2(x-1)(y-3)$$Tentukan nilai dari f(20,10) dan buat grafiknya di f(20,10:30,20)!


3. Sketsakan grafik fungsi dibawah ini pada[-pi,2pi]


$$y(t)=sin(5t)$$4. Diketahui suatu fungsi f(x):


$$f(x)=3^x$$Tentukan nilai f(a+2^b-c) jika nilai a=1, b=2, dan c=5!


5. Untuk fungsi:


$$f(x) = 2x^2-3x+20$$$$g(x)= 3x-5$$cari nilai


$$fog(5), gof(8)$$# 2. Limit

## Definisi limit

Pada dasarnya, limit digunakan untuk menyatakan sesuatu yang nilainya
mendekati nilai tertentu. Limit dapat diartikan sebagai menuju suatu
batas, sesuatu yang dekat namun tidak dapat dicapai. Mengapa nilainya
hanya mendekati? Karena suatu fungsi biasanya tidak terdefinisi pada
titik-titik tertentu. Walaupun suatu fungsi seringkali tidak
terdefinisi untuk titik tertentu, namun masih dapat dicari tahu berapa
nilai yang didekati oleh fungsi tersebut apabila titik tertentu
semakin didekati yaitu dengan limit.


Bentuk umum dari limit sendiri dinotasikan dengan:


$$\lim_{x\rightarrow c}{F\left(x\right)}=L$$Notasi tersebut menyatakan bahwa f(x) untuk niai x mendekati c sama
dengan L. F(x) disini dapat berupa bermacam-macam jenis fungsi. Dan L
dapat berupa konstanta, ataupun "und" (tak terdefinisi), "ind" (tak
tentu namun terbatas), "infinity" (kompleks tak hingga). Begitupun
dengan batas c, dapat berupa sebarang nilai atau pada tak hingga
(-inf, minf, dan inf).


Sebuah fungsi dapat dikatakan memiliki limit apabila limit kanan dan
limit kiri nya memiliki nilai yang sama. Dimana, limit dari fungsi
tersebut adalah nilai dari limit kanan dan limit kiri fungsi yang
bernilai sama tadi.


## Sifat-sifat Limit

Jika f(x) dan g(x) adalah fungsi yang memiliki limit di c, n merupakan
bilangan bulat positif, dan k adalah konstanta.


1.


$$\lim_{x \to c}k=k$$\>$showev('limit(5,x,2))


$$5=5$$$$\lim_{x \to 2}5=5$$2.


maxima: 'limit(x,x,c)=c


$$\lim_{x\rightarrow c}{x}=c$$\>$showev('limit(x,x,3))


$$\lim_{x\rightarrow 3}{x}=3$$3.


maxima: 'limit(kf(x),x,c)= k*maxima: 'limit(f(x),x,c)


$$\lim_{x\rightarrow c}{{\it kf}\left(x\right)}=k\,\left(\lim_{x
 \rightarrow c}{f\left(x\right)}\right)$$\>$showev('limit(4\*x^2,x,1))


$$4\,\left(\lim_{x\rightarrow 1}{x^2}\right)=4$$4.


maxima: 'limit([g(x)+f(x)],x,c)= maxima: 'limit(g(x),x,c) + maxima: 'limit(f(x),x,c)


$$\lim_{x\rightarrow c}{\left[ g\left(x\right)+f\left(x\right)
  \right] }=\lim_{x\rightarrow c}{g\left(x\right)}+\lim_{x
 \rightarrow c}{f\left(x\right)}$$\>$showev('limit(x^3+2\*x,x,1))


$$\lim_{x\rightarrow 1}{x^3+2\,x}=3$$5.


maxima: 'limit([g(x)-f(x)],x,c)= maxima: 'limit(g(x),x,c) - maxima: 'limit(f(x),x,c)


$$\lim_{x\rightarrow c}{\left[ g\left(x\right)-f\left(x\right)
  \right] }=\lim_{x\rightarrow c}{g\left(x\right)}-\lim_{x
 \rightarrow c}{f\left(x\right)}$$\>$showev('limit(x^2-4\*x,x,5))


$$\lim_{x\rightarrow 5}{x^2-4\,x}=5$$6.


maxima: 'limit([g(x)*f(x)],x,c)= maxima: 'limit(g(x),x,c) * maxima: 'limit(f(x),x,c)


$$\lim_{x\rightarrow c}{\left[ f\left(x\right)\,g\left(x\right)
  \right] }=\left(\lim_{x\rightarrow c}{f\left(x\right)}\right)\,
 \left(\lim_{x\rightarrow c}{g\left(x\right)}\right)$$\>$showev('limit((x-1)\*(x+4),x,3))


$$\lim_{x\rightarrow 3}{\left(x-1\right)\,\left(x+4\right)}=14$$7.


maxima: 'limit(g(x)/f(x),x,c)= maxima: 'limit(g(x),x,c) / maxima: 'limit(f(x),x,c)


$$\lim_{x\rightarrow c}{\frac{g\left(x\right)}{f\left(x\right)}}=
 \frac{\lim_{x\rightarrow c}{g\left(x\right)}}{\lim_{x\rightarrow c}{
 f\left(x\right)}}$$\>$showev('limit((x+5)/(x+1),x,0))


$$\lim_{x\rightarrow 0}{\frac{x+5}{x+1}}=5$$8.


maxima: 'limit(f(x)^n,x,c)=maxima:'limit(f(x),x,c)^n


$$\lim_{x\rightarrow c}{f^{n}\left(x\right)}=\left(\lim_{x
 \rightarrow c}{f\left(x\right)}\right)^{n}$$\>$showev('limit((x+3)^2,x,1))


$$\lim_{x\rightarrow 1}{\left(x+3\right)^2}=16$$9.


$$\lim_{x\rightarrow c}{f\left(x\right)^{\frac{1}{n}}}=\left(\lim_{x
 \rightarrow c}{f\left(x\right)}\right)^{\frac{1}{n}}$$\>$showev('limit((x^2+3\*x+1)^(1/2),x,2))


$$\lim_{x\rightarrow 2}{\sqrt{x^2+3\,x+1}}=\sqrt{11}$$# Limit pada EMT

Pada EMT cara mendefinisikan limit yaitu dengan format :


$showev('limit(f(x),x,c))


Format tersebut akan menampilkan limit yang dimaksud dan hasilnya.
Jika kita ingin menampilkan hasilnya saja dari sebuah limit tanpa
menampilkan limitnya, kita bisa menggunakan format :


$limit(f(x),x,c)


Sedangkan, untuk limit kanan dan limit kiri seperti pada definisi
dapat ditampilkan di EMT dengan cara menambah opsi "plus" atau "minus"
:


$showev('limit(f(x),x,c, plus)) atau 'limit(f(x),x,c, minus)


\>$showev('limit(x^2+3\*x+4,x,2))


$$\lim_{x\rightarrow 2}{x^2+3\,x+4}=14$$\>$limit(x^2+3\*x+4,x,2)


$$14$$# Menghitung dan Visualisasi Limit

Perhitungan limit pada EMT dapat dilakukan dengan menggunakan fungsi
Maxima, yakni "limit". Fungsi "limit" dapat digunakan untuk menghitung
limit fungsi dalam bentuk ekspresi maupun fungsi yang sudah
didefinisikan sebelumnya. Nilai limit dapat dihitung pada sebarang
nilai atau pada tak hingga (-inf, minf, dan inf). Limit kiri dan limit
kanan juga dapat dihitung, dengan cara memberi opsi "plus" atau
"minus". Hasil limit dapat berupa nilai, "und" (tak definisi), "ind"
(tak tentu namun terbatas), "infinity" (kompleks tak hingga).


Limit dapat divisualisasikan menggunakan plot 2 dimensi. Pada EMT
sendiri, format yang bisa digunakan untuk memvisualisasikan limit
adalah :


plot2d("f(x)",-c,c):


Dengan f(x) adalah fungsi pada limit yang dicari, dan c berupa
bilangan real menyesuaikan batas dari limit itu sendiri.


## Limit Aljabar



1. Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama. Berapakah nilai limitnya?


$$\lim_{x\rightarrow 0}{x^2+x-1}$$\>$showev('limit(x^2+x-1,x,0,minus))


$$\lim_{x\uparrow 0}{x^2+x-1}=-1$$\>$showev('limit(x^2+x-1,x,0,plus))


$$\lim_{x\downarrow 0}{x^2+x-1}=-1$$Dapat terlihat bahwa nilai limit kiri = nilai limit kanan. Maka fungsi
tersebut memiliki nilai limit, yaitu :


\>$showev('limit(x^2+x-1,x,0))


$$\lim_{x\rightarrow 0}{x^2+x-1}=-1$$2. Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama. Berapakah nilai limitnya?


$$\lim_{x\rightarrow 3}{\sqrt{x^2+x-1}}$$\>$showev('limit(sqrt(x^2+x-1),x,3,minus))


$$\lim_{x\uparrow 3}{\sqrt{x^2+x-1}}=\sqrt{11}$$\>$showev('limit(sqrt(x^2+x-1),x,3,plus))


$$\lim_{x\downarrow 3}{\sqrt{x^2+x-1}}=\sqrt{11}$$Dapat terlihat bahwa nilai limit kiri = nilai limit kanan. Maka fungsi
tersebut memiliki nilai limit, yaitu :


\>$showev('limit(sqrt(x^2+x-1),x,3))


$$\lim_{x\rightarrow 3}{\sqrt{x^2+x-1}}=\sqrt{11}$$3. Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama. Berapakah nilai limitnya?


$$\lim_{x\rightarrow -3}{\frac{\left| x+3\right| }{x+3}}$$\>$showev('limit(abs(x+3)/(x+3),x,-3,minus))


$$\lim_{x\uparrow -3}{\frac{\left| x+3\right| }{x+3}}=-1$$\>$showev('limit(abs(x+3)/(x+3),x,-3,plus))


$$\lim_{x\downarrow -3}{\frac{\left| x+3\right| }{x+3}}=1$$Karena nilai limit kiri tidak sama dengan nilai limit kanan. Maka
fungsi diatas tidak memiliki limit di x=-3


\>$showev('limit(abs(x+3)/(x+3),x,-3))


$$\lim_{x\rightarrow -3}{\frac{\left| x+3\right| }{x+3}}={\it und}$$\>$limit(x^3+4\*x+5,x,2)


$$21$$\>plot2d("x^3+4\*x+5",1.8,2.2); plot2d(2,21,\>points,style="ow",\>add):


![images/EMTKalkulus_kelompok%204-078.png](images/EMTKalkulus_kelompok%204-078.png)

Jadi berdasarkan grafik, nilai limit tersebut adalah 21.


5. Berapakah nilai limit dari fungsi berikut? Tunjukkan dengan
menggunakan grafik!


maxima: 'limit((abs(x-5))/(x-5),x,5)


$$\lim_{x\rightarrow 5}{\frac{\left| x-5\right| }{x-5}}$$\>plot2d("abs(x-5)/(x-5)",4.9,5.1):


![images/EMTKalkulus_kelompok%204-080.png](images/EMTKalkulus_kelompok%204-080.png)

Karena nilai limit kiri tidak sama dengan limit kanan. maka nili limit
fungsi tersebut tidak ada.


6. Berapakah nilai limit dari fungsi berikut?


$$\lim_{x\rightarrow \infty }{\frac{x^5-3\,x^3+x^2-9}{4\,x^5-7\,x^4+2
 \,x-1}}$$\>$showev('limit((x^5-3\*x^3+x^2-9)/(4\*x^5-7\*x^4+2\*x-1),x,inf))


$$\lim_{x\rightarrow \infty }{\frac{x^5-3\,x^3+x^2-9}{4\,x^5-7\,x^4+2
 \,x-1}}=\frac{1}{4}$$7. Tunjukkan nilai limit fungsi berikut dengan grafik!


maxima:  'limit(sqrt(x^2+x)-x,x,inf)


$$\lim_{x\rightarrow \infty }{\sqrt{x^2+x}-x}$$\>plot2d("sqrt(x^2+x)-x",0,10):


![images/EMTKalkulus_kelompok%204-084.png](images/EMTKalkulus_kelompok%204-084.png)

Dengan menggunakan grafik diperlihatkan bahwa nilai limit mendekati
0.5. Mari kita buktikan di baris perintah


\>$showev('limit(sqrt(x^2+x)-x,x,inf))


$$\lim_{x\rightarrow \infty }{\sqrt{x^2+x}-x}=\frac{1}{2}$$## Limit Trigonometri

1. Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama. Berapakah nilai limitnya?


$$\lim_{x\rightarrow 0}{\cos x\,\sin x}$$\>$showev('limit(cos(x)\*sin(x),x,0,minus))


$$\lim_{x\uparrow 0}{\cos x\,\sin x}=0$$\>$showev('limit(cos(x)\*sin(x),x,0,plus))


$$\lim_{x\downarrow 0}{\cos x\,\sin x}=0$$Dapat terlihat bahwa nilai limit kiri = nilai limit kanan. Maka fungsi
tersebut memiliki nilai limit, yaitu :


\>$showev('limit(cos(x)\*sin(x),x,0))


$$\lim_{x\rightarrow 0}{\cos x\,\sin x}=0$$2. Berapakah nilai limit dari fungsi berikut? Tunjukkan dengan
menggunakan grafik


$$\lim_{x\rightarrow 0}{\frac{1-\cos x}{x}}$$\>plot2d("(1-cos(x))/x",-pi/4,pi/4); plot2d(0,0,\>points,style="ow",\>add):


![images/EMTKalkulus_kelompok%204-091.png](images/EMTKalkulus_kelompok%204-091.png)

3. Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama. Berapakah nilai limitnya?


$$\lim_{x\rightarrow 0}{\frac{\sin x}{1-\cos x}}$$\>$showev('limit(3\*sin(x)^2/(1-cos(x)),x,0,minus))


$$3\,\left(\lim_{x\uparrow 0}{\frac{\sin ^2x}{1-\cos x}}\right)=6$$\>$showev('limit(3\*sin(x)^2/(1-cos(x)),x,0,plus))


$$3\,\left(\lim_{x\downarrow 0}{\frac{\sin ^2x}{1-\cos x}}\right)=6$$Dapat terlihat bahwa nilai limit kiri = nilai limit kanan. Maka fungsi
tersebut memiliki nilai limit, yaitu


\>$showev('limit(3\*sin(x)^2/(1-cos(x)),x,0))


$$3\,\left(\lim_{x\rightarrow 0}{\frac{\sin ^2x}{1-\cos x}}\right)=6$$4. Berapakah nilai limit dari fungsi berikut? Tunjukkan dengan
menggunakan grafik!


$$\lim_{x\rightarrow 0}{\left| \sin \left(2\,x\right)\right| -\cos x}$$\>$limit(abs(sin(2\*x))-cos(x),x,0)


$$-1$$\>plot2d("abs(sin(2x))-cos(x)",-pi/2,pi/2); plot2d(0,-1,\>points,style="ow",\>add):


![images/EMTKalkulus_kelompok%204-098.png](images/EMTKalkulus_kelompok%204-098.png)

Jadi berdasarkan grafik, nilai limit tersebut adalah -1.


5. Berapakah nilai limit dari fungsi berikut? Tunjukkan dengan
menggunakan grafik!


maxima: 'limit(2*sin(x)*cos(x)-tan(x),x,pi/3)


$$\lim_{x\rightarrow \frac{\pi}{3}}{2\,\cos x\,\sin x-\tan x}$$\>$limit(2\*cos(x)\*sin(x)-tan(x),x,pi/3)


$$-\frac{\sqrt{3}}{2}$$\>plot2d("2\*cos(x)\*sin(x)-tan(x)",0,pi/2.9); plot2d(pi/3,-(3)^(1/2)/2,\>points,style="ow",\>add):


![images/EMTKalkulus_kelompok%204-101.png](images/EMTKalkulus_kelompok%204-101.png)

Jadi berdasarkan grafik, nilai limit tersebut adalah -0.866.


6. Berapakah nilai limit dari fungsi berikut? Tunjukkan dengan
menggunakan grafik!


$$2\,\left(\lim_{x\rightarrow 0}{\sec x}\right)$$\>$limit(2\*sec(x),x,0)


$$2$$\>plot2d("2\*sec(x)",-pi/3,pi/3); plot2d(0,2,\>points,style="ow",\>add):


![images/EMTKalkulus_kelompok%204-104.png](images/EMTKalkulus_kelompok%204-104.png)

Jadi berdasarkan grafik, nilai limit tersebut adalah 2.


## Latihan

Tunjukkan bahwa limit kiri dan kanan dari fungsi berikut bernilai
sama!


$$\lim_{x\rightarrow 3}{\frac{\left(x-3\right)\,\left| x^3+5\,x+8
 \right| }{\cos x}}$$\>$limit(abs(x^3+5\*x+8)/cos(x)\*(x-3),x,3)


$$0$$Tunjukkan nilai limit fungsi berikut dengan menggunakan grafik!


$$\lim_{x\rightarrow 0.8}{\frac{\left(x^2+6\,x+1\right)\,\sin \left(3
 \,x\right)}{\cos x}}$$\>$limit((x^2+6\*x+1)\*sin(3\*x)/cos(x),x,0.8)


$$6.243635699770241$$# 3. Turunan Fungsi

  Turunan adalah pengukuran terhadap bagaimana fungsi berubah seiring  

perubahan nilai yang dimasukkan, atau secara umum turunan menunjukkan
bagaimana suatu besaran berubah akibat perubahan besaran lainnya.
Proses dalam menemukan turunan disebut diferensiasi.


Definisi turunan:


$$f'(x) = \lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$$

Berikut adalah contoh-contoh menentukan turunan fungsi dengan beberapa
cara.


## Turunan fungsi Aljabar

Mencari turunan dari


$$f(x)=x^n$$\>$showev('limit(((x+h)^n-x^n)/h,h,0)) // turunan x^n


$$\lim_{h\rightarrow 0}{\frac{\left(x+h\right)^{n}-x^{n}}{h}}=n\,x^{n
 -1}$$Bukti:


$$(x+h)^n= \binom{n}{0}x^{n-0}h^0+ \binom{n}{1}x^{n-1}h^1+\binom{n}{2}x^{n-2}h^2+...+\binom{n}{n}x^{n-n}h^n$$$$(x+h)^n = x^n+nx^{n-1}h+\binom{n}{2}x^{n-2}h^2+...+h^n$$$$(x+h)^n -x^n = nx^{n-1}h+\binom{n}{2}x^{n-2}h^2+...+h^n$$$$\frac{(x+h)^n -x^n}{h} = nx^{n-1}+\binom{n}{2}x^{n-2}h+...+h^{n-1}$$$$ \lim_{h\to 0}\frac{(x+h)^n -x^n}{h}=nx^{n-1}$$Mencari turunan dari


$$f(x)=x^2$$\>$showev('limit(((x+h)^2-x^2)/h,h,0)) // turunan x^2


$$\lim_{h\rightarrow 0}{\frac{\left(x+h\right)^2-x^2}{h}}=2\,x$$\>p &= expand((x+h)^2-x^2)|simplify; $p //pembilang dijabarkan dan disederhanakan


$$2\,h\,x+h^2$$\>q &=ratsimp(p/h); $q // ekspresi yang akan dihitung limitnya disederhanakan


$$2\,x+h$$\>$limit(q,h,0) // nilai limit sebagai turunan


$$2\,x$$\>plot2d(["x^2", "2x"], color=[black,red]):


![images/EMTKalkulus_kelompok%204-122.png](images/EMTKalkulus_kelompok%204-122.png)

Mencari turunan dari


$$f(x)=f(x)^x$$\>$showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f(x)=f(x)^x


    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Maxima is asking
    Acceptable answers are: yes, y, Y, no, n, N, unknown, uk
    Is x an integer?
    
    Use assume!
    Error in:
    $showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f(x)=f(x)^x ...
                                         ^

Di sini Maxima bermasalah terkait limit:


$$\lim_{h\to 0} \frac{(x+h)^{x+h}-x^x}{h}.$$Dalam hal ini diperlukan asumsi nilai x.


\>&assume(x\>0); $showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f(x)=f(x)^x


    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Maxima is asking
    Acceptable answers are: yes, y, Y, no, n, N, unknown, uk
    Is x an integer?
    
    Use assume!
    Error in:
    ... ssume(x&gt;0); $showev('limit((f(x+h)-f(x))/h,h,0)) // turunan f( ...
                                                         ^

\>&forget(x\>0) // jangan lupa, lupakan asumsi untuk kembali ke semula


    
                                   [x &gt; 0]
    

\>&forget(x<0)


    
                                   [x &lt; 0]
    

\>&facts()


    
                                      []
    

Selain dengan showev('limit...) kita juga dapat mencari turunan dengan
menyederhanakan pembilang seperti di awal


\>p &= expand(f(x+h)-f(x))|simplify;  $p


$$8^{x+h}-8^{x}$$\>q &=ratsimp(p/h); $q 


$$\frac{\left(8^{h}-1\right)\,8^{x}}{h}$$\>$limit(q,h,0)  


    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Maxima is asking
    Acceptable answers are: yes, y, Y, no, n, N, unknown, uk
    Is x an integer?
    
    Use assume!
    Error in:
    $limit(q,h,0)   ...
                   ^

Mencari turunan dari


$$f(x)=\frac{1}{x}$$\>$showev('limit((1/(x+h)-1/x)/h,h,0)) // turunan 1/x


$$\lim_{h\rightarrow 0}{\frac{\frac{1}{x+h}-\frac{1}{x}}{h}}=-\frac{1
 }{x^2}$$\>plot2d("-x^(-2)", color=red):


![images/EMTKalkulus_kelompok%204-129.png](images/EMTKalkulus_kelompok%204-129.png)

## Turunan fungsi trigonometri

Mencari turunan dari


$$sin(x)$$\>$showev('limit((sin(x+h)-sin(x))/h,h,0)) // turunan sin(x)


$$\lim_{h\rightarrow 0}{\frac{\sin \left(x+h\right)-\sin x}{h}}=\cos 
 x$$Bukti:


$$sin(x+h) = sin(x)cos(h)+cos(x)sin(h)$$$$sin(x+h)-sin(x) = sin(x)cos(h)+cos(x)sin(h)-sin(x)$$$$sin(x+h)-sin(x) = cos(x)sin(h) - sin(x)+sin(x)cos(h)$$$$sin(x+h)-sin(x) = cos(x)sin(h) - sin(x)(1-cos(h))$$$$\lim_{h\to 0}\frac{sin(x+h)-sin(x)}{h}= \lim_{h\to 0}\frac{cos(x)sin(h)}{h}-\lim_{h\to 0}\frac{sin(x)(1-cos(h)}{h}$$$$\lim_{h\to 0}\frac{sin(x+h)-sin(x)}{h}=cos(x)\lim_{h\to 0}\frac{sin(h)}{h}-sin(x)\lim_{h\to 0}\frac{(1-cos(h)}{h}$$$$=cos(x)\times 1 -sin(x) \times 0 =cos(x)$$\>p &= expand((sin(x+h)-sin(x)))|simplify; $p


$$\sin \left(x+h\right)-\sin x$$\>q &=ratsimp(p/h); $q


$$\frac{\sin \left(x+h\right)-\sin x}{h}$$\>$limit(q,h,0) // nilai limit sebagai turunan


$$\cos x$$\>plot2d(["sin(x)", "cos(x)"],0, 2\*pi, color=[blue,green]):


![images/EMTKalkulus_kelompok%204-142.png](images/EMTKalkulus_kelompok%204-142.png)

Mencari turunan dari


$$tan(x)$$\>$showev('limit((tan(x+h)-tan(x))/h,h,0)) // turunan tan(x)


$$\lim_{h\rightarrow 0}{\frac{\tan \left(x+h\right)-\tan x}{h}}=
 \frac{1}{\cos ^2x}$$Bukti:


$$tan(x+h) = \frac {tan (x)+tan (h)}{1-tan(x)tan(h)}$$$$tan(x+h)-tan (x) ={\frac {tan (x)+tan (h)-tan (x)+tan^2(x)tan(h)}{1-tan(x)tan(h)}}$$$$=\frac {tan(x+h)-tan (x)}{h} =\frac{ \frac {tan (x)+tan (h)-tan (x)+tan^2(x)tan(h)}{1-tan(x)tan(h)}}{h}$$$$=\frac {tan(h)+tan^2(x) tan(h)}{h(1-tan(x)tan(h)}$$$$=\lim_{h\to 0} \frac {tan(h)+tan^2(x) tan(h)}{h(1-tan(x)tan(h)}$$$$=\lim_{h\to 0} \frac {1 +tan^2(x)}{1-tan (x)tan(h)} \cdot \lim_{h\to 0} \frac{tan (h)}{h}$$$$=\frac {1 +tan^2(x)}{1-tan (x)tan(0)} \cdot 1$$$$=1+tan^2(x)$$$$=1+tan^2(x)=1+ \frac{sin^2(x)}{cos^2(x)}$$$$ =\frac{cos^2(x) + sin^2(x)}{cos^2(x)}$$$$ =\frac{1}{cos^2(x)}$$\>p &= expand((tan(x+h)-tan(x)))|simplify; $p


$$\tan \left(x+h\right)-\tan x$$\>q &=ratsimp(p/h); $q


$$\frac{\tan \left(x+h\right)-\tan x}{h}$$\>  $limit(q,h,0) // nilai limit sebagai turunan


$$\frac{1}{\cos ^2x}$$Mencari turunan dari


$$arcsin(x)$$\>$showev('limit((asin(x+h)-asin(x))/h,h,0)) // turunan arcsin(x)


$$\lim_{h\rightarrow 0}{\frac{\arcsin \left(x+h\right)-\arcsin x}{h}}=
 \frac{1}{\sqrt{1-x^2}}$$Bukti:


$$f'(x)= \lim_{h\to 0} \frac {arcsin(x+h)-arcsin(x)}{h}$$Misalkan arcsin(x+h)=A dan arcsin(x)=B


Sehingga sin A= x+h dan sin B=x


Kurangkan persamaan kedua dengan persamaan pertama


$$sin(A)-sin(B)=(x+h)-x$$$$sin(A)-sin(B) = h$$karena


$$h \to 0, sin(A)-sin(B) \to 0$$

maka


$$sin(A)\to sin(B),  A \to B, A-B \to 0$$sehingga f'(x) menjadi


$$f'(x) = \lim_{A-B \to 0} \frac{A-B}{sin A- sin B}$$Identitas trigonometri


$$sin(A)-sin(B) = 2 sin[\frac{A-B}{2}]cos[\frac{A+B}{2}]$$$$f'(x) = \lim_{A-B \to 0} \frac {A-B}{2 sin [\frac{A-B}{2}] cos [\frac{A+B}{2}]}$$$$f'(x) = \lim_{A-B \to 0} \frac {\frac{2(A-B)}{2}}{2 sin [\frac{A-B}{2}] cos [\frac{A+B}{2}]}$$ingat bahwa


$$\lim_{x \to 0} \frac{x}{sin (x)}=1$$$$f'(x) = \lim_{A-B \to 0}\frac{\frac{(A-B)}{2}}{sin [\frac{A-B}{2}]} \cdot \frac{2}{2cos [\frac{A+B}{2}]}$$$$f'(x) = 1 \cdot \frac{2}{2cos [\frac{B+B}{2}]}$$$$f'(x) = \frac {1}{cos (B)}$$$$f'(x) = \frac {1}{\sqrt{(cos^2 (B)}}$$$$f'(x) = \frac {1}{\sqrt{(1- sin^2 (B)}}= \frac {1}{\sqrt{(1-x^2}}$$\>p &= expand((asin(x+h)-asin(x)))|simplify; $p //pembilang dijabarkan dan disederhanakan


$$\arcsin \left(x+h\right)-\arcsin x$$\>q &=ratsimp(p/h); $q // ekspresi yang akan dihitung limitnya disederhanakan


$$\frac{\arcsin \left(x+h\right)-\arcsin x}{h}$$\>$limit(q,h,0) // nilai limit sebagai turunan


$$\frac{1}{\sqrt{1-x^2}}$$\>plot2d(["asin(x)","1/(sqrt(1-x^2))"],-1,1,color=[blue,red]):


![images/EMTKalkulus_kelompok%204-179.png](images/EMTKalkulus_kelompok%204-179.png)

Mencari turunan dari


$$x^2+10$$

di titik x=5


\>function f(x) &= x^2+10 // definisikan f(x)=x^2+10


    
                                    2
                                   x  + 10
    

\>function df(x) &= showev('diff(f(x),x)); $df(x)


$$\frac{d}{d\,x}\,\left(x^2+10\right)=2\,x$$\>$% with x=5


$${\it \%at}\left(\frac{d}{d\,x}\,\left(x^2+10\right) , x=5\right)=10$$\>diff(f,5), diffc(f,5)


    9.99999999997
    10

diff: Diferensiasi numerik yang pada dasarnya kurang akurat untuk
fungsi umum.


diffc: Menghitung turunan pertama untuk fungsi analitik nyata dengan
menggunakan bagian imajiner dari f(x+ih)/h. Cara ini memungkinkan
untuk mengevaluasi f dengan lebih akurat.


Mencari turunan dari


$$sinh(x)$$\>function f(x) &= sinh(x) // definisikan f(x)=sinh(x)


    
                                   sinh(x)
    

\>function df(x) &= limit((f(x+h)-f(x))/h,h,0); $df(x) // df(x) = f'(x)


$$\frac{e^ {- x }\,\left(e^{2\,x}+1\right)}{2}$$Hasilnya adalah cosh(x), karena


$$\frac{e^x+e^{-x}}{2}=\cosh(x).$$\>plot2d(["f(x)","df(x)"],-pi,pi,color=[blue,red]):


![images/EMTKalkulus_kelompok%204-186.png](images/EMTKalkulus_kelompok%204-186.png)

\>$showev('diff(f(x),x))


$$\frac{d}{d\,x}\,\sinh x=\cosh x$$\>$% with x=3


$${\it \%at}\left(\frac{d}{d\,x}\,\sinh x , x=3\right)=\cosh 3$$\>$float(%)


$${\it \%at}\left(\frac{d^{1.0}}{d\,x^{1.0}}\,\sinh x , x=3.0\right)=
 10.06766199577777$$\>plot2d(f,0,3.1):


![images/EMTKalkulus_kelompok%204-190.png](images/EMTKalkulus_kelompok%204-190.png)

Mencari turunan dari


$$f(x)=sin(3x^5+7)^2$$\>function f(x) &= sin(3\*x^5+7)^2


    
                                   2    5
                                sin (3 x  + 7)
    

\>$showev('diff(f(x),x))


$$\frac{d}{d\,x}\,\sin ^2\left(3\,x^5+7\right)=30\,x^4\,\cos \left(3
 \,x^5+7\right)\,\sin \left(3\,x^5+7\right)$$Kita akan mencari nilai turunan tersebut ketika x=2


\>$% with x = 2


$${\it \%at}\left(\frac{d}{d\,x}\,\sin ^2\left(3\,x^5+7\right) , x=2
 \right)=480\,\cos 103\,\sin 103$$\>$float(%)


$${\it \%at}\left(\frac{d^{1.0}}{d\,x^{1.0}}\,\sin ^2\left(3.0\,x^5+
 7.0\right) , x=2.0\right)=-233.9140567500984$$\>diff(f,2), diffc(f,2)


    -233.913935807
    -233.91405675

diff: Diferensiasi numerik yang pada dasarnya kurang akurat untuk
fungsi umum.


diffc: Menghitung turunan pertama untuk fungsi analitik nyata dengan
menggunakan bagian imajiner dari f(x+ih)/h. Cara ini memungkinkan
untuk mengevaluasi f dengan lebih akurat.


\>plot2d(f,0,3.1) :


![images/EMTKalkulus_kelompok%204-195.png](images/EMTKalkulus_kelompok%204-195.png)

Mencari turunan dari


$$a(x)=5cos(2x)-2xsin(2x)$$\>function a(x) &=5\*cos(2\*x)-2\*x\*sin(2\*x) // mendifinisikan fungsi a


    
                          5 cos(2 x) - 2 x sin(2 x)
    

\>function da(x) &=diff(a(x),x); $da(x) // da(x) = a'(x)


$$-12\,\sin \left(2\,x\right)-4\,x\,\cos \left(2\,x\right)$$\>$’a(1)=a(1), $float(a(1)), $’a(2)=a(2), $float(a(2)) // nilai a(1) dan a(2)


$$-3.899329036387075$$$$-0.2410081230863468$$\>xp=solve("da(x)",1,2,0) // solusi a'(x)=0 pada interval [1, 2]


    1.35822987384

\>da(xp), a(xp) // cek bahwa a'(xp)=0 dan nilai ekstrim di titik tersebut


    0
    -5.67530133759

\>plot2d(["a(x)","da(x)"],0,2\*pi,color=[blue,red]): //grafik fungsi dan turunannya


![images/EMTKalkulus_kelompok%204-200.png](images/EMTKalkulus_kelompok%204-200.png)

Pada titik puncak grafik a(x), nilai turunan a'(x) akan selalu sama
dengan nol. Ini karena gradien garis singgung pada titik puncak adalah
nol.


## Turunan fungsi logaritma

Mencari turunan dari


$$f(x)= log(x)$$\>$showev('limit((log(x+h)- log(x))/h,h,0)) // turunan log(x)


$$\lim_{h\rightarrow 0}{\frac{\log \left(x+h\right)-\log x}{h}}=
 \frac{1}{x}$$Bukti:


$$f'(x) = \lim_{h\to 0} \frac{log(x+h)-log x}{h}$$ingat bahwa


$$log(a)-log(b)= log (\frac{a}{b})$$$$f'(x)=\lim_{h\to 0}\frac{ log (\frac{x+h}{x})}{h}$$$$f'(x)=\lim_{h\to 0}\frac{ log (1 + \frac{h}{x})}{h}$$misalkan h/x = n sehingga h=nx


$$f'(x)=\lim_{n\to 0}\frac{ log (1 + n)}{nx}$$$$f'(x)=\lim_{n\to 0}\frac{1}{nx} \cdot log(1+n)$$ingat bahwa


$$a log b = log b^a$$$$f'(x)=\lim_{n\to 0} \frac{1}{x} \cdot log(1+n)^\frac{1}{n}$$$$f'(x)= \frac{1}{x}log \lim_{n\to 0}(1+n)^\frac{1}{n}$$$$\lim_{n\to 0}(1+n)^\frac{1}{n} = e$$$$f'(x)= \frac{1}{x}log e$$$$f'(x)=\frac{1}{x}$$\>$showev('limit((log((x+h)/(x)))/h,h,0))//definisi logaritma


$$\lim_{h\rightarrow 0}{\frac{\log \left(\frac{x+h}{x}\right)}{h}}=
 \frac{1}{x}$$\>$showev('limit(((h/x))/h,h,0))//menggunakan identitas logaritma, sisanya adalah hasil turunan


$$\frac{1}{x}=\frac{1}{x}$$## Turunan fungsi eksponensial

Mencari turunan dari


$$f(x)=e^x$$\>$showev('limit((E^(x+h)-E^x)/h,h,0)) // turunan f(x)=e^x


    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Answering "Is x an integer?" with "integer"
    Maxima is asking
    Acceptable answers are: yes, y, Y, no, n, N, unknown, uk
    Is x an integer?
    
    Use assume!
    Error in:
    $showev('limit((E^(x+h)-E^x)/h,h,0)) // turunan f(x)=e^x ...
                                         ^

 Maxima bermasalah dengan limit:  

 latex: \lim_{h\to 0}\frac{e^{x+h}-e^x}{h}.  

 Oleh karena itu diperlukan trik khusus agar hasilnya benar.  

\>$showev('factor(E^(x+h)-E^x))


$${\it factor}\left(e^{x+h}-e^{x}\right)=\left(e^{h}-1\right)\,e^{x}$$\>$showev('limit(factor((E^(x+h)-E^x)/h),h,0)) // turunan f(x)=e^x


$$\left(\lim_{h\rightarrow 0}{\frac{e^{h}-1}{h}}\right)\,e^{x}=e^{x}$$\>$showev('limit((E^h-1)/h,h,0))


## Sifat- sifat Turunan

1. Jika f(x)=k dengan k suatu konstanta maka untuk sebarang x, f'x = 0


   Bukti:


$$f'(x)= \lim_{h\to 0}\frac{f(x+h)-f(x)}{h} = \lim_{h\to 0}\frac{k-k}{h} = \lim_{h\to 0}0=0$$2. Jika f(x)=x, maka f'(x)=1


   Bukti:


$$f'(x)= \lim_{h\to 0}\frac{f(x+h)-f(x)}{h} = \lim_{h\to 0}\frac{x+h-x}{h}=\lim_{h\to 0}\frac {h}{h}=1$$3. Jika k suatu konstanta dan f suatu fungsi yang terdiferensialkan,


   maka (kf)'(x)= kf'(x)


   Bukti:


   Andaikan F(x) = kf(x), maka


$$F'(x)=\lim_{h\to 0}\frac{F(x+h)-F(x)}{h}=\lim_{h\to 0}\frac{kf(x+h)-kf(x)}{h}$$$$    = \lim_{h\to 0}k \frac{f(x+h)-f(x)}{h}=k\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$$$$= kf'(x)$$4. Jika f dan g adalah fungsi-fungsi yang terdiferensial,


   maka (f+g)'(x)=f'(x)+g'(x)


   Bukti:


$$F'(x)=\lim_{h\to 0}\frac{f(x+h)+g(x+h)-f(x)+g(x)}{h}$$$$=\lim_{h\to 0}[\frac{f(x+h)-f(x)}{h}+\frac{g(x+h)-g(x)}{h}]$$$$=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}+\lim_{h\to 0}\frac{g(x+h)-g(x)}{h}=f'(x)+g'(x)$$5. Andaikan f dan g adalah fungsi yang dapat didiferensialkan,


   maka (fg)'(x)=f'(x)g(x)+ f(x)g'(x)


   Bukti:


   Andaikan F(x)=f(x)g(x)


$$F'(x)= \lim_{h\to 0}\frac{F(x+h)-F(x)}{h}$$$$= \lim_{h\to 0}\frac{f(x+h)g(x+h)-f(x)g(x)}{h}$$$$= \lim_{h\to 0}\frac{f(x+h)g(x+h)-f(x+h)g(x)+f(x+h)g(x)-f(x)g(x)}{h}$$$$=\lim_{h\to 0}[f(x+h)\frac{g(x+h)-g(x)+g(x)f(x+h)-f(x)}{h}]$$$$=\lim_{h\to 0} f(x+h)=\lim_{h \to 0}\frac{g(x+h)-g(x)}{h}+g(x)\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}$$$$=f(x)g'(x)+g(x)f'(x)$$    
                                      2
                                   3 x  - 5
    

6. Andaikan f dan g adalah fungsi yang dapat didiferensialkan


   dengan g(x)tidak sama dengan 0, maka:


$$(\frac{f}{g})(x)=\frac{g(x)f'(x)-f(x)g'(x)}{g(x)^2}$$   Bukti:  
   Andaikan F(x)=f(x)/g(x)  

$$F'(x)= \lim_{h\to 0}\frac{F(x+h)-F(x)}{h}$$$$= \lim_{h\to 0}\frac{\frac{f(x+h)}{g(x+h}-\frac{f(x)}{g(x)}}{h}$$$$= \lim_{h\to 0}\frac{g(x)f(x+h)-f(x)g(x+h)}{h}\frac{1}{g(x)g(x+h)}$$$$= \lim_{h\to 0}[\frac{g(x)f(x+h)-g(x)f(x)+g(x)f(x)-f(x)g(x+h)}{h}\frac{1}{g(x)g(x+h)}]$$$$=\lim_{h\to 0} [g(x)\frac{f(x+h)-f(x)}{h}-f(x)\frac{g(x+h)-g(x)}{h}]\frac{1}{g(x)g(x+h)}$$$$=[g(x)f'(x)-f(x)g'(x)]\frac{1}{g(x)g(x)}$$$$=\frac{g(x)f'(x)-f(x)g'(x)}{g(x)^2}$$## Aplikasi turunan

1. Persamaan gerak suatu partikel dinyatakan dengan rumus


$$s=f(t)=(3t+1)^{\frac{1}{2}}$$   ( s dalam meter dan t dalam detik).  
   Kecepatan partikel tersebut pada saat t=8 adalah ... m/detik.  

   Penyelesaian:  

\>function f(t) &= (3\*t+1)^(1/2); $f(t) 


$$\sqrt{3\,t+1}$$\>function df(t) &= diff(f(t),t); $df(t)


$$\frac{3}{2\,\sqrt{3\,t+1}}$$\>$df(8); fraction %


$$\frac{3}{10}$$  Jadi, kecepatan partikel tersebut pada saat t=8 adalah 3/10 m/detik.  

2. Sebuah pabrik baju memerlukan x meter kain untuk diproduksi yang
dinyatakan dengan fungsi:


$$P(x)={\frac{1}{3}}x^2-12x+150$$   (dalam juta rupiah).  
   Berapa biaya produksi minimum yang dikeluarkan oleh pabrik baju  

tersebut?


   Penyelesaian:  

\>function P(x) &= (1/3)\*x^2-12\*x+150; $P(x)


$$\frac{x^2}{3}-12\,x+150$$\>function dP(x) &= diff(P(x),x); $dP(x)


$$\frac{2\,x}{3}-12$$   P(x) akan bernilai minimum jika P'(x)=0, maka:  

\>$dP(x)=0


$$\frac{2\,x}{3}-12=0$$\>$&solve(dP(x),x)


$$\left[ x=18 \right] $$   Dengan demikian, biaya produksinya adalah:  

\>P(18)


    42

   Jadi, biaya produksi minimum yang dikeluarkan oleh pabrik tersebut  

adalah 42 juta rupiah.


3. Sebuah peluru ditembakkan ke atas. Jika tinggi h meter setelah t


   detik dirumuskan dengan


$$h(t)=120t-5t^2$$   maka berapa tinggi maksimum yang dicapai peluru tersebut?  

   Penyelesaian:  
   Diketahui:  

$$h(t)=120t-5t^2$$   Turunan pertama fungsi h adalah  

\>function h(t) &= 120\*t-5\*t^2; $h(t)


$$120\,t-5\,t^2$$\>function dh(t) &= diff(h(t),t); $dh(t)


$$120-10\,t$$   Nilai t akan maksimum saat  

\>$dh(t)=0


$$120-10\,t=0$$\>$&solve(dh(t),t)


$$\left[ t=12 \right] $$   Ketinggian maksimum yang dapat dicapai peluru saat t=12, yaitu  

\>$h(12)


$$720$$   Jadi, ketinggian maksimum peluru adalah 720 meter.  

## Soal-soal Latihan

1. Cari f'(4) dari fungsi


$$f(x) = \frac {2x-1}{x^2-x}$$\>function f(x) &= (2\*x-1)/(x^2-x); $f(x)


$$\frac{2\,x-1}{x^2-x}$$\>function df(x) &= diff(f(x), x); $df(x)


$$\frac{2}{x^2-x}-\frac{\left(2\,x-1\right)^2}{\left(x^2-x\right)^2}$$\>df(4); fraction %


    -25/144

2. Cari turunan dari


$$g(x)=x^2.sin(x)$$\>function g(x) &= x^2\*sin(x); $g(x)


$$x^2\,\sin x$$\>function dg(x) &= diff (g(x), x); $dg(x)


$$2\,x\,\sin x+x^2\,\cos x$$3. Cari turunan dari


$$(4x-7)^2(2x+3)$$\>function f(x) &= (4\*x-7)^2\*(2\*x+3); $f(x) 


$$\left(2\,x+3\right)\,\left(4\,x-7\right)^2$$\>function df(x) &= diff(f(x), x); $df(x)


$$2\,\left(4\,x-7\right)^2+8\,\left(2\,x+3\right)\,\left(4\,x-7
 \right)$$\>F &= expand(df(x))|simplify; $F


$$96\,x^2-128\,x-70$$4. Temukan turunan dari


$$f(x)=ln(x^3+3x-4)$$5. Tentukan turunan dari


$$f(x)=cos(5x)+sin(2x)$$6. Sebuah kembang api diluncurkan ke udara. Ketinggian kembang api


   h=(t) (dalam meter) pada t sekon dimodelkan dengan


$$f(t)=16t^2+200t+4$$   Tentukan kecepatan luncur kembang api saat t= 3 sekon.  

# 4. Integral Tak Tentu

EMT dapat digunakan untuk menghitung integral, baik integral tak tentu
maupun integral tentu.


Pada notebook ini akan ditunjukkan perhitungan integral tentu dengan
menggunakan Teorema Dasar Kalkulus:


Fungsi untuk menentukan integral adalah integrate. Fungsi ini dapat
digunakan untuk menentukan, baik integral tentu maupun tak tentu (jika
fungsinya memiliki antiderivatif).


## CAKUPAN PEMBAHASAN

Definisi


Cara menulis integral pada EMT


Sifat-sifat


Rumus


Kurva


## DEFINISI

Integral Tak Tentu adalah bentuk integral yang variabel integrasinya
tidak memiliki batas sehingga integrasi dari sebuah fungsi akan
menghasilkan banyak kemungkinan dan hanya dinyatakan sebagai
penyelesaian umum. Istilah tak tentu berarti bentuk fungsi F(x) memuat
konstanta real sebarang.


Misalkan diketahui suatu fungsi F(x) yang merupakan fungsi umum yang
memiliki sifat F'(x)=f(x), maka integral tak tentu merupakan himpunan
anti turunan F(x) dari f(x) pada interval negatif tak hingga sampai
positif tak hingga yang dinotasikan :


$$F(x) = \int f(x) dx+c$$## MENULIS INTEGRAL PADA LATEX



Untuk menulis dengan Latex menggunakan fungsi \int


$$f(x)= \int x^3 dx$$$$\int 15x^7 dx$$$$\int x^4 dx$$$$\int 7x^3 dx$$$$\int 5x dx$$## SIFAT INTEGRAL TAK TENTU

1. Sifat Pangkat


   Jika n adalah sembarang bilangan rasional kecuali -1, maka integral
tak tentu dari x^n ditulis :


$$\int x^n dx+c=\frac{x^{n+1}}{n+1} +c$$Contoh:


$$\int x^2 dx+c=\frac{x^{2+1}}{2+1} +c =\frac{x^3}{3} +c$$2. Penjumlahan dan Pengurangan


$$\int[g(x)+f(x)]dx = \int g(x) dx + \int f(x)dx$$$$\int [x^2+4x] dx = \int x^2 dx + \int 4x dx$$$$\int[g(x)-f(x)]dx = \int g(x) dx - \int f(x)dx$$$$\int [x^7-3x] dx = \int x^7 dx - \int 3x dx$$3. Perkalian


Bayangkan f(x) dan g(x) adalah dua fungsi yang bisa kita hitung
integral tak tentu (artinya kita mencari antiturunannya), dan anggap k
adalah suatu angka tetap (konstanta). Maka aturannya berlaku:


$$\int kf(x)dx=k \int f(x)dx$$$$\int 4x^2dx=4 \int x^2dx$$## RUMUS INTEGRAL TAK TENTU



Integral tak tentu berarti nilai atau batasannya belum pasti, sehingga
ada nilai konstanta(c) di dalamnya. Jadi rumus dasar integral tak
tentu adalah :


\>$showev('integrate(x^n,x)+c)


    Answering "Is n equal to -1?" with "no"

$$\int {x^{n}}{\;dx}+c=\frac{x^{n+1}}{n+1}+c$$\>$showev('integrate(x^-1,x)+c)


$$\int {\frac{1}{x}}{\;dx}+c=\log x+c$$Integral dari fungsi


$$f(x)=x^{-1}$$

menghasilkan fungsi ln karena berasal dari teorema kalkulus


## KURVA FUNGSI INTEGRAL/ANTITURUNAN

Kurva fungsi antiturunan adalah kurva yang menggambarkan hubungan
antara suatu fungsi dan antiturunannya. Antiturunan, juga dikenal
sebagai integral.


Jangan lupa untuk menuliskan terhadap variabel apa suatu fungsi
tersebut diintegralkan


1. kurva antiturunan dari fungsi aljabar


$$ f(x)=4x^3 dx$$\> 


2. kurva antiderivatif fungsi trigonometri dengan


$$f(x)= cos(x)$$3. kurva antiderivatif dari fungsi eksponensial dengan


$$f(x)=x e^x$$\>$showev('integrate(x\*E^x,x)+c)


$$\int {x\,e^{x}}{\;dx}+c=\left(x-1\right)\,e^{x}+c$$\>plot2d(["x\*E^x","(x-1)E^x+1","(x-1)E^x+2","(x-1)E^x+3","(x-1)E^x+4"]):


![images/EMTKalkulus_kelompok%204-292.png](images/EMTKalkulus_kelompok%204-292.png)

4. kurva antiderivatif dari fungsi logaritma dengan


\>$showev('integrate(log(4\*x),x)+c)


$$\int {\log \left(4\,x\right)}{\;dx}+c=\frac{4\,x\,\log \left(4\,x
 \right)-4\,x}{4}+c$$\>plot2d(["log(4\*x)","(4\*x)log(4\*x)-4\*x/4 +1","(4\*x)log(4\*x)-4\*x/4 +2","(4\*x)log(4\*x)-4\*x/4 +3"]):


![images/EMTKalkulus_kelompok%204-294.png](images/EMTKalkulus_kelompok%204-294.png)

## LATIHAN SOAL

1. Tuliskan integral tak tentu dari fungsi aljabar berikut serta
buatlah grafiknya :


$$f(x)=x^5$$\> 


2. tentukan integral tak tentu dari fungsi aljabar berikut :


$$f(x)=9x^2$$3. tentukan integral tak tentu dari fungsi trigonometri berikut :


$$f(x)= 2 sin x$$\> 


4. tentukan integral tak tentu dari fungsi trigonometri berikut :


$$f(x)= sin x - cos x$$\> 


5. tentukan integral tak tentu dari fungsi eksponensial berikut :


$$f(x)=e^{2x}$$\> 


6. tentukan integral tak tentu dari fungsi eksponensial berikut :


$$f(x)=x e^x$$7. Tentukan integral tak tentu dari fungsi


$$\int \frac{\sin(x)}{x} \, dx$$Jawaban dari integral tersebut melibatkan fungsi gamma tidak lengkap
(incomplete gamma function) dengan bilangan kompleks. Hasil ini muncul
karena fungsi dari


$$\frac{sin(x)}{x}$$

tidak memiliki antiturunan dalam bentuk fungsi elementer, sehingga
pada software Euler Mat Toolbox mengembalikan solusi dalam bentuk
fungsi khusus yang lebih umum, seperti fungsi gamma tidak lengkap
dalam kasus ini.


8.


# Integral Tentu

## Pengertian Integral Tentu

Kata “tentu” di sini bermakna sudah pasti atau sudah ditentukan. Oleh
karena itu, Integral tentu adalah integral yang sudah ditentukan
batasan nilai awal dan akhirnya. Batas dari integral tentu adalah a
sampai b atau batas atas sampai batas bawah.


## Rumus Integral Tentu

$$\int_a^b f(x)\ dx = F(b)-F(a), \quad \text{ dengan  } F'(x) = f(x).$$Contoh:


carilah


$$\int_0^\pi sin(x)\ dx$$\>$showev('integrate(sin(x),x,a,b))


$$\int_{a}^{b}{\sin x\;dx}=\cos a-\cos b$$\>$showev('integrate(sin(x),x,0,pi))


$$\int_{0}^{\pi}{\sin x\;dx}=2$$\>plot2d("sin(x)",0,pi):


![images/EMTKalkulus_kelompok%204-307.png](images/EMTKalkulus_kelompok%204-307.png)

Carilah


$$\int_0^2 x^2 \sqrt{2x+1} dx$$\>$showev('integrate(x^2\*sqrt(2\*x+1),x))


$$\int {x^2\,\sqrt{2\,x+1}}{\;dx}=\frac{\left(2\,x+1\right)^{\frac{7
 }{2}}}{28}-\frac{\left(2\,x+1\right)^{\frac{5}{2}}}{10}+\frac{\left(
 2\,x+1\right)^{\frac{3}{2}}}{12}$$\>$showev('integrate(x^2\*sqrt(2\*x+1),x,0,2))


$$\int_{0}^{2}{x^2\,\sqrt{2\,x+1}\;dx}=\frac{2\,5^{\frac{5}{2}}}{21}-
 \frac{2}{105}$$\>$ratsimp(%)


$$\int_{0}^{2}{x^2\,\sqrt{2\,x+1}\;dx}=\frac{2\,5^{\frac{7}{2}}-2}{
 105}$$\>$showev('integrate((sin(sqrt(x)+a)\*E^sqrt(x))/sqrt(x),x,0,pi^2))


$$\int_{0}^{\pi^2}{\frac{\sin \left(\sqrt{x}+a\right)\,e^{\sqrt{x}}}{
 \sqrt{x}}\;dx}=\left(-e^{\pi}-1\right)\,\sin a+\left(e^{\pi}+1
 \right)\,\cos a$$\>$factor(%)


$$\int_{0}^{\pi^2}{\frac{\sin \left(\sqrt{x}+a\right)\,e^{\sqrt{x}}}{
 \sqrt{x}}\;dx}=\left(-e^{\pi}-1\right)\,\left(\sin a-\cos a\right)$$\>function map f(x) &= E^(-x^2)


    
                                        2
                                     - x
                                    E
    

\>s$showev('integrate(f(x),x))


    Syntax error in expression, or unfinished expression!
    Error in:
    s$showev('integrate(f(x),x)) ...
             ^

Fungsi f tidak memiliki antiturunan, integralnya masih memuat integral
lain.


$$erf(x) = \int \frac{e^{-x^2}}{\sqrt{\pi}} \ dx.$$Kita tidak dapat menggunakan teorema Dasar kalkulus untuk menghitung
integral tentu fungsi tersebut jika semua batasnya berhingga. Dalam
hal ini dapat digunakan metode numerik (rumus kuadratur).


Misalkan kita akan menghitung:


$$\int_{0}^{\pi}{e^ {- x^2 }\;dx}$$\>x=0:0.1:pi-0.1; plot2d(x,f(x+0.1),\>bar); plot2d("f(x)",0,pi,\>add):


![images/EMTKalkulus_kelompok%204-316.png](images/EMTKalkulus_kelompok%204-316.png)

Integral tentu


$$\int_{0}^{\pi}{e^ {- x^2 }\;dx}$$dapat dihampiri dengan jumlah luas persegi-persegi panjang di bawah
kurva y=f(x) tersebut. Langkah-langkahnya adalah sebagai berikut.


\>t &= makelist(a,a,0,pi-0.1,0.1);


 mendefinisikan t sebagai list untuk menyimpan nilai-nilai x  

\>fx &= makelist(f(t[i]+0.1),i,1,length(t)); 


simpan nilai-nilai f(x) dan jangan menggunakan x sebagai list


Hasilnya adalah:


$$\int_{0}^{\pi}{e^ {- x^2 }\;dx}=0.1950839272901491$$Jumlah tersebut diperoleh dari hasil kali lebar sub-subinterval (=0.1)
dan jumlah nilai-nilai f(x) untuk x = 0.1, 0.2, 0.3, ..., 3.2.


\>0.1\*sum(f(x+0.1))


    0.836219610253

Untuk mendapatkan nilai integral tentu yang mendekati nilai
sebenarnya, lebar sub-intervalnya dapat diperkecil lagi, sehingga
daerah di bawah kurva tertutup semuanya, misalnya dapat digunakan
lebar subinterval 0.001.


\>x=0:0.001:pi-0.1; plot2d(x,f(x+0.1),\>bar); plot2d("f(x)",0,pi,\>add):


![images/EMTKalkulus_kelompok%204-319.png](images/EMTKalkulus_kelompok%204-319.png)

Berikut adalah contoh lain fungsi yang tidak memiliki antiderivatif,
sehingga integral tentunya hanya dapat dihitung dengan metode numerik.


\>function f(x) &= x^x


    
                                       x
                                      x
    

\>$showev('integrate(f(x),x,0,1))


$$\int_{0}^{1}{x^{x}\;dx}=\int_{0}^{1}{x^{x}\;dx}$$\>x=0:0.1:1-0.01; plot2d(x,f(x+0.01),\>bar); plot2d("f(x)",0,1,\>add):


![images/EMTKalkulus_kelompok%204-321.png](images/EMTKalkulus_kelompok%204-321.png)

Karena maxima gagal menghitung integral tentu tersebut secara langsung
menggunakan perintah integrate. Untuk mendapat hasil atau pendekatan
nilai integral tentu tersebut kita lakukan seperti contoh sebelumnya.


\>t &= makelist(a,a,0,1-0.01,0.01);

\>fx &= makelist(f(t[i]+0.01),i,1,length(t)); 


$$\int_{0}^{1}{x^{x}\;dx}=0.7834935879025506$$\>function f(x) &= sin(3\*x^5+7)^2; $f(x)


$$\sin ^2\left(3\,x^5+7\right)$$\>integrate(f,0,1)


    0.542581176074

## Sifat - Sifat Integral Tentu

1. Linearitas


sifat 1: Jika c adalah konstanta, maka:


$$\int_a^b c f(x) dx = c \int_a^b f(x) dx$$

Sifat 2: Jika f(x) dan g(x) adalah dua fungsi yang terintegralkan pada
interval [a, b], maka:


$$\int_a^b (f(x) + g(x)) dx = \int_a^b f(x) dx + \int_a^b g(x) dx$$2. Interval


Sifat 3: Jika a &lt; c &lt; b, maka:


$$\int_a^b f(x) dx = \int_a^c f(x) dx + \int_c^b f(x) dx$$3. Fungsi Genap dan Ganjil


Fungsi Genap: Jika f(x) adalah fungsi genap (yaitu, f(-x) = f(x)),
maka:


$$\int_{-a}^a f(x) dx = 2 \int_0^a f(x) dx$$

Fungsi Ganjil: Jika f(x) adalah fungsi ganjil (yaitu, f(-x) = -f(x)),
maka:


$$\int_{-a}^a f(x) dx = 0$$4. Batas Integral Bertukar


$$\int_b^a f(x) dx = -\int_a^b f(x) dx$$## Aplikasi Integral Tentu

## Aplikasi Integral Tentu pada Panjang Kurva

Sebuah jalan tol memiliki bentuk lengkungan yang dapat dimodelkan
dengan persamaan y = x^2 dari titik x = 0 hingga x = 2 (dalam
kilometer). Berapakah panjang jalan tol tersebut


Penyelesaian:


$$s = \int_0^2 \sqrt{1 + (2x)^2} dx$$\>$showev('integrate(sqrt(1 + (2\*x)^2),x,0,2))


$$\int_{0}^{2}{\sqrt{4\,x^2+1}\;dx}=\frac{{\rm asinh}\; 4+4\,\sqrt{17
 }}{4}$$\>$float(%)


$$\int_{0.0}^{2.0}{\sqrt{4.0\,x^2+1.0}\;dx}=4.646783762432936$$Hitunglah panjang kurva berikut ini dan luas daerah di dalam kurva
tersebut.


$$\gamma(t) = (r(t) \cos(t), r(t) \sin(t))$$dengan


$$r(t) = 1 + \dfrac{\sin(3t)}{2},\quad 0\le t\le 2\pi.$$\>t=linspace(0,2pi,1000); r=1+sin(3\*t)/2; x=r\*cos(t); y=r\*sin(t); ...  
\>   plot2d(x,y,\>filled,fillcolor=red,style="/",r=1.5): // Kita gambar kurvanya terlebih dahulu


![images/EMTKalkulus_kelompok%204-335.png](images/EMTKalkulus_kelompok%204-335.png)

\>function r(t) &= 1+sin(3\*t)/2; $'r(t)=r(t)


$$r\left(\left[ 0 , 0.01 , 0.02 , 0.03 , 0.04 , 0.05 , 0.06 , 0.07 , 
 0.08 , 0.09 , 0.1 , 0.11 , 0.12 , 0.13 , 0.14 , 0.15 , 0.16 , 0.17
  , 0.18 , 0.19 , 0.2 , 0.21 , 0.2200000000000001 , 
 0.2300000000000001 , 0.2400000000000001 , 0.2500000000000001 , 
 0.2600000000000001 , 0.2700000000000001 , 0.2800000000000001 , 
 0.2900000000000001 , 0.3000000000000001 , 0.3100000000000001 , 
 0.3200000000000001 , 0.3300000000000001 , 0.3400000000000001 , 
 0.3500000000000001 , 0.3600000000000002 , 0.3700000000000002 , 
 0.3800000000000002 , 0.3900000000000002 , 0.4000000000000002 , 
 0.4100000000000002 , 0.4200000000000002 , 0.4300000000000002 , 
 0.4400000000000002 , 0.4500000000000002 , 0.4600000000000002 , 
 0.4700000000000003 , 0.4800000000000003 , 0.4900000000000003 , 
 0.5000000000000002 , 0.5100000000000002 , 0.5200000000000002 , 
 0.5300000000000002 , 0.5400000000000003 , 0.5500000000000003 , 
 0.5600000000000003 , 0.5700000000000003 , 0.5800000000000003 , 
 0.5900000000000003 , 0.6000000000000003 , 0.6100000000000003 , 
 0.6200000000000003 , 0.6300000000000003 , 0.6400000000000003 , 
 0.6500000000000004 , 0.6600000000000004 , 0.6700000000000004 , 
 0.6800000000000004 , 0.6900000000000004 , 0.7000000000000004 , 
 0.7100000000000004 , 0.7200000000000004 , 0.7300000000000004 , 
 0.7400000000000004 , 0.7500000000000004 , 0.7600000000000005 , 
 0.7700000000000005 , 0.7800000000000005 , 0.7900000000000005 , 
 0.8000000000000005 , 0.8100000000000005 , 0.8200000000000005 , 
 0.8300000000000005 , 0.8400000000000005 , 0.8500000000000005 , 
 0.8600000000000005 , 0.8700000000000006 , 0.8800000000000006 , 
 0.8900000000000006 , 0.9000000000000006 , 0.9100000000000006 , 
 0.9200000000000006 , 0.9300000000000006 , 0.9400000000000006 , 
 0.9500000000000006 , 0.9600000000000006 , 0.9700000000000006 , 
 0.9800000000000006 , 0.9900000000000007 \right] \right)=\left[ 1 , 
 1.014997750101248 , 1.029982003239722 , 1.044939274599006 , 
 1.05985610364446 , 1.0747190662368 , 1.089514786712912 , 
 1.10422994992305 , 1.118851313213567 , 1.133365718344415 , 
 1.14776010333067 , 1.162021514197434 , 1.176137116637545 , 
 1.190094207561581 , 1.203880226529785 , 1.217482767055615 , 
 1.230889587770742 , 1.244088623441454 , 1.257067995826556 , 
 1.269816024366985 , 1.282321236697518 , 1.294572378971135 , 
 1.306558425986717 , 1.318268591110984 , 1.329692335985737 , 
 1.340819380011667 , 1.351639709600205 , 1.362143587185071 , 
 1.37232155998543 , 1.382164468512753 , 1.391663454813742 , 
 1.400809970441889 , 1.409595784150499 , 1.41801298930026 , 
 1.426054010974682 , 1.433711612797009 , 1.440978903442474 , 
 1.447849342840024 , 1.454316748057942 , 1.460375298868068 , 
 1.466019542983613 , 1.471244400965849 , 1.476045170795258 , 
 1.480417532103036 , 1.484357550059133 , 1.48786167891333 , 
 1.49092676518618 , 1.493550050506925 , 1.495729174095843 , 
 1.49746217488879 , 1.498747493302027 , 1.499583972635738 , 
 1.499970860114983 , 1.499907807567145 , 1.499394871735262 , 
 1.498432514226959 , 1.497021601099038 , 1.495163402078079 , 
 1.492859589417777 , 1.490112236394023 , 1.486923815439098 , 
 1.483297195916649 , 1.479235641539457 , 1.474742807432315 , 
 1.469822736842662 , 1.464479857501934 , 1.458718977640905 , 
 1.4525452816626 , 1.44596432547669 , 1.438982031499539 , 
 1.431604683324436 , 1.423838920066784 , 1.415691730389341 , 
 1.407170446212898 , 1.398282736118043 , 1.38903659844396 , 
 1.379440354090461 , 1.369502639029735 , 1.359232396534563 , 
 1.348638869129968 , 1.337731590275575 , 1.326520375786132 , 
 1.315015314997945 , 1.303226761689157 , 1.29116532476204 , 
 1.278841858695708 , 1.26626745377781 , 1.253453426124026 , 
 1.240411307494323 , 1.227152834915152 , 1.213689940116914 , 
 1.200034738796209 , 1.186199519712527 , 1.172196733629194 , 
 1.158038982108526 , 1.143739006171271 , 1.129309674830555 , 
 1.114763973510631 , 1.100114992360884 , 1.085375914475572 \right] $$\>function fx(t) &= r(t)\*cos(t); $'fx(t)=fx(t)


$${\it fx}\left(\left[ 0 , 0.01 , 0.02 , 0.03 , 0.04 , 0.05 , 0.06 , 
 0.07 , 0.08 , 0.09 , 0.1 , 0.11 , 0.12 , 0.13 , 0.14 , 0.15 , 0.16
  , 0.17 , 0.18 , 0.19 , 0.2 , 0.21 , 0.2200000000000001 , 
 0.2300000000000001 , 0.2400000000000001 , 0.2500000000000001 , 
 0.2600000000000001 , 0.2700000000000001 , 0.2800000000000001 , 
 0.2900000000000001 , 0.3000000000000001 , 0.3100000000000001 , 
 0.3200000000000001 , 0.3300000000000001 , 0.3400000000000001 , 
 0.3500000000000001 , 0.3600000000000002 , 0.3700000000000002 , 
 0.3800000000000002 , 0.3900000000000002 , 0.4000000000000002 , 
 0.4100000000000002 , 0.4200000000000002 , 0.4300000000000002 , 
 0.4400000000000002 , 0.4500000000000002 , 0.4600000000000002 , 
 0.4700000000000003 , 0.4800000000000003 , 0.4900000000000003 , 
 0.5000000000000002 , 0.5100000000000002 , 0.5200000000000002 , 
 0.5300000000000002 , 0.5400000000000003 , 0.5500000000000003 , 
 0.5600000000000003 , 0.5700000000000003 , 0.5800000000000003 , 
 0.5900000000000003 , 0.6000000000000003 , 0.6100000000000003 , 
 0.6200000000000003 , 0.6300000000000003 , 0.6400000000000003 , 
 0.6500000000000004 , 0.6600000000000004 , 0.6700000000000004 , 
 0.6800000000000004 , 0.6900000000000004 , 0.7000000000000004 , 
 0.7100000000000004 , 0.7200000000000004 , 0.7300000000000004 , 
 0.7400000000000004 , 0.7500000000000004 , 0.7600000000000005 , 
 0.7700000000000005 , 0.7800000000000005 , 0.7900000000000005 , 
 0.8000000000000005 , 0.8100000000000005 , 0.8200000000000005 , 
 0.8300000000000005 , 0.8400000000000005 , 0.8500000000000005 , 
 0.8600000000000005 , 0.8700000000000006 , 0.8800000000000006 , 
 0.8900000000000006 , 0.9000000000000006 , 0.9100000000000006 , 
 0.9200000000000006 , 0.9300000000000006 , 0.9400000000000006 , 
 0.9500000000000006 , 0.9600000000000006 , 0.9700000000000006 , 
 0.9800000000000006 , 0.9900000000000007 \right] \right)=\left[ 1 , 
 1.014947000636657 , 1.029776013705529 , 1.044469087191079 , 
 1.059008331806833 , 1.073375947255439 , 1.087554248364218 , 
 1.101525691055367 , 1.11527289811021 , 1.128778684687222 , 
 1.142026083553954 , 1.154998369993414 , 1.16767908634602 , 
 1.180052066148761 , 1.192101457833886 , 1.203811747950136 , 
 1.215167783870255 , 1.226154795949382 , 1.236758419099762 , 
 1.246964713748154 , 1.256760186143285 , 1.266131807981756 , 
 1.275067035321848 , 1.283553826755846 , 1.29158066081265 , 
 1.29913655256367 , 1.306211069406282 , 1.312794346000405 , 
 1.318877098335118 , 1.324450636903608 , 1.329506878966172 , 
 1.334038359882425 , 1.338038243495345 , 1.341500331551311 , 
 1.344419072141793 , 1.346789567153917 , 1.348607578718725 , 
 1.349869534647481 , 1.350572532848044 , 1.350714344714907 , 
 1.350293417488142 , 1.349308875578123 , 1.347760520854542 , 
 1.345648831899879 , 1.342974962229111 , 1.339740737479097 , 
 1.335948651572729 , 1.331601861864506 , 1.326704183275865 , 
 1.321260081430156 , 1.315274664798767 , 1.308753675871437 , 
 1.301703481365363 , 1.294131061489226 , 1.286043998279732 , 
 1.277450463029762 , 1.268359202828647 , 1.25877952623647 , 
 1.248721288115691 , 1.238194873644713 , 1.227211181539273 , 
 1.215781606508839 , 1.203918020976346 , 1.191632756090801 , 
 1.17893858206338 , 1.165848687858719 , 1.152376660274093 , 
 1.138536462440146 , 1.124342411777761 , 1.10980915744646 , 
 1.094951657320579 , 1.079785154530145 , 1.064325153604093 , 
 1.04858739625406 , 1.032587836837555 , 1.0163426175398 , 
 0.999868043313951 , 0.9831805566197906 , 0.9662967120012925 , 
 0.9492331505436565 , 0.932006574250646 , 0.9146337203831 , 
 0.897131335799599 , 0.8795161513401855 , 0.8618048562939812 , 
 0.8440140729913906 , 0.8261603315613344 , 0.8082600448937051 , 
 0.7903294838468643 , 0.7723847527396025 , 0.754441765166499 , 
 0.7365162201750889 , 0.7186235788426429 , 0.7007790412897039 , 
 0.6829975241668103 , 0.6652936386500562 , 0.6476816689803099 , 
 0.6301755515800127 , 0.6127888547805567 , 0.595534759192214 \right] $$\>function fy(t) &= r(t)\*sin(t); $'fy(t)=fy(t)


$${\it fy}\left(\left[ 0 , 0.01 , 0.02 , 0.03 , 0.04 , 0.05 , 0.06 , 
 0.07 , 0.08 , 0.09 , 0.1 , 0.11 , 0.12 , 0.13 , 0.14 , 0.15 , 0.16
  , 0.17 , 0.18 , 0.19 , 0.2 , 0.21 , 0.2200000000000001 , 
 0.2300000000000001 , 0.2400000000000001 , 0.2500000000000001 , 
 0.2600000000000001 , 0.2700000000000001 , 0.2800000000000001 , 
 0.2900000000000001 , 0.3000000000000001 , 0.3100000000000001 , 
 0.3200000000000001 , 0.3300000000000001 , 0.3400000000000001 , 
 0.3500000000000001 , 0.3600000000000002 , 0.3700000000000002 , 
 0.3800000000000002 , 0.3900000000000002 , 0.4000000000000002 , 
 0.4100000000000002 , 0.4200000000000002 , 0.4300000000000002 , 
 0.4400000000000002 , 0.4500000000000002 , 0.4600000000000002 , 
 0.4700000000000003 , 0.4800000000000003 , 0.4900000000000003 , 
 0.5000000000000002 , 0.5100000000000002 , 0.5200000000000002 , 
 0.5300000000000002 , 0.5400000000000003 , 0.5500000000000003 , 
 0.5600000000000003 , 0.5700000000000003 , 0.5800000000000003 , 
 0.5900000000000003 , 0.6000000000000003 , 0.6100000000000003 , 
 0.6200000000000003 , 0.6300000000000003 , 0.6400000000000003 , 
 0.6500000000000004 , 0.6600000000000004 , 0.6700000000000004 , 
 0.6800000000000004 , 0.6900000000000004 , 0.7000000000000004 , 
 0.7100000000000004 , 0.7200000000000004 , 0.7300000000000004 , 
 0.7400000000000004 , 0.7500000000000004 , 0.7600000000000005 , 
 0.7700000000000005 , 0.7800000000000005 , 0.7900000000000005 , 
 0.8000000000000005 , 0.8100000000000005 , 0.8200000000000005 , 
 0.8300000000000005 , 0.8400000000000005 , 0.8500000000000005 , 
 0.8600000000000005 , 0.8700000000000006 , 0.8800000000000006 , 
 0.8900000000000006 , 0.9000000000000006 , 0.9100000000000006 , 
 0.9200000000000006 , 0.9300000000000006 , 0.9400000000000006 , 
 0.9500000000000006 , 0.9600000000000006 , 0.9700000000000006 , 
 0.9800000000000006 , 0.9900000000000007 \right] \right)=\left[ 0 , 
 0.01014980833556662 , 0.02059826678292271 , 0.03134347622283015 , 
 0.04238293991838228 , 0.05371356612987439 , 0.06533167172990376 , 
 0.07723298681299934 , 0.08941266029246918 , 0.1018652664755576 , 
 0.1145848126064173 , 0.1275647473648353 , 0.1407979703071057 , 
 0.1542768422339107 , 0.1679931964685752 , 0.1819383510275811 , 
 0.1961031216637831 , 0.2104778357613507 , 0.2250523470600841 , 
 0.2398160511854019 , 0.2547579019589912 , 0.2698664284638497 , 
 0.2851297528362152 , 0.3005356087557041 , 0.3160713606038417 , 
 0.3317240232600813 , 0.3474802825033731 , 0.3633265159863522 , 
 0.3792488147482899 , 0.3952330052320643 , 0.411264671769591 , 
 0.4273291794993832 , 0.4434116976792021 , 0.4594972233561165 , 
 0.4755706053556919 , 0.4916165685515136 , 0.5076197383757777 , 
 0.5235646655312819 , 0.5394358508648145 , 0.5552177703616642 , 
 0.5708949002207642 , 0.5864517419698421 , 0.6018728475798654 , 
 0.6171428445380648 , 0.6322464608388652 , 0.6471685498521687 , 
 0.6618941150286309 , 0.6764083344018014 , 0.6906965848473219 , 
 0.704744466059751 , 0.7185378242080237 , 0.7320627752310482 , 
 0.7453057277355214 , 0.7582534054586558 , 0.7708928692592016 , 
 0.7832115386008901 , 0.7951972124932317 , 0.8068380898554457 , 
 0.8181227892702304 , 0.8290403680950348 , 0.8395803408995157 , 
 0.8497326971989371 , 0.8594879184543822 , 0.8688369943118147 , 
 0.877771438053233 , 0.8862833012344233 , 0.894365187485098 , 
 0.9020102654485477 , 0.9092122808393135 , 0.91596556759876 , 
 0.9222650581299157 , 0.9281062925943645 , 0.9334854272555032 , 
 0.9383992418539865 , 0.9428451460027243 , 0.9468211845903713 , 
 0.9503260421838114 , 0.9533590464217597 , 0.9559201703932094 , 
 0.9580100339960551 , 0.9596299042728891 , 0.9607816947225576 , 
 0.9614679635877484 , 0.9616919111204768 , 0.9614573758289937 , 
 0.9607688297112769 , 0.9596313724818526 , 0.9580507248003547 , 
 0.9560332205117796 , 0.9535857979100135 , 0.950715990037748 , 
 0.9474319140374602 , 0.9437422595696462 , 0.9396562763159917 , 
 0.9351837605866338 , 0.9303350410521015 , 0.9251209636219332 , 
 0.9195528754933222 , 0.9136426083945087 , 0.9074024610488752
  \right] $$\>function ds(t) &= trigreduce(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'ds(t)=ds(t)


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... e(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'ds(t)=ds(t ...
                                                         ^

\>$integrate(ds(x),x,0,2\*pi) //panjang (keliling) kurva


$$\int_{0}^{2\,\pi}{{\it ds}\left(x\right)\;dx}$$Maxima gagal melakukan perhitungan eksak integral tersebut.


Berikut kita hitung integralnya secara numerik dengan perintah EMT.


\>integrate("ds(x)",0,2\*pi)


Spiral Logaritmik


$$x=e^{ax}\cos x,\ y=e^{ax}\sin x.$$\>a=0.1; plot2d("exp(a\*x)\*cos(x)","exp(a\*x)\*sin(x)",r=2,xmin=0,xmax=2\*pi):


![images/EMTKalkulus_kelompok%204-341.png](images/EMTKalkulus_kelompok%204-341.png)

\>&kill(a) // hapus expresi a


    
                                     done
    

\>function fx(t) &= exp(a\*t)\*cos(t); $'fx(t)=fx(t)


$${\it fx}\left(\left[ 0 , 0.01 , 0.02 , 0.03 , 0.04 , 0.05 , 0.06 , 
 0.07 , 0.08 , 0.09 , 0.1 , 0.11 , 0.12 , 0.13 , 0.14 , 0.15 , 0.16
  , 0.17 , 0.18 , 0.19 , 0.2 , 0.21 , 0.2200000000000001 , 
 0.2300000000000001 , 0.2400000000000001 , 0.2500000000000001 , 
 0.2600000000000001 , 0.2700000000000001 , 0.2800000000000001 , 
 0.2900000000000001 , 0.3000000000000001 , 0.3100000000000001 , 
 0.3200000000000001 , 0.3300000000000001 , 0.3400000000000001 , 
 0.3500000000000001 , 0.3600000000000002 , 0.3700000000000002 , 
 0.3800000000000002 , 0.3900000000000002 , 0.4000000000000002 , 
 0.4100000000000002 , 0.4200000000000002 , 0.4300000000000002 , 
 0.4400000000000002 , 0.4500000000000002 , 0.4600000000000002 , 
 0.4700000000000003 , 0.4800000000000003 , 0.4900000000000003 , 
 0.5000000000000002 , 0.5100000000000002 , 0.5200000000000002 , 
 0.5300000000000002 , 0.5400000000000003 , 0.5500000000000003 , 
 0.5600000000000003 , 0.5700000000000003 , 0.5800000000000003 , 
 0.5900000000000003 , 0.6000000000000003 , 0.6100000000000003 , 
 0.6200000000000003 , 0.6300000000000003 , 0.6400000000000003 , 
 0.6500000000000004 , 0.6600000000000004 , 0.6700000000000004 , 
 0.6800000000000004 , 0.6900000000000004 , 0.7000000000000004 , 
 0.7100000000000004 , 0.7200000000000004 , 0.7300000000000004 , 
 0.7400000000000004 , 0.7500000000000004 , 0.7600000000000005 , 
 0.7700000000000005 , 0.7800000000000005 , 0.7900000000000005 , 
 0.8000000000000005 , 0.8100000000000005 , 0.8200000000000005 , 
 0.8300000000000005 , 0.8400000000000005 , 0.8500000000000005 , 
 0.8600000000000005 , 0.8700000000000006 , 0.8800000000000006 , 
 0.8900000000000006 , 0.9000000000000006 , 0.9100000000000006 , 
 0.9200000000000006 , 0.9300000000000006 , 0.9400000000000006 , 
 0.9500000000000006 , 0.9600000000000006 , 0.9700000000000006 , 
 0.9800000000000006 , 0.9900000000000007 \right] \right)=\left[ 1 , 
 0.9999500004166653\,e^{0.01\,a} , 0.9998000066665778\,e^{0.02\,a} , 
 0.9995500337489875\,e^{0.03\,a} , 0.9992001066609779\,e^{0.04\,a} , 
 0.9987502603949663\,e^{0.05\,a} , 0.9982005399352042\,e^{0.06\,a} , 
 0.9975510002532796\,e^{0.07\,a} , 0.9968017063026194\,e^{0.08\,a} , 
 0.9959527330119943\,e^{0.09\,a} , 0.9950041652780258\,e^{0.1\,a} , 
 0.9939560979566968\,e^{0.11\,a} , 0.9928086358538663\,e^{0.12\,a} , 
 0.9915618937147881\,e^{0.13\,a} , 0.9902159962126372\,e^{0.14\,a} , 
 0.9887710779360422\,e^{0.15\,a} , 0.9872272833756269\,e^{0.16\,a} , 
 0.9855847669095608\,e^{0.17\,a} , 0.9838436927881214\,e^{0.18\,a} , 
 0.9820042351172703\,e^{0.19\,a} , 0.9800665778412416\,e^{0.2\,a} , 
 0.9780309147241483\,e^{0.21\,a} , 0.9758974493306055\,e^{
 0.2200000000000001\,a} , 0.9736663950053748\,e^{0.2300000000000001\,
 a} , 0.9713379748520296\,e^{0.2400000000000001\,a} , 
 0.9689124217106447\,e^{0.2500000000000001\,a} , 0.9663899781345132\,
 e^{0.2600000000000001\,a} , 0.9637708963658905\,e^{
 0.2700000000000001\,a} , 0.9610554383107709\,e^{0.2800000000000001\,
 a} , 0.9582438755126972\,e^{0.2900000000000001\,a} , 
 0.955336489125606\,e^{0.3000000000000001\,a} , 0.9523335698857134\,e
 ^{0.3100000000000001\,a} , 0.9492354180824408\,e^{0.3200000000000001
 \,a} , 0.9460423435283869\,e^{0.3300000000000001\,a} , 
 0.9427546655283462\,e^{0.3400000000000001\,a} , 0.9393727128473789\,
 e^{0.3500000000000001\,a} , 0.9358968236779348\,e^{
 0.3600000000000002\,a} , 0.9323273456060344\,e^{0.3700000000000002\,
 a} , 0.9286646355765101\,e^{0.3800000000000002\,a} , 
 0.924909059857313\,e^{0.3900000000000002\,a} , 0.921060994002885\,e
 ^{0.4000000000000002\,a} , 0.917120822816605\,e^{0.4100000000000002
 \,a} , 0.9130889403123081\,e^{0.4200000000000002\,a} , 
 0.9089657496748851\,e^{0.4300000000000002\,a} , 0.9047516632199634\,
 e^{0.4400000000000002\,a} , 0.9004471023526768\,e^{
 0.4500000000000002\,a} , 0.8960524975255252\,e^{0.4600000000000002\,
 a} , 0.8915682881953289\,e^{0.4700000000000003\,a} , 
 0.886994922779284\,e^{0.4800000000000003\,a} , 0.8823328586101213\,e
 ^{0.4900000000000003\,a} , 0.8775825618903726\,e^{0.5000000000000002
 \,a} , 0.8727445076457512\,e^{0.5100000000000002\,a} , 
 0.8678191796776498\,e^{0.5200000000000002\,a} , 0.8628070705147609\,
 e^{0.5300000000000002\,a} , 0.857708681363824\,e^{0.5400000000000003
 \,a} , 0.8525245220595056\,e^{0.5500000000000003\,a} , 
 0.847255111013416\,e^{0.5600000000000003\,a} , 0.8419009751622686\,e
 ^{0.5700000000000003\,a} , 0.8364626499151868\,e^{0.5800000000000003
 \,a} , 0.8309406791001633\,e^{0.5900000000000003\,a} , 
 0.8253356149096781\,e^{0.6000000000000003\,a} , 0.8196480178454794\,
 e^{0.6100000000000003\,a} , 0.8138784566625338\,e^{
 0.6200000000000003\,a} , 0.8080275083121516\,e^{0.6300000000000003\,
 a} , 0.8020957578842924\,e^{0.6400000000000003\,a} , 
 0.7960837985490556\,e^{0.6500000000000004\,a} , 0.7899922314973649\,
 e^{0.6600000000000004\,a} , 0.783821665880849\,e^{0.6700000000000004
 \,a} , 0.7775727187509277\,e^{0.6800000000000004\,a} , 
 0.7712460149971063\,e^{0.6900000000000004\,a} , 0.7648421872844882\,
 e^{0.7000000000000004\,a} , 0.7583618759905079\,e^{
 0.7100000000000004\,a} , 0.7518057291408947\,e^{0.7200000000000004\,
 a} , 0.7451744023448701\,e^{0.7300000000000004\,a} , 
 0.7384685587295876\,e^{0.7400000000000004\,a} , 0.7316888688738206\,
 e^{0.7500000000000004\,a} , 0.7248360107409049\,e^{
 0.7600000000000005\,a} , 0.7179106696109431\,e^{0.7700000000000005\,
 a} , 0.7109135380122771\,e^{0.7800000000000005\,a} , 
 0.7038453156522357\,e^{0.7900000000000005\,a} , 0.696706709347165\,e
 ^{0.8000000000000005\,a} , 0.6894984329517466\,e^{0.8100000000000005
 \,a} , 0.6822212072876132\,e^{0.8200000000000005\,a} , 
 0.6748757600712667\,e^{0.8300000000000005\,a} , 0.6674628258413078\,
 e^{0.8400000000000005\,a} , 0.6599831458849817\,e^{
 0.8500000000000005\,a} , 0.6524374681640515\,e^{0.8600000000000005\,
 a} , 0.6448265472400008\,e^{0.8700000000000006\,a} , 
 0.6371511441985798\,e^{0.8800000000000006\,a} , 0.6294120265736964\,
 e^{0.8900000000000006\,a} , 0.6216099682706641\,e^{
 0.9000000000000006\,a} , 0.6137457494888111\,e^{0.9100000000000006\,
 a} , 0.6058201566434623\,e^{0.9200000000000006\,a} , 
 0.5978339822872978\,e^{0.9300000000000006\,a} , 0.5897880250310977\,
 e^{0.9400000000000006\,a} , 0.581683089463883\,e^{0.9500000000000006
 \,a} , 0.5735199860724561\,e^{0.9600000000000006\,a} , 
 0.5652995311603538\,e^{0.9700000000000006\,a} , 0.5570225467662168\,
 e^{0.9800000000000006\,a} , 0.548689860581587\,e^{0.9900000000000007
 \,a} \right] $$\>function fy(t) &= exp(a\*t)\*sin(t); $'fy(t)=fy(t)


$${\it fy}\left(\left[ 0 , 0.01 , 0.02 , 0.03 , 0.04 , 0.05 , 0.06 , 
 0.07 , 0.08 , 0.09 , 0.1 , 0.11 , 0.12 , 0.13 , 0.14 , 0.15 , 0.16
  , 0.17 , 0.18 , 0.19 , 0.2 , 0.21 , 0.2200000000000001 , 
 0.2300000000000001 , 0.2400000000000001 , 0.2500000000000001 , 
 0.2600000000000001 , 0.2700000000000001 , 0.2800000000000001 , 
 0.2900000000000001 , 0.3000000000000001 , 0.3100000000000001 , 
 0.3200000000000001 , 0.3300000000000001 , 0.3400000000000001 , 
 0.3500000000000001 , 0.3600000000000002 , 0.3700000000000002 , 
 0.3800000000000002 , 0.3900000000000002 , 0.4000000000000002 , 
 0.4100000000000002 , 0.4200000000000002 , 0.4300000000000002 , 
 0.4400000000000002 , 0.4500000000000002 , 0.4600000000000002 , 
 0.4700000000000003 , 0.4800000000000003 , 0.4900000000000003 , 
 0.5000000000000002 , 0.5100000000000002 , 0.5200000000000002 , 
 0.5300000000000002 , 0.5400000000000003 , 0.5500000000000003 , 
 0.5600000000000003 , 0.5700000000000003 , 0.5800000000000003 , 
 0.5900000000000003 , 0.6000000000000003 , 0.6100000000000003 , 
 0.6200000000000003 , 0.6300000000000003 , 0.6400000000000003 , 
 0.6500000000000004 , 0.6600000000000004 , 0.6700000000000004 , 
 0.6800000000000004 , 0.6900000000000004 , 0.7000000000000004 , 
 0.7100000000000004 , 0.7200000000000004 , 0.7300000000000004 , 
 0.7400000000000004 , 0.7500000000000004 , 0.7600000000000005 , 
 0.7700000000000005 , 0.7800000000000005 , 0.7900000000000005 , 
 0.8000000000000005 , 0.8100000000000005 , 0.8200000000000005 , 
 0.8300000000000005 , 0.8400000000000005 , 0.8500000000000005 , 
 0.8600000000000005 , 0.8700000000000006 , 0.8800000000000006 , 
 0.8900000000000006 , 0.9000000000000006 , 0.9100000000000006 , 
 0.9200000000000006 , 0.9300000000000006 , 0.9400000000000006 , 
 0.9500000000000006 , 0.9600000000000006 , 0.9700000000000006 , 
 0.9800000000000006 , 0.9900000000000007 \right] \right)=\left[ 0 , 
 0.009999833334166664\,e^{0.01\,a} , 0.01999866669333308\,e^{0.02\,a}
  , 0.02999550020249566\,e^{0.03\,a} , 0.03998933418663416\,e^{0.04\,
 a} , 0.04997916927067833\,e^{0.05\,a} , 0.0599640064794446\,e^{0.06
 \,a} , 0.06994284733753277\,e^{0.07\,a} , 0.0799146939691727\,e^{
 0.08\,a} , 0.08987854919801104\,e^{0.09\,a} , 0.09983341664682814\,e
 ^{0.1\,a} , 0.1097783008371748\,e^{0.11\,a} , 0.1197122072889193\,e
 ^{0.12\,a} , 0.1296341426196948\,e^{0.13\,a} , 0.1395431146442365\,e
 ^{0.14\,a} , 0.1494381324735992\,e^{0.15\,a} , 0.159318206614246\,e
 ^{0.16\,a} , 0.169182349066996\,e^{0.17\,a} , 0.1790295734258242\,e
 ^{0.18\,a} , 0.1888588949765006\,e^{0.19\,a} , 0.1986693307950612\,e
 ^{0.2\,a} , 0.2084598998460996\,e^{0.21\,a} , 0.2182296230808694\,e
 ^{0.2200000000000001\,a} , 0.2279775235351885\,e^{0.2300000000000001
 \,a} , 0.2377026264271347\,e^{0.2400000000000001\,a} , 
 0.247403959254523\,e^{0.2500000000000001\,a} , 0.2570805518921552\,e
 ^{0.2600000000000001\,a} , 0.2667314366888312\,e^{0.2700000000000001
 \,a} , 0.2763556485641138\,e^{0.2800000000000001\,a} , 
 0.2859522251048356\,e^{0.2900000000000001\,a} , 0.2955202066613397\,
 e^{0.3000000000000001\,a} , 0.3050586364434436\,e^{
 0.3100000000000001\,a} , 0.3145665606161179\,e^{0.3200000000000001\,
 a} , 0.3240430283948685\,e^{0.3300000000000001\,a} , 
 0.3334870921408145\,e^{0.3400000000000001\,a} , 0.3428978074554515\,
 e^{0.3500000000000001\,a} , 0.3522742332750901\,e^{
 0.3600000000000002\,a} , 0.3616154319649622\,e^{0.3700000000000002\,
 a} , 0.3709204694129828\,e^{0.3800000000000002\,a} , 
 0.3801884151231616\,e^{0.3900000000000002\,a} , 0.3894183423086507\,
 e^{0.4000000000000002\,a} , 0.3986093279844231\,e^{
 0.4100000000000002\,a} , 0.4077604530595704\,e^{0.4200000000000002\,
 a} , 0.416870802429211\,e^{0.4300000000000002\,a} , 
 0.4259394650659998\,e^{0.4400000000000002\,a} , 0.4349655341112304\,
 e^{0.4500000000000002\,a} , 0.44394810696552\,e^{0.4600000000000002
 \,a} , 0.4528862853790685\,e^{0.4700000000000003\,a} , 
 0.4617791755414831\,e^{0.4800000000000003\,a} , 0.4706258881711582\,
 e^{0.4900000000000003\,a} , 0.4794255386042032\,e^{
 0.5000000000000002\,a} , 0.4881772468829077\,e^{0.5100000000000002\,
 a} , 0.4968801378437369\,e^{0.5200000000000002\,a} , 
 0.5055333412048472\,e^{0.5300000000000002\,a} , 0.5141359916531133\,
 e^{0.5400000000000003\,a} , 0.5226872289306594\,e^{
 0.5500000000000003\,a} , 0.5311861979208836\,e^{0.5600000000000003\,
 a} , 0.5396320487339695\,e^{0.5700000000000003\,a} , 
 0.5480239367918738\,e^{0.5800000000000003\,a} , 0.556361022912784\,e
 ^{0.5900000000000003\,a} , 0.5646424733950356\,e^{0.6000000000000003
 \,a} , 0.5728674601004815\,e^{0.6100000000000003\,a} , 
 0.5810351605373053\,e^{0.6200000000000003\,a} , 0.5891447579422698\,
 e^{0.6300000000000003\,a} , 0.5971954413623923\,e^{
 0.6400000000000003\,a} , 0.6051864057360399\,e^{0.6500000000000004\,
 a} , 0.6131168519734341\,e^{0.6600000000000004\,a} , 
 0.6209859870365599\,e^{0.6700000000000004\,a} , 0.6287930240184688\,
 e^{0.6800000000000004\,a} , 0.6365371822219682\,e^{
 0.6900000000000004\,a} , 0.6442176872376913\,e^{0.7000000000000004\,
 a} , 0.651833771021537\,e^{0.7100000000000004\,a} , 
 0.6593846719714734\,e^{0.7200000000000004\,a} , 0.6668696350036982\,
 e^{0.7300000000000004\,a} , 0.6742879116281454\,e^{
 0.7400000000000004\,a} , 0.6816387600233345\,e^{0.7500000000000004\,
 a} , 0.6889214451105516\,e^{0.7600000000000005\,a} , 
 0.696135238627357\,e^{0.7700000000000005\,a} , 0.7032794192004105\,e
 ^{0.7800000000000005\,a} , 0.7103532724176082\,e^{0.7900000000000005
 \,a} , 0.7173560908995231\,e^{0.8000000000000005\,a} , 
 0.7242871743701429\,e^{0.8100000000000005\,a} , 0.7311458297268962\,
 e^{0.8200000000000005\,a} , 0.7379313711099631\,e^{
 0.8300000000000005\,a} , 0.7446431199708596\,e^{0.8400000000000005\,
 a} , 0.751280405140293\,e^{0.8500000000000005\,a} , 
 0.7578425628952773\,e^{0.8600000000000005\,a} , 0.7643289370255054\,
 e^{0.8700000000000006\,a} , 0.7707388788989696\,e^{
 0.8800000000000006\,a} , 0.7770717475268242\,e^{0.8900000000000006\,
 a} , 0.7833269096274837\,e^{0.9000000000000006\,a} , 
 0.7895037396899508\,e^{0.9100000000000006\,a} , 0.7956016200363664\,
 e^{0.9200000000000006\,a} , 0.8016199408837775\,e^{
 0.9300000000000006\,a} , 0.8075581004051147\,e^{0.9400000000000006\,
 a} , 0.8134155047893741\,e^{0.9500000000000006\,a} , 
 0.8191915683009986\,e^{0.9600000000000006\,a} , 0.8248857133384504\,
 e^{0.9700000000000006\,a} , 0.8304973704919708\,e^{
 0.9800000000000006\,a} , 0.8360259786005209\,e^{0.9900000000000007\,
 a} \right] $$\>function df(t) &= trigreduce(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'df(t)=df(t)


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ... e(radcan(sqrt(diff(fx(t),t)^2+diff(fy(t),t)^2))); $'df(t)=df(t ...
                                                         ^

\>S &=integrate(df(t),t,0,2\*%pi); $S // panjang kurva (spiral)


    Maxima said:
    defint: variable of integration cannot be a constant; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    S &amp;=integrate(df(t),t,0,2*%pi); $S // panjang kurva (spiral) ...
                                  ^

\>S(a=0.1) // Panjang kurva untuk a=0.1


    Function S not found.
    Try list ... to find functions!
    Error in:
    S(a=0.1) // Panjang kurva untuk a=0.1 ...
            ^

Soal:


Tunjukkan bahwa keliling lingkaran dengan jari-jari r adalah K=2.pi.r.


Penyelesaian:


Lingkaran dalam Koordinat Kartesius: Kita dapat merepresentasikan
suatu lingkaran dengan pusat di titik asal (0,0) dan jari-jari r
dengan persamaan parametrik berikut:


$$x(t) = r \cos(t)$$$$y(t) = r \sin(t)$$

di mana t adalah parameter yang bervariasi dari 0 hingga 2p.


Panjang Kurva Parametrik: Panjang kurva parametrik (x(t), y(t)) dari
t=a hingga t=b dapat dihitung dengan integral:


$$s = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} dt$$1. Mencari Turunan


$$x(t) = r \cos(t)$$\>&showev('diff(r\*cos(t),t))


    Maxima said:
    diff: second argument must be a variable; found errexp1
    #0: showev(f='diff([r,0.9999500004166653*r,0.9998000066665778*r,0.9995500337489875*r,0.9992001066609779*r,0.99875...)
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    &amp;showev('diff(r*cos(t),t)) ...
                              ^

$$y(t)=rsin(t)$$\>&showev('diff(r\*sin(t),t))


    Maxima said:
    diff: second argument must be a variable; found errexp1
    #0: showev(f='diff([0,0.009999833334166664*r,0.01999866669333308*r,0.02999550020249566*r,0.03998933418663416*r,0....)
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    &amp;showev('diff(r*sin(t),t)) ...
                              ^

2. Substitusi ke Rumus Panjang Kurva:


$$s = \int_0^{2\pi} \sqrt{(-r \sin(t))^2 + (r \cos(t))^2} dt$$$$s = \int_0^{2\pi} \sqrt{r^2 (\sin^2(t) + \cos^2(t))} dt$$

Karena


$$sin^2(t) + cos^2(t) = 1,$$

maka:


$$s = \int_0^{2\pi} r dt$$3. Integral


$$s = r \int_0^{2\pi} dt = r[t]_0^{2\pi} = r(2p - 0) = 2\pi r$$Berikut adalah contoh menghitung panjang parabola.


\>plot2d("x^2",xmin=-1,xmax=1):


![images/EMTKalkulus_kelompok%204-354.png](images/EMTKalkulus_kelompok%204-354.png)

\>$showev('integrate(sqrt(1+diff(x^2,x)^2),x,-1,1))


$$\int_{-1}^{1}{\sqrt{4\,x^2+1}\;dx}=\frac{{\rm asinh}\; 2+2\,\sqrt{5
 }}{2}$$\>$float(%)


$$\int_{-1.0}^{1.0}{\sqrt{4.0\,x^2+1.0}\;dx}=2.957885715089195$$\>x=-1:0.2:1; y=x^2; plot2d(x,y);  ...  
\>     plot2d(x,y,points=1,style="o#",add=1):


![images/EMTKalkulus_kelompok%204-357.png](images/EMTKalkulus_kelompok%204-357.png)

Panjang tersebut dapat dihampiri dengan menggunakan jumlah panjang
ruas-ruas garis yang menghubungkan titik-titik pada parabola tersebut.


\>i=1:cols(x)-1; sum(sqrt((x[i+1]-x[i])^2+(y[i+1]-y[i])^2))


    2.95191957027

Hasilnya mendekati panjang yang dihitung secara eksak. Untuk
mendapatkan hampiran yang cukup akurat, jarak antar titik dapat
diperkecil, misalnya 0.1, 0.05, 0.01, dan seterusnya. Cobalah Anda
ulangi perhitungannya dengan nilai-nilai tersebut.


## Koordinat Kartesius

Berikut diberikan contoh perhitungan panjang kurva menggunakan
koordinat Kartesius. Kita akan hitung panjang kurva dengan persamaan
implisit:


$$x^3+y^3-3xy=0.$$\>z &= x^3+y^3-3\*x\*y; $z


$$y^3-3\,x\,y+x^3$$\>plot2d(z,r=2,level=0,n=100):


![images/EMTKalkulus_kelompok%204-360.png](images/EMTKalkulus_kelompok%204-360.png)

Kita tertarik pada kurva di kuadran pertama.


\>plot2d(z,a=0,b=2,c=0,d=2,level=[-10;0],n=100,contourwidth=3,style="/"):


![images/EMTKalkulus_kelompok%204-361.png](images/EMTKalkulus_kelompok%204-361.png)

\>plot2d(z,a=0,b=2,c=0,d=2,level=[-10;0],n=100,contourwidth=3,style="/"):


![images/EMTKalkulus_kelompok%204-362.png](images/EMTKalkulus_kelompok%204-362.png)

Kita selesaikan persamaannya untuk x.


\>$z with y=l\*x, sol &= solve(%,x); $sol


$$l^3\,x^3+x^3-3\,l\,x^2$$$$\left[ x=\frac{3\,l}{l^3+1} , x=0 \right] $$Kita gunakan solusi tersebut untuk mendefinisikan fungsi dengan
Maxima.


\>function f(l) &= rhs(sol[1]); $'f(l)=f(l)


$$f\left(l\right)=\frac{3\,l}{l^3+1}$$Fungsi tersebut juga dapat digunaka untuk menggambar kurvanya. Ingat,
bahwa fungsi tersebut adalah nilai x dan nilai y=l*x, yakni x=f(l) dan
y=l*f(l).


\>plot2d(&f(x),&x\*f(x),xmin=-0.5,xmax=2,a=0,b=2,c=0,d=2,r=1.5):


![images/EMTKalkulus_kelompok%204-366.png](images/EMTKalkulus_kelompok%204-366.png)

Elemen panjang kurva adalah:


$$ds=\sqrt{f'(l)^2+(lf'(l)+f(l))^2}.$$\>function ds(l) &= ratsimp(sqrt(diff(f(l),l)^2+diff(l\*f(l),l)^2)); $'ds(l)=ds(l)


$${\it ds}\left(l\right)=\frac{\sqrt{9\,l^8+36\,l^6-36\,l^5-36\,l^3+
 36\,l^2+9}}{\sqrt{l^{12}+4\,l^9+6\,l^6+4\,l^3+1}}$$\>$integrate(ds(l),l,0,1)


$$\int_{0}^{1}{\frac{\sqrt{9\,l^8+36\,l^6-36\,l^5-36\,l^3+36\,l^2+9}
 }{\sqrt{l^{12}+4\,l^9+6\,l^6+4\,l^3+1}}\;dl}$$Integral tersebut tidak dapat dihitung secara eksak menggunakan
Maxima. Kita hitung integral etrsebut secara numerik dengan Euler.
Karena kurva simetris, kita hitung untuk nilai variabel integrasi dari
0 sampai 1, kemudian hasilnya dikalikan 2.


\>2\*integrate("ds(x)",0,1)


    4.91748872168

\>2\*romberg(&ds(x),0,1)// perintah Euler lain untuk menghitung nilai hampiran integral 


    4.91748872168

Perhitungan di datas dapat dilakukan untuk sebarang fungsi x dan y
dengan mendefinisikan fungsi EMT, misalnya kita beri nama
panjangkurva. Fungsi ini selalu memanggil Maxima untuk menurunkan
fungsi yang diberikan.


\>function panjangkurva(fx,fy,a,b) ...


    ds=mxm("sqrt(diff(@fx,x)^2+diff(@fy,x)^2)");
    return romberg(ds,a,b);
    endfunction
</pre>
\>panjangkurva("x","x^2",-1,1)


    2.95788571509

Bandingkan dengan nilai eksak di atas.


\>2\*panjangkurva(mxm("f(x)"),mxm("x\*f(x)"),0,1)


    4.91748872168

Kita hitung panjang spiral Archimides berikut ini dengan fungsi
tersebut.


\>plot2d("x\*cos(x)","x\*sin(x)",xmin=0,xmax=2\*pi,square=1):


![images/EMTKalkulus_kelompok%204-370.png](images/EMTKalkulus_kelompok%204-370.png)

\>panjangkurva("x\*cos(x)","x\*sin(x)",0,2\*pi)


    21.2562941482

Berikut kita definisikan fungsi yang sama namun dengan Maxima, untuk
perhitungan eksak.


\>&kill(ds,x,fx,fy)


    
                                     done
    

\>function ds(fx,fy) &&= sqrt(diff(fx,x)^2+diff(fy,x)^2)


    
                               2              2
                      sqrt(diff (fy, x) + diff (fx, x))
    

\>sol &= ds(x\*cos(x),x\*sin(x)); $sol // Kita gunakan untuk menghitung panjang kurva terak


$$\sqrt{\left(\cos x-x\,\sin x\right)^2+\left(\sin x+x\,\cos x\right)
 ^2}$$\>$sol | trigreduce | expand, $integrate(%,x,0,2\*pi), %()


$$\sqrt{x^2+1}$$$$\frac{{\rm asinh}\; \left(2\,\pi\right)+2\,\pi\,\sqrt{4\,\pi^2+1}}{
 2}$$    21.2562941482

Hasilnya sama dengan perhitungan menggunakan fungsi EMT.


Berikut adalah contoh lain penggunaan fungsi Maxima tersebut.


\>plot2d("3\*x^2-1","3\*x^3-1",xmin=-1/sqrt(3),xmax=1/sqrt(3),square=1):


![images/EMTKalkulus_kelompok%204-374.png](images/EMTKalkulus_kelompok%204-374.png)

\>sol &= radcan(ds(3\*x^2-1,3\*x^3-1)); $sol


$$3\,x\,\sqrt{9\,x^2+4}$$\>$showev('integrate(sol,x,0,1/sqrt(3))), $2\*float(%) // panjang kurva di atas


$$3\,\int_{0}^{\frac{1}{\sqrt{3}}}{x\,\sqrt{9\,x^2+4}\;dx}=3\,\left(
 \frac{7^{\frac{3}{2}}}{27}-\frac{8}{27}\right)$$$$6.0\,\int_{0.0}^{0.5773502691896258}{x\,\sqrt{9.0\,x^2+4.0}\;dx}=
 2.337835372767141$$## Sikloid

Berikut kita akan menghitung panjang kurva lintasan (sikloid) suatu
titik pada lingkaran yang berputar ke kanan pada permukaan datar.
Misalkan jari-jari lingkaran tersebut adalah r. Posisi titik pusat
lingkaran pada saat t adalah:


$$(rt,r).$$Misalkan posisi titik pada lingkaran tersebut mula-mula (0,0) dan
posisinya pada saat t adalah:


$$(r(t-\sin(t)),r(1-\cos(t))).$$Berikut kita plot lintasan tersebut dan beberapa posisi lingkaran
ketika t=0, t=pi/2, t=r*pi.


\>x &= r\*(t-sin(t))


    
            [0, 1.66665833335744e-7 r, 1.33330666692022e-6 r, 
    4.499797504338432e-6 r, 1.066581336583994e-5 r, 
    2.083072932167196e-5 r, 3.599352055540239e-5 r, 
    5.71526624672386e-5 r, 8.530603082730626e-5 r, 
    1.214508019889565e-4 r, 1.665833531718508e-4 r, 
    2.216991628251896e-4 r, 2.877927110806339e-4 r, 
    3.658573803051457e-4 r, 4.568853557635201e-4 r, 
    5.618675264007778e-4 r, 6.817933857540259e-4 r, 
    8.176509330039827e-4 r, 9.704265741758145e-4 r, 
    0.001141105023499428 r, 0.001330669204938795 r, 
    0.001540100153900437 r, 0.001770376919130678 r, 
    0.002022476464811601 r, 0.002297373572865413 r, 
    0.002596040745477063 r, 0.002919448107844891 r, 
    0.003268563311168871 r, 0.003644351435886262 r, 
    0.004047774895164447 r, 0.004479793338660443 r, 0.0049413635565565 r, 
    0.005433439383882244 r, 0.005956971605131645 r, 
    0.006512907859185624 r, 0.007102192544548636 r, 
    0.007725766724910044 r, 0.00838456803503801 r, 
    0.009079530587017326 r, 0.009811584876838586 r, 0.0105816576913495 r, 
    0.01139067201557714 r, 0.01223954694042984 r, 0.01312919757078923 r, 
    0.01406053493400045 r, 0.01503446588876983 r, 0.01605189303448024 r, 
    0.01711371462093175 r, 0.01822082445851714 r, 0.01937411182884202 r, 
    0.02057446139579705 r, 0.02182275311709253 r, 0.02311986215626333 r, 
    0.02446665879515308 r, 0.02586400834688696 r, 0.02731277106934082 r, 
    0.02881380207911666 r, 0.03036795126603076 r, 0.03197606320812652 r, 
    0.0336389770872163 r, 0.03535752660496472 r, 0.03713253989951881 r, 
    0.03896483946269502 r, 0.0408552420577305 r, 0.04280455863760801 r, 
    0.04481359426396048 r, 0.04688314802656623 r, 0.04901401296344043 r, 
    0.05120697598153157 r, 0.05346281777803219 r, 0.05578231276230905 r, 
    0.05816622897846346 r, 0.06061532802852698 r, 0.0631303649963022 r, 
    0.06571208837185505 r, 0.06836123997666599 r, 0.07107855488944881 r, 
    0.07386476137264342 r, 0.07672058079958999 r, 0.07964672758239233 r, 
    0.08264390910047736 r, 0.0857128256298576 r, 0.08885417027310427 r, 
    0.09206862889003742 r, 0.09535688002914089 r, 0.0987195948597075 r, 
    0.1021574371047232 r, 0.1056710629744951 r, 0.1092611211010309 r, 
    0.1129282524731764 r, 0.1166730903725168 r, 0.1204962603100498 r, 
    0.1243983799636342 r, 0.1283800591162231 r, 0.1324418995948859 r, 
    0.1365844952106265 r, 0.140808431699002 r, 0.1451142866615502 r, 
    0.1495026295080298 r, 0.1539740213994798 r]
    

\>y &= r\*(1-cos(t))


    
            [0, 4.999958333473664e-5 r, 1.999933334222437e-4 r, 
    4.499662510124569e-4 r, 7.998933390220841e-4 r, 
    0.001249739605033717 r, 0.00179946006479581 r, 
    0.002448999746720415 r, 0.003198293697380561 r, 
    0.004047266988005727 r, 0.004995834721974179 r, 
    0.006043902043303184 r, 0.00719136414613375 r, 0.00843810628521191 r, 
    0.009784003787362772 r, 0.01122892206395776 r, 0.01277271662437307 r, 
    0.01441523309043924 r, 0.01615630721187855 r, 0.01799576488272969 r, 
    0.01993342215875837 r, 0.02196908527585173 r, 0.02410255066939448 r, 
    0.02633360499462523 r, 0.02866202514797045 r, 0.03108757828935527 r, 
    0.03361002186548678 r, 0.03622910363410947 r, 0.03894456168922911 r, 
    0.04175612448730281 r, 0.04466351087439402 r, 0.04766643011428662 r, 
    0.05076458191755917 r, 0.0539576564716131 r, 0.05724533447165381 r, 
    0.06062728715262111 r, 0.06410317632206519 r, 0.06767265439396564 r, 
    0.07133536442348987 r, 0.07509094014268702 r, 0.07893900599711501 r, 
    0.08287917718339499 r, 0.08691105968769186 r, 0.09103425032511492 r, 
    0.09524833678003664 r, 0.09955289764732322 r, 0.1039475024744748 r, 
    0.1084317118046711 r, 0.113005077220716 r, 0.1176671413898787 r, 
    0.1224174381096274 r, 0.1272554923542488 r, 0.1321808203223502 r, 
    0.1371929294852391 r, 0.1422913186361759 r, 0.1474754779404944 r, 
    0.152744888986584 r, 0.1580990248377314 r, 0.1635373500848132 r, 
    0.1690593208998367 r, 0.1746643850903219 r, 0.1803519821545206 r, 
    0.1861215433374662 r, 0.1919724916878484 r, 0.1979042421157076 r, 
    0.2039162014509444 r, 0.2100077685026351 r, 0.216178334119151 r, 
    0.2224272812490723 r, 0.2287539850028937 r, 0.2351578127155118 r, 
    0.2416381240094921 r, 0.2481942708591053 r, 0.2548255976551299 r, 
    0.2615314412704124 r, 0.2683111311261794 r, 0.2751639892590951 r, 
    0.2820893303890569 r, 0.2890864619877229 r, 0.2961546843477643 r, 
    0.3032932906528349 r, 0.3105015670482534 r, 0.3177787927123868 r, 
    0.3251242399287333 r, 0.3325371741586922 r, 0.3400168541150183 r, 
    0.3475625318359485 r, 0.3551734527599992 r, 0.3628488558014202 r, 
    0.3705879734263036 r, 0.3783900317293359 r, 0.3862542505111889 r, 
    0.3941798433565377 r, 0.4021660177127022 r, 0.4102119749689023 r, 
    0.418316910536117 r, 0.4264800139275439 r, 0.4347004688396462 r, 
    0.4429774532337832 r, 0.451310139418413 r]
    

Berikut kita gambar sikloid untuk r=1.


\>ex &= x-sin(x); ey &= 1-cos(x); aspect(1);

\>plot2d(ex,ey,xmin=0,xmax=4pi,square=1); ...  
\>     plot2d("2+cos(x)","1+sin(x)",xmin=0,xmax=2pi,\>add,color=blue); ...  
\>     plot2d([2,ex(2)],[1,ey(2)],color=red,\>add); ...  
\>     plot2d(ex(2),ey(2),\>points,\>add,color=red); ...  
\>     plot2d("2pi+cos(x)","1+sin(x)",xmin=0,xmax=2pi,\>add,color=blue); ...  
\>     plot2d([2pi,ex(2pi)],[1,ey(2pi)],color=red,\>add);  ...  
\>     plot2d(ex(2pi),ey(2pi),\>points,\>add,color=red):


    Error : [0,1.66665833335744e-7*r-sin(1.66665833335744e-7*r),1.33330666692022e-6*r-sin(1.33330666692022e-6*r),4.499797504338432e-6*r-sin(4.499797504338432e-6*r),1.066581336583994e-5*r-sin(1.066581336583994e-5*r),2.083072932167196e-5*r-sin(2.083072932167196e-5*r),3.599352055540239e-5*r-sin(3.599352055540239e-5*r),5.71526624672386e-5*r-sin(5.71526624672386e-5*r),8.530603082730626e-5*r-sin(8.530603082730626e-5*r),1.214508019889565e-4*r-sin(1.214508019889565e-4*r),1.665833531718508e-4*r-sin(1.665833531718508e-4*r),2.216991628251896e-4*r-sin(2.216991628251896e-4*r),2.877927110806339e-4*r-sin(2.877927110806339e-4*r),3.658573803051457e-4*r-sin(3.658573803051457e-4*r),4.5688535576352e-4*r-sin(4.5688535576352e-4*r),5.618675264007778e-4*r-sin(5.618675264007778e-4*r),6.817933857540259e-4*r-sin(6.817933857540259e-4*r),8.176509330039827e-4*r-sin(8.176509330039827e-4*r),9.704265741758145e-4*r-sin(9.704265741758145e-4*r),0.001141105023499428*r-sin(0.001141105023499428*r),0.001330669204938795*r-sin(0.001330669204938795*r),0.001540100153900437*r-sin(0.001540100153900437*r),0.001770376919130678*r-sin(0.001770376919130678*r),0.002022476464811601*r-sin(0.002022476464811601*r),0.002297373572865413*r-sin(0.002297373572865413*r),0.002596040745477063*r-sin(0.002596040745477063*r),0.002919448107844891*r-sin(0.002919448107844891*r),0.003268563311168871*r-sin(0.003268563311168871*r),0.003644351435886262*r-sin(0.003644351435886262*r),0.004047774895164447*r-sin(0.004047774895164447*r),0.004479793338660443*r-sin(0.004479793338660443*r),0.0049413635565565*r-sin(0.0049413635565565*r),0.005433439383882244*r-sin(0.005433439383882244*r),0.005956971605131645*r-sin(0.005956971605131645*r),0.006512907859185624*r-sin(0.006512907859185624*r),0.007102192544548636*r-sin(0.007102192544548636*r),0.007725766724910044*r-sin(0.007725766724910044*r),0.00838456803503801*r-sin(0.00838456803503801*r),0.009079530587017326*r-sin(0.009079530587017326*r),0.009811584876838586*r-sin(0.009811584876838586*r),0.0105816576913495*r-sin(0.0105816576913495*r),0.01139067201557714*r-sin(0.01139067201557714*r),0.01223954694042984*r-sin(0.01223954694042984*r),0.01312919757078923*r-sin(0.01312919757078923*r),0.01406053493400045*r-sin(0.01406053493400045*r),0.01503446588876983*r-sin(0.01503446588876983*r),0.01605189303448024*r-sin(0.01605189303448024*r),0.01711371462093175*r-sin(0.01711371462093175*r),0.01822082445851714*r-sin(0.01822082445851714*r),0.01937411182884202*r-sin(0.01937411182884202*r),0.02057446139579705*r-sin(0.02057446139579705*r),0.02182275311709253*r-sin(0.02182275311709253*r),0.02311986215626333*r-sin(0.02311986215626333*r),0.02446665879515308*r-sin(0.02446665879515308*r),0.02586400834688696*r-sin(0.02586400834688696*r),0.02731277106934082*r-sin(0.02731277106934082*r),0.02881380207911666*r-sin(0.02881380207911666*r),0.03036795126603076*r-sin(0.03036795126603076*r),0.03197606320812652*r-sin(0.03197606320812652*r),0.0336389770872163*r-sin(0.0336389770872163*r),0.03535752660496472*r-sin(0.03535752660496472*r),0.03713253989951881*r-sin(0.03713253989951881*r),0.03896483946269502*r-sin(0.03896483946269502*r),0.0408552420577305*r-sin(0.0408552420577305*r),0.04280455863760801*r-sin(0.04280455863760801*r),0.04481359426396048*r-sin(0.04481359426396048*r),0.04688314802656623*r-sin(0.04688314802656623*r),0.04901401296344043*r-sin(0.04901401296344043*r),0.05120697598153157*r-sin(0.05120697598153157*r),0.05346281777803219*r-sin(0.05346281777803219*r),0.05578231276230905*r-sin(0.05578231276230905*r),0.05816622897846346*r-sin(0.05816622897846346*r),0.06061532802852698*r-sin(0.06061532802852698*r),0.0631303649963022*r-sin(0.0631303649963022*r),0.06571208837185505*r-sin(0.06571208837185505*r),0.06836123997666599*r-sin(0.06836123997666599*r),0.07107855488944881*r-sin(0.07107855488944881*r),0.07386476137264342*r-sin(0.07386476137264342*r),0.07672058079958999*r-sin(0.07672058079958999*r),0.07964672758239233*r-sin(0.07964672758239233*r),0.08264390910047736*r-sin(0.08264390910047736*r),0.0857128256298576*r-sin(0.0857128256298576*r),0.08885417027310427*r-sin(0.08885417027310427*r),0.09206862889003742*r-sin(0.09206862889003742*r),0.09535688002914089*r-sin(0.09535688002914089*r),0.0987195948597075*r-sin(0.0987195948597075*r),0.1021574371047232*r-sin(0.1021574371047232*r),0.1056710629744951*r-sin(0.1056710629744951*r),0.1092611211010309*r-sin(0.1092611211010309*r),0.1129282524731764*r-sin(0.1129282524731764*r),0.1166730903725168*r-sin(0.1166730903725168*r),0.1204962603100498*r-sin(0.1204962603100498*r),0.1243983799636342*r-sin(0.1243983799636342*r),0.1283800591162231*r-sin(0.1283800591162231*r),0.1324418995948859*r-sin(0.1324418995948859*r),0.1365844952106265*r-sin(0.1365844952106265*r),0.140808431699002*r-sin(0.140808431699002*r),0.1451142866615502*r-sin(0.1451142866615502*r),0.1495026295080298*r-sin(0.1495026295080298*r),0.1539740213994798*r-sin(0.1539740213994798*r)] does not produce a real or column vector
    
    Error generated by error() command
    
    adaptiveeval:
        error(f$|" does not produce a real or column vector"); 
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        dw/n,dw/n^2,dw/n;args());

\>ds &= radcan(sqrt(diff(ex,x)^2+diff(ey,x)^2)); $ds=trigsimp(ds) // elemen panjang kurva sikloid


    Maxima said:
    diff: second argument must be a variable; found errexp1
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    ds &amp;= radcan(sqrt(diff(ex,x)^2+diff(ey,x)^2)); $ds=trigsimp(ds ...
                                                 ^

\>ds &= trigsimp(ds); $ds

\>$showev('integrate(ds,x,0,2\*pi)) // hitung panjang sikloid satu putaran penuh


    Maxima said:
    defint: variable of integration must be a simple or subscripted variable.
    defint: found errexp1
    #0: showev(f='integrate(ds,[0,1.66665833335744e-7*r,1.33330666692022e-6*r,4.499797504338432e-6*r,1.06658133658399...)
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    $showev('integrate(ds,x,0,2*pi)) // hitung panjang sikloid sat ...
                                     ^

\>integrate(mxm("ds"),0,2\*pi) // hitung secara numerik


    Illegal function result in map.
    %evalexpression:
        if maps then return %mapexpression1(x,f$;args());
    gauss:
        if maps then y=%evalexpression(f$,a+h-(h*xn)',maps;args());
    adaptivegauss:
        t1=gauss(f$,c,c+h;args(),=maps);
    Try "trace errors" to inspect local variables after errors.
    integrate:
        return adaptivegauss(f$,a,b,eps*1000;args(),=maps);

\>romberg(mxm("ds"),0,2\*pi) // cara lain hitung secara numerik


    Wrong argument!
    
    Cannot combine a symbolic expression here.
    Did you want to create a symbolic expression?
    Then start with &amp;.
    
    Try "trace errors" to inspect local variables after errors.
    romberg:
        if cols(y)==1 then return y*(b-a); endif;
    Error in:
    romberg(mxm("ds"),0,2*pi) // cara lain hitung secara numerik ...
                             ^

Perhatikan, seperti terlihat pada gambar, panjang sikloid lebih besar
daripada keliling lingkarannya, yakni:


$$2\pi.$$## Kurvatur (Kelengkungan) Kurva

image: Osculating.png


Aslinya, kelengkungan kurva diferensiabel (yakni, kurva mulus yang
tidak lancip) di titik P didefinisikan melalui lingkaran oskulasi
(yaitu, lingkaran yang melalui titik P dan terbaik memperkirakan,
paling banyak menyinggung kurva di sekitar P). Pusat dan radius
kelengkungan kurva di P adalah pusat dan radius lingkaran oskulasi.
Kelengkungan adalah kebalikan dari radius kelengkungan:


$$\kappa =\frac {1}{R}$$dengan R adalah radius kelengkungan. (Setiap lingkaran memiliki
kelengkungan ini pada setiap titiknya, dapat diartikan, setiap
lingkaran berputar 2pi sejauh 2piR.)


Definisi ini sulit dimanipulasi dan dinyatakan ke dalam rumus untuk
kurva umum. Oleh karena itu digunakan definisi lain yang ekivalen.


# Barisan dan Deret

Barisan adalah susunan bilangan yang memiliki pola atau karakteristik
tertentu, sedangkan deret adalah hasil penjumlahan dari
anggota-anggota dalam barian tertentu.


Barisan dapat didefinisikan dengan beberapa cara di dalam EMT, di
antaranya:


- menggunakan titik dua ":", sama seperti saat mendefinisikan vektor
dengan elemen-elemen beraturan


- menggunakan perintah "sequence" dan rumus barisan (suku ke -n);


- menggunakan perintah "iterate" atau "niterate";


- menggunakan fungsi Maxima "create_list" atau "makelist" untuk
menghasilkan barisan simbolik;


- menggunakan fungsi biasa yang inputnya vektor atau barisan;


- menggunakan fungsi rekursif.


EMT menyediakan beberapa perintah (fungsi) terkait barisan, yakni:


- sum: menghitung jumlah semua elemen suatu barisan


- cumsum: jumlah kumulatif suatu barisan


- differences: selisih antar elemen-elemen berturutan


EMT juga dapat digunakan untuk menghitung jumlah deret berhingga
maupun deret tak hingga, dengan menggunakan perintah (fungsi) "sum".
Perhitungan dapat dilakukan secara numerik maupun simbolik dan eksak.


Contoh perhitungan barisan dan deret menggunakan EMT.


## Menggunakan titik dua

\>1:15


    [1,  2,  3,  4,  5,  6,  7,  8,  9,  10,  11,  12,  13,  14,  15]

\>1:3:30


    [1,  4,  7,  10,  13,  16,  19,  22,  25,  28]

\>sum(1:3:30)


    145

\>cumsum(1:3:30)


    [1,  5,  12,  22,  35,  51,  70,  92,  117,  145]

## Menggunakan perintah "sequence" dan rumus barisan (suku ke -n)

Untuk barisan yang lebih kompleks dapat digunakan fungsi "sequence()".
Fungsi ini menghitung nilai-nilai x[n] dari semua nilai sebelumnya,
x[1],...,x[n-1] yang diketahui.


Berikut adalah contoh barisan Fibonacci.


$$x_n = x_{n-1}+x_{n-2}, \quad x_1=1, \quad x_2 =1$$\>sequence("x[n-1]+x[n-2]",[1,1],15) //suku ke satu :1, suku ke dua :1


    [1,  1,  2,  3,  5,  8,  13,  21,  34,  55,  89,  144,  233,  377,  610]

\>plot2d(sequence("x[n-1]+x[n-2]",[1,1],15)):


![images/EMTKalkulus_kelompok%204-383.png](images/EMTKalkulus_kelompok%204-383.png)

\>sequence("x[n-1]+x[n-2]",[1,1],250)^(1/(1:250))


    [1,  1,  1.25992,  1.31607,  1.37973,  1.41421,  1.44256,  1.46311,
    1.47967,  1.49292,  1.50389,  1.51309,  1.52091,  1.52765,  1.53352,
    1.53867,  1.54323,  1.54729,  1.55094,  1.55422,  1.5572,  1.55992,
    1.5624,  1.56468,  1.56678,  1.56872,  1.57052,  1.57219,  1.57375,
    1.57521,  1.57657,  1.57785,  1.57905,  1.58019,  1.58126,  1.58227,
    1.58322,  1.58413,  1.58499,  1.58581,  1.58659,  1.58733,  1.58804,
    1.58871,  1.58936,  1.58997,  1.59057,  1.59113,  1.59168,  1.5922,
    1.5927,  1.59319,  1.59365,  1.5941,  1.59453,  1.59495,  1.59535,
    1.59574,  1.59611,  1.59648,  1.59683,  1.59717,  1.5975,  1.59782,
    1.59813,  1.59843,  1.59872,  1.599,  1.59927,  1.59954,  1.5998,
    1.60005,  1.6003,  1.60053,  1.60077,  1.60099,  1.60121,  1.60143,
    1.60164,  1.60184,  1.60204,  1.60223,  1.60242,  1.60261,  1.60279,
    1.60296,  1.60314,  1.60331,  1.60347,  1.60363,  1.60379,  1.60394,
    1.60409,  1.60424,  1.60439,  1.60453,  1.60467,  1.6048,  1.60494,
    1.60507,  1.60519,  1.60532,  1.60544,  1.60556,  1.60568,  1.6058,
    1.60591,  1.60602,  1.60613,  1.60624,  1.60635,  1.60645,  1.60655,
    1.60665,  1.60675,  1.60685,  1.60694,  1.60704,  1.60713,  1.60722,
    1.60731,  1.6074,  1.60748,  1.60757,  1.60765,  1.60773,  1.60781,
    1.60789,  1.60797,  1.60805,  1.60813,  1.6082,  1.60827,  1.60835,
    1.60842,  1.60849,  1.60856,  1.60863,  1.60869,  1.60876,  1.60883,
     ... ]

\>plot2d(sequence("x[n-1]+x[n-2]",[1,1],250)^(1/(1:250))):


![images/EMTKalkulus_kelompok%204-384.png](images/EMTKalkulus_kelompok%204-384.png)

## Menggunakan perintah "iterate" atau "niterate"

EMT menyediakan fungsi iterate("g(x)", x0, n) untuk melakukan iterasi


$$x_{k+1}=g(x_k), \ x_0=x_0, k= 1, 2, 3, ..., n.$$Berikut contoh penggunaan iterasi


Contoh : Menunjukkan pertumbuhan dari nilai awal 1000 dengan laju
pertambahan 5%, selama 10 periode.


\>q=1.05; iterate("x\*q",1000,n=10)'


             1000 
             1050 
           1102.5 
          1157.63 
          1215.51 
          1276.28 
           1340.1 
           1407.1 
          1477.46 
          1551.33 
          1628.89 

# Spiral Theodorus

konstruksi segitiga siku-siku yang berkesinambungan menjadi spiral
atau dalam kata lain sebuah spiral yang dibangun dari segitiga
siku-siku yang berurutan. Setiap segitiga siku-siku yang baru dibuat
dengan menghubungkan sisi miring segitiga sebelumnya dengan sisi alas
yang panjangnya 1 satuan.


Spiral Theodorus (spiral segitiga siku-siku) dapat digambar secara
rekursif. Rumus rekursifnya adalah:


$$x_n = \left( 1 + \frac{i}{\sqrt{n-1}} \right) \, x_{n-1}, \quad x_1=1,$$yang menghasilkan barisan bilangan kompleks.


\>function g(n) := 1+I/sqrt(n)


Rekursinya dapat dijalankan sebanyak 17 untuk menghasilkan barisan 17
bilangan kompleks, kemudian digambar bilangan-bilangan kompleksnya.


\>x=sequence("g(n-1)\*x[n-1]",1,20); plot2d(x,r=3.5);...  
\>   textbox(latex("Spiral\\ Theodorus"),0.4):


![images/EMTKalkulus_kelompok%204-387.png](images/EMTKalkulus_kelompok%204-387.png)

Selanjutnya dihubungan titik 0 dengan titik-titik kompleks tersebut
menggunakan loop.


\>for i=1:cols(x); plot2d([0,x[i]],\>add); end:


![images/EMTKalkulus_kelompok%204-388.png](images/EMTKalkulus_kelompok%204-388.png)

\>function gstep (v) ...


    w=[-v[2];v[1]];
    return v+w/norm(w);
    endfunction
</pre>
\>x=iterate("gstep",[1;0],16); plot2d(x[1],x[2],r=3.5,\>points):


![images/EMTKalkulus_kelompok%204-389.png](images/EMTKalkulus_kelompok%204-389.png)

# Limit Barisan Limit dari suatu barisan (x_n) saat (n) mendekati tak

hingga adalah nilai yang didekati oleh elemen-elemen barisan tersebut
seiring dengan bertambahnya (n). Secara formal, kita mengatakan bahwa
barisan (x_n) memiliki limit (L).


Definisi formal:


$$\forall \varepsilon > 0, \exists k \in \mathbb{N} : (\forall n \in \mathbb{N}, n \geq k \implies |x_n - L| <\varepsilon)$$Dapat dinotasikan sebagai


$$\lim_{n \to \infty}x_n=L$$Contoh:


1.


$$x_n = \lim_{n \to \infty}\frac{1}{n}$$\>$showev('limit(1/n,n,inf))


$$\lim_{n\rightarrow \infty }{\frac{1}{n}}=0$$Limit barisan juga dapat kita definisikan dulu


\>$x\_n := 1/n


$$\frac{1}{n}$$Lalu mencari nilai limit nya


\>$limit(x\_n,n,inf)


$$0$$2.


$$\lim_{n\to\infty}\frac{2n^2-1}{n^2+5}$$\>$showev('limit((2\*n^2-1)/(n^2+5),n,inf))


$$\lim_{n\rightarrow \infty }{\frac{2\,n^2-1}{n^2+5}}=2$$# Kekonvergenan

Iterasi sampai konvergen merupakan proses yang terus berulang sampai
mendapat nilai yang stabil atau tidak berubah secara signifikan.
Tetapi, apabila iterasinya tidak konvergen setelah ditunggu lama, Kita
dapat menghentikannya dengan menekan tombol [ESC].


\>iterate("cos(x)",1) // iterasi x(n+1)=cos(x(n)), dengan x(0)=1.


    0.739085133216

Iterasi tersebut konvergen ke penyelesaian persamaan


$$x = \cos(x).$$Iterasi ini juga dapat dilakukan pada interval, hasilnya adalah
barisan interval yang memuat akar tersebut.


\>hasil := iterate("cos(x)",~1,2~) //iterasi x(n+1)=cos(x(n)), dengan interval awal (1, 2)


    ~0.739085133211,0.7390851332133~

\>h=expand(hasil,100), cos(h) << h


    ~0.73908513309,0.73908513333~
    1

Iterasi juga dapat digunakan pada fungsi yang didefinisikan.


\>function f(x) := (x+2/x)/2


Iterasi x(n+1)=f(x(n)) akan konvergen ke akar kuadrat 2.


\>iterate("f",2), sqrt(2)


    1.41421356237
    1.41421356237

# Deret Taylor

Deret Taylor suatu fungsi f yang diferensiabel sampai tak hingga di
sekitar x=a adalah:


$$f(x) = \sum_{k=0}^\infty \frac{(x-a)^k f^{(k)}(a)}{k!}.$$Diberikan contoh fungsi exponensial yang didekati dengan Deret Taylor


\>$'e^x =taylor(exp(x),x,0,10) 


    Maxima said:
    taylor: 0.1539740213994798*r cannot be a variable.
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    $'e^x =taylor(exp(x),x,0,10)  ...
                                 ^

Menghitung exp(x) untuk x=4 yang di potong pada k=10


\>deret &= makelist(taylor(exp(x),x,0,k),k,10); $deret


    Maxima said:
    taylor: 0.1539740213994798*r cannot be a variable.
     -- an error. To debug this try: debugmode(true);
    
    Error in:
    deret &amp;= makelist(taylor(exp(x),x,0,k),k,10); $deret ...
                                                ^

\>taylor\_exp := taylor(exp(x), x, 0, 10);


    Variable taylor not found!
    Error in:
    taylor_exp := taylor(exp(x), x, 0, 10); ...
               ^

\>nilai := eval(taylor\_exp, x=4):


    Variable taylor not found!
    Error in:
    nilai := eval(taylor_exp, x=4): ...
                            ^

\>println(nilai);


    Variable or function nilai not found.
    Error in:
    println(nilai); ...
                 ^

Bukti :


$$e^x = \frac{(x)^{10}}{(3628800)} + \frac{(x)^{9}}{(362880)} + \frac{(x)^{8}}{(40320)} + \frac{(x)^{7}}{(5040)} + \frac{(x)^{6}}{(720)} + \frac{(x)^{5}}{(120)} + \frac{(x)^{4}}{(24)} + \frac{(x)^{3}}{(6)} + \frac{(x)^{2}}{(2)} + x + 1$$$$e^4 = \frac{(4)^{10}}{(3628800)} + \frac{(4)^{9}}{(362880)} + \frac{(4)^{8}}{(40320)} + \frac{(4)^{7}}{(5040)} + \frac{(4)^{6}}{(720)} + \frac{(4)^{5}}{(120)} + \frac{(4)^{4}}{(24)} + \frac{(4)^{3}}{(6)} + \frac{(4)^{2}}{(2)} + 4 + 1$$$$e^4 = \frac{(4)^{10}}{(3628800)} + \frac{(4)^{9}}{(362880)} + \frac{(4)^{8}}{(40320)} + \frac{(4)^{7}}{(5040)} + \frac{(4)^{6}}{(720)} + \frac{(4)^{5}}{(120)} + \frac{(4)^{4}}{(24)} + \frac{(4)^{3}}{(6)} + \frac{(4)^{2}}{(2)} + 5$$$$e^4 = 54,4431$$


# GEOMETRI

# Visualisasi dan Perhitungan Geometri dengan EMT

Euler menyediakan beberapa fungsi untuk melakukan visualisasi dan
perhitungan geometri, baik secara numerik maupun analitik (seperti
biasanya tentunya, menggunakan Maxima). Fungsi-fungsi untuk
visualisasi dan perhitungan geometeri tersebut disimpan di dalam file
program "geometry.e", sehingga file tersebut harus dipanggil sebelum
menggunakan fungsi-fungsi atau perintah-perintah untuk geometri.


\>load geometry


    Numerical and symbolic geometry.

# Sub Materi 1

## Fungsi-fungsi Geometri

Fungsi-fungsi untuk Menggambar Objek Geometri:


* 
defaultd:=textheight()*1.5: nilai asli untuk parameter d
* Fungsi ini

* 
setPlotRange(x1,x2,y1,y2): menentukan rentang x dan y pada bidang
* koordinat. Fungsi ini menunjukkan rentang koordinat yang akan kita
* pakai.
* setPlotRange(2,3,-2,-3):

* 
setPlotRange(r): pusat bidang koordinat (0,0) dan batas-batas
* sumbu-x dan y adalah -r sd r. Dalam perintah ini, rentang x dan y
* diatur secara otomatis dengan pusat koordinat di (0, 0) dan batas pada
* -r hingga r untuk kedua sumbu. Ini berarti bahwa rentang untuk sumbu x
* dan y akan simetris dengan pusat di titik nol.

* 
plotPoint (P, "P"): menggambar titik P dan diberi label "P".

* 
plotSegment (A,B, "AB", d): menggambar ruas garis AB, diberi label
* "AB" sejauh d.

* 
plotLine (g, "g", d): menggambar garis g diberi label "g" sejauh d

* 
plotCircle (c,"c",v,d): Menggambar lingkaran c dan diberi label "c"

* 
plotLabel (label, P, V, d): menuliskan label pada posisi P


Fungsi-fungsi Geometri Analitik (numerik maupun simbolik):


* 
turn(v, phi): memutar vektor v sejauh phi.
* Memutar vektor v sejauh sudut phi (dalam radian atau derajat) dari
* posisi awalnya. Fungsi ini mengubah arah vektor tanpa mengubah
* panjangnya.

* 
turnLeft(v):   memutar vektor v ke kiri.
* Memutar vektor v ke kiri (biasanya sebesar 90 derajat berlawanan arah
* jarum jam).

* 
turnRight(v):  memutar vektor v ke kanan.
* Memutar vektor v ke kanan (biasanya sebesar 90 derajat searah jarum
* jam).

* 
normalize(v): normal vektor v.
* Mengubah vektor v menjadi vektor satuan (vektor dengan panjang 1)
* dengan mempertahankan arah vektor.


* 
crossProduct(v, w): hasil kali silang vektorv dan w.
* Menghitung hasil kali silang dua vektor v dan w. Hasilnya adalah
* vektor baru yang tegak lurus terhadap kedua vektor asal dalam ruang 3
* dimensi.

* 
lineThrough(A, B): garis melalui A dan B, hasilnya [a,b,c] sdh.
* ax+by=c.
* Menghitung persamaan garis yang melalui dua titik A dan B. Hasilnya
* dalam bentuk persamaan ax + by = c.

* 
lineWithDirection(A,v): garis melalui A searah vektor v.
* Menghasilkan persamaan garis yang melalui titik A dan searah dengan
* vektor v. Ini berguna untuk mendefinisikan garis berdasarkan titik dan
* arah.

* 
getLineDirection(g): vektor arah (gradien) garis g.
* Menghasilkan vektor arah dari garis g. Vektor arah ini biasanya
* ditentukan dari gradien atau kemiringan garis.

* 
getNormal(g): vektor normal (tegak lurus) garis g.
* Menghasilkan vektor normal atau tegak lurus terhadap garis g. Vektor
* normal ini penting dalam banyak aplikasi seperti perhitungan pantulan
* atau bidang normal.

* 
getPointOnLine(g):  titik pada garis gMenghasilkan vektor arah dari
* garis g.
* Menghasilkan titik yang terletak pada garis g. Titik ini biasanya
* diambil dari koordinat pada garis yang memenuhi persamaan garis
* tersebut.

* 
perpendicular(A, g):  mencari garis melalui A yang tegak lurus
* terhadap garis g

* 
parallel (A, g):  garis melalui A sejajar garis g

* 
lineIntersection(g, h): mencari titik potong antara garis g dan
* garis h

* 
projectToLine(A, g):   proyeksi titik A pada garis g atau mencari
* titik pada garis g yang merupakan proyeksi dari titik A.

* 
distance(A, B):  mencari perhitungan jarak titik A dan titik B pada
* bidang kartesius.

* 
distanceSquared(A, B):  mencari kuadrat dari jarak antara titik A
* dan titik B

* 
quadrance(A, B): mencari kuadrat jarak antara titik A dan titik B

* 
areaTriangle(A, B, C): mencari perhitungan luas segitiga ABC

* 
computeAngle(A, B, C): mencari perhitungan berapa besar sudut &lt;ABC

* 
angleBisector(A, B, C): mencari perhitungan garis bagi (pembagi)
* sudut &lt;ABC, titik B yang merupakan titik tengah antara titik A dan C

* 
circleWithCenter (A, r): mencari lingkaran dengan pusat A dan
* jari-jari r

* 
getCircleCenter(c): mencari sebuah titik pusat pada lingkaran c

* 
getCircleRadius(c): mencari perhitungan jari-jari dari lingkaran c

* 
circleThrough(A,B,C): mencari persamaan lingkaran yang melalui tiga
* titik yang berikan (titik A, B, C)

* 
middlePerpendicular(A, B): mencari garis tegak lurus melalui titik
* tengah dari AB

* 
lineCircleIntersections(g, c): mencari perhitungan titik potong
* garis g dan lingkran c

* 
circleCircleIntersections (c1, c2): mencari perhitungan titik potong
* lingkaran c1 dan c2

* 
planeThrough(A, B, C): mencari persamaan bidang melalui titik A, B,
* C di dalam ruang tiga dimensi.


##  Fungsi-fungsi Khusus Untuk Geometri Simbolik:

* 
getLineEquation (g,x,y): persamaan garis g dinyatakan dalam x dan y,
* artinya mencari persamaan garis g yang akan melewati dua titik yaitu x
* dan y dalam kartesius.

* 
getHesseForm (g,x,y,A): bentuk Hesse garis g dinyatakan dalam x dan
* y dengan titik A pada sisi positif (kanan/atas) garis

* 
quad(A,B): mencari persamaan kuadrat panjang jarak antara kedua
* titik A dan B

* 
spread(a,b,c): Spread segitiga dengan panjang sisi-sisi a,b,c, yakni
* sin(alpha)^2 dengan alpha sudut yang menghadap sisi a.

* 
crosslaw(a,b,c,sa): persamaan 3 quads dan 1 spread pada segitiga
* dengan panjang sisi a, b, c.

* 
triplespread(sa,sb,sc): persamaan 3 spread sa,sb,sc yang memebntuk
* suatu segitiga dan fungsi ini untuk menghitung spread dari ketiga sisi
* segitiga

* 
doublespread(sa): Spread sudut rangkap Spread 2*phi, dengan
* sa=sin(phi)^2 spread a.


# Sub Materi 2

## Menentukan Luas Bidang Koordinat

Sebelum kita membuat atau menggambarkan objek geometri, tentunya
sebelum itu kita harus membuat sebuah bidang koordinat, sampai
didefinisikan bidang koordinat yang baru.


Jika ingin membuat bidang koordinat kita dapat menggunakan


setPlotRange(x1,x2,y1,y2):


keterangan :


- x1,x2 adalah panjang garis koordinat x yang akan dibuat dari x1
sampai x2


- y1,y2 adalah lebar garis koordinat y yang akan dibuat dari y1 sampai
y2


\>setPlotRange(x1,x2,y1,y2); // Menentukan rentang koordinat


    Variable or function x1 not found.
    Error in:
    setPlotRange(x1,x2,y1,y2); // Menentukan rentang koordinat ...
                   ^

Sebagai contoh:


Akan dibuatkan luas bidang koordinat dengan panjang 5 satuan sisi x
dan lebar 5 satuan sisi y, gambarkanlah bidang koordinat tersebut!


\>setPlotRange(1,5,1,5); 

\>aspect(1); 


Dari hasil grafik dapat dilihat bahwa panjang dan lebar grafiknya
sebesar 5 satuan. Dimulai dari titik (1,1) sampai (5,5)


## Contoh

1. Buatkanlah sebuah bidang koordinat dengan panjang dan lebar 8
satuan dimulai titik koordinat (-1,1) sampai dengan (7,7)


x1 =-1 dan x2 =7


y1 =-1 dan y2 =7


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-1,7,-1,7);

\>aspect(1): 


![images/Presentasi_EMT_#Geometri-001.png](images/Presentasi_EMT_#Geometri-001.png)

\>setPlotRange(-2,10,-1,10); //

\>A=[1,5]; plotPoint(A,"A"); // Membuat titik A

\>B=[4,1]; plotPoint(B,"B"); //Membuat titik B

\>plotSegment(A,B,"c"); //Membuat garis dengan menghubungkan titik A dan B

\>aspect(1) ; plotSegment(A,B): //Menampilkan hasil plot 


![images/Presentasi_EMT_#Geometri-002.png](images/Presentasi_EMT_#Geometri-002.png)

Dilihat dari gambar grafik tersebut bidang koordinat dengan rentang -1
sampai 10 satuan, dan digambarkan sebuah garis AB dengan titik
A(1,5)dan B(4,1)


3. Akan dibuat sebuah bidang koordinat dengan rentang koordinat x,
x1=-10 dan x2=50, rentang koordinat y, y=-10 dan y2=-100!


\>setPlotRange(-10,50,-10,100);

\>aspect(1):


![images/Presentasi_EMT_#Geometri-003.png](images/Presentasi_EMT_#Geometri-003.png)

## Latihan

Buatlah sebuah bidang koordinat dengan rentang koordinat x 100 satuan
dimulai dan rentang koordinay y 100 satuan dimulai dari titik (0,0).
Kemudian buatkanlah titik D(58,82),E(15,90), dan F(80,41)!


\>setPlotRange(0,100,0,100); //membuat bidang koordinat

\>D=[58,82]; plotPoint(D,"D"); //titik D

\>E=[15,90]; plotPoint(E,"E"); //titik E

\>F=[80,41]; plotPoint(F,"F"); //titik F

\>aspect(1):


![images/Presentasi_EMT_#Geometri-004.png](images/Presentasi_EMT_#Geometri-004.png)

# Sub Materi 3

* Menggambar Titik, Ruas Garis, Garis, Segi Banyak, 
* Lingkaran, Elips, Parabola, Hiperbola


## 1) Menggambar Titik

Titik merupakan suatu tempat/posisi dalam ruang. Sebuah titik tidak
memiliki ukuran dan dimensi, tetapi menunjukkan lokasi yang pasti.
Serangkaian titik menyusun garis, ruas garis, sinar, dan bidang. Titik
diberi nama dengan huruf besar miring ditempatkan di sebelahnya.
Sebuah titik dimodelkan dengan sebuah noktah.


Untuk menggambar objek-objek geometri, langkah pertama adalah
menentukan rentang sumbu-sumbu koordinat. Semua objek geometri akan
digambar pada satu bidang koordinat, sampai didefinisikan bidang
koordinat yang baru.


Perintah untuk menggambar titik sebagai berikut.


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-5,5,-5,5); // mendefinisikan bidang koordinat baru

\>A=[3,2]; plotPoint(A,"A"): // definisi dan gambar titik


![images/Presentasi_EMT_#Geometri-005.png](images/Presentasi_EMT_#Geometri-005.png)

## 2) Menggambar Garis

Sebuah garis dipikirkan sebagai suatu himpunan titik berderet yang
panjang tak terbatas, tetapi tidak memiliki lebar. Garis terdiri dari
serangkaian titik-titik tak terhingga. Sebuah garis dinamai dengan
salah satu huruf kecil italic atau dengan menyebutkan dua titik pada
garis tersebut.


Dalam sistem koordinat dua dimensi, garis dapat digambar menggunakan
persamaan linear, seperti


$$y = mx + b$$di mana


m adalah kemiringan dan


b adalah titik potong dengan sumbu y.


Misalkan, terdapat garis


$$y = 2x + 3$$\>plot2d("2x+3"):


![images/Presentasi_EMT_#Geometri-008.png](images/Presentasi_EMT_#Geometri-008.png)

## Latihan



Soal Benar Salah


Tentukan pernyataan di bawah, benar atau salah.


a. Diberikan garis dengan persamaan


$$y=3x+2.$$

Garis ini memiliki gradien 3 dan memotong sumbu y di titik (0,2).


b. Dua garis dengan persamaan


$$y=4x+1, y=3x+1$$adalah garis yang sejajar.


c. Garis dengan persamaan


$$-4x-y=8$$

memiliki gambar dengan kemiringan ke kiri(turun ke bawah).


Kunci jawaban:


a. Diberikan garis dengan persamaan


$$y=3x+2.$$Garis ini memiliki gradien 3 dan memotong sumbu y di titik (0,2).


Jawaban: Benar


Koefisien 3 pada variabel x menyatakan gradien. Lalu, saat memotong
sumbu y, berarti x = 0, sehingga didapat y = 2. Titiknya: (0,2).


\>plot2d("3\*x+2"):


![images/Presentasi_EMT_#Geometri-013.png](images/Presentasi_EMT_#Geometri-013.png)

b. Dua garis dengan persamaan


$$y=4x+1, y=3x+1$$adalah garis yang sejajar.


Jawaban: Salah


Karena 2 garis tersebut mempunyai kemiringan yang berbeda, yakni 4 dan
3.


\>plot2d("4\*x+1",color=red); plot2d("3\*x+1",\>add):


![images/Presentasi_EMT_#Geometri-015.png](images/Presentasi_EMT_#Geometri-015.png)

Dapat dilihat bahwa gambar tidak sejajar.


c. Garis dengan persamaan


$$-4x-y=8$$

memiliki gambar dengan kemiringan ke kiri.


Jawaban: Benar


$$-4x-y=8$$$$y=-4x-8$$

Garis ini punya kemiringan -4 (negatif), sehingga gambarnya punya
kemiringan ke kiri (turun ke bawah).


\>plot2d("-4\*x-8"):


![images/Presentasi_EMT_#Geometri-019.png](images/Presentasi_EMT_#Geometri-019.png)

## 3) Menggambar Ruas Garis

Ruas garis atau segmen garis adalah bagian dari garis yang memiliki
dua titik ujung. Berbeda dengan garis yang tidak memiliki batas dan
terus memanjang di kedua arah, ruas garis memiliki panjang yang
terbatas karena terbatas oleh dua titik tersebut.


Ruas garis dapat digunakan untuk membentuk objek geometri, salah
satunya adalah segitiga.


\>setPlotRange(-2,2,-2,2); // mendefinisikan bidang koordinat baru


Misalkan diberikan tiga titik.


\>A=[0,-1]; plotPoint(A,"A");

\>B=[-1,0]; plotPoint(B,"B");

\>C=[1,1]; plotPoint(C,"C");


Lalu, akan kita buat ruas garis.


\>plotSegment(A,B,"c"): // c=AB


![images/Presentasi_EMT_#Geometri-020.png](images/Presentasi_EMT_#Geometri-020.png)

\>plotSegment(B,C,"a"): // a=BC


![images/Presentasi_EMT_#Geometri-021.png](images/Presentasi_EMT_#Geometri-021.png)

\>plotSegment(A,C,"b"): // b=AC


![images/Presentasi_EMT_#Geometri-022.png](images/Presentasi_EMT_#Geometri-022.png)

Dari ruas garis di atas, yaitu ruas garis


membentuk segitiga di atas.


\>reset;


## 4) Menggambar segi banyak

Akan digambar segi-n beraturan jika diketahui titik pusat O, n, dan
jarak titik pusat ke titik-titik sudut segi-n tersebut (jari-jari
lingkaran luar segi-n), r.


Contoh: Menggambar segi 6


\>n = 6; // Jumlah sisi

\>r = 1; // Jarak titik pusat ke sudut

\>O = [0, 0]


    [0,  0]

\>t = linspace(0, 2\*pi, n); // Sudut untuk titik-titik sudut

\>x = r \* cos(t);

\>y = r \* sin(t);

\>setPlotRange(-2,2,-2,2); 

\>plot(x, y): //  Gambar segi-n


![images/Presentasi_EMT_#Geometri-023.png](images/Presentasi_EMT_#Geometri-023.png)

## Latihan Soal

Gambarkan plot segi-8, dengan jarak titik pusat ke titik sudutnya
adalah 2


\>n = 8; // Jumlah sisi

\>r = 1; // Jari-jari

\>O = [0, 0]


    [0,  0]

\>t = linspace(0, 2\*pi, n); // Sudut untuk titik-titik sudut

\>x = r \* cos(t);

\>y = r \* sin(t);

\>plot(x, y): //  Gambar segi-n 


![images/Presentasi_EMT_#Geometri-024.png](images/Presentasi_EMT_#Geometri-024.png)

## 5) Menggambar Lingkaran



Lingkaran adalah himpunan semua titik dalam bidang yang memiliki jarak
yang sama dari sebuah titik tetap, yang disebut pusat lingkaran. Jarak
tetap ini disebut jari-jari lingkaran.


Persamaan umum lingkaran ada 2 yaitu


1) Persamaan lingkaran dengan pusat (0,0)




2) Persamaan lingkaran dengan pusat (h,k)


Untuk menggambar lingkaran di EMT, kita dapat menggunakan perintah
plotCircle, circleTrough dan circleWithCenter


1) Menggambar dengan perintah circleThrough


perintah ini dapat digunakan untuk menggambar lingkaran yang melalui 3
titik


Contoh: Menggambar lingkaran yang melalui titik (0,2), (3,5), dan
(6,2)


\>setPlotRange(-7,7,-7,7);

\>A=[0,2]; plotPoint(A,"A");

\>B=[3,5]; plotPoint(B,"B");

\>C=[6,2]; plotPoint(C,"C");

\>c=circleThrough(A,B,C);

\>plotCircle(c):


![images/Presentasi_EMT_#Geometri-025.png](images/Presentasi_EMT_#Geometri-025.png)

2) Menggambar dengan perintah circleWithCenter


Perintah ini digunakan untuk menggambar lingkaran yang telah diketahui
titik pusat dan jari-jari nya. Baris perintah berupa
circleWithCenter(A,r) dengan A adalah pusat dan r adalah jari-jarinya.


Contoh:


Gambar Lingkaran yang memiliki persamaan


$$x^2+y^2+4x-6y+4=0$$\>setPlotRange(-6,6,-6,6);


$$x^2+y^2+4x-6y+4=0$$$$x^2+4x+y^2-6y+4+9-9=0$$$$(x^2+4x+4)+(y^2-6y+9)=9$$$$(x+2)^2+(y-3)^2 = 3^2$$

jadi, pusat lingkaran tersebut adalah (-2,3) dan jari-jarinya 3


\>A=[-2,3]; plotPoint(A,"A");

\>r = 3;

\>d=circleWithCenter(A,r);

\>plotCircle(d):


![images/Presentasi_EMT_#Geometri-031.png](images/Presentasi_EMT_#Geometri-031.png)

## LATIHAN SOAL



Gambarlah lingkaran yang melalui tiga titik berikut ini:


A = [-4,0], B = [4,0], C = [0,4]


\>setPlotRange(-10,10,-10,10);

\>A=[-4,0]; plotPoint(A,"A");

\>B=[4,0]; plotPoint(B,"B");

\>C=[0,4]; plotPoint(C,"C");

\>c=circleThrough(A,B,C);

\>plotCircle(c):


![images/Presentasi_EMT_#Geometri-032.png](images/Presentasi_EMT_#Geometri-032.png)

## 6) Menggambar ellips



Elips adalah bentuk geometri dua dimensi yang dapat didefinisikan
sebagai himpunan semua titik dalam bidang, di mana jumlah jarak dari
dua titik tetap yang disebut fokus ke setiap titik pada elips adalah
konstan. Untuk menggambar ellips kita dapat menggunakan perintah plot.


Persamaan umum ellips:


1) ellips dengan pusat (0,0)


$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

2) ellips dengan pusat (h,k)


$$\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = 1$$

dengan


a = setengah panjang sumbu x


b = setengah panjang sumbu y


jika a&gt;b maka ellips horizontal, jika a&lt;b maka ellips vertikal


Menggambar ellips dengan pusat (0,0)


Contoh:


Gambar ellips yang memiliki persamaan


$$\frac{x^2}{25}+\frac{y^2}{9} = 1$$\>setPlotRange(-10,10,-10,10); // Mengatur bidang koordinat


$$\frac{x^2}{25}+\frac{y^2}{9} = 1$$$$a^2 = 25, a = 5$$$$b^2 = 9, b = 3$$a&gt;b, maka gambarnya akan berupa ellips horizontal


\>a=5; // sumbu semi mayor x

\>b=3; // sumbu semi minor y

\>t = linspace(0, 2\*pi, 100); // parameter t

\>x = a \* cos(t); // koordinat x

\>y = b \* sin(t); // koordinat y

\>plot(x,y):


![images/Presentasi_EMT_#Geometri-039.png](images/Presentasi_EMT_#Geometri-039.png)

Cara lain:


\>x=linspace(0,2\*pi,100); plot2d(sin(x),0.6\*cos(x);r=2):


![images/Presentasi_EMT_#Geometri-040.png](images/Presentasi_EMT_#Geometri-040.png)

Menggambar Ellips dengan pusat (h,k)


Contoh:


Gambar ellips yang mempunyai persamaan


$$\frac{x^2-8x+16}{25} + \frac{y^2+4y+4}{9} =1$$\>setPlotRange(-10,10,-10,10); // Mengatur bidang koordinat


$$\frac{x^2-8x+16}{25} + \frac{y^2+4y+4}{9} = 1$$$$a^2 = 25, a = 5$$$$b^2 = 9, b = 3$$a&gt;b, maka gambarnya akan berupa ellips horizontal


\>a=5; // sumbu semi mayor

\>b=3; // sumbu semi minor

\>t = linspace(0, 2\*pi, 100); // parameter t


$$\frac{x^2-8x+16}{25} + \frac{y^2+4y+4}{9} = 1$$$$(x^2-8x+16) = (x-4)^2$$$$(y^2+4y+4) = (y+2)^2$$$$\frac{(x-4)^2}{25} + \frac{(y+2)^2}{9} = 1$$Jadi, pusat ellips tersebut adalah (4,-2)


\>x = 4+ a \* cos(t); // koordinat x

\>y = -2+ b \* sin(t); // koordinat x

\>plot(x,y):


![images/Presentasi_EMT_#Geometri-049.png](images/Presentasi_EMT_#Geometri-049.png)

## LATIHAN SOAL



Gambar ellips yang mempunyai persamaan


$$\frac{x^2}{16} + \frac{y^2}{36} =1$$\>setPlotRange(-16,16,-16,16);

\>a=4;

\>b=6;

\>t = linspace(0, 2\*pi, 100);

\>x = a\*cos(t);

\>y = b\*sin(t);

\>plot(x,y):


![images/Presentasi_EMT_#Geometri-051.png](images/Presentasi_EMT_#Geometri-051.png)

\>reset;


# 7) Menggambar Parabola

Parabola adalah tempat kedudukan titik-titik yang jaraknya ke suatu
titik tertentu sama dengan jaraknya ke suatu garis tertentu. Bentuk
standar parabola(terbuka ke atas atau ke bawah) dapat dituliskan:


$$y = ax^2+bx+c=0$$a: menentukan kelengkungan parabola; jika a &gt; 0, parabola terbuka ke
atas; jika a &lt; 0, parabola terbuka ke bawah.


b: menggeser parabola ke kiri atau kanan.


c: menentukan titik potong parabola dengan sumbu y.


Sementara itu, parabola dengan sumbu simetri horizontal (terbuka ke
kanan atau kiri) berbentuk:


$$x = ay^2 + by + c$$Jika a &gt; 0, terbuka ke kanan;  jika a &lt; 0, terbuka ke kiri.


Pada subbab ini, akan digambar parabola yang sudah diketahui
persamaannya dan diketahui titik-titik yang diberikan.


## Menggambar Parabola yang Diketahui Persamaannya



Misalkan, suatu parabola sudah diketahui persamaannya.


Contoh:


Gambarkan parabola dengan persamaan:


$$y = 2x^2+4x+2$$\>plot2d("2\*x^2+4\*x+2",-40,40):


![images/Presentasi_EMT_#Geometri-055.png](images/Presentasi_EMT_#Geometri-055.png)

Karena a = 2, berarti a &gt; 0. Parabola terbuka ke atas.


Contoh lain:


Gambarkan parabola dengan persamaan:


$$y = -3x^2+4x-12$$\>plot2d("-3\*x^2+4\*x-12",-30,30):


![images/Presentasi_EMT_#Geometri-057.png](images/Presentasi_EMT_#Geometri-057.png)

Persamaan di atas menunjukkan bahwa nilai a = -3, berarti a &lt; 0, maka
parabola terbuka ke bawah.


Contoh selanjutnya:


Parabola terbuka ke kanan atau kiri


Diberikan persamaan parabola berikut, gambarkan.


$$x = y^2+6y$$$$x = -5y^2+10y+20$$\>plot2d("y^2+6\*y")


    Error : y^2+6*y does not produce a real or column vector
    
    Error generated by error() command
    
    %ploteval:
        error(f$|" does not produce a real or column vector"); 
    adaptiveevalone:
        s=%ploteval(g$,t;args());
    Try "trace errors" to inspect local variables after errors.
    plot2d:
        dw/n,dw/n^2,dw/n,auto;args());

\>y := -40:0.1:40; // rentang nilai y, langkah 0,1

\>x := y^2 + 6\*y;

\>plot2d(x, y, style="lines"):


![images/Presentasi_EMT_#Geometri-060.png](images/Presentasi_EMT_#Geometri-060.png)

Karena persamaan tersebut adalah persamaan berbasis y (bukan x), kita
perlu menggunakan plot parametrik. Kita bisa mengekspresikan x sebagai
fungsi dari y dan kemudian menggambar x terhadap y.


Seperti yang kita lihat, a &gt; 0 pada persamaan parabola sumbu simetri
horizontal, terbuka ke kanan.


\>y := -40:0.1:40;

\>x := -5\*y^2 + 10\*y+20;

\>plot2d(x, y, style="lines"):


![images/Presentasi_EMT_#Geometri-061.png](images/Presentasi_EMT_#Geometri-061.png)

a &lt; 0, terbuka ke kiri.


## Menggambar Parabola yang Melalui Tiga Titik

Contoh:


Gambarkan parabola yang melalui titik A=(0,-4), B=(1,0), dan C=(4,0).


Langkahnya:


- Menggunakan persamaan parabolanya. Untuk soal ini, gunakan sumbu
simetri vertikal. Maka, menggunakan persamaan:


$$y= ax^2+bx+c.$$* 
Substitusikan koordinat titik-titik yang diketahui ke persamaan
* tersebut.

* 
Selesaikan SPL yang terbentuk untuk mendapatkan nilai-nilai a, b, c.

* 
Didapatkan persamaan parabolanya, lalu gambar menggunakan fungsi
* plot2d.


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(5); A=[0,-4]; B=[1,0]; C=[4,0];

\>plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"):


![images/Presentasi_EMT_#Geometri-063.png](images/Presentasi_EMT_#Geometri-063.png)

Substitusi titik A, B, C ke persamaan parabola


$$y = ax^2+bx+c$$Titik A(0,-4)


$$-4 = a(0)^2+b(0)+c$$$$c = -4$$Titik B(1,0)


$$0 = a(1)^2+b(1)+c$$$$0 = a+b+c$$$$a+b =-c$$Titik C(4,0)


$$0 = a(4)^2+b(4)+c$$$$0 = 16a+4b+c$$$$16a+4b =-c$$\>sol &= solve([a+b=-c,16\*a+4\*b=-c,c=-4],[a,b,c]); $sol


$$\left[ \left[ a=-1 , b=5 , c=-4 \right]  \right] $$Dari 3 persamaan tadi, gunakan proses substitusi dan eliminasi untuk
mendapatkan nilai a, b, dan c.


Dari titik A, didapat bahwa


$$c = -4$$Substitusikan ke


$$a+b=-c, 16+4b=-c$$Didapatkan:


$$a+b=4$$$$16a+4b=4$$Eliminasi


$$a + b (4) = 4(4)$$$$4a+4b=16$$$$16a+4b=4$$Kurangkan, didapat:


$$-12a=12$$$$a = -1$$Substitusikan ke


$$a + b = 4$$$$-1+b=4$$$$b=5$$Maka, didapatkan bahwa


$$a=-1, b=5, c=-4$$Persamaan parabolanya menjadi


$$y=x^2+5x-4$$\>function f(x)&=-x^2+5\*x-4; $f(x)


$$-x^2+5\,x-4$$\>plot2d("-x^2+5\*x-4",-100,105):


![images/Presentasi_EMT_#Geometri-089.png](images/Presentasi_EMT_#Geometri-089.png)

## Latihan

1. Gambarkan plot parabola terbuka ke atas/bawah yang diketahui a = 2,
sedangkan b = 3, dan c=0.


Maka, persamaan menjadi:


$$y=2x^2+3x$$\>plot2d("2\*x^2+3\*x",-60,60):


![images/Presentasi_EMT_#Geometri-091.png](images/Presentasi_EMT_#Geometri-091.png)

2. Diketahui persamaan parabola


$$y=ax^2+bx+c$$Suatu parabola melalui titik A=(1,2), B=(2,3), dan C=(3,8). Tentukan
persamaan parabola dan buatlah gambarnya.


Jawaban:


Substitusi titik A, B, C ke persamaan parabola


$$y = ax^2+bx+c$$Titik A(1,2)


$$2 = a(1)^2+b(1)+c$$$$2 = a+b+c$$Titik B(2,3)


$$3 = a(2)^2+b(2)+c$$$$3 = 4a+2b+c$$Titik C(3,8)


$$8 = a(3)^2+b(3)+c$$$$8 = 9a+3b+c$$Didapat 3 persamaan:


$$2 = a+b+c ... (1)$$$$3 = 4a+2b+c...(2)$$$$8 = 9a+3b+c...(3)$$Selesaikan dengan SPL.


Eliminasi (1) dan (2)


$$2 = a+b+c$$$$3 = 4a+2b+c$$

menjadi


$$-1 =-3a+b ...(4)$$Eliminasi (1) dan (3)


$$2 = a+b+c$$$$8 = 9a+3b+c$$

menjadi


$$-6 =-8a-2b...(6)$$Eliminasi (4) dan (6)


$$-1 =-3a+b$$$$-6 =-8a-2b$$

menjadi


$$b =- 5, a =2$$Substitusi ke (1)


$$2 = a+b+c$$$$2 = 2-5+c$$$$c = 5$$Jadi, a = 2, b=-5, c=5


Persamaan parabola menjadi:


$$y=2x^2-5x+5$$\>load geometry


    Numerical and symbolic geometry.

\>reset;

\>setPlotRange(10); A=[1,2]; B=[2,3]; C=[3,8];

\>plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"):


![images/Presentasi_EMT_#Geometri-116.png](images/Presentasi_EMT_#Geometri-116.png)

\>sol &= solve([a+b+c=2,4\*a+2\*b+c=3,9\*a+3\*b+c=8],[a,b,c]); $sol


$$\left[ \left[ a=2 , b=-5 , c=5 \right]  \right] $$\>function f(x)&=2\*x^2-5\*x+5; $f(x)


$$2\,x^2-5\,x+5$$\>plot2d("2\*x^2-5\*x+5",-100,105):


![images/Presentasi_EMT_#Geometri-119.png](images/Presentasi_EMT_#Geometri-119.png)

# 8) Menggambar Hiperbola

Hiperbola adalah tempat kedudukan titik-titik yang selisih jaraknya ke
dua titik tertentu tetap. Hiperbola memiliki bentuk persamaan umum:


Hiperbola vertikal (terbuka ke atas atau bawah)


$$\frac{(y-k)^2}{a^2}-\frac{(x-h)^2}{b^2}=1$$Hiperbola horizontal (terbuka ke kanan atau kiri)


$$\frac{(x-h)^2}{a^2}-\frac{(y-k)^2}{b^2}=1$$Dengan (h, k) adalah pusatnya.


Misalkan, diberikan suatu hiperbola dengan persamaan


$$\frac{x^2}{1}-\frac{y^2}{0,25}=1$$Gambarkan hiperbolanya.


\>a = 1; // Jarak dari pusat ke titik pada sumbu x

\>b = 0.5; // Jarak dari pusat ke titik pada sumbu y

\>t = linspace(-2, 2, 100);

\>x = [a \* cosh(t), -a \* cosh(t)];

\>y = [b \* sinh(t), b \* sinh(t)];

\>plot2d(x, y):


![images/Presentasi_EMT_#Geometri-123.png](images/Presentasi_EMT_#Geometri-123.png)

# Sub Materi 4

## Menentukan Titik Tengah Ruas Garis

Titik tengah dari ruas garis adalah titik yang membagi ruas garis
tersebut menjadi dua bagian yang sama panjang. Misalkan titik A(x1,y1)
dan B(x2,y2), maka titik tengah M dari ruas AB dapat dihitung dengan:


$$M = \left (\frac {x_1+x_2} {2}, \frac {y_1+y_2} {2} \right)$$\>load geometry


    Numerical and symbolic geometry.

\>A := [11,-2];

\>B := [-5,16];

\>M := (A + B)/2;

\>M


    [3,  7]

Menggunakan cara manual


Titik tengah:


$$\left(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}\right)$$Diketahui:


A = (11, -2)


B = (-5, 16)


Tentukan titik tengah?


$$x = \frac{x_1 + x_2}{2} = \frac{11 + (-5)}{2} = 3$$$$y = \frac{y_1 + y_2}{2} = \frac{-2 + 16}{2} = 7$$Jadi, titik tengahnya adalah (3, 7)


\>function f(x) := 2x+3;

\>a := 2; b := 0; c := 3; // ketika memotong di sumbu x (y=0)

\>X := -(c / a); 

\>X // hasilnya (X,0) = (-1.5,0)


    -1.5

\>a := 0; b := -1; c := 3; // ketika memotong di sumbu y (x=0)

\>Y := -(c / b) // hasilnya (0,Y) = (0,3)


    3

\>C := [-1.5,0]; // Menentukan titik tengah

\>D := [0,3];

\>M := (C + D)/2;

\>M


    [-0.75,  1.5]

Diketahui fungsi:


$$f(x) = 2x + 3$$Tentukan titik potong dengan sumbu x dan y:


Untuk sumbu x (y = 0):


$$0 = 2x + 3$$$$x = -\frac{3}{2} = -1.5$$Untuk sumbu y (x = 0):


$$y = 2(0) + 3$$$$y = 3$$Jadi, titik potong dengan sumbu x dan y adalah


$$(-1.5, 0) dan (0, 3).$$Tentukan titik tengah?


$$x = \frac{x_1 + x_2}{2} = \frac{-1,5 + 0}{2} = -0.75$$$$y = \frac{y_1 + y_2}{2} = \frac{0 + 3}{2} = 1.5$$Jadi, titik tengahnya adalah (-0.75, 1.5)


## LATIHAN SOAL

1. Diketahui titik A(2, 3) dan B(8, 7). Tentukan koordinat titik
tengah ruas garis AB.


\>A := [2,3];

\>B := [8,7];

\>M(A,B) := (A + B)/2;


    Unexpected "(". Index () not allowed in strict mode!
    In Euler files, use relax to avoid this.
    Error in:
    M(A,B) := (A + B)/2; ...
          ^

\>M


    [-0.75,  1.5]

2. Diketahui persamaan garis 3x+4y-12=0. Tentukan titik tengah dari
segmen garis yang menghubungkan dua titik potong garis tersebut dengan
sumbu koordinat.


\>function f(x) := (3/4)x-3;

\>a := 3/4; b := 0; c := -3; // ketika memotong di sumbu x (y=0)

\>X := -(c / a);

\>X // hasilnya (X,0) = (4,0)


    4

\>a := 0; b := -1; c := -3; // ketika memotong di sumbu y (x=0)

\>Y := -(c / b) // hasilnya (0,Y) = (0,-3)


    -3

\>J := [4,0]; // Menentukan titik tengah

\>K := [0,-3];

\>M := (J + K)/2;

\>M


    [2,  -1.5]

## Titik Potong Dua Garis

Titik potong dua garis adalah titik di mana kedua garis tersebut
berinterseksi atau bertemu. Dalam sistem koordinat dua dimensi, setiap
garis dapat dinyatakan dengan persamaan linear, biasanya dalam bentuk


y=mx+b, di mana m adalah kemiringan garis dan b adalah titik potong
garis dengan sumbu-y.


\>A &= [1,2]; B &= [4,6]; C &= [2,5];

\>p &= lineThrough(A,B)


    
                                 [- 4, 3, 2]
    

\>$getLineEquation(p,x,y), $solve(%,y) | expand


$$3\,y-4\,x=2$$$$\left[ y=\frac{4\,x}{3}+\frac{2}{3} \right] $$\>q &= lineThrough(A,C)


    
                                [- 3, 1, - 1]
    

\>$getLineEquation(q,x,y), $solve(%,y) | expand


$$y-3\,x=-1$$$$\left[ y=3\,x-1 \right] $$\>H &= lineIntersection(p,q)


    
                                    [1, 2]
    

Menggunakan cara manual


A = (1,2)


B = (4,6)


C = (2,5)


Persamaan garis melalui A dan B:


$$\frac{x-x_1}{x_2-x_1} = \frac{y-y_1}{y_2-y_1}$$$$\Rightarrow \frac{x-1}{4-1} = \frac{y-2}{6-2}$$$$\Rightarrow \frac{x-1}{3} = \frac{y-2}{4}$$$$\Rightarrow 4(x-1) = 3(y-2)$$$$\Rightarrow 4x - 4 = 3y - 6$$$$\Rightarrow y = \frac{4}{3}x + \frac{2}{3} \quad ...(1)$$Persamaan garis melalui A dan C:


$$\frac{x-x_1}{x_2-x_1} = \frac{y-y_1}{y_2-y_1}$$$$\Rightarrow \frac{x-1}{2-1} = \frac{y-2}{5-2}$$$$\Rightarrow x-1 = \frac{y-2}{3}$$$$\Rightarrow 3x - 3 = y - 2$$$$\Rightarrow y = 3x - 1 \quad ...(2)$$Substitusi (2) ke (1):


$$3x - 1 = \frac{4}{3}x + \frac{2}{3}$$$$\Rightarrow 9x - 3 = 4x + 2$$$$\Rightarrow 5x = 5$$$$\Rightarrow x = 1$$Substitusi x = 1 ke (2):


$$y = 3(1) - 1$$$$\Rightarrow y = 2$$Jadi, titik potong adalah (1,2).


## LATIHAN SOAL

1. Diketahui A(2,3), B(5,8), C(4,1). Tentukan persamaan garis yang
melaui titik AB dan persamaan garis yang melalui titik BC. Apakah
kedua garis berpotongan? Jika iya, di titik berapa?


\>A &= [2,3]; B &= [5,8]; C &= [4,1]; 

\>t &= lineThrough(A,B)


    
                                [- 5, 3, - 1]
    

\>$getLineEquation(t,x,y), $solve(%,y) | expand 


$$3\,y-5\,x=-1$$$$\left[ y=\frac{5\,x}{3}-\frac{1}{3} \right] $$\>u &= lineThrough(B,C)


    
                                 [7, - 1, 27]
    

\>$getLineEquation(u,x,y), $solve(%,y) | expand


$$7\,x-y=27$$$$\left[ y=7\,x-27 \right] $$\>plot2d(["(5/3)\*x-1/3", "7\*x-27"],-5,10,5,10):


![images/Presentasi_EMT_#Geometri-161.png](images/Presentasi_EMT_#Geometri-161.png)

\>H &= lineIntersection(t,u)


    
                                    [5, 8]
    

\>plot2d(["(5/3)\*x-1/3", "7\*x-27"],-10,10,0,15); plot2d(5,8,\>points,style="ow",\>add):


![images/Presentasi_EMT_#Geometri-162.png](images/Presentasi_EMT_#Geometri-162.png)

Ya, kedua garis berpotongan. 


2. Diketahui A(2,3), B(5,6), C(4,5). Tentukan persamaan garis yang
melaui titik AB dan persamaan garis yang melalui titik AC. Apakah
kedua garis berpotongan? Jika iya, di titik berapa?


\>A &= [1,2]; B &= [4,5]; C &= [3,4]; 

\>v &= lineThrough(A,B)


    
                                 [- 3, 3, 3]
    

\>$getLineEquation(v,x,y), $solve(%,y) | expand


$$3\,y-3\,x=3$$$$\left[ y=x+1 \right] $$\>w &= lineThrough(A,C)


    
                                 [- 2, 2, 2]
    

\>$getLineEquation(w,x,y), $solve(%,y) | expand


$$2\,y-2\,x=2$$$$\left[ y=x+1 \right] $$Didapat bahwa persamaan garisnya adalah sama, artinya kedua garis
berimpit. Pada kasus ini, titik potongnya adalah berada di sepanjang
garis. Namun, titik potong pada garis yang berimpit adalah tidak
berbeda atau tidak unik.


Berikut ditunjukkan plotnya.


\>plot2d(["x+1", "x+1"],-5,10,5,10):


![images/Presentasi_EMT_#Geometri-167.png](images/Presentasi_EMT_#Geometri-167.png)

## Menentukan Titik Potong Garis dan Lingkaran

Titik potong antara garis dan lingkaran adalah titik-titik di mana
kedua objek tersebut berpotongan yang secara geometris ada tiga
kemungkinan dengan melalui rumus


$$D = b^2-4ac$$dengan D = nilai Diskriminan persamaan kuadrat, a = koefisien x^2 atau
y^2, b = koefisien x atau y, dan c = konstanta. Saat nilai D diperoleh
maka akan ada tiga kemungkinan, yaitu:


1. D &gt; 0 (memotong di dua titik)


2. D = 0 (memotong di satu titik/menyinggung)


3. D &lt; 0 (tidak ada titik potong)


Mendefinisikan titik A dan c berpusat di titik A dengan jari-jari 4


\>A &:= [1,0]; c=circleWithCenter(A,4);

\>B &:= [1,2]; C &:= [2,1]; // mendefinisikan titik B dan C

\>l=lineThrough(B,C); // Membuat garis l melalui titik B dan C

\>setPlotRange(5); // Mengatur jangkauan garis sumbu x dan y

\>plotCircle(c); // Menampilkan lingkaran c

\>plotLine(l): // Menampilkan garis l


![images/Presentasi_EMT_#Geometri-169.png](images/Presentasi_EMT_#Geometri-169.png)

Perpotongan garis dengan lingkaran menghasilkan dua titik dan jumlah
titik potong


\>{P1,P2,f}=lineCircleIntersections(l,c);

\>P1, P2, f // P1=titik potong 1, P2=titik potong 2, f=jumlah titik potong


    [4.64575,  -1.64575]
    [-0.645751,  3.64575]
    2

\>plotPoint(P1); plotPoint(P2):


![images/Presentasi_EMT_#Geometri-170.png](images/Presentasi_EMT_#Geometri-170.png)

\>c &= circleWithCenter(A,4) // Definisi c=lingkaran dengan pusat A & jari-jari 4


    
                                  [1, 0, 4]
    

Keterangan hasil


1: koordinat x pusat lingkaran, yaitu 1.


0: koordinat y dari pusat lingkaran, yaitu 0.


4: Jari-jari lingkaran, yaitu 4.


Diketahui:


A=(1,0); B=(1,2); C=(2,1)


Rumus persamaan lingkaran dengan pusat (h,k) das jari-jari r


$$(x-h)^2+(y-k)^2=r^2$$Pusat A(1,0) dan r = 4.


$$(x-1)^2+(y-0)^2 = 4^2$$$$(x-1)^2+y^2 = 16$$$$x^2-2x+1+y^2=16$$$$x^2+y^2-2x-15=0$$\>l &= lineThrough(B,C) // garis l melalui BC menghasilkan koef x,y,c(konstanta)


    
                                  [1, 1, 3]
    

\>$getLineEquation(l,x,y), $solve(%,y) // persamaan garis l menggunakan EMT


$$y+x=3$$$$\left[ y=3-x \right] $$Menggunakan cara manual


Diketahui:


 B(x1,y1) = B(1,2)


 C(x2,y2) = C(2,1)


 Rumus menentukan persamaan garis melalui dua titik, yaitu  

$$\frac {y_2-y_1} {y-y_1} = \frac {x_2-x_1} {x-x_1}$$$$\frac {1-2} {y-2} = \frac {2-1} {x-1}$$$$\frac {-1} {y-2} = \frac {1} {x-1}$$$$-1(x-1) = 1(y-2)$$$$-x+1 = y-2$$$$y+x=3$$$$y = 3-x$$

Terbukti.


\>$lineCircleIntersections(l,c) | radcan, // titik potong lingkaran c dan garis l


$$\left[ \left[ \sqrt{7}+2 , 1-\sqrt{7} \right]  , \left[ 2-\sqrt{7}
  , \sqrt{7}+1 \right]  \right] $$Substitusi y=3-x ke persamaan


$$x^2+y^2-2x-15=0$$$$x^2+(3-x)^2-2x-15=0$$$$x^2+9-6x+x^2-2x-15=0$$$$2x^2-8x-6=0$$$$x^2-4x-3=0$$Cek apakah memotong atau tidak


$$D = b^2-4ac$$$$D = (-4)^2-4(1)(-3)$$$$D = 16+12 = 28 > 0$$karena D &gt; 0, maka memotong di dua titik.


Mencari titik potong:


$$x_{1,2} = \frac {-b \pm \sqrt{b^2-4ac}} {2a}$$$$        = \frac {-b \pm \sqrt{D}} {2a}$$$$        = \frac {-(-4) \pm \sqrt{28}} {2.1}$$$$        = \frac {4 \pm \sqrt{28}} {2}$$$$        = \frac {4 \pm 2\sqrt{7}} {2}$$$$        = 2 \pm \sqrt{7}$$$$x_1 = 2+\sqrt{7} = 4.4645$$$$x_2 = 2-\sqrt{7} = -0.645$$menentukan y1 dan y2 dengan substitusi x1 dan x2 ke persamaan y=3-x


$$3-(2 + \sqrt{7}) = 1+\sqrt{7} = -1.645$$$$3-(2 - \sqrt{7}) = 1-\sqrt{7} = 3.645$$Jadi, titik potongnya adalah


$$(2+\sqrt{7},1+\sqrt{7}) (2-\sqrt{7},1-\sqrt{7})$$

atau


$$(4.4645,-1.645) (-0.645,3.645)$$Akan ditunjukkan bahwa sudut-sudut yang menghadap busur yang sama
adalah sama besar


\>C=A+normalize([-2,-3])\*4; plotPoint(C); plotSegment(P1,C); plotSegment(P2,C);

\>degprint(computeAngle(P1,C,P2))


    69°17'42.68''

\>C=A+normalize([-4,-3])\*4; plotPoint(C); plotSegment(P1,C); plotSegment(P2,C); 

\>degprint(computeAngle(P1,C,P2))


    69°17'42.68''

\>insimg;


![images/Presentasi_EMT_#Geometri-206.png](images/Presentasi_EMT_#Geometri-206.png)

image: SudutKel.JPEG


$$m \angle PRQ = m \angle PSQ$$Diketahui sudut pusat = 2*sudut keliling


$$\angle POQ = 2\angle PSQ$$$$\angle POQ = 2\angle PRQ$$$$2\angle PSQ = 2\angle PRQ$$$$\angle PSQ = \angle PRQ$$

Terbukti.


## LATIHAN SOAL



1. Diketahui sebuah lingkaran dengan pusat di titik O(2,3) dengan r=5
dan sebuah garis yang melalui A(1,1) dan B(4,5). Tentukan titik
perpotongan garis dan lingkaran tersebut.


\>O &:= [2,3]; c=circleWithCenter(O,5);

\>A &:= [1,1]; B &:= [4,5]; l=lineThrough(A,B);

\>setPlotRange(10); plotCircle(c); plotLine(l):


![images/Presentasi_EMT_#Geometri-212.png](images/Presentasi_EMT_#Geometri-212.png)

\>{P1,P2,f}=lineCircleIntersections(l,c);

\>P1, P2, f


    [5.31038,  6.74718]
    [-0.670385,  -1.22718]
    2

2. Dari soal no 1, Tentukanlah besar sudut keliling yang dibentuk
menghadap busur AB. tunjukkan juga bahwa sudut kelilingnya adalah sama


\>plotPoint(P1); plotPoint(P2):


![images/Presentasi_EMT_#Geometri-213.png](images/Presentasi_EMT_#Geometri-213.png)

\>$lineCircleIntersections(l,c) | radcan, // titik potong lingkaran c dan garis l


$$\left[ \left[ \sqrt{7}+2 , 1-\sqrt{7} \right]  , \left[ 2-\sqrt{7}
  , \sqrt{7}+1 \right]  \right] $$\>M=O+normalize([-5,-1])\*5; plotPoint(M); plotSegment(P1,M); plotSegment(P2,M);

\>degprint(computeAngle(P1,M,P2))


    85°24'41.16''

\>N=O+normalize([-2,3])\*5; plotPoint(N); plotSegment(P1,N); plotSegment(P2,N);

\>degprint(computeAngle(P1,N,P2))


    85°24'41.16''

\>insimg:


![images/Presentasi_EMT_#Geometri-215.png](images/Presentasi_EMT_#Geometri-215.png)

![images/Presentasi_EMT_#Geometri-216.png](images/Presentasi_EMT_#Geometri-216.png)

## Titik Potong 2 Lingkaran

\>A=[1,3]; B=[-1,-2];

\>c1=circleWithCenter(A,4);

\>c2=circleWithCenter(B,6);

\>{P1,P2,f}=circleCircleIntersections(c1,c2);

\>l=lineThrough(P1,P2);

\>setPlotRange(5); plotCircle(c1); plotCircle(c2);

\>plotPoint(A); plotPoint(B); plotPoint(P1); plotPoint(P2); plotLine(l):


![images/Presentasi_EMT_#Geometri-217.png](images/Presentasi_EMT_#Geometri-217.png)

\>{P1,P2}=circleCircleIntersections(c1,c2)


    [4.32162,  0.771353]

\>P1, P2


    [4.32162,  0.771353]
    [-2.94231,  3.67692]

Apakah berpotongan untuk pusat A dan B dengan masing-masing
jari-jarinya?


A=(1,3), r=4


B=(-1,-2), r=6


Persamaan lingkaran A dengan pusat (h,k) dan jari-jari r:


$$(x-h)^2+(y-k)^2=r^2$$$$\Rightarrow (x-1)^2 + (y-3)^2 = 4^2$$$$\Rightarrow x^2 - 2x + 1 + y^2 - 10y + 25 = 16$$$$\Rightarrow x^2 + y^2 - 2x - 10y + 10 = 0 \quad ... (1)$$Persamaan Lingkaran B dengan pusat (h,k) dan jari-jari r:


$$(x+1)^2 + (y+2)^2 = 6^2$$$$\Rightarrow x^2 + 2x + 1 + y^2 + 4y + 4 = 36$$$$\Rightarrow x^2 + y^2 + 2x + 4y - 31 = 0 \quad ... (2)$$kurangkan persamaan (2) dari persamaan (1):


$$\Rightarrow -4x - 14y + 41 = 0$$$$\Rightarrow 4x = 41 - 14y$$$$\Rightarrow x = \frac{41 - 14y}{4}$$Substitusi nilai x ke persamaan (1):


$$\left(\frac{41 - 14y}{4}\right)^2 + y^2 - 2\left(\frac{41 - 14y}{4}\right) - 10y + 10 = 0$$$$116y^2 - 516y + 329 = 0$$$$\Rightarrow 116y^2 - 516y + 329 = 0$$Cek apakah memotong atau tidak:


$$D = b^2 - 4ac$$$$\Rightarrow (-516)^2 - 4\cdot 116 \cdot 329 = 113600 > 0, D > 0$$$$y_{1,2} = \frac{-b \pm \sqrt{D}}{2a}$$$$\frac{-(-516) \pm \sqrt{113600}}{2 \cdot 116}$$$$\frac{516 \pm \sqrt{16 \cdot 7100}}{232}$$$$\frac{516 \pm 40 \sqrt{71}}{232}$$$$y_1 = \frac{516 + 40 \sqrt{71}}{232}$$$$\approx 3.676, \quad x = \frac{25 - 10(3.676)}{4}$$$$\approx -2.940$$$$y_2 = \frac{516 - 40 \sqrt{71}}{232}$$$$\approx 0.771, \quad x = \frac{25 - 10(0.771)}{4}$$$$\approx 4.322$$$$\Rightarrow \text{Titik potong: } (-2.940, 3.676) \text{ dan } (4.322, 0.771)$$## LATIHAN  SOAL

1. Diketahui dua lingkaran dengan pusat K(2,3) dengan r=4 dan pusat
L(6,7) dengan r=3. Tunjukan titik potong kedua lingkaran tersebut.


\>K=[2,3]; L=[6,7];

\>c1=circleWithCenter(K,4);

\>c2=circleWithCenter(L,3);

\>{Z1,Z2,f}=circleCircleIntersections(c1,c2);

\>l=lineThrough(P1,P2);

\>setPlotRange(10); plotCircle(c1); plotCircle(c2);

\>plotPoint(K); plotPoint(L); plotPoint(Z1); plotPoint(Z2); plotLine(l):


![images/Presentasi_EMT_#Geometri-244.png](images/Presentasi_EMT_#Geometri-244.png)

\>{Z1,Z2}=circleCircleIntersections(c1,c2)


    [3.00272,  6.87228]

\>Z1, Z2


    [3.00272,  6.87228]
    [5.87228,  4.00272]

2. Diketahui dua lingkaran dengan pusat M(2,1) dengan r=6 dan pusat
N(5,5) dengan r=-3. Apakah kedua lingkaran mempunyai titik potong?
Mengapa?


Perhatikan jari-jari lingkaran kedua yaitu r=-3, hal ini sangat ganjil
karena r adalah jarak atau panjang yang selalu bernilai positif atau
0. Adapun lingkaran tersebut akan menjadi tidak valid.


Jadi, bisa disimpulkan bahwa tidak ada perpotongan antar kedua
lingkaran tersebut.


3. Diketahui dua lingkaran dengan pusat R(1,1) dengan r=3 dan pusat
S(8,1) dengan r=2. Apakah kedua lingkaran mempunyai titik potong? Jika
tidak maka bagaimana kedudukannya?


\>R=[1,1]; S=[8,1];

\>c1=circleWithCenter(R,3);

\>c2=circleWithCenter(S,2);

\>{P1,P2,f}=circleCircleIntersections(c1,c2);

\>l=lineThrough(P1,P2);

\>setPlotRange(15); plotCircle(c1); plotCircle(c2);

\>plotPoint(R); plotPoint(S); plotPoint(P1); plotPoint(P2); plotLine(l):


![images/Presentasi_EMT_#Geometri-245.png](images/Presentasi_EMT_#Geometri-245.png)

 Terlihat bahwa lingkaran R dan S tidak berpotongan sehingga kondisi  
 seperti ini tidak memungkinkan untuk mendapatkan titik potong kedua  
 lingkaran tersebut. Atau simplenya lingkaran R dan S adalah saling  
 asing.  

\> 


# Persamaan Garis Melalui Dua Titik

\>load geometry


    Numerical and symbolic geometry.

$$\text{Misalkan terdapat dua titik } A(x_1, y_1) \text{ dan } B(x_2, y_2).$$$$\text{Gradien garis } m \text{ dari garis yang melalui dua titik } A \text{ dan } B \text{ adalah:}$$$$m = \frac{y_2 - y_1}{x_2 - x_1}$$$$\text{Dengan gradien } m \text{ dan titik } A(x_1, y_1), \text{ persamaan garis dalam bentuk titik-kemiringan (point-slope) adalah:}$$$$y - y_1 = m(x - x_1)$$$$\text{Setelah disederhanakan, bentuk eksplisit dari persamaan garis tersebut adalah:}$$$$y = mx + c$$$$\text{Atau dalam bentuk umum:}$$$$Ax + By + C = 0$$$$\text{Dimana } A, B, \text{ dan } C \text{ adalah konstanta-konstanta yang menentukan garis linear.}$$diberikan titik


$$A(2,1)\text{dan}B(-1,-4)$$\>A &= [2,1]; B &= [-1,-4]; // menentukan dua titik A, B


Fungsi untuk garis dan lingkaran bekerja seperti fungsi Euler, tetapi
menyediakan komputasi simbolis


\>c &= lineThrough(A,B) // c=AB


    
                                 [5, - 3, 7]
    

\>function f(x)


    endfunction
</pre>
Kita bisa mendapatkan persamaan untuk sebuah garis dengan mudah.
dengan Fungsi:


getLineEquation (g,x,y): persamaan garis g dinyatakan dalam x dan y


\>$getLineEquation(c,x,y), $solve(%,y) | expand // persamaan garis c


$$5\,x-3\,y=7$$$$\left[ y=\frac{5\,x}{3}-\frac{7}{3} \right] $$\>$getLineEquation(lineThrough([2,1],[-1,-4]),x,y), $solve(%,y) // persamaan garis melalui(x1, y1) dan (x2, y2)


$$5\,x-3\,y=7$$$$\left[ y=\frac{5\,x-7}{3} \right] $$Pembuktian secara manual:


$$A = (2, 1), \quad B = (-1, -4)$$$$\text{Gradien } m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{-4 - 1}{-1 - 2} = \frac{-5}{-3} = \frac{5}{3}$$$$\text{Persamaan garis: }$$$$y - y_A = m(x - x_A)$$$$y - 1 = \frac{5}{3}(x - 2)$$$$y - 1 = \frac{5}{3}x - \frac{10}{3}$$$$y = \frac{5}{3}x - \frac{10}{3} + 1$$$$y = \frac{5}{3}x - \frac{7}{3}$$$$\text{Kalikan dengan 3 untuk menghilangkan penyebut:}$$$$3y = 5x - 7$$$$5x - 3y - 7 = 0$$\>function f(x):=(5x/3)-(7/3);

\>plot2d("(5x/3)-(7/3)",r=4,grid=8): 


![images/Presentasi_EMT_#Geometri-272.png](images/Presentasi_EMT_#Geometri-272.png)

## Latihan

Tentukan persamaan garis yang melalui titik A(2,3) dan B(4,1)


\>E = [2,3]; //mendefinisikan titik E

\>F = [4,1]; //mendefinisikan titik F

\>$getLineEquation(lineThrough([2,3],[4,1]),x,y), $solve(%,y) 


$$2\,y+2\,x=10$$$$\left[ y=5-x \right] $$pembuktian manual:


$$A = (2, 3), \quad B = (4, 1)$$$$\text{Gradien } m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{1 - 3}{4 - 2} = \frac{-2}{2} = -1$$$$\text{Persamaan garis: }$$$$y - y_A = m(x - x_A)$$$$y - 3 = -1(x - 2)$$$$y - 3 = -x + 2$$$$y = -x + 2 + 3$$$$y = -x + 5$$$$\text{Kalikan dengan -1 untuk menghilangkan tanda negatif:}$$$$x + y - 5 = 0$$\>function f(x):=-x+5;

\>plot2d("-x+5",r=6,grid=8,\>frame):


![images/Presentasi_EMT_#Geometri-285.png](images/Presentasi_EMT_#Geometri-285.png)

# Garis Sumbu

Garis sumbu pada dua lingkaran biasanya merujuk pada garis yang
menghubungkan pusat dua lingkaran dan berada di tengah-tengah antara
kedua lingkaran tersebut. Dalam konteks geometri, garis sumbu dapat
membantu menentukan lokasi persimpangan atau titik-titik lain yang
berkaitan dengan kedua lingkaran.


Berikut adalah langkah-langkah menggambar garis sumbu ruas garis AB:


1. Gambar lingkaran dengan pusat A melalui B.


2. Gambar lingkaran dengan pusat B melalui A.


3. Tarik garis melallui kedua titik potong kedua lingkaran tersebut.
Garis ini merupakan garis sumbu (melalui titik tengah dan tegak lurus)
AB.


\>A=[2,2]; B=[-1,-2]; //mendefinisikan titik

\>c1=circleWithCenter(A,distance(A,B)); //membuat lingkaran c1 berpusat di titik A dan jari-jarinya adalah jarak titik A dengan B 

\>c2=circleWithCenter(B,distance(A,B)); //membuat lingkaran c2 berpusat di titik B dan jari-jarinya adalah jarak titik A dengan B

\>{P1,P2,f}=circleCircleIntersections(c1,c2); //mencari titik potong lingkaran c1 dan c2 

\>l=lineThrough(P1,P2); //membuat garis yang melalui titik potong dua lingkaran

\>setPlotRange(8); plotCircle(c1); plotCircle(c2): //menggambar lingkaran di bidang grafik


![images/Presentasi_EMT_#Geometri-286.png](images/Presentasi_EMT_#Geometri-286.png)

\>plotPoint(A); plotPoint(B); plotSegment(A,B); plotLine(l):


![images/Presentasi_EMT_#Geometri-287.png](images/Presentasi_EMT_#Geometri-287.png)

Selanjutnya, kami melakukan hal yang sama di Maxima dengan koordinat
umum.


\>A &= [x1,y1]; B &= [x2,y2];

\>c1 &= circleWithCenter(A,distance(A,B));

\>c2 &= circleWithCenter(B,distance(A,B));

\>P &= circleCircleIntersections(c1,c2); P1 &= P[1]; P2 &= P[2];


Persamaan untuk persimpangan cukup rumit. Tetapi kita dapat
menyederhanakannya, jika kita menyelesaikan untuk y.


\>g &= getLineEquation(lineThrough(P1,P2),x,y);

\>$solve(g,y)


$$\left[ y=\frac{{\it y_2}^2-{\it y_1}^2+{\it x_2}^2-2\,x\,{\it x_2}-
 {\it x_1}^2+2\,x\,{\it x_1}}{2\,{\it y_2}-2\,{\it y_1}} \right] $$Persamaan untuk persimpangan cukup rumit. Tetapi kita dapat
menyederhanakannya, jika kita menyelesaikan untuk y.


\>$solve(getLineEquation(middlePerpendicular(A,B),x,y),y)


$$\left[ y=\frac{{\it y_2}^2-{\it y_1}^2+{\it x_2}^2-2\,x\,{\it x_2}-
 {\it x_1}^2+2\,x\,{\it x_1}}{2\,{\it y_2}-2\,{\it y_1}} \right] $$\>h &=getLineEquation(lineThrough(A,B),x,y);

\>$solve(h,y)


$$\left[ y=\frac{-\left({\it x_1}-x\right)\,{\it y_2}-\left(x-
 {\it x_2}\right)\,{\it y_1}}{{\it x_2}-{\it x_1}} \right] $$Perhatikan hasil kali gradien garis g dan h adalah:


$$\frac{-(x_2-x_1)}{(y_2-y_1)}\times \frac{(y_2-y_1)}{(x_2-x_1)} = -1.$$Artinya kedua garis tegak lurus.


\> 


# Garis Bagi Sudut

Garis bagi sudut adalah garis, sinar, atau ruas garis yang membagi
sudut menjadi dua bagian yang sama besar (kongruen). Garis bagi sudut
juga merupakan tempat kedudukan titik-titik yang memiliki jarak yang
sama dengan kedua lengan sudut.


Untuk menggambar objek-objek geometri, langkah pertama adalah
menentukan rentang sumbu-sumbu koordinat. Semua objek geometri akan
digambar pada satu bidang koordinat, sampai didefinisikan bidang
koordinat yang baru.


\>setPlotRange(-0.5,2.5,-0.5,2.5); // mendefinisikan bidang koordinat baru 


Sekarang, tetapkan tiga titik dan plotkan


\>A=[1,0]; plotPoint(A,"A"); // definisi dan gambar tiga titik

\>B=[0,1]; plotPoint(B,"B");

\>C=[2,2]; plotPoint(C,"C"); 


Kemudian tiga segmen.


\>plotSegment(A,B,"c"); // c=AB

\>plotSegment(B,C,"a"); // a=BC

\>plotSegment(A,C,"b"); // b=AC 

\>l=angleBisector(A,C,B); // garis bagi <ACB

\>degprint(computeAngle(A,C,B))


    36°52'11.63''

\>g=angleBisector(C,A,B); // garis bagi <CAB

\>degprint(computeAngle(C,A,B))


    71°33'54.18''

\>j=angleBisector(A,B,C); // garis bagi <ABC

\>degprint(computeAngle(A,B,C))


    71°33'54.18''

\>color(5); plotLine(l); plotLine(g); plotLine(j); color(1): 


![images/Presentasi_EMT_#Geometri-292.png](images/Presentasi_EMT_#Geometri-292.png)

## Latihan

diberikan tiga titik A(1,2), B(5,6), C(3,4)


\>setPlotRange(-10,10,-10,10); // mendefinisikan bidang koordinat baru 


Sekarang, tetapkan tiga titik dan plotkan


\>G=[5,1]; plotPoint(G,"G"); // definisi dan gambar tiga titik

\>H=[-4,2]; plotPoint(H,"H");

\>I=[0,7]; plotPoint(I,"I"); 


Kemudian tiga segmen.


\>plotSegment(G,H,"c"); // c=AB

\>plotSegment(G,I,"a"); // a=BC

\>plotSegment(H,I,"b"); // b=AC 

\>l=angleBisector(G,H,I); // garis bagi <GHI 

\>computeAngle(G,H,I)\*(180/pi)


    57.6803834918

\>g=angleBisector(G,I,H); // garis bagi <GIH

\>computeAngle(G,I,H)\*(180/pi)


    78.4653793464

\>j=angleBisector(I,G,H); // garis bagi <IGH

\>computeAngle(I,G,H)\*(180/pi)


    43.8542371618

\>color(5); plotLine(l); plotLine(g); plotLine(j); color(1):


![images/Presentasi_EMT_#Geometri-293.png](images/Presentasi_EMT_#Geometri-293.png)

# Sub Materi 5

## Garis berat pada segitiga



Garis berat adalah garis yang ditarik dari salah satu titik sudut
segitiga menuju titik tengah sisi yang berhadapan. Jadi, garis ini
membagi sisi yang berhadapan menjadi dua bagian yang sama panjang.


alam segitiga, terdapat tiga garis berat, dan ketiga garis tersebut
akan bertemu di satu titik yang disebut titik berat (centroid). Titik
berat adalah titik yang menjadi pusat massa dari segitiga, di mana
segitiga dapat seimbang jika ditopang pada titik ini.


\>                                                                                   


\>load geometry


    Numerical and symbolic geometry.

$$AD = m_a$$$$BD = CD = \frac{c}{2}$$$$AB^2 = AD^2 + BD^2$$$$AC^2 = AD^2 + CD^2$$$$b^2 = m_a^2 + \left(\frac{c}{2}\right)^2$$$$c^2 = m_a^2 + \left(\frac{b}{2}\right)^2$$$$b^2 + c^2 = 2m_a^2 + 2\left(\frac{a}{2}\right)^2$$$$m_a^2 = \frac{2b^2 + 2c^2 - a^2}{4}$$$$m_a = \frac{1}{2} \sqrt{2b^2 + 2c^2 - a^2}$$\>function m(a,b,c) := ((sqrt(2\*B^2 + 2\*C-A^2)/2)

\>setPlotRange(-0.5,2.5,-0.5,2.5); // mendefinisikan bidang koordinat baru 


Sekarang tetapkan tiga poin dan plot mereka.


\>A=[1,0]; plotPoint(A,"A"); // definisi dan gambar tiga titik

\>B=[0,1]; plotPoint(B,"B");

\>C=[2,2]; plotPoint(C,"C");


Kemudian tiga segmen.


\>plotSegment(A,B,"c"); // c=AB

\>plotSegment(B,C,"a"); // a=BC

\>plotSegment(A,C,"b"); // b=AC

\>plotCircle(LL()); plotPoint(O(),"O"):


    Function LL not found.
    Try list ... to find functions!
    Error in:
    plotCircle(LL()); plotPoint(O(),"O"): ...
                   ^

\>function median := m(a,b,c)

\>m(2,2,1)


    
    Trying to overwrite protected function median!
    Error in:
    function median := m(a,b,c) ...
                    ^
    
    Trying to overwrite protected function median!
    Error in:
    function median := m(a,b,c) ...
                    ^
    Closing bracket ) missing!
    Try "trace errors" to inspect local variables after errors.
    m:
        useglobal; return ((sqrt(2*B^2 + 2*C-A^2)/2) 
    Error in:
    m(2,2,1) ...
            ^

## Garis Euler



Garis Euler adalah garis yang ditentukan dari sembarang segitiga yang
tidak sama sisi. Ini adalah garis tengah segitiga, dan melewati
beberapa titik penting yang ditentukan dari segitiga, termasuk
orthocenter, circumcenter, centroid, titik Exeter dan pusat lingkaran
sembilan titik segitiga.


Orthocenter: Titik perpotongan garis tinggi.


Circumcenter: Titik pusat lingkaran luar segitiga.


Centroid: Titik berat atau pusat massa segitiga.


Titik Exeter: Titik istimewa yang terletak pada sumbu Euler.


Pusat Lingkaran sembilan titik: Titik pusat lingkaran sembilan titik
yang melalui beberapa titik penting pada segitiga.


Pertama, mendefinisikan sudut-sudut segitiga yang akan digunakan dalam
menghitung garis euler. Sudut-sudut ini akan diekspresikan dalam
bentuk simbolik atau aljabar, sehingga mempermudah perhitungan lebih
lanjut yang berkaitan dengan segitiga tersebut.


\>A::=[-1,-1]; B::=[2,0]; C::=[1,2];


Untuk memplot objek geometris, kita menyiapkan area plot, dan
menambahkan titik-titiknya. Semua plot objek geometris ditambahkan ke
plot saat ini.


\>setPlotRange(3); plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C");


Kita juga bisa menambahkan sisi-sisi segitiga.


\>plotSegment(A,B,""); plotSegment(B,C,""); plotSegment(C,A,""):


![images/Presentasi_EMT_#Geometri-303.png](images/Presentasi_EMT_#Geometri-303.png)

Berikut ini adalah luas area segitiga, dengan menggunakan rumus
determinan. Tentu saja, kita harus mengambil nilai absolut dari hasil
ini.


\>$areaTriangle(A,B,C)


$$-\frac{7}{2}$$Kita dapat menghitung koefisien dari sisi c.


\>c &= lineThrough(A,B)


    
                                [- 1, 3, - 2]
    

Dan juga mendapatkan formula untuk baris ini.


\>$getLineEquation(c,x,y)


$$3\,y-x=-2$$Untuk bentuk Hesse, kita perlu menentukan sebuah titik, sehingga titik
tersebut berada di sisi positif dari bentuk Hesse. Memasukkan titik
tersebut akan menghasilkan jarak positif ke garis.


\>$getHesseForm(c,x,y,C), $at(%,[x=C[1],y=C[2]])


$$\frac{3\,y-x+2}{\sqrt{10}}$$$$\frac{7}{\sqrt{10}}$$Sekarang kita menghitung keliling ABC.  


\>LL &= circleThrough(A,B,C); $getCircleEquation(LL,x,y)


$$\left(y-\frac{5}{14}\right)^2+\left(x-\frac{3}{14}\right)^2=\frac{
 325}{98}$$\>O &= getCircleCenter(LL); $O


$$\left[ \frac{3}{14} , \frac{5}{14} \right] $$Plot lingkaran dan pusatnya. Cu dan U adalah simbolik. Kami
mengevaluasi ekspresi ini untuk Euler


\>plotCircle(LL()); plotPoint(O(),"O"):


![images/Presentasi_EMT_#Geometri-310.png](images/Presentasi_EMT_#Geometri-310.png)

Kita dapat menghitung perpotongan ketinggian di ABC (pusat
ortosentrum) secara numerik dengan rumus berikut ini.


\>H &= lineIntersection(perpendicular(A,lineThrough(C,B)),...  
\>     perpendicular(B,lineThrough(A,C))); $H


$$\left[ \frac{11}{7} , \frac{2}{7} \right] $$Sekarang kita dapat menghitung garis Euler dari segitiga tersebut.


\>el &= lineThrough(H,O); $getLineEquation(el,x,y)


$$-\frac{19\,y}{14}-\frac{x}{14}=-\frac{1}{2}$$Tambahkan ke plot kita.


\>plotPoint(H(),"H"); plotLine(el(),"Garis Euler"):


![images/Presentasi_EMT_#Geometri-313.png](images/Presentasi_EMT_#Geometri-313.png)

Pusat gravitasi harus berada pada garis ini.


\>M &= (A+B+C)/3; $getLineEquation(el,x,y) with [x=M[1],y=M[2]]


$$-\frac{1}{2}=-\frac{1}{2}$$\>plotPoint(M(),"M"): // titik berat


![images/Presentasi_EMT_#Geometri-315.png](images/Presentasi_EMT_#Geometri-315.png)

Teori mengatakan bahwa MH = 2*MO. Kita perlu menyederhanakan dengan
radcan untuk mencapai hal ini.


\>$distance(M,H)/distance(M,O)|radcan


$$2$$Fungsi-fungsi ini juga mencakup fungsi untuk sudut.


\>$computeAngle(A,C,B), degprint(%())


$$\arccos \left(\frac{4}{\sqrt{5}\,\sqrt{13}}\right)$$    60°15'18.43''

Persamaan untuk bagian tengah lingkaran tidak terlalu bagus.


\>Q &= lineIntersection(angleBisector(A,C,B),angleBisector(C,B,A))|radcan; $Q


$$\left[ \frac{\left(2^{\frac{3}{2}}+1\right)\,\sqrt{5}\,\sqrt{13}-15
 \,\sqrt{2}+3}{14} , \frac{\left(\sqrt{2}-3\right)\,\sqrt{5}\,\sqrt{
 13}+5\,2^{\frac{3}{2}}+5}{14} \right] $$Mari kita hitung juga ekspresi untuk jari-jari lingkaran yang
tertulis.


\>r &= distance(Q,projectToLine(Q,lineThrough(A,B)))|ratsimp; $r


$$\frac{\sqrt{\left(-41\,\sqrt{2}-31\right)\,\sqrt{5}\,\sqrt{13}+115
 \,\sqrt{2}+614}}{7\,\sqrt{2}}$$\>LD &=  circleWithCenter(Q,r); // Lingkaran dalam


Mari kita tambahkan ini ke dalam plot.


\>color(5); plotCircle(LD()):


![images/Presentasi_EMT_#Geometri-320.png](images/Presentasi_EMT_#Geometri-320.png)

## Sub Materi 6

## Titik Pusat



1. Titik Pusat Lingkaran Dalam (Incenter)


Titik pusat lingkaran dalam adalah titik perpotongan dari tiga garis
bagi sudut dalam segitiga. Rumus untuk mencari koordinat incenter (I)
dari segitiga dengan titik-titik sudut A(x1, y1), B(x2, y2),
C(x3,y3)adalah:


$$x_I = \frac{a \cdot x_1 + b \cdot x_2 + c \cdot x_3}{a + b + c}$$$$y_I = \frac{a \cdot y_1 + b \cdot y_2 + c \cdot y_3}{a + b + c}$$$$a = \sqrt{(x_2 - x_3)^2 + (y_2 - y_3)^2}$$$$b = \sqrt{(x_1 - x_3)^2 + (y_1 - y_3)^2}$$$$c = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$$\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-0.5,2.5,-0.5,2.5); // mendefinisikan bidang koordinat baru 


Sekarang tetapkan tiga poin dan plot mereka.


\>A=[1,0]; plotPoint(A,"A"); // definisi dan gambar tiga titik

\>B=[0,1]; plotPoint(B,"B");

\>C=[2,2]; plotPoint(C,"C");


Kemudian tiga segmen.


\>plotSegment(A,B,"c"); // c=AB

\>plotSegment(B,C,"a"); // a=BC

\>plotSegment(A,C,"b"); // b=AC


\>l=angleBisector(A,C,B); // garis bagi <ACB

\>g=angleBisector(C,A,B); // garis bagi <CAB

\>P=lineIntersection(l,g) // titik potong kedua garis bagi sudut


    [0.86038,  0.86038]

\>color(5); plotLine(l); plotLine(g); color(1); // gambar kedua garis bagi sudut

\>plotPoint(P,"P"); // gambar titik potongnya

\>r=norm(P-projectToLine(P,lineThrough(A,B))) // jari-jari lingkaran dalam


    0.509653732104

$$a = \sqrt{(0 - 2)^2 + (1 - 2)^2} = \sqrt{4 + 1} = \sqrt{5}$$$$b = \sqrt{(1 - 2)^2 + (0 - 2)^2} = \sqrt{1 + 4} = \sqrt{5}$$$$c = \sqrt{(1 - 0)^2 + (0 - 1)^2} = \sqrt{1 + 1} = \sqrt{2}$$$$x_I = \frac{a \cdot x_1 + b \cdot x_2 + c \cdot x_3}{a + b + c}$$$$y_I = \frac{a \cdot y_1 + b \cdot y_2 + c \cdot y_3}{a + b + c}$$$$x_I = \frac{\sqrt{5} \cdot 1 + \sqrt{5} \cdot 0 + \sqrt{2} \cdot 2}{\sqrt{5} + \sqrt{5} + \sqrt{2}}$$$$x_I = \frac{\sqrt{5} + 2\sqrt{2}}{2\sqrt{5} + \sqrt{2}}$$$$y_I = \frac{\sqrt{5} \cdot 0 + \sqrt{5} \cdot 1 + \sqrt{2} \cdot 2}{\sqrt{5} + \sqrt{5} + \sqrt{2}}$$$$y_I = \frac{\sqrt{5} + 2\sqrt{2}}{2\sqrt{5} + \sqrt{2}}$$4. Hasil akhir untuk koordinat incenter  P adalah:


$$\left( \frac{\sqrt{5} + 2\sqrt{2}}{2\sqrt{5} + \sqrt{2}}, \frac{\sqrt{5} + 2\sqrt{2}}{2\sqrt{5} + \sqrt{2}} \right)$$Hasil ini mendekati nilai (0.86038, 0.86038) .


\>color(5); plotLine(l); plotLine(g); color(1); // gambar kedua garis bagi sudut

\>plotPoint(P,"P"); // gambar titik potongnya       

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"): // gambar lingkaran dalam


![images/Presentasi_EMT_#Geometri-336.png](images/Presentasi_EMT_#Geometri-336.png)

2. Titik Pusat Lingkaran Luar (Circumcenter)


Titik pusat lingkaran luar adalah titik perpotongan dari tiga garis
tengah tegak lurus (garis yang tegak lurus dan melalui titik tengah
sisi-sisi segitiga). Rumus koordinat circumcenter (O) dapat dihitung
menggunakan determinan atau secara simbolik dengan EMT.


#Menentukan Titik Tengah dari Dua Sisi


Kita mulai dengan dua sisi segitiga:


Sisi B: Titik tengah M_AB dariB adalah:


$$M_{AB} = \left( \frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2} \right)$$Sisi C: Titik tengah M_BC dari C adalah:


$$M_{BC} = \left( \frac{x_2 + x_3}{2}, \frac{y_2 + y_3}{2} \right)$$#Menentukan Kemiringan Sisi dan Sumbu Tegak Lurus


Selanjutnya, kita hitung kemiringan dari


AB dan BC untuk menentukan kemiringan garis sumbu tegak lurus.


Kemiringan AB:


$$m_{AB} = \frac{y_2 - y_1}{x_2 - x_1}$$Kemiringan sumbu tegak lurus dari AB adalah negatif kebalikannya:


$$m_{\perp AB} = -\frac{1}{m_{AB}} = -\frac{x_2 - x_1}{y_2 - y_1}$$Kemiringan BC:


$$m_{BC} = \frac{y_3 - y_2}{x_3 - x_2}$$Kemiringan sumbu tegak lurus dariBC adalah:


$$m_{\perp BC} = -\frac{1}{m_{BC}} = -\frac{x_3 - x_2}{y_3 - y_2}$$#Menyusun Persamaan Garis Sumbu Tegak Lurus


Menggunakan rumus garis


$$y - y_0 = m(x - x_0)$$

kita dapatkan persamaan sumbu tegak lurus untuk sisi AB dan BC.


Persamaan Sumbu Tegak Lurus Sisi AB melalui M_AB


$$y - \frac{y_1 + y_2}{2} = -\frac{x_2 - x_1}{y_2 - y_1} \left( x - \frac{x_1 + x_2}{2} \right)$$Persamaan Sumbu Tegak Lurus Sisi C melalui M_BC:


$$y - \frac{y_2 + y_3}{2} = -\frac{x_3 - x_2}{y_3 - y_2} \left( x - \frac{x_2 + x_3}{2} \right)$$#Menemukan Titik Potong Kedua Persamaan


Titik potong dari dua garis ini memberikan koordinat circumcenter


O(x,y). Setelah menyelesaikan sistem persamaan ini, kita memperoleh:


$$x = \frac{(x_1^2 + y_1^2)(y_2 - y_3) + (x_2^2 + y_2^2)(y_3 - y_1) + (x_3^2 + y_3^2)(y_1 - y_2)}{2 \left( x_1(y_2 - y_3) + x_2(y_3 - y_1) + x_3(y_1 - y_2) \right)}$$$$y = \frac{(x_1^2 + y_1^2)(x_3 - x_2) + (x_2^2 + y_2^2)(x_1 - x_3) + (x_3^2 + y_3^2)(x_2 - x_1)}{2 \left( x_1(y_2 - y_3) + x_2(y_3 - y_1) + x_3(y_1 - y_2) \right)}$$\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Presentasi_EMT_#Geometri-348.png](images/Presentasi_EMT_#Geometri-348.png)

$$x = \frac{(1^2 + 0^2)(1 - 2) + (0^2 + 1^2)(2 - 0) + (2^2 + 2^2)(0 - 1)}{2 \left( 1(1 - 2) + 0(2 - 0) + 2(0 - 1) \right)}$$$$= \frac{(1)(-1) + (1)(2) + (8)(-1)}{2(-3)} = \frac{-1 + 2 - 8}{-6} = \frac{-7}{-6} = 1.167$$$$y = \frac{(1^2 + 0^2)(2 - 0) + (0^2 + 1^2)(1 - 2) + (2^2 + 2^2)(0 - 1)}{2 \left( 1(1 - 2) + 0(2 - 0) + 2(0 - 1) \right)}$$$$= \frac{(1)(2) + (1)(-1) + (8)(-1)}{-6} = \frac{2 - 1 - 8}{-6} = \frac{-7}{-6} = 1.167$$\>O, R


    [1.16667,  1.16667]
    1.17851130198

## Latihan lingkaran dalam

1. Tentukan ketiga titik singgung lingkaran dalam dengan sisi-sisi
segitiga ABC.


A=[-2,1]; 


B=[1,-2]; 


C=[4,4]; 


\>setPlotRange(-2.5,4.5,-2.5,4.5);

\>A=[-2,1]; plotPoint(A,"A");

\>B=[1,-2]; plotPoint(B,"B");

\>C=[4,4]; plotPoint(C,"C");


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Presentasi_EMT_#Geometri-353.png](images/Presentasi_EMT_#Geometri-353.png)

3. Tunjukkan bahwa garis bagi sudut yang ke tiga juga melalui titik
pusat lingkaran dalam.


\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [0.581139,  0.581139]

$$a = \sqrt{(4 - 6)^2 + (7 - 2)^2} = \sqrt{(-2)^2 + 5^2} = \sqrt{4 + 25} = \sqrt{29}$$$$b = \sqrt{(2 - 6)^2 + (3 - 2)^2} = \sqrt{(-4)^2 + 1^2} = \sqrt{16 + 1} = \sqrt{17}$$$$c = \sqrt{(2 - 4)^2 + (3 - 7)^2} = \sqrt{(-2)^2 + (-4)^2} = \sqrt{4 + 16} = \sqrt{20}$$$$x_I = \frac{\sqrt{29} \cdot 2 + \sqrt{17} \cdot 4 + \sqrt{20} \cdot 6}{\sqrt{29} + \sqrt{17} + \sqrt{20}}$$$$y_I = \frac{\sqrt{29} \cdot 3 + \sqrt{17} \cdot 7 + \sqrt{20} \cdot 2}{\sqrt{29} + \sqrt{17} + \sqrt{20}}$$Hasil akhir untuk koordinat incenter  P adalah:


$$(\frac{\sqrt{29} \cdot 2 + \sqrt{17} \cdot 4 + \sqrt{20} \cdot 6}{\sqrt{29} + \sqrt{17} + \sqrt{20}}, \frac{\sqrt{29} \cdot 3 + \sqrt{17} \cdot 7 + \sqrt{20} \cdot 2}{\sqrt{29} + \sqrt{17} + \sqrt{20}})$$Hasil ini mendekati nilai (0.581139, 0.583119).


\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P"); // gambar titik potongnya 


Jadi, terbukti bahwa garis bagi sudut yang ketiga juga melalui titik
pusat lingkaran dalam.


\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.52896119631

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Presentasi_EMT_#Geometri-360.png](images/Presentasi_EMT_#Geometri-360.png)

## Latian lingkaran luar



1. Tentukan titik pusat dari lingkaran luar segitiga dengan koordinat:


A=[-4,1]


B= [3,-2]


C= [1,4]


\>setPlotRange(-5,4.5,-5,4.5);

\>A=[-4,1]; plotPoint(A,"A");

\>B=[3,-2]; plotPoint(B,"B");

\>C=[1,4]; plotPoint(C,"C");    


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Presentasi_EMT_#Geometri-361.png](images/Presentasi_EMT_#Geometri-361.png)

\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [-0.00958929,  1.27082]

$$a = \sqrt{(3 - 1)^2 + (-2 - 4)^2} = \sqrt{2^2 + (-6)^2} = \sqrt{4 + 36} = \sqrt{40}$$$$b = \sqrt{(-4 - 1)^2 + (1 - 4)^2} = \sqrt{(-5)^2 + (-3)^2} = \sqrt{25 + 9} = \sqrt{34}$$$$c = \sqrt{(-4 - 3)^2 + (1 - (-2))^2} = \sqrt{(-7)^2 + 3^2} = \sqrt{49 + 9} = \sqrt{58}$$$$x_I = \frac{\sqrt{40} \cdot (-4) + \sqrt{34} \cdot 3 + \sqrt{58} \cdot 1}{\sqrt{40} + \sqrt{34} + \sqrt{58}}$$$$y_I = \frac{\sqrt{40} \cdot 1 + \sqrt{34} \cdot (-2) + \sqrt{58} \cdot 4}{\sqrt{40} + \sqrt{34} + \sqrt{58}}$$Hasil akhir untuk koordinat incenter  P adalah:


$$(\frac{\sqrt{40} \cdot (-4) + \sqrt{34} \cdot 3 + \sqrt{58} \cdot 1}{\sqrt{40} + \sqrt{34} + \sqrt{58}}, \frac{\sqrt{40} \cdot 1 + \sqrt{34} \cdot (-2) + \sqrt{58} \cdot 4}{\sqrt{40} + \sqrt{34} + \sqrt{58}}$$Hasil ini mendekati nilai (-0.0958929, 01.27082).


\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P");


\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Presentasi_EMT_#Geometri-368.png](images/Presentasi_EMT_#Geometri-368.png)

$$x = \frac{((-4)^2 + 1^2)(-2 - 4) + (3^2 + (-2)^2)(4 - 1) + (1^2 + 4^2)(1 + 2)}{2 \left( (-4)(-2 - 4) + 3(4 - 1) + 1(1 + 2) \right)}$$$$= \frac{(16 + 1)(-6) + (9 + 4)(3) + (1 + 16)(3)}{2 \cdot (24 + 9 + 3)}$$$$=\frac{17 \cdot (-6) + 13 \cdot 3 + 17 \cdot 3}{2 \cdot 36}$$$$=\frac{-102 + 39 + 51}{72}$$$$= \frac{-12}{72} = -0.167$$$$y = \frac{(16 + 1)(1 - 3) + (9 + 4)(-4 - 1) + (1 + 16)(3 + 4)}{2 \cdot 36}$$$$= \frac{17 \cdot (-2) + 13 \cdot (-5) + 17 \cdot 7}{72}$$$$= \frac{-34 - 65 + 119}{72}$$$$= \frac{20}{72} = 0.278$$\>O, R


    [-0.166667,  0.277778]
    3.90077548479

## Sub Materi 7

## Menentukan Persamaan Lingkaran Melalui Tiga Titik

Diberikan tiga titik A(1,2), B(4,6), dan C(5,2). Tentukan persamaan
lingkaran yang melalui ketiga titik tersebut.


Penyelesaian:


Persamaan umum lingkaran:


$$x^2+y^2+Dx+Ey+F=0$$Substitusi masing-masing ititk ke persamaan umum lingkaran


Titik A(1,2)


$$1^2+2^2+D.1+E.2+F=0$$$$D+2E+F=-5 ...(i)$$Titik B(4,6)


$$4^2+6^2+D.4+E.6+F=0$$$$4D+6E+F=-52 ...(ii)$$Titik C(5,2)


$$5^2+2^2+D.5+E.2+F=0$$$$5D+2E+F=-29 ...(iii)$$Eliminasi (i) dan (ii)


$$(4D+6E+F)-(D+2E+F)=-52+5$$$$3D+4E=-47...(iv)$$Eliminasi (i) dan (iii)


$$(5D+2E+F)-(D+2E+F)=-29+5$$$$4D=-24$$$$D=-6$$Substitusi D=-6  ke persamaan (iv)


$$3(-6)+4E=-47$$$$-18+4E=-47$$$$4E=-29$$$$E=-\frac{29}{4}$$Substitusikan D dan E ke persamaan (i)


$$-6+2(-\frac{29}{4})+F=-5$$$$-6-\frac{29}{2}+F=-5$$$$F=-5+6+\frac{29}{2}$$$$\frac{29}{2}+1=\frac{31}{2}$$Substitusikan nilai D, E, F ke persamaan umum lingkaran


$$x^2+y^2-6x-\frac{29}{4}y+\frac{31}{2}=0$$

atau


$$4x^2+4y^2-24x-29y+62=0$$Jadi persamaan lingkaran yang melalui A(1,2), B(4,6), dan C(5,2)
adalah


$$4x^2+4y^2-24x-29y+62=0$$\>load geometry


    Numerical and symbolic geometry.

\>A::=[1,2]; B::=[4,6]; C::=[5,2];

\>LL &= circleThrough(A,B,C);

\>O &= getCircleCenter(LL); $O


$$\left[ 3 , \frac{29}{8} \right] $$\>setPlotRange(-0.5,7,-0.5,7); plotCircle(LL()); plotPoint(O(),"O"):


![images/Presentasi_EMT_#Geometri-402.png](images/Presentasi_EMT_#Geometri-402.png)

# Sub Materi 8

## Jari-jari lingkaran

 Jari-jari lingkaran adalah jarak terpendek antara titik pusat  

lingkaran dengan titik manapun pada lingkaran itu sendiri. Jari-jari
seringkali disimbolkan dengan huruf r.


## Lingkaran dalam segitiga



Misalkan sebuah segitiga memiliki panjang sisi a, b, dan c. Luas
segitiga juga dapat dihitung sebagai hasil kali dari inradius dan
semi-perimeter. Ini berasal dari fakta bahwa luas segitiga dapat
dinyatakan sebagai jumlah dari tiga segitiga kecil yang masing-masing
terbentuk oleh radius lingkaran dalam dan satu sisi segitiga.


Semi-perimeter dari segitiga adalah:


$$s = \frac{a + b + c}{2}$$Jika kita bagi segitiga menjadi tiga segitiga kecil yang masing-masing
terbentuk oleh inradius r dan masing-masing sisi, maka luas segitiga
total A adalah penjumlahan dari luas ketiga segitiga kecil tersebut:


Luas segitiga dengan sisi a dan tinggi r:


$$ a = \frac{1}{2} \cdot a \cdot r$$Luas segitiga dengan sisi dan tinggi r:


$$b = \frac{1}{2} \cdot b \cdot r$$Luas segitiga dengan sisi dan tinggi r:


$$c = \frac{1}{2} \cdot c \cdot r$$Maka diperoleh A


$$A = \text{Luas}_a + \text{Luas}_b + \text{Luas}_c$$$$A = \frac{1}{2} \cdot a \cdot r + \frac{1}{2} \cdot b \cdot r + \frac{1}{2} \cdot c \cdot r$$$$A = \frac{1}{2} \cdot (a + b + c) \cdot r$$Sehingga r adalah


$$r = \frac{\sqrt{s(s-a)(s-b)(s-c)}\quad }{s}$$## Lingkaran luar segitiga



Hubungan Sisi dan Sudut dalam Lingkaran Luar


alam lingkaran luar, ada hubungan antara panjang sisi segitiga, sudut
berhadapan, dan circumradius. Berdasarkan aturan sinus, kita memiliki:


$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2r$$Dari hubungan ini, kita bisa menyusun ulang untuk mendapatkan
circumradius r dalam bentuk:


$$r = \frac{a}{2 \sin A} = \frac{b}{2 \sin B} = \frac{c}{2 \sin C}$$Luas Segitiga dengan Inradius dan Circumradius


Luas segitiga juga dapat dihitung menggunakan circumradius dan
sisi-sisi segitiga. Ada rumus trigonometri untuk luas segitiga:


$$A = \frac{1}{2} \cdot a \cdot b \cdot \sin C$$Dengan menggunakan aturan sinus


$$sin C = \frac{c}{2R}$$

kita substitusikan nilai didalam rumus luas segitiga:


$$A = \frac{a \cdot b \cdot c}{4r}$$Dari sini, kita bisa menyusun ulang untuk mendapatkan:


$$R = \frac{abc}{4 \sqrt{s(s-a)(s-b)(s-c)}}$$\>setPlotRange(-5,4.5,-5,4.5);

\>A=[-4,1]; plotPoint(A,"A");

\>B=[4,-2]; plotPoint(B,"B");

\>C=[4,2]; plotPoint(C,"C");


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Presentasi_EMT_#Geometri-417.png](images/Presentasi_EMT_#Geometri-417.png)

3. Tunjukkan bahwa garis bagi sudut yang ke tiga juga melalui titik
pusat lingkaran dalam.


\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [2.44707,  0.240873]

$$a = \sqrt{(1 - 3)^2 + (4 - (-2))^2} = \sqrt{(-2)^2 + (6)^2} = \sqrt{4 + 36} = \sqrt{40}$$$$b = \sqrt{(1 - (-4))^2 + (4 - 1)^2} = \sqrt{(5)^2 + (3)^2} = \sqrt{25 + 9} = \sqrt{34}$$$$c = \sqrt{(3 - (-4))^2 + (-2 - 1)^2} = \sqrt{(7)^2 + (-3)^2} = \sqrt{49 + 9} = \sqrt{58}$$$$x_I = \frac{a \cdot x_A + b \cdot x_B + c \cdot x_C}{a + b + c} = \frac{\sqrt{40} \cdot (-4) + \sqrt{34} \cdot 3 + \sqrt{58} \cdot 1}{\sqrt{40} + \sqrt{34} + \sqrt{58}}$$$$y_I = \frac{a \cdot y_A + b \cdot y_B + c \cdot y_C}{a + b + c} = \frac{\sqrt{40} \cdot 1 + \sqrt{34} \cdot (-2) + \sqrt{58} \cdot 4}{\sqrt{40} + \sqrt{34} + \sqrt{58}}$$Hasil akhir untuk koordinat incenter  P adalah:


$$(\frac{\sqrt{40} \cdot (-4) + \sqrt{34} \cdot 3 + \sqrt{58} \cdot 1}{\sqrt{40} + \sqrt{34} + \sqrt{58}},\frac{\sqrt{40} \cdot 1 + \sqrt{34} \cdot (-2) + \sqrt{58} \cdot 4}{\sqrt{40} + \sqrt{34} + \sqrt{58}})$$Hasil ini mendekati nilai (2.44707, 0.240873).


\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P"); 

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Presentasi_EMT_#Geometri-424.png](images/Presentasi_EMT_#Geometri-424.png)

Jadi, terbukti bahwa garis bagi sudut yang ketiga juga melalui titik
pusat lingkaran dalam.


\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O, R


    
                                       29
                                   [3, --]
                                       8
    
    3.90077548479

$$s = \frac{a + b + c}{2} = \frac{4 + \sqrt{65} + \sqrt{73}}{2}$$$$= \frac{4 + 8.062 + 8.544}{2} \approx \frac{20.606}{2} \approx 10.303$$$$r = \frac{abc}{4 \sqrt{s(s-a)(s-b)(s-c)}}$$$$A = \sqrt{s \cdot (s-a) \cdot (s-b) \cdot (s-c)}$$$$= \sqrt{10.303 \cdot 6.303 \cdot 2.241 \cdot 1.759}$$$$\approx \sqrt{238.1227} \approx 15.43$$$$r = \frac{abc}{4A}$$$$= \frac{4 \cdot \sqrt{65} \cdot \sqrt{73}}{4 \cdot 15.43}$$$$= \frac{\sqrt{65 \cdot 73}}{15.43}$$$$\approx \frac{68.88}{15.43}$$$$\approx 3.02$$\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Presentasi_EMT_#Geometri-436.png](images/Presentasi_EMT_#Geometri-436.png)

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>O, R


    [0.1875,  0]
    4.30524752482

## Latihan



Cari panjang jari-jari lingkaran dalam dan lingkaran luar dengan
koordinat yang diketahui adalah:


A =(-3,2)


B =(1,-1)


C = (3,1)


\>setPlotRange(-5,4.5,-5,4.5);

\>A=[-3,2]; plotPoint(A,"A");

\>B=[1,-1]; plotPoint(B,"B");

\>C=[3,1]; plotPoint(C,"C");


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Presentasi_EMT_#Geometri-437.png](images/Presentasi_EMT_#Geometri-437.png)

3. Tunjukkan bahwa garis bagi sudut yang ke tiga juga melalui titik
pusat lingkaran dalam.


\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [0.905565,  0.328807]

$$a = \sqrt{(3 - 1)^2 + (1 - (-1))^2} = \sqrt{(2)^2 + (2)^2} = \sqrt{4 + 4} = \sqrt{8}$$$$b = \sqrt{(3 - (-3))^2 + (1 - 2)^2} = \sqrt{(6)^2 + (-1)^2} = \sqrt{36 + 1} = \sqrt{37}$$$$c = \sqrt{(1 - (-3))^2 + (-1 - 2)^2} = \sqrt{(4)^2 + (-3)^2} = \sqrt{16 + 9} = \sqrt{25}$$Hasil untuk nilai P


$$x_I = \frac{\sqrt{8} \cdot (-3) + \sqrt{37} \cdot 1 + \sqrt{25} \cdot 3}{\sqrt{8} + \sqrt{37} + \sqrt{25}},y_I = \frac{\sqrt{8} \cdot 2 + \sqrt{37} \cdot (-1) + \sqrt{25} \cdot 1}{\sqrt{8} + \sqrt{37} + \sqrt{25}})$$Maka diperoleh (0.905565, 0.328807)


\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P");

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Presentasi_EMT_#Geometri-442.png](images/Presentasi_EMT_#Geometri-442.png)

Jadi, terbukti bahwa garis bagi sudut yang ketiga juga melalui titik
pusat lingkaran dalam.


4. Gambar jari-jari lingkaran dalam.


$$a = \sqrt{(x_B - x_C)^2 + (y_B - y_C)^2} = \sqrt{(1 - 3)^2 + (-1 - 1)^2} = \sqrt{(-2)^2 + (-2)^2} = \sqrt{4 + 4} = \sqrt{8} \approx 2.828$$$$b = \sqrt{(x_A - x_C)^2 + (y_A - y_C)^2} = \sqrt{(-3 - 3)^2 + (2 - 1)^2} = \sqrt{(-6)^2 + (1)^2} = \sqrt{36 + 1} = \sqrt{37} \approx 6.083$$$$c = \sqrt{(x_A - x_B)^2 + (y_A - y_B)^2} = \sqrt{(-3 - 1)^2 + (2 - (-1))^2} = \sqrt{(-4)^2 + (3)^2} = \sqrt{16 + 9} = \sqrt{25} = 5$$$$s = \frac{a + b + c}{2} = \frac{\sqrt{8} + \sqrt{37} + 5}{2}$$$$= \frac{2.828 + 6.083 + 5}{2} \approx \frac{13.911}{2} \approx 6.9555$$$$r = \frac{\sqrt{s \cdot (s - a) \cdot (s - b) \cdot (s - c)}}{s}$$$$= \frac{\sqrt{6.9555 \cdot \left(6.9555 - 2.828\right) \cdot \left(6.9555 - 6.083\right) \cdot \left(6.9555 - 5\right)}}{6.9555}$$$$= \frac{\sqrt{6.9555 \cdot 4.1275 \cdot 0.8725 \cdot 1.9555}}{6.9555}$$$$\approx \frac{\sqrt{6.9555 \cdot 4.1275 \cdot 0.8725 \cdot 1.9555}}{6.9555}$$$$\approx \frac{\sqrt{6.9555 \cdot 4.1275 \cdot 0.8725 \cdot 1.9555}}{6.9555}$$$$\approx \frac{\sqrt{48.89}}{6.9555} \approx \frac{6.998}{6.9555}$$$$\approx 1.006$$\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.00638409418

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O, R


    [0.1875,  0]
    4.30524752482

$$a = \sqrt{(x_B - x_C)^2 + (y_B - y_C)^2} = \sqrt{(1 - 3)^2 + (-1 - 1)^2}$$$$= \sqrt{(-2)^2 + (-2)^2} = \sqrt{4 + 4} = \sqrt{8} \approx 2.828$$$$b = \sqrt{(x_A - x_C)^2 + (y_A - y_C)^2} = \sqrt{(-3 - 3)^2 + (2 - 1)^2} = \sqrt{(-6)^2 + (1)^2} = \sqrt{36 + 1} = \sqrt{37} \approx 6.083$$$$c = \sqrt{(x_A - x_B)^2 + (y_A - y_B)^2} = \sqrt{(-3 - 1)^2 + (2 - (-1))^2} = \sqrt{(-4)^2 + (3)^2} = \sqrt{16 + 9} = \sqrt{25} = 5$$$$s = \frac{a + b + c}{2} = \frac{2.828 + 6.083 + 5}{2} \approx \frac{13.911}{2} \approx 6.9555$$$$A = \sqrt{s \cdot (s-a) \cdot (s-b) \cdot (s-c)}$$$$= \sqrt{6.9555 \cdot 4.1275 \cdot 0.8725 \cdot 1.9555} \approx \sqrt{48.89} \approx 6.998$$$$r = \frac{abc}{4A}$$$$= \frac{(2.828)(6.083)(5)}{4 \cdot 6.998}$$$$\approx \frac{86.186}{27.992}$$$$\approx 3.08$$\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Presentasi_EMT_#Geometri-466.png](images/Presentasi_EMT_#Geometri-466.png)

## Latihan 2



Cari panjang jari-jari lingkaran dalam dan lingkaran luar dengan
koordinat yang diketahui adalah:


A =(-2,2)


B =(1,3)


C = (3,1)


\>                                        

\>setPlotRange(-5,4.5,-5,4.5);

\>A=[-2,2]; plotPoint(A,"A");

\>B=[1,-3]; plotPoint(B,"B");

\>C=[3,1]; plotPoint(C,"C");


2. Gambar segitiga dengan titik-titik sudut ketiga titik singgung
tersebut.


\>plotSegment(A,B,"c")

\>plotSegment(B,C,"a")

\>plotSegment(A,C,"b")

\>aspect(1):


![images/Presentasi_EMT_#Geometri-467.png](images/Presentasi_EMT_#Geometri-467.png)

3. Tunjukkan bahwa garis bagi sudut yang ke tiga juga melalui titik
pusat lingkaran dalam.


\>l=angleBisector(A,C,B);

\>g=angleBisector(C,A,B);

\>P=lineIntersection(l,g)


    [0.886087,  -0.0338807]

$$a =\sqrt{(3 - 1)^2 + (1 - (-3))^2} = \sqrt{(2)^2 + (4)^2} = \sqrt{4 + 16} = \sqrt{20}$$$$b = \sqrt{(3 - (-2))^2 + (1 - 2)^2} = \sqrt{(5)^2 + (-1)^2} = \sqrt{25 + 1} = \sqrt{26}$$$$c =  \sqrt{(1 - (-2))^2 + (-3 - 2)^2} = \sqrt{(3)^2 + (-5)^2} = \sqrt{9 + 25} = \sqrt{34}$$$$x_I = \frac{\sqrt{20} \cdot (-2) + \sqrt{26} \cdot 1 + \sqrt{34} \cdot 3}{\sqrt{20} + \sqrt{26} + \sqrt{34}}$$$$y_I =\frac{\sqrt{20} \cdot 2 + \sqrt{26} \cdot (-3) + \sqrt{34} \cdot 1}{\sqrt{20} + \sqrt{26} + \sqrt{34}}$$Hasil nilai P adalah


$$(\frac{\sqrt{20} \cdot (-2) + \sqrt{26} \cdot 1 + \sqrt{34} \cdot 3}{\sqrt{20} + \sqrt{26} + \sqrt{34}},\frac{\sqrt{20} \cdot 2 + \sqrt{26} \cdot (-3) + \sqrt{34} \cdot 1}{\sqrt{20} + \sqrt{26} + \sqrt{34}})$$

Maka hasilnya (0.886087, -0.0338807)


\>color(5); plotLine(l); plotLine(g); color(1);

\>plotPoint(P,"P");

\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.42837596706

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Presentasi_EMT_#Geometri-474.png](images/Presentasi_EMT_#Geometri-474.png)

Jadi, terbukti bahwa garis bagi sudut yang ketiga juga melalui titik
pusat lingkaran dalam.


4. Gambar jari-jari lingkaran dalam.


$$a = \sqrt{(x_B - x_C)^2 + (y_B - y_C)^2} = \sqrt{(1 - 3)^2 + (-3 - 1)^2} = \sqrt{(-2)^2 + (-4)^2} = \sqrt{4 + 16} = \sqrt{20} \approx 4.472$$$$b = \sqrt{(x_A - x_C)^2 + (y_A - y_C)^2} = \sqrt{(-2 - 3)^2 + (2 - 1)^2} = \sqrt{(-5)^2 + (1)^2} = \sqrt{25 + 1} = \sqrt{26} \approx 5.099$$$$c = \sqrt{(x_A - x_B)^2 + (y_A - y_B)^2} = \sqrt{(-2 - 1)^2 + (2 - (-3))^2} = \sqrt{(-3)^2 + (5)^2} = \sqrt{9 + 25} = \sqrt{34} \approx 5.831$$$$s = \frac{a + b + c}{2} = \frac{\sqrt{20} + \sqrt{26} + \sqrt{34}}{2}$$$$= \frac{4.472 + 5.099 + 5.831}{2} \approx \frac{15.402}{2} \approx 7.701$$$$r = \frac{\sqrt{s \cdot (s - a) \cdot (s - b) \cdot (s - c)}}{s}$$$$= \frac{\sqrt{7.701 \cdot (7.701 - 4.472) \cdot (7.701 - 5.099) \cdot (7.701 - 5.831)}}{7.701}$$$$= \frac{\sqrt{7.701 \cdot 3.229 \cdot 2.602 \cdot 1.870}}{7.701}$$$$\approx \frac{\sqrt{7.701 \cdot 3.229 \cdot 2.602 \cdot 1.870}}{7.701}$$$$\approx \frac{\sqrt{(7.701)(3.229)(2.602)(1.870)}}{7.701}$$$$\approx \frac{\sqrt{121.14}}{7.701} \approx \frac{11.00}{7.701} \approx 1.43$$\>r=norm(P-projectToLine(P,lineThrough(A,B)))


    1.42837596706

\>plotCircle(circleWithCenter(P,r),"Lingkaran dalam segitiga ABC"):


![images/Presentasi_EMT_#Geometri-486.png](images/Presentasi_EMT_#Geometri-486.png)

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>O, R


    [0.0714286,  1.92857]
    3.07225902394

$$a = \sqrt{(x_B - x_C)^2 + (y_B - y_C)^2} = \sqrt{(1 - 3)^2 + (-3 - 1)^2} = \sqrt{(-2)^2 + (-4)^2} = \sqrt{4 + 16} = \sqrt{20} \approx 4.472$$$$b = \sqrt{(x_A - x_C)^2 + (y_A - y_C)^2} = \sqrt{(-2 - 3)^2 + (2 - 1)^2} = \sqrt{(-5)^2 + (1)^2} = \sqrt{25 + 1} = \sqrt{26} \approx 5.099$$$$c = \sqrt{(x_A - x_B)^2 + (y_A - y_B)^2} = \sqrt{(-2 - 1)^2 + (2 - (-3))^2} = \sqrt{(-3)^2 + (5)^2} = \sqrt{9 + 25} = \sqrt{34} \approx 5.831$$$$s = \frac{a + b + c}{2} = \frac{\sqrt{20} + \sqrt{26} + \sqrt{34}}{2}$$$$\approx \frac{4.472 + 5.099 + 5.831}{2} \approx \frac{15.402}{2} \approx 7.701$$$$A = \sqrt{s \cdot (s-a) \cdot (s-b) \cdot (s-c)}$$$$= \sqrt{7.701 \cdot (7.701 - 4.472) \cdot (7.701 - 5.099) \cdot (7.701 - 5.831)}$$$$= \sqrt{7.701 \cdot 3.229 \cdot 2.602 \cdot 1.870} \approx \sqrt{121.695} \approx 11.02$$$$r = \frac{abc}{4A} = \frac{(4.472)(5.099)(5.831)}{4 \cdot 7.071}$$$$\approx \frac{132.55}{44.08} \approx 3.07$$\>c=circleThrough(A,B,C); // lingkaran luar segitiga ABC

\>R=getCircleRadius(c); // jari2 lingkaran luar

\>O=getCircleCenter(c); // titik pusat lingkaran c

\>O, R


    [0.181818,  -0.0909091]
    3.02195820702

$$a = \sqrt{(x_2 - x_3)^2 + (y_2 - y_3)^2} = \sqrt{(1 - 3)^2 + (-3 - 1)^2} = \sqrt{(-2)^2 + (-4)^2} = \sqrt{4 + 16} = \sqrt{20} = 4.472$$$$b = \sqrt{(x_1 - x_3)^2 + (y_1 - y_3)^2} = \sqrt{(-2 - 3)^2 + (2 - 1)^2} = \sqrt{(-5)^2 + (1)^2} = \sqrt{25 + 1} = \sqrt{26} = 5.099$$$$c = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2} = \sqrt{(-2 - 1)^2 + (2 + 3)^2} = \sqrt{(-3)^2 + (5)^2} = \sqrt{9 + 25} = \sqrt{34} = 5.831$$$$s = \frac{a + b + c}{2} = \frac{4.472 + 5.099 + 5.831}{2} = \frac{15.402}{2} = 7.701$$$$A = \sqrt{7.701 \cdot (7.701 - 4.472) \cdot (7.701 - 5.099) \cdot (7.701 - 5.831)}$$$$= \sqrt{7.701 \cdot 3.229 \cdot 2.602 \cdot 1.870}$$$$= \sqrt{115.62} = 10.72$$$$r = \frac{a \cdot b \cdot c}{4 \cdot K}$$$$= \frac{4.472 \cdot 5.099 \cdot 5.831}{4 \cdot 9.826}$$$$= \frac{132.446}{42.89}$$$$\approx 3.02$$\>plotPoint(O,"O"); // gambar titik "O"

\>plotCircle(c,"Lingkaran luar segitiga ABC"):


![images/Presentasi_EMT_#Geometri-508.png](images/Presentasi_EMT_#Geometri-508.png)

# Sub Materi 9

# PARABOLA

Definisi : Tempat kedudukan titik titik P yang jaraknya ke suatu titik
tertentu dan jaraknya ke suatu garis(direktriks) tertentu dinamakan
parabola


## Persamaan Parabola

Akan diilustrasikan gambar dari kurva parabola. Misalkan titik fokus
F(p,0), titik puncak O(0,0), garis arah (direktris) yaitu garis g dan
kita pilih R (-p,y) pada garis g, kita pilih sembarang titik P(x,y)
yang ada pada parabola. Berikut ilustrasi gambar dari kurva
parabolanya


Jika P(x,y) adalah sembarang titik pada parabola, maka dari definisi
kurva parabola diperoleh hubungan


$$|PF| = |PR|$$$$\sqrt{(x-p)^2+(y-0)^2} = \sqrt{(x-(-p))^2+(y-y)^2}$$$$\sqrt{(x-p)^2+y^2} = \sqrt{(x+p+(0)^2}$$$$\sqrt{(x-p)^2+y^2} = \sqrt{(x+p)^2}$$$$(x-p)^2+y^2 = (x+p)^2$$$$x^2-2px+p^2+y^2 = x^2+2px+p^2$$$$y^2 = 2px+2p$$$$y^2 = 4px$$Persamaan parabola y^2 = 4px dengan titik puncak O (0,0) dengan titik
fokus F(p,0) akan mepresentasikan parabola terbuka ke kanan (arah
sumbu x positif).


Parabola dengan sumbu sejajar sumbu x dan puncaknya di (h,k)


$$(y-k)^2 = 4p(x-h)$$

dengan titik puncak di (h,k)


Jika kita jabarkan lagi,


$$y^2 = 4p(x-h)$$$$y^2-2ky+k^2 = 4px-4ph$$$$y^2-2ky-4px+k^2+4ph = 0$$$$Ay^2+By+Cx+D = 0$$persamaan umum dari parabola adalah


$$Ay^2+By+Cx+D = 0$$sebagai contoh :


Buatlah sebuah grafik parabola dari fungsi,


$$y=2x^2$$

dan tentukanlah titik puncaknya, apakah grafik terbuka keatas atau
kebawah?


Jawab :


$$y=2x^2$$

fungsi tersebut dapat kita dari titik puncaknya (p,0) dicari
menggunakan rumus dengan


$$x= \frac{-b}{(2a)}$$

diketahui a= 2, b=0


maka,


$$x=\frac{0}{(2(2))}$$$$x=\frac{0}{(4)}$$$$x=0$$

sehingga, titik puncak berada di (0,0)


jika kita menggambarkan grafik menggunakan EMT:


\>load geometry


    Numerical and symbolic geometry.

\>setPlotRange(-2,2,0,8);

\>plot2d("2x^2");

\>o=[0,0]; plotPoint(o;"o")


Dari gambar tersebut terbentuk grafik parabola terbuka keatas dengan
titik puncak berada di (0,0)


## Parabola melalui 3 titik

Dengan cara perhitungan yang mirip dengan cara di atas, maka kita akan
dapat menentukan representasi dari tiga persamaan parabola lainnya
yang menghadap ke arah yang berbeda.


Misalnya diketahui bahwa sebuah persamaan parabola melalui 3 titik
yaitu titik (-2,1),(1,4),(1,-2)dan searah dengan sumbu X! maka kita
dapat hitung:


- Persamaan parabola melaui tiga titik dan searah sumbu X adalah
y^2+Ay+Bx+C=0, persamaan parabola melaui tiga titik dan searah sumbu Y
adalah x^2+Ax+By+C=0.


- Karena pada kurva ini searah dengan sumbu X maka Pada soal ini
parabola searah sumbu X sehingga yang kita gunakan adalah
y^2+Ay+Bx+C=0.


- Substitusi ketiga titik yang dilalui oleh kurva parabola:


kita substitusi titik (1,4) kedalam persamaan sehingga diperoleh
16+4A+B+C=0, menjadi (persamaan 1)


lalu kita substitusi (1,-2) kedalam persamaan 4-2A+B+C=0, menjadi
(persamaan 2)


Selanjutnya kita subtitusi titik terakhir yaitu titik (-2,1)?kedalam
persamaan sehingga didapat 1+A-2B+C=0 menjadi (persamaan 3)


- Langkah selanjutnya kita eliminasi persamaan (1 dan 2), sehingga
didapat


$$16+4*A+B+C=0$$$$4-2*A+B+C=0/12+6*A=0$$

-Maka akan kita peroleh A=-2.


-Substitusikan A=-2 ke persamaan 1 sehingga didapat 16+(-8)+B+C=0,
lalu kita peroleh B+C=-8, kita jadikan ini (persamaan 4)


-Substitusikan A=-2 ke persamaan 2 sehingga didapat 1+(-2)-2B+C=0,
lalu kita peroleh 2B+C=1, kita jadikan ini (persamaan 5)


- Lalu jika kita eliminasi (persamaan 4 dan 5) melalui perhitungan
manual kita peroleh 3B=-9. Dan didapat B=-3


- Substitusikan B=-3 kedalam kedalam (persamaan 4)sehingga menjadi
-3+C=-5. Dan akan didapat C=-5.


- Kita akhirnya memperoleh nilai A= -2, B=-3 lalu C=-5. Kita
substitusikan kedalam persamaan parabola sehingga didapat
y^2-2y-3x-5=0. Kita ubah persamaan parabolanya sehingga menjadi


$$y^2-2y-3x-5=0$$Parabola dengan sumbu sejajar sumbu x dan puncaknya di (h,k)


$$(y-k)^2 = 4p(x-h)$$

dengan titik puncak di (h,k)


Jika kita jabarkan lagi,


$$y^2 = 4p(x-h)$$$$y^2-2ky+k^2 = 4px-4ph$$$$y^2-2ky-4px+k^2+4ph = 0$$$$Ay^2+By+Cx+D = 0$$persamaan umum dari parabola adalah


$$Ay^2+By+Cx+D = 0$$## Persamaan parabola jika diketahui titik dan arahnya



Dengan membuat perhitungan yang mirip dengan cara diatas, maka kita
akan dapat menentukan representasi dari tiga persamaan parabola
lainnya yang menghadap kesuatu arah.


-Misalnya diketahui bahwa sebuah persamaan parabola yang melalui 3
titik yaitu titik (-2,1),(1,4),(1,-2) yang searah dengan sumbu x! maka
dapat kita hitung:


-Persamaan parabola melalui 3 titik dan searah dengan sumbu x adalah


$$y^2+Ay+Bx+C=0$$

-Persamaan parabola yang melalui 3 titik dan searah dengan sumbu y
adalah


$$x^2+Ax+By+C=0.$$

-Karena pada kurva ini searah pada sumbu x maka persamaan lyang kita
gunakan adalah


$$y^2+Ay+Bx+C=0$$

-Substitusi ketiga titik yang dilalui oleh kurva parabola.


-Pertama, kita substitusikan titik (1,4) kedalam persamaan sehingga
diperoleh 16+4A+Bx+C, menjadi (persamaan 1)


-Selanjutkan kita substitusikan titik (1,-2) kedalam persamaan
sehingga diperoleh 4-2A+B+C=0, menjadi (persamaan 2)


-Lalu terakhir kita substitusikan (-2,1) kedalam persamaan sehingga
diperoleh 1+A-2B+C=0, menjadi (persamaan 3)


-Langkah selanjutnya kita eliminasi (persamaan 1 dan 2), sehingga
didapat


$$12+6A=0$$$$6A=-12$$$$A=-2$$

-Substitusikan A=-2 kedalam (persamaan 1) sehingga didapat


$$16+(4)(-2)+B+C=0$$$$16-8+B+C=0$$$$B+C=-8$$

B+C=-8, menjadi (persamaan 4)


-Substitusi A=-2 kedalam (persamaan 2) sehingga didapat


$$1-2-2B+C=0$$$$2B+C=1$$## Contoh Soal

1. Tentukanlan persamaan dari parabola yang melalui 3 titik A (-1,-1),
B (2,0), C(1,2) dan gambarkan parabolanya.


2B+C=1, menjadi (persamaan 5)


-Eliminasikan (persamaan 4 dan 5) melalui perhitungan manual kita
peroleh 3B=-9, lalun didapat B=-3


-Substitusikan B=-3 kedalam (persamaan 4) sehingga menjadi


$$-3+C=-5$$$$C=-5$$

-Darisini kita peroleh


$$A=-2$$$$B=-3$$$$C=-5.$$

-Kita substitusikan kedalam persamaan parabola sehingga menjadi


$$y^2-2y-3x-5=0$$$$y^2-2y=3x+5$$$$(y-1)^2-1=3x+5$$$$(y-1)^2=3x+6$$$$(y-1)^2=3(x+2)$$

-Jadi diperoleh persamaan parabolanya


$$(y-1)^2=3(x+2)$$Selanjutnya kita coba menggambar parabola yang diketahui tiga titik
menggunakan latex


\>load geometry 


    Numerical and symbolic geometry.

\>A &=[-1,-1]; B &=[2,0]; C &=[1,2];

\>c &=(lineThrough(A,B)); $c //  melalui garis A dan B


$$\left[ -1 , 3 , -2 \right] $$\>$ getLineEquation(c,x,y); $solve(%,y)  // Persamaan garis c,x,y


$$\left[ y=\frac{x-2}{3} \right] $$Rumus umum persamaan garis


$$ax+by+c=0$$Mancari gradien garis


$$m = \frac{y_2-y_1}{x_2-x_1}$$$$m = \frac{0-(-1)}{2-(-1)}$$$$m = \frac{1}{3}$$Persamaan Garis (Bentuk Slope-Intercept)


$$y = mx + b$$

Gunakan titik A untuk mencari b:


$$y = \frac{1}{3} x + b$$

Substitusi A(-1,-1):


$$-1 = \frac{1}{3}(-1) + b$$$$-1 = -\frac{1}{3} + b$$$$b = -1 + \frac{1}{3}(-1)$$$$b = -\frac{2}{3}$$

Jadi,persamaan garis dalam bentuk slope-intercept adalah:


$$y = \frac{1}{3}x - \frac{2}{3}$$Selanjutnya akan dicari persamaan tempat kedudukan titik-titik yang
berjarak sama ke titik C dan ke garis AB.


\>p &=getHesseForm(lineThrough(A,B),x,y,C)-distance([x,y],C); $p='0


$$\frac{3\,y-x+2}{\sqrt{10}}-\sqrt{\left(2-y\right)^2+\left(1-x
 \right)^2}=0$$\>akar &= solve(getHesseForm(lineThrough(A,B),x,y,C)^2-distance([x,y],C)^2,y)


    
            [y = - 3 x - sqrt(70) sqrt(9 - 2 x) + 26, 
                                  y = - 3 x + sqrt(70) sqrt(9 - 2 x) + 26]
    

\>A=[-1,-1]; B=[2,0]; C=[1,2];

\>setPlotRange (-3,4,-3,4); plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C"):


![images/Presentasi_EMT_#Geometri-574.png](images/Presentasi_EMT_#Geometri-574.png)

\>plotLine(lineThrough(A,B)):


![images/Presentasi_EMT_#Geometri-575.png](images/Presentasi_EMT_#Geometri-575.png)

\>plot2d(p,level=0,add=1,contourcolor=11):


![images/Presentasi_EMT_#Geometri-576.png](images/Presentasi_EMT_#Geometri-576.png)

\> load geometry


    Numerical and symbolic geometry.

\>A &=[3,2]; B &=[2,1]; C &=[2,2];

\>r&=(lineThrough(A,B)); $r


$$\left[ 1 , -1 , 1 \right] $$\>$getLineEquation(r,x,y); $solve(%,y)


$$\left[ y=x-1 \right] $$\>p &=getHesseForm(lineThrough(A,B),x,y,C)-distance([x,y],C); $p='0


$$\frac{y-x+1}{\sqrt{2}}-\sqrt{\left(2-y\right)^2+\left(2-x\right)^2}=
 0$$\>akar &= solve(getHesseForm(lineThrough(A,B),x,y,C)^2-distance([x,y],C)^2,y


    Closing bracket missing.
    Found: solve(getHesseForm(lineThrough(A,B),x,y,C)^2-distance([x,y],C)^2,y
    Brackets: 1 (, 0 [
    Error in:
    ... m(lineThrough(A,B),x,y,C)^2-distance([x,y],C)^2,y ...
                                                         ^

\>A=[3,2]; B=[2,1]; C=[2,2]; 

\>setPlotRange (6); plotPoint(A,"A"); plotPoint(B,"B"); plotPoint(C,"C");

\>plotLine(lineThrough(A,B));

\>plot2d(p,level=0,add=1,contourcolor=2):


![images/Presentasi_EMT_#Geometri-580.png](images/Presentasi_EMT_#Geometri-580.png)

# Sub Materi 10

# Menentukan Persamaan Elips * Jika Diketahui Titik Fokus

## Elips Secara Umum

Definisi


Elips merupakan himpunan semua titik pada bidang XY yang jaraknya dari
dua titik tetap (yang disebut fokus) jika dijumlahkan akan
menghasilkan suatu nilai konstan.


Dalam geometri, elips adalah bentuk dua dimensi yang didefinisikan
sepanjang sumbunya. Elips memiliki dua titik fokus. Jumlah kedua jarak
ke titik fokus, untuk semua titik dalam kurva, selalu konstan.


Lingkaran juga merupakan elips, yang fokusnya berada di titik yang
sama, yaitu pusat lingkaran.


image: elips2.JPEG


Menggunakan rumus jarak, jarak dapat dituliskan sebagai:


$$\sqrt{(x+c)^2 + y^2} + \sqrt{(x-c)^2 + y^2} = 2a$$Dengan mengkuadratkan dan menyederhanakan kedua sisi, kita peroleh:


$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \quad \text{(definisi elips)}$$Sekarang, karena titik P terletak pada elips, maka ia harus memenuhi
persamaan (2) sehingga 0 &lt; c &lt; a:


$$y^2 = b^2 \left(1 - \frac{x^2}{a^2}\right)$$Dengan demikian,


$$PF_1 = \sqrt{(x+c)^2 + y^2}$$$$= \sqrt{(x+c)^2 + b^2 \left(1 - \frac{x^2}{a^2}\right)}$$Dengan menyederhanakan, diperoleh


$$PF_1 = a + \frac{(\frac {c} {a}) x}{a}$$Demikian pula,


$$PF_2 = a - \frac{(\frac {c} {a}) x}{a}$$Karena itu,


$$PF_1 + PF_2 = 2a$$Jadi, persamaan elips dengan pusat di asal dan sumbu mayor sepanjang
sumbu-x adalah:


$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$dengan


$$-a \leq x \leq a.$$Demikian pula, persamaan elips dengan pusat di asal dan sumbu mayor
sepanjang sumbu-y adalah:


$$\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1$$dengan


$$-b \leq y \leq b.$$Jika pusat elips di titik C(h,k) persamaan umumnya akan menjadi


Jika sumbu mayor sepanjang sumbu-x


$$\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1$$Jika sumbu mayor sepanjang sumbu-y


$$\frac{(x - h)^2}{b^2} + \frac{(y - k)^2}{a^2} = 1$$image: segitiga.JPEG


Jumlah jarak titik B dari F1 adalah


$$F_1 B + F_2 B = F_1 O + OB + F_2 B \quad (\text{dari gambar di atas})$$$$\Rightarrow c + a + a - c = 2a$$Jumlah jarak titik C ke F_1 adalah F_1 C + F_2 C


$$\Rightarrow F_1 C + F_2 C = \sqrt{b^2 + c^2} + \sqrt{b^2 + c^2} = 2\sqrt{b^2 + c^2}$$Menurut definisi elips;


$$2\sqrt{b^2 + c^2} = 2a$$$$\Rightarrow a = \sqrt{b^2 + c^2}$$$$\Rightarrow a^2 = b^2 + c^2$$$$\Rightarrow c^2 = a^2 - b^2$$\>load geometry


    Numerical and symbolic geometry.

\>a := 5; // panjang sumbu semi mayor

\>d := 4; // asumsikan d adalah jarak kedua fokus

\>c := d/2 // jarak pusat dengan salah satu fokus


    2

\>b := sqrt (a^2-c^2) // panjang sumbu smei minor


    4.58257569496

\>a2 := a^2


    25

\>b2 := b^2


    21

Persamaan elips adalah


$$\frac {x^2} {a^2} + \frac {y^2} {b^2} = 1$$sehingga


\>$&expand(x^2/25+y^2/21 = 1)


$$\frac{y^2}{21}+\frac{x^2}{25}=1$$\>t := linspace(0,2pi,100);

\>x := a\*cos(t);

\>y := b\*sin(t);

\>setPlotRange(5); 

\>C := [0,0]; F1 := [-2,0]; F2 := [2,0]; // F1 & F2 adalah nilai (plus minus c,0)

\>aspect(1.1); plot2d(x, y); plotPoint(C); plotPoint(F1); plotPoint(F2):


![images/Presentasi_EMT_#Geometri-604.png](images/Presentasi_EMT_#Geometri-604.png)

Bagaimana jika pusat elips tidak di titik asal (0,0)???


Let's get started!


Misalnya diberikan elips dengan pusat C(-4,5), salah satu titik
fokusnya berada di F1(-1,5) dengan panjang sumbu mayor adalah 12.
Tentukan F2, dan persamaan elips tersebut serta tunjukkan plotnya.


Hint: sumbu mayor sejajar sumbu x


\>a := 6; // panjang sumbu semi mayor

\>C := [-4,5]; F1 &= [-1,5];

\>c := $distance(C,F1) // jarak pusat ke salah satu fokus


$$3\,\sqrt{2}$$\>c := 3;

\>b := sqrt (a^2-c^2) // panjang sumbu semi minor


    5.19615242271

\>"persamaan elips: ((x-h)^2/a^2)+((y-k)^2^2/b^2)=1";

\>a2 := a^2


    36

\>b2 := b^2


    27

\>persamaan := "persamaan elips adalah (x+4)^2/a2+(y-5)^2/b2 = 1"


    persamaan elips adalah (x+4)^2/a2+(y-5)^2/b2 = 1

\>expr &= ((x+4)^2/a2+(y-5)^2/b2 = 1)


    
                                  2          2
                           (y - 5)    (x + 4)
                           -------- + -------- = 1
                              b2         a2
    

\>F1 &= [-4+c,5];

\>F2 &= [-4-c,5];

\>F1, F2


    
                             [[- 5, - 1, - 6], 5]
    
    
                             [[- 3, - 7, - 2], 5]
    

\>t = linspace(0, 2\*pi, 100);

\>x = -4+a\*cos(t);

\>y = 5+b\*sin(t);

\>setPlotRange(10);

\>C := [-4,5]; F1 := [-1,5]; F2 := [-7,5];

\>aspect(1.1); plot2d(x,y); plotPoint(C); plotPoint(F1); plotPoint(F2):


![images/Presentasi_EMT_#Geometri-606.png](images/Presentasi_EMT_#Geometri-606.png)

# LATIHAN SOAL

1. Diketahui titik fokus elips berada di F1(3,0) dan F2(-3,0). Jika
panjang sumbu mayor adalah 10, buatlah persamaan elips tersebut.
Apakah elips ini dapat dilukis dalam satu kuadran? Jelaskan alasamnu!


\>a := 5; C := [0,0]


    [0,  0]

\>F1 := [3,0];

\>F2 := [-3,0];

\>d &= 2\*c;

\>d := $distance(F1,F2)


$$\left[ 2 , 6 , 4 \right] $$\>c := 6/2


    3

\>b := sqrt(a^2-c^2)


    4

\>t := linspace(0,2pi,100);

\>x := a\*cos(t);

\>y := b\*sin(t);

\>setPlotRange(10);

\>aspect(1.2); plot2d(x, y); plotPoint(F1); plotPoint(F2); plotPoint(C):


![images/Presentasi_EMT_#Geometri-608.png](images/Presentasi_EMT_#Geometri-608.png)

Persamaan elipsnya menjadi


$$\frac{x^2}{25} + \frac{y^2}{16} = 1$$Elips ini tidak dapat dilukis dalam satu kuadran. Karena elips ini
simetris terhadap sumbu-x dan sumbu-y, bagian dari elips akan berada
di kuadran I, II, III, dan IV. Dengan pusat di titik (0,0), elips ini
akan memiliki bagian di seluruh kuadran, tidak terbatas hanya pada
satu kuadran.


Simplenya lihat saja 2 titik fokusnya sudah berada di kuadran yang
berbeda.


Penyelesaian


a. Identifikasi Parameter:


   - Fokus F1(3, 0) dan F2(-3, 0) menunjukkan bahwa fokus terletak
pada sumbu x.


   - Panjang sumbu mayor 2a = 10, sehingga a = 5.


   - Jarak dari pusat ke fokus (c) dapat dihitung:


jarak dari pusat ke fokus = 3


   - Pusat elips adalah titik tengah antara F1 dan F2, yaitu C(0, 0).  

$$2a = 10$$$$a = 5$$$$c = 3$$$$C : (0, 0)$$b. Hitung Panjang Sumbu Minor (b):


   - Gunakan hubungan


$$c^2 = a^2 - b^2$$$$c^2 = 3^2 = 9$$   - Dari hubungan  

$$c^2 = a^2 - b^2$$$$9 = 5^2 - b^2$$$$9 = 25 - b^2$$$$b^2 = 25 - 9$$$$b^2 = 16$$$$b = 4$$c. Tentukan Persamaan Elips


   - Persamaan elips dengan pusat di C(0, 0) dan sumbu horizontal
adalah:


$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$Menjadi:


$$\frac{x^2}{5^2} + \frac{y^2}{4^2} = 1$$Sehingga persamaan elips adalah:


$$\frac{x^2}{25} + \frac{y^2}{16} = 1$$d. Apakah Elips Ini Dapat Dilukis dalam Satu Kuadran?


   - Elips ini tidak dapat dilukis dalam satu kuadran. Karena elips
ini simetris terhadap sumbu x dan sumbu y, bagian dari elips akan
berada di kuadran I, II, III, dan IV.


   - Alasan: Dengan pusat di titik (0, 0, elips ini akan memiliki
bagian di seluruh kuadran, tidak terbatas hanya pada satu kuadran.


2. Diketahui elips memiliki fokus di P1(3,6) dan P2(3,-2) dengan pusat
elips berada di titik C(3,2). Panjang sumbu mayor adalah 12. Tentukan
persamaan elips tersebut! Apakah elips tersebut simetris terhadap
sumbu-y? Jelaskan!


\>P1 := [3,6];

\>P2 := [3,-2];

\>C := [3,2];

\>a := 6;

\>d &= 2\*c;

\>c := 6-2


    4

\>b := sqrt(a^2-c^2)


    4.472135955

\>t := linspace(0,2pi,100);

\>x := 3+ a\*cos(t);

\>y := 2+ b\*sin(t);

\>setPlotRange(-10,10);

\>aspect(0.8); plot2d(x, y); plotPoint(P1); plotPoint(P2); plotPoint(C):


![images/Presentasi_EMT_#Geometri-625.png](images/Presentasi_EMT_#Geometri-625.png)

Persamaan elips menjadi


$$\frac{(x - 3)^2}{20} + \frac{(y - 2)^2}{36} = 1$$a. Tentukan Nilai a:


   Panjang sumbu mayor adalah 12, sehingga 2a = 12. Maka:


$$a = \frac{12}{2} = 6$$b. Tentukan Jarak Fokus dan Nilai c:


   Fokus elips berada di F1(3, 6) dan F2(3, -2).


   Jarak antara pusat C(3, 2) dan fokus F1(3, 6) adalah c:


$$c = |6 - 2| = 4$$c. Hitung Nilai b:


   Gunakan hubungan


$$c^2 = a^2 - b^2$$$$4^2 = 6^2 - b^2$$$$16 = 36 - b^2$$$$b^2 = 36 - 16 = 20$$$$b = \sqrt{20} = 2\sqrt{5}$$d. Tentukan Persamaan Elips:


   Karena sumbu mayor elips berada di sepanjang sumbu y, bentuk umum
persamaan elips dengan pusat di (h, k) = (3, 2) adalah:


$$\frac{(x - h)^2}{b^2} + \frac{(y - k)^2}{a^2} = 1$$   Masukkan nilai:  

$$h = 3, k = 2, a = 6, dan b = 2\sqrt{5}$$$$\frac{(x - 3)^2}{(2\sqrt{5})^2} + \frac{(y - 2)^2}{6^2} = 1$$   Sederhanakan:  

$$\frac{(x - 3)^2}{20} + \frac{(y - 2)^2}{36} = 1$$Elips tersebut akan simetris terhadap sumbu-y, mengingat sumbu
mayornya berada di sumbu-y dengan pusat di C(3,2). Artinya pusat elips
bergeser dari titik asal ke titik C tanpa mengubah bentuk elipsnya.
Fakta tersebut sejalan dengan sifat simetri elips, elips yang
berbentuk persamaan standard akan simetris terhadap sumbu-y jika
pusatnya di (h,k) dan sumbu mayornya sejajar dengan sumbu-y yang
kemudian setiap titik (x,y) pada elips akan memiliki pasangan simetris
(-x+2h,y) yang juga berada pada elips. Dalam kasus tersebut setiap
titik (x,y) dalam elips akan kan memiliki pasangan simetris (-x+6,y)
yang juga berada pada elips tersebut.


3. Gambarlah suatu elips jika diketahui kedua titik fokusnya, misalnya
P dan Q. Ingat elips dengan fokus P dan Q adalah tempat kedudukan
titik-titik yang jumlah jarak ke P dan ke Q selalu sama (konstan).


Penyelesaian:


Diketahui kedua titik fokus P = [-1,-1] dan Q = [1,-1]


\>P := [-1,-1]; Q := [1,-1];

\>c := 1; // |-1-1|/2 = 1 diperoleh dari jarak PQ/2


karena jarak pusat ke fokus adalah 1, maka pusatya adalah di titik
asal C(0,-1)


\>C := [0,-1];

\>a := 8; b := 2; // dimisalkan

\>t := linspace(0,2pi,100);

\>x := a\*cos(t);

\>y := -1+b\*sin(t);

\>setPlotRange(10);

\>aspect(1.2); plot2d(x, y); plotPoint(P); plotPoint(Q); plotPoint(C):     


    Syntax error in expression, or unfinished expression!
    Error in:
    ... ); plotPoint(P); plotPoint(Q); plotPoint(C):      ...
                                                         ^

# Sub Materi 11

## Perhitungan geometris: jarak dua titik (panjang ruas garis),

## luas dan keliling segitiga, luas dan keliling lingkaran

## 1. Jarak Dua Titik (Panjang Ruang Garis) Jarak antara dua titik

adalah panjang garis lurus yang menghubungkan kedua titik tersebut
dalam bidang atau ruang tiga dimensi.


Misal terdapat dua titik


$$A(x_1,y_1)$$$$B(x_2,y_2)$$Rumus untuk menghitung jarak antara dua titik adalah:


$$|d| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$Rumus ini didapatkan dari teorema Pythagoras, di mana jarak tersebut
membentuk hipotenusa dari segitiga siku-siku dengan panjang sisi
horizontal


$$|x_2 - x_1|$$

dan sisi vertikal


$$|y_2 - y_1|$$Contoh:


Jarak antara A(1,2) dan B(5,5)


$$|d| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|d| = \sqrt{(5 - 1)^2 + (5 - 2)^2}$$$$|d| = \sqrt{4^2 + 3^2}$$$$|d| = \sqrt{16 + 9} = \sqrt{25} = 5$$

Jadi, jarak antara titik A(1,2) dan B(5,5) adalah 5.


Bandingkan dengan menggunakan EMT:


\>load geometry


    Numerical and symbolic geometry.

\>A=[1,2];

\>B=[5,5];

\>distance(A,B)


    5

\>setPlotRange(0,7,0,7);

\>A=[1,2]; plotPoint(A,"A");

\>B=[5,5]; plotPoint(B,"B");

\>plotSegment(A,B,"c"):


![images/Presentasi_EMT_#Geometri-647.png](images/Presentasi_EMT_#Geometri-647.png)

\>reset;


# 2. Luas Segitiga Luas segitiga dapat dihitung menggunakan beberapa

metode tergantung pada informasi yang diberikan. Berikut adalah
beberapa cara umum untuk menghitung luas segitiga.


## 1) Menggunakan Alas dan Tinggi



Jika diketahui panjang alas (a) dan tinggi (t) segitiga, maka luasnya
dapat dihitung dengan rumus:


$$L = \frac{1}{2} \times a \times t$$Rumus luas segitiga di atas didapat dari hubungan dengan persegi
panjang. Bayangkan sebuah persegi panjang dengan panjang a (alas
segitiga) dan lebar t (tinggi segitiga). Luas persegi panjang ini
adalah:


$$a \times t$$Jika kita membagi persegi panjang ini menjadi dua segitiga yang
identik dengan menarik diagonal dari satu sudut ke sudut berlawanan,
kita akan mendapatkan dua segitiga dengan alas a dan tinggi t. Karena
luas kedua segitiga ini sama, maka luas setiap segitiga adalah
setengah dari luas persegi panjang tersebut, yang dapat ditulis:


$$L = \frac{1}{2} \times a \times t$$

Contoh:


Hitung luas segitiga dengan alas 10cm dan tingginya 8cm.


$$L = \frac{1}{2} \times 10 \times 8$$$$L = \frac{1}{2} \times 80 = 40cm^2$$

Jadi, luas segitiga tersebut adalah 40cm^2.


Bandingkan dengan EMT.


\>a:= 10;

\>t:= 8;

\>0.5\*10\*8


    40

## 2) Luas Segitiga Menggunakan Rumus Heron

Rumus Heron biasanya digunakan untuk menghitung luas segitiga ketika
yang diketahui adalah panjang ketiga sisi segitiga dan koordinat
titik-titiknya.


Rumus Heron menyatakan bahwa luas segitiga dengan panjang sisi-sisi a,
b dan c adalah:


$$L = \sqrt{s(s-a)(s-b)(s-c)}\quad \text{ dengan } s=\frac{(a+b+c)}{2},$$atau bisa ditulis dalam bentuk lain:


$$L = \frac{1}{4}\sqrt{(a+b+c)(b+c-a)(a+c-b)(a+b-c)}$$Untuk membuktikan hal ini kita misalkan C(0,0), B(a,0) dan A(x,y),
b=AC, c=AB. Luas segitiga ABC adalah


$$L_{\triangle ABC}=\frac{1}{2}a\times y.$$Nilai y didapat dengan menyelesaikan sistem persamaan:


$$x^2+y^2=b^2, \quad (x-a)^2+y^2=c^2.$$Contoh.


Diketahui suatu segitiga melalui titik-titik A[1,2], B[4,6], dan
C[7,2]. Hitunglah luas segitiga tersebut.


Jawab:


Yang pertama dilakukan adalah menghitung panjang garisnya menggunakan
rumus panjang garis (jarak dua titik).


Garis pertama, garis AB didefinisikan sebagai a.


Jarak antara A(1,2) dan B(4,6)


$$|a| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|a| = \sqrt{(4 - 1)^2 + (6 - 2)^2}$$$$|a| = \sqrt{3^2 + 4^2}$$$$|a| = \sqrt{9 + 16} = \sqrt{25}=5$$

sehingga a = 5.


Garis kedua, garis BC yang didefinisikan sebagai b.


Jarak antara B(4,6) dan C(7,2)


$$|b| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|b| = \sqrt{(7 - 4)^2 + (2 - 6)^2}=$$$$|b| = \sqrt{3^2 + (-4)^2}$$$$|b| = \sqrt{9 + 16} = \sqrt{25} = 5$$

sehingga b = 5.


Garis ketiga, garis AC yang didefinisikan sebagai c.


Jarak antara A(1,2) dan C(7,2)


$$|c| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|c| = \sqrt{(7 - 1)^2 + (2-0)^2}=$$$$|c| = \sqrt{6^2 + 0^2}$$$$|c| = \sqrt{36 + 0} = \sqrt{36}= 6$$

sehingga c = 6.


$$s=\frac{(5+5+6)}{2} = \frac{16}{2}=8$$$$L = \sqrt{s(s-a)(s-b)(s-c)}$$$$L = \sqrt{8(8-5)(8-5)(8-6)}$$$$L = \sqrt{8(3)(3)(2)} = \sqrt{144}=12$$Jadi, luas segitiga yang melalui titik-titik A[1,2], B[4,6], dan
C[7,2] adalah 12cm^2.


Perhitungan dengan EMT


\>A=[1,2];

\>B=[4,6];

\>C=[7,2];

\>areaTriangle(A,B,C)


    12

## Latihan

Diketahui segitiga dengan alas a dan tinggi t memiliki luas 20 cm^2.
Tentukan pasangan nilai a dan t berikut yang dapat menjadi panjang
alas dan tinggi segitiga tersebut jika alas dan tinggi merupakan
bilangan bulat positif.


Pilihan jawaban:


A. a=5 cm dan t=8cm


B. a=10cm dan t=4cm


C. a=7cm dan  t=6cm


D. a=4cm dan  t=10cm


E. a=6cm dan t=6cm


$$L = \frac{1}{2} \times a \times t$$

Maka, a*t=40


Perkalian a dan t menghasilkan 40, yang benar adalah opsi A, B, dan D.


\>load "C:\\Users\\ASUS\\Euler\\EulerTemp.e"


    Could not open C:\Users\ASUS\Euler\EulerTemp.e!
    Error in:
    load "C:\Users\ASUS\Euler\EulerTemp.e" ...
                                          ^

# 3. Keliling Segitiga

Secara umum, keliling segitiga (P) adalah jumlah panjang ketiga
sisinya. Misalkan kita memiliki segitiga dengan tiga sisi a, b, dan c
maka kelilingnya dapat diperoleh dengan


$$P = a + b + c$$Contoh


Diketahui segitiga dengan titik sudut A(4,0), B(-4,0) dan C(0,3).
Berapa keliling segitiga tersebut?


Yang pertama dilakukan adalah menghitung panjang garisnya menggunakan
rumus panjang garis (jarak dua titik).


Garis pertama, garis AB didefinisikan sebagai a.


Jarak antara A(4,0) dan B(-4,0)


$$|a| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|a| = \sqrt{(4 - (-4))^2 + (0 - 0)^2}$$$$|a| = \sqrt{8^2 + 0^2}$$$$|a| = \sqrt{64 + 0} = \sqrt{64}=8$$

sehingga a = 8.


Garis kedua, garis BC yang didefinisikan sebagai b.


Jarak antara B(-4,0) dan C(0,3)


$$|b| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|b| = \sqrt{(0 - (-4))^2 + (3 - 0)^2}=$$$$|b| = \sqrt{4^2 + 3^2}$$$$|b| = \sqrt{16 + 9} = \sqrt{25} = 5$$

sehingga b = 5.


Garis ketiga, garis AC yang didefinisikan sebagai c.


Jarak antara A(4,0) dan C(0,3)


$$|c| = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$$$|c| = \sqrt{(0 - 4)^2 + (3-0)^2}=$$$$|c| = \sqrt{(-4)^2 + 3^2}$$$$|c| = \sqrt{16 + 9} = \sqrt{25}= 5$$

sehingga c = 5.


$$P = a + b + c = 8 + 5 + 5 = 18$$Jadi, keliling segitiga tersebut adalah 18


Bandingkan dengan perhitungan EMT.


\>load geometry


    Numerical and symbolic geometry.

\>A = [4,0];

\>B = [-4,0];

\>C = [0,3];

\>a = distance(A,B)


    8

\>b = distance(B,C)


    5

\>c = distance(A,C)


    5

\>K = a + b + c


    18

# 4. Luas Lingkaran

Luas lingkaran adalah ukuran dari area atau wilayah yang tertutup oleh
sebuah lingkaran. Untuk menghitung luas lingkaran, kita bisa
menggunakan rumus:


$$\text{Luas} = \pi \times r^2$$di mana:


$$\pi \text{ adalah konstanta dengan nilai mendekati 3,14159}$$$$r \text{  adalah jari-jari lingkaran, yaitu jarak dari pusat lingkaran ke tepi lingkaran}$$Contoh Penghitungan Luas Lingkaran


Jika sebuah lingkaran memiliki jari-jari 10 cm, maka luasnya adalah:


$$L = \pi \times r^2=\pi \times 10^2 = 3,14159 \times 100 = 314,159 \text{ cm}^2$$Luas lingkaran sangat bergantung pada jari-jarinya. Jika jari-jari
lingkaran bertambah, maka luas lingkaran akan bertambah dengan kuadrat
dari jari-jari.


\>r=10;

\>area := pi \* r^2;

\>area


    314.159265359

## Latihan

1. Sebuah taman kota berbentuk lingkaran memiliki jari-jari 20 meter.
Taman tersebut akan ditanami rumput. Berapa luas area taman yang akan
ditanami rumput tersebut?


A) 1236,637


B) 628,3185


C) 1256,637


D) 2256, 637


Jawaban:


$$L = \pi \times r^2=\pi \times 20^2 = 3,14159 \times 400 = 1256,637 \text{ cm}^2$$\>r=20;

\>area := pi \* r^2;

\>area


    1256.63706144

2. Seorang pelukis membuat karya lukis objek geomtri berbentuk
lingkaran. Ada dua lingkaran yang memiliki pusat yang sama
(konsentris). Lingkaran yang lebih besar memiliki jari-jari 15 meter,
dan lingkaran yang lebih kecil di dalamnya memiliki jari-jari 8 meter.
Seorang pelukis ingin mewarnai area antara dua lingkaran ini. Berapa
luas area yang perlu diwarnai?


Jawab:


Luas lingkaran besar:


$$L = \pi \times r^2=\pi \times 15^2 = 3,14159 \times 225 = 706,858 \text{ m}^2$$Luas lingkaran kecil:


$$L = \pi \times r^2=\pi \times 8^2 = 3,14159 \times 64 = 201,062 \text{ m}^2$$Luas di antara lingkaran besar dan kecil didapat dengan mengurangkan
luas lingkaran besar dan kecil.


$$706,858-201,062 = 505,796 \text{ m}^2$$\>r1=15;

\>area1:= pi \* r1^2;

\>area1


    706.858347058

\>r2=8;

\>area2:=pi\*r2^2;

\>area2


    201.06192983

\>area1-area2


    505.796417228

# 5. Keliling Lingkaran

Keliling lingkaran adalah panjang batas luar dari lingkaran. Untuk
menghitung keliling, kita memerlukan informasi tentang jari-jari atau
diameter (d), di mana diameter adalah dua kali jari-jari (d=2r).


Untuk menghitung keliling lingkaran, kita dapat menggunakan rumus:


$$K = 2 \pi r$$Keterangan:


- K = keliling lingkaran


- r = jari-jari lingkaran


Contoh.


Keliling lingkaran dengan jari-jari 5


$$K = 2 \pi r$$$$K = 2 \pi 5$$$$K = 10(3,14)=31,4$$Bandingkan dengan perhitungan EMT


\>r := 5;

\>K = 2\*pi\*r


    31.4159265359

Contoh


Sebuah roda memiliki jari-jari 21 cm. Jika roda tersebut berputar satu
kali penuh, berapa jarak yang dilalui? Jika roda berputar selama 5
menit dengan kecepatan 30 putaran per menit, berapa jarak total yang
ditempuh?


1. Menghitung keliling roda


$$K = 2 \pi r$$$$K = 2 \pi 21$$$$K = 2 \times (\frac{22}{7}) \times 21 = 132cm$$

Jadi, keliling roda adalah 132cm


2. Menghitung jarak yang ditempuh dalam 5 Menit


Jika roda berputar 30 putaran per menit, maka dalam 5 menit:


Total putaran = 30 putaran/menit×5 menit = 150 putaran


Jarak total= Keliling×total putaran


$$132\times 150 = 19800cm = 198m$$Bandingkan dengan perhitungan EMT


\>r:=21;

\>K=2\*pi\*r


    131.946891451

\>TP = 30\*5


    150

\>JT = K\*TP


    19792.0337176

Contoh


Sebuah lingkaran memiliki jari-jari yang berubah-ubah. Jari-jari
lingkaran ditentukan dengan rumus r=4+k, di mana k adalah angka yang
mulai dari 1 hingga 5. Hitunglah total keliling lingkaran saat k
bervariasi dari 1 hingga 5.


1. Mengitung jari-jari untuk setiap nilai k:


$$k = 1, r = 4 + 1 = 5$$$$k = 2, r = 4 + 2 = 6$$$$k = 3, r = 4 + 3 = 7$$$$k = 4, r = 4 + 4 = 8$$$$k = 5, r = 4 + 5 = 9$$2. Hitung keliling untuk setiap jari-jari:


$$K(1) = 2\pi(5)= 10\pi$$$$K(2) = 2\pi(6)= 12\pi$$$$K(3) = 2\pi(7)= 14\pi$$$$K(4) = 2\pi(8)= 16\pi$$$$K(4) = 2\pi(9)= 18\pi$$3. Jumlah total keliling


$$K = 10\pi + 12\pi + 14\pi + 16\pi +18\pi = 70\pi = 219,911$$Bandingkan dengan perhitungan EMT


\>k = 1:4;

\>r = 6-k;

\>KT = sum(2\*pi\*r)


    87.9645943005

Sebuah kolam berbentuk lingkaran memiliki keliling 40pi. Kolam
tersebut akan dipasang ubin sesuai luasnya. Berapa luas kolam
tersebut?


Jawab:


keliling


$$\pi \times 2r$$$$40 \pi= \pi \times 2r$$\>&solve(40\*pi=pi\*2\*r)


    
                                      []
    

\>r = 20


    20

\>area:=pi\*r^2


    1256.63706144

## LATIHAN SOAL



Sebuah lingkaran memiliki jari-jari yang berubah-ubah. Jari-jari
lingkaran ditentukan dengan rumus r=6-k, di mana k adalah angka yang
mulai dari 1 hingga 4. Berapa total keliling lingkaran saat k
bervariasi dari 1 hingga 4?


\>k = 1:4;

\>r = 6-k;

\>KT = sum(2\*pi\*r)


    87.9645943005

Jadi, jawaban yang benar adalah a yaitu 87,9654


## LATIHAN SOAL



Sebuah kolam berbentuk lingkaran memiliki keliling 40pi. Apakah benar
luas kolam tersebut adalah 1256.637?


\>&solve(40\*pi=pi\*2\*r) // mencari jari-jari


    
                                      []
    

\>r = 20


    20

\>area:=pi\*r^2


    1256.63706144

Jadi, benar bahwa luas kolam tersebut adalah 1256.637


## LATIHAN SOAL



Jodohkan setiap ruas garis yang dibentuk oleh 2 titik dengan jaraknya


a. AB,dengan  A=(-1,-1)  dan B(5,-1)


b. BC,dengan  B=(5,-1) dan C(5,7)


c. AC,dengan  A=(-1,-1)  dan C(5,7)


Jarak


\>load Geometry


    Numerical and symbolic geometry.

\>A = [-1,-1];

\>B = [5,-1];

\>C = [5,7];

\>AB = distance(A,B)


    6

\>BC = distance(B,C)


    8

\>AC = distance(A,C)


    10

## LATIHAN SOAL



Terdapat dua segitiga, yaitu segitiga A dan segitiga B. Segitiga A
memiliki titik sudut (2,2),(2,6)  dan (8,2). Sedangkan, segitiga B
memiliki titik sudut (3,-4),(-2,-4)  dan (-4,6). Hitunglah kedua luas
segitiga tersebut, dan pilihlah pernyataan yang benar.


a. Luas segitiga A lebih besar dibandingkan luas segitiga B


b. Luas segitiga B lebih besar dibandingkan luas segitiga A


c. Luas segitiga A sama dengan luas segitiga B


d. Selisih kedua luas segitiga tersebut adalah 13


\>A1 = [2,2];

\>A2 = [2,6];

\>A3 = [8,2];

\>LA = areaTriangle(A1,A2,A3) // Luas segitiga A


    12

\>B1 = [3,-4];

\>B2 = [-2,-4];

\>B3 = [-4,6];

\>LB = areaTriangle(B1,B2,B3) // Luas segitiga B


    25

\>selisih = LB-LA


    13

Jadi, pernyataan yang benar adalah b (Luas segitiga B lebih besar
dibandingkan luas segitiga A) dan d (Selisih kedua luas segitiga
tersebut adalah 13)





# EMT untuk Statistika

Dalam buku catatan ini, kami mendemonstrasikan plot statistik utama,
tes dan distribusi dalam Euler.


Mari kita mulai dengan beberapa statistik deskriptif. Ini bukanlah
sebuah pengantar statistik. Jadi, Anda mungkin memerlukan beberapa
latar belakang untuk memahami detailnya.


Asumsikan pengukuran berikut ini. Kita ingin menghitung nilai
rata-rata dan deviasi standar yang diukur.


\>M=[1000,1004,998,997,1002,1001,998,1004,998,997]; ...  
\>   median(M), mean(M), dev(M),


    999
    999.9
    2.72641400622

Kita dapat memplot plot kotak dan kumis untuk data tersebut. Dalam
kasus kami, tidak ada pencilan.


\>aspect(1.75); boxplot(M):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-001.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-001.png)

Kami menghitung probabilitas bahwa suatu nilai lebih besar dari 1005,
dengan mengasumsikan nilai yang diukur dari distribusi normal.


Semua fungsi untuk distribusi dalam Euler diakhiri dengan ...dis dan
menghitung distribusi probabilitas kumulatif (CPF).


$$\text{normaldis(x,m,d)}=\int_{-\infty}^x \frac{1}{d\sqrt{2\pi}}e^{-\frac{1}{2}(\frac{t-m}{d})^2}\ dt.$$Kami mencetak hasilnya dalam % dengan akurasi 2 digit menggunakan
fungsi cetak.


\>print((1-normaldis(1005,mean(M),dev(M)))\*100,2,unit=" %")


          3.07 %

Untuk contoh berikutnya, kami mengasumsikan jumlah pria berikut ini
dalam rentang ukuran tertentu.


\>r=155.5:4:187.5; v=[22,71,136,169,139,71,32,8];


Ini adalah plot distribsusinya


\>plot2d(r,v,a=150,b=200,c=0,d=190,bar=1,style="\\/"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-003.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-003.png)

Kita dapat memasukkan data mentah tersebut ke dalam tabel.


Tabel adalah sebuah metode untuk menyimpan data statistik. Tabel kita
harus berisi tiga kolom: Awal rentang, akhir rentang, jumlah orang
dalam rentang.


Tabel dapat dicetak dengan header. Kami menggunakan vektor string
untuk mengatur header.


\>T:=r[1:8]' | r[2:9]' | v'; writetable(T,labc=["BB","BA","Frek"])


            BB        BA      Frek
         155.5     159.5        22
         159.5     163.5        71
         163.5     167.5       136
         167.5     171.5       169
         171.5     175.5       139
         175.5     179.5        71
         179.5     183.5        32
         183.5     187.5         8

Jika kita membutuhkan nilai rata-rata dan statistik lain dari ukuran,
kita perlu menghitung titik tengah rentang. Kita dapat menggunakan dua
kolom pertama dari tabel kita untuk hal ini.


Sumbol “|” digunakan untuk memisahkan kolom, fungsi “writetable”
digunakan untuk menulis tabel, dengan opsi “labc” untuk menentukan
judul kolom.


\>(T[,1]+T[,2])/2 // the midpoint of each interval


            157.5 
            161.5 
            165.5 
            169.5 
            173.5 
            177.5 
            181.5 
            185.5 

Tetapi akan lebih mudah, untuk melipat rentang dengan vektor
[1/2,1/2].


\>M=fold(r,[0.5,0.5])


    [157.5,  161.5,  165.5,  169.5,  173.5,  177.5,  181.5,  185.5]

Sekarang kita dapat menghitung rata-rata dan deviasi sampel dengan
frekuensi yang diberikan.


\>{m,d}=meandev(M,v); m, d,


    169.901234568
    5.98912964449

Mari kita tambahkan distribusi normal dari nilai-nilai tersebut ke
dalam diagram batang di atas. Rumus untuk distribusi normal dengan
rata-rata m dan deviasi standar d adalah:


$$y=\frac{1}{d\sqrt{2\pi}}e^{\frac{-(x-m)^2}{2d^2}}.$$Karena nilainya antara 0 dan 1, untuk memplotnya pada diagram batang,
nilai tersebut harus dikalikan dengan 4 kali jumlah data.


\>plot2d("qnormal(x,m,d)\*sum(v)\*4", ...  
\>     xmin=min(r),xmax=max(r),thickness=3,add=1):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-005.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-005.png)

# Tabel

Dalam direktori buku catatan ini, Anda dapat menemukan file dengan
tabel. Data tersebut mewakili hasil survei. Berikut adalah empat baris
pertama dari file tersebut. Data berasal dari sebuah buku online
berbahasa Jerman “Einführung in die Statistik mit R” oleh A. Handl.


\>printfile("table.dat",4);


    Person Sex Age Titanic Evaluation Tip Problem
    1 m 30 n . 1.80 n
    2 f 23 y g 1.80 n
    3 f 26 y g 1.80 y

Tabel berisi 7 kolom angka atau token (string). Kita ingin membaca
tabel tersebut dari file. Pertama, kita menggunakan terjemahan kita
sendiri untuk token-token tersebut.


Untuk itu, kita mendefinisikan set token. Fungsi strtokens()
mendapatkan vektor string token dari string yang diberikan.


\>mf:=["m","f"]; yn:=["y","n"]; ev:=strtokens("g vg m b vb");


Sekarang kita membaca tabel dengan terjemahan ini.


Argumen tok2, tok4, dan lain-lain adalah terjemahan dari kolom-kolom
tabel. Argumen-argumen ini tidak ada dalam daftar parameter
readtable(), jadi Anda perlu memberikannya dengan “:=”.


\>{MT,hd}=readtable("table.dat",tok2:=mf,tok4:=yn,tok5:=ev,tok7:=yn);

\>load over statistics;


Untuk mencetak, kita perlu menentukan set token yang sama. Kami
mencetak empat baris pertama saja.


\>writetable(MT[1:10],labc=hd,wc=5,tok2:=mf,tok4:=yn,tok5:=ev,tok7:=yn);


     Person  Sex  Age Titanic Evaluation  Tip Problem
          1    m   30       n          .  1.8       n
          2    f   23       y          g  1.8       n
          3    f   26       y          g  1.8       y
          4    m   33       n          .  2.8       n
          5    m   37       n          .  1.8       n
          6    m   28       y          g  2.8       y
          7    f   31       y         vg  2.8       n
          8    m   23       n          .  0.8       n
          9    f   24       y         vg  1.8       y
         10    m   26       n          .  1.8       n

Tanda titik “.” mewakili nilai yang tidak tersedia.


Jika kita tidak ingin menentukan token untuk terjemahan sebelumnya,
kita hanya perlu menentukan kolom mana yang berisi token dan bukan
angka.


\>ctok=[2,4,5,7]; {MT,hd,tok}=readtable("table.dat",ctok=ctok);


Fungsi readtable() sekarang mengembalikan satu set token.


\>tok


    m
    n
    f
    y
    g
    vg

Tabel berisi entri dari file dengan token yang diterjemahkan ke angka.


String khusus NA=“.” ditafsirkan sebagai “Tidak Tersedia”, dan
mendapatkan NAN (bukan angka) dalam tabel. Terjemahan ini dapat diubah
dengan parameter NA, dan NAval.


\>MT[1]


    [1,  1,  30,  2,  NAN,  1.8,  2]

Berikut ini adalah isi tabel dengan angka yang tidak diterjemahkan.


\>writetable(MT,wc=5)


        1    1   30    2    .  1.8    2
        2    3   23    4    5  1.8    2
        3    3   26    4    5  1.8    4
        4    1   33    2    .  2.8    2
        5    1   37    2    .  1.8    2
        6    1   28    4    5  2.8    4
        7    3   31    4    6  2.8    2
        8    1   23    2    .  0.8    2
        9    3   24    4    6  1.8    4
       10    1   26    2    .  1.8    2
       11    3   23    4    6  1.8    4
       12    1   32    4    5  1.8    2
       13    1   29    4    6  1.8    4
       14    3   25    4    5  1.8    4
       15    3   31    4    5  0.8    2
       16    1   26    4    5  2.8    2
       17    1   37    2    .  3.8    2
       18    1   38    4    5    .    2
       19    3   29    2    .  3.8    2
       20    3   28    4    6  1.8    2
       21    3   28    4    1  2.8    4
       22    3   28    4    6  1.8    4
       23    3   38    4    5  2.8    2
       24    3   27    4    1  1.8    4
       25    1   27    2    .  2.8    4

Untuk kenyamanan, Anda dapat menaruh output dari readtable() ke dalam
sebuah daftar.


\>Table={{readtable("table.dat",ctok=ctok)}};


Dengan menggunakan kolom token yang sama dan token yang dibaca dari
file, kita dapat mencetak tabel. Kita dapat menentukan ctok, tok, dll.
atau menggunakan daftar Tabel.


\>writetable(Table,ctok=ctok,wc=5);


     Person  Sex  Age Titanic Evaluation  Tip Problem
          1    m   30       n          .  1.8       n
          2    f   23       y          g  1.8       n
          3    f   26       y          g  1.8       y
          4    m   33       n          .  2.8       n
          5    m   37       n          .  1.8       n
          6    m   28       y          g  2.8       y
          7    f   31       y         vg  2.8       n
          8    m   23       n          .  0.8       n
          9    f   24       y         vg  1.8       y
         10    m   26       n          .  1.8       n
         11    f   23       y         vg  1.8       y
         12    m   32       y          g  1.8       n
         13    m   29       y         vg  1.8       y
         14    f   25       y          g  1.8       y
         15    f   31       y          g  0.8       n
         16    m   26       y          g  2.8       n
         17    m   37       n          .  3.8       n
         18    m   38       y          g    .       n
         19    f   29       n          .  3.8       n
         20    f   28       y         vg  1.8       n
         21    f   28       y          m  2.8       y
         22    f   28       y         vg  1.8       y
         23    f   38       y          g  2.8       n
         24    f   27       y          m  1.8       y
         25    m   27       n          .  2.8       y

Fungsi tablecol() mengembalikan nilai kolom dari tabel, melewatkan
setiap baris dengan nilai NAN (“.” dalam file), dan indeks kolom, yang
berisi nilai-nilai ini.


\>{c,i}=tablecol(MT,[5,6]);


Kita dapat menggunakan ini untuk mengekstrak kolom dari tabel untuk
tabel baru.


\>j=[1,5,6]; writetable(MT[i,j],labc=hd[j],ctok=[2],tok=tok)


        Person Evaluation       Tip
             2          g       1.8
             3          g       1.8
             6          g       2.8
             7         vg       2.8
             9         vg       1.8
            11         vg       1.8
            12          g       1.8
            13         vg       1.8
            14          g       1.8
            15          g       0.8
            16          g       2.8
            20         vg       1.8
            21          m       2.8
            22         vg       1.8
            23          g       2.8
            24          m       1.8

Tentu saja, kita perlu mengekstrak tabel itu sendiri dari daftar Tabel
dalam kasus ini.


\>MT=Table[1];


Tentu saja, kita juga dapat menggunakannya untuk menentukan nilai
rata-rata kolom atau nilai statistik lainnya.


\>mean(tablecol(MT,6))


    2.175

Fungsi getstatistics() mengembalikan elemen-elemen dalam sebuah
vektor, dan jumlahnya. Kita menerapkannya pada nilai “m” dan “f” pada
kolom kedua tabel kita.


\>{xu,count}=getstatistics(tablecol(MT,2)); xu, count,


    [1,  3]
    [12,  13]

Kita bisa mencetak hasilnya dalam tabel baru.


\>writetable(count',labr=tok[xu])


             m        12
             f        13

Fungsi selecttable() mengembalikan sebuah tabel baru dengan nilai
dalam satu kolom yang dipilih dari vektor indeks. Pertama, kita
mencari indeks dari dua nilai kita dalam tabel token.


\>v:=indexof(tok,["g","vg"])


    [5,  6]

Sekarang kita dapat memilih baris-baris dari tabel, yang memiliki
salah satu nilai dalam v di baris ke-5.


\>MT1:=MT[selectrows(MT,5,v)]; i:=sortedrows(MT1,5);


Sekarang kita dapat mencetak tabel, dengan nilai yang diekstrak dan
diurutkan di kolom ke-5.


\>writetable(MT1[i],labc=hd,ctok=ctok,tok=tok,wc=7);


     Person    Sex    Age Titanic Evaluation    Tip Problem
          2      f     23       y          g    1.8       n
          3      f     26       y          g    1.8       y
          6      m     28       y          g    2.8       y
         18      m     38       y          g      .       n
         16      m     26       y          g    2.8       n
         15      f     31       y          g    0.8       n
         12      m     32       y          g    1.8       n
         23      f     38       y          g    2.8       n
         14      f     25       y          g    1.8       y
          9      f     24       y         vg    1.8       y
          7      f     31       y         vg    2.8       n
         20      f     28       y         vg    1.8       n
         22      f     28       y         vg    1.8       y
         13      m     29       y         vg    1.8       y
         11      f     23       y         vg    1.8       y

Untuk statistik berikutnya, kita ingin menghubungkan dua kolom tabel.
Jadi kita mengekstrak kolom 2 dan 4 dan mengurutkan tabel.


\>i=sortedrows(MT,[2,4]);  ...  
\>     writetable(tablecol(MT[i],[2,4])',ctok=[1,2],tok=tok)


             m         n
             m         n
             m         n
             m         n
             m         n
             m         n
             m         n
             m         y
             m         y
             m         y
             m         y
             m         y
             f         n
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y
             f         y

Dengan getstatistics(), kita juga dapat menghubungkan hitungan dalam
dua kolom tabel satu sama lain.


\>MT24=tablecol(MT,[2,4]); ...  
\>   {xu1,xu2,count}=getstatistics(MT24[1],MT24[2]); ...  
\>   writetable(count,labr=tok[xu1],labc=tok[xu2])


                       n         y
             m         7         5
             f         1        12

Tabel dapat ditulis ke sebuah file.


\>filename="test.dat"; ...  
\>   writetable(count,labr=tok[xu1],labc=tok[xu2],file=filename);


Lalu kita bisa membaca tabel dari file.


\>{MT2,hd,tok2,hdr}=readtable(filename,\>clabs,\>rlabs); ...  
\>   writetable(MT2,labr=hdr,labc=hd)


                       n         y
             m         7         5
             f         1        12

Hapus file ini.


\>fileremove(filename);


# Distribusi

Dengan plot2d, ada metode yang sangat mudah untuk memplot distribusi
data eksperimen.


\>p=normal(1,1000); //1000 random normal-distributed sample p

\>plot2d(p,distribution=20,style="\\/"); // plot the random sample p

\>plot2d("qnormal(x,0,1)",add=1): // add the standard normal distribution plot


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-006.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-006.png)

Perhatikan perbedaan antara plot batang (sampel) dan kurva normal
(distribusi sesungguhnya). Masukkan kembali ketiga perintah tersebut
untuk melihat hasil pengambilan sampel yang lain.


Berikut ini adalah perbandingan 10 simulasi dari 1000 nilai
terdistribusi normal dengan menggunakan apa yang disebut plot kotak.
Plot ini menunjukkan median, kuartil 25% dan 75%, nilai minimal dan
maksimal, serta pencilan.


\>p=normal(10,1000); boxplot(p):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-007.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-007.png)

Untuk menghasilkan bilangan bulat acak, Euler memiliki intrandom. Mari
kita simulasikan pelemparan dadu dan memplot distribusinya.


Kita menggunakan fungsi getmultiplicities(v,x), yang menghitung
seberapa sering elemen-elemen dari v muncul di dalam x. Kemudian kita
memplot hasilnya menggunakan columnsplot().


\>k=intrandom(1,6000,6);  ...  
\>   columnsplot(getmultiplicities(1:6,k));  ...  
\>   ygrid(1000,color=red):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-008.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-008.png)

Meskipun intrandom(n,m,k) menghasilkan bilangan bulat yang
terdistribusi secara seragam dari 1 sampai k, adalah mungkin untuk
menggunakan distribusi bilangan bulat yang lain dengan randpint().


Pada contoh berikut, probabilitas untuk 1,2,3 adalah 0.4, 0.1, 0.5
secara berurutan.


\>randpint(1,1000,[0.4,0.1,0.5]); getmultiplicities(1:3,%)


    [378,  102,  520]

Euler dapat menghasilkan nilai acak dari lebih banyak distribusi.
Lihatlah ke dalam referensi.


Misalnya, kita mencoba distribusi eksponensial. Variabel acak kontinu
X is said to have an exponential distribution, if its PDF is given by


$$f_X(x)=\lambda e^{-\lambda x},\quad x>0,\quad \lambda>0,$$

dengan parameter


$$\lambda=\frac{1}{\mu},\quad \mu \text{ is the mean, and denoted by } X \sim \text{Exponential}(\lambda).$$\>plot2d(randexponential(1,1000,2),\>distribution):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-011.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-011.png)

Untuk banyak distribusi, Euler dapat menghitung fungsi distribusi dan
kebalikannya.


\>plot2d("normaldis",-4,4): 


Berikut ini adalah salah satu cara untuk memplot kuantil.


\>plot2d("qnormal(x,1,1.5)",-4,6);  ...  
\>   plot2d("qnormal(x,1,1.5)",a=2,b=5,\>add,\>filled):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-012.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-012.png)

$$\text{normaldis(x,m,d)}=\int_{-\infty}^x \frac{1}{d\sqrt{2\pi}}e^{-\frac{1}{2}(\frac{t-m}{d})^2}\ dt.$$

Probabilitas untuk berada di area hijau adalah sebagai berikut.


\>normaldis(5,1,1.5)-normaldis(2,1,1.5)


    0.248662156979

Hal ini dapat dihitung secara numerik dengan integral berikut ini.


$$\int_2^5 \frac{1}{1.5\sqrt{2\pi}}e^{-\frac{1}{2}(\frac{x-1}{1.5})^2}\ dx.$$\>gauss("qnormal(x,1,1.5)",2,5)


    0.248662156979

Mari kita bandingkan distribusi binomial dengan distribusi normal
dengan rata-rata dan deviasi yang sama. Fungsi invbindis()
menyelesaikan interpolasi linier antara nilai bilangan bulat.


\>invbindis(0.95,1000,0.5), invnormaldis(0.95,500,0.5\*sqrt(1000))


    525.516721219
    526.007419394

Fungsi qdis() adalah densitas dari distribusi chi-square. Seperti
biasa, Euler memetakan vektor ke fungsi ini. Dengan demikian kita
mendapatkan plot semua distribusi chi-kuadrat dengan derajat 5 hingga
30 dengan mudah dengan cara berikut.


\>plot2d("qchidis(x,(5:5:50)')",0,50):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-015.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-015.png)

Euler memiliki fungsi-fungsi yang akurat untuk mengevaluasi
distribusi-distribusi. Mari kita periksa chidis() dengan sebuah
integral.


Penamaannya diusahakan untuk konsisten. Sebagai contoh,


* 
distribusi chi-kuadrat adalah chidis(),

* 
fungsi kebalikannya adalah invchidis(),

* 
densitasnya adalah qchidis().


Pelengkap dari distribusi (ekor atas) adalah chicdis().


\>chidis(1.5,2), integrate("qchidis(x,2)",0,1.5)


    0.527633447259
    0.527633447259

# Distribusi Diskrit

Untuk menentukan distribusi diskrit Anda sendiri, Anda dapat
menggunakan metode berikut.


Pertama, kita tetapkan fungsi distribusinya.


\>wd = 0|((1:6)+[-0.01,0.01,0,0,0,0])/6


    [0,  0.165,  0.335,  0.5,  0.666667,  0.833333,  1]

Artinya, dengan probabilitas wd[i+1]-wd[i] kita menghasilkan nilai
acak i.


Ini hampir merupakan distribusi yang seragam. Mari kita definisikan
sebuah generator bilangan acak untuk ini. Fungsi find(v,x) menemukan
nilai x dalam vektor v. Fungsi ini juga dapat digunakan untuk vektor
x.


\>function wrongdice (n,m) := find(wd,random(n,m))


Kesalahan ini sangat halus sehingga kita hanya bisa melihatnya setelah
melakukan iterasi yang sangat banyak.


\>columnsplot(getmultiplicities(1:6,wrongdice(1,1000000))):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-016.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-016.png)

Berikut ini adalah fungsi sederhana untuk memeriksa distribusi seragam
dari nilai 1... K dalam v. Kami menerima hasilnya, jika untuk semua
frekuensi


$$\left|f_i-\frac{1}{K}\right| < \frac{\delta}{\sqrt{n}}.$$\>function checkrandom (v, delta=1) ...


      K=max(v); n=cols(v);
      fr=getfrequencies(v,1:K);
      return max(fr/n-1/K)<delta/sqrt(n);
      endfunction
</pre>
Memang fungsi ini menolak distribusi seragam.


\>checkrandom(wrongdice(1,1000000))


    0

Dan ini menerima generator acak bawaan.


\>checkrandom(intrandom(1,1000000,6))


    1

Kita dapat menghitung distribusi binomial. Pertama, ada binomialsum(),
yang mengembalikan probabilitas i atau kurang dari n percobaan.


\>bindis(410,1000,0.4)


    0.751401349654

Fungsi Beta invers digunakan untuk menghitung interval kepercayaan
Clopper-Pearson untuk parameter p. Tingkat defaultnya adalah alpha.


Arti dari interval ini adalah jika p berada di luar interval, hasil
yang diamati sebesar 410 dalam 1000 jarang terjadi.


\>clopperpearson(410,1000)


    [0.37932,  0.441212]

Perintah berikut ini adalah cara langsung untuk mendapatkan hasil di
atas. Tetapi untuk n yang besar, penjumlahan langsung tidak akurat dan
lambat.


\>p=0.4; i=0:410; n=1000; sum(bin(n,i)\*p^i\*(1-p)^(n-i))


    0.751401349655

Omong-omong, invbinsum() menghitung kebalikan dari binomialsum().


\>invbindis(0.75,1000,0.4)


    409.932733047

Dalam Bridge, kita mengasumsikan 5 kartu yang terbuka (dari 52 kartu)
di dua tangan (26 kartu). Mari kita hitung probabilitas distribusi
yang lebih buruk dari 3:2 (misalnya 0:5, 1:4, 4:1, atau 5:0).


\>2\*hypergeomsum(1,5,13,26)


    0.321739130435

Ada juga simulasi distribusi multinomial.


\>randmultinomial(10,1000,[0.4,0.1,0.5])


              381           100           519 
              376            91           533 
              417            80           503 
              440            94           466 
              406           112           482 
              408            94           498 
              395           107           498 
              399            96           505 
              428            87           485 
              400            99           501 

# Memplot Data

Untuk memplot data, kami mencoba hasil pemilihan umum Jerman sejak
tahun 1990, yang diukur dalam kursi.


\>BW := [ ...  
\>   1990,662,319,239,79,8,17; ...  
\>   1994,672,294,252,47,49,30; ...  
\>   1998,669,245,298,43,47,36; ...  
\>   2002,603,248,251,47,55,2; ...  
\>   2005,614,226,222,61,51,54; ...  
\>   2009,622,239,146,93,68,76; ...  
\>   2013,631,311,193,0,63,64];


Untuk pesta, kami menggunakan serangkaian nama.


\>P:=["CDU/CSU","SPD","FDP","Gr","Li"];


Mari kita cetak persentasenya dengan baik.


Pertama kita ekstrak kolom-kolom yang diperlukan. Kolom 3 sampai 7
adalah kursi masing-masing partai, dan kolom 2 adalah jumlah total
kursi. kolom adalah tahun pemilihan.


\>BT:=BW[,3:7]; BT:=BT/sum(BT); YT:=BW[,1]';


Kemudian kita mencetak statistik dalam bentuk tabel. Kita menggunakan
nama sebagai judul kolom, dan tahun sebagai judul baris. Lebar default
untuk kolom adalah wc = 10, tetapi kami lebih suka output yang lebih
padat. Kolom-kolom akan diperluas untuk label-label kolom, jika perlu.


\>writetable(BT\*100,wc=6,dc=0,\>fixed,labc=P,labr=YT)


           CDU/CSU   SPD   FDP    Gr    Li
      1990      48    36    12     1     3
      1994      44    38     7     7     4
      1998      37    45     6     7     5
      2002      41    42     8     9     0
      2005      37    36    10     8     9
      2009      38    23    15    11    12
      2013      49    31     0    10    10

Perkalian matriks berikut ini mengekstrak jumlah persentase dua partai
besar yang menunjukkan bahwa partai-partai kecil telah memperoleh
suara di parlemen hingga tahun 2009.


\>BT1:=(BT.[1;1;0;0;0])'\*100


    [84.29,  81.25,  81.1659,  82.7529,  72.9642,  61.8971,  79.8732]

Ada juga plot statistik sederhana. Kita menggunakannya untuk
menampilkan garis dan titik secara bersamaan. Alternatif lainnya
adalah memanggil plot2d dua kali dengan &gt;add.


\>statplot(YT,BT1,"b"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-018.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-018.png)

Tentukan beberapa warna untuk masing-masing pihak.


\>CP:=[rgb(0.5,0.5,0.5),red,yellow,green,rgb(0.8,0,0)];


Sekarang kita dapat memplot hasil pemilu 2009 dan perubahannya ke
dalam satu plot menggunakan figure. Kita dapat menambahkan vektor
kolom pada setiap plot.


\>figure(2,1);  ...  
\>   figure(1); columnsplot(BW[6,3:7],P,color=CP); ...  
\>   figure(2); columnsplot(BW[6,3:7]-BW[5,3:7],P,color=CP);  ...  
\>   figure(0):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-019.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-019.png)

Plot data menggabungkan baris data statistik dalam satu plot.


\>J:=BW[,1]'; DP:=BW[,3:7]'; ...  
\>   dataplot(YT,BT',color=CP);  ...  
\>   labelbox(P,colors=CP,styles="[]",\>points,w=0.2,x=0.3,y=0.4):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-020.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-020.png)

Plot kolom 3D menunjukkan deretan data statistik dalam bentuk kolom.
Kami menyediakan label untuk baris dan kolom. angle adalah sudut
pandang.


\>columnsplot3d(BT,scols=P,srows=YT, ...  
\>     angle=30°,ccols=CP):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-021.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-021.png)

Representasi lainnya adalah plot mosaik. Perhatikan bahwa kolom-kolom
pada plot mewakili kolom-kolom pada matriks di sini. Karena panjangnya
label CDU/CSU, kita mengambil jendela yang lebih kecil dari biasanya.


\>shrinkwindow(\>smaller);  ...  
\>   mosaicplot(BT',srows=YT,scols=P,color=CP,style="#"); ...  
\>   shrinkwindow():


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-022.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-022.png)

Kita juga bisa membuat diagram lingkaran. Karena warna hitam dan
kuning membentuk sebuah koalisi, kita menyusun ulang elemen-elemennya.


\>i=[1,3,5,4,2]; piechart(BW[6,3:7][i],color=CP[i],lab=P[i]):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-023.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-023.png)

Berikut ini jenis plot yang lain.


\>starplot(normal(1,10)+4,lab=1:10,\>rays):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-024.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-024.png)

Beberapa plot di plot2d bagus untuk statika. Berikut ini adalah plot
impuls dari data acak, yang terdistribusi secara seragam dalam [0,1].


\>plot2d(makeimpulse(1:10,random(1,10)),\>bar):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-025.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-025.png)

Tetapi untuk data yang terdistribusi secara eksponensial, kita mungkin
memerlukan plot logaritmik.


\>logimpulseplot(1:10,-log(random(1,10))\*10):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-026.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-026.png)

Fungsi columnsplot() lebih mudah digunakan, karena hanya membutuhkan
sebuah vektor nilai. Selain itu, fungsi ini dapat mengatur labelnya
menjadi apa pun yang kita inginkan, kita telah mendemonstrasikan hal
ini dalam tutorial ini.


Berikut ini adalah aplikasi lain, di mana kita menghitung karakter
dalam sebuah kalimat dan memplot statistik.


\>v=strtochar("the quick brown fox jumps over the lazy dog"); ...  
\>   w=ascii("a"):ascii("z"); x=getmultiplicities(w,v); ...  
\>   cw=[]; for k=w; cw=cw|char(k); end; ...  
\>   columnsplot(x,lab=cw,width=0.05):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-027.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-027.png)

Anda juga dapat menetapkan sumbu secara manual.


\>n=10; p=0.4; i=0:n; x=bin(n,i)\*p^i\*(1-p)^(n-i); ...  
\>   columnsplot(x,lab=i,width=0.05,<frame,<grid); ...  
\>   yaxis(0,0:0.1:1,style="-\>",\>left); xaxis(0,style="."); ...  
\>   label("p",0,0.25), label("i",11,0); ...  
\>   textbox(["Binomial distribution","with p=0.4"]):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-028.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-028.png)

Berikut ini adalah cara untuk memplot frekuensi angka dalam vektor.


Kami membuat vektor angka acak bilangan bulat 1 hingga 6.


\>v:=intrandom(1,10,10)


    [8,  5,  8,  8,  6,  8,  8,  3,  5,  5]

Kemudian ekstrak nomor unik dalam v.


\>vu:=unique(v)


    [3,  5,  6,  8]

Dan memplot frekuensi dalam plot kolom.


\>columnsplot(getmultiplicities(vu,v),lab=vu,style="/"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-029.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-029.png)

Kami ingin mendemonstrasikan fungsi untuk distribusi nilai empiris.


\>x=normal(1,20);


Fungsi empdist(x,vs) membutuhkan larik nilai yang telah diurutkan.
Jadi kita harus mengurutkan x sebelum dapat menggunakannya.


\>xs=sort(x);


Kemudian kita memplot distribusi empiris dan beberapa batang kepadatan
ke dalam satu plot. Alih-alih plot batang untuk distribusi, kali ini
kami menggunakan plot gigi gergaji.


\>figure(2,1); ...  
\>   figure(1); plot2d("empdist",-4,4;xs); ...  
\>   figure(2); plot2d(histo(x,v=-4:0.2:4,<bar));  ...  
\>   figure(0):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-030.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-030.png)

Plot sebaran mudah dilakukan di Euler dengan plot titik biasa. Grafik
berikut ini menunjukkan bahwa X dan X+Y berkorelasi positif secara
jelas.


\>x=normal(1,100); plot2d(x,x+rotright(x),\>points,style=".."):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-031.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-031.png)

Sering kali, kita ingin membandingkan dua sampel dari distribusi yang
berbeda. Hal ini dapat dilakukan dengan plot kuantil-kuantil.


Untuk pengujian, kami mencoba distribusi student-t dan distribusi
eksponensial.


\>x=randt(1,1000,5); y=randnormal(1,1000,mean(x),dev(x)); ...  
\>   plot2d("x",r=6,style="--",yl="normal",xl="student-t",\>vertical); ...  
\>   plot2d(sort(x),sort(y),\>points,color=red,style="x",\>add):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-032.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-032.png)

Plot ini dengan jelas menunjukkan bahwa nilai yang terdistribusi
normal cenderung lebih kecil pada ujung yang ekstrim.


Jika kita memiliki dua distribusi dengan ukuran yang berbeda, kita
dapat memperluas distribusi yang lebih kecil atau memperkecil
distribusi yang lebih besar. Fungsi berikut ini bagus untuk keduanya.
Fungsi ini mengambil nilai median dengan persentase antara 0 dan 1.


\>function medianexpand (x,n) := median(x,p=linspace(0,1,n-1));


Mari kita bandingkan dua distribusi yang sama.


\>x=random(1000); y=random(400); ...  
\>   plot2d("x",0,1,style="--"); ...  
\>   plot2d(sort(medianexpand(x,400)),sort(y),\>points,color=red,style="x",\>add):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-033.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-033.png)

# Regresi dan Korelasi

Regresi linier dapat dilakukan dengan fungsi polyfit() atau berbagai
fungsi kecocokan.


Sebagai permulaan, kita mencari garis regresi untuk data univariat
dengan polyfit(x,y,1).


\>x=1:10; y=[2,3,1,5,6,3,7,8,9,8]; writetable(x'|y',labc=["x","y"])


             x         y
             1         2
             2         3
             3         1
             4         5
             5         6
             6         3
             7         7
             8         8
             9         9
            10         8

Kami ingin membandingkan kecocokan tanpa bobot dan dengan bobot.
Pertama, koefisien dari kecocokan linier.


\>p=polyfit(x,y,1)


    [0.733333,  0.812121]

Sekarang, koefisien dengan bobot yang menekankan nilai terakhir.


\>w &= "exp(-(x-10)^2/10)"; pw=polyfit(x,y,1,w=w(x))


    [4.71566,  0.38319]

Kami menempatkan semuanya ke dalam satu plot untuk titik-titik dan
garis regresi, dan untuk bobot yang digunakan.


\>figure(2,1);  ...  
\>   figure(1); statplot(x,y,"b",xl="Regression"); ...  
\>     plot2d("evalpoly(x,p)",\>add,color=blue,style="--"); ...  
\>     plot2d("evalpoly(x,pw)",5,10,\>add,color=red,style="--"); ...  
\>   figure(2); plot2d(w,1,10,\>filled,style="/",fillcolor=red,xl=w); ...  
\>   figure(0):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-034.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-034.png)

Untuk contoh lain, kita membaca survei tentang siswa, usia mereka,
usia orang tua mereka, dan jumlah saudara kandung dari sebuah file.


Tabel ini berisi “m” dan “f” pada kolom kedua. Kita menggunakan
variabel tok2 untuk mengatur terjemahan yang tepat dan bukannya
membiarkan readtable() mengumpulkan terjemahan.


\>{MS,hd}:=readtable("table1.dat",tok2:=["m","f"]);  ...  
\>   writetable(MS,labc=hd,tok2:=["m","f"]);


        Person       Sex       Age    Mother    Father  Siblings
             1         m        29        58        61         1
             2         f        26        53        54         2
             3         m        24        49        55         1
             4         f        25        56        63         3
             5         f        25        49        53         0
             6         f        23        55        55         2
             7         m        23        48        54         2
             8         m        27        56        58         1
             9         m        25        57        59         1
            10         m        24        50        54         1
            11         f        26        61        65         1
            12         m        24        50        52         1
            13         m        29        54        56         1
            14         m        28        48        51         2
            15         f        23        52        52         1
            16         m        24        45        57         1
            17         f        24        59        63         0
            18         f        23        52        55         1
            19         m        24        54        61         2
            20         f        23        54        55         1

Bagaimana usia saling bergantung satu sama lain? Kesan pertama datang
dari scatterplot berpasangan.


\>scatterplots(tablecol(MS,3:5),hd[3:5]):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-035.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-035.png)

Jelas bahwa usia ayah dan ibu saling bergantung satu sama lain. Mari
kita tentukan dan plot garis regresinya.


\>cs:=MS[,4:5]'; ps:=polyfit(cs[1],cs[2],1)


    [17.3789,  0.740964]

Ini jelas merupakan model yang salah. Garis regresinya adalah s = 17 +
0,74t, di mana t adalah usia ibu dan s adalah usia ayah. Perbedaan
usia mungkin sedikit bergantung pada usia, tetapi tidak terlalu
banyak.


Sebaliknya, kita menduga fungsi seperti s = a + t. Kemudian a adalah
rata-rata dari s-t. Ini adalah perbedaan usia rata-rata antara ayah
dan ibu.


\>da:=mean(cs[2]-cs[1])


    3.65

Mari buat plot ini menjadi satu buah scatter plot.


\>plot2d(cs[1],cs[2],\>points);  ...  
\>   plot2d("evalpoly(x,ps)",color=red,style=".",\>add);  ...  
\>   plot2d("x+da",color=blue,\>add):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-036.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-036.png)

Berikut ini adalah plot kotak dari kedua usia tersebut. Ini hanya
menunjukkan, bahwa usia keduanya berbeda.


\>boxplot(cs,["mothers","fathers"]):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-037.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-037.png)

Sangat menarik bahwa perbedaan dalam median tidak sebesar perbedaan
dalam mean.


\>median(cs[2])-median(cs[1])


    1.5

Koefisien korelasi menunjukkan korelasi positif.


\>correl(cs[1],cs[2])


    0.7588307236

Korelasi peringkat adalah ukuran untuk urutan yang sama dalam kedua
vektor. Korelasi ini juga cukup positif.


\>rankcorrel(cs[1],cs[2])


    0.758925292358

# Membuat Fungsi baru

Tentu saja, bahasa EMT dapat digunakan untuk memprogram fungsi baru.
Misalnya, kita mendefinisikan fungsi kemiringan.


$$\text{sk}(x) = \dfrac{\sqrt{n} \sum_i (x_i-m)^3}{\left(\sum_i (x_i-m)^2\right)^{3/2}}$$Dimana m adalah rata-rata dari x.


\>function skew (x:vector) ...


    m=mean(x);
    return sqrt(cols(x))*sum((x-m)^3)/(sum((x-m)^2))^(3/2);
    endfunction
</pre>
Seperti yang Anda lihat, kita dapat dengan mudah menggunakan bahasa
matriks untuk mendapatkan implementasi yang sangat singkat dan
efisien. Mari kita coba fungsi ini.


\>data=normal(20); skew(normal(10))


    -0.442260891308

Berikut ini adalah fungsi lain, yang disebut koefisien kemencengan
Pearson.


\>function skew1 (x) := 3\*(mean(x)-median(x))/dev(x)

\>skew1(data)


    Variable or function data not found.
    Error in:
    skew1(data) ...
              ^

# Simulasi Monte Carlo

Euler dapat digunakan untuk mensimulasikan kejadian acak. Kita telah
melihat contoh sederhana di atas. Berikut ini adalah contoh lainnya,
yang mensimulasikan 1000 kali pelemparan 3 dadu, dan menanyakan
distribusi dari jumlah tersebut.


\>ds:=sum(intrandom(1000,3,6))';  fs=getmultiplicities(3:18,ds)


    [4,  18,  28,  45,  57,  103,  126,  130,  124,  112,  97,  68,  53,
    26,  7,  2]

Kita bisa membuat plotnya.


\>columnsplot(fs,lab=3:18):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-039.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-039.png)

Untuk menentukan distribusi yang diharapkan tidaklah mudah. Kami
menggunakan rekursi tingkat lanjut untuk hal ini.


Fungsi berikut ini menghitung jumlah cara angka k dapat
direpresentasikan sebagai jumlah n angka dalam rentang 1 hingga m.
Fungsi ini bekerja secara rekursif dengan cara yang jelas.


\>function map countways (k; n, m) ...


      if n==1 then return k>=1 && k<=m
      else
        sum=0; 
        loop 1 to m; sum=sum+countways(k-#,n-1,m); end;
        return sum;
      end;
    endfunction
</pre>
Berikut ini adalah hasil dari tiga lemparan dadu.


\>countways(5:25,5,5)


    [1,  5,  15,  35,  70,  121,  185,  255,  320,  365,  381,  365,  320,
    255,  185,  121,  70,  35,  15,  5,  1]

\>cw=countways(3:18,3,6)


    [1,  3,  6,  10,  15,  21,  25,  27,  27,  25,  21,  15,  10,  6,  3,
    1]

Kami menambahkan nilai yang diharapkan ke plot.


\>plot2d(cw/6^3\*1000,\>add); plot2d(cw/6^3\*1000,\>points,\>add):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-040.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-040.png)

Untuk simulasi lainnya, deviasi nilai rata-rata dari n variabel acak
berdistribusi normal 0-1 adalah 1/sqrt(n).


\>longformat; 1/sqrt(10)


    0.316227766017

Mari kita periksa hal ini dengan sebuah simulasi. Kami menghasilkan
10.000 kali 10 vektor acak.


\>M=normal(10000,10); dev(mean(M)')


    0.318168725546

\>plot2d(mean(M)',\>distribution):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-041.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-041.png)

Median dari 10 bilangan acak berdistribusi normal 0-1 memiliki deviasi
yang lebih besar.


\>dev(median(M)')


    0.375058811006

Karena kita dapat dengan mudah menghasilkan jalan acak, kita dapat
mensimulasikan proses Wiener. Kami mengambil 1000 langkah dari 1000
proses. Kami kemudian memplot deviasi standar dan rata-rata dari
langkah ke-n dari proses-proses ini bersama dengan nilai yang
diharapkan dalam warna merah.


\>n=1000; m=1000; M=cumsum(normal(n,m)/sqrt(m)); ...  
\>   t=(1:n)/n; figure(2,1); ...  
\>   figure(1); plot2d(t,mean(M')'); plot2d(t,0,color=red,\>add); ...  
\>   figure(2); plot2d(t,dev(M')'); plot2d(t,sqrt(t),color=red,\>add); ...  
\>   figure(0):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-042.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-042.png)

# Tes

Tes adalah alat yang penting dalam statistik. Dalam Euler, banyak tes
yang diterapkan. Semua tes ini mengembalikan kesalahan yang kita
terima jika kita menolak hipotesis nol.


Sebagai contoh, kita menguji lemparan dadu untuk distribusi yang
seragam. Pada 600 lemparan, kita mendapatkan nilai berikut, yang kita
masukkan ke dalam uji chi-kuadrat.


\>chitest([90,103,114,101,103,89],dup(100,6)')


    0.498830517952

Uji chi-square juga memiliki mode, yang menggunakan simulasi Monte
Carlo untuk menguji statistik. Hasilnya seharusnya hampir sama.
Parameter &gt;p menginterpretasikan vektor y sebagai vektor probabilitas.


\>chitest([90,103,114,101,103,89],dup(1/6,6)',\>p,\>montecarlo)


    0.521

Kesalahan ini terlalu besar. Jadi kita tidak bisa menolak distribusi
seragam. Ini tidak membuktikan bahwa dadu kita adil. Tetapi kita tidak
bisa menolak hipotesis kita.


Selanjutnya kita buat 1000 lemparan dadu dengan menggunakan generator
bilangan acak, dan lakukan pengujian yang sama.


\>n=1000; t=random([1,n\*6]); chitest(count(t\*6,6),dup(n,6)')


    0.704302790658

Mari kita uji nilai rata-rata 100 dengan uji-t.


\>s=200+normal([1,100])\*10; ...  
\>   ttest(mean(s),dev(s),100,200)


    0.351598518865

Fungsi ttest() membutuhkan nilai rata-rata, deviasi, jumlah data, dan
nilai rata-rata untuk diuji.


Sekarang mari kita periksa dua pengukuran untuk mean yang sama. Kita
tolak hipotesis bahwa kedua pengukuran tersebut memiliki nilai
rata-rata yang sama, jika hasilnya &lt; 0,05.


\>tcomparedata(normal(1,10),normal(1,10))


    0.00141562352977

Jika kita menambahkan bias pada satu distribusi, kita akan mendapatkan
lebih banyak penolakan. Ulangi simulasi ini beberapa kali untuk
melihat efeknya.


\>tcomparedata(normal(1,10),normal(1,10)+2)


    0.00719460163986

Pada contoh berikut, kita membuat 20 lemparan dadu secara acak
sebanyak 100 kali dan menghitung jumlah dadu yang muncul. Rata-rata
harus ada 20/6 = 3,3 mata dadu.


\>R=random(100,20); R=sum(R\*6<=1)'; mean(R)


    3.07

Sekarang kita bandingkan jumlah satu dengan distribusi binomial.
Pertama, kita memplot distribusi angka satu.


\>plot2d(R,distribution=max(R)+1,even=1,style="\\/"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-043.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-043.png)

\>t=count(R,21);


Kemudian kami menghitung nilai yang diharapkan.


\>n=0:20; b=bin(20,n)\*(1/6)^n\*(5/6)^(20-n)\*100;


Kami harus mengumpulkan beberapa angka untuk mendapatkan kategori yang
cukup besar.


\>t1=sum(t[1:2])|t[3:7]|sum(t[8:21]); ...  
\>   b1=sum(b[1:2])|b[3:7]|sum(b[8:21]);


Uji chi-square menolak hipotesis bahwa distribusi kita adalah
distribusi binomial, jika hasilnya &lt;0,05.


\>chitest(t1,b1)


    0.404163936278

Contoh berikut ini berisi hasil dari dua kelompok orang (laki-laki dan
perempuan, katakanlah) yang memberikan suara untuk satu dari enam
partai.


\>A=[23,37,43,52,64,74;27,39,41,49,63,76];  ...  
\>     writetable(A,wc=6,labr=["m","f"],labc=1:6)


               1     2     3     4     5     6
         m    23    37    43    52    64    74
         f    27    39    41    49    63    76

We wish to test for independence of the votes from the sex. The chi^2
table test does this. The result is way to large to reject
independence. So we cannot say, if the voting depends on the sex from
these data.


\>tabletest(A)


    0.990701632326

Berikut ini adalah tabel yang diharapkan, jika kita mengasumsikan
frekuensi pemungutan suara yang diamati.


\>writetable(expectedtable(A),wc=6,dc=1,labr=["m","f"],labc=1:6)


               1     2     3     4     5     6
         m  24.9  37.9  41.9  50.3  63.3  74.7
         f  25.1  38.1  42.1  50.7  63.7  75.3

Kita dapat menghitung koefisien kontingensi yang telah dikoreksi.
Karena koefisien ini sangat dekat dengan 0, kami menyimpulkan bahwa
pemungutan suara tidak bergantung pada jenis kelamin.


\>contingency(A)


    0.0427225484717

# Beberapa Tes Lainnya

Selanjutnya kita menggunakan analisis varians (uji F) untuk menguji
tiga sampel data yang terdistribusi secara normal dengan nilai
rata-rata yang sama. Metode ini disebut ANOVA (analisis varians).
Dalam Euler, fungsi varanalysis() digunakan.


\>x1=[109,111,98,119,91,118,109,99,115,109,94]; mean(x1),


    106.545454545

\>x2=[120,124,115,139,114,110,113,120,117]; mean(x2),


    119.111111111

\>x3=[120,112,115,110,105,134,105,130,121,111]; mean(x3)


    116.3

\>varanalysis(x1,x2,x3)


    0.0138048221371

Ini berarti, kami menolak hipotesis nilai rata-rata yang sama. Kami
melakukan ini dengan probabilitas kesalahan sebesar 1,3%.


Ada juga uji median, yang menolak sampel data dengan distribusi
rata-rata yang berbeda dengan menguji median dari sampel gabungan.


\>a=[56,66,68,49,61,53,45,58,54];

\>b=[72,81,51,73,69,78,59,67,65,71,68,71];

\>mediantest(a,b)


    0.0241724220052

Uji lain tentang kesetaraan adalah uji peringkat. Uji ini jauh lebih
tajam daripada uji median.


\>ranktest(a,b)


    0.00199969612469

Dalam contoh berikut ini, kedua distribusi memiliki rata-rata yang
sama.


\>ranktest(random(1,100),random(1,50)\*3-1)


    0.218457593705

Sekarang mari kita coba mensimulasikan dua perawatan a dan b yang
diterapkan pada orang yang berbeda.


\>a=[8.0,7.4,5.9,9.4,8.6,8.2,7.6,8.1,6.2,8.9];

\>b=[6.8,7.1,6.8,8.3,7.9,7.2,7.4,6.8,6.8,8.1];


Uji signum memutuskan, apakah a lebih baik daripada b.


\>signtest(a,b)


    0.0546875

Ini adalah kesalahan yang terlalu besar. Kita tidak dapat menolak
bahwa a sama baiknya dengan b.


Uji Wilcoxon lebih tajam daripada uji ini, tetapi bergantung pada
nilai kuantitatif dari perbedaan.


\>wilcoxon(a,b)


    0.0296680599405

Mari kita coba dua pengujian lagi dengan menggunakan rangkaian yang
dihasilkan.


\>wilcoxon(normal(1,20),normal(1,20)-1)


    0.000258357561928

\>wilcoxon(normal(1,20),normal(1,20))


    0.588619799108

# Bilangan Acak

Berikut ini adalah tes untuk generator bilangan acak. Euler
menggunakan generator yang sangat bagus, jadi kita tidak perlu
mengharapkan adanya masalah.


Pertama, kita akan membangkitkan sepuluh juta bilangan acak dalam
[0,1].


\>n:=10000000; r:=random(1,n);


Selanjutnya, kami menghitung jarak antara dua angka yang kurang dari
0,05.


\>a:=0.05; d:=differences(nonzeros(r<a));


Terakhir, kami memplot berapa kali, setiap jarak yang terjadi, dan
membandingkannya dengan nilai yang diharapkan.


\>m=getmultiplicities(1:100,d); plot2d(m); ...  
\>     plot2d("n\*(1-a)^(x-1)\*a^2",color=red,\>add):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-044.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-044.png)

Bersihkan data.


\>remvalue n;


# Pengantar untuk Pengguna Proyek R

Jelas, EMT tidak bersaing dengan R sebagai sebuah paket statistik.
Namun, ada banyak prosedur dan fungsi statistik yang tersedia di EMT
juga. Jadi EMT dapat memenuhi kebutuhan dasar. Bagaimanapun, EMT hadir
dengan paket numerik dan sistem aljabar komputer.


Buku ini diperuntukkan bagi Anda yang sudah terbiasa dengan R, tetapi
perlu mengetahui perbedaan sintaks EMT dan R. Kami mencoba memberikan
gambaran umum mengenai hal-hal yang jelas dan kurang jelas yang perlu
Anda ketahui.


Selain itu, kami juga membahas cara-cara untuk bertukar data di antara
kedua sistem tersebut.


Note that this is a work in progress.


# Sintaks Dasar

Hal pertama yang Anda pelajari dalam R adalah membuat sebuah vektor.
Dalam EMT, perbedaan utamanya adalah operator : dapat mengambil ukuran
langkah. Selain itu, operator ini memiliki daya ikat yang rendah.


\>n=10; 0:n/20:n-1


    [0,  0.5,  1,  1.5,  2,  2.5,  3,  3.5,  4,  4.5,  5,  5.5,  6,  6.5,
    7,  7.5,  8,  8.5,  9]

Fungsi c() tidak ada. Anda dapat menggunakan vektor untuk
menggabungkan beberapa hal.


Contoh berikut ini, seperti banyak contoh lainnya, berasal dari
“Interoduksi ke R” yang disertakan dengan proyek R. Jika Anda membaca
PDF ini, Anda akan menemukan bahwa saya mengikuti alurnya dalam
tutorial ini.


\>x=[10.4, 5.6, 3.1, 6.4, 21.7]; [x,0,x]


    [10.4,  5.6,  3.1,  6.4,  21.7,  0,  10.4,  5.6,  3.1,  6.4,  21.7]

Operator titik dua dengan ukuran langkah EMT digantikan oleh fungsi
seq() dalam R. Kita dapat menulis fungsi ini dalam EMT.


\>function seq(a,b,c) := a:b:c; ...  
\>   seq(0,-0.1,-1)


    [0,  -0.1,  -0.2,  -0.3,  -0.4,  -0.5,  -0.6,  -0.7,  -0.8,  -0.9,  -1]

Fungsi rep() dari R tidak ada dalam EMT. Untuk input vektor, dapat
dituliskan sebagai berikut.


\>function rep(x:vector,n:index) := flatten(dup(x,n)); ...  
\>   rep(x,2)


    [10.4,  5.6,  3.1,  6.4,  21.7,  10.4,  5.6,  3.1,  6.4,  21.7]

Perhatikan bahwa “=” atau “:=” digunakan untuk penugasan. Operator
“-&gt;” digunakan untuk unit dalam EMT.


\>125km -\> " miles"


    77.6713990297 miles

Operator “&lt;-” untuk penugasan menyesatkan, dan bukan ide yang baik
untuk R. Berikut ini akan membandingkan a dan -4 dalam EMT.


\>a=2; a<-4


    0

Dalam R, “a&lt;-4&lt;3” bisa digunakan, tetapi “a&lt;-4&lt;-3” tidak. Saya juga
mengalami ambiguitas yang sama di EMT, tetapi saya mencoba untuk
menghilangkannya.


EMT dan R memiliki vektor dengan tipe boolean. Tetapi dalam EMT, angka
0 dan 1 digunakan untuk merepresentasikan salah dan benar. Dalam R,
nilai benar dan salah tetap dapat digunakan dalam aritmatika biasa
seperti dalam EMT.


\>x<5, %\*x


    [0,  0,  1,  0,  0]
    [0,  0,  3.1,  0,  0]

EMT melempar kesalahan atau menghasilkan NAN tergantung pada flag
“kesalahan”.


\>errors off; 0/0, isNAN(sqrt(-1)), errors on;


    NAN
    1

String sama saja dalam R dan EMT. Keduanya berada di lokal saat ini,
bukan di Unicode.


Dalam R ada paket-paket untuk Unicode. Dalam EMT, sebuah string dapat
berupa string Unicode. Sebuah string Unicode dapat diterjemahkan ke
pengkodean lokal dan sebaliknya. Selain itu, u“...” dapat berisi
entitas HTML.


\>u"&#169; Ren&eacut; Grothmann"


    © René Grothmann

Berikut ini mungkin atau mungkin tidak ditampilkan dengan benar pada
sistem Anda sebagai A dengan titik dan tanda hubung di atasnya. Hal
ini tergantung pada jenis huruf yang Anda gunakan.


\>chartoutf([480])


    Ǡ

Penggabungan string dilakukan dengan “+” atau “|”. Ini dapat
menyertakan angka, yang akan dicetak dalam format saat ini.


\>"pi = "+pi


    pi = 3.14159265359

# Pengindeksan

Sebagian besar waktu, ini akan bekerja seperti pada R.


Tetapi EMT akan menginterpretasikan indeks negatif dari bagian
belakang vektor, sementara R menginterpretasikan x[n] sebagai x tanpa
elemen ke-n.


\>x, x[1:3], x[-2]


    [10.4,  5.6,  3.1,  6.4,  21.7]
    [10.4,  5.6,  3.1]
    6.4

Perilaku R dapat dicapai dalam EMT dengan drop().


\>drop(x,2)


    [10.4,  3.1,  6.4,  21.7]

Vektor logika tidak diperlakukan secara berbeda dengan indeks di EMT,
berbeda dengan R. Anda harus mengekstrak elemen-elemen yang bukan nol
terlebih dahulu di EMT.


\>x, x\>5, x[nonzeros(x\>5)]


    [10.4,  5.6,  3.1,  6.4,  21.7]
    [1,  1,  0,  1,  1]
    [10.4,  5.6,  6.4,  21.7]

Sama seperti di R, vektor indeks dapat berisi pengulangan.


\>x[[1,2,2,1]]


    [10.4,  5.6,  5.6,  10.4]

Namun pemberian nama untuk indeks tidak dimungkinkan dalam EMT. Untuk
paket statistik, hal ini mungkin sering diperlukan untuk memudahkan
akses ke elemen-elemen vektor.


Untuk meniru perilaku ini, kita dapat mendefinisikan sebuah fungsi
sebagai berikut.


\>function sel (v,i,s) := v[indexof(s,i)]; ...  
\>   s=["first","second","third","fourth"]; sel(x,["first","third"],s)


    
    Trying to overwrite protected function sel!
    Error in:
    function sel (v,i,s) := v[indexof(s,i)]; ... ...
                 ^
    [10.4,  3.1]

# Tipe Data

EMT memiliki lebih banyak tipe data yang tetap dibandingkan R. Jelas,
dalam R terdapat vektor yang berkembang. Anda bisa mengatur sebuah
vektor numerik kosong v dan memberikan sebuah nilai pada elemen v[17].
Hal ini tidak mungkin dilakukan dalam EMT.


Hal berikut ini sedikit tidak efisien.


\>v=[]; for i=1 to 10000; v=v|i; end;


EMT sekarang akan membuat vektor dengan v dan i yang ditambahkan pada
tumpukan dan menyalin vektor tersebut kembali ke variabel global v.


Semakin efisien mendefinisikan vektor.


\>v=zeros(10000); for i=1 to 10000; v[i]=i; end;


Untuk mengubah jenis tanggal di EMT, Anda dapat menggunakan fungsi
seperti complex().


\>complex(1:4)


    [ 1+0i ,  2+0i ,  3+0i ,  4+0i  ]

Konversi ke string hanya dapat dilakukan untuk tipe data dasar. Format
saat ini digunakan untuk penggabungan string sederhana. Tetapi ada
fungsi-fungsi seperti print() atau frac().


Untuk vektor, Anda dapat dengan mudah menulis fungsi Anda sendiri.


\>function tostr (v) ...


    s="[";
    loop 1 to length(v);
       s=s+print(v[#],2,0);
       if #<length(v) then s=s+","; endif;
    end;
    return s+"]";
    endfunction
</pre>
\>tostr(linspace(0,1,10))


    [0.00,0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.90,1.00]

Untuk komunikasi dengan Maxima, ada sebuah fungsi convertmxm(), yang
juga dapat digunakan untuk memformat vektor untuk output.


\>convertmxm(1:10)


    [1,2,3,4,5,6,7,8,9,10]

Untuk Latex, perintah tex dapat digunakan untuk mendapatkan perintah
Latex.


\>tex(&[1,2,3])


    \left[ 1 , 2 , 3 \right] 

# Faktor dan Tabel

Pada pengantar R terdapat sebuah contoh dengan apa yang disebut
faktor.


Berikut ini adalah daftar wilayah dari 30 negara bagian.


\>austates = ["tas", "sa", "qld", "nsw", "nsw", "nt", "wa", "wa", ...  
\>   "qld", "vic", "nsw", "vic", "qld", "qld", "sa", "tas", ...  
\>   "sa", "nt", "wa", "vic", "qld", "nsw", "nsw", "wa", ...  
\>   "sa", "act", "nsw", "vic", "vic", "act"];


Asumsikan, kita memiliki pendapatan yang sesuai di setiap negara
bagian.


\>incomes = [60, 49, 40, 61, 64, 60, 59, 54, 62, 69, 70, 42, 56, ...  
\>   61, 61, 61, 58, 51, 48, 65, 49, 49, 41, 48, 52, 46, ...  
\>   59, 46, 58, 43];


Sekarang, kita ingin menghitung rata-rata pendapatan di wilayah
tersebut. Sebagai sebuah program statistik, R memiliki fungsi factor()
dan tappy() untuk hal ini.


EMT dapat melakukan hal ini dengan mencari indeks dari wilayah-wilayah
di dalam daftar unik dari wilayah-wilayah tersebut.


\>auterr=sort(unique(austates)); f=indexofsorted(auterr,austates)


    [6,  5,  4,  2,  2,  3,  8,  8,  4,  7,  2,  7,  4,  4,  5,  6,  5,  3,
    8,  7,  4,  2,  2,  8,  5,  1,  2,  7,  7,  1]

Pada titik ini, kita dapat menulis fungsi perulangan kita sendiri
untuk melakukan berbagai hal untuk satu faktor saja.


Atau kita dapat meniru fungsi tapply() dengan cara berikut.


\>function map tappl (i; f$:call, cat, x) ...


    u=sort(unique(cat));
    f=indexof(u,cat);
    return f$(x[nonzeros(f==indexof(u,i))]);
    endfunction
</pre>
Ini sedikit tidak efisien, karena menghitung wilayah unik untuk setiap
i, tetapi berfungsi.


\>tappl(auterr,"mean",austates,incomes)


    [44.5,  57.3333333333,  55.5,  53.6,  55,  60.5,  56,  52.25]

Perhatikan bahwa ini bekerja untuk setiap vektor wilayah.


\>tappl(["act","nsw"],"mean",austates,incomes)


    [44.5,  57.3333333333]

Sekarang, paket statistik EMT mendefinisikan tabel seperti halnya di
R. Fungsi readtable() dan writetable() dapat digunakan untuk input dan
output.


Jadi kita dapat mencetak rata-rata pendapatan negara di wilayah dengan
cara yang ramah.


\>writetable(tappl(auterr,"mean",austates,incomes),labc=auterr,wc=7)


        act    nsw     nt    qld     sa    tas    vic     wa
       44.5  57.33   55.5   53.6     55   60.5     56  52.25

Kita juga dapat mencoba meniru perilaku R sepenuhnya.


Faktor-faktor tersebut harus disimpan dengan jelas dalam sebuah
koleksi dengan jenis dan kategorinya (negara bagian dan wilayah dalam
contoh kita). Untuk EMT, kita menambahkan indeks yang telah dihitung
sebelumnya.


\>function makef (t) ...


    ## Factor data
    ## Returns a collection with data t, unique data, indices.
    ## See: tapply
    u=sort(unique(t));
    return {{t,u,indexofsorted(u,t)}};
    endfunction
</pre>
\>statef=makef(austates);


Sekarang elemen ketiga dari koleksi ini akan berisi indeks.


\>statef[3]


    [6,  5,  4,  2,  2,  3,  8,  8,  4,  7,  2,  7,  4,  4,  5,  6,  5,  3,
    8,  7,  4,  2,  2,  8,  5,  1,  2,  7,  7,  1]

Sekarang kita dapat meniru tapply() dengan cara berikut. Ini akan
mengembalikan sebuah tabel sebagai kumpulan data tabel dan judul
kolom.


\>function tapply (t:vector,tf,f$:call) ...


    ## Makes a table of data and factors
    ## tf : output of makef()
    ## See: makef
    uf=tf[2]; f=tf[3]; x=zeros(length(uf));
    for i=1 to length(uf);
       ind=nonzeros(f==i);
       if length(ind)==0 then x[i]=NAN;
       else x[i]=f$(t[ind]);
       endif;
    end;
    return {{x,uf}};
    endfunction
</pre>
Kami tidak menambahkan banyak pemeriksaan tipe di sini. Satu-satunya
tindakan pencegahan adalah kategori (faktor) yang tidak memiliki data.
Tetapi kita harus memeriksa panjang t yang benar dan kebenaran koleksi
tf.


Tabel ini bisa dicetak sebagai sebuah tabel dengan writetable().


\>writetable(tapply(incomes,statef,"mean"),wc=7)


        act    nsw     nt    qld     sa    tas    vic     wa
       44.5  57.33   55.5   53.6     55   60.5     56  52.25

# Larik

EMT hanya memiliki dua dimensi untuk array. Tipe datanya disebut
matriks. Akan lebih mudah untuk menulis fungsi untuk dimensi yang
lebih tinggi atau sebuah pustaka C untuk ini.


R memiliki lebih dari dua dimensi. Dalam R, larik adalah sebuah vektor
dengan sebuah bidang dimensi.


Dalam EMT, sebuah vektor adalah sebuah matriks dengan satu baris. Ini
bisa dibuat menjadi sebuah matriks dengan redim().


\>shortformat; X=redim(1:20,4,5)


            1         2         3         4         5 
            6         7         8         9        10 
           11        12        13        14        15 
           16        17        18        19        20 

Ekstraksi baris dan kolom, atau sub-matriks, sama seperti di R.


\>X[,2:3]


            2         3 
            7         8 
           12        13 
           17        18 

Namun, dalam R dimungkinkan untuk mengatur daftar indeks tertentu dari
vektor ke suatu nilai. Hal yang sama juga dapat dilakukan dalam EMT
hanya dengan sebuah perulangan.


\>function setmatrixvalue (M, i, j, v) ...


    loop 1 to max(length(i),length(j),length(v))
       M[i{#},j{#}] = v{#};
    end;
    endfunction
</pre>
Kami mendemonstrasikan hal ini untuk menunjukkan bahwa matriks
diteruskan dengan referensi dalam EMT. Jika Anda tidak ingin mengubah
matriks asli M, Anda perlu menyalinnya dalam fungsi.


\>setmatrixvalue(X,1:3,3:-1:1,0); X,


            1         2         0         4         5 
            6         0         8         9        10 
            0        12        13        14        15 
           16        17        18        19        20 

Hasil kali luar dalam EMT hanya dapat dilakukan di antara vektor. Hal
ini otomatis karena bahasa matriks. Satu vektor harus berupa vektor
kolom dan vektor baris.


\>(1:5)\*(1:5)'


            1         2         3         4         5 
            2         4         6         8        10 
            3         6         9        12        15 
            4         8        12        16        20 
            5        10        15        20        25 

Dalam pengantar PDF untuk R ada sebuah contoh, yang menghitung
distribusi ab-cd untuk a, b, c, d yang dipilih dari 0 sampai n secara
acak. Solusinya dalam R adalah membentuk sebuah matriks 4 dimensi dan
menjalankan table() di atasnya.


Tentu saja, ini bisa dicapai dengan sebuah perulangan. Tetapi
perulangan tidak efektif dalam EMT atau R. Dalam EMT, kita bisa
menulis perulangan dalam C dan itu adalah solusi tercepat.


Tetapi kita ingin meniru perilaku R. Untuk ini, kita perlu meratakan
perkalian ab dan membuat sebuah matriks ab-cd.


Translated with DeepL.com (free version)


\>a=0:6; b=a'; p=flatten(a\*b); q=flatten(p-p'); ...  
\>   u=sort(unique(q)); f=getmultiplicities(u,q); ...  
\>   statplot(u,f,"h"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-045.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-045.png)

Selain kelipatan yang tepat, EMT dapat menghitung frekuensi dalam
vektor.


\>getfrequencies(q,-50:10:50)


    [0,  23,  132,  316,  602,  801,  333,  141,  53,  0]

Cara yang paling mudah untuk memplot ini sebagai distribusi adalah
sebagai berikut.


\>plot2d(q,distribution=11):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-046.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-046.png)

Tetapi juga memungkinkan untuk menghitung jumlah dalam interval yang
dipilih sebelumnya. Tentu saja, berikut ini menggunakan
getfrequencies() secara internal.


Karena fungsi histo() mengembalikan frekuensi, kita perlu
menskalakannya sehingga integral di bawah grafik batang adalah 1.


\>{x,y}=histo(q,v=-55:10:55); y=y/sum(y)/differences(x); ...  
\>   plot2d(x,y,\>bar,style="/"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-047.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-047.png)

# Daftar

EMT memiliki dua jenis daftar. Pertama adalah daftar global yang dapat
diubah, dan yang kedua adalah jenis daftar yang tidak dapat diubah.
Kita tidak peduli dengan daftar global di sini.


Tipe daftar yang tidak dapat diubah disebut koleksi dalam EMT. Ia
berperilaku seperti struktur dalam C, tetapi elemen-elemennya hanya
diberi nomor dan tidak diberi nama.


\>L={{"Fred","Flintstone",40,[1990,1992]}}


    Fred
    Flintstone
    40
    [1990,  1992]

Saat ini elemen-elemen tersebut tidak memiliki nama, meskipun nama
dapat ditetapkan untuk tujuan khusus. Elemen-elemen tersebut diakses
dengan angka.


\>(L[4])[2]


    1992

# Input dan Output File (Membaca dan Menulis Data)

Anda mungkin sering ingin mengimpor matriks data dari sumber lain ke
EMT. Tutorial ini akan menjelaskan kepada Anda tentang berbagai cara
untuk melakukan hal tersebut. Fungsi yang sederhana adalah
writematrix() dan readmatrix().


Mari kita tunjukkan bagaimana cara membaca dan menulis sebuah vektor
real ke sebuah file.


\>a=random(1,100); mean(a), dev(a),


    0.49807
    0.29665

Untuk menulis data ke sebuah berkas, kita menggunakan fungsi
writematrix().


Karena pengenalan ini kemungkinan besar berada di sebuah direktori, di
mana pengguna tidak memiliki akses tulis, kita menulis data ke
direktori home pengguna. Untuk notebook sendiri, hal ini tidak
diperlukan, karena file data akan ditulis ke dalam direktori yang
sama.


\>filename="test.dat";


Sekarang kita tuliskan vektor kolom a' ke dalam file. Hal ini akan
menghasilkan satu angka pada setiap baris file.


\>writematrix(a',filename);


Untuk membaca datanya, kita menggunakan readmatrix().


\>a=readmatrix(filename)';


Hapus file ini.


\>fileremove(filename);

\>mean(a), dev(a),


    0.49807
    0.29665

Fungsi writematrix() atau writetable() dapat dikonfigurasi untuk
bahasa lain.


Sebagai contoh, jika Anda memiliki sistem bahasa Indonesia (titik
desimal dengan koma), Excel Anda membutuhkan nilai dengan koma desimal
yang dipisahkan oleh titik koma dalam file csv (defaultnya adalah
nilai yang dipisahkan dengan koma). File “test.csv” berikut ini akan
muncul di folder cuurent Anda.


\>filename="test.csv"; ...  
\>   writematrix(random(5,3),file=filename,separator=",");


Anda sekarang dapat membuka file ini dengan Excel Indonesia secara
langsung.


\>fileremove(filename);


Terkadang kita memiliki string dengan token seperti berikut ini.


\>s1:="f m m f m m m f f f m m f";  ...  
\>   s2:="f f f m m f f";


Untuk menandai ini, kita mendefinisikan vektor token.


\>tok:=["f","m"]


    f
    m

Kemudian kita dapat menghitung berapa kali setiap token muncul dalam
string, dan memasukkan hasilnya ke dalam tabel.


\>M:=getmultiplicities(tok,strtokens(s1))\_ ...  
\>     getmultiplicities(tok,strtokens(s2));


Tulis tabel dengan tajuk token.


\>writetable(M,labc=tok,labr=1:2,wc=8)


                   f       m
           1       6       7
           2       5       2

Untuk statika, EMT dapat membaca dan menulis tabel.


\>file="test.dat"; open(file,"w"); ...  
\>   writeln("A,B,C"); writematrix(random(3,3)); ...  
\>   close();


File akan terlihat seperti ini.


\>printfile(file)


    A,B,C
    0.05192095433048956,0.4915301374998231,0.3270781826235566
    0.5036807371363335,0.3568577819191439,0.8126814999049192
    0.4596446263928866,0.01234816948398687,0.3893948072095209
    

Fungsi readtable() dalam bentuknya yang paling sederhana dapat membaca
ini dan mengembalikan sebuah koleksi nilai dan baris judul.


\>L=readtable(file,\>list);


Koleksi ini dapat dicetak dengan writetable() ke buku catatan, atau ke
sebuah file.


\>writetable(L,wc=10,dc=5)


               Flintstone
          1990Can only use one index for strings or string vectors!
    Try "trace errors" to inspect local variables after errors.
    writetable:
        if x[i,j]==NAval then

Matriks nilai adalah elemen pertama dari L. Perhatikan bahwa mean()
dalam EMT menghitung nilai rata-rata dari baris-baris matriks.


\>mean(L[1])


    Function mean needs a numerical type for x
    Error in:
    mean(L[1]) ...
              ^

# File CSV

Pertama, mari kita tulis sebuah matriks ke dalam sebuah file. Untuk
keluarannya, kami membuat file di direktori kerja saat ini.


\>file="test.csv";  ...  
\>   M=random(3,3); writematrix(M,file);


Ini adalah ini dari file tersebut.


\>printfile(file)


    0.9224484830201236,0.4379570736672502,0.5843973451637543
    0.1684144094191607,0.9442599663800081,0.1638450566338514
    0.2363725426102365,0.1576648505411634,0.7660642164365661
    

CVS ini dapat dibuka di sistem bahasa Inggris ke Excel dengan klik dua
kali. Jika Anda mendapatkan file seperti itu pada sistem Jerman, Anda
perlu mengimpor data ke Excel dengan memperhatikan titik desimal.


Namun, titik desimal juga merupakan format default untuk EMT. Anda
dapat membaca sebuah matriks dari sebuah file dengan readmatrix().


\>readmatrix(file)


      0.92245   0.43796    0.5844 
      0.16841   0.94426   0.16385 
      0.23637   0.15766   0.76606 

Dimungkinkan untuk menulis beberapa matriks ke dalam satu file.
Perintah open() dapat membuka file untuk menulis dengan parameter “w”.
Standarnya adalah “r” untuk membaca.


\>open(file,"w"); writematrix(M); writematrix(M'); close();


Matriks-matriks tersebut dipisahkan oleh sebuah baris kosong. Untuk
membaca matriks, buka file dan panggil readmatrix() beberapa kali.


\>open(file); A=readmatrix(); B=readmatrix(); A==B, close();


            1         0         0 
            0         1         0 
            0         0         1 

Di Excel atau spreadsheet serupa, Anda dapat mengekspor matriks
sebagai CSV (nilai yang dipisahkan dengan koma). Pada Excel 2007,
gunakan “simpan sebagai” dan “format lain”, lalu pilih “CSV”.
Pastikan, tabel saat ini hanya berisi data yang ingin Anda ekspor.


Berikut ini adalah contohnya.


\>printfile("excel-data.csv")


    0;1000;1000
    1;1051,271096;1072,508181
    2;1105,170918;1150,273799
    3;1161,834243;1233,67806
    4;1221,402758;1323,129812
    5;1284,025417;1419,067549
    6;1349,858808;1521,961556
    7;1419,067549;1632,31622
    8;1491,824698;1750,6725
    9;1568,312185;1877,610579
    10;1648,721271;2013,752707

Seperti yang Anda lihat, sistem Jerman saya menggunakan titik koma
sebagai pemisah dan koma desimal. Anda dapat mengubahnya di pengaturan
sistem atau di Excel, tetapi tidak perlu untuk membaca matriks ke
dalam EMT.


Cara termudah untuk membaca ini ke dalam Euler adalah readmatrix().
Semua koma digantikan oleh titik dengan parameter &gt;comma. Untuk CSV
bahasa Inggris, hilangkan saja parameter ini.


\>M=readmatrix("excel-data.csv",\>comma)


            0      1000      1000 
            1    1051.3    1072.5 
            2    1105.2    1150.3 
            3    1161.8    1233.7 
            4    1221.4    1323.1 
            5      1284    1419.1 
            6    1349.9      1522 
            7    1419.1    1632.3 
            8    1491.8    1750.7 
            9    1568.3    1877.6 
           10    1648.7    2013.8 

Mari buat plotnya.


\>plot2d(M'[1],M'[2:3],\>points,color=[red,green]'):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-048.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-048.png)

Ada beberapa cara yang lebih mendasar untuk membaca data dari file.
Anda dapat membuka file dan membaca angka baris demi baris. Fungsi
getvectorline() akan membaca angka dari sebuah baris data. Secara
default, fungsi ini mengharapkan sebuah titik desimal. Tetapi fungsi
ini juga dapat menggunakan koma desimal, jika Anda memanggil
setdecimaldot(“,”) sebelum menggunakan fungsi ini.


Fungsi berikut ini adalah contohnya. Fungsi ini akan berhenti pada
akhir file atau baris kosong.


\>function myload (file) ...


    open(file);
    M=[];
    repeat
       until eof();
       v=getvectorline(3);
       if length(v)>0 then M=M_v; else break; endif;
    end;
    return M;
    close(file);
    endfunction
</pre>
\>myload(file)


      0.92245   0.43796    0.5844 
      0.16841   0.94426   0.16385 
      0.23637   0.15766   0.76606 

Anda juga dapat membaca semua angka dalam file tersebut dengan
getvector().


\>open(file); v=getvector(10000); close(); redim(v[1:9],3,3)


      0.92245   0.43796    0.5844 
      0.16841   0.94426   0.16385 
      0.23637   0.15766   0.76606 

Dengan demikian, sangat mudah untuk menyimpan vektor nilai, satu nilai
di setiap baris dan membaca kembali vektor ini.


\>v=random(1000); mean(v)


    0.50126

\>writematrix(v',file); mean(readmatrix(file)')


    0.50126

# Menggunakan Tabel

Tabel dapat digunakan untuk membaca atau menulis data numerik. Sebagai
contoh, kita menulis tabel dengan judul baris dan kolom ke file.


\>file="test.tab"; M=random(3,3);  ...  
\>   open(file,"w");  ...  
\>   writetable(M,separator=",",labc=["one","two","three"]);  ...  
\>   close(); ...  
\>   printfile(file)


    one,two,three
          0.56,      0.45,      0.55
          0.14,      0.15,      0.99
          0.32,      0.44,       0.3

File ini dapat diimpor ke Excel.


Untuk membaca file di EMT, kita menggunakan readtable().


\>{M,headings}=readtable(file,\>clabs); ...  
\>   writetable(M,labc=headings)


           one       two     three
          0.56      0.45      0.55
          0.14      0.15      0.99
          0.32      0.44       0.3

# Menganalisis Garis

Anda bahkan dapat mengevaluasi setiap baris dengan tangan. Misalkan,
kita memiliki baris dengan format berikut.


\>line="2020-11-03,Tue,1'114.05"


    2020-11-03,Tue,1'114.05

Pertama, kita dapat memberi tanda pada garis tersebut.


\>vt=strtokens(line)


    2020-11-03
    Tue
    1'114.05

Kemudian, kita dapat mengevaluasi setiap elemen garis dengan
menggunakan evaluasi yang sesuai.


\>day(vt[1]),  ...  
\>   indexof(["mon","tue","wed","thu","fri","sat","sun"],tolower(vt[2])),  ...  
\>   strrepl(vt[3],"'","")()


    7.3816e+05
    2
    1114

Dengan menggunakan ekspresi reguler, Anda dapat mengekstrak hampir
semua informasi dari sebuah baris data.


Anggaplah kita memiliki baris dokumen HTML berikut ini.


\>line="<tr\><td\>1145.45</td\><td\>5.6</td\><td\>-4.5</td\><tr\>"


    &lt;tr&gt;&lt;td&gt;1145.45&lt;/td&gt;&lt;td&gt;5.6&lt;/td&gt;&lt;td&gt;-4.5&lt;/td&gt;&lt;tr&gt;

Untuk mengekstrak ini, kita menggunakan ekspresi reguler, yang mencari


- tanda kurung tutup &gt;,


 string apa pun yang tidak mengandung tanda kurung dengan
sub-pencocokan “(...)”,


 kurung pembuka dan kurung penutup menggunakan solusi terpendek,


 sekali lagi, semua string yang tidak mengandung tanda kurung,


 dan sebuah kurung pembuka &lt;.


Ekspresi reguler agak sulit untuk dipelajari tetapi sangat kuat.


\>{pos,s,vt}=strxfind(line,"\>([^<\>]+)<.+?\>([^<\>]+)<");


Hasilnya adalah posisi kecocokan, string yang cocok, dan vektor string
untuk sub-cocokan.


\>for k=1:length(vt); vt[k](), end;


    1145.5
    5.6

Berikut ini adalah fungsi yang membaca semua item numerik antara &lt;td&gt;
dan &lt;/td&gt;.


\>function readtd (line) ...


    v=[]; cp=0;
    repeat
       {pos,s,vt}=strxfind(line,"<td.*?>(.+?)</td>",cp);
       until pos==0;
       if length(vt)>0 then v=v|vt[1]; endif;
       cp=pos+strlen(s);
    end;
    return v;
    endfunction
</pre>
\>readtd(line+"<td\>non-numerical</td\>")


    1145.45
    5.6
    -4.5
    non-numerical

# Membaca dari Web

Situs web atau file dengan URL dapat dibuka di EMT dan dapat dibaca
baris demi baris.


Dalam contoh, kita membaca versi saat ini dari situs EMT. Kami
menggunakan ekspresi reguler untuk memindai “Versi ...” dalam judul.


\>function readversion () ...


    urlopen("http://www.euler-math-toolbox.de/Programs/Changes.html");
    repeat
      until urleof();
      s=urlgetline();
      k=strfind(s,"Version ",1);
      if k>0 then substring(s,k,strfind(s,"<",k)-1), break; endif;
    end;
    urlclose();
    endfunction
</pre>
\>readversion


    Version 2024-01-12

# Masukan dan Keluaran Variabel

Anda dapat menulis variabel dalam bentuk definisi Euler ke file atau
ke baris perintah.


\>writevar(pi,"mypi");


    mypi = 3.141592653589793;

Untuk pengujian, kami membuat file Euler di direktori kerja EMT.


\>file="test.e"; ...  
\>   writevar(random(2,2),"M",file); ...  
\>   printfile(file,3)


    M = [ ..
    0.6788474487615903, 0.1044046845633528;
    0.2032555347665774, 0.06053708733322678];

Sekarang kita dapat memuat file tersebut. Ini akan mendefinisikan
matriks M.


\>load(file); show M,


    M = 
      0.67885    0.1044 
      0.20326  0.060537 

Sebagai catatan, jika writevar() digunakan pada sebuah variabel, maka
ia akan mencetak definisi variabel dengan nama variabel tersebut.


\>writevar(M); writevar(inch$)


    M = [ ..
    0.6788474487615903, 0.1044046845633528;
    0.2032555347665774, 0.06053708733322678];
    inch$ = 0.0254;

Kita juga dapat membuka file baru atau menambahkan ke file yang sudah
ada. Dalam contoh ini, kami menambahkan ke file yang telah dibuat
sebelumnya.


\>open(file,"a"); ...  
\>   writevar(random(2,2),"M1"); ...  
\>   writevar(random(3,1),"M2"); ...  
\>   close();

\>load(file); show M1; show M2;


    M1 = 
      0.32271   0.18702 
      0.76022   0.13907 
    M2 = 
      0.70041 
      0.53494 
     0.070953 

To remove any files use fileremove().


\>fileremove(file);


Sebuah vektor baris dalam sebuah file tidak membutuhkan koma, jika
setiap angka berada dalam baris baru. Mari kita buat file seperti itu,
menulis setiap baris satu per satu dengan writeln().


\>open(file,"w"); writeln("M = ["); ...  
\>   for i=1 to 5; writeln(""+random()); end; ...  
\>   writeln("];"); close(); ...  
\>   printfile(file)


    M = [
    0.950746735471
    0.260536145952
    0.658151434242
    0.860839511813
    0.153523243987
    ];

\>load(file); M


    [0.95075,  0.26054,  0.65815,  0.86084,  0.15352]

# Contoh Latihan

* Grafik Statistika 


## Diagram kotak

\>A=[40,21,44,43,43,48,32,47]


    [40,  21,  44,  43,  43,  48,  32,  47]

\>boxplot(A):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-049.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-049.png)

\>P=[90,100,80,85,87,98,34,59,29,96,87,85,83,80]


    [90,  100,  80,  85,  87,  98,  34,  59,  29,  96,  87,  85,  83,  80]

\>boxplot(P):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-050.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-050.png)

Kuartil 1 (Q1 - 25%): 80.0


Kuartil 2 (Median - Q2 - 50%): 85.0


(median)


Kuartil 3 (Q3 - 75%): 89.25


mean: 78.07


max: 100


min: 29


## Diagram batang

\>januari=100; februari=90; 

\>columnsplot(cumsum(random(6))):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-051.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-051.png)

\>days=["senin","selasa","rabu","kamis","jumat","sabtu","minggu"];

\>values=[30,40,20,10,50,60,70];

\>columnsplot(values,lab=days,color=yellow);

\>title("penjualan warung"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-052.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-052.png)

\>month=["januari","februari","maret","april","mei","juni","juli","agustus","september","oktober","november","desember"];

\>values=[100,200,250,50,300,500,680,300,450,450,600,700];

\>columnsplot(values,lab=month,color=red);

\>title("penjualan gaje warung"):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-053.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-053.png)

## Diagram lingkaran

\>cp:=[rgb(0.5,0.5,0.5),red,yellow,green,rgb(0.9,0,0)]


    [5.87532e+07,  2,  15,  3,  6.54049e+07]

\>i=[1,2,3,4,5]


    [1,  2,  3,  4,  5]

\>piechart(values[i],color=cp[i],lab=month[i]):


![images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-054.png](images/Nur%20Muhammad%20Al%20Fahamiey_23030630058_EMTStatistika-054.png)

## Uji Korelasi Kontingensi

\>absenceGenders = [10,5;9,6]


               10             5 
                9             6 

Buat tabel agar mudah melihatnya


\>writetable(absenceGenders, wc = 10, labr=["Pria", "Wanita"], labc = ["Ikut", "Tidak"])


                    Ikut     Tidak
          Pria        10         5
        Wanita         9         6

Memeriksa tabel untuk uji chi-kuadratnya


\>tabletest(absenceGenders)


    0.704786173865

Karena nilai terlalu besar, maka belum bisa menyimpulkan apakah
terdapat hubungan antara keikutsertaan dengan gender


Lalu, dibuat tabel nilai harapan untuk melihat nilai harapan pada
tabel tersebut


\>writetable(expectedtable(absenceGenders), dc=1, wc=10, labr=["Pria", "Wanita"], labc=["Ikut", "Tidak"])


                    Ikut     Tidak
          Pria       9.5       5.5
        Wanita       9.5       5.5

Terakhir, adalah menghitung nilai koefisien kontingensi


\>contingency(absenceGenders)


    0.0975900072949

Karena nilai koefisien kontingensi mendekati 0, maka dapat disimpulkan
bahwa hubungan antara keikutsertaan dengan jenis kelamin tidak ada
(sangat lemah).


## Uji t

Berdasarkan 100 laporan kematian di AS yang diambil secara acak,
diperoleh bahwa rata-rata usia hidup orang AS adalah 71.8 tahun dengan
simpangan baku 8.9 tahun. Hal ini memberikan dugaan bahwa rata-rata
usia hidup orang AS lebih dari 70 tahun. Dengan taraf signifikansi 5%
ujilah kebenaran dugaan tersebut.


Penyelesaian


Rumusan Hipotesis


Parameter populasi yang akan diuji  disini adalah rata-rata hidup dari
populasi orang AS


$$\begin{array}{cc} \text{Hipotesis nol} & H_0: \mu\le 70. \\ \text{Hipotesis alternatif} & H_1: \mu > 70. \\ \end{array}$$\>nReport = 100; meanLifeExpect = 71.8; devLife = 8.9; meanLifeEstimate = 70;

\>ttest(meanLifeEstimate, devLife, nReport, meanLifeExpect)


    0.022912369887

$$t_{\text{hitung}} = \dfrac{\overline{x}-\mu_0}{s/\sqrt{n}} = \dfrac{71,\!8-70}{8,\!9/\sqrt{100}} \approx 2,\!02.$$Daerah kritis:


Uji yang dilakukan diatas merupakan uji satu arah (kanan). Dengan
menggunakan tabel-t, nilai-t, dengan taraf signifikansi 0.05 dan
derajat kebabasan n - 1 = 100 - 1 = 99, maka


$$t_{\text{tabel}} = t_{0,05; ~99} \approx 1,\!66.$$Dengan demikian, diperoleh bahwa daerah kritis terletak  di


$$t > 1,\!66.$$Keputusan:


Karena


$$t_{\text{hitung}} = 2,\!02 > 1,\!66 = t_{\text{tabel}},$$disimpulkan bahwa statistik uji akan terdapat pada daerah kritis.Degan
demikian hipotesis nol akan ditolak


Kesimpulan:


Dugaan bahwa rata-rata usia hidup orang AS lebih dari 70 tahun
diterima.


Kesimpulan dari fungsi:


Karena nilai t test &lt; 0.05, maka hipotesis nol akan ditolak


membandingkan nilai rata-rata dari dua distribusi yang berbeda, untuk
menghitung nilai error dari keduanya.


misalkan


diberikan distribusi pertama dengan distribusi Gauss-0-1 variabel acak
dengan banyaknya 10 begitu juga distribusi kedua


sedemikian sehingga


\>disOne = normal(1,10)


    [-0.49861,  -1.80528,  -0.350986,  0.618965,  -1.04209,  0.929849,
    -1.46048,  -0.28266,  -0.252612,  0.546577]

\>disTwo = normal(1,10)


    [-1.37955,  -0.164841,  -0.835865,  0.196176,  -0.495418,  1.6463,
    -0.390056,  -1.98151,  3.44132,  0.308178]

\>tcomparedata(disOne, disTwo)


    0.248213899937

Hasil diatas menunjukkan error dari perbedaan rata-rata dari
distribusi tersebut.


## Uji ANOVA

Terdapat tiga kelompok subjek penelitian untuk menguji metode
pengajaran mana yang paling baik dalam meningkatkan pembelajaran.
Metode pertama adalah ceramah, kedua adalah diskusi dan ketiga adalah
praktek


Penelitian tersebut menghasilkan data sebagai berikut.


Ceramah | Diskusi | Praktek


25      | 17      | 26


11      | 16      | 20


16      | 18      | 17


26      | 20      | 26


32      | 10      | 43


25      | 14      | 46


30      | 19      | 35


17                | 34


Penyelesaian


Rumusan Hipotesis


Parameter populasi yang akan diuji disini adalah hasil peningkatan
pembelajaran untuk metode-metode diatas


$$\begin{array}{cc} \text{Hipotesis nol} & H_0: m_i = 0, i = m_1, m_2, m_3 \\ \text{Hipotesis alternatif} & H_1: \text{setidaknya ada } m_i \ne 0 \\ \end{array}$$\>lecture = [25,11,16,26,32,25,30,17];

\>discuss = [17,16,18,20,10,14,19];

\>practice = [26,20,17,26,43,46,35,34];

\>varanalysis(lecture, discuss, practice)


    0.006052468478

karena hasil fungsi &lt; 0.05, maka kita tolak hipotesis nol, yang
artinya bahwa hasil peningkatan pembelajaran setelah melalui
metode-metode tersebut memiliki hasil yang berbeda.


## nilai acak

\>a=random(1,100)


    [0.914616,  0.739491,  0.445335,  0.122201,  0.253266,  0.437406,
    0.769867,  0.13904,  0.431159,  0.25174,  0.312421,  0.668159,
    0.0906142,  0.0795298,  0.091447,  0.756939,  0.0768507,  0.337977,
    0.144064,  0.189068,  0.510555,  0.2968,  0.812262,  0.0112935,
    0.412134,  0.491958,  0.239305,  0.63047,  0.780325,  0.259808,
    0.803298,  0.213349,  0.644852,  0.251652,  0.462119,  0.250842,
    0.667631,  0.683252,  0.115061,  0.50759,  0.246544,  0.817425,
    0.665396,  0.802732,  0.40999,  0.732504,  0.261977,  0.426526,
    0.226197,  0.318141,  0.674854,  0.507825,  0.817756,  0.237657,
    0.874048,  0.0889354,  0.698952,  0.216593,  0.883197,  0.761987,
    0.943352,  0.668347,  0.421187,  0.522053,  0.517532,  0.0583076,
    0.540146,  0.167618,  0.0631314,  0.898548,  0.894827,  0.33746,
    0.142055,  0.819197,  0.080668,  0.731151,  0.212862,  0.40939,
    0.235042,  0.174254,  0.292994,  0.618589,  0.322745,  0.989193,
    0.23385,  0.870244,  0.772039,  0.588073,  0.598806,  0.872291,
    0.00849096,  0.445958,  0.194692,  0.474801,  0.646867,  0.305645,
    0.714231,  0.777219,  0.108094,  0.539835]

