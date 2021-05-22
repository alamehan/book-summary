# 📘 JavaScript Uncover by Andre Pratama (Duniailkom.com)

<div id="daftarisi"></div>

# Daftar Isi:

<p align="left">
	<a href="#bab01">1. Berkenalan Dengan JavaScript</a>&nbsp;<br>
	<a href="#bab02">2. Sejarah dan Perkembangan JavaScript</a>&nbsp;<br>
	<a href="#bab03">3. Menjalankan Kode Program JavaScript</a>&nbsp;<br>
	<a href="#bab04">4. Aturan Dasar, Variabel dan Konstanta</a>&nbsp;<br>
	<a href="#bab05">5. Variabel dan Konstanta</a>&nbsp;<br>
	<a href="#bab06">6. Tipe Data JavaScript</a>&nbsp;<br>
	<a href="#bab07">7. Operator JavaScript</a>&nbsp;<br>
	<a href="#bab08">8. Struktur Logika dan Perulangan</a>&nbsp;<br>
	<a href="#bab09">9. Function</a>&nbsp;<br>
	<a href="#bab10">10. JavaScript Object</a>&nbsp;<br>
</p>

<div id="bab01"></div>

# 1. Berkenalan Dengan JavaScript <a href="#daftarisi">🡹</a>

1. JavaScript merupakan bagian dari 5 materi dasar web programming, yakni: HTML, CSS, PHP, MySQL dan JavaScript. Bersama-sama dengan HTML dan CSS, ketiganya berbagi peran masing-masing. HTML digunakan untuk membuat struktur dan isi dari halaman web (content). CSS untuk mempercantik tampilan website (design). Sedangkan JavaScript berfungsi menangani interaksi (behavior).**“HTML for content, CSS for presentation and JavaScript for behavior”**.
2. HTML, CSS dan JavaScript sama-sama termasuk ke dalam kelompok “client side programming language”, yakni bahasa pemrograman yang dijalankan di sisi client (web browser). PHP juga merupakan bahasa pemrograman web, tapi berada di dalam server, sehingga disebut sebagai “server side programming language”.
3. **Client Side Programming**: Ini artinya, untuk menjalankan JavaScript kita hanya butuh 2 aplikasi, yakni text editor dan web browser. Text editor digunakan membuat kode JavaScript, dan kode JavaScript tersebut bisa langsung diakses dari web browser. Kita pun bisa melihat kode JavaScript yang digunakan dari sebuah website (sama seperti HTML dan CSS). Silahkan buka website apa saja, klik kanan lalu pilih View Page Source.
4. **Server Side Programming**: Untuk menjalankan kode program PHP kita harus menggunakan aplikasi seperti Apache web server (yang merupakan bagian dari XAMPP). Kita tidak bisa melihat kode PHP yang digunakan sebuah website secara langsung layaknya HTML, CSS dan JavaScript.
5. Perkembangan JavaScript yang sangat pesat akhir-akhir ini melahirkan banyak penerapan lain dari JavaScript. Sebagai contoh, **Node.js** adalah penggunaan JavaScript di sisi server. Dalam buku ini kita hanya fokus membahas penggunaan JavaScript di sisi client (di dalam web browser).
6. Apa yang akan kita pelajari dalam buku ini terdiri dari 2 kelompok besar: JavaScript dan **DOM (Document Object Model)**. JavaScript adalah bahasa pemrograman, sedangkan DOM merupakan objek HTML yang akan kita manipulasi, seperti teks, gambar, form, tombol, title bar web browser, event, dll. Bahasa pemrograman JavaScript di kembangkan oleh ECMA, sedangkan DOM dikembangkan oleh W3C (organisasi yang juga membuat standar HTML dan CSS). Bisa dibilang, JavaScript sepenuhnya terpisah dari HTML.
7. Setelah mempelajari JavaScript, barulah kita masuk ke DOM. Disinilah JavaScript digunakan untuk mengubah total tampilan halaman web. Jadi, jika anda merasa jenuh dengan pembahasan dari bab 2 hingga 18, tahan dulu! Paksakan untuk terus mempelajarinya. Dengan pemahaman JavaScript yang cukup, kita memiliki pondasi yang kuat untuk memanipulasi objek HTML yang nantinya diakses lewat DOM mulai dari bab 19 hingga akhir buku.
<img src="images/1-1-DOM.png">

<br>
<div id="bab02"></div>

# 2. Sejarah dan Perkembangan JavaScript <a href="#daftarisi">🡹</a>

1. Brendan Eich membuat prototype bahasa baru dalam 10 hari. Pada Mei 1995, bahasa pemrograman “Mocha” lahir. Bahasa pemrograman inilah yang diputuskan untuk digunakan Netscape. Bahasa pemograman Mocha dirilis pertama kali ke dalam versi beta Netscape Navigator 2.0 di bulan September 1995, tetapi dengan menggunakan nama baru: LiveScript. Umur dari LiveScript ternyata tidak lama. 3 bulan kemudian, tepatnya Desember 1995, hadir Netscape Navigator 2.0 beta 3 dengan sebuah bahasa baru: JavaScript. Sebenarnya ini bukanlah bahasa pemrograman baru, tapi perubahan nama dari LiveScript. Nama JavaScript dipilih agar Netscape bisa ‘nompang tenar’ dari bahasa pemrograman JAVA milik Sun Microsystems, yang pada masa itu sangat populer di kalangan programmer.
<img src="images/2-1-Brendan.png">

2. “The first browser war”, perang web browser pertama antara Internet Explorer buatan Microsoft vs Netscape Navigator buatan Netscape Communications.
3. **ECMAScript** adalah sebuah standar bahasa pemrograman komputer, dimana JavaScript merupakan salah satu implementasi dari ECMAScript. JavaScript tidak bisa dijadikan standar karena masalah merk “JAVA” yang merupakan trademark SUN Micosystem (sekarang sudah diakuisisi Oracle). Intinya: Standarisasi **JavaScript = ECMAScript**. EMCAScript digunakan hanya saat merujuk ke versi dari JavaScript.
4. Pengembangan ECMAScript 4 berhenti di tengah jalan, ini disebabkan perbedaan pendapat antar anggota komite TC39, terutama mengenai fitur apa yang harus ada di ECMAScript 4. Proses “perseteruan” berlangsung cukup lama, memakan waktu hingga 10 tahun (sampai dengan 2009). Selama jangka waktu tersebut, tidak ada versi baru dari ECMAScript.
5. Di pasar web browser, Internet Explorer menjadi sangat dominan, menguasai lebih dari 80% -90% market share dari tahun 2001 hingga 2009. Netscape Navigator bisa dibilang sudah punah pada tahun 2004. Web browser Opera hadir sebagai alternatif, tapi tidak bisa berbuat banyak.
6. **AJAX**, singkatan dari **(Asynchronous JavaScript and XML)**. AJAX memungkinkan sebuah halaman web berkomunikasi langsung dengan server tanpa harus di-reload. Komunikasi antara web browser dengan web server berlangsung di latar belakang (background) secara asynchronous, hasilnya website menjadi lebih dinamis. Sebagai contoh, halaman registrasi bisa langsung mengecek apakah username yang diinput sudah ada di database atau belum. Ini dapat dilakukan sesaat setelah user berpindah dari kolom input username ke kolom dibawahnya. Tanpa menggunakan AJAX, proses pengecekan baru berlangsung saat user selesai mengisi form dan men-klik tombol submit (karena pengecekan harus dilakukan ke database yang ada di server).
7. Selain AJAX, berkembang juga berbagai komunitas dan library JavaScript seperti Prototype, jQuery, Dojo Toolkit, dan MooTools. Masa-masa ini bisa dibilang awal kebangkitan JavaScript. Dengan menggunakan library seperti jQuery, perbedaan implementasi ECMAScript dari berbagai web browser bisa diatasi dengan mudah. jQuery menyediakan ‘abstraction layer’ agar web programmer bisa berfokus kepada fitur yang ingin dicapai. Programmer yang sebelumnya “anti” dengan JavaScript (karena susahnya mengatasi perbedaan fitur web browser), mulai melirik library seperti jQuery.
8. Setelah perang web browser pertama berakhir dengan kekalahan telak Netscape, perang kedua segera mulai dengan dirilisnya Mozilla Firefox (sebagai "Reingkarnasi Netscape"). Dengan cepat Firefox menjadi web browser favorit yang sepertinya akan segera menggusur IE. Puncaknya di tahun 2010 Firefox menguasai sekitar 30% pasar web browser, walaupun IE masih tetap dominan tapi setiap tahun mengalami tren penurunan. Tidak lama lagi sepertinya Firefox bisa menjadi web browser paling populer menggantikan IE. Namun harapan ini pupus karena muncul web browser baru dari raja mesin pencari: Google Chrome yang dirilis pada Desember 2008. Didukung dengan promosi gencar, nama besar Google, fitur menawan, dan eksekusi yang cepat, membuat Google Chrome segera menjadi web browser paling banyak digunakan hingga saat ini, mengalahkan IE, Firefox, dan Opera.
<img src="images/2-2-Browser.png">

9. ECMAScript 6 atau ES6 atau ECMAScript 2015 dirilis pada bulan Juni 2015. Cukup banyak penambahan baru pada versi ini, sebagian besar merupakan fitur lanjutan untuk membuat aplikasi yang memiliki kompleksitas tinggi, seperti penggunaan **JavaScript di server menggunakan Node.js**. Mulai dari ECMAScript 6 dan selanjutnya, penamaan ECMAScript akan menggunakan nama tahun saat standar tersebut dirilis, seperti ECMAScript 2015, ECMAScript 2016, dst. Banyak perdebatan mengenai pilihan nama ini, sehingga masih sering disebut sebagai ECMAScript 6 (ES6). Dalam buku ini kita lebih banyak membahas ECMAScript 5. Walaupun menggunakan ECMAScript 5, dasar JavaScript yang ada di buku ini tetap valid untuk versi 6 dan versi 7. Fitur tambahan yang ada di ECMAScript 6 dan ECMAScript 7 juga lebih banyak ke materi lanjutan yang terlalu kompleks jika dimasukkan ke buku JavaScript untuk pemula. ES6 dan ES7 lebih cocok jika anda berniat mempelajari JavaScript sebagai bahasa pemrograman server menggunakan Node.js.
10. JavaScript Engine adalah mekanisme internal yang dimiliki oleh web browser untuk menjalankan kode JavaScript. JavaScript Engine dapat disamakan dengan compiler dalam bahasa pemograman lain, yakni algoritma yang digunakan untuk menjalankan JavaScript. Semakin cepat sebuah web browser menjalankan JavaScript akan semakin baik. **V8** adalah nama JavaScript Engine untuk Google Chrome, **SpiderMonkey** untuk Mozilla Firefox, dan **Chakra** untuk Internet Explorer.
11. Perkembangan JavaScript Saat Ini: Website yang tidak berbentuk “website”, tetapi menyerupai aplikasi desktop yang dikenal sebagai **Single-page Application (SPA)**. Contoh dari Single-page Application ini seperti aplikasi Google: Gmail, GDrive, Google Doc, dll. Di website tersebut, halamannya akan tetap sama, tidak di reload seperti layaknya sebuah website.
12. Namun perlu juga dipahami bahwa walaupun materi di eBook JavaScript Uncover sudah lumayan rumit, ini barulah dasar dari JavaScript. Jika anda serius ingin mempelajari JavaScript lebih jauh lagi, bisa lanjut ke library seperti **jQuery**, framework seperti **AngularJS** maupun **ReactJS**, atau ke server menggunakan **Node.js**.
13. Timeline sejarah JavaScript dari awal lahir hingga saat ini secara ringkas dapat diakses <a href="https://www.jetbrains.com/lp/javascript-25/">disini</a>. Daftar feature baru dari mulai **ES6 hingga ES.Next** dapat diakses di <a href="https://en.wikipedia.org/wiki/ECMAScript">Wikipedia</a>, <a href="https://www.javascripttutorial.net/es-next/">JavaScriptTutorial</a>, <a href="https://jsfeatures.in/">JSFeatures</a>, <a href="https://www.freecodecamp.org/news/es5-to-esnext-heres-every-feature-added-to-javascript-since-2015-d0c255e13c6e/">FreeCodeCamp</a>, <a href="https://github.com/daumann/ECMAScript-new-features-list">GitHub</a>, <a href="https://javascript.info/">JavaScriptInfo</a>.
  
<br>
<div id="bab03"></div>

# 3. Menjalankan Kode Program JavaScript <a href="#daftarisi">🡹</a>

1. Dalam bab ini kita akan mempelajari cara menjalankan kode program JavaScript. Dimulai dari mempersiapkan aplikasi teks editor dan web browser, membahas 3 metode input JavaScript, mengenal tab console dari web developer tools, hingga menampilkan pesan untuk web browser yang tidak mendukung JavaScript.
```HTML
====================
A. Inline JavaScript
====================

<html>
  <head>
    ...
  </head>
  <body>
    ...
    <button onclick="alert('Sedang Belajar JavaScript');"></button>
    ...
  </body> 
</html>
```

```HTML
======================
B. Internal JavaScript
======================

<html>
  <head>
    ...
    <script>
      // Kode JavaScript Disini
    </script>
  </head>
  <body>
    ...
  </body> 
</html>
```

```HTML
======================
C. External JavaScript
======================

<html>
  <head>
    ...
  </head>
  <body>
    ...
    <script src="script.js"></script>
  </body> 
</html>
```
2. Menempatkan kode JavaScript di bagian atas banyak ditemukan. Namun berkaitan dengan masalah performa, beberapa developer web menyarankan meletakkan JavaScript dibagian bawah tag ```<body>```, yakni sebelum tag penutup ```</body>```, sebagaimana yang dijelaskan dari sebuah artikel di Yahoo Developer Network: Best Practices for Speeding Up Your Web Site. 
3. Cara web browser dalam menampilkan sebuah halaman web, yakni secara berurutan dari atas ke bawah, mulai dari baris pertama hingga baris terakhir.
4. Fitur cache dari web browser bisa mempercepat pengaksesan website dengan cara menyimpan file JavaScript di dalam cache.
5. Dengan memanggil file external JavaScript dari bagian bawah tag ```<body>```, memberi kesempatan web browser untuk memproses kode HTML terlebih dahulu, baru kemudian mendownload file JavaScript. Efeknya, pengujung web bisa langsung melihat tampilan web selama proses ini, tidak hanya halaman kosong. 
6. Atribut **async** dan **defer**: kita bisa mengatur kapan dan bagaimana file external JavaScript diproses. Kedua atribut ini memungkinkan penulisan tag ```<script>``` tidak harus di bawah tag ```<body>```. Jika atribut **async** ditambahkan ke dalam tag ```<script>```, file JavaScript akan diproses pada saat yang bersamaan dengan kode HTML (secara simultan). Dengan kata lain, web browser tidak “terkunci” untuk menjalankan kode JavaScript. Metode ini juga dikenal dengan istilah **Asynchronous JavaScript** (Di proses secara bersamaan = Asynchronous). 
7. Dengan tambahan atribut **async**, kode HTML tetap diproses sembari mendownload file JavaScript. Dengan kata lain, web browser tidak masuk ke dalam Render-Blocking JavaScript. Atribut **defer** digunakan untuk mengatur kapan file JavaScript dijalankan. Dengan atribut ini, file JavaScript baru di download dan dieksekusi setelah seluruh kode HTML selesai diproses. Efek dari atribut **async** dan **defer** mungkin terdengar sama. Perbedaaan mendasar adalah, **async** digunakan untuk mengatur cara eksekusi kode JavaScript, sedangkan **defer** untuk mengatur kapan file JavaScript tersebut di download dan diproses.
8. Tambahan atribut **async** dan **defer** dari HTML5 membawa perubahan terkait posisi terbaik peletakan kode JavaScript. Standar saat ini adalah menempatkan kode JavaScript di bagian ```<head>``` dengan tambahan atribut **async**. Alasannya, web browser bisa langsung mengeksekusi file JavaScript pada saat yang bersamaan dengan proses kode HTML, sehingga website dapat ditampilkan dengan lebih cepat (tidak mengalami Render-Blocking JavaScript). Untuk kode JavaScript yang tidak terlalu penting (dan bisa menunggu), tambahkan atribut **defer**. Sebagai tambahan, atribut **async** dan **defer** hanya berlaku untuk external JavaScript. Untuk internal JavaScript, atribut ini akan diabaikan dan posisi terbaik tetap di bagian bawah tag ```<body>```.
```HTML
=============================================
Posisi Terbaik Internal & External JavaScript
=============================================

<html>
  <head>
    ...
    <script src="script-penting.js" async></script>
    <script src="script.js" defer></script>
  </head>
  <body>
    ...
    <script>
      // Internal JavaScript
    </script>
  </body> 
</html>
```
9. Berbeda dengan mayoritas bahasa pemrograman lain, secara default kita tidak bisa melihat pesan error dari JavaScript. Padahal ini sangat penting selama pembuatan kode program. Tidak ada yang lebih membuat pusing dari program yang tidak berjalan, namun tidak tahu salahnya dimana. Untuk menampilkan pesan error JavaScript, kita bisa menggunakan menu **Web developer tools** bawaan web browser. Setiap web browser modern memiliki tools seperti ini.
<img src="images/2-3-Inspector.png">

10. Tab Inspector (1) bisa digunakan untuk menelusuri seluruh kode HTML yang terdapat di dalam halaman web (2), di sisi kanan kita bisa melihat kode CSS yang digunakan oleh tag HTML tersebut (3). Jika anda sering mengedit kode CSS, tab Inspector ini sangat bermanfaat untuk melihat dan menjalankan (mengedit) kode CSS tanpa perlu mengubah file asli.
11. Tab yang sering kita akses selama membuat kode program JavaScript adalah **Tab Console**, yang berada di sebelah kanan tab Inspector. Apabila kode yang anda buat tidak berjalan sebagaimana mestinya, hal pertama yang harus dilakukan adalah memeriksa tab Console ini. Selain menampilkan pesan error, di dalam tab Console kita juga bisa menjalankan kode program JavaScript secara langsung, tanpa harus menulisnya di dalam file HTML. Fungsi **console.log()** berguna untuk menampilkan hasil kode program ke tab Console.
12. Salah satu kelemahan (sekaligus keunggulan) dari JavaScript adalah, pengunjung web bisa mematikan JavaScript yang ada di web browser mereka. Tag ```<noscript>``` bisa digunakan untuk menampilkan teks keterangan yang hanya bisa terlihat pada web browser yang tidak memiliki JavaScript (atau JavaScriptnya dimatikan).
```HTML
============================
Contoh Penggunaan <noscript>
============================

<html>
  <head>
    ...
  </head>
  <body>
    ...
    <script>
      alert("JavaScript aktif");
    </script>
    <noscript>
      JavaScript anda tidak aktif, mohon diaktifkan untuk bisa mengakses web ini.
    </noscript>
  </body> 
</html>
```

<br>
<div id="bab04"></div>

# 4. Aturan Dasar, Variabel dan Konstanta <a href="#daftarisi">🡹</a>

1. **Statement** adalah sebutan untuk sebuah baris perintah JavaScript. Walaupun saya menggunakan kata “baris”, bisa saja sebuah statement butuh beberapa baris (seperti function). Atau dalam 1 baris bisa terdiri dari beberapa statement. Setiap statement diakhiri dengan tanda titik koma (semi colon): ‘ ; ‘. Sebenarnya, tanda titik koma untuk mengakhiri statement JavaScript ini adalah opsional. Artinya, boleh tidak ditulis sepanjang statement tersebut harus berada dalam baris baru (1 statement, 1 baris). Sebaiknya kita tetap menambahkan tanda titik koma untuk mengakhiri setiap statement di dalam JavaScript.
2. **Case Sensitivity**: JavaScript termasuk bahasa pemrograman yang bersifat case sensitif, artinya huruf besar dan huruf kecil dianggap berbeda. Salah menulis huruf sangat sering terjadi.
3. **Whitespace** berarti karakter “kosong” seperti spasi, tab, atau baris baru (new line). Secara umum di dalam JavaScript whitespace akan diabaikan.
4. **Indenting** adalah istilah yang digunakan untuk menambahkan spasi atau tab diawal baris kode program. Tujuannya agar kode program lebih mudah dibaca terutama jika kode program tersebut sudah mencapai puluhan atau ratusan baris kode program. 
5. **Comment** atau baris komentar adalah sebutan untuk kode program yang tidak akan di eksekusi oleh JavaScript. Selain sebagai dokumentasi, komentar juga sering digunakan untuk menghentikan sementara baris kode program.

<br>
<div id="bab05"></div>

# 5. Variabel dan Konstanta <a href="#daftarisi">🡹</a>

1. Secara sederhana, variabel adalah “penampung” dari sebuah data. Disebut variabel karena data yang kita simpan bisa berubah-ubah sepanjang kode program (isinya tidak tetap). ```var angka = 192;``` **Operasi Asignment** atau memberikan nilai ke sebuah variabel dibaca dari kanan ke kiri (right-to-left, baca selengkapnya <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence">disini</a>). Artinya, 192 “dimasukkan” sebagai nilai ke variabel ```angka```.
2. JavaScript termasuk ke dalam bahasa pemrograman **Typeless Programming Language**, yakni kelompok bahasa pemrograman yang variabelnya bisa diisi dengan tipe data apa saja tanpa harus dideklarasikan terlebih dahulu.
3. Apabila anda sering mengikuti tutorial programming dari situs berbahasa inggris, nama variabel **foo**, **bar**, dan **baz** sering digunakan. Ketiganya dikenal sebagai **dummy variabel**, yakni variabel yang fungsinya hanya sebagai contoh. Mirip seperti teks “Lorem Ipsum dolor sit amet” dalam bidang design.
4. Kita bisa memberi nama apa saja untuk variabel, apakah itu ```angka```, ```foo```, ```bar```, ```andi```, atau ```username```. Selain variabel, kita juga bebas untuk membuat nama konstanta, function, maupun object. Semua inilah yang termasuk kedalam kelompok **Identifier**. Identifier di dalam JavaScript memiliki aturan sebagai berikut:
   - Bisa terdiri dari huruf, angka, garis bawah “ _ ” (underscore), dan tanda dollar “ $ “ (dollar sign). Selain itu, dianggap sebagai karakter ilegal (tidak boleh digunakan). 
   - Karakter pertama dari identifier tidak boleh berupa angka. Angka hanya bisa digunakan sebagai karakter kedua dan seterusnya.
   - Bersifat case sensitive, dimana huruf besar dan kecil dianggap berbeda.
   - Harus selain dari **reserved keyword**, yakni kata khusus yang berfungsi sebagai perintah di dalam pemrograman JavaScript, seperti ```var```, ```while```, ```function```, dll.
5. Di CSS kita menggunakan cara penulisan selector yang dipisah dengan tanda “ - ”, seperti ```main-box```, ```left-sidebar```, dan ```single-post```. Di PHP kita mengenal Snake Case, yakni menggunakan huruf kecil dan tanda underscore sebagai pemisah variabel, seperti ```jumlah_barang```, ```nama_dosen```, dan ```alamat_siswa```. Di JavaScript menggunakan CamelCase. CamelCase adalah cara penulisan variabel dimana jika sebuah variabel terdiri dari beberapa kata, huruf pertama dari kata kedua dan seterusnya diubah menjadi huruf besar, seperti: ```banyakAnggota```, ```totalBiaya```, ```mainBox```, atau ```jumlahKlikSatuHari```. Jika variabel tersebut hanya terdiri dari 1 kata, ditulis dengan huruf kecil semua.
6. **Strict Mode** memaksa JavaScript menampilkan error (di Tab Console) pada kode program yang seharusnya bisa berjalan “normal”. Tujuannya, meminimalisir kemungkinan bug karena penulisan yang salah, typo, dan berbagai hal lain. Strict mode sepenuhnya opsional dan mungkin tidak bisa selalu anda gunakan, terutama jika terdapat kode JavaScript pendahulu yang terlalu rumit untuk diubah semuanya. Strict Mode akan membuat web browser menampilkan error dimana sebelumnya hanya ada **“silent error”**. Salah satunya ketika membuat variabel tanpa perintah ```var```. Untuk masuk ke dalam Strict Mode, tambahkan string ```"use strict";``` di baris pertama kode JavaScript atau di baris paling awal dari sebuah function.
7. EcmaScript 6 membawa fitur baru ke dalam JavaScript, yakni menggunakan perintah ```let``` untuk membuat variabel (sebagai alternatif dari ```var```). Perbedaan mendasar dari ```var``` dan ```let``` adalah terkait dengan **variabel scope**, yakni di bagian mana sebuah variabel masih bisa diakses. Penjelasan mengenai variabel scope akan saya bahas pada bab tentang function.
8. Konstanta (```const```) dapat dikatakan sebagai variabel yang tidak bisa diubah sepanjang kode program. Setelah konstanta ditulis dan diberi nilai awal, isi konstanta tersebut tidak bisa ditukar dengan nilai lain. Berbeda dengan variabel yang menggunakan CamelCase, konstanta biasa ditulis menggunakan huruf besar dan garis bawah (underscore) sebagai pemisah kata. Tujuannya agar mudah dibedakan dengan variabel.
```HTML
================
Var, Let & Const
================

<html>
  <head>
    ...
  </head>
  <body>
    ...
    <script>
      "use strict";

      var harga = 12000;
      let namaLengkap = "Rudi Siswoyo";
      const NILAI_PI = 3.14;

      ...
    </script>
  </body> 
</html>
```
9. Berdasarkan contoh diatas: variabel ```harga```, let ```namaLengkap```, dan konstanta ```NILAI_PI``` adalah **Identifier**. Sedangkan ```12000```, ```"Rudi Siswoyo"```, dan ```3.14``` adalah **Literal**.

<br>
<div id="bab06"></div>

# 6. Tipe Data JavaScript <a href="#daftarisi">🡹</a>

1. Secara garis besar, tipe data dalam JavaScript terdiri dari 2 kelompok, yakni tipe data primitif (primitive type), dan tipe data object. Tipe data primitif disebut demikian karena tipe data ini “sederhana” dan hanya terdiri dari 1 nilai. Di dalam JavaScript terdapat 6 **tipe data primitif**, yaitu: **Number, String, Boolean, Null, Undefined, Symbol**. Sedangkan tipe data object, bisa disebut sebagai tipe data “khusus” yang prilaku dan isinya bermacam-macam. Adapun **tipe data object** bawaan JavaScript yaitu: **Array, Date, RegExp, Map, WeakMap, Set, WeakSet.**
2. Untuk tipe data Object, dalam bab ini saya hanya membahas Object Array. Tipe data Object Date dan RegExp akan dibahas dalam bab tersendiri karena butuh penjelasan yang cukup panjang, termasuk cara membuat object bentukan sendiri. Tipe data Symbol, Map, WeakMap, Set dan WeakSet adalah tipe data baru dalam ECMAScript 6. Tipe data ini tidak akan saya bahas karena termasuk materi lanjutan yang cukup kompleks untuk pemula.

```Javascript
// ===================
// A. Tipe Data Number
// ===================

var numA = 100;                       // angka bulat
var numB = -100;                      // angka bulat negatif
var numC = 0.66634;                   // angka pecahan
var numD = -0.66634;                  // angka pecahan negatif
var numE = 3e3;                       // 3 x 10^3
var numF = 0.4e-3;                    // 0.4 x 10^-3
var numG = 999;                       // desimal (basis 10)
var numH = 0b1111100111;              // biner (basis 2), diawali 0b
var numI = 0o1747;                    // oktal (basis 8), diawali 0o
var numJ = 0x3E7;                     // heksadesimal (basis 16), diawali 0x
var numK = 9/"a"; console.log(numK);  // output: NaN (Not a Number)
var numL = 9/0; console.log(numL);    // output: Infinity (Tak Hingga)
```

```Javascript
// ===================
// B. Tipe Data String
// ===================

var strA = "Hello World!";            // string dengan kutip dua
var strB = 'Hello World!';            // string dengan kutip satu
var strC = "Hari Jum'at";             // kutip satu didalam kutip dua
var strD = 'Dia berkata: "Hey"';      // kutip dua didalam kutip satu
var strE = "Dia berkata: \"Hey\"";    // kutip dua didalam kutip dua, pakai escape character (\)
var strF = 'Hari Jum\'at';            // kutip satu didalam kutip satu, pakai escape character (\)
var strG = "\u2764 You!"              // contoh pemakaian Unicode ⇨ hasilnya: ❤ You!

/*
Ragam karakter escape di JavaScript:
 1. \0    : Karakter NUL
 2. \b    : Backspace
 3. \t    : Horizontal tab
 4. \n    : Newline
 5. \v    : Vertical tab
 6. \f    : Form feed
 7. \r    : Carriage return
 8. \"    : Tanda kutip dua (double quote)
 9. \'    : Tanda kutip satu (apostrophe atau single quote)
10. \\    : Garis miring backslash
11. \xXX  : Karakter Latin-1 dengan menggunakan dua digit heksa desimal XX
12. \uXXXX: Karakter Unicode dengan menggunakan empat digit heksa XXXX

Daftar Karakter Latin-1 & Unicode: http://unicode-table.com/
*/

var strH = "Indonesia";
var strI = "Bahasa " + strH;          // Sebelum ada fitur Template String ES6 ⇨ hasilnya: Bahasa Indonesia
var strJ = `Bahasa ${strH}`;          // Setelah ada fitur Template String ES6 ⇨ hasilnya: Bahasa Indonesia
```

```Javascript
// ====================
// C. Tipe Data Boolean
// ====================

var bolA = true;                      // bernilai true, biasanya di pakai di if, else, while, dan do while
var bolB = false;                     // bernilai false, biasanya di pakai di if, else, while, dan do while
```

```Javascript
// =============================
// D. Tipe Data Null & Undefined
// =============================

var nudA = null;                      // keadaan dimana data "kosong", biasanya sengaja diinput oleh programmer
var nudB = undefined;                 // keadaan dimana data "tidak terdefinisi", biasanya terjadi karena error

// Kasus yang menghasilkan undefined

var und1;
console.log(und1);                    // output: undefined (var yang dibuat tanpa langsung diisi nilai, menjadi undefined)

var und2 = [1, 2, 3];
console.log(und2[3]);                 // output: undefined (mengakses array diluar indeks yang dibuat, menjadi undefined)

var und3 = {nama: "iyan", umur: 24};
console.log(und3["alamat"]);          // output: undefined (mengakses object diluar key yang dibuat, menjadi undefined)
```

```Javascript
// ==================
// E. Tipe Data Array
// ==================

var arrSiswa = ["Andri", "Joko", "Sukma"];    // Array 1D berisi hanya data string
var arrAcak  = [1, 2.0, "tiga", true, null];  // Array 1D berisi beragam tipe data
var arr2D    = [[2,5], [9,5], [3,5]];         // Array 2D, misalnya untuk koordinat

console.log(arrSiswa);                // output: ["Andri", "Joko", "Sukma"]
console.log(arrSiswa[0]);             // output: Andri
console.log(arrSiswa[1]);             // output: Joko
console.log(arrSiswa[2]);             // output: Sukma
console.log(arrSiswa[3]);             // output: undefined

console.log(arr2D);                   // output: [[2,5],[9,5],[3,5]]
console.log(arr2D[0]);                // output: [2,5]
console.log(arr2D[1]);                // output: [9,5]
console.log(arr2D[2]);                // output: [3,5]
console.log(arr2D[0][0]);             // output: 2
console.log(arr2D[0][1]);             // output: 5
console.log(arr2D[1][0]);             // output: 9
console.log(arr2D[1][1]);             // output: 5
console.log(arr2D[2][0]);             // output: 3
console.log(arr2D[2][1]);             // output: 5
```

```Javascript
// ===================
// F. Tipe Data Object
// ===================

// Dibahas di BAB 10!
```

```Javascript
// ==================
// G. Operator typeof
// ==================

/*
Operator typeof digunakan untuk melihat tipe data dari sebuah variabel
Apakah tipe datanya number, string, boolean, undefined, atau sebuah object. 
*/

console.log(typeof numA);                 // output: number
console.log(typeof strA);                 // output: string
console.log(typeof bolA);                 // output: boolean
console.log(typeof nudA);                 // output: object (bukan null)
console.log(typeof nudB);                 // output: undefined
console.log(typeof arrSiswa);             // output: object

// Check Tipe Data (Materi Lanjutan)

var num = 10;                             // tipe data: number
var str = "JavaScript";                   // tipe data: string
var bol = true;                           // tipe data: boolean
var nul = null;                           // tipe data: null
var und = undefined;                      // tipe data: undefined
var arr = [1, 2, "tiga"];                 // tipe data: Array
var nan = 9/"a";                          // tipe data: NaN
var inf = 9/0;                            // tipe data: Infinity

console.log(typeof num === "number");     // output: true   (check apakah datanya number)
console.log(typeof str === "string");     // output: true   (check apakah datanya string)
console.log(typeof bol === "boolean");    // output: true   (check apakah datanya boolean)
console.log(nul === null);                // output: true   (check apakah datanya null)
console.log(und === undefined);           // output: true   (check apakah datanya undefined)
console.log(inf === Infinity);            // output: true   (check apakah datanya infinity)
console.log(Array.isArray(arr));          // output: true   (check apakah datanya array)
console.log(Number.isNaN(nan));           // output: true   (check apakah datanya NaN)
```

<br>
<div id="bab07"></div>

# 7. Operator JavaScript <a href="#daftarisi">🡹</a>

```Javascript
// ======================
// A. Operator Aritmatika
// ======================

var a = 10;
var b = 2;

console.log(a + b);                   // output: 12     ⇨ addition (tambah)
console.log(a - b);                   // output: 8      ⇨ substraction (kurang)
console.log(a * b);                   // output: 20     ⇨ multiplication (kali)
console.log(a / b);                   // output: 5      ⇨ division (bagi)
console.log(a % b);                   // output: 0      ⇨ modulo (sisa bagi)
console.log(a ** b);                  // output: 100    ⇨ exponentiation (pangkat)

console.log(4+6/5-3*2+3);             // output: 2.2    ⇨ operator * dan / diproses lebih awal (precedence: 15)
console.log((4+6)/(5-3)*2+3);         // output: 13     ⇨ operator () diproses lebih awal (precedence: 21)

/*
Baca urutan prioritas operator (precedence) secara lengkap di:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence
*/
```

```Javascript
// ===================================
// B. Operator Increment dan Decrement
// ===================================

var c = 10, d = 10, e = 10, f = 10;

console.log(++c);                     // output: 11     ⇨ pre-increment: langsung tambahkan
console.log(c);                       // output: 11
console.log(--d);                     // output: 9      ⇨ pre-decrement: langsung kurangi
console.log(d);                       // output: 9

console.log(e++);                     // output: 10     ⇨ post-increment: tampilkan dulu, baru tambahkan
console.log(e);                       // output: 11
console.log(f--);                     // output: 10     ⇨ post-decrement: tampilkan dulu, baru kurangi
console.log(f);                       // output: 9
```

```Javascript
// ========================
// C. Operator Perbandingan
// ========================

console.log(8 == 12);                 // output: false  ⇨ equality (sama dengan)
console.log(8 != 12);                 // output: true   ⇨ inquality (tidak sama dengan)
console.log(10 < 11);                 // output: true   ⇨ less than (kurang dari)
console.log(11 <= 11);                // output: true   ⇨ less than or equal (kurang dari atau sama dengan)
console.log(21 > 20);                 // output: true   ⇨ greater than (lebih dari)
console.log(21 >= 21);                // output: true   ⇨ greater than or equal (lebih dari atau sama dengan)

console.log(9 == "9");                // output: true
console.log(9 === "9");               // output: false  ⇨ strict equality (identik dengan)
console.log(9 != '9');                // output: false
console.log(9 !== '9');               // output: true   ⇨ strict inequality (tidak identik dengan)

// C1. Anda Harus Tahu

console.log(1 == true);               // output: true
console.log(1 === true);              // output: false
console.log(0 == false);              // output: true
console.log(0 === false);             // output: false
console.log(0.3 == 3e-1);             // output: true
console.log(0.3 === 3e-1);            // output: true   (karena memang nilainya sama)
console.log(true > false)             // output: true   (ingat: true = 1, false = 0)

// C2. Perbandingan String 

/*
Setiap karakter dalam string menggunakan nomor urut
desimal di ASCII-Code: https://www.ascii-code.com/
*/

console.log("a" < "b");               // output: true   (a = 97, b = 98)
console.log("a" < "A");               // output: false  (a = 97, A = 65)
console.log("ali" < "ala");           // output: false  (ali = 97→108→105, ala = 97→108→97)
console.log("ali" < "alo");           // output: true   (ali = 97→108→105, alo = 97→108→111)
console.log("ali" < "alika");         // output: true   (ali = 97→108→105, alika = 97→108→105→107→97)
console.log("ali" < 9999999);         // output: false  (perbandingan String & Number selalu menghasilkan false)
```

```Javascript
// =======================
// D. Falsy & Truthy Value
// =======================

/*
Di JavaScript sebuah tipe data akan berubah menjadi tipe data lain tergantung operator
yang digunakan. Untuk operator perbandingan, tipe data ini akan dikonversi menjadi
boolean (true/false). Nilai yang dikonversi menjadi false disebut Falsy Value, dan
nilai yang dikonversi menjadi true disebut Truthy Value.

Yang dikonversi menjadi false:
• false
• null
• undefined
• 0
• NaN
• ''        (string kosong)
• ""        (string kosong)

Yang dikonversi menjadi true:
• true
• {}        (object kosong)
• []        (array kosong)
• 42        (sembarang angka, termasuk pecahan dan negatif, selain 0)
• "foo"     (sembarang string, selama bukan string kosong)
• infinity  (termasuk -infinity)
*/

console.log('' == '0');               // output: false  (hasil konversi: false == true)
console.log(0 == '');                 // output: true   (hasil konversi: false == false) 
console.log(0 == '0');                // output: true   (bukan operator indentik, jadinya true) 
console.log(false == 'false');        // output: false  (hasil konversi: false == true) 
console.log(false == '0');            // output: true   (bukan operator indentik & false kan bernilai 0, jadinya true) 
console.log(false == undefined);      // output: false  (pengecualian) 
console.log(false == null);           // output: false  (pengecualian) 
console.log(null == undefined);       // output: true   (hasil konversi: false == false) 
console.log('\t\r\n' == 0);           // output: true   (pengecualian) 
```

```Javascript
// ==================
// E. Operator Logika
// ==================

console.log(true && false);           // output: false  ⇨ and operator (true hanya jika kedua nilai true)
console.log(true || false);           // output: true   ⇨ or operator (true jika salah satu nilai true)
console.log(!false);                  // output: true   ⇨ not operator (negasi/kebalikannya)
console.log(true || true && false);   // output: true   ⇨ operator && diproses lebih awal (precedence: 7)

// E1. Cara Kerja Operasi Logika

/* 
Operasi logika di proses dari kiri ke kanan (left-to-right), baca selengkapnya di:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

Selain itu, operasi logika pun menggunakan prinsip short-circuit-evaluation, maksudnya jika
dengan memeriksa 1 nilai saja hasil operasi tersebut sudah diketahui, nilai-nilai lain tidak
akan diperiksa, kecuali jika terdapat operator && dan || dalam 1 operasi, maka operator &&
akan dijalankan terlebih dahulu (karena nilai precedence && lebih tinggi daripada ||)
*/

console.log(true || false || true);   // kiri ke kanan: true bertemu operator ||, stop, sudah pasti hasilnya true
console.log(false && true && true);   // kiri ke kanan: false bertemu operator &&, stop, sudah pasti hasilnya false
console.log(true || true && false);   // operator && duluan, menjadi: true || false, hasilnya true

console.log(true && alert("HYA!"));   // fungsi alert() berjalan, karena true bertemu &&, lanjut ke alert()
console.log(false && alert("HYA!"));  // fungsi alert() tidak berjalan, karena false bertemu &&, stop
console.log(true || alert("HYA!"));   // fungsi alert() tidak berjalan, karena true bertemu ||, stop
console.log(false || alert("HYA!"));  // fungsi alert() berjalan, karena false bertemu ||, lanjut ke alert()

// E2. Operasi Logika Non-Boolean

/*
Nilai yang dibandingkan menggunakan operator logika harus bertipe boolean, jika tidak, akan di
konversi secara otomatis berdasarkan ketentuan Falsy & Truthy Value. Lalu, hasil akhir dari
operasi logika non-boolean ini berupa nilai dari posisi terakhir yang diperiksa.
*/

console.log("Hello" || "World");      // output: Hello  ("Hello" ≈ true, lalu bertemu ||, stop, hasilnya string Hello)
console.log("Hello" && "World");      // output: World  ("Hello" ≈ true, lalu bertemu &&, lanjut, hasilnya string World)
console.log(true || "World");         // output: true   (true bertemu ||, stop, hasilnya true)
console.log(false || "World");        // output: World  (false bertemu ||, lanjut, "World" ≈ true, hasilnya string World)
console.log("Hello" && false);        // output: false  ("Hello" ≈ true, lalu bertemu &&, lanjut, hasilnya false)
console.log(false && "World");        // output: false  (false bertemu &&, stop, hasilnya false)

console.log(false || false && true || "World");   // output: World  (&& duluan, menjadi: false || false || "World", ...)
console.log(true || false && true || "World");    // output: true   (&& duluan, menjadi: true || false || "World", ...)
```

```Javascript
// ==================
// F. Operator String
// ==================

var arr = ["Andri", "Joko", "Sukma"];

strA = arr[0] + " dan " + arr[1] + " adalah teman akrab.";  // string concatenation (sebelum ES6), "+" sebagai penyambung
strB = `${arr[0]} dan ${arr[1]} adalah teman akrab`;        // template string (setelah ES6), memakai backtick (``)

// Kasus Konversi Number ke String

console.log(10 + 10 + 9);             // output: 29     (number)
console.log("10" + 10 + 9);           // output: 10109  (string)  dari hasil konversi: console.log("10" + "10" + "9");
console.log(10 + "10" + 9);           // output: 10109  (string)  dari hasil konversi: console.log(10 + "10" + "9");
console.log(10 + 10 + "9");           // output: 209    (string)  dari hasil konversi: console.log(20 + "9");
```

```Javascript
// ===================
// G. Operator Bitwise
// ===================

/*
Operator bitwise adalah operator khusus untuk menangani operasi
logika bilangan biner. Operator ini sangat jarang digunakan dalam
JavaScript dan cukup rumit. Sehingga tidak akan dibahas disini.
*/
```

```Javascript
// ======================
// H. Operator Assignment
// ======================

var g = 10;       // artinya 10 dimasukkan sebagai nilai ke variabel g (operator assignment memiliki precedence: 3)
var h = 10 + 5;   // jumlahkan 10 + 5 dulu (operator "+" memiliki precedence: 14), lalu masukkan hasilnya ke variabel h
var i = g + h;    // more: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

// Operator Gabungan Assignment

var gabA = gabB = gabC = gabD = gabE = 20;

gabA += 10;       // gabA = gabA + 10 🡲 gabA = 20 + 10  (output: 30) 
gabB -= 10;       // gabB = gabB - 10 🡲 gabB = 20 - 10  (output: 10)
gabC /= 10;       // gabC = gabC / 10 🡲 gabC = 20 / 10  (output: 2)
gabD *= 10;       // gabD = gabD * 10 🡲 gabD = 20 * 10  (output: 200) 
gabE %= 10;       // gabE = gabE % 10 🡲 gabE = 20 % 10  (output: 0)
```

```Javascript
// ==================
// I. Operator Spread
// ==================

/*
Spread merupakan operator baru di ES6. Operator ini digunakan untuk berbagai keperluan yang berhubungan dengan array, salah
satunya untuk menggabungkan array. Operator ini menggunakan tanda titik tiga kali (...), kemudian diikuti dengan nama variabel.
*/

var nilai1 = ["a", "b", "c", "d"];
var nilai2 = [1, 2, 3, 4];

var nilai3 = [...nilai1, "e", "f"];   // ...nilai1 berarti mengakses seluruh element dari array nilai1
console.log(nilai3);                  // output: ["a", "b", "c", "d", "e", "f"]

var nilai4 = [0, ...nilai2, 5, 6];    // ...nilai2 berarti mengakses seluruh element dari array nilai2
console.log(nilai4);                  // output: [0, 1, 2, 3, 4, 5, 6]

var nilai5 = [...nilai3, ...nilai4];
console.log(nilai5);                  // output: ["a", "b", "c", "d", "e", "f", 0, 1, 2, 3, 4, 5, 6]
```

<br>
<div id="bab08"></div>

# 8. Struktur Logika dan Perulangan <a href="#daftarisi">🡹</a>

```Javascript
// ===========================
// A. Struktur Logika: IF-ELSE
// ===========================

var nilai = 90;                     

if (nilai >= 0 && nilai <= 100){      // jika nilai >= 0 dan <= 100, masuk ke kondisi berikutnya, selain itu tidak valid!
  if (nilai >= 80){
    console.log("A");
  } else if (nilai >= 70){
    console.log("B");
  } else if (nilai >= 60){
    console.log("C");
  } else if (nilai >= 50){
    console.log("D");
  } else{
    console.log("E");
  }
} else {
  console.log("Tidak Valid!");
}
```

```Javascript
// ==========================
// B. Struktur Logika: SWITCH
// ==========================

var nilaiTK = 6;   

switch(nilaiTK){                      // case 1-5: kurang, case 6-7: cukup, case 8-10: baik, selain itu tidak valid!
  case 1:
  case 2:
  case 3:
  case 4:
  case 5:
    console.log("kurang");
    break;
  case 6:
  case 7:
    console.log("cukup");
    break;
  case 8:
  case 9:
  case 10:
    console.log("baik");
    break;
  default:
    console.log("Tidak Valid!");
}
```

```Javascript
// ====================================
// C. Struktur Logika: Ternary Operator
// ====================================

var jumlah = 501;
var pesan = jumlah > 500 ? "Cukup!" : "Produksi lagi!";

/*
Cara baca: Apakah jumlah > 500? jika iya (true), kirim string "Cukup!" ke variabel
pesan. Jika tidak (false) kirim string "Produksi lagi!" ke variabel pesan.
*/

var user = "admin";
var akses = user === "admin" ? true : false;

if (akses){ // jika akses bernilai true
  console.log("Welcome, admin!");
}

/*
Cara baca: Apakah user === "admin"? jika iya, kirim boolean true ke variabel akses, lalu kondisi "if (akses)"
akan dijalankan. Jika tidak, kirim boolean false ke variabel akses, dan kondisi "if (akses)" tidak jalan.
*/
```

```Javascript
// ==================
// D. Perulangan: FOR
// ==================

for (var i=1; i<=10; i++){            // output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
}

for (var j=20; j>0; j=j-2){           // output: 20, 18, 16, 14, 12, 10, 8, 6, 4, 2
  console.log(j);
}

for (var k=1; k<3; k++){              // output: outer 1 inner 1 s/d outer 2 inner 3
  for (var l=1; l<=3; l++){           
    console.log(`outer ${k} inner ${l}`);
  }
}

// D1. Break: Berhenti memproses perulangan (keluar dari perulangan)

for (var m=10; m>=1; m--){            // output: 10, 9, 8, 7, 6, 5, 4, 3
  if (m === 2){
    break;
  }
  console.log(m);
}

// D2. Continue: Berhenti memproses perulangan saat ini & lanjut ke perulangan berikutnya

for (var m=10; m>=1; m--){            // output: 10, 9, 8, 7, 6, 5, 4, 3, 1
  if (m === 2){
    continue;
  }
  console.log(m);
}

// D3. Menampilkan element array dengan perulangan FOR

var arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];
for (var n=0; n<arrSiswa.length; n++){
  console.log(arrSiswa[n]);
}                                     // output: Andri, Joko, Sukma, Rina, Sari

```

```Javascript
// ====================
// E. Perulangan: WHILE
// ====================

/*
Perulangan WHILE cocok digunakan untuk situasi dimana kita tidak tahu berapa banyak perulangan
yang mesti dijalankan. Berbeda dengan perulangan FOR yang kita tahu berapa banyak perulangannya.
*/

var i = 1;
while (i <= 10){                      // output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
  i++;
}

var j = 10;
while (j > 1){                        // output: 20, 18, 16, 14, 12
  if (j === 5){
    break;
  }
  console.log(j*2);
  j--;
}
```

```Javascript
// =======================
// F. Perulangan: DO WHILE
// =======================

/*
Dalam perulangan DO WHILE, kondisi akan di check di akhir, hal ini menyebabkan setidaknya
perulangan akan diproses 1 kali, walaupun kondisi tersebut sudah tidak terpenuhi sejak awal.
*/

var i = 1;
do {                                  // output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
  i++;
} while (i <= 10);

var j = 1;
do {                                  // output: 1
  console.log(j);
  j--;
} while (j > 999);
```

```Javascript
// =====================
// G. Perulangan: FOR OF
// =====================

/*
Perulangan FOR OF merupakan fitur baru dari ES6, digunakan khusus untuk menampilkan element array.
Hasil dari perulangan FOR OF dibawah ini, sama dengan hasil perulangan FOR di point D3 diatas.
*/

var arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];
for (var i of arrSiswa){
  console.log(i);
}                                     // output: Andri, Joko, Sukma, Rina, Sari
```

```Javascript
// =====================
// H. Perulangan: FOR IN
// =====================

/*
Note: Agar lebih paham, coba baca dulu BAB 10 tentang tipe data Object.

Perulangan FOR IN merupakan fitur baru dari ES6, digunakan khusus untuk menampilkan seluruh
isi object (property dan method). Sebenarnya, bisa juga digunakan untuk menampilkan isi array
(karena array pun termasuk kedalam tipe data Object), namun tidak disarankan.
*/

var objMobil = {
  merk: "Toyota Avanza",
  tipe: "MPV",
  harga: 200000000,
  warna: "biru",
  hidupkan: function() {return "Mesin dihidupkan!";}
};

for (var i in objMobil) {
  console.log(`Isi ${i} = ${objMobil[i]}`);
}

/*
Output:
Isi merk = Toyota Avanza
Isi tipe = MPV
Isi harga = 200000000
Isi warna = biru
Isi hidupkan = function() {return "Mesin dihidupkan!";}
*/
```

<br>
<div id="bab09"></div>

# 9. Function <a href="#daftarisi">🡹</a>

```Javascript
// =====================
// A. Function Sederhana
// =====================

function pagiMalam(){
  console.log("Selamat Pagi!");
  console.log("Selamat Malam!");
}

pagiMalam();                          // output: Selamat Pagi!, Selamat Malam!
```

```Javascript
// =====================================
// B. Function dengan Parameter & Return
// =====================================

function salam(kapan, nama){          // kapan & nama adalah sebuah parameter yang akan menampung nilai dari argument
  return `Selamat ${kapan} ${nama}!`; // return berfungsi untuk mengembalikan nilai & memberhentikan function
}

function ratarata(a, b, c, d){
  var hasil = (a+b+c+d)/4;
  return hasil;
}

console.log(salam("Pagi", "Budi"));   // output: Selamat Pagi Budi!     ⇨ "Pagi" & "Budi" merupakan sebuah argument
console.log(salam("Malam", "Putri")); // output: Selamat Malam Putri!

console.log(ratarata(1, 2, 3, 4));    // output: 2.5 (hasil dari (1+2+3+4)/4 🡲 10/4)
console.log(ratarata(1, 2, 3, 4, 5)); // output: 2.5 (argument ke-5 akan diabaikan, karena tidak ada "slot"-nya di function)
console.log(ratarata(1, 2, 3));       // output: NaN (argument ke-4 tidak ada, maka secara defaultnya nilainya undefined)
```
```Javascript
// ====================================
// C. Function dengan Default Parameter
// ====================================

function tambah(a=10, b=10, c=10, d=10){
  return a+b+c+d;
}

function kurang(a, b, c=10, d=10){
  return a-b-c-d;
}

function kali(a=10, b=10, c, d){
  return a*b*c*d;
}

console.log(tambah());                // output: 40 (hasil dari 10+10+10+10)
console.log(tambah(20));              // output: 50 (hasil dari 20+10+10+10)
console.log(tambah(20, 25));          // output: 65 (hasil dari 20+25+10+10)
console.log(tambah(20, 25, 30));      // output: 85 (hasil dari 20+25+30+10)
console.log(tambah(20, 25, 30, 15));  // output: 90 (hasil dari 20+25+30+15)

console.log(kurang());                // output: NaN (function kurang butuh minimal 2 argument! untuk parameter a & b)
console.log(kurang(20));              // output: NaN (function kurang butuh minimal 2 argument! kurang argument ke-2)
console.log(kurang(20, 25));          // output: -25 (argument c & d jika tidak diisi, maka akan diisi nilai defaultnya)
console.log(kurang(20, 25, 30));      // output: -45 (hasil dari 20-25-30-10)
console.log(kurang(20, 25, 30, 15));  // output: -50 (hasil dari 20-25-30-15)

console.log(kali());                  // output: NaN (function kali butuh minimal 4 argument! untuk parameter a, b, c & d)
console.log(kali(20, 25));            // output: NaN (function kali butuh minimal 4 argument! kurang argument ke-3 & ke-4)
console.log(kali(20, 25, 30, 15));    // output: 225000 (hasil dari 20*25*30*15)
console.log(kali(undefined, undefined, 30, 15));  // output: 45000 (hasil dari 10*10*30*15), undefined akan diisi nilai default
```

```Javascript
// ===================================
// D. Function dengan Arguments Object
// ===================================

// D1. Array Argument

function numA(){                      // function dibuat tanpa parameter (tanpa wadah untuk argument), namun setiap argument
  console.log(arguments[0]);          // dapat ditangkap oleh array argument (bawaan JavaScript) berapapun jumlahnya (fleksibel)
  console.log(arguments[1]);
  console.log(arguments[2]);
  console.log(arguments[3]);
}

numA(20, 25, 30, 15);                 // output: 20, 25, 30, 15
numA(20, 25);                         // output: 20, 25, undefined, undefined

// D2. arguments.length

function numB(){                      // karena array argument merupakan sebuah array, maka kita dapat menghitung jumlah argument
  total = arguments.length;           // yang dikirimkan pada saat pemanggilan function dengan menggunakan property length
  return total;
}

console.log(numB());                  // output: 0 (terdapat 0 argument saat pemanggilan function)
console.log(numB(20));                // output: 1 (terdapat 1 argument saat pemanggilan function)
console.log(numB(20, 25));            // output: 2 (terdapat 2 argument saat pemanggilan function)
console.log(numB(20, 25, 30));        // output: 3 (terdapat 3 argument saat pemanggilan function)
console.log(numB(20, 25, 30, 15));    // output: 4 (terdapat 4 argument saat pemanggilan function)

// D3. Studi Kasus: Rata-Rata

function ratarata(){                  // berbekal array argument dan arguments.length, kita bisa membuat sebuah function
  var totalArg = arguments.length;    // rata-rata yang bisa menerima berarapun jumlah argumentnya (fleksibel)
  var hasil = 0;
  for (var i=0; i<totalArg; i++){
    hasil += arguments[i];
  }
  return hasil/totalArg;
}

console.log(ratarata(2, 4));          // output: 3   (hasil dari (2+4)/2 🡲 6/2)
console.log(ratarata(2, 4, 8, 16));   // output: 7.5 (hasil dari (2+4+8+16)/4 🡲 30/4)

// D4. Spread Operator

function numC(...arg){                // selain untuk menggabungkan array seperti yang dijelaskan di bab 7 (operator),
  console.log(arg[0]);                // spread (...) juga dapat digunakan untuk menggantikan peran arguments object.
  console.log(arg[1]);                // coba bandingkan hasilnya dengan point D1, maka akan sama saja.
  console.log(arg[2]);                // penulisannya tidak harus ...arg, bisa dengan kata lain, misalnya ...angka, dll
  console.log(arg[3]);
}

numC(20, 25, 30, 15);                 // output: 20, 25, 30, 15
numC(20, 25);                         // output: 20, 25, undefined, undefined

// D5. Argument + Spread Operator

function numD(a, b, ...sisa){         // cara baca: jika function numD dipanggil dengan lebih dari 3 argument, maka argument
  console.log(a);                     // pertama dan kedua masuk ke variabel a dan b, sisanya disimpan kedalam array sisa
  console.log(b);
  console.log(sisa);
}

numD(20, 25);                         // output: 20, 25, []
numD(20, 25, 30);                     // output: 20, 25, [30]
numD(20, 25, 30, 15);                 // output: 20, 25, [30, 15]

// D6. Studi Kasus: Rata-Rata V2

function rataratav2(...nilai){        // studi kasus pada point D3, dapat kita buat ulang dengan memanfaatkan spread
  var totalArg = nilai.length;        // serta perulangan for of, hasilnya aka sama saja, dan juga tetap fleksibel
  var hasil = 0;
  for (var i of nilai){
    hasil += i;
  }
  return hasil/totalArg;
}

console.log(rataratav2(2, 4));        // output: 3   (hasil dari (2+4)/2 🡲 6/2)
console.log(rataratav2(2, 4, 8, 16)); // output: 7.5 (hasil dari (2+4+8+16)/4 🡲 30/4)
```

```Javascript
// =================
// E. Variable Scope
// =================

/*
Variable Scope adalah istilah tentang sejauh mana sebuah variable masih dapat diakses. Global Variable dapat diakses dari-
mana saja, sedangkan Local Variable hanya bisa diakses di dalam ruang lingkup terbatas, milsanya di dalam sebuah function
*/

// E1. Global Variable

var a = "Belajar JS";                 // a merupakan global variable, oleh karena itu dapat diakses darimana saja
function boo(){
  console.log(a);                     // a yang diakses disini yaitu a global varibale, berhubung function foo
}                                     // tidak memiliki local variable a, maka akan "naik" mencari ke global

boo();                                // output: Belajar JS (hasil dari dalam function)
console.log(a);                       // output: Belajar JS (hasil dari global variable a)

// E2. Global & Local Variable

var b = "Belajar JS";                 // b disini merupakan global variable
function coo(){
  var b = "Belajar CSS";              // b disini merupakan local variable
  console.log(b);                     // b yang diakses disini yaitu b local variable
}

coo();                                // output: Belajar CSS (hasil dari dalam function)
console.log(b);                       // output: Belajar JS (hasil dari global variable b)

// E3. Contoh dalam Argument (1)

function doo(c, d){
  var c = 20;                         // c disini merupakan local variable
  var d = 40;                         // d disini merupakan local variable
  return c+d;                         // function mengembalikan nilai 60
}

var c = 5;                            // c disini merupakan global variable
var d = 10;                           // d disini merupakan global variable
var e = doo(c, d);                    // argument yang dikirim yaitu baz(5, 10)

console.log(c);                       // output: 5
console.log(d);                       // output: 10
console.log(e);                       // output: 60 (bukan 15, karena nilai var c & d tertimpa saat didalam function)

// E4. Contoh dalam Argument (2)

function foo(){
  c = 20;                             // c disini menimpa global variable c (jika didefinisikan tanpa var, maka berefek ke global)
  d = 40;                             // d disini menimpa global variable d (jika didefinisikan tanpa var, maka berefek ke global)
  return c+d;                         // function mengembalikan nilai 60
}

var c = 5;                            // c disini merupakan global variable
var d = 10;                           // d disini merupakan global variable
var e = foo();                        // tidak ada argument yang dikirim

console.log(c);                       // output: 20 (bukan 5, karena nilai c tertimpa saat didalam function)
console.log(d);                       // output: 40 (bukan 10, karena nilai d tertimpa saat didalam function)
console.log(e);                       // output: 60 (bukan 15, karena nilai var c & d tertimpa saat didalam function)
```

```Javascript
// =============
// F. VAR vs LET
// =============

/*
Penggunaan var dapat mempengaruhi nilai diluar scope (tidak aman!), sedangkan penggunaan let tidak mempengaruhi
nilai diluar scope (aman!). let sendiri merupakan fitur baru di ES6, tujuannya untuk "mengganti" penggunaan var.
*/

// F1. Perbandingan var & let (1)

for (var i=1; i<3; i++){
  console.log(i);
}
console.log(i);                       // output: 3

for (let j=1; j<3; j++){
  console.log(j);
}
console.log(j);                       // output: ReferenceError j is not defined

// F1. Perbandingan var & let (2)

var k = 1000;
for (var k=1; k<3; k++){
  console.log(k);
}
console.log(`Harganya Rp.${k}`);      // output: Harganya Rp.3 (nilai k global tertimpa, saat didalam perulangan)

let l = 1000;
for (let l=1; l<3; l++){
  console.log(l);
}
console.log(`Harganya Rp.${l}`);      // output: Harganya Rp.1000 (nilai l global tidak tertimpa)
```

```Javascript
// ========================
// G-1. JavaScript Hoisting
// ========================

/*
Hoisting terkait cara JavaScript mengeksekusi kode program, dimana terdapat 2 fase yaitu creation & execution.
Di fase creation, pertama-tama JavaScript akan "mengangkat" (hoisting) semua variabel & function yang dibuat
ke baris paling atas kode program, untuk setiap variable akan diisi nilai undefined, sedangkan function akan
diisi functionnya itu sendiri. Selanjutya, barulah masuk ke fase execution, dimana kode program akan dieksekusi
baris per baris, dari atas ke bawah. Gunakan tools visualusasi berikut: http://pythontutor.com/javascript.html
*/

// Contoh 1: Variable

// Contoh 1-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksA);                   // console.log(teksA);              🡲 output: ReferenceError teksA is not defined (STOP!)

// Contoh 1-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksB);                   // 𝘃𝗮𝗿 𝘁𝗲𝗸𝘀𝗕 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
console.log(teksC);                   // console.log(teksB);              🡲 output: undefined
var teksB = "Belajar JS";             // console.log(teksC);              🡲 output: ReferenceError teksC is not defined (STOP!)
                                      // var teksB = "Belajar JS";        🡲 baris ini tidak akan dieksekusi, karena error diatas
                                      
// Contoh 1-3                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksD);                   // 𝘃𝗮𝗿 𝘁𝗲𝗸𝘀𝗗 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var teksD = "Belajar JS";             // console.log(teksD);              🡲 output: undefined
console.log(teksD);                   // var teksD = "Belajar JS";
                                      // console.log(teksD);              🡲 output: Belajar JS

// Contoh 1-4                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(satu);                    // 𝘃𝗮𝗿 𝘀𝗮𝘁𝘂 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
console.log(dua);                     // 𝘃𝗮𝗿 𝗱𝘂𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var satu = "Belajar HTML";            // 𝘃𝗮𝗿 𝘁𝗶𝗴𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var dua = "Belajar CSS";              // console.log(satu);               🡲 output: undefined
console.log(tiga);                    // console.log(dua);                🡲 output: undefined
var tiga = "Belajar JS";              // var satu = "Belajar HTML";
console.log(satu);                    // var dua = "Belajar CSS";
                                      // console.log(tiga);               🡲 output: undefined
                                      // var tiga = "Belajar JS";
                                      // console.log(satu);               🡲 output: Belajar HTML

// Contoh 2: Function

// Contoh 2-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaPagi);                // 𝘀𝗮𝗽𝗮𝗣𝗮𝗴𝗶 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗣𝗮𝗴𝗶(){...}
console.log(sapaPagi());              // console.log(sapaPagi)            🡲 output: function sapaPagi(){...}
function sapaPagi(){                  // console.log(sapaPagi());         🡲 output: Selamat Pagi!
  console.log("Selamat Pagi!");       // function sapaPagi(){
}                                     //   console.log("Selamat Pagi!");
                                      // }                                🡲 output: undefined (terjadi karena tidak ada return)

// Contoh 2-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSiang);               // 𝘀𝗮𝗽𝗮𝗦𝗶𝗮𝗻𝗴 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗶𝗮𝗻𝗴(){...}
console.log(sapaSiang());             // console.log(sapaSiang)           🡲 output: function sapaSiang(){...}
function sapaSiang(){                 // console.log(sapaSiang());        🡲 output: Selamat Siang!
  return "Selamat Siang!";            // function sapaSiang(){
}                                     //   return "Selamat Siang!";
                                      // }                                🡲 karena terdapat return, maka tidak ada output apapun

// Contoh 2-3                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSore());              // 𝘀𝗮𝗽𝗮𝗦𝗼𝗿𝗲 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗼𝗿𝗲(){...}
function sapaSore(){                  // 𝘀𝗮𝗽𝗮𝗠𝗮𝗹𝗮𝗺 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗠𝗮𝗹𝗮𝗺(){...}
  return "Selamat Sore!";             // console.log(sapaSore());         🡲 output: Selamat Sore!
}                                     // function sapaSore(){
console.log(sapaMalam());             //   return "Selamat Sore!";
function sapaMalam(){                 // }
  return "Selamat Malam!";            // console.log(sapaMalam());        🡲 output: Selamat Malam!
}                                     // function sapaMalam(){
                                      //   return "Selamat Malam!";
                                      // }

// Contoh 3: Variable & Function

// Contoh 3-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSatu());              // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var nama = "Budi";                    // 𝘃𝗮𝗿 𝘂𝗺𝘂𝗿 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var umur = 25;                        // 𝘀𝗮𝗽𝗮𝗦𝗮𝘁𝘂 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗮𝘁𝘂(){...}
function sapaSatu(){                  // console.log(sapaSatu());         🡲 output: undefined, undefined tahun!
  return `${nama}, ${umur} tahun!`;   // var nama = "Budi";
}                                     // var umur = 25;
                                      // function sapaSatu(){
                                      //   return `${nama}, ${umur} tahun!`;
                                      // }

// Contoh 3-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
var nama = "Budi";                    // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var umur = 25;                        // 𝘃𝗮𝗿 𝘂𝗺𝘂𝗿 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
console.log(sapaDua());               // 𝘀𝗮𝗽𝗮𝗗𝘂𝗮 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗗𝘂𝗮(){...}
function sapaDua(){                   // var nama = "Budi";
  return `${nama}, ${umur} tahun!`;   // var umur = 25;
}                                     // console.log(sapaDua());          🡲 output: Budi, 25 tahun!
                                      // function sapaDua(){
                                      //   return `${nama}, ${umur} tahun!`;
                                      // }

// Contoh 4: Local Hoisting

// Contoh 4-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
var nama = "Budi Lorem";              // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;             🡲 Global Hoisting
var user = "@budilorem";              // 𝘃𝗮𝗿 𝘂𝘀𝗲𝗿 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;              🡲 Global Hoisting
function cetakURL(user){              // 𝗰𝗲𝘁𝗮𝗸𝗨𝗥𝗟 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗰𝗲𝘁𝗮𝗸𝗨𝗥𝗟(){...}🡲 Global Hoisting
  var twtURL = "http://twitter.com/"; // var nama = "Budi Lorem";
  return twtURL+user;                 // var user = "@budilorem";
}                                     // function cetakURL(user){
console.log(cetakURL(user));          //   𝘃𝗮𝗿 𝘁𝘄𝘁𝗨𝗥𝗟 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;         🡲 Local Hoisting di dalam function
                                      //   var twtURL = "http://twitter.com/";
                                      //   return twtURL+user;
                                      // }
                                      // console.log(cetakURL(user));     🡲 http://twitter.com/@budilorem

// Contoh 4-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
function luar(){                      // 𝗹𝘂𝗮𝗿 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗹𝘂𝗮𝗿(){...}        🡲 Global Hoisting
  console.log("A");                   // function luar(){
  function tengah(){                  //   𝘁𝗲𝗻𝗴𝗮𝗵 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘁𝗲𝗻𝗴𝗮𝗵(){...} 🡲 Local Hoisting di dalam function
    console.log("B");                 //   console.log("A");
    function dalam(){                 //   function tengah(){
      console.log("C");               //     𝗱𝗮𝗹𝗮𝗺 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗱𝗮𝗹𝗮𝗺(){...} 🡲 Local Hoisting di dalam function
    }                                 //     console.log("B");
    dalam();                          //     function dalam(){
  }                                   //       console.log("C");
  tengah();                           //     }
}                                     //     dalam();
luar();                               //   }
                                      //   tengah();
                                      // }
                                      // luar();                          🡲 urutan output: A, B, C

// Contoh 5: More Example             ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
function funA(){                      // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
  var nama = "Budi";                  // 𝗳𝘂𝗻𝗔 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗳𝘂𝗻𝗔(){...}
  console.log(nama);                  // 𝗳𝘂𝗻𝗕 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗳𝘂𝗻𝗕(){...}
}                                     // function funA(){
function funB(){                      //   𝘃𝗮𝗿 𝗻𝗮𝗺𝗲 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
  console.log(nama);                  //   var nama = "Budi";
}                                     //   console.log(nama);
console.log(nama);                    // }
var nama = "Jaka";                    // function funB(){
funA();                               //   console.log(nama);
funB("Tono");                         // }
console.log(nama);                    // console.log(nama);               🡲 output: undefined
                                      // var nama = "Jaka";
                                      // funA();                          🡲 output: Budi
                                      // funB("Tono");                    🡲 output: Jaka (bukan Tono ya!)
                                      // console.log(nama);               🡲 output: Jaka
```

```Javascript
// ===================================
// G-2. Kesimpulan JavaScript Hoisting
// ===================================

/*
➊ Selalu definisikan variable (var) diawal kode program/function, dan sebaiknya langsung diisi nilai, agar tidak undefined.
➋ Pemanggilan function bisa dimana saja, tidak peduli pendefinisian functionnya berada di atas maupun bawah kode program.
➌ Agar lebih "aman", ganti penggunaan var dengan let. Let akan menampilkan error saat ia dipanggil namun belum didefinisikan
  di baris atas kode program (ini yang seharusnya terjadi), sedangkan var malah diisi undefined. Perhatikan contoh dibawah:
*/

// Contoh VAR                         ᴠᴀʀ ɪᴛᴜ ᴛɪᴅᴀᴋ ᴀᴍᴀɴ:
console.log(a);                       // output: undefined
var a = "Hello World!";               // seharusnya sih error, tapi karena efek hoisting, jadilah undefined (tidak professional)

// Contoh LET                         ʟᴇᴛ ɪᴛᴜ ᴀᴍᴀɴ & ᴘʀᴏꜰᴇꜱꜱɪᴏɴᴀʟ:
console.log(b);                       // output: ReferenceError Cannot access 'b' before initialization
let b = "Hello World!";               // ini artinya kita memang harus mendefinisikan var/let dulu, sebelum dipakai! (professional)
```

```Javascript
// =======================================
// H. Function sebagai First-Class Citizen
// =======================================

/*
Hal yang unik dari JavaScript yaitu function dianggap sebagai tipe data, ini berarti:
➊ Function dapat disimpan ke dalam variable (a.k.a Function Expressions)
➋ Function dapat digunakan sebagai argument layaknya tipe data biasa
*/

// H1. Function Expressions

var hitung = function ratarata(a, b){ // function ratarata disimpan ke dalam variable hitung
  return (a+b)/2;
}
console.log(hitung(4, 8));            // output: 6
console.log(ratarata(4, 8));          // output: ReferenceError ratarata is not defined

// H2. Anonymous Functions

var hitung = function(a, b){          // Function Expressions tanpa nama function disebut sebagai
  return (a+b)/2;                     // Anonymous Functions, ini yang banyak dipakai nantinya!
}
console.log(hitung(4, 8));            // output: 6

// H3. Return Function sebagai Argument

function rerata(a, b){
  return (a+b)/2;
}
function tambah(c, d){
  return c+d;
}
var hasil = tambah(6, rerata(4, 8));  // Hasil return function rerata(4, 8) digunakan sebagai argument
console.log(hasil);                   // output: 12

// H4. Function sebagai Argument (1)

function rerata(a, b){
  return (a+b)/2;
}
function tambah(c, d){                // Step 2 🡲 Parameter d akan menangkap function rerata dari argument 
  return c+d(4, 8);                   // Step 3 🡲 Dengan demikian d(4, 8) akan menjadi rerata(4, 8)
}
var hasil = tambah(6, rerata);        // Step 1 🡲 Mengirim function bernama rerata sebagai sebuah argument
console.log(hasil);                   // output: 12

// H5. Function sebagai Argument (2)

function foo(apa){
  alert(apa);                         // Step 4 🡲 foo("Belajar JS") akan dieksekusi sebagai alert("Belajar JS")
}
function salam(bar){                  // Step 2 🡲 Parameter bar akan menangkap function foo dari argument
  bar("Belajar JS");                  // Step 3 🡲 Dengan demikian bar("Belajar JS") menjadi foo("Belajar JS")
}
salam(foo);                           // Step 1 🡲 Mengirim function bernama foo sebagai sebuah argument
```

```Javascript
// =======================
// I. Arrow Function (ES6)
// =======================

/*
Arrow Function merupakan fitur baru ES6, digunakan sebagai alternatif penulisan Function Expressions. Arrow Function lebih
sederhana secara penulisan syntax, namun intinya bukan itu, melainkan nanti akan banyak dipakai di konsep JavaScript Object.
*/

// Contoh tanpa Argument

var pagiA = function(){ return "Selamat Pagi!"; };    // Penulisan Function Expressions biasa
var pagiB = () => { return "Selamat Pagi!"; };        // Penulisan Function Expressions dengan Arrow Function

console.log(pagiA());                                 // output: Selamat Pagi!
console.log(pagiB());                                 // output: Selamat Pagi!

// Contoh dengan Argument

var totalA = function(a, b, c){ return a+b+c; };      // Penulisan Function Expressions biasa
var totalB = (a, b, c) => { return a+b+c; };          // Penulisan Function Expressions dengan Arrow Function

console.log(totalA(1, 2, 3));                         // output: 6
console.log(totalB(1, 2, 3));                         // output: 6
```

<br>
<div id="bab10"></div>

# 10. JavaScript Object <a href="#daftarisi">🡹</a>

```Javascript
// ============
// A. BLABLABLA
// ============
```
