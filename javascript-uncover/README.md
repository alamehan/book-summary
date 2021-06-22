# 📘 JavaScript Uncover

Materi utama di page ini diambil dari buku <a href="https://www.duniailkom.com/javascript-uncover-panduan-belajar-javascript-untuk-pemula/">JavaScript Uncover by Duniailkom.com</a>. Selebihnya merupakan materi tambahan (pelengkap), gabungan dari website <a href="https://www.youtube.com/channel/UCkXmLjEr95LVtGuIm3l2dPg">Web Programming UNPAS</a>, <a href="https://www.youtube.com/channel/UC14ZKB9XsDZbnHVmr4AmUpQ">Programmer Zaman Now</a>, <a href="https://bukureact.id/">BukuReact.id</a>, <a href="https://www.w3schools.com/">W3Schools</a> dan <a href="https://www.w3docs.com/">W3Docs</a>. Untuk Cheat Sheet dapat diakses di <a href="https://www.w3schools.com/jsref/default.asp">W3Schools: JavaScript Reference</a>. Semoga bermanfaat 😊. 

**Summary by**: alamehan.github.io

<div id="daftarisi"></div>

| Judul BAB                                                     	| Estimasi Baca 	|
|---------------------------------------------------------------	|---------------	|
| <a href="#bab01">1. Berkenalan Dengan JavaScript</a>          	| ± 2 menit     	|
| <a href="#bab02">2. Sejarah dan Perkembangan JavaScript</a>   	| ± 5 menit     	|
| <a href="#bab03">3. Menjalankan Kode Program JavaScript</a>   	| ± 4 menit     	|
| <a href="#bab04">4. Aturan Dasar, Variabel dan Konstanta</a>  	| ± 1 menit     	|
| <a href="#bab05">5. Variabel dan Konstanta</a>                	| ± 4 menit     	|
| <a href="#bab06">6. Tipe Data JavaScript</a>                  	| ± 7 menit     	|
| <a href="#bab07">7. Operator JavaScript</a>                   	| ± 8 menit     	|
| <a href="#bab08">8. Struktur Logika dan Perulangan</a>        	| ± 4 menit     	|
| <a href="#bab09">9. Function</a>                              	| ± 18 menit    	|
| <a href="#bab10">10. JavaScript Object</a>                    	| ± 4 menit     	|
| <a href="#bab11">11. Object Oriented Programming (OOP)</a>    	| ± 12 menit    	|
| <a href="#bab12">12. JavaScript Native Object</a>             	| ± 40 menit     	|
| <a href="#bab13">13. Global Property dan Global Function</a>    | ± 2 menit     	|
| <a href="#bab14">14. Document Object Model (DOM)</a>            | ± 15 menit     	|
| <a href="#bab15">15. DOM Event</a>                              | ± X menit     	|
| <a href="#babxx">XX. Materi Tambahan: Advanced JavaScript</a> 	| ± X menit     	|
| <p>Estimasi Total Durasi Baca</p> 	                            | ± 3 Jam         |

<!-- Estimasi baca hasil generate dari  : https://wordcounter.net/ -->
<!-- Markdown table hasil generate dari : https://www.tablesgenerator.com/markdown_tables -->

<div id="bab01"></div>

# 1. Berkenalan Dengan JavaScript <a href="#daftarisi">🡹</a>

<img src="images/BAB-1.png">

1. JavaScript merupakan bagian dari 5 materi dasar web programming, yakni: HTML, CSS, PHP, MySQL dan JavaScript. Bersama-sama dengan HTML dan CSS, ketiganya berbagi peran masing-masing. HTML digunakan untuk membuat struktur dan isi dari halaman web (content). CSS untuk mempercantik tampilan website (design). Sedangkan JavaScript berfungsi menangani interaksi (behavior).**“HTML for content, CSS for presentation and JavaScript for behavior”**.
2. HTML, CSS dan JavaScript sama-sama termasuk ke dalam kelompok “client side programming language”, yakni bahasa pemrograman yang dijalankan di sisi client (web browser). PHP juga merupakan bahasa pemrograman web, tapi berada di dalam server, sehingga disebut sebagai “server side programming language”.
3. **Client Side Programming**: Ini artinya, untuk menjalankan JavaScript kita hanya butuh 2 aplikasi, yakni text editor dan web browser. Text editor digunakan membuat kode JavaScript, dan kode JavaScript tersebut bisa langsung diakses dari web browser. Kita pun bisa melihat kode JavaScript yang digunakan dari sebuah website (sama seperti HTML dan CSS). Silahkan buka website apa saja, klik kanan lalu pilih View Page Source.
4. **Server Side Programming**: Untuk menjalankan kode program PHP kita harus menggunakan aplikasi seperti Apache web server (yang merupakan bagian dari XAMPP). Kita tidak bisa melihat kode PHP yang digunakan sebuah website secara langsung layaknya HTML, CSS dan JavaScript.
5. Perkembangan JavaScript yang sangat pesat akhir-akhir ini melahirkan banyak penerapan lain dari JavaScript. Sebagai contoh, **Node.js** adalah penggunaan JavaScript di sisi server. Dalam buku ini kita hanya fokus membahas penggunaan JavaScript di sisi client (di dalam web browser).
6. Apa yang akan kita pelajari dalam buku ini terdiri dari 2 kelompok besar: JavaScript dan **DOM (Document Object Model)**. JavaScript adalah bahasa pemrograman, sedangkan DOM merupakan objek HTML yang akan kita manipulasi, seperti teks, gambar, form, tombol, title bar web browser, event, dll. Bahasa pemrograman JavaScript dikembangkan oleh ECMA, sedangkan DOM dikembangkan oleh W3C (organisasi yang juga membuat standar HTML dan CSS). Bisa dibilang, JavaScript sepenuhnya terpisah dari HTML.
7. Setelah mempelajari JavaScript, barulah kita masuk ke DOM. Disinilah JavaScript digunakan untuk mengubah total tampilan halaman web. Jadi, jika anda merasa jenuh dengan pembahasan dari BAB 2 hingga 13, tahan dulu! Paksakan untuk terus mempelajarinya. Dengan pemahaman JavaScript yang cukup, kita memiliki pondasi yang kuat untuk memanipulasi objek HTML yang nantinya diakses lewat DOM mulai dari BAB 14 hingga akhir buku.

<br>
<div id="bab02"></div>

# 2. Sejarah dan Perkembangan JavaScript <a href="#daftarisi">🡹</a>

<img src="images/BAB-2-1.png">

1. **Brendan Eich** membuat prototype bahasa baru dalam 10 hari. Pada Mei 1995, bahasa pemrograman “Mocha” lahir. Bahasa pemrograman inilah yang diputuskan untuk digunakan Netscape. Bahasa pemograman Mocha dirilis pertama kali ke dalam versi beta Netscape Navigator 2.0 di bulan September 1995, tetapi dengan menggunakan nama baru: LiveScript. Umur dari LiveScript ternyata tidak lama. 3 bulan kemudian, tepatnya Desember 1995, hadir Netscape Navigator 2.0 beta 3 dengan sebuah bahasa baru: JavaScript. Sebenarnya ini bukanlah bahasa pemrograman baru, tapi perubahan nama dari LiveScript. Nama JavaScript dipilih agar Netscape bisa ‘nompang tenar’ dari bahasa pemrograman JAVA milik Sun Microsystems, yang pada masa itu sangat populer di kalangan programmer.

<img src="images/BAB-2-2.png">

2. “The first browser war”, perang web browser pertama antara Internet Explorer buatan Microsoft vs Netscape Navigator buatan Netscape Communications.
3. **ECMAScript** adalah sebuah standar bahasa pemrograman komputer, dimana JavaScript merupakan salah satu implementasi dari ECMAScript. JavaScript tidak bisa dijadikan standar karena masalah merk “JAVA” yang merupakan trademark SUN Micosystem (sekarang sudah diakuisisi Oracle). Intinya: Standarisasi **JavaScript = ECMAScript**. EMCAScript digunakan hanya saat merujuk ke versi dari JavaScript.
4. Pengembangan ECMAScript 4 berhenti di tengah jalan, ini disebabkan perbedaan pendapat antar anggota **komite TC39**, terutama mengenai fitur apa yang harus ada di ECMAScript 4. Proses “perseteruan” berlangsung cukup lama, memakan waktu hingga 10 tahun (sampai dengan 2009). Selama jangka waktu tersebut, tidak ada versi baru dari ECMAScript.
5. Di pasar web browser, Internet Explorer menjadi sangat dominan, menguasai lebih dari 80% -90% market share dari tahun 2001 hingga 2009. Netscape Navigator bisa dibilang sudah punah pada tahun 2004. Web browser Opera hadir sebagai alternatif, tapi tidak bisa berbuat banyak.
6. **AJAX**, singkatan dari **(Asynchronous JavaScript and XML)**. AJAX memungkinkan sebuah halaman web berkomunikasi langsung dengan server tanpa harus di-reload. Komunikasi antara web browser dengan web server berlangsung di latar belakang (background) secara asynchronous, hasilnya website menjadi lebih dinamis. Sebagai contoh, halaman registrasi bisa langsung mengecek apakah username yang diinput sudah ada di database atau belum. Ini dapat dilakukan sesaat setelah user berpindah dari kolom input username ke kolom dibawahnya. Tanpa menggunakan AJAX, proses pengecekan baru berlangsung saat user selesai mengisi form dan men-klik tombol submit (karena pengecekan harus dilakukan ke database yang ada di server).
7. Selain AJAX, berkembang juga berbagai komunitas dan library JavaScript seperti Prototype, **jQuery**, Dojo Toolkit, dan MooTools. Masa-masa ini bisa dibilang awal kebangkitan JavaScript. Dengan menggunakan library seperti jQuery, perbedaan implementasi ECMAScript dari berbagai web browser bisa diatasi dengan mudah. jQuery menyediakan ‘abstraction layer’ agar web programmer bisa berfokus kepada fitur yang ingin dicapai. Programmer yang sebelumnya “anti” dengan JavaScript (karena susahnya mengatasi perbedaan fitur web browser), mulai melirik library seperti jQuery.
8. Setelah perang web browser pertama berakhir dengan kekalahan telak Netscape, perang kedua segera mulai dengan dirilisnya Mozilla Firefox (sebagai "Reingkarnasi Netscape"). Dengan cepat Firefox menjadi web browser favorit yang sepertinya akan segera menggusur IE. Puncaknya di tahun 2010 Firefox menguasai sekitar 30% pasar web browser, walaupun IE masih tetap dominan tapi setiap tahun mengalami tren penurunan. Tidak lama lagi sepertinya Firefox bisa menjadi web browser paling populer menggantikan IE. Namun harapan ini pupus karena muncul web browser baru dari raja mesin pencari: Google Chrome yang dirilis pada Desember 2008. Didukung dengan promosi gencar, nama besar Google, fitur menawan, dan eksekusi yang cepat, membuat Google Chrome segera menjadi web browser paling banyak digunakan hingga saat ini, mengalahkan IE, Firefox, dan Opera.

<img src="images/BAB-2-3.png">

9. ECMAScript 6 atau ES6 atau ECMAScript 2015 dirilis pada bulan Juni 2015. Cukup banyak penambahan baru pada versi ini, sebagian besar merupakan fitur lanjutan untuk membuat aplikasi yang memiliki kompleksitas tinggi, seperti penggunaan **JavaScript di server menggunakan Node.js**. Mulai dari ECMAScript 6 dan selanjutnya, penamaan ECMAScript akan menggunakan nama tahun saat standar tersebut dirilis, seperti ECMAScript 2015, ECMAScript 2016, dst. Banyak perdebatan mengenai pilihan nama ini, sehingga masih sering disebut sebagai ECMAScript 6 (ES6). Dalam buku ini kita lebih banyak membahas ECMAScript 5. Walaupun menggunakan ECMAScript 5, dasar JavaScript yang ada di buku ini tetap valid untuk versi 6 dan versi 7. Fitur tambahan yang ada di ECMAScript 6 dan ECMAScript 7 juga lebih banyak ke materi lanjutan yang terlalu kompleks jika dimasukkan ke buku JavaScript untuk pemula. ES6 dan ES7 lebih cocok jika anda berniat mempelajari JavaScript sebagai bahasa pemrograman server menggunakan Node.js.
10. **JavaScript Engine** adalah mekanisme internal yang dimiliki oleh web browser untuk menjalankan kode JavaScript. JavaScript Engine dapat disamakan dengan compiler dalam bahasa pemograman lain, yakni algoritma yang digunakan untuk menjalankan JavaScript. Semakin cepat sebuah web browser menjalankan JavaScript akan semakin baik. **V8** adalah nama JavaScript Engine untuk Google Chrome, **SpiderMonkey** untuk Mozilla Firefox, dan **Chakra** untuk Internet Explorer.
11. Perkembangan JavaScript Saat Ini: Website yang tidak berbentuk “website”, tetapi menyerupai aplikasi desktop yang dikenal sebagai **Single-page Application (SPA)**. Contoh dari Single-page Application ini seperti aplikasi Google: Gmail, GDrive, Google Doc, dll. Di website tersebut, halamannya akan tetap sama, tidak di reload seperti layaknya sebuah website.
12. Namun perlu juga dipahami bahwa walaupun materi di eBook JavaScript Uncover sudah lumayan rumit, ini barulah dasar dari JavaScript. Jika anda serius ingin mempelajari JavaScript lebih jauh lagi, bisa lanjut ke library seperti **jQuery**, framework seperti **AngularJS**, **ReactJS** maupun **VueJS**, atau ke server menggunakan **Node.js**.
13. Timeline sejarah JavaScript dari awal lahir hingga saat ini secara ringkas dapat diakses <a href="https://www.jetbrains.com/lp/javascript-25/">disini</a>. Daftar feature baru dari mulai **ES6 hingga ES.Next** dapat diakses di <a href="https://en.wikipedia.org/wiki/ECMAScript">Wikipedia</a>, <a href="https://www.javascripttutorial.net/es-next/">JavaScriptTutorial</a>, <a href="https://jsfeatures.in/">JSFeatures</a>, <a href="https://www.freecodecamp.org/news/es5-to-esnext-heres-every-feature-added-to-javascript-since-2015-d0c255e13c6e/">FreeCodeCamp</a>, <a href="https://github.com/daumann/ECMAScript-new-features-list">GitHub</a>, <a href="https://javascript.info/">JavaScriptInfo</a>.
  
<br>
<div id="bab03"></div>

# 3. Menjalankan Kode Program JavaScript <a href="#daftarisi">🡹</a>

<img src="images/BAB-3-1.png">

```HTML
<!-- A. Inline JavaScript -->

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
<hr>

```HTML
<!-- B. Internal JavaScript -->

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
<hr>

```HTML
<!-- C. External JavaScript -->

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

1. Menempatkan kode JavaScript di bagian atas banyak ditemukan. Namun berkaitan dengan masalah performa, beberapa developer web menyarankan meletakkan JavaScript dibagian bawah tag ```<body>```, yakni sebelum tag penutup ```</body>```, sebagaimana yang dijelaskan dari sebuah artikel di Yahoo Developer Network: Best Practices for Speeding Up Your Web Site. 
2. Cara web browser dalam menampilkan sebuah halaman web, yakni secara berurutan dari atas ke bawah, mulai dari baris pertama hingga baris terakhir.
3. Fitur **cache** dari web browser bisa mempercepat pengaksesan website dengan cara menyimpan file JavaScript di dalam cache.
4. Dengan memanggil file external JavaScript dari bagian bawah tag ```<body>```, memberi kesempatan web browser untuk memproses kode HTML terlebih dahulu, baru kemudian mendownload file JavaScript. Efeknya, pengujung web bisa langsung melihat tampilan web selama proses ini, tidak hanya halaman kosong. 
5. Atribut **async** dan **defer**: kita bisa mengatur kapan dan bagaimana file external JavaScript diproses. Kedua atribut ini memungkinkan penulisan tag ```<script>``` tidak harus di bawah tag ```<body>```. Jika atribut **async** ditambahkan ke dalam tag ```<script>```, file JavaScript akan diproses pada saat yang bersamaan dengan kode HTML (secara simultan). Dengan kata lain, web browser tidak “terkunci” untuk menjalankan kode JavaScript. Metode ini juga dikenal dengan istilah **Asynchronous JavaScript** (Di proses secara bersamaan = Asynchronous). 
6. Dengan tambahan atribut **async**, kode HTML tetap diproses sembari mendownload file JavaScript. Dengan kata lain, web browser tidak masuk ke dalam Render-Blocking JavaScript. Atribut **defer** digunakan untuk mengatur kapan file JavaScript dijalankan. Dengan atribut ini, file JavaScript baru di download dan dieksekusi setelah seluruh kode HTML selesai diproses. Efek dari atribut **async** dan **defer** mungkin terdengar sama. Perbedaaan mendasar adalah, **async** digunakan untuk mengatur cara eksekusi kode JavaScript, sedangkan **defer** untuk mengatur kapan file JavaScript tersebut di download dan diproses.
7. Tambahan atribut **async** dan **defer** dari HTML5 membawa perubahan terkait posisi terbaik peletakan kode JavaScript. Standar saat ini adalah menempatkan kode JavaScript di bagian ```<head>``` dengan tambahan atribut **async**. Alasannya, web browser bisa langsung mengeksekusi file JavaScript pada saat yang bersamaan dengan proses kode HTML, sehingga website dapat ditampilkan dengan lebih cepat (tidak mengalami Render-Blocking JavaScript). Untuk kode JavaScript yang tidak terlalu penting (dan bisa menunggu), tambahkan atribut **defer**. Sebagai tambahan, atribut **async** dan **defer** hanya berlaku untuk external JavaScript. Untuk internal JavaScript, atribut ini akan diabaikan dan posisi terbaik tetap di bagian bawah tag ```<body>```.

```HTML
<!-- Posisi Terbaik Internal & External JavaScript -->

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

8. Berbeda dengan mayoritas bahasa pemrograman lain, secara default kita tidak bisa melihat pesan error dari JavaScript. Padahal ini sangat penting selama pembuatan kode program. Tidak ada yang lebih membuat pusing dari program yang tidak berjalan, namun tidak tahu salahnya dimana. Untuk menampilkan pesan error JavaScript, kita bisa menggunakan menu **Web developer tools** bawaan web browser. Setiap web browser modern memiliki tools seperti ini.

<img src="images/BAB-3-2.png">

9. Tab Inspector (1) bisa digunakan untuk menelusuri seluruh kode HTML yang terdapat di dalam halaman web (2), di sisi kanan kita bisa melihat kode CSS yang digunakan oleh tag HTML tersebut (3). Jika anda sering mengedit kode CSS, tab Inspector ini sangat bermanfaat untuk melihat dan menjalankan (mengedit) kode CSS tanpa perlu mengubah file asli.
10. Tab yang sering kita akses selama membuat kode program JavaScript adalah **Tab Console**, yang berada di sebelah kanan tab Inspector. Apabila kode yang anda buat tidak berjalan sebagaimana mestinya, hal pertama yang harus dilakukan adalah memeriksa tab Console ini. Selain menampilkan pesan error, di dalam tab Console kita juga bisa menjalankan kode program JavaScript secara langsung, tanpa harus menulisnya di dalam file HTML. Fungsi ```console.log()``` berguna untuk menampilkan hasil kode program ke tab Console.
11. Salah satu kelemahan (sekaligus keunggulan) dari JavaScript adalah, pengunjung web bisa mematikan JavaScript yang ada di web browser mereka. Tag ```<noscript>``` bisa digunakan untuk menampilkan teks keterangan yang hanya bisa terlihat pada web browser yang tidak memiliki JavaScript (atau JavaScriptnya dimatikan).

```HTML
<!-- Contoh Penggunaan <noscript> -->

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

<img src="images/BAB-4.png">

1. **Statement** adalah sebutan untuk sebuah baris perintah JavaScript. Walaupun saya menggunakan kata “baris”, bisa saja sebuah Statement butuh beberapa baris (seperti Function). Atau dalam 1 baris bisa terdiri dari beberapa Statement. Setiap Statement diakhiri dengan tanda titik koma (semi colon): ‘ ; ‘. Sebenarnya, tanda titik koma untuk mengakhiri Statement JavaScript ini adalah opsional. Artinya, boleh tidak ditulis sepanjang Statement tersebut harus berada dalam baris baru (1 Statement, 1 baris). Sebaiknya kita tetap menambahkan tanda titik koma untuk mengakhiri setiap Statement di dalam JavaScript.
2. **Case Sensitivity**: JavaScript termasuk bahasa pemrograman yang bersifat case sensitif, artinya huruf besar dan huruf kecil dianggap berbeda. Salah menulis huruf sangat sering terjadi.
3. **Whitespace** berarti karakter “kosong” seperti spasi, tab, atau baris baru (new line). Secara umum di dalam JavaScript whitespace akan diabaikan.
4. **Indenting** adalah istilah yang digunakan untuk menambahkan spasi atau tab diawal baris kode program. Tujuannya agar kode program lebih mudah dibaca terutama jika kode program tersebut sudah mencapai puluhan atau ratusan baris kode program. 
5. **Comment** atau baris komentar adalah sebutan untuk kode program yang tidak akan di eksekusi oleh JavaScript. Selain sebagai dokumentasi, komentar juga sering digunakan untuk menghentikan sementara baris kode program. Di JavaScript, Comment ditulis menggunakan karakter ```// komentar``` (untuk single line) & ```/* komentar */``` (untuk multiple line). Di sepanjang contoh kode yang disertakan di BAB-BAB selanjutnya, penggunaan Comment akan banyak sekali ditemukan (sebagai dokumentasi/keterangan dari baris sebuah kode).

<br>
<div id="bab05"></div>

# 5. Variabel dan Konstanta <a href="#daftarisi">🡹</a>

<img src="images/BAB-5.png">

1. Secara sederhana, Variable adalah “penampung” dari sebuah data. Disebut Variable karena data yang kita simpan bisa berubah-ubah sepanjang kode program (isinya tidak tetap). ```var angka = 192;``` **Operasi Asignment** atau memberikan nilai ke sebuah Variable dibaca dari kanan ke kiri (right-to-left, baca selengkapnya <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence">disini</a>). Artinya, 192 “dimasukkan” sebagai nilai ke Variable ```angka```.
2. JavaScript termasuk ke dalam bahasa pemrograman **Typeless Programming Language**, yakni kelompok bahasa pemrograman yang variabelnya bisa diisi dengan tipe data apa saja tanpa harus dideklarasikan terlebih dahulu.
3. Apabila anda sering mengikuti tutorial programming dari situs berbahasa inggris, nama Variable **foo**, **bar**, dan **baz** sering digunakan. Ketiganya dikenal sebagai **dummy Variable**, yakni Variable yang fungsinya hanya sebagai contoh. Mirip seperti teks “Lorem Ipsum dolor sit amet” dalam bidang design.
4. Kita bisa memberi nama apa saja untuk Variable, apakah itu ```angka```, ```foo```, ```bar```, ```andi```, atau ```username```. Selain Variable, kita juga bebas untuk membuat nama Konstanta, Function, maupun Object. Semua inilah yang termasuk ke dalam kelompok **Identifier**. Identifier di dalam JavaScript memiliki aturan sebagai berikut:
   - Bisa terdiri dari huruf, angka, garis bawah “ _ ” (underscore), dan tanda dollar “ $ “ (dollar sign). Selain itu, dianggap sebagai karakter ilegal (tidak boleh digunakan). 
   - Karakter pertama dari Identifier tidak boleh berupa angka. Angka hanya bisa digunakan sebagai karakter kedua dan seterusnya.
   - Bersifat case sensitive, dimana huruf besar dan kecil dianggap berbeda.
   - Harus selain dari **reserved keyword**, yakni kata khusus yang berfungsi sebagai perintah di dalam pemrograman JavaScript, seperti ```var```, ```while```, ```function```, dll.
5. Di CSS kita menggunakan cara penulisan selector yang dipisah dengan tanda “ - ”, seperti ```main-box```, ```left-sidebar```, dan ```single-post```. Di PHP kita mengenal **Snake Case**, yakni menggunakan huruf kecil dan tanda underscore sebagai pemisah Variable, seperti ```jumlah_barang```, ```nama_dosen```, dan ```alamat_siswa```. Di JavaScript menggunakan **CamelCase**. CamelCase adalah cara penulisan Variable dimana jika sebuah Variable terdiri dari beberapa kata, huruf pertama dari kata kedua dan seterusnya diubah menjadi huruf besar, seperti: ```banyakAnggota```, ```totalBiaya```, ```mainBox```, atau ```jumlahKlikSatuHari```. Jika Variable tersebut hanya terdiri dari 1 kata, ditulis dengan huruf kecil semua.
6. **Strict Mode** memaksa JavaScript menampilkan error (di Tab Console) pada kode program yang seharusnya bisa berjalan “normal”. Tujuannya, meminimalisir kemungkinan bug karena penulisan yang salah, typo, dan berbagai hal lain. Strict mode sepenuhnya opsional dan mungkin tidak bisa selalu anda gunakan, terutama jika terdapat kode JavaScript pendahulu yang terlalu rumit untuk diubah semuanya. Strict Mode akan membuat web browser menampilkan error dimana sebelumnya hanya ada **“silent error”**. Salah satunya ketika membuat Variable tanpa perintah ```var```. Untuk masuk ke dalam Strict Mode, tambahkan String ```"use strict";``` di baris pertama kode JavaScript atau di baris paling awal dari sebuah Function.
7. EcmaScript 6 membawa fitur baru ke dalam JavaScript, yakni menggunakan perintah ```let``` untuk membuat Variable (sebagai alternatif dari ```var```). Perbedaan mendasar dari ```var``` dan ```let``` adalah terkait dengan **Variable scope**, yakni di bagian mana sebuah Variable masih bisa diakses. Penjelasan mengenai Variable scope akan saya bahas pada BAB tentang Function.
8. Konstanta (```const```) dapat dikatakan sebagai Variable yang tidak bisa diubah sepanjang kode program. Setelah Konstanta ditulis dan diberi nilai awal, isi Konstanta tersebut tidak bisa ditukar dengan nilai lain. Berbeda dengan Variable yang menggunakan **CamelCase**, Konstanta biasa ditulis menggunakan huruf besar dan garis bawah (underscore) sebagai pemisah kata.
9. Rekap format penulisan: Variable diawali huruf kecil (```total```, ```totalBiaya```, dst), Konstanta huruf besar semua (```PI```, ```RUMUS_A```, dst), dan Class diawali huruf besar (```Mobil```, ```MobilBaru```, dst). **Class dibahas di BAB 11**. Tujuan dari format penulisan ini yaitu agar programmer dapat dengan mudah membedakan mana Variabel, Konstanta maupun Class.

```HTML
<!-- Var, Let & Const -->

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

10. Berdasarkan contoh di atas: Variable ```harga```, let ```namaLengkap```, dan Konstanta ```NILAI_PI``` adalah **Identifier**. Sedangkan ```12000```, ```"Rudi Siswoyo"```, dan ```3.14``` adalah **Literal**.

<br>
<div id="bab06"></div>

# 6. Tipe Data JavaScript <a href="#daftarisi">🡹</a>

<img src="images/BAB-6.png">

1. Secara garis besar, tipe data dalam JavaScript terdiri dari 2 kelompok, yakni tipe data primitif (primitive type), dan tipe data object. Tipe data primitif disebut demikian karena tipe data ini “sederhana” dan hanya terdiri dari 1 nilai. Di dalam JavaScript terdapat 6 **tipe data primitif**, yaitu: **Number, String, Boolean, Null, Undefined, Symbol**. Sedangkan tipe data object, bisa disebut sebagai tipe data “khusus” yang prilaku dan isinya bermacam-macam. Adapun **tipe data object** bawaan JavaScript yaitu: **Array, RegExp, Date, Map, WeakMap, Set, WeakSet.**
2. Untuk tipe data Object, dalam BAB ini saya hanya membahas Object Array. Tipe data Object Date dan RegExp akan dibahas dalam BAB tersendiri karena butuh penjelasan yang cukup panjang, termasuk cara membuat object bentukan sendiri. Tipe data Symbol, Map, WeakMap, Set dan WeakSet adalah tipe data baru dalam ECMAScript 6. Tipe data ini tidak akan saya bahas karena termasuk materi lanjutan yang cukup kompleks untuk pemula.

```Javascript
// ===================
// A. Tipe Data Number
// ===================

var numA = 100;                       // Angka bulat
var numB = -100;                      // Angka bulat negatif
var numC = 0.66634;                   // Angka pecahan
var numD = -0.66634;                  // Angka pecahan negatif
var numE = 3e3;                       // ≈ 3 x 10^3
var numF = 0.4e-3;                    // ≈0.4 x 10^-3
var numG = 999;                       // Desimal (basis 10)
var numH = 0b1111100111;              // Biner (basis 2), diawali 0b
var numI = 0o1747;                    // Oktal (basis 8), diawali 0o
var numJ = 0x3E7;                     // Heksadesimal (basis 16), diawali 0x
var numK = 9/"a"; console.log(numK);  // Output: NaN (Not a Number)
var numL = 9/0; console.log(numL);    // Output: Infinity (Tak Hingga)
```
<hr>

```Javascript
// ===================
// B. Tipe Data String
// ===================

var strA = "Hello World!";            // String dengan kutip dua
var strB = 'Hello World!';            // String dengan kutip satu
var strC = "Hari Jum'at";             // Kutip satu di dalam kutip dua
var strD = 'Dia berkata: "Hey"';      // Kutip dua di dalam kutip satu
var strE = "Dia berkata: \"Hey\"";    // Kutip dua di dalam kutip dua, pakai escape character (\)
var strF = 'Hari Jum\'at';            // Kutip satu di dalam kutip satu, pakai escape character (\)
var strG = "\u2764 You!"              // Contoh pemakaian Unicode ⇨ Hasilnya: ❤ You!

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

📚 Daftar Karakter Latin-1 & Unicode: http://unicode-table.com/
*/

// Template String (Template Literals)

var strH = "Indonesia";               // Coba ganti nilainya menjadi String apapun (bebas)
var strI = "Bahasa " + strH;          // Sebelum ada fitur Template String ES6 ⇨ Menggunakan concatenation (+)
var strJ = `Bahasa ${strH}`;          // Setelah ada fitur Template String ES6 ⇨ Langsung di dalam backtick (``)
console.log(strJ);                    // Output: Bahasa Indonesia

var number  = 24;                                         // Coba ganti nilainya menjadi berapapun (bebas)
var result  = `${number} ditambah 6 = ${number+6}`;       // Template String bisa dipakai juga untuk expressions
console.log(result);                                      // Output: 24 ditambah 6 = 30
```
<hr>

```Javascript
// ====================
// C. Tipe Data Boolean
// ====================

var bolA = true;                      // Bernilai true, biasanya di pakai di if, else, while, dan do while
var bolB = false;                     // Bernilai false, biasanya di pakai di if, else, while, dan do while
```
<hr>

```Javascript
// ======================================
// D. Tipe Data Nullish: Null & Undefined
// ======================================

var nudA = null;                      // Keadaan dimana data "kosong", biasanya sengaja diinput oleh programmer
var nudB = undefined;                 // Keadaan dimana data "tidak terdefinisi", biasanya terjadi karena error

// Kasus yang menghasilkan Undefined

var und1;
console.log(und1);                    // Output: undefined (Var yang dibuat tanpa langsung diisi nilai, menjadi Undefined)

var und2 = [1, 2, 3];
console.log(und2[3]);                 // Output: undefined (Mengakses Array diluar indeks yang dibuat, menjadi Undefined)

var und3 = {nama: "iyan", umur: 24};
console.log(und3["alamat"]);          // Output: undefined (Mengakses Object diluar key yang dibuat, menjadi Undefined)
                                      // 𝗡𝗼𝘁𝗲: 𝗢𝗯𝗷𝗲𝗰𝘁 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟬 & 𝟭𝟭
```
<hr>

```Javascript
// ===================
// E. Tipe Data Symbol
// ===================

// 𝗡𝗼𝘁𝗲: 𝗠𝗮𝘁𝗲𝗿𝗶 𝗹𝗮𝗻𝗷𝘂𝘁𝗮𝗻 (𝘁𝗶𝗱𝗮𝗸 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗯𝘂𝗸𝘂 𝗶𝗻𝗶)
```
<hr>

```Javascript
// ==================
// F. Tipe Data Array
// ==================

var arrSiswa = ["Andri", "Joko", "Sukma"];    // Array 1D berisi hanya data String
var arrAcak  = [1, 2.0, "tiga", true, null];  // Array 1D berisi beragam tipe data
var arr2D    = [[2,5], [9,5], [3,5]];         // Array 2D, misalnya untuk koordinat

console.log(arrSiswa);                // Output: ["Andri", "Joko", "Sukma"]
console.log(arrSiswa[0]);             // Output: Andri                        ⇨ Array di JavaScript dimulai dari indeks ke 0,
console.log(arrSiswa[1]);             // Output: Joko                           bukan dari indeks ke 1, ingat baik-baik ya.
console.log(arrSiswa[2]);             // Output: Sukma
console.log(arrSiswa[3]);             // Output: undefined

console.log(arr2D);                   // Output: [[2,5],[9,5],[3,5]]
console.log(arr2D[0]);                // Output: [2,5]
console.log(arr2D[1]);                // Output: [9,5]
console.log(arr2D[2]);                // Output: [3,5]
console.log(arr2D[0][0]);             // Output: 2
console.log(arr2D[0][1]);             // Output: 5
console.log(arr2D[1][0]);             // Output: 9
console.log(arr2D[1][1]);             // Output: 5
console.log(arr2D[2][0]);             // Output: 3
console.log(arr2D[2][1]);             // Output: 5
```
<hr>

```Javascript
// ==================================
// G. Tipe Data Object, RegExp & Date
// ==================================

// 𝗡𝗼𝘁𝗲:
// 𝗢𝗯𝗷𝗲𝗰𝘁 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟬 & 𝟭𝟭
// 𝗥𝗲𝗴𝗘𝘅𝗽 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟮 (𝗯𝗮𝗴𝗶𝗮𝗻 𝗗)
// 𝗗𝗮𝘁𝗲 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟮 (𝗯𝗮𝗴𝗶𝗮𝗻 𝗙)
```
<hr>

```Javascript
// ========================================
// H. Tipe Data Map, WeakMap, Set & WeakSet
// ========================================

// 𝗡𝗼𝘁𝗲: 𝗠𝗮𝘁𝗲𝗿𝗶 𝗹𝗮𝗻𝗷𝘂𝘁𝗮𝗻 (𝘁𝗶𝗱𝗮𝗸 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗯𝘂𝗸𝘂 𝗶𝗻𝗶)
```
<hr>

```Javascript
// ==================
// I. Operator typeof
// ==================

/*
Operator typeof digunakan untuk melihat tipe data dari sebuah Variable
Apakah tipe datanya Number, String, Boolean, Undefined, atau sebuah Object. 
*/

var numA = 100;
var strA = "Hello World!";
var bolA = true;
var nudA = null;
var nudB = undefined;
var arrSiswa = ["Andri", "Joko", "Sukma"];

console.log(typeof numA);                 // Output: number
console.log(typeof strA);                 // Output: string
console.log(typeof bolA);                 // Output: boolean
console.log(typeof nudA);                 // Output: object (bukan Null)
console.log(typeof nudB);                 // Output: undefined
console.log(typeof arrSiswa);             // Output: object (Array termasuk Object)

// Check Tipe Data (Materi Tambahan)

var num = 10;                             // Tipe data: Number
var str = "JavaScript";                   // Tipe data: String
var bol = true;                           // Tipe data: Boolean
var nul = null;                           // Tipe data: Null
var und = undefined;                      // Tipe data: Undefined
var arr = [1, 2, "tiga"];                 // Tipe data: Array
var obj = {nama: "Budi", umur: 13};       // Tipe data: Object      // 𝗢𝗯𝗷𝗲𝗰𝘁 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟬 & 𝟭𝟭
var reg = /^\d\w\s$/;                     // Tipe data: RegExp      // 𝗥𝗲𝗴𝗘𝘅𝗽 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟮 (𝗗)
var dat = new Date(2016,11,2,9,30,15);    // Tipe data: Date        // 𝗗𝗮𝘁𝗲 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟮 (𝗙)
var nan = 9/"a";                          // Tipe data: NaN
var inf = 9/0;                            // Tipe data: Infinity

console.log(typeof num === "number");     // Output: true   (Check apakah datanya Number)
console.log(typeof str === "string");     // Output: true   (Check apakah datanya String)
console.log(typeof bol === "boolean");    // Output: true   (Check apakah datanya Boolean)
console.log(nul === null);                // Output: true   (Check apakah datanya Null)
console.log(und === undefined);           // Output: true   (Check apakah datanya Undefined)
console.log(Array.isArray(arr));          // Output: true   (Check apakah datanya Array - cara 1)
console.log(arr instanceof Array);        // Output: true   (Check apakah datanya Array - cara 2)
console.log(arr.constructor === Array);   // Output: true   (Check apakah datanya Array - cara 3)
console.log(typeof obj === "object");     // Output: true   (Check apakah datanya Object - cara 1)
console.log(obj instanceof Object);       // Output: true   (Check apakah datanya Object - cara 2)
console.log(obj.constructor === Object);  // Output: true   (Check apakah datanya Object - cara 3)
console.log(reg instanceof RegExp);       // Output: true   (Check apakah datanya RegExp - cara 1)
console.log(reg.constructor === RegExp);  // Output: true   (Check apakah datanya RegExp - cara 2)
console.log(dat instanceof Date);         // Output: true   (Check apakah datanya Date - cara 1)
console.log(dat.constructor === Date);    // Output: true   (Check apakah datanya Date - cara 2)
console.log(Number.isNaN(nan));           // Output: true   (Check apakah datanya NaN)
console.log(inf === Infinity);            // Output: true   (Check apakah datanya Infinity)
```
<hr>

```Javascript
// ======================
// J. Operator instanceof
// ======================

// 𝗡𝗼𝘁𝗲: 𝗢𝗽𝗲𝗿𝗮𝘁𝗼𝗿 𝗶𝗻𝘀𝘁𝗮𝗻𝗰𝗲𝗼𝗳 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟭 (𝗯𝗮𝗴𝗶𝗮𝗻 𝗕𝟯)
```

<br>
<div id="bab07"></div>

# 7. Operator JavaScript <a href="#daftarisi">🡹</a>

<img src="images/BAB-7.png">

```Javascript
// ======================
// A. Operator Aritmatika
// ======================

var a = 10;
var b = 2;

console.log(a + b);                   // Output: 12     ⇨ Addition (tambah)
console.log(a - b);                   // Output: 8      ⇨ Substraction (kurang)
console.log(a * b);                   // Output: 20     ⇨ Multiplication (kali)
console.log(a / b);                   // Output: 5      ⇨ Division (bagi)
console.log(a % b);                   // Output: 0      ⇨ Modulo (sisa bagi)
console.log(a ** b);                  // Output: 100    ⇨ Exponentiation (pangkat)

console.log(4+6/5-3*2+3);             // Output: 2.2    ⇨ Operator * dan / diproses lebih awal (precedence: 15)
console.log((4+6)/(5-3)*2+3);         // Output: 13     ⇨ Operator () diproses lebih awal (precedence: 21)

/*
📚 Baca urutan prioritas operator (precedence) secara lengkap di:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence
*/
```
<hr>

```Javascript
// ===================================
// B. Operator Increment dan Decrement
// ===================================

var c = 10, d = 10, e = 10, f = 10;

console.log(++c);                     // Output: 11     ⇨ Pre-increment: langsung tambahkan
console.log(c);                       // Output: 11
console.log(--d);                     // Output: 9      ⇨ Pre-decrement: langsung kurangi
console.log(d);                       // Output: 9

console.log(e++);                     // Output: 10     ⇨ Post-increment: tampilkan dulu, baru tambahkan
console.log(e);                       // Output: 11
console.log(f--);                     // Output: 10     ⇨ Post-decrement: tampilkan dulu, baru kurangi
console.log(f);                       // Output: 9
```
<hr>

```Javascript
// ========================
// C. Operator Perbandingan
// ========================

console.log(8 == 12);                 // Output: false  ⇨ Equality (sama dengan)
console.log(8 != 12);                 // Output: true   ⇨ Inquality (tidak sama dengan)
console.log(10 < 11);                 // Output: true   ⇨ Less than (kurang dari)
console.log(11 <= 11);                // Output: true   ⇨ Less than or equal (kurang dari atau sama dengan)
console.log(21 > 20);                 // Output: true   ⇨ Greater than (lebih dari)
console.log(21 >= 21);                // Output: true   ⇨ Greater than or equal (lebih dari atau sama dengan)

console.log(9 == "9");                // Output: true
console.log(9 === "9");               // Output: false  ⇨ Strict equality (identik dengan)
console.log(9 != '9');                // Output: false
console.log(9 !== '9');               // Output: true   ⇨ Strict inequality (tidak identik dengan)

// C1. Anda Harus Tahu

console.log(1 == true);               // Output: true
console.log(1 === true);              // Output: false
console.log(0 == false);              // Output: true
console.log(0 === false);             // Output: false
console.log(0.3 == 3e-1);             // Output: true
console.log(0.3 === 3e-1);            // Output: true   (Karena memang nilainya sama)
console.log(true > false)             // Output: true   (Ingat: true = 1, false = 0)

// C2. Perbandingan String 

/*
📚 Setiap karakter dalam String menggunakan nomor urut
desimal di ASCII-Code: https://www.ascii-code.com/
*/

console.log("a" < "b");               // Output: true   (a = 97, b = 98)
console.log("a" < "A");               // Output: false  (a = 97, A = 65)
console.log("ali" < "ala");           // Output: false  (ali = 97→108→105, ala = 97→108→97)
console.log("ali" < "alo");           // Output: true   (ali = 97→108→105, alo = 97→108→111)
console.log("ali" < "alika");         // Output: true   (String yang lebih pendek akan dianggap lebih kecil) 
console.log("ali" < 9999999);         // Output: false  (Perbandingan String & Number selalu menghasilkan false)
```
<hr>

```Javascript
// =======================
// D. Falsy & Truthy Value
// =======================

/*
Di JavaScript sebuah tipe data akan berubah menjadi tipe data lain tergantung operator
yang digunakan. Untuk operator perbandingan, tipe data ini akan dikonversi menjadi
Boolean (true/false). Nilai yang dikonversi menjadi false disebut Falsy Value, dan
nilai yang dikonversi menjadi true disebut Truthy Value.

Yang dikonversi menjadi false:
• false
• null
• undefined
• 0
• NaN
• ''        (String kosong)
• ""        (String kosong)

Yang dikonversi menjadi true:
• true
• {}        (Object kosong)           // 𝗡𝗼𝘁𝗲: 𝗢𝗯𝗷𝗲𝗰𝘁 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟬 & 𝟭𝟭
• []        (Array kosong)
• 42        (Sembarang angka, termasuk pecahan dan negatif, selain 0)
• "foo"     (Sembarang String, selama bukan String kosong)
• infinity  (Termasuk -infinity)
*/

console.log('' == '0');               // Output: false  (Hasil konversi: false == true)
console.log(0 == '');                 // Output: true   (Hasil konversi: false == false) 
console.log(0 == '0');                // Output: true   (Bukan operator indentik, jadinya true) 
console.log(false == 'false');        // Output: false  (Hasil konversi: false == true) 
console.log(false == '0');            // Output: true   (Bukan operator indentik & false kan bernilai 0, jadinya true) 
console.log(false == undefined);      // Output: false  (Pengecualian) 
console.log(false == null);           // Output: false  (Pengecualian) 
console.log(null == undefined);       // Output: true   (Hasil konversi: false == false) 
console.log('\t\r\n' == 0);           // Output: true   (Pengecualian) 
```
<hr>

```Javascript
// ==================
// E. Operator Logika
// ==================

console.log(true && false);           // Output: false  ⇨ and operator (true hanya jika kedua nilai true)
console.log(true || false);           // Output: true   ⇨ or operator (true jika salah satu nilai true)
console.log(!false);                  // Output: true   ⇨ not operator (negasi/kebalikannya)
console.log(true || true && false);   // Output: true   ⇨ Operator && diproses lebih awal (precedence: 7)

// E1. Cara Kerja Operasi Logika

/* 
📚 Operasi logika di proses dari kiri ke kanan (left-to-right), baca selengkapnya di:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

Selain itu, operasi logika pun menggunakan prinsip short-circuit-evaluation, maksudnya jika
dengan memeriksa 1 nilai saja hasil operasi tersebut sudah diketahui, nilai-nilai lain tidak
akan diperiksa, kecuali jika terdapat operator && dan || dalam 1 operasi, maka operator &&
akan dijalankan terlebih dahulu (karena nilai precedence && lebih tinggi daripada ||)
*/

console.log(true || false || true);   // Kiri ke kanan: true bertemu operator ||, stop, sudah pasti hasilnya true
console.log(false && true && true);   // Kiri ke kanan: false bertemu operator &&, stop, sudah pasti hasilnya false
console.log(true || true && false);   // Operator && duluan, menjadi: true || false, hasilnya true

console.log(true && alert("HYA!"));   // Function alert() berjalan, karena true bertemu &&, lanjut ke alert()
console.log(false && alert("HYA!"));  // Function alert() tidak berjalan, karena false bertemu &&, stop
console.log(true || alert("HYA!"));   // Function alert() tidak berjalan, karena true bertemu ||, stop
console.log(false || alert("HYA!"));  // Function alert() berjalan, karena false bertemu ||, lanjut ke alert()

// E2. Operasi Logika Non-Boolean

/*
Nilai yang dibandingkan menggunakan operator logika harus bertipe Boolean, jika tidak, akan di
konversi secara otomatis berdasarkan ketentuan Falsy & Truthy Value. Lalu, hasil akhir dari
operasi logika non-Boolean ini berupa nilai dari posisi terakhir yang diperiksa.
*/

console.log("Hello" || "World");      // Output: Hello  ("Hello" ≈ true, lalu bertemu ||, stop, hasilnya String Hello)
console.log("Hello" && "World");      // Output: World  ("Hello" ≈ true, lalu bertemu &&, lanjut, hasilnya String World)
console.log(true || "World");         // Output: true   (true bertemu ||, stop, hasilnya true)
console.log(false || "World");        // Output: World  (false bertemu ||, lanjut, "World" ≈ true, hasilnya String World)
console.log("Hello" && false);        // Output: false  ("Hello" ≈ true, lalu bertemu &&, lanjut, hasilnya false)
console.log(false && "World");        // Output: false  (false bertemu &&, stop, hasilnya false)

console.log(false || false && true || "World");   // Output: World  (&& duluan, menjadi: false || false || "World", ...)
console.log(true || false && true || "World");    // Output: true   (&& duluan, menjadi: true || false || "World", ...)
```
<hr>

```Javascript
// ==================
// F. Operator String
// ==================

var arr = ["Andri", "Joko", "Sukma"];

strA = arr[0] + " dan " + arr[1] + " adalah teman akrab.";  // String concatenation (sebelum ES6), "+" sebagai penyambung
strB = `${arr[0]} dan ${arr[1]} adalah teman akrab`;        // Template String (setelah ES6), memakai backtick (``)

// Kasus Konversi Number ke String

console.log(10 + 10 + 9);             // Output: 29     (Number)
console.log("10" + 10 + 9);           // Output: 10109  (String)  dari hasil konversi: console.log("10" + "10" + "9");
console.log(10 + "10" + 9);           // Output: 10109  (String)  dari hasil konversi: console.log(10 + "10" + "9");
console.log(10 + 10 + "9");           // Output: 209    (String)  dari hasil konversi: console.log(20 + "9");
```
<hr>

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
<hr>

```Javascript
// ======================
// H. Operator Assignment
// ======================

var g = 10;       // Artinya 10 dimasukkan sebagai nilai ke Variable g (operator assignment memiliki precedence: 3)
var h = 10 + 5;   // Jumlahkan 10 + 5 dulu (operator "+" memiliki precedence: 14), lalu masukkan hasilnya ke Variable h
var i = g + h;    // 📚 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

// Operator Gabungan Assignment

var gabA = gabB = gabC = gabD = gabE = 20;

gabA += 10;       // gabA = gabA + 10 🡲 gabA = 20 + 10  (Output: 30) 
gabB -= 10;       // gabB = gabB - 10 🡲 gabB = 20 - 10  (Output: 10)
gabC /= 10;       // gabC = gabC / 10 🡲 gabC = 20 / 10  (Output: 2)
gabD *= 10;       // gabD = gabD * 10 🡲 gabD = 20 * 10  (Output: 200) 
gabE %= 10;       // gabE = gabE % 10 🡲 gabE = 20 % 10  (Output: 0)
```
<hr>

```Javascript
// ==================
// I. Operator Spread
// ==================

/*
Spread merupakan operator baru di ES6. Operator ini digunakan untuk berbagai keperluan yang berhubungan dengan Array, salah
satunya untuk menggabungkan Array. Operator ini menggunakan tanda titik tiga kali (...), kemudian diikuti dengan nama Variable.
*/

var nilai1 = ["a", "b", "c", "d"];
var nilai2 = [1, 2, 3, 4];

var nilai3 = [...nilai1, "e", "f"];   // ...nilai1 berarti mengakses seluruh element dari array nilai1
console.log(nilai3);                  // Output: ["a", "b", "c", "d", "e", "f"]

var nilai4 = [0, ...nilai2, 5, 6];    // ...nilai2 berarti mengakses seluruh element dari array nilai2
console.log(nilai4);                  // Output: [0, 1, 2, 3, 4, 5, 6]

var nilai5 = [...nilai3, ...nilai4];
console.log(nilai5);                  // Output: ["a", "b", "c", "d", "e", "f", 0, 1, 2, 3, 4, 5, 6]
```

<br>
<div id="bab08"></div>

# 8. Struktur Logika dan Perulangan <a href="#daftarisi">🡹</a>

<img src="images/BAB-8.png">

```Javascript
// ===========================
// A. Struktur Logika: IF-ELSE
// ===========================

var nilai = 90;                     

if (nilai >= 0 && nilai <= 100){      // Jika nilai >= 0 dan <= 100, masuk ke kondisi berikutnya, selain itu tidak valid!
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
<hr>

```Javascript
// ==========================
// B. Struktur Logika: SWITCH
// ==========================

var nilaiTK = 6;   

switch(nilaiTK){                      // Case 1-5: kurang, case 6-7: cukup, case 8-10: baik, selain itu tidak valid!
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
<hr>

```Javascript
// ================================================
// C. Struktur Logika: Conditional Ternary Operator
// ================================================

var jumlah = 501;
var pesan = jumlah > 500 ? "Cukup!" : "Produksi lagi!";

/*
Cara baca: Apakah jumlah > 500? jika iya (true), kirim String "Cukup!" ke Variable
pesan. Jika tidak (false) kirim String "Produksi lagi!" ke Variable pesan.
*/

var user = "admin";
var akses = user === "admin" ? true : false;

if (akses){ // jika akses bernilai true
  console.log("Welcome, admin!");
}

/*
Cara baca: Apakah user === "admin"? jika iya, kirim Boolean true ke Variable akses, lalu kondisi "if (akses)"
akan dijalankan. Jika tidak, kirim Boolean false ke Variable akses, dan kondisi "if (akses)" tidak jalan.
*/
```
<hr>

```Javascript
// ===============================================
// D. Struktur Logika: Nullish Coalescing Operator
// ===============================================

var dataDariLuar1;
data1 = dataDariLuar1 ?? "Nilai Default";
console.log(data1);                   // Output: Nilai Default (karena sebelumnya dataDariLuar1 bernilai undefined)

/*
Cara baca: Apakah dataDariLuar1 bernilai Null atau Undefined? jika iya (true), isi dataDariLuar1 dengan
String "Nilai Default". Jika tidak (bukan null/undefined), tidak perlu dilakukan apapun.
*/

var dataDariLuar2 = "Ada isinya";
data2 = dataDariLuar2 ?? "Nilai Defailt";
console.log(data2);                   // Output: Ada isinya (karena sebelumnya dataDariLuar2 memang sudah ada isinya)
```

```Javascript
// ==================
// E. Perulangan: FOR
// ==================

for (var i=1; i<=10; i++){            // Output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
}

for (var j=20; j>0; j=j-2){           // Output: 20, 18, 16, 14, 12, 10, 8, 6, 4, 2
  console.log(j);
}

for (var k=1; k<3; k++){              // Output: outer 1 inner 1 s/d outer 2 inner 3
  for (var l=1; l<=3; l++){           
    console.log(`outer ${k} inner ${l}`);
  }
}

// E1. Break: Berhenti memproses perulangan (keluar dari perulangan)

for (var m=10; m>=1; m--){            // Output: 10, 9, 8, 7, 6, 5, 4, 3
  if (m === 2){
    break;
  }
  console.log(m);
}

// E2. Continue: Berhenti memproses perulangan saat ini & lanjut ke perulangan berikutnya

for (var m=10; m>=1; m--){            // Output: 10, 9, 8, 7, 6, 5, 4, 3, 1
  if (m === 2){
    continue;
  }
  console.log(m);
}

// E3. Menampilkan element Erray dengan perulangan FOR

var arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];
for (var n=0; n<arrSiswa.length; n++){
  console.log(arrSiswa[n]);
}                                     // Output: Andri, Joko, Sukma, Rina, Sari

```
<hr>

```Javascript
// ====================
// F. Perulangan: WHILE
// ====================

/*
Perulangan WHILE cocok digunakan untuk situasi dimana kita tidak tahu berapa banyak perulangan
yang mesti dijalankan. Berbeda dengan perulangan FOR yang kita tahu berapa banyak perulangannya.
*/

var i = 1;
while (i <= 10){                      // Output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
  i++;
}

var j = 10;
while (j > 1){                        // Output: 20, 18, 16, 14, 12
  if (j === 5){
    break;
  }
  console.log(j*2);
  j--;
}
```
<hr>

```Javascript
// =======================
// G. Perulangan: DO WHILE
// =======================

/*
Dalam perulangan DO WHILE, kondisi akan di check di akhir, hal ini menyebabkan setidaknya
perulangan akan diproses 1 kali, walaupun kondisi tersebut sudah tidak terpenuhi sejak awal.
*/

var i = 1;
do {                                  // Output: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
  console.log(i);
  i++;
} while (i <= 10);

var j = 1;
do {                                  // Output: 1
  console.log(j);
  j--;
} while (j > 999);
```
<hr>

```Javascript
// =====================
// H. Perulangan: FOR OF
// =====================

/*
Perulangan FOR OF merupakan fitur baru dari ES6, digunakan khusus untuk menampilkan element Erray.
Hasil dari perulangan FOR OF di bawah ini, sama dengan hasil perulangan FOR di point E3 di atas.
*/

var arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];
for (var i of arrSiswa){
  console.log(i);
}                                     // Output: Andri, Joko, Sukma, Rina, Sari
```
<hr>

```Javascript
// =====================
// I. Perulangan: FOR IN
// =====================

/*
Perulangan FOR IN merupakan fitur baru dari ES6, digunakan khusus untuk menampilkan seluruh
isi Object (property dan method). Sebenarnya, bisa juga digunakan untuk menampilkan isi Array
(karena Array pun termasuk ke dalam tipe data Object), namun tidak disarankan.

𝗡𝗼𝘁𝗲: 𝗢𝗯𝗷𝗲𝗰𝘁 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟬 & 𝟭𝟭
*/

var objMobil = {
  merk: "Toyota Avanza",
  tipe: "MPV",
  harga: 200000000,
  warna: "biru",
  hidupkan: function(){return "Mesin dihidupkan!";}
};

for (var i in objMobil){
  console.log(`Isi ${i} = ${objMobil[i]}`);
}

/* 
Output:
Isi merk = Toyota Avanza
Isi tipe = MPV
Isi harga = 200000000
Isi warna = biru
Isi hidupkan = function(){return "Mesin dihidupkan!";}
*/
```

<br>
<div id="bab09"></div>

# 9. Function <a href="#daftarisi">🡹</a>

<img src="images/BAB-9.png">

```Javascript
// ===================================
// A. Function Declaration (Sederhana)
// ===================================

function pagiMalam(){
  console.log("Selamat Pagi!");
  console.log("Selamat Malam!");
}

pagiMalam();                          // Output: Selamat Pagi!
                                      //         Selamat Malam!
```
<hr>

```Javascript
// =====================================
// B. Function dengan Parameter & Return
// =====================================

function salam(kapan, nama){          // Kapan & nama adalah sebuah parameter yang akan menampung nilai dari argument
  return `Selamat ${kapan} ${nama}!`; // return berfungsi untuk mengembalikan nilai & memberhentikan Function
}

function ratarata(a, b, c, d){
  var hasil = (a+b+c+d)/4;
  return hasil;
}

console.log(salam("Pagi", "Budi"));   // Output: Selamat Pagi Budi!     ⇨ "Pagi" & "Budi" merupakan sebuah argument
console.log(salam("Malam", "Putri")); // Output: Selamat Malam Putri!

console.log(ratarata(1, 2, 3, 4));    // Output: 2.5 (Hasil dari (1+2+3+4)/4 🡲 10/4)
console.log(ratarata(1, 2, 3, 4, 5)); // Output: 2.5 (Argument ke-5 akan diabaikan, karena tidak ada "slot"-nya di Function)
console.log(ratarata(1, 2, 3));       // Output: NaN (Argument ke-4 tidak ada, maka secara defaultnya nilainya Undefined)
```
<hr>

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

console.log(tambah());                // Output: 40 (Hasil dari 10+10+10+10)
console.log(tambah(20));              // Output: 50 (Hasil dari 20+10+10+10)
console.log(tambah(20, 25));          // Output: 65 (Hasil dari 20+25+10+10)
console.log(tambah(20, 25, 30));      // Output: 85 (Hasil dari 20+25+30+10)
console.log(tambah(20, 25, 30, 15));  // Output: 90 (Hasil dari 20+25+30+15)

console.log(kurang());                // Output: NaN (Function kurang() butuh minimal 2 argument! untuk parameter a & b)
console.log(kurang(20));              // Output: NaN (Function kurang() butuh minimal 2 argument! kurang argument ke-2)
console.log(kurang(20, 25));          // Output: -25 (Argument c & d jika tidak diisi, maka akan diisi nilai defaultnya)
console.log(kurang(20, 25, 30));      // Output: -45 (Hasil dari 20-25-30-10)
console.log(kurang(20, 25, 30, 15));  // Output: -50 (Hasil dari 20-25-30-15)

console.log(kali());                  // Output: NaN (Function kali butuh minimal 4 argument! untuk parameter a, b, c & d)
console.log(kali(20, 25));            // Output: NaN (Function kali butuh minimal 4 argument! kurang argument ke-3 & ke-4)
console.log(kali(20, 25, 30, 15));    // Output: 225000 (Hasil dari 20*25*30*15)
console.log(kali(undefined, undefined, 30, 15));  // Output: 45000 (Hasil dari 10*10*30*15), Undefined akan diisi nilai default
```
<hr>

```Javascript
// ====================================================
// D. Function dengan Arguments Object (Array Argument)
// ====================================================

// D1. Array Argument

function numA(){                      // Function dibuat tanpa parameter (tanpa wadah untuk argument), namun setiap argument
  console.log(arguments[0]);          // Dapat ditangkap oleh Array argument (bawaan JavaScript) berapapun jumlahnya (fleksibel)
  console.log(arguments[1]);
  console.log(arguments[2]);
  console.log(arguments[3]);
}

numA(20, 25, 30, 15);                 // Output: 20, 25, 30, 15
numA(20, 25);                         // Output: 20, 25, undefined, undefined

// D2. arguments.length

function numB(){                      // Karena Array argument merupakan sebuah Array, maka kita dapat menghitung jumlah argument
  total = arguments.length;           // yang dikirimkan pada saat pemanggilan Function dengan menggunakan property length
  return total;
}

console.log(numB());                  // Output: 0 (Terdapat 0 argument saat pemanggilan Function)
console.log(numB(20));                // Output: 1 (Terdapat 1 argument saat pemanggilan Function)
console.log(numB(20, 25));            // Output: 2 (Terdapat 2 argument saat pemanggilan Function)
console.log(numB(20, 25, 30));        // Output: 3 (Terdapat 3 argument saat pemanggilan Function)
console.log(numB(20, 25, 30, 15));    // Output: 4 (Terdapat 4 argument saat pemanggilan Function)

// D3. Studi Kasus: Rata-Rata

function ratarata(){                  // Berbekal Array argument dan arguments.length, kita bisa membuat sebuah Function
  var totalArg = arguments.length;    // rata-rata yang bisa menerima berarapun jumlah argumentnya (fleksibel)
  var hasil = 0;
  for (var i=0; i<totalArg; i++){
    hasil += arguments[i];
  }
  return hasil/totalArg;
}

console.log(ratarata(2, 4));          // Output: 3   (hasil dari (2+4)/2 🡲 6/2)
console.log(ratarata(2, 4, 8, 16));   // Output: 7.5 (hasil dari (2+4+8+16)/4 🡲 30/4)

// D4. Rest Parameter (1)

function numC(...arg){                // Selain untuk menggabungkan Array seperti yang dijelaskan di BAB 7 (operator),
  console.log(arg[0]);                // spread (...) juga dapat digunakan untuk menggantikan peran Arguments Object,
  console.log(arg[1]);                // dan inilah yang disebut dengan 𝗥𝗲𝘀𝘁 𝗣𝗮𝗿𝗮𝗺𝗲𝘁𝗲𝗿. Hasil sama saja dengan point D1.
  console.log(arg[2]);                // Penulisannya tidak harus ...arg, bisa dengan kata lain, misalnya ...angka, dll
  console.log(arg[3]);
}

numC(20, 25, 30, 15);                 // Output: 20, 25, 30, 15
numC(20, 25);                         // Output: 20, 25, undefined, undefined

// D5. Rest Parameter (2)

function numD(a, b, ...sisa){         // Cara baca: jika Function numD dipanggil dengan lebih dari 3 argument, maka argument
  console.log(a);                     // pertama dan kedua masuk ke Variable a dan b, sisanya disimpan ke dalam Rest Parameter
  console.log(b);
  console.log(sisa);
}

numD(20, 25);                         // Output: 20, 25, []
numD(20, 25, 30);                     // Output: 20, 25, [30]
numD(20, 25, 30, 15);                 // Output: 20, 25, [30, 15]

// D6. Studi Kasus: Rata-Rata V2

function rataratav2(...nilai){        // Studi kasus pada point D3, dapat kita buat ulang dengan memanfaatkan Rest Parameter
  var totalArg = nilai.length;        // serta perulangan for of, hasilnya aka sama saja, dan juga tetap fleksibel
  var hasil = 0;
  for (var i of nilai){
    hasil += i;
  }
  return hasil/totalArg;
}

console.log(rataratav2(2, 4));        // Output: 3   (hasil dari (2+4)/2 🡲 6/2)
console.log(rataratav2(2, 4, 8, 16)); // Output: 7.5 (hasil dari (2+4+8+16)/4 🡲 30/4)
```
<hr>

```Javascript
// =================
// E. Variable Scope
// =================

/*
Variable Scope adalah istilah tentang sejauh mana sebuah Variable masih dapat diakses. Global Variable dapat diakses dari-
mana saja, sedangkan Local Variable hanya bisa diakses di dalam ruang lingkup terbatas, milsanya di dalam sebuah Function
*/

// E1. Global Variable

var a = "Belajar JS";                 // a merupakan global Variable, oleh karena itu dapat diakses darimana saja
function boo(){
  console.log(a);                     // a yang diakses disini yaitu a global varibale, berhubung Function boo
}                                     // tidak memiliki local Variable a, maka akan "naik" mencari ke global

boo();                                // Output: Belajar JS (Hasil dari dalam Function)
console.log(a);                       // Output: Belajar JS (Hasil dari global Variable a)

// E2. Global & Local Variable

var b = "Belajar JS";                 // b disini merupakan global Variable
function coo(){
  var b = "Belajar CSS";              // b disini merupakan local Variable
  console.log(b);                     // b yang diakses disini yaitu b local Variable
}

coo();                                // Output: Belajar CSS (Hasil dari dalam Function)
console.log(b);                       // Output: Belajar JS (Hasil dari global Variable b)

// E3. Contoh dalam Argument (1)

function doo(c, d){
  var c = 20;                         // c disini merupakan local Variable
  var d = 40;                         // d disini merupakan local Variable
  return c+d;                         // Function mengembalikan nilai 60
}

var c = 5;                            // c disini merupakan global Variable
var d = 10;                           // d disini merupakan global Variable
var e = doo(c, d);                    // Argument yang dikirim yaitu doo(5, 10)

console.log(c);                       // Output: 5
console.log(d);                       // Output: 10
console.log(e);                       // Output: 60 (Bukan 15, karena nilai var c & d tertimpa saat di dalam Function)

// E4. Contoh dalam Argument (2)

function foo(){
  c = 20;                             // c disini menimpa global Variable c (Jika didefinisikan tanpa var, maka berefek ke global)
  d = 40;                             // d disini menimpa global Variable d (Jika didefinisikan tanpa var, maka berefek ke global)
  return c+d;                         // Function mengembalikan nilai 60
}

var c = 5;                            // c disini merupakan global Variable
var d = 10;                           // d disini merupakan global Variable
var e = foo();                        // Tidak ada argument yang dikirim

console.log(c);                       // Output: 20 (Bukan 5, karena nilai c tertimpa saat di dalam Function)
console.log(d);                       // Output: 40 (Bukan 10, karena nilai d tertimpa saat di dalam Function)
console.log(e);                       // Output: 60 (Bukan 15, karena nilai var c & d tertimpa saat di dalam Function)
```
<hr>

```Javascript
// =============
// F. VAR vs LET
// =============

/*
Penggunaan Var dapat mempengaruhi nilai diluar scope (tidak aman!), sedangkan penggunaan Let tidak mempengaruhi
nilai diluar scope (aman!). Let sendiri merupakan fitur baru di ES6, tujuannya untuk "mengganti" penggunaan Var.
*/

// F1. Perbandingan var & let (1)

for (var i=1; i<3; i++){
  console.log(i);
}
console.log(i);                       // Output: 3                                ⇨ Var bersifat Function Scope, artinya cakupan
                                      //                                             scopenya itu Function. Sehingga pada contoh
                                      //                                             di samping, Var masih bisa diakses dari luar
                                      //                                             (ini tidak aman!), seolah tidak Private.

for (let j=1; j<3; j++){
  console.log(j);
}
console.log(j);                       // Output: ReferenceError j is not defined  ⇨ Let bersifat Block Scope, artinya cakupan
                                      //                                             scopenya itu tanda {}. Sehingga pada contoh
                                      //                                             di samping, Let tidak bisa diakses dari luar
                                      //                                             (dan menghasilkan Error), seolah Private.

// F2. Perbandingan var & let (2)

var k = 1000;
for (var k=1; k<3; k++){
  console.log(k);
}
console.log(`Harganya Rp.${k}`);      // Output: Harganya Rp.3 (Nilai k global tertimpa, saat di dalam perulangan)

let l = 1000;
for (let l=1; l<3; l++){
  console.log(l);
}
console.log(`Harganya Rp.${l}`);      // Output: Harganya Rp.1000 (Nilai l global tidak tertimpa)
```
<hr>

```Javascript
// ========================
// G-1. JavaScript Hoisting
// ========================

/*
Hoisting terkait cara JavaScript mengeksekusi kode program, dimana terdapat 2 fase yaitu creation & execution.
Di fase creation, pertama-tama JavaScript akan "mengangkat" (hoisting) semua Variable & Function yang dibuat
ke baris paling atas kode program, untuk setiap Variable akan diisi nilai Undefined, sedangkan Function akan
diisi Functionnya itu sendiri. Selanjutya, barulah masuk ke fase execution, dimana kode program akan dieksekusi
baris per baris, dari atas ke bawah. 📚 Pakai tools visualusasi berikut: http://pythontutor.com/javascript.html
*/

// Contoh 1: Variable

// Contoh 1-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksA);                   // console.log(teksA);              🡲 Output: ReferenceError teksA is not defined (STOP!)

// Contoh 1-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksB);                   // 𝘃𝗮𝗿 𝘁𝗲𝗸𝘀𝗕 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
console.log(teksC);                   // console.log(teksB);              🡲 Output: undefined
var teksB = "Belajar JS";             // console.log(teksC);              🡲 Output: ReferenceError teksC is not defined (STOP!)
                                      // var teksB = "Belajar JS";        🡲 Baris ini tidak akan dieksekusi, karena error di atas
                                      
// Contoh 1-3                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(teksD);                   // 𝘃𝗮𝗿 𝘁𝗲𝗸𝘀𝗗 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var teksD = "Belajar JS";             // console.log(teksD);              🡲 Output: undefined
console.log(teksD);                   // var teksD = "Belajar JS";
                                      // console.log(teksD);              🡲 Output: Belajar JS

// Contoh 1-4                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(satu);                    // 𝘃𝗮𝗿 𝘀𝗮𝘁𝘂 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
console.log(dua);                     // 𝘃𝗮𝗿 𝗱𝘂𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var satu = "Belajar HTML";            // 𝘃𝗮𝗿 𝘁𝗶𝗴𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var dua = "Belajar CSS";              // console.log(satu);               🡲 Output: undefined
console.log(tiga);                    // console.log(dua);                🡲 Output: undefined
var tiga = "Belajar JS";              // var satu = "Belajar HTML";
console.log(satu);                    // var dua = "Belajar CSS";
                                      // console.log(tiga);               🡲 Output: undefined
                                      // var tiga = "Belajar JS";
                                      // console.log(satu);               🡲 Output: Belajar HTML

// Contoh 2: Function

// Contoh 2-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaPagi);                // 𝘀𝗮𝗽𝗮𝗣𝗮𝗴𝗶 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗣𝗮𝗴𝗶(){...}
console.log(sapaPagi());              // console.log(sapaPagi)            🡲 Output: function sapaPagi(){...}
function sapaPagi(){                  // console.log(sapaPagi());         🡲 Output: Selamat Pagi! (Function bisa berjalan! padahal
  console.log("Selamat Pagi!");       // function sapaPagi(){                                       pendefinisiannya dibawah, ini
}                                     //   console.log("Selamat Pagi!");                            terjadi akibat efek hoisting)
                                      // }                                🡲 Output: undefined (terjadi karena tidak ada return)

// Contoh 2-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSiang);               // 𝘀𝗮𝗽𝗮𝗦𝗶𝗮𝗻𝗴 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗶𝗮𝗻𝗴(){...}
console.log(sapaSiang());             // console.log(sapaSiang)           🡲 Output: function sapaSiang(){...}
function sapaSiang(){                 // console.log(sapaSiang());        🡲 Output: Selamat Siang!
  return "Selamat Siang!";            // function sapaSiang(){
}                                     //   return "Selamat Siang!";
                                      // }                                🡲 Karena ada return, maka tidak ada Output: undefined

// Contoh 2-3                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSore());              // 𝘀𝗮𝗽𝗮𝗦𝗼𝗿𝗲 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗼𝗿𝗲(){...}
function sapaSore(){                  // 𝘀𝗮𝗽𝗮𝗠𝗮𝗹𝗮𝗺 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗠𝗮𝗹𝗮𝗺(){...}
  return "Selamat Sore!";             // console.log(sapaSore());         🡲 Output: Selamat Sore!
}                                     // function sapaSore(){
console.log(sapaMalam());             //   return "Selamat Sore!";
function sapaMalam(){                 // }
  return "Selamat Malam!";            // console.log(sapaMalam());        🡲 Output: Selamat Malam!
}                                     // function sapaMalam(){
                                      //   return "Selamat Malam!";
                                      // }

// Contoh 3: Variable & Function

// Contoh 3-1                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
console.log(sapaSatu());              // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var nama = "Budi";                    // 𝘃𝗮𝗿 𝘂𝗺𝘂𝗿 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
var umur = 25;                        // 𝘀𝗮𝗽𝗮𝗦𝗮𝘁𝘂 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘀𝗮𝗽𝗮𝗦𝗮𝘁𝘂(){...}
function sapaSatu(){                  // console.log(sapaSatu());         🡲 Output: undefined, undefined tahun!
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
}                                     // console.log(sapaDua());          🡲 Output: Budi, 25 tahun!
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
console.log(cetakURL(user));          //   𝘃𝗮𝗿 𝘁𝘄𝘁𝗨𝗥𝗟 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;         🡲 Local Hoisting di dalam Function
                                      //   var twtURL = "http://twitter.com/";
                                      //   return twtURL+user;
                                      // }
                                      // console.log(cetakURL(user));     🡲 http://twitter.com/@budilorem

// Contoh 4-2                         ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
function luar(){                      // 𝗹𝘂𝗮𝗿 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗹𝘂𝗮𝗿(){...}        🡲 Global Hoisting
  console.log("A");                   // function luar(){
  function tengah(){                  //   𝘁𝗲𝗻𝗴𝗮𝗵 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝘁𝗲𝗻𝗴𝗮𝗵(){...} 🡲 Local Hoisting di dalam Function
    console.log("B");                 //   console.log("A");
    function dalam(){                 //   function tengah(){
      console.log("C");               //     𝗱𝗮𝗹𝗮𝗺 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗱𝗮𝗹𝗮𝗺(){...} 🡲 Local Hoisting di dalam Function (nested)
    }                                 //     console.log("B");
    dalam();                          //     function dalam(){
  }                                   //       console.log("C");
  tengah();                           //     }
}                                     //     dalam();
luar();                               //   }
                                      //   tengah();
                                      // }
                                      // luar();                          🡲 urutan Output: A, B, C

// Contoh 5: More Example             ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
function funA(){                      // 𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
  var nama = "Budi";                  // 𝗳𝘂𝗻𝗔 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗳𝘂𝗻𝗔(){...}
  console.log(nama);                  // 𝗳𝘂𝗻𝗕 = 𝗳𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗳𝘂𝗻𝗕(){...}
}                                     // function funA(){
function funB(){                      //   𝘃𝗮𝗿 𝗻𝗮𝗺𝗮 = 𝘂𝗻𝗱𝗲𝗳𝗶𝗻𝗲𝗱;
  console.log(nama);                  //   var nama = "Budi";
  console.log(arguments[0]);          //   console.log(nama);
}                                     // } 
console.log(nama);                    // function funB(){                 🡲 Tidak ada parameter yang menangkap argument
var nama = "Jaka";                    //   console.log(nama);             🡲 Baris ini akan mencari variable "nama" di Global
funA();                               //   console.log(arguments[0]);     🡲 Argument yang dikirim akan masuk ke Array Argument
funB("Tono");                         // }                                   ⤷ Lihat lagi point D1 & D4 di atas
console.log(nama);                    // console.log(nama);               🡲 Output: undefined
                                      // var nama = "Jaka";
                                      // funA();                          🡲 Output: Budi
                                      // funB("Tono");                    🡲 Output: Jaka  (dari var "nama" di luar Function)
                                      //                                             Tono  (dari Array Argument)
                                      // console.log(nama);               🡲 Output: Jaka
```
<hr>

```Javascript
// ===================================
// G-2. Kesimpulan JavaScript Hoisting
// ===================================

/*
➊ Selalu definisikan Variable (var) diawal kode program/Function, dan sebaiknya langsung diisi nilai, agar tidak Undefined.
➋ Pemanggilan Function bisa dimana saja, tidak peduli pendefinisian Functionnya berada di atas maupun bawah kode program.
   Namun tetap saja, agar lebih "aman" dan seragam, sama seperti var, lebih baik definisikan Function di awal kode program.
➌ Ganti penggunaan var dengan let. Let akan menampilkan error saat ia dipanggil namun belum didefinisikan di baris atas kode
   programnya (ini yang seharusnya terjadi), sedangkan var malah diisi Undefined (karena efek hoisting). Simak contoh di bawah.
   ⤷ Selain itu penggunaan var pun dapat mempengaruhi nilai diluar scope, ini tidak aman! (lihat kembali point F di atas).
*/

// Contoh VAR                         ᴠᴀʀ ɪᴛᴜ ᴛɪᴅᴀᴋ ᴀᴍᴀɴ:
console.log(a);                       // Output: undefined
var a = "Hello World!";               // Seharusnya sih error, tapi karena efek hoisting, jadilah Undefined (tidak professional)

// Contoh LET                         ʟᴇᴛ ɪᴛᴜ ᴀᴍᴀɴ & ᴘʀᴏꜰᴇꜱꜱɪᴏɴᴀʟ:
console.log(b);                       // Output: ReferenceError Cannot access 'b' before initialization
let b = "Hello World!";               // Ini artinya kita memang harus mendefinisikan var/let dulu, sebelum dipakai! (professional)
```
<hr>

```Javascript
// ============================================================
// H. Function sebagai First-Class Citizen/First-Class Function
// ============================================================

/*
Hal yang unik dari JavaScript yaitu Function dianggap sebagai tipe data, ini berarti:
➊ Function dapat disimpan ke dalam Variable, disebut 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗘𝘅𝗽𝗿𝗲𝘀𝘀𝗶𝗼𝗻𝘀.
  ⤷ Function Expressions tanpa nama Function, disebut 𝗔𝗻𝗼𝗻𝘆𝗺𝗼𝘂𝘀 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻𝘀.
➋ Function dapat digunakan sebagai argument layaknya tipe data biasa, disebut 𝗖𝗮𝗹𝗹𝗯𝗮𝗰𝗸.
  ⤷ Function yang memiliki Callback sebagai argument, disebut 𝗛𝗶𝗴𝗵𝗲𝗿 𝗢𝗿𝗱𝗲𝗿 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻.
*/

// H1. Function Expressions

let hitung = function ratarata(a, b){ // Function ratarata disimpan ke dalam Let hitung
  return (a+b)/2;
}
console.log(hitung(4, 8));            // Output: 6
console.log(ratarata(4, 8));          // Output: ReferenceError ratarata is not defined

// H2. Anonymous Functions

let hitung = function(a, b){          // Function Expressions tanpa nama Function disebut sebagai
  return (a+b)/2;                     // Anonymous Functions, ini yang banyak dipakai nantinya!
}
console.log(hitung(4, 8));            // Output: 6

// H3. Return Function sebagai Argument

function rerata(a, b){
  return (a+b)/2;
}
function tambah(c, d){
  return c+d;
}
let hasil = tambah(6, rerata(4, 8));  // Hasil return Function rerata(4, 8) digunakan sebagai argument
console.log(hasil);                   // Output: 12

// H4. Function sebagai Argument (1)

function rerata(a, b){
  return (a+b)/2;
}
function tambah(c, d){                // Step 2 🡲 parameter d akan menangkap Function rerata dari argument 
  return c+d(4, 8);                   // Step 3 🡲 dengan demikian d(4, 8) akan menjadi rerata(4, 8)
}
let hasil = tambah(6, rerata);        // Step 1 🡲 mengirim Function bernama rerata sebagai sebuah argument
                                      // Note: rerata merupakan Callback & tambah merupakan Higher Order Function
console.log(hasil);                   // Output: 12

// H5. Function sebagai Argument (2)

function foo(apa){
  alert(apa);                         // Step 4 🡲 foo("Belajar JS") akan dieksekusi sebagai alert("Belajar JS")
}
function salam(bar){                  // Step 2 🡲 parameter bar akan menangkap Function foo dari argument
  bar("Belajar JS");                  // Step 3 🡲 dengan demikian bar("Belajar JS") menjadi foo("Belajar JS")
}
salam(foo);                           // Step 1 🡲 mengirim Function bernama foo (Callback) sebagai sebuah argument
                                      // Note: foo merupakan Callback & salam merupakan Higher Order Function
```

```JavaScript
/*
𝗡𝗼𝘁𝗲: 𝗖𝗮𝗹𝗹𝗯𝗮𝗰𝗸 𝘀𝗲𝗰𝗮𝗿𝗮 𝗱𝗲𝘁𝗮𝗶𝗹 𝗱𝗶𝗯𝗮𝗵𝗮𝘀 𝗱𝗶 𝗕𝗔𝗕 𝟭𝟮 (𝗯𝗮𝗴𝗶𝗮𝗻 𝗘𝟰)

Tambahan: Selain uraian di atas, ada pula beberapa istilah lainnya terkait Function yang perlu diketahui.
➊ Function yang berada di dalam Function, disebut 𝗜𝗻𝗻𝗲𝗿 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻.
➋ Inner Function yang memiliki akses ke parent scope-nya (𝗢𝘂𝘁𝗲𝗿 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻) atau dengan kata
   lain yang menggunakan data/Var/Let yang ada di parent scope-nya, disebut 𝗖𝗹𝗼𝘀𝘂𝗿𝗲.
➌ Function yang berjalan dari hasil Function lainnya (sudah jalan ½ nya), disebut 𝗙𝗮𝗰𝘁𝗼𝗿𝘆 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻.
➍ 𝗜𝗺𝗺𝗲𝗱𝗶𝗮𝘁𝗲𝗹𝘆-𝗶𝗻𝘃𝗼𝗸𝗲𝗱 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻 𝗘𝘅𝗽𝗿𝗲𝘀𝘀𝗶𝗼𝗻𝘀 (𝗜𝗜𝗙𝗘), selebihnya lihat contohnya di point H8 di bawah.
*/

// H6. Contoh Closure

function init(){
  let nama = "Budi";
  function tampilNama(){                  // Di dalam Function tampilNama() tidak terdapat pendefinisian Var/Let nama, sehingga
    console.log(nama);                    // perintah console.log(nama) akan "mencari keluar" scope, dan ditemukanlah Let nama di
  }                                       // parent-nya, lalu digunakan. Dengan demikian Function tampilNama() disebut Closure.
  tampilNama();
}
init();                                   // Output: Budi

// H7. Contoh Factory Function

                                          // ᴘᴇɴᴜʟɪꜱᴀɴ ʟᴇʙɪʜ ʀɪɴɢᴋᴀꜱ:
function ucapkanSalam(waktu){             // function ucapkanSalam(waktu){
  function tampilkan(nama){               //   return function(nama){
    console.log(`${waktu}, ${nama}!`);    //     console.log(`${waktu}, ${nama}!`);
  }                                       //   }
  return tampilkan;                       // }
}
                                          // Cara baca:
let selamatPagi = ucapkanSalam("Pagi");   // ⤷ Jalankan Function ucapkanSalam() dengan mengirim argument berupa String "Pagi"
                                          // ⤷ Parameter waktu di ucapkanSalam(waktu) akan menangkap String "Pagi" dari argument
                                          // ⤷ Function ucapkanSalam() akan me-return (bukan menjalankan) Function tampilkan yang
                                          //   sudah menampung nilai dari waktu, yaitu String "Pagi" (Anggap: Sudah jalan ½ nya)
                                          // ⤷ Simpan hasil return tersebut kedalam Let selamatPagi

selamatPagi("Budi");                      // Output: Pagi, Budi!    ⇨ Menjalankan Factory Function selamatPagi("Budi");
selamatPagi("Joko");                      // Output: Pagi, Joko!    ⇨ Menjalankan Factory Function selamatPagi("Joko");

// H8-1. Function Expression VS IIFE

cetak = function(){                       // Cara penulisan Function Expression (Annonymous Function) biasa
  for (let i = 1; i <= 10; i++){
    console.log(i);
  }
}
cetak();                                  // Panggil Function untuk dijalankan

(function(){                              // Cara penulisan IIFE. Dengan cara seperti ini Function akan langsung dijalankan tanpa
  for (let i = 1; i <= 10; i++){          // perlu dipanggil terlebih dahulu layaknya Function Declaration/Expression biasa. IIFE
    console.log(i);                       // ditulis dengan pola (function() {...})(); Awalnya, dahulu IIFE digunakan untuk mem-
  }                                       // buat Function Scope (lihat kembali point F di atas), tujuannya agar Variable (var)
})();                                     // yang berada di dalam IIFE seolah bersifat Private dan tidak bisa diakses dari luar.
                                          // Namun semenjak ES6, kita tidak perlu repot lagi membuat IIFE, karena cukup gunakan
                                          // Let sebagai pengganti Var. Prilaku Let sudah Block Scope (seolah Private), tidak
                                          // lagi Function Scope seperti Var. Kegunaan lainnya dari IIFE, simak contoh di bawah.

// H8-2. Contoh IIFE (1)

                                          // ᴘᴇɴᴜʟɪꜱᴀɴ ʟᴇʙɪʜ ʀɪɴɢᴋᴀꜱ:
let sapa = (function(waktu){              // let sapa = (function(waktu){
  waktu = "Pagi";                         //   waktu = "Pagi";
  function tampilkan(nama){               //   return function(nama){
    console.log(`${waktu}, ${nama}!`);    //     console.log(`${waktu}, ${nama}!`);
  }                                       //   }
  return tampilkan;                       // })();
})();
                                          // Cara baca:
                                          // ⤷ Pada saat di assign ke Let sapa, Anonymous function(waktu) akan langsung berjalan
                                          //   begitu pula Inner Function-nya, yaitu function tampilkan(nama){ ... }. Hal ini
                                          //   berbeda dengan kasus di Factory Function yang "hanya berjalan ½ nya".

sapa("Budi");                             // Output: Pagi, Budi!    ⇨ Menjalankan IIFE sapa("Budi");
sapa("Joko");                             // Output: Pagi, Joko!    ⇨ Menjalankan IIFE sapa("Joko");

// H8-3. Contoh IIFE (2)

                                          // ᴘᴇɴᴜʟɪꜱᴀɴ ʟᴇʙɪʜ ʀɪɴɢᴋᴀꜱ:
let add = (function(){                    // let add = (function(){
  let counter = 0;                        //   let counter = 0;
  function tambah(){                      //   return function(){
    return ++counter;                     //     return ++counter;
  }                                       //   } 
  return tambah;                          // })();
})();

console.log(add());                       // Output: 1              ⇨ Menjalankan IIFE add();
console.log(add());                       // Output: 2              ⇨ Menjalankan IIFE add();
console.log(add());                       // Output: 3              ⇨ Menjalankan IIFE add();
```
<hr>

```Javascript
// =======================
// I. Arrow Function (ES6)
// =======================

/*
Arrow Function merupakan fitur baru ES6, digunakan sebagai alternatif penulisan Function Expressions. Arrow Function lebih
sederhana secara penulisan syntax. Namun tidak hanya itu, di BAB Advanced JavaScript nanti akan dibahas fitur lanjutannya.
*/

// Contoh tanpa Argument

let pagiA = function(){ return "Selamat Pagi!"; };    // Penulisan Function Expressions biasa
let pagiB = () => { return "Selamat Pagi!"; };        // Penulisan Function Expressions dengan Arrow Function

console.log(pagiA());                                 // Output: Selamat Pagi!
console.log(pagiB());                                 // Output: Selamat Pagi!

// Contoh dengan Argument

let totalA = function(a, b, c){ return a+b+c; };      // Penulisan Function Expressions biasa
let totalB = (a, b, c) => { return a+b+c; };          // Penulisan Function Expressions dengan Arrow Function

console.log(totalA(1, 2, 3));                         // Output: 6
console.log(totalB(1, 2, 3));                         // Output: 6
```

<br>
<div id="bab10"></div>

# 10. JavaScript Object <a href="#daftarisi">🡹</a>

<img src="images/BAB-10.png">

```Javascript
// ===========================
// A. Object sebagai Tipe Data
// ===========================

/*
JavaScript menggunakan konsep prototypical inheritance untuk menerapkan konsep pemrograman berbasis object. Singkatnya,
untuk membuat object di JavaScript, caranya dengan langsung menulis object tersebut (tidak perlu membuat class, seperti
yang dilakukan di bahasa pemrograman lain). Di dalam object, terdapat istilah property & method.

Property merupakan Var/Let yang berada di dalam object, sedangkan method merupakan Function yang berada di dalam object.
Untuk method, ditulis menggunakan Function expressions (Anonymous Function). Baik property maupun method diberi nilai
menggunakan tanda titik dua ":", bukan tanda sama dengan "=" sebagaimana layaknya pengisian Var/Let biasa. Serta,
diantara property/method yang satu dengan yang lain, dipisahkan menggunakan tanda koma ",".
*/

// A1. Pendefinisian Object

let objA = {};                        // Let objA berisi object kosong
console.log(typeof objA);             // Output: object

let objB = {                          // Let objB berisi object dengan property & method
  property1: "isi_property1",
  property2: "isi_property1",
  property3: "isi_property1",

  method1: function(){
    "isi method 1";
  },

  method2: function(){
    "isi method 2";
  }
};

// A2. Contoh Aplikasinya

let mobil = {                         // Let mobil berisi object seputar mobil (sebagai contoh saja)
  merk: "Toyota Avanza",
  tipe: "MPV",
  harga: 200000000,

  hidupkan: function(){
    return "Mesin Dihidupkan!";
  },
  pergi: function(tempat){
    return `Pergi ke ${tempat}`;
  }
};

// A3. Mengakses Property & Method

console.log(mobil.merk);              // Output: Toyota Avanza      ⇨ Mengakses property menggunakan dot notation (✔️ Recommended)
console.log(mobil["merk"]);           // Output: Toyota Avanza      ⇨ Mengakses property menggunakan bracket (❌ Not Recommended)
console.log(mobil.hidupkan());        // Output: Mesin Dihidupkan!  ⇨ Mengakses method tanpa argument
console.log(mobil.pergi("Bali"));     // Output: Pergi ke Bali      ⇨ Mengakses method dengan argument

// A4. Menambah Property & Method

mobil.warna = "Biru";                 // Menambah property warna ke object mobil (ditambahkan di luar pendefinisian object mobil)
mobil.modif = true;                   // Menambah property modif ke object mobil (ditambahkan di luar pendefinisian object mobil)
mobil.matikan = function(){           // Menambah method matikan ke object mobil (ditambahkan di luar pendefinisian object mobil)
  return "Mesin Dimatikan!";
};
console.log(mobil.warna);             // Output: Biru
console.log(mobil.modif);             // Output: true
console.log(mobil.matikan());         // Output: Mesin Dimatikan!

// A5. Mengubah nilai Property & Method

console.log(mobil.merk);              // Output: Toyota Avanza      (Nilai property merk sebelum diubah)
console.log(mobil.tipe);              // Output: MPV                (Nilai property tipe sebelum diubah)
console.log(mobil.hidupkan());        // Output: Mesin Dihidupkan!  (Hasil return method hidupkan sebelum diubah)

mobil.merk = "Honda Civic";           // Menimpa nilai property merk dari object mobil
mobil.tipe = "Sedan";                 // Menimpa nilai property tipe dari object mobil
mobil.hidupkan = function(){          // Menimpa nilai method hidupkan dari object mobil
  return "Mesin Dinyalakan!";
};

console.log(mobil.merk);              // Output: Honda Civic        (Nilai property merk sesudah diubah)
console.log(mobil.tipe);              // Output: Sedan              (Nilai property tipe sesudah diubah)
console.log(mobil.hidupkan());        // Output: Mesin Dinyalakan!  (Hasil return method hidupkan sesudah diubah)
```
<hr>

```Javascript
// ================
// B. Nested Object
// ================

let mahasiswa = {
  nama: "Budi",
  jurusan: "Informatika",
  ipk: {                              // Nested object (object ipk di dalam object mahasiswa)
    semester1: 3.1,
    semester2: 3.6,
  },
  smt: 3
};

console.log(mahasiswa.ipk)            // Output: {semester1: 3.1, semester2: 3.6}
console.log(mahasiswa.ipk.semester1)  // Output: 3.1                ⇨ Mengakses nested object dengan dot notation
console.log(mahasiswa.ipk.semester2)  // Output: 3.6                ⇨ Mengakses nested object dengan dot notation
```
<hr>

```Javascript
// ===================
// C. Object Reference
// ===================

// C1. Tipe Data Primitif: Assignment by Value

let motor = "NMax";
let motorBaru = motor;                // Assignment by Value        ⇨ Value (nilai) dari let motor di-copy ke let motorBaru
console.log(motor);                   // Output: NMax
console.log(motorBaru);               // Output: NMax

motorBaru = "Ninja";                  // Update nilai motorBaru
console.log(motor);                   // Output: NMax               ⇨ Nilai dari motor tidak terpengaruh
console.log(motorBaru);               // Output: Ninja              ⇨ Nilai dari motorBaru sudah berubah

motor = "PCX";                        // Update nilai motor
console.log(motor);                   // Output: PCX
console.log(motorBaru);               // Output: Ninja

// C2. Tipe Data Object: Assignment by Reference

let mobil = {
  merk: "Toyota Avanza",
  tipe: "MPV"
};
let mobilBaru = mobil;                // Assignment by reference    ⇨ Reference (alamat memory) mobil di-copy ke mobilBaru
console.log(mobil.merk);              // Output: Toyota Avanza
console.log(mobilBaru.merk);          // Output: Toyota Avanza

mobilBaru.merk = "Honda Civic";       // Update nilai mobilBaru.merk
console.log(mobil.merk);              // Output: Honda Civic        ⇨ Nilai dari mobil.merk ikut terpengaruh
console.log(mobilBaru.merk);          // Output: Honda Civic        ⇨ Nilai dari mobilBaru.merk sudah berubah

mobil.tipe = "Sedan";                 // Update nilai mobil.tipe
console.log(mobil.tipe);              // Output: Sedan
console.log(mobilBaru.tipe);          // Output: Sedan

// C3. Efek Assignment by Reference di Operasi Perbandingan

let mhs1 = {
  nama: "Budi",
  jurusan: "Informatika"
};
let mhs1Baru = mhs1;                  // Assignment by reference
console.log(mhs1 == mhs1Baru);        // Output: true
console.log(mhs1 === mhs1Baru);       // Output: true

let mhs2 = {
  nama: "Joko",
  jurusan: "Arsitektur"
};
let mhs2Baru = {
  nama: "Joko",
  jurusan: "Arsitektur"
};
console.log(mhs2 == mhs2Baru);        // Output: false  (Why? meskipun mhs2 & mhs2Baru isinya sama, tapi berbeda alamat memory)
console.log(mhs2 === mhs2Baru);       // Output: false  (Why? meskipun mhs2 & mhs2Baru isinya sama, tapi berbeda alamat memory)
```

<br>
<div id="bab11"></div>

# 11. Object Oriented Programming (OOP) <a href="#daftarisi">🡹</a>

<img src="images/BAB-11.png">

```Javascript
// ==========================================
// A. Paradigma Pemrograman Prosedural vs OOP
// ==========================================

// A1. Paradigma: Prosedural (berbasiskan Function)

// ...                                // Asumsi terdapat sebuah Function potongTeks yang gunanya ya tentu memotong sebuah teks
let teks = "Hello World";
let hasil = potongTeks(teks, 6, 10);  // Output: World  ⇨ Berbasiskan Function

// A2. Paradigma: Object Oriented Programming (OOP)

// ...                                // Asumsi sudah terdapat sebuah method potongTeks di dalam String Object (lihat point C1)
let teks = new String("Hello World"); // Sebenarnya sama aja dengan let teks = "Hello World"; (lihat point A3)
let hasil = teks.potongTeks(6, 10);   // Output: World  ⇨ berbasiskan object (mengakses method potongTeks dengan dot notation)
                                      // 𝗡𝗼𝘁𝗲: 𝘁𝗲𝗿𝗸𝗮𝗶𝘁 𝗸𝗲𝘆𝘄𝗼𝗿𝗱 𝗻𝗲𝘄 (𝗹𝗶𝗵𝗮𝘁 𝗽𝗼𝗶𝗻𝘁 𝗕𝟯)

// A3. Penulisan Literals vs Object Constructor

let num1 = 52;                        // Cara penulisan: Number literals  (✔️ Recommended)
let num2 = new Number(52);            // Cara penulisan: Number object    (❌ Not Recommended)
let str1 = "Belajar JS";              // Cara penulisan: String literals  (✔️ Recommended)
let str2 = new String("Belajar JS");  // Cara penulisan: String Object    (❌ Not Recommended)
let bol1 = true;                      // Cara penulisan: Boolean literals (✔️ Recommended)
let bol2 = new Boolean(true);         // Cara penulisan: Boolean object   (❌ Not Recommended)
let arr1 = [1, 2, 3];                 // Cara penulisan: Array literals   (✔️ Recommended)
let arr2 = new Array(1, 2, 3);        // Cara penulisan: Array object     (❌ Not Recommended)
let obj1 = {nama: "Budi", umur: 24};  // Cara penulisan: Object literals  (✔️ Recommended)
let obj2 = new Object();              // Cara penulisan: Object object    (❌ Not Recommended)
obj2.nama = "Budi";                   // ⤷ property & method didefinisikan
obj2.umur = 24;                       // ⤷ setelah Object object dibuat
let reg1 = /ab+c/;                    // Cara penulisan: RegExp literals  (✔️ Recommended)      𝗥𝗲𝗴𝗘𝘅𝗽 𝗕𝗔𝗕 𝟭𝟮 (𝗗)!
let reg2 = new RegExp("ab+c");        // Cara penulisan: RegExp object    (❌ Not Recommended)
let date = new Date(2016,11,2,9,30);  // Cara penulisan: Date object      (✔️ Recommended)      𝗗𝗮𝘁𝗲 𝗕𝗔𝗕 𝟭𝟮 (𝗙)!
                                      // ⤷ Date tidak ada literals-nya

let fun1 = function (a, b){ return a+b; };        // Cara penulisan: Function Expressions/Anonymous Function  (✔️ Recommended)
let fun2 = new Function('a', 'b', 'return a+b');  // Cara penulisan: Function object                          (❌ Not Recommended)
```
<hr>

```Javascript
// ========================================================
// B. Object sebagai OOP / Object sebagai bagian dari Class
// ========================================================

// B1. Tanpa OOP (Pendefinisian object biasa)

let mobilBudi = {
  merk: "Toyota Avanza",
  tipe: "MPV",
  harga: 200000000,
    hidupkan: function(){
    return "Mesin Dihidupkan!";
  },
  pergi: function(tempat){
    return `Pergi ke ${tempat}`;
  }
};

let mobilJoko = {
  merk: "Honda Civic",
  tipe: "Sedan",
  harga: 200000000,
    hidupkan: function(){
    return "Mesin Dihidupkan!";
  },
  pergi: function(tempat){
    return `Pergi ke ${tempat}`;
  }
};

/*
Object mobilBudi & mobilJoko sebenarnya memiliki property dan method yang sama. Bagaimana jika nanti ada object mobilPutri,
mobilAndi, dst, misalya kita butuh hingga 100 object mobil (dengan property dan method yang sama), maka akan sangat tidak
efisien jika object tersebut ditulis secara manual satu per satu secara berulang. Oleh karena itulah, konsep OOP hadir
sebagai solusi, dimana kita dapat menggunakan Class sebagai wadah yang menyediakan semua hal yang dibutuhkan oleh object.

Class berperan sebagai "blue print"/cetakan/sesuatu yang masih abstrak yang menjadi kelompok umum dari object. Misalnya,
jika Mobil adalah Class, maka mobilBudi, mobilJoko, mobilPutri, dst merupakan object dari Class Mobil. Jika Binatang adalah
Class, maka sapi, kambing, kuda, dst merupakan object dari Class Binatang. Simak penjelasan di point B2 & B3 di bawah ini.
*/
```

```JavaScript
// B2. Dengan OOP: Menggunakan Cara Lama (❌)

// ➊ OOP dengan Function Declaration

function Mobil(merkArg, tipeArg, hargaArg){       // Function Declaration yang berfungsi sebagai "blue print mobil"
  let mobil   = {};                               // Note: Harus ada deklarasi Object kosong, sebagai "penampung"
  mobil.merk  = merkArg;
  mobil.tipe  = tipeArg;
  mobil.harga = hargaArg;
  mobil.hidupkan = function(){
    return `Mesin ${mobil.merk} dihidupkan!`; 
  }
  mobil.pergi = function(tempat){
    return `${mobil.merk} pergi ke ${tempat}`;
  }
  return mobil;                                   // Note: Di baris akhir Function Declaration harus ada return
}

// ➋ OOP dengan Function Declaration + Object.create()

const khususMethod = {
  hidupkan: function(){
    return `Mesin ${this.merk} dihidupkan!`;      // 𝗡𝗼𝘁𝗲: 𝘁𝗲𝗿𝗸𝗮𝗶𝘁 𝗸𝗲𝘆𝘄𝗼𝗿𝗱 𝘁𝗵𝗶𝘀 (𝗹𝗶𝗵𝗮𝘁 𝗽𝗼𝗶𝗻𝘁 𝗕𝟱)
  },
  pergi: function(tempat){
    return `${this.merk} pergi ke ${tempat}`;
  }
}

function Mobil(merkArg, tipeArg, hargaArg){       // Function Declaration yang berfungsi sebagai "blue print mobil"
  let mobil   = Object.create(khususMethod);      // Note: Sebenarnya sama dengan "let mobil = {}", hanya saja dengan
  mobil.merk  = merkArg;                          //       menggunakan Object.create() kita dapat menyimpan parameter
  mobil.tipe  = tipeArg;                          //       yang mengacu ke Object lainnya, tujuannya untuk membawa
  mobil.harga = hargaArg;                         //       propery & method dari Object lainnya tersebut.
  return mobil;                                   // Note: Di baris akhir Function Declaration harus ada return
}

// ➌ Membuat Object dari point 1 & 2 di atas

let mobilBudi = Mobil("Toyota Avanza", "MPV", 200000000);   // Proses instansiasi objek Mobil baru (tanpa keyword new)
let mobilJoko = Mobil("Honda Civic", "Sedan", 200000000);

console.log(mobilBudi instanceof Mobil);          // Output: false  ⇨ Karena memang kita tidak instansiasi Object
console.log(mobilJoko instanceof Mobil);          // Output: false     dengan keyword new (Lihat point B3-3 di bawah)

console.log(mobilBudi.merk);                      // Output: Toyota Avanza
console.log(mobilBudi.hidupkan());                // Output: Mesin Toyota Avanza dihidupkan!
console.log(mobilBudi.pergi("Bali"));             // Output: Toyota Avanza pergi ke Bali

console.log(mobilJoko.merk);                      // Output: Honda Civic
console.log(mobilJoko.hidupkan());                // Output: Mesin Honda Civic dihidupkan!
console.log(mobilJoko.pergi("Solo"));             // Output: Honda Civic pergi ke Solo
```

```JavaScript
// B3. Dengan OOP: Menggunakan Cara Baru (✔️)

// ➊ OOP dengan Constructor Functions (Sebelum ES6)

function Mobil(merkArg, tipeArg, hargaArg){       // Constructor Functions sebagai "blue print mobil"
  this.merk   = merkArg;                          // 𝗡𝗼𝘁𝗲: 𝘁𝗲𝗿𝗸𝗮𝗶𝘁 𝗸𝗲𝘆𝘄𝗼𝗿𝗱 𝘁𝗵𝗶𝘀 (𝗹𝗶𝗵𝗮𝘁 𝗽𝗼𝗶𝗻𝘁 𝗕𝟱)
  this.tipe   = tipeArg;                          // Note: Tidak perlu ada deklarasi Object kosong dan keyword return
  this.harga  = hargaArg;                         //       di baris akhir Function, karena dengan menggunakan Constructor
  this.hidupkan = function(){                     //       Functions, di belakang layar JavaScript secara otomatis membuat:
    return `Mesin ${this.merk} dihidupkan!`;      //       ⤷ 𝗹𝗲𝘁 𝘁𝗵𝗶𝘀 = 𝗢𝗯𝗷𝗲𝗰𝘁.𝗰𝗿𝗲𝗮𝘁𝗲(𝗠𝗼𝗯𝗶𝗹.𝗽𝗿𝗼𝘁𝗼𝘁𝘆𝗽𝗲);
  }                                               //       ⤷ 𝗿𝗲𝘁𝘂𝗿𝗻 𝘁𝗵𝗶𝘀;
  this.pergi = function(tempat){
    return `${this.merk} pergi ke ${tempat}`;
  }
}

// ➋ OOP dengan Class (Setelah ES6)

class Mobil{                                      // Class sebagai "blue print mobil" (Kedepannya Class inilah yang akan digunakan)
  constructor(merkArg, tipeArg, hargaArg){        // Note: Setiap property wajib berada di dalam method constructor(), 
    this.merk   = merkArg;                        //       yaitu sebuah method yang otomatis dijalankan pada saat proses
    this.tipe   = tipeArg;                        //       instansiasi/pembuatan object.
    this.harga  = hargaArg; 
  }
  hidupkan(){                                     // Cara penulisan method: Langsung ditulis nama Functionnya (simple!)
    return `Mesin ${this.merk} dihidupkan!`;
  }
  pergi(tempat){
    return `${this.merk} pergi ke ${tempat}`;
  }
}

// ➌ Membuat Object dari point 1 & 2 di atas

let mobilBudi = new Mobil("Toyota Avanza", "MPV", 200000000);   // Proses instansiasi objek Mobil baru menggunakan keyword new
let mobilJoko = new Mobil("Honda Civic", "Sedan", 200000000);   // (Instansiasi: membuat sesuatu yang berwujud dari yang abstrak)

console.log(mobilBudi instanceof Mobil);          // Output: true   ⇨ Operator instanceof digunakan memeriksa apakah suatu object
console.log(mobilJoko instanceof Mobil);          // Output: true      merupakan instance dari sebuah Constructor Functions/Class

console.log(mobilBudi.merk);                      // Output: Toyota Avanza
console.log(mobilBudi.hidupkan());                // Output: Mesin Toyota Avanza dihidupkan!
console.log(mobilBudi.pergi("Bali"));             // Output: Toyota Avanza pergi ke Bali

console.log(mobilJoko.merk);                      // Output: Honda Civic
console.log(mobilJoko.hidupkan());                // Output: Mesin Honda Civic dihidupkan!
console.log(mobilJoko.pergi("Solo"));             // Output: Honda Civic pergi ke Solo

/*
Bisa dilihat bahwa dengan menerapkan konsep OOP melalui Constructor Functions maupun Class (kedepannya kita hanya akan menggunakan
Class saja), kita tidak usah repot-repot menulis object mobil secara manual satu per satu secara berulang (seperti yang dilakukan
di point B1), cukup dengan membuat "blue print"/"wadah"/cetakan berupa Class, lalu buat object yang diinginkan melalui proses
instansiasi, mudah dan cepat, bahkan jika kita butuh 100 object sekalipun. Ini akan terasa manfaatnya saat aplikasi sudah besar.
*/
```

```JavaScript
// B4. Menambah property & method sebuah Class dengan Prototype

Mobil.prototype.jumlahRoda = 4;                   // Menambahkan property jumlahRoda ke Class Mobil (di luar pendefinisian Class)
Mobil.prototype.pulang = function(tempat){        // Menambahkan method pulang ke Class Mobil (di luar pendefinisian Class)
  return `${this.merk} pulang ke ${tempat}`;      // Cara penulisan method: Function Expressions (Anonymous Function)
}

console.log(mobilBudi.jumlahRoda);                // Output: 4
console.log(mobilBudi.pulang("Bandung"));         // Output: Toyota Avanza pulang ke Bandung

console.log(mobilJoko.jumlahRoda);                // Output: 4
console.log(mobilJoko.pulang("Jakarta"));         // Output: Honda Civic pulang ke Jakarta

// B5. Penjelasan dibalik keyword this

/*
this adalah object khusus sebagai pengganti object yang nantinya dibuat dari Class tertentu. Misal kita mengacu ke Class Mobil
di point B3-2, maka setiap kali instansiasi object Mobil baru menggunakan keyword new, yang terjadi di belakang layar yaitu
keyword this akan diganti sesuai dengan instansiasi object Mobil barunya. Jika instansisasi object mobilBudi, maka this akan
diganti menjadi mobilBudi. Dengan demikian keyword this ini membuat sebuah Class menjadi "fleksibel". Simak penjelasan berikut:
*/

// saat instansiasi object mobilBudi (lihat B3)   ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
class Mobil{                                      // class Mobil{
  constructor(merkArg, tipeArg, hargaArg){        //   constructor(merkArg, tipeArg, hargaArg){
    this.merk = merkArg;                          //     mobilBudi.merk = merkArg;                      🡲 this menjadi mobilBudi
    this.tipe = tipeArg;                          //     mobilBudi.tipe = tipeArg;                      🡲 this menjadi mobilBudi
    this.harga = hargaArg;                        //     mobilBudi.harga = hargaArg;                    🡲 this menjadi mobilBudi
  }                                               //   }
  hidupkan(){                                     //   hidupkan(){
    return `Mesin ${this.merk} dihidupkan!`;      //     return `Mesin ${mobilBudi.merk} dihidupkan!`;  🡲 this menjadi mobilBudi
  }                                               //   }
  pergi(tempat){                                  //   pergi(tempat){
    return `${this.merk} pergi ke ${tempat}`;     //     return `${mobilBudi.merk} pergi ke ${tempat}`; 🡲 this menjadi mobilBudi
  }                                               //   }
}                                                 // }

// saat instansiasi object mobilJoko (lihat B3)   ʏᴀɴɢ ᴛᴇʀᴊᴀᴅɪ ᴅɪ ʙᴇʟᴀᴋᴀɴɢ ʟᴀʏᴀʀ:
class Mobil{                                      // class Mobil{
  constructor(merkArg, tipeArg, hargaArg){        //   constructor(merkArg, tipeArg, hargaArg){
    this.merk = merkArg;                          //     mobilJoko.merk = merkArg;                      🡲 this menjadi mobilJoko
    this.tipe = tipeArg;                          //     mobilJoko.tipe = tipeArg;                      🡲 this menjadi mobilJoko
    this.harga = hargaArg;                        //     mobilJoko.harga = hargaArg;                    🡲 this menjadi mobilJoko
  }                                               //   }
  hidupkan(){                                     //   hidupkan(){
    return `Mesin ${this.merk} dihidupkan!`;      //     return `Mesin ${mobilBudi.merk} dihidupkan!`;  🡲 this menjadi mobilJoko
  }                                               //   }
  pergi(tempat){                                  //   pergi(tempat){
    return `${this.merk} pergi ke ${tempat}`;     //     return `${mobilBudi.merk} pergi ke ${tempat}`; 🡲 this menjadi mobilJoko
  }                                               //   }
}                                                 // }
```
<hr>

```Javascript
// ==========================================
// C. JavaScript Native Object (Introduction)
// ==========================================

/*
Sampai disini, kita telah membuat object sebagai tipe data (BAB 10) maupun object sebagai OOP-bagian dari Class (BAB 11), keduanya
merupakan object yang kita buat (definisikan) sendiri. Selain itu, JavaScript memiliki object bawaan (JavaScript Native Object)
yang bisa kita gunakan secara langsung. Object bawaan ini memiliki banyak property & method. 📚 Daftar lengkap object bawaan
JavaScript dapat dilihat di: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects

Di buku ini akan dibahas beberapa diantaranya yang paling populer (dibahas di BAB 12), yaitu:
• Number      • Math
• String      • Array
• Boolean     • RegExp
• Function    • Date

4 istilah yang perlu diketahui terlebih dahulu (lihat perbedaan bagaimana cara mengaksesnya):
• Object property             Contoh: console.log(Number.MAX_VALUE);                            🡲 Output: 1.7976931348623157e+308
• Object method               Contoh: console.log(Number.parseInt("12.045"));                   🡲 Output: 12 (Number, not String)
• Object instance property    Contoh: let foo = "Belajar JavaScript"; console.log(foo.length);  🡲 Output: 18 
• Object instance method      Contoh: let foo = 50.12345; console.log(foo.toPrecision(5));      🡲 Output: 50.123

⤷ Object property & Object method melekat langsung ke Object-nya (Class-nya): Number.MAX_VALUE & Number.parseInt("12.045"),
  dimana Number merupakan Object-nya, sedangkan MAX_VALUE sebagai Object property & parsetInt() sebagai Object method-nya.
  - Penulisan formal: Number.MAX_VALUE, Number.parseInt(), dst. (perhatikan ada polanya, yaitu: Object.property/method())

⤷ Object instance property & Object instance method melekat ke Instance Object: foo.length & foo.toPrecision(), dimana foo
  merupakan hasil instance dari Object (Class) String (untuk foo.length) & hasil instance dari Object Number (untuk foo.
  toPrecision(5)), sedangkan length sebagai Object instance property & toPrecision() sebagai Object instance method-nya.
  - Penulisan formal: String.prototype.length, Number.prototype.toPrecision(), dst. (pola: Object.prototype.property/method())
  - Mengapa perlu tahu penulisan formalnya? Nantinya pada saat buka dokumentasi JavaScript Native Object di MDN, kita dapat
    dengan mudah membedakan mana Object property/Object method dengan Object instance property/Object instance method.

Note: Tidak semua Object bawaan JavaScript secara utuh memiliki Object property, Object method, Object instance property,
dan Object instance method. Misal seperti Math Object (lihat di BAB 12), hanya memiliki Object property & Object method saja.
Selain itu, buku ini hanya akan membahas Object property/Object method/Object instance property/Object instance method yang
umum saja. 📚 Referensi lengkap lihat di: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects

⚠️ Beberapa method bersifat Mutating (mengubah Object/data aslinya), selebihnya Non-Mutating (tidak mengubah data aslinya).
*/

// C1. Contoh: String (object)

let foo = new String("Hello World");  // Kita tidak pernah mendefinisikan Class String bukan? tetapi kenapa langsung bisa dipakai?
                                      // itu karena, String merupakan salah satu object bawaan JavaScript. Ingat saat kita instan-
                                      // siasi object Mobil baru dengan perintah "let mobilBudi = new Mobil(...)", itu bisa kita
                                      // lakukan karena sebelumnya kita sudah membuat Class Mobil. Nah, String itu "Class bawaan".

console.log(foo.toUpperCase());       // Output: HELLO WORLD. Kita tidak pernah mendefinisikan method toUpperCase() bukan? tetapi
                                      // kenapa langsung bisa dipakai (melalui dot notation)? itu karena, toUpperCase() merupakan 
                                      // salah satu "Instance method" bawaan milik String Object, jadi kita bisa langsung pakai.
console.log(foo.length)               // Output: 11. length merupakan salah satu "Instance property" bawaan milik String Object.

// C2. Contoh: String (literals)

let bar = "Hello World";              // Cara penulisan: String literals (lebih "hemat" dibandingkan Object Constructor di atas)
console.log(bar.toUpperCase());       // Output: HELLO WORLD. Ternyata meskipun Var/Let bar didefinisikan secara String literals,
                                      // bukan secara String Object, kita masih tetap bisa memakai "Instance method" bawaan String
                                      // object. Oleh karena itu penulisan literals lebih direkomendasikan (lihat lagi point A3).
console.log(bar.length);              // Output: 11. Kita pun masih tetap bisa memakai "Instance property" bawaan String Object.
```

<br>
<div id="bab12"></div>

# 12. JavaScript Native Object <a href="#daftarisi">🡹</a>

<img src="images/BAB-12-1.png">

<img src="images/BAB-12-2.png">

```Javascript
// ================
// A. Number Object
// ================

// A1. Object property

console.log(Number.EPSILON);          // Output: 2.220446049250313e-16    ⇨ Interval terkecil dari dua angka di dalam JS
console.log(Number.MAX_VALUE);        // Output: 1.7976931348623157e+308  ⇨ Angka tertinggi yang bisa ditampung di dalam JS
console.log(Number.MIN_VALUE);        // Output: 5e-324                   ⇨ Angka positif terkecil yang bisa ditampung JS
console.log(Number.MAX_SAFE_INTEGER); // Output: 9007199254740991         ⇨ Nilai maksimum integer (standar IEEE-754) ≈ 2⁵³-1
console.log(Number.MIN_SAFE_INTEGER); // Output: -9007199254740991        ⇨ Nilai minimum integer (standar IEEE-754) ≈ -(2⁵³-1)
console.log(Number.NaN);              // Output: NaN                      ⇨ Cara untuk membuat nilai NaN (Not a Number)
console.log(Number.POSITIVE_INFINITY) // Output: Infinity                 ⇨ Cara untuk membuat nilai infinity
console.log(Number.NEGATIVE_INFINITY) // Output: -Infinity                ⇨ Cara untuk membuat nilai -infinity

// A2. Object method

console.log(Number.isNaN(5/'a'));                     // Output: true     ⇨ Check apakah hasil operasi/suatu Var/Let berisi NaN
console.log(Number.isNaN(Number.NaN));                // Output: true
console.log(Number.isFinite(3.21456));                // Output: true     ⇨ Check apakah sebuah nilai/Var/Let berisi angka standar
console.log(Number.isFinite(1/0));                    // Output: false
console.log(Number.isInteger(9007199254740992));      // Output: true     ⇨ Check apakah suatu nilai/Var/Let berisi angka integer
console.log(Number.isInteger(3.21456));               // Output: false
console.log(Number.isSafeInteger(9007199254740992));  // Output: false    ⇨ Sama seperti isInteger, tapi dibatasi standar IEEE-754
console.log(Number.isSafeInteger(3.21456));           // Output: false
console.log(Number.parseFloat("1.23"));               // Output: 1.23 (number)  ⇨ Mengkonversi String menjadi Number (Pecahan)
console.log(Number.parseFloat("10.3% keuntungan"));   // Output: 10.3 (number)  ⤷ Selain Number akan dihilangkan di Output-nya
console.log(Number.parseInt("1.23"));                 // Output: 1    (number)  ⇨ Mengkonversi String menjadi Number (Bulat)
console.log(Number.parseInt("10.3% keuntungan"));     // Output: 10   (number)  ⤷ Default: proses sebagai desimal (Basis 10)
console.log(Number.parseInt("10101101", 2));          // Output: 173  (number)  ⤷ 2 artinya: proses sebagai biner (Basis 2)
console.log(Number.parseInt("255", 8));               // Output: 173  (number)  ⤷ 8 artinya: proses sebagai oktal (Basis 8)
console.log(Number.parseInt("AD", 16));               // Output: 173  (number)  ⤷ 8 artinya: proses sebagai heksa (Basis 16)

// A3. Object instance method

numA = 500.123;
numB = 50;
numC = 1234500.346;

console.log(numA.toExponential());    // Output: 5.00123e+2       ≈ 5.00123x10² ⇨ Format angka menjadi scientific notation
console.log(numA.toExponential(1));   // Output: 5.0e+2           ≈ 5.0x10²
console.log(numA.toExponential(5));   // Output: 5.00123e+2       ≈ 5.00123x10² 
console.log(numA.toExponential(10));  // Output: 5.0012300000e+2  ≈ 5.0012300000x10²
console.log(numA.toFixed());          // Output: 500              ⇨ Format angka dengan jumlah digit desimal (angka belakang koma)
console.log(numA.toFixed(1));         // Output: 500.1              yang tetap, toFixed(5) artinya 5 digit angka di belakang koma.
console.log(numA.toFixed(5));         // Output: 500.12300
console.log(numA.toFixed(10));        // Output: 500.1230000000
console.log(numA.toPrecision());      // Output: 500.123          ⇨ Format angka dengan jumlah digit yang tetap, toPrecision(5)
console.log(numA.toPrecision(1));     // Output: 5e+2               artinya total digit angka berjumlah 5 digit.
console.log(numA.toPrecision(5));     // Output: 500.12
console.log(numA.toPrecision(10));    // Output: 500.1230000
console.log(numB.toString());         // Output: 50     (string)  ⇨ Mengkonversi Number menjadi String
console.log(numB.toString(2));        // Output: 110010 (string)  ⤷ Konversi ke biner (Basis 2)
console.log(numB.toString(8));        // Output: 62     (string)  ⤷ Konversi ke oktal (Basis 8) 
console.log(numB.toString(16));       // Output: 32     (string)  ⤷ Konversi ke heksa (Basis 16)
console.log(numC.toLocaleString('id-ID'));  // Output: 1.234.500,346  ⇨ Konversi Number ke String + memakai format angka lokal
console.log(numC.toLocaleString('en-US'));  // Output: 1,234,500.346  ⤷ en-US: Format angka Amerika Serikat (US)
console.log(numC.toLocaleString('fr-FR'));  // Output: 1 234 500,346  ⤷ fr-FR: Format angka Perancis (FR)
console.log(numC.toLocaleString('id-ID', {style: 'decimal'}));                    // Output: 1.234.500,346    (Default)
console.log(numC.toLocaleString('id-ID', {style: 'percent'}));                    // Output: 123.450.035%     (Persen)
console.log(numC.toLocaleString('id-ID', {style: 'currency', currency: 'IDR'}));  // Output: Rp 1.234.500,35  (Mata uang)
```
<hr>

```Javascript
// ==============
// B. Math Object
// ==============

// B1. Object property

console.log(Math.E);                  // Output: 2.718281828459045        ⇨ Angka logaritma natural e
console.log(Math.LN10);               // Output: 2.302585092994046        ⇨ Angka logaritma natural 10
console.log(Math.LN2);                // Output: 0.6931471805599453       ⇨ Angka logaritma natural 2
console.log(Math.LOG10E);             // Output: 0.4342944819032518       ⇨ Angka logaritma natural e basis 10
console.log(Math.LOG2E);              // Output: 1.4426950408889634       ⇨ Angka logaritma natural e basis 2
console.log(Math.PI);                 // Output: 3.141592653589793        ⇨ Angka pi (π)
console.log(Math.SQRT1_2);            // Output: 0.7071067811865476       ⇨ Angka 1 dibagi dengan akar kuadrat 2
console.log(Math.SQRT2);              // Output: 1.4142135623730951       ⇨ Angka akar kuadrat dari 2

let jariJari = 7;                                     // Studi kasus: contoh penggunaan Math.PI & toFixed() untuk mencari luas
let luasLingkaran = Math.PI * jariJari * jariJari;    // lingkaran kemudian memformat angkanya dengan jumlah digit desimal = 2
console.log(luasLingkaran);                           // Output: 153.93804002589985
console.log(luasLingkaran.toFixed(2));                // Output: 153.94

// B2. Object method

console.log(Math.floor(12.54));       // Output: 12             ⇨ Pembulatan ke bawah
console.log(Math.ceil(12.54));        // Output: 13             ⇨ Pembulatan ke atas
console.log(Math.round(12.54));       // Output: 13             ⇨ Pembulatan ke bawah jika < 0.5 & pembulatan ke atas jika >= 0.5
console.log(Math.random());           // Output: 0.734554...    ⇨ Generate angka acak rentang 0-1 (0, 0.9, dst), 1 tidak termasuk
console.log(Math.max(45,90,12,55));   // Output: 90             ⇨ Mencari nilai paling besar dari angka yang di input di argument
console.log(Math.min(45,90,12,55));   // Output: 12             ⇨ Mencari nilai paling kecil dari angka yang di input di argument
console.log(Math.abs(-5));            // Output: 5              ⇨ Menghasilkan nilai absolut, jika angka negatif maka jadi positif
console.log(Math.pow(5, 2));          // Output: 25 ≈ 5²        ⇨ Pemangkatan angka (Update: sudah diganti dengan operator **)
console.log(Math.sqrt(81));           // Output: 9              ⇨ Akar kuadrat dari suatu angka (81 ya 9, karena 81 dari 9x9) 
console.log(Math.log(10));            // Output: 2.302585...    ⇨ Mencari nilai logaritma natural (e)
console.log(Math.log10(1000));        // Output: 3              ⇨ Mencari nilai logaritma basis 10 (desimal) (Biasa digunakan)
console.log(Math.log2(256));          // Output: 8              ⇨ Mencari nilai logaritma basis 2 (biner)
console.log(Math.sin(60));            // Output: -0.30481...    ⇨ Mencari nilai sinus   (Nilai argument: radian, bukan derajat)
console.log(Math.cos(60));            // Output: -0.95241...    ⇨ Mencari nilai cosinus (Nilai argument: radian, bukan derajat)
console.log(Math.tan(60));            // Output: 0.320040...    ⇨ Mencari nilai tangen  (Nilai argument: radian, bukan derajat)

let mthA = Math.floor(Math.random()*(10))   // Studi kasus: tips untuk generate angka bulat acak rentang 0-9 (tidak lagi pecahan!)
console.log(mthA);                          // Output: 7 (contoh)

let mthB = [45, 90, 12, 55];                // Studi kasus: mencari nilai paling besar/kecil dari Array (pakai spread operator)
console.log(Math.max(...mthB));             // Output: 90
console.log(Math.min(...mthB));             // Output: 12
```
<hr>

```Javascript
// ================
// C. String Object
// ================

// C1. Object method

console.log(String.fromCharCode(65, 66, 67));               // Output: ABC      ⇨ Membuat String berdasarkan kode unicode
console.log(String.fromCharCode(9749, 10052, 12096));       // Output: ☕❄⽀   ⤷ Penulisan dengan nomor urut desimal
console.log(String.fromCharCode(0x2615, 0x2744, 0x2F40));   // Output: ☕❄⽀   ⤷ Penulisan dengan nomor urut heksadesimal (0x...)
console.log(String.fromCharCode(128656, 128663, 128690));   // Output:      ‏‏‎ ‎‎⤷ Gagal menampilkan karakter terbaru unicode
console.log(String.fromCodePoint(65, 66, 67));              // Output: ABC      ⇨ Membuat String berdasarkan kode unicode (ES6)
console.log(String.fromCodePoint(9749, 10052, 12096));      // Output: ☕❄⽀     fromCodePoint "Versi Update" dari fromCharCode
console.log(String.fromCodePoint(0x2615, 0x2744, 0x2F40));  // Output: ☕❄⽀
console.log(String.fromCodePoint(128656, 128663, 128690));  // Output: 🚐🚗🚲  ⤷ Berhasil menampilkan karakter terbaru unicode
                                                            // 📚 Daftar Karakter Latin-1 & Unicode: http://unicode-table.com/ 

// C2. Object instance property

let strA = "Hello World!";
let strB = "Belajar JavaScript";

console.log(strA.length);               // Output: 12       ⇨ Mengambil info panjang karakter dari sebuah String
console.log(strB.length);               // Output: 18       ⤷ Banyak digunakan di validasi form, misal syarat minimal 8 karakter

// C3. Object instance method

let strC = "Bandung";
let strD = "Bandung kota kembang";
let strE = "Satu, dua, tiga, empat";
let strF = "satu,dua;tiga-empat";
let strG = "  username  ";

console.log(strC.toLowerCase());        // Output: bandung  ⇨ Mengubah String menjadi huruf kecil
console.log(strC.toUpperCase());        // Output: BANDUNG  ⇨ Mengubah String menjadi huruf besar
console.log(strC.toLocaleLowerCase());  // Output: bandung  ⇨ Serupa dengan toLowerCase namun sesuai settingan bahasa lokal
console.log(strC.toLocaleUpperCase());  // Output: BANDUNG  ⇨ Serupa dengan toUpperCase namun sesuai settingan bahasa lokal
console.log(strC.charAt(0));            // Output: B        ⇨ Menampilkan karakter yang berada di posisi tertentu dari String
console.log(strC.charAt(5));            // Output: n        ⤷ strC.charAt(5) sebenarnya bisa juga diakses dengan strC[5]
console.log(strC.charCodeAt(0));        // Output: 66       ⇨ Menampilkan kode unicode dari sebuah karakter di String (B = 66)
console.log(strC.codePointAt(0));       // Output: 66       ⇨ codePointAt (ES6) merupakan "Versi Update" dari charCodeAt
console.log(strC.substr(2));            // Output: ndung    ⇨ Ambil String dari indeks ke 2 (depan) s.d. akhir
console.log(strC.substr(-2));           // Output: ng       ⤷ Ambil String dari indeks ke 2 (belakang) s.d. akhir
console.log(strC.substr(2, 4));         // Output: ndun     ⤷ Ambil String dari indeks ke 2 (depan) sebanyak 4 karakter
console.log(strC.substr(-4, 3));        // Output: dun      ⤷ Ambil String dari indeks ke 4 (belakang) sebanyak 3 karakter
console.log(strC.substring(2));         // Output: ndung    ⇨ Ambil String dari indeks ke 2 (depan) s.d. akhir
console.log(strC.substring(2, 4));      // Output: nd       ⤷ Ambil String dari indeks ke 2 (depan) s.d indeks ke 4 (depan)
console.log(strC.substring(-4, 6));     // Output: Bandun   ⤷ Ambil String dari indeks ke 0 s.d indeks ke 6 (negatif jadi 0)
console.log(strC.substring(4, 0));      // Output: Band     ⤷ Ambil 4 karakter pertama dari String (indeks ke 0 s.d. ke 4)
console.log(strC.slice(2));             // Output: ndung    ⇨ Ambil String dari indeks ke 2 (depan) s.d. akhir
console.log(strC.slice(2, 4));          // Output: nd       ⤷ Ambil String dari indeks ke 2 (depan) s.d indeks ke 4 (depan)
console.log(strC.slice(-4, 6));         // Output: dun      ⤷ Ambil String dari indeks ke 4 (belakang) s.d. indeks ke 6 (depan)
console.log(strC.slice(-4));            // Output: dung     ⤷ Ambil String dari indeks ke 4 (belakang) s.d. akhir
                                        // Note: Object instance method substr(), substring() & slice() sangat mirip satu 
                                        // sama lain, perbedaannya hanya pada prilaku argument kedua masing-masing method

console.log(strD.split());              // Output: ["Bandung kota kembang"]         ⇨ split() dipakai untuk memecah sebuah String
console.log(strD.split(""));            // Output: ["B", "a", "n", "d" ...]            menjadi sebuah Array, argument pertama diisi
console.log(strD.split("", 1));         // Output: ["B"]                               karakter "pembatas" yang digunakan untuk
console.log(strD.split(" "));           // Output: ["Bandung", "kota", "kembang"]      memecah String (atau bisa juga diisi dengan 
console.log(strD.split(" ", 2));        // Output: ["Bandung", "kota"]                 RegExp, dibahas di point D), sedangkan 
console.log(strE.split(", "));          // Output: ["Satu", "dua", "tiga", "empat"]    argument kedua (optional), diisi dengan 
console.log(strE.split(", ", 3));       // Output: ["Satu", "dua", "tiga"]             jumlah element Array yang ingin diambil.
console.log(strF.split(/\W/));          // Output: ["Satu", "dua", "tiga", "empat"]  ⤷ /\W/ merupakan contoh pemakaian RegExp
console.log(strF.split(/\W/, 3));       // Output: ["Satu", "dua", "tiga"]            
console.log(strG.trim());               // Output: username       ⇨ Hapus karakter whitespace (tab, dll) di awal & akhir String
console.log(strC.concat(" Juara"));     // Output: Bandung Juara  ⇨ Menyambung String (Update: diganti menjadi operator concat +) 
console.log(strD.includes("kota"));     // Output: true           ⇨ Check apakah String "kota" ada di dalam String strD
console.log(strD.includes("kota", 9));  // Output: false          ⤷ Argument ke 2: 9 menjadi indeks dimana pencarian dimulai
console.log(strE.startsWith("Satu"));   // Output: true           ⇨ Check apakah String strE diawali dengan String "Satu"
console.log(strE.startsWith("dua", 6)); // Output: true           ⤷ Argument ke 2: 6 menjadi indeks awal String
console.log(strE.endsWith("empat"));    // Output: true           ⇨ Check apakah String strE diakhiri dengan String "empat"
console.log(strE.endsWith("dua", 9));   // Output: true           ⤷ Argument ke 2: 9 menjadi indeks akhir String
console.log(strC.repeat(2));            // Output: BandungBandung ⇨ Mengulang String sebanyak jumlah yang diinput di argument
console.log(numB.toString());           // Output: 50 (String)    ⇨ Konversi menjadi tipe data String (primitif)
console.log(strD.indexOf("kota"));      // Output: 8              ⇨ Serupa dengan includes(), namun outputnya berupa posisi indeks
console.log(strD.indexOf("city"));      // Output: -1             ⤷ Jika Output = -1, artinya String yang dicari tidak ditemukan
console.log(strD.indexOf("kota", 9));   // Output: -1             ⤷ Argument ke 2: 9 menjadi indeks dimana pencarian dimulai
console.log(strD.lastIndexOf("kota"));  // Output: 8              ⇨ Serupa dengan indexOf(), namun pencarian dimulai dari akhir
console.log(strD.lastIndexOf("ota", 9));// Output: 9              ⤷ 9 menjadi indeks dimana pencarian dimulai (gerak dari 9 ke 0)
console.log(strD.search(/KOTA/i));      // Output: 8              ⇨ Serupa dengan indexOf(), namun argument diisi dengan RegExp
console.log(strD.match(/\w*o\w*/g));    // Output: ["kota"]       ⇨ Serupa dengan search(), namun Output berupa Array
console.log(strD.match(/\w*z\w*/g));    // Output: null           ⤷ Jika Output = null, artinya tidak ada pola tersebut di String
console.log(strD.replace("kota", "X")); // Output: Bandung X kembang      ⇨ Mengganti String dengan String lain (di argument)
console.log(strD.replace(/a/g, "o"));   // Output: Bondung koto kembong   ⤷ Argument ke 1: bisa diisi juga dengan RegExp

let strH = "Nama saya Budi Setiawan";   // Studi kasus: menghitung berapa kali String "a" muncul di dalam String strH
let count = 0;                          // Dengan memanfaatkan Object instance method indexOf() dan perulangan while
let posisi = strH.indexOf("a");
while (posisi !== -1){                  // Perulangan berhenti saat posisi = -1 (Artinya String "a" tidak ditemukan lagi)
  count++;                              // count menghitung berapa kali perulangan berjalan = jumlah String "a" muncul
  posisi = strH.indexOf("a", posisi+1); // Perintah di baris ini berarti terus mencari posisi berikutnya dari String "a"
}
console.log(count);                     // Output: 6
```
<hr>

```Javascript
// =====================================
// D. Regular Expression (RegExp) Object
// =====================================

// D1. Object instance method

let regA = "Belajar JavaScript dari buku JavaScript Uncover";
let polaA = /JavaScript/;

console.log(polaA.test(regA));          // Output: true           ⇨ Check apakah pola /JavaScript/ terdapat di dalam String regA
console.log(/buku/.test(regA));         // Output: true           ⤷ Penulisan bisa langsung, tanpa disimpan ke dalam Let, hal ini
console.log(/Buku/.test(regA));         // Output: false          ⤷ berlaku juga untuk semua Object instance property & method 🔔
console.log(/Buku/i.test(regA));        // Output: true           ⤷ i artinya mengabaikan Case Sensitive (selebihnya di point D2)

// D2. Pola Regular Expression (RegExp)

// ➊ Pola RegExp sebagai String

let regB = "Belajar JavaScript";
let regC = "Satu Dua Tiga Empat";

console.log(/JavaScript/.test(regB));   // Output: true
console.log(/Javascript/.test(regB));   // Output: false
console.log(/Belajar/.test(regB));      // Output: true
console.log(/ajar/.test(regB));         // Output: true

// ➋ RegExp Flag (Penanda)

console.log(/jAvASCriPt/.test(regB));   // Output: false                ⇨ Flag i (ignore case) untuk mengabaikan Case Sensitive
console.log(/jAvASCriPt/i.test(regB));  // Output: true                    atau disebut juga sebagai Case Insensitive.
console.log(regB.replace(/a/, "o"));    // Output: Belojar JavaScript   ⇨ Flag g (global match) untuk mencari seluruh String yang
console.log(regB.replace(/a/g, "o"));   // Output: Belojor JovoScript      cocok dengan pola, hanya bisa dipakai di method yang
console.log(regB.replace(/a/g, "u"));   // Output: Belujur JuvuScript      mendukung banyak pencarian sekaligus, seperti replace(),
console.log(regC.match(/\w*u\w*/g));    // Output: ["Satu", "Dua"]         match() & exec(). Jika flag g tidak ditambahkan, RegExp
console.log(regC.match(/\w*o\w*/g));    // Output: null                    akan langsung berhenti di pola pertama.

                                        // Note: terdapat beberapa flag lainnya seperti m (multiline), u (unicode), s (dot all) &
                                        // d (has indices), namun tidak banyak digunakan. Selebihnya lihat dokumentasi di MDN.

// ➌ Pola Awal & Akhir

console.log(/^Belajar/.test(regB));     // Output: true                     ⇨ ^ sebagai karakter penanda awal pola          
console.log(/^Bel/.test(regB));         // Output: true       
console.log(regB.replace(/^/, "GO! ")); // Output: GO! Belojar JavaScript
console.log(/Script$/.test(regB));      // Output: true                     ⇨ $ sebagai karakter penanda akhir pola
console.log(/ipt$/.test(regB));         // Output: true
console.log(regB.replace(/$/, " GO!")); // Output: Belajar JavaScript GO!

// ➍ Pola Wildcard

                                        // Wildcard, pola yang bisa diganti dengan karakter apa saja (bebas), ditulis dengan titik:
let polaB = /.b../;                     // ⤷ Artinya: [minimal 1 karakter bebas] + [huruf b] + [minimal 2 karakter bebas]
let polaC = /^.b..$/;                   // ⤷ Artinya: [tepat 1 karakter apa saja] + [huruf b] + [tepat 2 karakter]
                                        // ⤷ ^ diawal dan $ diakhir, artinya tidak boleh ada karakter lain sebelum & sesudah String

console.log(polaB.test("abaa"));        // Output: true     ⇨ Test pola /.b../ di dalam String "abaa"
console.log(polaB.test("1b11"));        // Output: true
console.log(polaB.test(" b  "));        // Output: true
console.log(polaB.test("aaabaaaa"));    // Output: true
console.log(polaB.test("aba"));         // Output: false
console.log(polaB.test("acaa"));        // Output: false

console.log(polaC.test("abaa"));        // Output: true     ⇨ Test pola /^.b..$/ di dalam String "abaa"
console.log(polaC.test("1b11"));        // Output: true
console.log(polaC.test(" b  "));        // Output: true
console.log(polaC.test("aaabaaaa"));    // Output: false
console.log(polaC.test("aba"));         // Output: false
console.log(polaC.test("acaa"));        // Output: false

// ➎ Pola Character Set

                                        // Character Set, membuat syarat bahwa hanya karakter tertentu saja yang boleh ditulis:
let polaD = /[abcde]/;                  // ⤷ Artinya: [minimal terdapat 1 karakter diantara huruf a-e]
let polaE = /[a-e]/;                    // ⤷ [a-e] merupakan alternatif penulisan dari [abcde] (✔️ Recommended)
let polaF = /^[a-e]$/;                  // ⤷ Artinya: [tepat terdapat 1 karakter diantara huruf a-e]
let polaG = /^[a-e][1-9]../;            // ⤷ Artinya: [tepat 1 karakter a-e] + [min 1 karakter 1-9] + [min 2 karakter bebas]
let polaH = /[a-e][1-9]..$/;            // ⤷ Artinya: [min 1 karakter a-e] + [tepat 1 karakter 1-9] + [tepat 2 karakter bebas]
let polaI = /^[a-e][1-9]..$/;           // ⤷ Artinya: [tepat 1 karakter a-e] + [tepat 1 karakter 1-9] + [tepat 2 karakter bebas]

console.log(polaE.test("a"));           // Output: true     ⇨ Test pola /[a-e]/ di dalam String "a"
console.log(polaE.test("f"));           // Output: false
console.log(polaE.test("af"));          // Output: true
console.log(polaE.test("fa"));          // Output: true
console.log(polaE.test("  e  "));       // Output: true
console.log(polaE.test("  g  "));       // Output: false

console.log(polaF.test("a"));           // Output: true     ⇨ Test pola /^[a-e]$/ di dalam String "a"
console.log(polaF.test("f"));           // Output: false
console.log(polaF.test("af"));          // Output: false
console.log(polaF.test("fa"));          // Output: false
console.log(polaF.test("  e  "));       // Output: false
console.log(polaF.test("  g  "));       // Output: false

console.log(polaG.test("a1bc"));        // Output: true     ⇨ Test pola /^[a-e][1-9]../ di dalam String "a1bc"
console.log(polaG.test("a197bcxyz"));   // Output: true
console.log(polaG.test("a1    "));      // Output: true
console.log(polaG.test("e123  "));      // Output: true
console.log(polaG.test("f1    "));      // Output: false
console.log(polaG.test("ae1   "));      // Output: false

console.log(polaH.test("a1bc"));        // Output: true     ⇨ Test pola /[a-e][1-9]..$/ di dalam String "a1bc"
console.log(polaH.test("a1bcd"));       // Output: false
console.log(polaH.test("aa1bc"));       // Output: true
console.log(polaH.test("a1  "));        // Output: true
console.log(polaH.test("a1   "));       // Output: false
console.log(polaH.test("abcde1  "));    // Output: true

console.log(polaI.test("a1bc"));        // Output: true     ⇨ Test pola /^[a-e][1-9]..$/ di dalam String "a1bc"
console.log(polaI.test("aa1bc"));       // Output: false
console.log(polaI.test("a12bc"));       // Output: false
console.log(polaI.test("a1bcd"));       // Output: false
console.log(polaI.test("a1  "));        // Output: true
console.log(polaI.test("a1   "));       // Output: false

// ➏ Pola Negasi Character Set

                                        // Negasi Character Set, artinya pola "selain" di character set, simak contoh berikut:
let polaJ = /^[a-e]$/;                  // ⤷ Artinya: [tepat 1 karakter a-e]
let polaK = /^[^a-e]$/;                 // ⤷ Artinya: [tepat 1 karakter selain a-e] (^ di dalam character set menandakan negasi)
let polaL = /^[^a-e].[^1-9]b..$/;       // ⤷ Artinya: [tepat 1 karakter selain a-e] + [tepat 1 karakter bebas] + [tepat 1
                                        //            karakter selain 1-9] + [huruf b] + [tepat 2 karakter bebas]

console.log(polaK.test("a"));           // Output: false    ⇨ Test pola /^[^a-e]$/ di dalam String "a"
console.log(polaK.test("f"));           // Output: true
console.log(polaK.test("z"));           // Output: true
console.log(polaK.test("zz"));          // Output: false

console.log(polaL.test("f$xb--"));      // Output: true     ⇨ Test pola /^[^a-e].[^1-9]b..$/ di dalam String "f$xb--"
console.log(polaL.test("xyzb00"));      // Output: true
console.log(polaL.test("zzzb  "));      // Output: true
console.log(polaL.test("zz1b  "));      // Output: false

// ➐ Membatasi Jumlah Karakter

                                        // Karakter yang digunakan untuk membuat pola batas jumlah karakter yaitu kurung kurawal:
let polaM = /A{2}1{3}/;                 // ⤷ Artinya: [min 2 huruf A] + [min 3 angka 1]
let polaN = /^A{2}1{3}$/;               // ⤷ Artinya: [tepat 2 huruf A] + [tepat 3 angka 1]
let polaO = /^A{2}1{2,4}$/;             // ⤷ Artinya: [tepat 2 huruf A] + [min 2 & max 4 angka 1]
let polaP = /^A{2}1{2,}$/;              // ⤷ Artinya: [tepat 2 huruf A] + [min 2 & max ∞ angka 1] (∞ artinya tak terbatas)
let polaQ = /^[A-Z0-9]{2,}z{2}_$/;      // ⤷ Artinya: [min 2 huruf A-Z/angka 1-9] + [tepat 2 huruf z] + [karakter underscore: _]

console.log(polaM.test("AA111"));       // Output: true     ⇨ Test pola /A{2}1{3}/ di dalam String "AA111"
console.log(polaM.test("xyzAA111xyz")); // Output: true
console.log(polaM.test("  AA111  "));   // Output: true
console.log(polaM.test("BA111"));       // Output: false

console.log(polaN.test("AA111"));       // Output: true     ⇨ Test pola /^A{2}1{3}$/ di dalam String "AA111"
console.log(polaN.test("xyzAA111xyz")); // Output: false
console.log(polaN.test("  AA111  "));   // Output: false
console.log(polaN.test("BA111"));       // Output: false

console.log(polaO.test("AA11"));        // ouput: true      ⇨ Test pola /^A{2}1{2,4}$/ di dalam String "AA11"
console.log(polaO.test("AA1111"));      // ouput: true
console.log(polaO.test("AA11111"));     // ouput: false
console.log(polaO.test("A1111"));       // ouput: false

console.log(polaP.test("AA11"));        // ouput: true      ⇨ Test pola /^A{2}1{2,}$/ di dalam String "AA11"
console.log(polaP.test("AA1111"));      // ouput: true
console.log(polaP.test("AA11111111"));  // ouput: true
console.log(polaP.test("AA11111111x")); // ouput: false

console.log(polaQ.test("AAzz_"));       // Output: true     ⇨ Test pola /^[A-Z0-9]{2,}z{2}_$/ di dalam String "AAzz_"
console.log(polaQ.test("11zz_"));       // Output: true
console.log(polaQ.test("A1zz_"));       // Output: true
console.log(polaQ.test("1A2B3C4Dzz_")); // Output: true

// ➑ Karakter Pembatas Pola

                                        // RegExp menyediakan beberapa karakter khusus untuk membatasi pola, yaitu:
let polaR = /ab*c/;                     // * sama dengan {0,} maka b* di samping = b{0,}    (Artinya 0 atau lebih huruf b)
let polaS = /ab+c/;                     // + sama dengan {1,} maka b+ di samping = b{1,}    (Artinya 1 atau lebih huruf b)
let polaT = /ab?c/;                     // ? sama dengan {0,1} maka b? di samping = b{0,1}  (Artinya 0 atau 1 huruf b)

console.log(polaR.test("abc"));         // Output: true     ⇨ Test pola /ab*c/ di dalam String "abc"
console.log(polaR.test("abbbbbc"));     // Output: true
console.log(polaR.test("ac"));          // Output: true
console.log(polaR.test("aaaab"));       // Output: false

console.log(polaS.test("abc"));         // Output: true     ⇨ Test pola /ab+c/ di dalam String "abc"
console.log(polaS.test("abbbbbc"));     // Output: true
console.log(polaS.test("ac"));          // Output: false
console.log(polaS.test("aaaab"));       // Output: false

console.log(polaT.test("abc"));         // Output: true     ⇨ Test pola /ab?c/ di dalam String "abc"
console.log(polaT.test("abbbbbc"));     // Output: false
console.log(polaT.test("ac"));          // Output: true
console.log(polaT.test("aaaab"));       // Output: false

// ➒ Pola Karakter Khusus

                                        // RegExp menyediakan beberapa karakter khusus untuk mewakiki pola tertentu, yaitu:
let polaU01 = /\d/;                     // \d sama dengan [0-9]           Artinya seluruh digit angka
let polaU02 = /\D/;                     // \D sama dengan [^0-9]          Artinya seluruh digit selain angka
let polaU03 = /\w/;                     // \w sama dengan [A-Za-z0-9_]    Artinya seluruh huruf dan angka serta underscore
let polaU04 = /\W/;                     // \W sama dengan [^A-Za-z0-9_]   Artinya seluruh karakter selain huruf/angka/underscore
let polaU05 = /\s/;                     // \s sama dengan whitespace                      (Spasi, tab, linefeed, form-feed, dll)
let polaU06 = /\S/;                     // \S sama dengan satu karakter selain whitespace
let polaU07 = /\t/;                     // \t sama dengan satu karakter tab               (Horizontal tab)
let polaU08 = /\r/;                     // \r sama dengan satu karakter enter             (Carriage return)
let polaU09 = /\n/;                     // \n sama dengan satu karakter new line          (Linefeed)
let polaU10 = /\v/;                     // \v sama dengan satu karakter tab vertikal      (Vertical tab)
let polaU11 = /\f/;                     // \f sama dengan satu karakter form-feed
let polaU12 = /\./;                     // Backslash "\" digunakan sebagai karakter escape, fungsinya untuk mencegah sebuah karak-
let polaU13 = /\//;                     // ⤷ ter dianggap sebagai karakter khusus, misalnya membuat karakter titik & garis miring,
                                        // ⤷ kita tidak bisa langsung menulis titik begitu saja (karena akan dianggap wildcard)
                                        // ⤷ atau menulis langsung garis miring begitu saja (karena akan dianggap comment), oleh
                                        // ⤷ karena itu untuk menulis titik atau garis miring di dalam RegExp perlu diawali "\"

let polaV = /^\d\w\s$/;                 // Pola di samping sama dengan /^[0-9][A-Za-z0-9_][whitespace]$/
let polaW = /^www\.....\.com$/;         // Artinya: [wwww.] + [4 karakter bebas] + [.com] (\. bukan wildcard ya!)
let polaX = /^.+@.+\..+$/;              // Pola di samping sama dengan /^.{1,}@.{1,}\..{1,}$/ artinya [1/lebih karakter bebas] +
                                        // ⤷ [@] + [1/lebih karakter bebas] + [.] + [1/lebih karakter bebas] (pola untuk email)

console.log(polaV.test("1a "));                       // Output: true     ⇨ Test pola /^\d\w\s$/ di dalam String "1a "
console.log(polaV.test("19 "));                       // Output: true
console.log(polaV.test("1_ "));                       // Output: true
console.log(polaV.test("1a"));                        // Output: false

console.log(polaW.test("www.abcd.com"));              // Output: true     ⇨ Test pola /^www\.....\.com$/ di dalam "www.abcd.com"
console.log(polaW.test("www.xyz1.com"));              // Output: true
console.log(polaW.test("www.123 .com"));              // Output: true
console.log(polaW.test("www.google.com"));            // Output: false    False karena terdapat 5 karakter bebas, harusnya tepat 4

console.log(polaX.test("aku@gmail.com"));             // Output: true     ⇨ Test pola /^.+@.+\..+$/ di dalam "aku@gmail.com"
console.log(polaX.test("hehe@co.cocok"));             // Output: true
console.log(polaX.test("123@123.12"));                // Output: true
console.log(polaX.test(" @ . "));                     // Output: true
console.log(polaX.test("duniailkom@gmail.com"));      // Output: true
console.log(polaX.test("raihanralam@gmail.com"));     // Output: true

/* 
polaX tujuannya untuk pola penulisan email, namun tidak sempurna, lihat " @ . " dianggap true (ya karena memang lolos dari polaX),
oleh karena itu untuk kebutuhan pengecheck-an pola email yang lebih tepat & akurat dapat gunakan pola RegExp di link berikut:
📚 http://emailregex.com/ (pola RegExp yang disusun sangat kompleks, itu tidak lain untuk ketepatan pola email yang akurat)
*/

// ➓ Pola Logika OR

                                        // RegExp menyediakan karakter khusus untuk membuat kondisi OR yaitu karakter pipe "|":
let polaY = /aku|dia|kami/;             // ⤷ true jika terdapat setidaknya 1 kata dari 3 kemungkinan di samping (aku/dia/kami)

console.log(polaY.test("aku disini"));                // Output: true
console.log(polaY.test("dia disana"));                // Output: true
console.log(polaY.test("akuu dan diaa di Bali"));     // Output: true
console.log(polaY.test("kami belajar JavaScript"));   // Output: true
console.log(polaY.test("Budi belajar JavaScript"));   // Output: false

// Bonus: Latihan RegExp

let polaZ = /^[A-Za-z]{1,2}\s*\d{1,4}\s*[A-Za-z]{1,3}$/;    // Artinya: [1/2 karakter A-Za-z] + [0/lebih whitespace] +
                                                            // ⤷ [min 1 & max 4 karakter 0-9] + [0/lebih whitespace] +
                                                            // ⤷ [min 1 & max 3 karakter A-Za-z], juga karena diawali ^ dan
                                                            // ⤷ diakhiri $, maka tidak boleh ada karakter sebelum/sesudah String
                                                            // ⤷ pola RegExp ini merupakan pola untuk memeriksa nomor polisi

console.log(polaZ.test("B 1 RI"));                    // Output: true
console.log(polaZ.test("B1RI"));                      // Output: true
console.log(polaZ.test("DA 9999 XYZ "));              // Output: false
console.log(polaZ.test("DA 9999 XYZ"));               // Output: true
console.log(polaZ.test("bk9he"));                     // Output: true
console.log(polaZ.test("zz 9YES"));                   // Output: true
console.log(polaZ.test("_zz9YES"));                   // Output: false
```
<hr>

```Javascript
// ===============
// E. Array Object
// ===============

// E1. Object method

console.log(Array.isArray([1, 2, 3]));                // Output: true     ⇨ Check apakah sebuah nilai/var bertipe data Array
console.log(Array.isArray(["satu", 2, null]));        // Output: true
console.log(Array.isArray([]));                       // Output: true

// E2. Object instance property

let arrA = ["a","b","c","d","e"];
let arrB = [[1,2],[3,4],[5,6]];
let arrC = [1,2,3,4,5];
let arrD = [1,2,3,4,5];

console.log(arrA.length);               // Output: 5        ⇨ Mengambil info jumlah element dari sebuah Array
console.log(arrB.length);               // Output: 3
console.log(arrB[0].length);            // Output: 2

arrC.length = 3;                        // Property length sebuah Array bisa dikurangi
console.log(arrC);                      // Output: [1,2,3]
console.log(arrC.length);               // Output: 3

arrD.length = 7;                        // Property length sebuah Array bisa ditambah
console.log(arrD);                      // Output: [1,2,3,4,5,<2 empty slots>]
console.log(arrD.length);               // Output: 7

let arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];  // Contoh ini sama seperti di BAB 8 (D3). Kondisi (n<arrSiswa.length)
for (let n=0; n<arrSiswa.length; n++){                      // ⤷ akan selalu di check nilainya dalam setiap perulangan, padahal
  console.log(arrSiswa[n]);                                 // ⤷ nilai arrSiswa.length tidak pernah berubah (tidak efisien).
}                                                           // Output: Andri, Joko, Sukma, Rina, Sari

let arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];  // Contoh ini merupakan versi perbaikan (lebih efisien) dari contoh
let panjangArr = arrSiswa.length;                           // ⤷ di atas, karena nilai arrSiswa.length tidak disimpan langsung di
for (let n=0; n<panjangArr; n++){                           // ⤷ kondisi, melainkan ditampung terlebih dahulu ke dalam sebuah Let.
  console.log(arrSiswa[n]);                                 // Output: Andri, Joko, Sukma, Rina, Sari
}                                                           

// E3. Object instance method

let arrE = ["a","b","c"];
let arrF = [1,2,3];
let arrG = ["a","b","c","d","e","f","g"];

console.log(arrE.reverse());            // Output: ["c","b","a"]          ⇨ Membalik urutan element Array
console.log(arrE);                      // Output: ["c","b","a"]          ⤷ Method reverse() bersifat Mutating ⚠️
console.log(arrE.concat(arrF));         // Output: ["c","b","a",1,2,3]    ⇨ Menggabungkan/menyambung Array
console.log(arrE.concat(arrF,4,5));     // Output: ["c","b","a",1,2,3,4,5]⤷ Argument bisa lebih dari satu
console.log(arrG.slice(3));             // Output: ["d","e","f","g"]      ⇨ Mengambil sebagian element Array
console.log(arrG.slice(3,5));           // Output: ["d","e"]              ⤷ Argument ke 1: index awal pengambilan
console.log(arrG.slice(-5));            // Output: ["c","d","e","f","g"]  ⤷ Argument ke 2: index akhir pengambilan
console.log(arrG.slice(-5,-2));         // Output: ["c","d","e"]          ⤷ (Tetapi tidak termasuk index akhir itu sendiri)

let arrH = [1,2,3,4,5,6];
let arrI = [1,2,3,4,5,6];
let arrJ = [1,2,3,4,5,6];
let arrK = [1,2,3,4,5,6];

console.log(arrH.splice(3));            // Output: [4,5,6]                ⇨ Menambah atau mengurangi element Array
console.log(arrH);                      // Output: [1,2,3]                ⤷ Method splice() bersifat Mutating ⚠️
console.log(arrI.splice(3,2));          // Output: [4,5]                  ⤷ Argument ke 1: index awal penambahan/pengurangan
console.log(arrI);                      // Output: [1,2,3,6]              ⤷ Argument ke 2: jumlah element yang akan dihapus, jika
console.log(arrJ.splice(3,2,"new"));    // Output: [4,5]                  ⤷ Diisi 0 (nol), artinya tidak ada element yang dihapus
console.log(arrJ);                      // Output: [1,2,3,"new",6]        ⤷ Argument ke 3 dan seterusnya: element Array baru yang
console.log(arrK.splice(3,0,97,98,99)); // Output: []                     ⤷ Ingin ditambahkan (ditambahkannya dimulai dari index
console.log(arrK);                      // Output: [1,2,3,97,98,99,4,5,6] ⤷ yang diinputkan di argument ke 1)

let arrL = ["a","b","c"];
let tempA, tempB;

console.log(arrL.join());               // Output: a,b,c                  ⇨ Menggabungkan element Array menjadi String
console.log(arrL.join("-"));            // Output: a-b-c                  ⤷ Argument diisi dengan karakter yang diinginkan sebagai
console.log(arrL.join(" "));            // Output: a b c                  ⤷ Pemisah antar element (Defaul pemisahnya ialah koma)
arrL.push("d","e","f");                 // push() untuk menambah element Array ke posisi terakhir (bisa lebih dari 1 argument)
console.log(arrL);                      // ⤷ Output: ["a","b","c","d","e","f"]
tempA = arrL.pop();                     // pop() untuk mengurangi element Array dari posisi terakhir (hanya 1 element saja)
console.log(tempA);                     // ⤷ Output: f
console.log(arrL);                      // ⤷ Output: ["a","b","c","d","e"]
arrL.unshift("x","y","z");              // unshift() untuk menambah element Array ke posisi awal (bisa lebih dari 1 argument)
console.log(arrL);                      // ⤷ Output: ["x","y","z","a","b","c","d","e"]
tempB = arrL.shift();                   // shift() untuk mengurangi element Array dari posisi awal (hanya 1 elemnt saja)
console.log(tempB);                     // ⤷ Output: x
console.log(arrL);                      // ⤷ Output: ["y","z","a","b","c","d","e"]
                                        // method push(), pop(), unshift() & shift() bersifat Mutating ⚠️

let arrM = ["a","b","c","d"];

console.log(arrM.toString());           // Output: a,b,c,d  ⇨ Konversi Array menjadi String (serupa dengan join())
console.log(arrM.toLocaleString());     // Output: a,b,c,d  ⇨ Konversi Array menjadi String + memakai format bahasa lokal
console.log(arrM.includes("a"));        // Output: true     ⇨ Check apakah sebuah nilai ada di dalam element Array
console.log(arrM.includes("a",1));      // Output: false    ⤷ Argument ke 2: 1 menjadi indeks dimana pencarian dimulai
console.log(arrM.includes("e"));        // Output: false
console.log(arrM.indexOf("a"));         // Output: 0        ⇨ Serupa dengan includes(), namun outputnya berupa posisi indeks
console.log(arrM.indexOf("a",1));       // Output: -1       ⤷ jika Output = -1, artinya nilai yang dicari tidak ditemukan
console.log(arrM.indexOf("e"));         // Output: -1


// E4. Object instance method (𝗱𝗲𝗻𝗴𝗮𝗻 𝗖𝗮𝗹𝗹𝗯𝗮𝗰𝗸)

/* 
Dari semua method bawaan JavaScript yang telah kita pelajari hingga saat ini, seluruh argument dari method tersebut berupa tipe
data primitif (String, Number, Array, dll). Sekarang, kita akan mulai membahas method yang argumentnya berupa Function (Callback).
*/

let arrN = ["a","b","c","d"];
let arrO = ["Budi","Joko","Putri"];

arrN.forEach(                                         // forEach() berfungsi menjalankan Function untuk setiap element Array
  function(element, index, array){                    // (mirip seperti perulangan for of, jalan sebanyak jumlah element di Array)
    console.log(`Index ke-${index} = ${element}`);    // ⤷ Argument ke 1: nilai element/value Array 
  }                                                   // ⤷ Argument ke 2: index element/key Array   (optional)
);                                                    // ⤷ Argument ke 3: isi seluruh Array         (optional)
                                                      // ⤷ Penulisan argument tidak harus element/index/arrray (bebas saja)
                                                      // ⤷ Peranan argument ke 3 tidak sepenting argument ke 1 & ke 2, oleh
                                                      // ⤷ karena itu contoh di samping tidak menyertakan console.log(array);

/*
Output:
Index ke-0 = a
Index ke-1 = b
Index ke-2 = c
Index ke-3 = d
*/

function tampil(elm, idx, arr){                       // Dalam contoh di atas, Function Callback secara langsung disimpan dalam
  console.log(`Index ke-${idx} = ${elm}`);            // argument, namun sebenarnya bisa pula dipisah menjadi Function tersendiri
}                                                     // (dipisahkan keluar), dengan demikian dapat dipakai oleh Array lainnya.
arrN.forEach(tampil);                                 // Simak cara penulisan & pemanggilan Callback-nya pada contoh di samping.
arrO.forEach(tampil);                                 // ⤷ Lihat, Function tampil() bisa dipakai oleh arrN & arrO

/* 
Output:
Index ke-0 = a
Index ke-1 = b
Index ke-2 = c
Index ke-3 = d
Index ke-0 = Budi
Index ke-1 = Joko
Index ke-2 = Putri
*/                                          

let arrP = [1,2,3,4,5];
let arrQ = [5,6,7,8,9];
let arrR = [4,9,16,25];
let arrS = [36,49,64,81];

function kaliDua(elm){ return elm*2; }                                 
function pangkatTiga(elm){ return elm**3; }
function akarKuadrat(elm){ return Math.sqrt(elm); }
function ganjilGenap(elm){ return elm%2 === 0 ? "genap" : "ganjil"; }

                                                      // map() serupa dengan forEach(), bedanya method map() mengembalikan sebuah
                                                      // Array baru (memakai keyword return). map() tidak mengubah Array asal.
console.log(arrP.map(kaliDua));                       // Output: [2,4,6,8,10]
console.log(arrQ.map(kaliDua));                       // Output: [10,12,14,16,18]
console.log(arrP.map(pangkatTiga));                   // Output: [1,8,27,64,125]
console.log(arrQ.map(pangkatTiga));                   // Output: [125,216,343,512,729]
console.log(arrR.map(akarKuadrat));                   // Output: [2,3,4,5]
console.log(arrS.map(akarKuadrat));                   // Output: [6,7,8,9]
console.log(arrR.map(ganjilGenap));                   // Output: ["genap","ganjil","genap","ganjil"]
console.log(arrS.map(ganjilGenap));                   // Output: ["genap","ganjil","genap","ganjil"]

function genapOnly(elm){                              // Jika genap return true, jika ganjil return false. Sebenarnya bisa juga
  return (elm%2 === 0);                               // ditulis dengan IF-ELSE, namun tidak efisien (baris kode-nya panjang).
}
function besarDari10(elm){                            // Jika lebih dari 10 return true, jika tidak, return false. Sama seperti
  return (elm>10);                                    // genapOnly(), sebenarnya bisa ditulis dengan IF-ELSE, tapi tidak efisien.
}
                                                      // filter() serupa dengan map(), bedanya hasil return berupa true/false.
                                                      // Jika true pertahankan element Array, jika false hapus element tersebut.
console.log(arrP.filter(genapOnly));                  // Output: [2,4]
console.log(arrQ.filter(genapOnly));                  // Output: [6,8]
console.log(arrR.filter(genapOnly));                  // Output: [4,16]
console.log(arrS.filter(genapOnly));                  // Output: [36,64]

                                                      // every() berfungsi memeriksa apakah seluruh element Array memenuhi syarat
                                                      // tertentu (syarat kita definisikan sendiri di dalam Function). Jika ya
                                                      // (seluruh element menghasilkan true), maka method every() akan me-return
                                                      // true. Namun jika tidak (ada salah satu saja element yang menghasilkan 
                                                      // false), maka method every () akan me-return false.
console.log(arrR.every(besarDari10));                 // Output: false  (karena terdapat nilai 4 & 9 yang memang kurang dari 10)
console.log(arrS.every(besarDari10));                 // Output: true   (karena semua element di arrS bernilai lebih besar dari 10)

                                                      // some() serupa dengan every(), bedanya syaratnya terbalik, yaitu method
                                                      // some() akan me-return true jika ada salah satu element saja yang meng-
                                                      // hasilkan true (memenuhi syarat yang telah didefinisikan).
console.log(arrQ.some(besarDari10));                  // Output: false  (karena semua element di arrQ bernilai lebih kecil dari 10)
console.log(arrR.some(besarDari10));                  // Output: true   (karena terdapat nilai 16 & 25 yang memang memenuhi syarat)

                                                      // find() & findIndex() digunakan untuk mencari suatu nilai di dalam Array
                                                      // berdasarkan syarat tertentu. Kedua method ini akan langsung berhenti dan
                                                      // me-return nilai yang ditemukan pertama kali. find() akan me-return nilai
                                                      // element Arrray tersebut, sedangkan findIndex() me-return index Array-nya.
console.log(arrR.find(besarDari10));                  // Output: 16
console.log(arrS.find(besarDari10));                  // Output: 36
console.log(arrQ.find(besarDari10));                  // Output: undefined
console.log(arrR.findIndex(besarDari10));             // Output: 2
console.log(arrQ.findIndex(besarDari10));             // Output: -1

function tambah(total, elm, idx, arr){
  return total + elm;
}
function pangkat2(total, elm, idx, arr){
  return total + Math.pow(elm, 2);
}
                                                      // reduce() & reduceRight() digunakan untuk memproses total seluruh element
                                                      // Array dan menghasilkan 1 nilai akhir. reduce() memproses dari awal Array,
                                                      // sedangkan reduceRight() memproses dari akhir element Array.
                                                      // ⤷ argument ke 1: Var/Let penampung nilai total
                                                      // ⤷ argument ke 2: nilai element/value Array
                                                      // ⤷ argument ke 3: index element/key Array       (optional)
                                                      // ⤷ argument ke 4: isi seluruh Array             (optional)
console.log(arrP.reduce(tambah));                     // Output: 15   (hasil dari 1+2+3+4+5)
console.log(arrP.reduce(tambah,10));                  // Output: 25   (hasil dari 10+1+2+3+4+5)
console.log(arrQ.reduce(pangkat2));                   // Output: 235  (hasil dari 5+6²+7²+8²+9²)
console.log(arrQ.reduce(pangkat2,0));                 // Output: 255  (hasil dari 0+5²+6²+7²+8²+9²)
console.log(arrP.reduceRight(tambah));                // Output: 15   (hasil dari 5+4+3+2+1)
console.log(arrP.reduceRight(tambah,10));             // Output: 25   (hasil dari 10+5+4+3+2+1)
console.log(arrQ.reduceRight(pangkat2));              // Output: 183  (hasil dari 9+8²+7²+6²+5²)
console.log(arrQ.reduceRight(pangkat2,0));            // Output: 255  (hasil dari 0+9²+8²+7²+6²+5²)

/*
Note: Argument ke 1 yang berisi Var/Let penampung nilai total pada awalnya akan langsung diisi oleh nilai dari element pertama di
Array (default). Perhatikan proses perhitungan pada baris console.log(arrQ.reduce(pangkat2)), element pertama arrQ yang bernilai 5
tidak ikut dipangkatkan 2, itu karena 5 langsung disimpan ke dalam Var/Let total. Untuk menghindari hal seperti ini, kita dapat
mengatur nilai awal untuk Var/Let total dengan cara menyisipkan argument tambahan setelah Callback. Perhatikan proses perhitungan
pada baris console.log(arrQ.reduce(pangkat2,0)), Var/Let total diisi oleh nilai 0 diawal, sesuai dengan argument tambahan yang
disisipkan setelah Callback, tidak lagi mengambil dari element pertama Array.
*/

let arrT = ["Zaki","Aldo","Erpan","Joko","Budi"];
let arrU = [3,5,2,8,1,31,22,44,33,11];

                                                      // sort() berfungsi mengurutkan element Array berdasarkan nomor urut Unicode
                                                      // ⤷ method sort() bersifat Mutating ⚠️
arrT.sort(); console.log(arrT);                       // Output: ["Aldo","Budi","Erpan","Joko","Zaki"]
arrU.sort(); console.log(arrU);                       // Output: [1,11,2,22,3,31,33,44,5,8]
                                                      // ⤷ Terjadi karena Number mula-mula akan dikonversi menjadi String, lalu
                                                      // ⤷ selanjutnya barulah diurutkan berdasarkan nomor urut Unicode-nya

let arrV = [3,5,2,8,1,31,22,44,33,11];

function bandingkan(a, b){                            // Function ini mempunyai logika sebagai berikut:
  return a-b;                                         // ⤷ Jika a < b, return angka negatif, artinya a diurutkan sebelum b.
}                                                     // ⤷ Jika a > b, return angka positif, artinya a diurutkan setelah b.
                                                      // ⤷ Jika a = b, return 0, artinya a dan b sama, urutan tidak berubah.

arrV.sort(bandingkan);                                // sort() yang menggunakan Callback sebagai pengatur urutan element Array
console.log(arrV);                                    // Output: [1,2,3,5,8,11,22,31,33,44]
```
<hr>

```Javascript
// ==============
// F. Date Object
// ==============

// F1. Membuat Date Object

// ➊ Tanpa argument

let datA = new Date();                                // Cara penulisan 1: Tanpa argument
console.log(datA);                                    // Output: Fri Jun 04 2021 17:42:22 GMT+0700 (GMT+07:00)
                                                      // ⤷ Menampilkan waktu saat kode console.log(datA) dieksekusi
                                                      // ⤷ Kode dieksekusi di Jawa Barat Indonesia (WIB), oleh karena itu muncul 
                                                      // ⤷ GMT+0700 yang artinya waktu di WIB lebih cepat 7 jam dari waktu GMT/UTC
                                                      // ⤷ (standard waktu internasional), berarti waktu di GMT yaitu 17:35:22.

// ➋ Dengan 7 argument

let datB = new Date(2021,05,04,17,42,22,125);         // Cara penulisan 2: Dengan 7 argument
                                                      // ⤷ Argument ke 1: tahun
                                                      // ⤷ Argument ke 2: bulan     (Indeks dimulai dari 0 = Januari, dst)
                                                      // ⤷ Argument ke 3: hari
                                                      // ⤷ Argument ke 4: jam
                                                      // ⤷ Argument ke 5: menit
                                                      // ⤷ Argument ke 6: detik
                                                      // ⤷ Argument ke 7: milidetik
                                                      // ⤷ Kita tidak harus menginput ke 7 argument ini sekaligus (optional),
                                                      // ⤷ namun jika menginput hanya argument ke 1 saja, secara otomatis JS
                                                      // ⤷ membacanya sebagai milidetik, bukan tahun, catat baik-baik ya.
console.log(datB);                                    // Output: Fri Jun 04 2021 17:42:22 GMT+0700 (GMT+07:00)
                                                      // ⤷ Menampilkan waktu sesuai dengan yang diinputkan di argument

// ➌ Dengan 1 argument dateString

let datC = new Date("04 Jun 2021 17:42:22");          // Cara penulisan 3: Dengan 1 argument dateString
                                                      // ⤷ dateString yaitu String yang berformat tanggal, nantinya String ini
                                                      // ⤷ akan dikonversi menjadi Date oleh JS. Contoh di samping merupakan salah
                                                      // ⤷ satu format penulisan saja, karena terdapat banyak format dateString
                                                      // ⤷ misalnya "06/04/2021 17:42:22" atau "June 04, 2021 17:42:22", dll.
console.log(datC);                                    // Output: Fri Jun 04 2021 17:42:22 GMT+0700 (GMT+07:00)
                                                      // ⤷ Menampilkan waktu sesuai dengan yang diinputkan di argument

// ➍ Dengan 1 argument milidetik

let datD = new Date(1622803342000);                   // Cara penulisan 4: Dengan 1 argument milidetik
                                                      // ⤷ Argument merupakan total milidetik sejak tanggal 1 Januari 1970 atau
                                                      // ⤷ yang disebut UNIX Epoch Time. Dalam contoh di samping 1622803342000
                                                      // ⤷ milidetik berarti ± 51 tahun 167 hari 10 jam 42 menit 22 detik
                                                      // ⤷ semenjak 1 Januari 1970, maka itu berarti ± 4 Juni 2021.
console.log(datD);                                    // Output: Fri Jun 04 2021 17:42:22 GMT+0700 (GMT+07:00)
                                                      // ⤷ Menampilkan waktu sesuai dengan yang diinputkan di argument

// F2. Object instance method

/*
GMT atau UTC merupakan standard waktu internasional. WIB merupakan waktu untuk daerah Jawa Barat, Indonesia (dimana konten ini
ditulis). GMT/UTC dengan WIB memiliki selisih waktu, dimana WIB lebih cepat 7 jam dibandingkan GMT/UTC. Misalnya:
Sabtu, 5 Juni 2021 pukul 07:55:30 WIB   ⇨ Sabtu, 5 Juni 2021 pukul 00:55:30 GMT   (Waktu di WIB dikurangi 7 jam, jadinya GMT/UTC)
Sabtu, 5 Juni 2021 pukul 03:30:00 WIB   ⇨ Sabtu, 4 Juni 2021 pukul 20:30:00 GMT   (Waktu di WIB dikurangi 7 jam, jadinya GMT/UTC)

Method Getter & Setter UTC yang akan dijelaskan di bawah menampilkan tanggal dan waktu dalam UTC (standard waktu internasional),
Method Getter & Setter Locale menampilkan tanggal dan waktu sesuai settingan di sistem lokal, dalam kasus ini WIB (Jawa Barat).
⤷ Dari mana JavaScript tahu sistem lokal memakai waktu WIB? Dari web browser, dimana web browser mengambilnya dari sistem operasi,
  yakni settingan tanggal dari Windows. Umumnya, tampilan seperti inilah yang akan dipakai di website nanti.

𝗡𝗼𝘁𝗲: 
- Method Getter UTC & Getter Locale pada contoh di bawah dieksekusi pada    : Sabtu, 5 Juni 2021, pukul 07:55:30 (di Jawa Barat)
- Method Setter UTC & Setter Locale pada contoh di bawah dibuat ke tanggal  : Sabtu, 5 Juni 2021, pukul 10:55:30
*/

// ➊ Getter UTC (Waktu UTC)

let datE = new Date();

console.log(datE.toISOString());        // Output: 2021-06-05T00:55:30.215Z       ⇨ Tanggal dalam format ISO 
console.log(datE.toJSON());             // Output: 2021-06-05T00:55:30.215Z       ⇨ Sama seperti toISOString()
console.log(datE.toUTCString());        // Output: Sat, 05 Jun 2021 00:55:30 GMT  ⇨ Tanggal dalam format UTC
console.log(datE.valueOf());            // Output: 1622854530215                  ⇨ Milidetik sejak 1 Januari 1970 hingga saat ini
console.log(datE.getTime());            // Output: 1622854530215                  ⇨ Milidetik sejak 1 Januari 1970 hingga saat ini

console.log(datE.getUTCFullYear());     // Output: 2021                           ⇨ Tahun UTC
console.log(datE.getUTCMonth());        // Output: 5                              ⇨ Bulan UTC     (Indeks dari 0, 5 artinya Juni)
console.log(datE.getUTCDate());         // Output: 5                              ⇨ Tanggal UTC
console.log(datE.getUTCDay());          // Output: 6                              ⇨ Hari UTC      (Indeks dari 0, 6 artinya Sabtu)
console.log(datE.getUTCHours());        // Output: 0                              ⇨ Jam UTC       (Hasil dari waktu di WIB-7 jam)
console.log(datE.getUTCMinutes());      // Output: 55                             ⇨ Menit UTC
console.log(datE.getUTCSeconds());      // Output: 30                             ⇨ Detik UTC
console.log(datE.getUTCMilliseconds()); // Output: 215                            ⇨ Milidetik UTC

// ➋ Getter Locale (Waktu Sistem Lokal)

console.log(datE.toDateString());       // Output: Sat Jun 05 2021                ⇨ Hari Bulan Tanggal Tahun
console.log(datE.toTimeString());       // Output: 07:55:30 GMT+0700 (GMT+07:00)  ⇨ Jam Menit Detik
console.log(datE.toLocaleDateString()); // Output: 6/5/2021                       ⇨ Serupa toDateString(), format = sistem lokal
console.log(datE.toLocaleTimeString()); // Output: 7:55:30 AM                     ⇨ Serupa toTimeString(), format = sistem lokal
console.log(datE.toLocaleString());     // Output: 6/5/2021, 7:55:30 AM           ⇨ toLocaleDateString() & toLocaleTimeString()
console.log(datE.toString());           // Output: Sat Jun 05 2021 07:55:30       ⇨ Tampilan default ketika Date "dipaksa" tampil
                                        //         GMT+0700 (GMT+07:00)           ⤷ Misalnya jika dibuat ke dalam jendela alert()

console.log(datE.getFullYear());        // Output: 2021                           ⇨ Tahun S.Lokal
console.log(datE.getMonth());           // Output: 5                              ⇨ Bulan S.Lokal (Indeks dari 0, 5 artinya Juni)
console.log(datE.getDate());            // Output: 5                              ⇨ Tanggal S.Lokal
console.log(datE.getDay());             // Output: 6                              ⇨ Hari S.Lokal  (Indeks dari 0, 6 artinya Sabtu)
console.log(datE.getHours());           // Output: 7                              ⇨ Jam S.Lokal
console.log(datE.getMinutes());         // Output: 55                             ⇨ Menit S.Lokal
console.log(datE.getSeconds());         // Output: 30                             ⇨ Detik S.Lokal
console.log(datE.getMilliseconds());    // Output: 215                            ⇨ Milidetik S.Lokal
console.log(datE.getTimezoneOffset());  // Output: -420                           ⇨ Selisih waktu antara UTC dengan waktu S.lokal
                                        //                                        ⤷ -420 milidetik = -7 jam = 7 jam selisih waktu

// ➌ Setter UTC (Waktu UTC)

let datF = new Date(0);       console.log(datF.toUTCString());    // Output: Thu, 01 Jan 1970 00:00:00 GMT  ⇨ UNIX Epoch
datF.setUTCFullYear(2021);    console.log(datF.toUTCString());    // Output: Fri, 01 Jan 2021 00:00:00 GMT  ⇨ Ubah tahun
datF.setUTCMonth(5);          console.log(datF.toUTCString());    // Output: Tue, 01 Jun 2021 00:00:00 GMT  ⇨ Ubah bulan
datF.setUTCDate(5);           console.log(datF.toUTCString());    // Output: Sat, 05 Jun 2021 00:00:00 GMT  ⇨ Ubah tanggal
datF.setUTCHours(10);         console.log(datF.toUTCString());    // Output: Sat, 05 Jun 2021 10:00:00 GMT  ⇨ Ubah jam
datF.setUTCMinutes(55);       console.log(datF.toUTCString());    // Output: Sat, 05 Jun 2021 10:55:00 GMT  ⇨ Ubah menit
datF.setUTCSeconds(30);       console.log(datF.toUTCString());    // Output: Sat, 05 Jun 2021 10:55:30 GMT  ⇨ Ubah detik
datF.setUTCMilliseconds(215); console.log(datF.toISOString());    // Output: 2021-06-05T10:55:30.215Z       ⇨ Ubah milidetik

// ➍ Setter Locale (Waktu Sistem Lokal)

let datG = new Date(0);       console.log(datG.toLocaleString()); // Output: 1/1/1970, 7:00:00 AM           ⇨ UNIX Epoch (+7 jam)
datG.setFullYear(2021);       console.log(datG.toLocaleString()); // Output: 1/1/2021, 7:00:00 AM           ⇨ Ubah tahun
datG.setMonth(5);             console.log(datG.toLocaleString()); // Output: 6/1/2021, 7:00:00 AM           ⇨ Ubah bulan
datG.setDate(5);              console.log(datG.toLocaleString()); // Output: 6/5/2021, 7:00:00 AM           ⇨ Ubah tanggal
datG.setHours(10);            console.log(datG.toLocaleString()); // Output: 6/5/2021, 10:00:00 AM          ⇨ Ubah jam
datG.setMinutes(55);          console.log(datG.toLocaleString()); // Output: 6/5/2021, 10:55:00 AM          ⇨ Ubah menit
datG.setSeconds(30);          console.log(datG.toLocaleString()); // Output: 6/5/2021, 10:55:30 AM          ⇨ Ubah detik
datG.setMilliseconds(125);    console.log(datG.toISOString());    // Output: 2021-06-05T03:55:30.125Z       ⇨ Ubah milidetik

// F3. Latihan Program

// ➊ Menampilkan Tanggal dengan Format Tertentu

let datH    = new Date();
let tahun   = datH.getFullYear();           // Dapatkan tahun     (Getter Locale)
let bulan   = datH.getMonth();              // Dapatkan bulan     (Getter Locale)
let tanggal = datH.getDate();               // Dapatkan tanggal   (Getter Locale)
let hari    = datH.getDay();                // Dapatkan hari      (Getter Locale)
let jam     = datH.getHours();              // Dapatkan jam       (Getter Locale)
let menit   = datH.getMinutes();            // Dapatkan menit     (Getter Locale)
let detik   = datH.getSeconds();            // Dapatkan detik     (Getter Locale)
let mdetik  = datH.getMilliseconds();       // Dapatkan milidetik (Getter Locale)

let namaHari;
let namaBulan;

switch (hari){                              // Memanfaatkan index hari untuk membuat
  case 0: namaHari = "Minggu";  break;      // nama hari dalam Bahasa Indonesia
  case 1: namaHari = "Senin";   break;
  case 2: namaHari = "Selasa";  break;
  case 3: namaHari = "Rabu";    break;
  case 4: namaHari = "Kamis";   break;
  case 5: namaHari = "Jumat";   break;
  case 6: namaHari = "Sabtu";   break;
}

switch (bulan){                             // Memanfaatkan index bulan untuk membuat
  case 0: namaBulan = "Januari";    break;  // nama bulan dalam Bahasa Indonesia
  case 1: namaBulan = "Februari";   break;
  case 2: namaBulan = "Maret";      break;
  case 3: namaBulan = "April";      break;
  case 4: namaBulan = "Mei";        break;
  case 5: namaBulan = "Juni";       break;
  case 6: namaBulan = "Juli";       break;
  case 7: namaBulan = "Agustus";    break;
  case 8: namaBulan = "September";  break;
  case 9: namaBulan = "Oktober";    break;
  case 10: namaBulan = "November";  break;
  case 11: namaBulan = "Desember";  break;
}

let hasil = `${namaHari}, ${tanggal} ${namaBulan} ${tahun} ${jam}:${menit}:${detik}`;
console.log(hasil);                         // Output: Sabtu, 5 Juni 2021 13:25:30 (Waktu dimana kode dieksekusi)
                                            // ⤷ Format seperti ini umum digunakan di Indonesia

// ➋ Menghitung Selisih Tanggal

                                            // Membuat Date Object dengan 1 argument dateString
let tglAwal   = new Date("06/05/2021");     // Let tglAwal diisi dengan 5 Juni 2021          Note: Perhatikan, urutan tanggal
let tglAkhir  = new Date("12/20/2021");     // Let tglAkhir diisi dengan 12 Desember 2021          dan bulan terbalik 🔔

let timeAwal  = tglAwal.getTime();          // Dapatkan total milidetik sejak 1 Januari 1970 hingga tglAwal (5 Juni 2021)
let timeAkhir = tglAkhir.getTime();         // Dapatkan total milidetik sejak 1 Januari 1970 hingga tglAkhir (12 Desember 2021)

let selisihTgl = timeAkhir-timeAwal;        // Menghitung selisih milidetek antara tglAwal dengan tglAkhir
console.log(Math.abs(selisihTgl));          // Output: 17107200000 (Dalam milidetik)
                                            // ⤷ Math.abs() digunakan untuk mendapatkan angka multak (jika negatif jadi positif)

let ms1Hari_coba     = 1000*60*60*24;               // Menghitung banyak milidetik dalam 1 hari
let selisihHari_coba = selisihTgl/ms1Hari_coba;     // Dapatkan selisih hari
console.log(`Selisih = ${selisihHari_coba} hari`);  // Output: Selisih = 198 hari

/*
Tantangan selanjutnya, bagaimana mengkonversi 198 hari ini menjadi sekian tahun, sekian bulan dan sekian hari?
Di bawah ini merupakan contoh algoritma (lebih ke ilustrasi menjawab persoalan) yang dapat diaplikasikan.

500 hari itu berapa tahun, berapa bulan dan berapa hari?
⤷ Pertama, bagi 500 dengan 365, 500/365 = 1.37. Artinya 500 hari sama dengan 1.37 tahun.
  Simpan angka 1 tahun, dan kita akan konversi kelebihan 0.37 tahun menjadi bulan dan hari.
⤷ Kedua, karena 500 hari terdiri dari 1 tahun lebih, sisa hari bisa didapat dengan rumus 500-(1*365) = 135.
  Dengan mengasumsikan 1 bulan = 30 hari, maka 135 hari sama dengan 135/30 = 4.5 bulan.
  Simpan angka 4 bulan, dan kita akan konversi kelebihan 0.5 bulan ini menjadi hari.
⤷ Ketiga, sisa hari didapat dari pengurangan jumlah tahun dan jumlah bulan.
  Ini bisa dicari dengan rumus 500-(1*365)-(4*30) = 15 hari.
⤷ Akhirnya didapat bahwa 500 hari = 1 tahun 4 bulan 15 hari.

Sekarang, bagaimana dengan 198 hari? Mari kita hitung.
⤷ Jumlah tahun  = 198/365 = 0.54            Artinya tidak cukup 1 tahun. Simpan 0.
⤷ Jumlah bulan  = 198-(0*365)/30 = 6.6      Artinya terdapat 6 bulan lebih. Simpan 6, dan kita akan cari berapa hari lebihnya.
⤷ Jumlah hari   = 198-(0*365)-(6*30) = 18   Akhirnya didapat bahwa 198 hari = 0 tahun 6 bulan 18 hari.

Di bawah ini merupakan implementasi algoritma untuk mencari selisih tanggal (berdasarkan ilustrasi di atas):
*/

let ms1Hari   = 1000*60*60*24;              // Menghitung banyak milidetik dalam 1 hari
let ms1Bulan  = 1000*60*60*24*30;           // Menghitung banyak milidetik dalam 1 bulan
let ms1Tahun  = 1000*60*60*24*365;          // Menghitung banyak milidetik dalam 1 tahun

let selisihTahun  = Math.floor(selisihTgl/ms1Tahun);                                                  // Dapatkan selisih tahun
let selisihBulan  = Math.floor((selisihTgl-(selisihTahun*ms1Tahun))/ms1Bulan);                        // Dapatkan selisih bulan
let selisihHari   = Math.floor((selisihTgl-(selisihTahun*ms1Tahun)-(selisihBulan*ms1Bulan))/ms1Hari); // Dapatkan selisih hari

let hasil = `${selisihTahun} Tahun ${selisihBulan} Bulan ${selisihHari} Hari`;
console.log(hasil);                         // Output: 0 Tahun 6 Bulan 18 Hari

/*
Note: Program menghitung selisih tanggal ini belum sempurna, karena tidak memperhitungkan aspek lainnya seperti tahun kabisat dan
perbedaan hari dalam tiap bulan. Untuk pemrosesan Date yang lebih advanced, pelajari library JavaScript seperti 𝗠𝗼𝗺𝗲𝗻𝘁𝗝𝗦.

Info: Algoritma di atas, serupa juga dengan algoritma "Membagi nilai rupiah". Misalnya jika inputan awal 257,500. Hasil kode
program berupa: 2 lembar uang 100.000, 1 lembar uang 50.000, 1 lembar uang 5000, 1 lembar uang 2000, 1 lembar uang 500. Untuk
mempertajam kemampuan problem solving & analysis, coba buat program "Membagi nilai rupiah" ini menggunakan JavaScript. Good Luck!
*/
```

<br>
<div id="bab13"></div>

# 13. Global Property dan Global Function <a href="#daftarisi">🡹</a>

<img src="images/BAB-13.png">

```Javascript

/*
Selain Object property, Object method, Object instance property & Object instance method yang telah dibahas di BAB sebelumnya,
JavaScript pun memiliki Global property & Global function yang tidak "melekat" ke object apapun, dan bisa diakses dari mana saja.

𝗡𝗼𝘁𝗲: 𝗝𝘂𝗺𝗹𝗮𝗵𝗻𝘆𝗮 𝘁𝗶𝗱𝗮𝗸 𝗯𝗮𝗻𝘆𝗮𝗸 & 𝘀𝗲𝗯𝗮𝗴𝗶𝗮𝗻 𝗯𝗲𝘀𝗮𝗿 𝘀𝘂𝗱𝗮𝗵 𝗸𝗶𝘁𝗮 𝗽𝗲𝗹𝗮𝗷𝗮𝗿𝗶.
*/

// ==================
// A. Global Property
// ==================

let boo = NaN;                          // Membuat tipe data NaN secara manual        ⇨ Sama dengan Number.NaN
let coo = Infinity;                     // Membuat tipe data Infinity secara manual   ⇨ Sama dengan Number.POSITIVE_INFINITY
let doo = -Infinity;                    // Membuat tipe data -Infinity secara manual  ⇨ Sama dengan Number.NEGATIVE_INFINITY
let foo = undefined;                    // Membuat tipe data undefined secara manual
let goo = null;                         // Membuat tipe data null secara manual

console.log(boo);                       // Output: NaN
console.log(coo);                       // Output: Infinity
console.log(doo);                       // Output: -Infinity
console.log(foo);                       // Output: undefined
console.log(goo);                       // Output: null
```
<hr>

```Javascript
// ==================
// B. Global Function
// ==================

// B1. Dibawah ini sudah kita dipelajari

console.log(isNaN(5/'a'));              // Output: true   ⇨ Sama dengan Number.isNaN(5/'a')
console.log(isFinite(1/0));             // Output: false  ⇨ Sama dengan Number.isFinite(1/0)
console.log(parseFloat("1.23"));        // Output: 1.23   ⇨ Sama dengan Number.parseFloat("1.23")
console.log(parseInt("1.23"));          // Output: 1      ⇨ Sama dengan Number.parseInt("1.23")

// B2. Function eval()

let hoo = "100+30";
let joo = "let bar = 500*3";
let koo = "alert('Hello World')";

console.log(hoo);                       // Output: 100+30                 (String)
console.log(joo);                       // Output: let bar = 500*3        (String)
console.log(koo);                       // Output: alert('Hello World')   (String)

console.log(eval(hoo));                 // Output: 130                            ⇨ eval() digunakan untuk memproses String men-
eval(joo); console.log(bar);            // Output: 1500                              jadi perintah JavaScript. Biasanya dipakai
eval(koo);                              // Output: Muncul Popup "Hello World"        pada saat penggunaan API & script dari luar.

// B3. Function encodeURI() & encodeURIComponent()

let loo = "http://www.duniailkom.com/Belajar #JavaScript";
let moo = encodeURI(loo);               // encodeURI() untuk Encode beberapa karakter khusus yang biasanya ada di URI (URL).
let noo = encodeURIComponent(loo);      // encodeURIComponent() sama saja, namun dengan Encode lebih banyak karakter.

console.log(moo);                       // Output: http://www.duniailkom.com/Belajar%20#JavaScript
console.log(noo);                       // Output: http%3A%2F%2Fwww.duniailkom.com%2FBelajar%20%23JavaScript

// B4. Function decodeURI() & decodeURIComponent()

                                        // decodeURI() & decodeURIComponent() merupakan kebalikan dari Encode, yaitu Decode.
console.log(decodeURI(moo));            // Output: http://www.duniailkom.com/Belajar #JavaScript
console.log(decodeURIComponent(noo));   // Output: http://www.duniailkom.com/Belajar #JavaScript
```

<br>
<div id="bab14"></div>

# 14. Document Object Model <a href="#daftarisi">🡹</a>

<img src="images/BAB-14-2.png">

1. **Materi tentang JavaScript sudah selesai!** Mulai dari sini JavaScript akan digunakan untuk merakit komponen DOM (pemrosesan DOM tidak harus selalu menggunakan JavaScript, hanya saja JavaScript memang sangat dominan dan nyaris tidak tersaingi). DOM Merupakan pemodelan dokumen HTML ke dalam bentuk Object. Artinya, setiap tag-tag HTML seperti ```<h1>```, ```<p>``` atau ```<form>``` dimodelkan menjadi sebuah Object. Sebagaimana layaknya object, tag-tag HTML ini nantinya memiliki property dan method yang bisa digunakan untuk mengatur tampilan. “Model” yang dipakai di dalam DOM adalah dengan “memetakan” seluruh object HTML layaknya sebuah **pohon (tree)**.
   
```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1>Belajar JavaScript</h1>
    <p>Sedang belajar <em>JavaScript</em> <b>dari Duniailkom</b></p>
  </body>
</html>
```

<img src="images/BAB-14-3.png">

2. **BOM (Browser Object Model)** adalah model dari seluruh Object yang ada di dalam web browser. Artinya BOM merupakan ruang lingkup yang lebih luas daripada DOM. BOM terdiri dari banyak Object di dalamnya, seperti Location Object, History Object, Navigator Object, Screen Object, dan tentu saja Document Object (DOM). Semua Object BOM ini berada langsung di bawah Window Object.

<img src="images/BAB-14-4.png">

3. **Window Object** berperan sebagai Global Object. Semua Var/Let, Function hingga Object di JavaScript "melekat" langsung ke Window Object. Ini berarti sebenarnya penulisan, misal ```console.log(Math.PI);``` itu sama saja dengan ```console.log(window.Math.PI);```. Namun, karena status Global Object-nya, penulisan ```window``` tidak diharuskan (web browser akan menambahkannya secara otomatis).

```Javascript
// =================
// A. Windows Object
// =================

// A1. Penulisan window itu optional

let foo = "Hello World";
function salam(a){
  console.log(`Hello ${a}`);
}

console.log(window.foo);                  // Output: Hello World                 ⇨ Sama dengan console.log(foo);
window.salam("Bandung");                  // Output: Hello Bandung               ⇨ Sama dengan salam("Bandung");
console.log(window.Math.PI);              // Output: 3.141592653589793           ⇨ Sama dengan console.log(Math.PI);
console.log(window.Number.isNaN(5/'a'));  // Output: true                        ⇨ Sama dengan console.log(Number.isNaN(5/'a'));

// A2. Window property

window.console.log(1+1);                  // Output: 2                            ≈ console.log(1+1);
window.console.info({nama:"A", umur:7});  // Output: {nama: "A", umur: 7}         ≈ console.info({nama:"A", umur:7});
window.console.table({nama:"A", umur:7}); // Output: Tabel (check sendiri)        ≈ console.table({nama:"A", umur:7});
window.console.dir({nama:"A", umur:7});   // Output: ▶Object                      ≈ console.dir({nama:"A", umur:7});

                                          // console merupakan salah satu property window. Memiliki beberapa method, diantaranya
                                          // log(), info(), table(), dir(). 📚 https://www.w3schools.com/jsref/obj_console.asp

console.log(window.location);             // Output: ▶Location  (Object)         ≈ console.log(location);
console.log(window.history);              // Output: ▶History   (Object)         ≈ console.log(history);
console.log(window.navigator);            // Output: ▶Navigator (Object)         ≈ console.log(navigator);
console.log(window.screen);               // Output: ▶Screen    (Object)         ≈ console.log(screen);
console.log(window.document);             // Output: ▶#document (Object)         ≈ console.log(document);

// A3. Window method

window.alert("Hello World!");             // Output: Muncul Popup "Hello World!"            ≈ alert("Hello World!");
window.prompt("Masukkan Nama!");          // Output: Muncul Popup Input "Masukkan Nama!"    ≈ prompt("Masukkan Nama!");
window.confirm("Anda Setuju?");           // Output: Muncul Popup Konfirmasi "Anda Setuju?" ≈ confirm("Anda Setuju?");
window.open();                            // Output: Muncul New Tab di Browser              ≈ open();
window.print();                           // Output: Muncul Menu Print di Browser           ≈ print();
window.getComputedStyle();                // Output: (Menampilkan seluruh Style CSS)

                                          // 📚 Referensi window property & method lainnya:
                                          // https://www.w3schools.com/jsref/obj_window.asp
                                          // https://developer.mozilla.org/en-US/docs/Web/API/Window
```
<hr>

```Javascript
// ===================================
// B. Window Object ➜ Document Object
// ===================================

// B1. Document property

console.log(window.document.URL);       // Output: http://127.0.0.1:5500/contoh.html  ⇨ URL lengkap dari dokumen HTML
console.log(window.document.baseURI);   // Output: http://127.0.0.1:5500/contoh.html  ⇨ Absolute base URI dari dokumen

                                        // Note: Dari sini hingga seterusnya penulisan window tidak akan disertakan 🔔
console.log(document.domain);           // Output: 127.0.0.1                          ⇨ Nama domain server yang memuat dokumen
console.log(document.lastModified);     // Output: 06/10/2021 00:22:21                ⇨ Tanggal & waktu dokumen terakhir diubah
console.log(document.title);            // Output: Belajar JS                         ⇨ Judul dari dokumen

// B2. Document method

document.write("Hello World");          // Menulis ekspresi/teks HTML atau kode JavaScript ke dokumen
document.writeln("Hello World");        // Sama seperti write() namun menambah baris baru untuk setiap statement
                                        // ⤷ Note: Biasanya banyak dipakai di tutorial-tutorial di Internet. Namun untuk
                                        //         proses debugging, console.log() lebih banyak (dan lebih disarankan)
                                        //         digunakan, karena menampilkan informasi yang lebih lengkap.
```
<hr>

```Javascript
// ==================================================
// C. Window Object ➜ Document Object ➜ Node Object
// ==================================================
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1>Belajar JavaScript</h1>
    <p>Sedang belajar <em>JavaScript</em> <b>dari Duniailkom</b></p>
    <script>
      // 𝗦𝗰𝗿𝗶𝗽𝘁 𝗱𝗶 𝗖𝟭 & 𝗖𝟮 𝘀𝗶𝗺𝗽𝗮𝗻 𝗱𝗶𝘀𝗶𝗻𝗶
    </script>
  </body>
</html>
```

```Javascript
// C1. Menelusuri struktur DOM (𝗖𝗮𝗿𝗮 𝟭: 𝗺𝗮𝗻𝘂𝗮𝗹/𝘀𝘂𝗹𝗶𝘁 🔔)

console.log(document.childNodes[0]);                                            // Output: <!𝗗𝗢𝗖𝗧𝗬𝗣𝗘 𝗵𝘁𝗺𝗹>
console.log(document.childNodes[1]);                                            // Output: <𝗵𝘁𝗺𝗹> ... </𝗵𝘁𝗺𝗹>
console.log(document.childNodes[1].childNodes[0]);                              // Output: <𝗵𝗲𝗮𝗱> ... </𝗵𝗲𝗮𝗱>
console.log(document.childNodes[1].childNodes[0].childNodes[0]);                // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[0].childNodes[1]);                // Output: <𝗺𝗲𝘁𝗮 𝗰𝗵𝗮𝗿𝘀𝗲𝘁="𝘂𝘁𝗳-𝟴">
console.log(document.childNodes[1].childNodes[0].childNodes[2]);                // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[0].childNodes[3]);                // Output: <𝘁𝗶𝘁𝗹𝗲>Belajar JavaScript</𝘁𝗶𝘁𝗹𝗲>
console.log(document.childNodes[1].childNodes[1]);                              // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[2]);                              // Output: <𝗯𝗼𝗱𝘆> ... </𝗯𝗼𝗱𝘆>
console.log(document.childNodes[1].childNodes[2].childNodes[0]);                // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[2].childNodes[1]);                // Output: <𝗵𝟭>Belajar JavaScript</𝗵𝟭>
console.log(document.childNodes[1].childNodes[2].childNodes[2]);                // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[2].childNodes[3]);                // Output: <𝗽> ... </𝗽>
console.log(document.childNodes[1].childNodes[2].childNodes[3].childNodes[0]);  // Output: "Sedang Belajar"
console.log(document.childNodes[1].childNodes[2].childNodes[3].childNodes[1]);  // Output: <𝗲𝗺>JavaScript</𝗲𝗺>
console.log(document.childNodes[1].childNodes[2].childNodes[3].childNodes[2]);  // Output: #𝘁𝗲𝘅𝘁  (Karakter Carriage Return)
console.log(document.childNodes[1].childNodes[2].childNodes[3].childNodes[3]);  // Output: <𝗯>dari Duniailkom</𝗯>

/*
Note: Karakter Carriage Return adalah karakter enter/baris baru. Karakter tersebut dianggap sebagai Text Node. Inilah salah satu
masalah yang 𝘀𝗲𝗿𝗶𝗻𝗴 𝗺𝗲𝗺𝗯𝘂𝗮𝘁 𝗽𝘂𝘀𝗶𝗻𝗴 jika menelusuri struktur DOM tree satu per satu secara manual. Solusinya? Lihat ...
*/

// C2. Node property

let bar = document.childNodes[1].childNodes[2].childNodes[3]; // Let bar berisi <𝗽> ... </𝗽>

console.log(bar.tagName);                           // Output: 𝗣
console.log(bar.nodeName);                          // Output: 𝗣
console.log(bar.nodeType);                          // Output: 𝟭 (📚 https://www.w3schools.com/jsref/prop_node_nodetype.asp)
console.log(bar.nodeValue);                         // Output: 𝗻𝘂𝗹𝗹 (Element Node selalu menghasilkan null, beda dengan Text Node)
console.log(bar.ownerDocument);                     // Output: ▶#𝗱𝗼𝗰𝘂𝗺𝗲𝗻𝘁 (Object)
console.log(bar.parentNode);                        // Output: <𝗯𝗼𝗱𝘆> ... </𝗯𝗼𝗱𝘆>
console.log(bar.parentElement);                     // Output: <𝗯𝗼𝗱𝘆> ... </𝗯𝗼𝗱𝘆> (Akan null jika parent bukan Element Node)
console.log(bar.childNodes);                        // Output: ▶𝗡𝗼𝗱𝗲𝗟𝗶𝘀𝘁(𝟰) [text, em, text, b]   ❌ Text Node ikut dihitung
console.log(bar.children);                          // Output: ▶𝗛𝗧𝗠𝗟𝗖𝗼𝗹𝗹𝗲𝗰𝘁𝗶𝗼𝗻(𝟮) [em, b]         ✔️ Text Node tidak dihitung
console.log(bar.childElementCount);                 // Output: 𝟮
console.log(bar.firstChild);                        // Output: "Sedang Belajar"             ❌ Bikin Pusing (dengan Text Node)
console.log(bar.lastChild);                         // Output: <𝗯>dari Duniailkom</𝗯>       ❌ Bikin Pusing (dengan Text Node)
console.log(bar.previousSibling);                   // Output: #𝘁𝗲𝘅𝘁                         ❌ Bikin Pusing (dengan Text Node)
console.log(bar.previousSibling.previousSibling);   // Output: <𝗵𝟭>Belajar JavaScript</𝗵𝟭>  ❌ Bikin Pusing (dengan Text Node)
console.log(bar.nextSibling);                       // Output: #𝘁𝗲𝘅𝘁                         ❌ Bikin Pusing (dengan Text Node)
console.log(bar.nextSibling.nextSibling);           // Output: <𝘀𝗰𝗿𝗶𝗽𝘁> ... </𝘀𝗰𝗿𝗶𝗽𝘁>          ❌ Bikin Pusing (dengan Text Node)
console.log(bar.firstElementChild);                 // Output: <𝗲𝗺>JavaScript</𝗲𝗺>         ✔️ Lebih Mudah (tanpa Text Node)
console.log(bar.lastElementChild);                  // Output: <𝗯>dari Duniailkom</𝗯>       ✔️ Lebih Mudah (tanpa Text Node)
console.log(bar.previousElementSibling);            // Output: <𝗵𝟭>Belajar JavaScript</𝗵𝟭>  ✔️ Lebih Mudah (tanpa Text Node)
console.log(bar.nextElementSibling);                // Output: <𝘀𝗰𝗿𝗶𝗽𝘁> ... </𝘀𝗰𝗿𝗶𝗽𝘁>          ✔️ Lebih Mudah (tanpa Text Node)

                                                    // Note:
                                                    // ⤷ 𝗡𝗼𝗱𝗲𝗟𝗶𝘀𝘁: Kumpulan Node (Element Node & Text Node). 
                                                    // ⤷ 𝗛𝗧𝗠𝗟𝗖𝗼𝗹𝗹𝗲𝗰𝘁𝗶𝗼𝗻: Kumpulan Node, tetapi khusus Element Node saja.
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1>Belajar JavaScript</h1>
    <p>Sedang belajar <em>JavaScript</em> <b>dari Duniailkom</b></p>
    <script>
      let nodeBody  = document.childNodes[1].childNodes[2];     // Berisi <𝗯𝗼𝗱𝘆> ... </𝗯𝗼𝗱𝘆>
      let nodeH1    = nodeBody.childNodes[1];                   // Berisi <𝗵𝟭>Belajar JavaScript</𝗵𝟭>
      let nodeP     = nodeBody.childNodes[3];                   // Berisi <𝗽> ... </𝗽>
      let nodeEm    = nodeP.childNodes[1];                      // Berisi <𝗲𝗺>JavaScript</𝗲𝗺>
      let nodeB     = nodeP.childNodes[3];                      // Berisi <𝗯>dari Duniailkom</𝗯>

      // 𝗦𝗰𝗿𝗶𝗽𝘁 𝗱𝗶 𝗖𝟯 𝘀𝗶𝗺𝗽𝗮𝗻 𝗱𝗶𝘀𝗶𝗻𝗶
    </script>
  </body>
</html>
```

```Javascript
// C3. Node method

let nodeP_new1    = document.createElement("p");              // createElement() untuk Membuat Element Node baru
let nodeP_new2    = document.createElement("h2");             // createTextNode() untuk Membuat Text Node baru
let nodeP_new3    = document.createElement("span");           // Note: Method createElement() & createTextNode() bukan
let nodeText_new1 = document.createTextNode("Text Baru 1");   //       milik Node Object, melainkan milik Document Object
let nodeText_new2 = document.createTextNode("Text Baru 2");   //       (lihat bagian B di atas). Selain itu, terdapat juga
let nodeText_new3 = document.createTextNode("Text Baru 3");   //       method createAttribute(), namun tidak dibahas disini.

nodeP_new1.appendChild(nodeText_new1);              // Hasilnya menjadi: <𝗽>Text Baru 1</𝗽>
nodeP_new2.appendChild(nodeText_new2);              // Hasilnya menjadi: <𝗵𝟮>Text Baru 2</𝗵𝟮>
nodeP_new3.appendChild(nodeText_new3);              // Hasilnya menjadi: <𝘀𝗽𝗮𝗻>Text Baru 3</𝘀𝗽𝗮𝗻>

nodeBody.appendChild(nodeP_new1);                   // Memasukkan <𝗽>Text Baru 1</𝗽> ke dalam <𝗯𝗼𝗱𝘆> (sebagai Node terakhir)
nodeBody.insertBefore(nodeP_new2, nodeH1);          // Memasukkan <𝗵𝟮>Text Baru 2</𝗵𝟮> sebelum <𝗵𝟭>Belajar JavaScript</𝗵𝟭>
nodeBody.replaceChild(nodeP_new3, nodeH1);          // Mengganti <𝗵𝟭>Belajar JavaScript</𝗵𝟭> menjadi <𝘀𝗽𝗮𝗻>Text Baru 3</𝘀𝗽𝗮𝗻>
let ambil = nodeP.removeChild(nodeB);               // Menghapus <𝗯>dari Duniailkom</𝗯> dari <𝗽> ... </𝗽> (disimpan di Let)
let klon1 = nodeP.cloneNode(true);                  // Copy nodeP dengan Childnya : <𝗽>Sedang belajar <𝗲𝗺>JavaScript</𝗲𝗺></𝗽>
let klon2 = nodeP.cloneNode(false);                 // Copy nodeP tanpa Childnya  : <𝗽></𝗽>
console.log(nodeP.contains(nodeEm));                // Output: true   ⇨ Check apakah nodeP memiliki Child nodeEm di dalamnya
console.log(klon1.hasChildNodes());                 // Output: true   ⇨ Check apakah klon1 memiliki Child (meskipun hanya 1)
console.log(klon2.hasChildNodes());                 // Output: false  ⇨ Hanya berisi <𝗽></𝗽> (artinya tidak punya Child)
```

```Javascript
// C4. Studi Kasus: Menambahkan Table ke Dalam DOM
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Belajar JavaScript</title>
    <style>
      table,
      tr,
      td {
        border-collapse: collapse;
        border: 1px solid black;
      }
    </style>
  </head>
  <body>
    <h1>Belajar JavaScript</h1>
    <p>Sedang belajar <em>JavaScript</em> <b>dari Duniailkom</b></p>
    <script>
      // 1. Siapkan Let shorcut untuk Node
      let nodeBody  = document.childNodes[1].childNodes[2];
      let nodeP     = nodeBody.childNodes[3];
  
      // 2. Buat tag <table> & siapkan beberapa Let untuk looping
      let nodeTable = document.createElement("table");
      let nodeTr, nodeTd1, nodeTd2, nomorUrut, nomorAcak, nomorAcakText;
  
      for (let i = 1; i <= 10; i++) {
        // 3. Buat 1 tag <tr>, 2 tag <td>, text node (nomor urut & acak)
        nodeTr        = document.createElement("tr");
        nodeTd1       = document.createElement("td");
        nodeTd2       = document.createElement("td");
        nomorUrut     = document.createTextNode(i);
        nomorAcak     = Math.floor(Math.random() * 90) + 10; // Rentang 10-99
        nomorAcakText = document.createTextNode(nomorAcak);
  
        // 4. Rangkai text node ➜ <td> ➜ <tr> ➜ <table>
        nodeTd1.appendChild(nomorUrut);
        nodeTd2.appendChild(nomorAcakText);
        nodeTr.appendChild(nodeTd1);
        nodeTr.appendChild(nodeTd2);
        nodeTable.appendChild(nodeTr);
      }
  
      // 5. Masukkan tag <table> kedalam DOM, posisi sebelum tag <p>
      nodeBody.insertBefore(nodeTable, nodeP);
    </script>
  </body>
</html>
```
<hr>

```Javascript
// ==============================================
// D. Window Object ➜ Document Object (Lanjutan)
// ==============================================
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1 id="judul">Belajar JavaScript</h1>
    <h2 class="kelas-a">JavaScript itu <b>menyenangkan</b></h2>
    <p class="kelas-a">Sedang belajar <em id="miring">JavaScript</em> <b>dari Duniailkom</b></p>
    <p><b>Duniailkom</b> menyajikan banyak materi Web Programming</p>
    <input type="text" name="isian" value="Isian 1">
    <input type="text" name="isian" value="Isian 2">
    <script>
      // 𝗦𝗰𝗿𝗶𝗽𝘁 𝗱𝗶 𝗯𝗮𝘄𝗮𝗵 𝘀𝗶𝗺𝗽𝗮𝗻 𝗱𝗶𝘀𝗶𝗻𝗶
    </script>
  </body>
</html>
```

```Javascript
// Menelusuri struktur DOM (𝗖𝗮𝗿𝗮 𝟮: 𝗺𝘂𝗱𝗮𝗵/𝗰𝗲𝗽𝗮𝘁 🔔)

let nodeEm    = document.getElementById("miring");            // Mencari Element Node berdasarkan nilai atribut id
let nodeClass = document.getElementsByClassName("kelas-a");   // Mencari Element Node berdasarkan class tertentu
let nodeTag   = document.getElementsByTagName("p");           // Mencari Element Node berdasarkan nama tag
let nodeName  = document.getElementsByName("isian");          // Mencari Element Node berdasarkan nilai atribut name
let nodeQS    = document.querySelector("p b");                // Mencari Element Node menggunakan 𝗦𝗲𝗹𝗲𝗰𝘁𝗼𝗿 𝗖𝗦𝗦
let nodeQSA   = document.querySelectorAll("p b");             // ⤷ querySelector() mengambil element yang ditemukan pertama saja
                                                              // ⤷ querySelectorAll() mengambil seluruh element yang ditemukan

                                                              // 📚 Referensi document property & method lainnya:
                                                              // https://www.w3schools.com/jsref/dom_obj_document.asp
                                                              // https://developer.mozilla.org/en-US/docs/Web/API/Document

console.log(nodeEm);                    // Output: <𝗲𝗺 id="miring">JavaScript</𝗲𝗺>
console.log(nodeClass);                 // Output: ▶𝗛𝗧𝗠𝗟𝗖𝗼𝗹𝗹𝗲𝗰𝘁𝗶𝗼𝗻(𝟮) [h2.kelas-a, p.kelas-a]
console.log(nodeClass[0]);              // Output: <𝗵𝟮 class="kelas-a"> ... </𝗵𝟮>
console.log(nodeClass[1]);              // Output: <𝗽 class="kelas-a"> ... </𝗽>
console.log(nodeTag);                   // Output: ▶𝗛𝗧𝗠𝗟𝗖𝗼𝗹𝗹𝗲𝗰𝘁𝗶𝗼𝗻(𝟮) [p.kelas-a, p]
console.log(nodeTag[0]);                // Output: <𝗽 class="kelas-a"> ... </𝗽>
console.log(nodeTag[1]);                // Output: <𝗽> ... </𝗽>
console.log(nodeName);                  // Output: ▶𝗡𝗼𝗱𝗲𝗟𝗶𝘀𝘁(𝟮) [input, input]
console.log(nodeName[0]);               // Output: <𝗶𝗻𝗽𝘂𝘁 type="text" name="isian" value="Isian 1">
console.log(nodeName[1]);               // Output: <𝗶𝗻𝗽𝘂𝘁 type="text" name="isian" value="Isian 2">
console.log(nodeQS);                    // Output: <𝗯>dari Duniailkom</𝗯>
console.log(nodeQSA);                   // Output: ▶𝗡𝗼𝗱𝗲𝗟𝗶𝘀𝘁(𝟮) [b, b]
console.log(nodeQSA[0]);                // Output: <𝗯>dari Duniailkom</𝗯>
console.log(nodeQSA[1]);                // Output: <𝗯>Duniailkom</𝗯>
```
<hr>

```Javascript
// =============================================================
// E. Window Object ➜ Document Object ➜ Node Object (Lanjutan)
// =============================================================
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
    <style>
      p:nth-child(3){
        text-decoration: underline;
      }
      .merah {
        color: red;
      }
      .hijau {
        color: green;
      }
      .tebal {
        font-weight: bold;
      }
    </style>
  </head>
  <body>
    <h1 id="judul">Belajar JavaScript</h1>
    <p>Sedang belajar <em>JavaScript</em> <b>dari Duniailkom</b></p>
    <p style="color: blue;">Mohon tidak mengganggu, terimakasih!</p>
    <div class="merah tebal">Materi pertama tentang Variable</div>
    <div class="merah">Materi kedua tentang Function</div>
    <script>
      // 𝗦𝗰𝗿𝗶𝗽𝘁 𝗱𝗶 𝗯𝗮𝘄𝗮𝗵 𝘀𝗶𝗺𝗽𝗮𝗻 𝗱𝗶𝘀𝗶𝗻𝗶
    </script>
  </body>
</html>
```

```Javascript

// E1. Memanipulasi tag HTML + konten isinya

let boo = document.querySelector("p");              // Let boo berisi <𝗽> ... </𝗽>
let coo = document.querySelector("title");          // Let coo berisi <𝘁𝗶𝘁𝗹𝗲>Belajar JavaScript</𝘁𝗶𝘁𝗹𝗲>

console.log(boo.textContent);                       // Output: Sedang Belajar JavaScript dari Duniailkom
console.log(boo.innerHTML);                         // Output: Sedang belajar <𝗲𝗺>JavaScript</𝗲𝗺> <𝗯>dari Duniailkom</𝗯>
console.log(boo.outerHTML);                         // Output: <𝗽>Sedang belajar <𝗲𝗺>JavaScript</𝗲𝗺> <𝗯>dari Duniailkom</𝗯></𝗽>
console.log(boo.innerText);                         // Output: Sedang belajar JavaScript dari Duniailkom
console.log(boo.outerText);                         // Output: Sedang belajar JavaScript dari Duniailkom
                                                    // ⤷ innerHTML berisi konten yang ada di dalam tag yang dipilih
                                                    // ⤷ outerHTML berisi tag yang dipilih lengkap beserta konten isinya
                                                    // ⤷ innerText & outerText (dalam banyak kasus) jarang sekali digunakan

boo.textContent = "<b>Teks baru 1!</b>";            // Mengubah konten isi dari <𝗽> ... </𝗽>   (<b> terbaca sebagai teks biasa)
boo.innerHTML   = "<b>Teks baru 2!</b>";            // Mengubah konten isi dari <𝗽> ... </𝗽>   (<b> membuat teks menjadi tebal)
boo.outerHTML   = "<h1>Teks baru 3!</h1>"           // Mengubah <𝗽> ... </𝗽> + konten isinya   (diganti menjadi <𝗵𝟭> ... </𝗵𝟭>)
coo.innerHTML   = "Title baru di tab browser!";     // Bahkan <𝘁𝗶𝘁𝗹𝗲> ... </𝘁𝗶𝘁𝗹𝗲> yang ada di <head> pun konten isinya bisa diubah
                                                    // ⤷ Jalankan Script di tab console, dan lihat perubahannya secara live! 🔔
                                                  
// E2. Mematribut di tag HTML

let doo = document.querySelector("h1");             // Let doo berisi <𝗵𝟭 id="judul">Belajar JavaScript</𝗵𝟭>

console.log(doo.hasAttribute("id"));                // Output: true             ⇨ Memeriksa apakah doo memiliki atribut id
console.log(doo.hasAttribute("class"));             // Output: false            ⇨ Memeriksa apakah doo memiliki atribut class
console.log(doo.getAttribute("id"));                // Output: judul            ⇨ Mengambil nilai dari suatu atribut

doo.setAttribute("title", "Sedang belajar");        // Menambah/menimpa sebuah atribut + nilainya
console.log(doo.hasAttribute("title"));             // Output: true             ⤷ Argument ke 1: Nama atributenya
console.log(doo.getAttribute("title"));             // Output: Sedang belajar   ⤷ Argument ke 2: Nilai atributnya
console.log(doo);                                   // Output: <𝗵𝟭 id="judul" title="Sedang belajar">Belajar JavaScript</𝗵𝟭>

                                                    // Menampilkan seluruh atribut beserta nilainya, dari sebuah tag HTML:
console.log(doo.attributes);                        // Output: ▶𝗡𝗮𝗺𝗲𝗱𝗡𝗼𝗱𝗲𝗠𝗮𝗽 [id="judul", title="Sedang belajar"] (length: 2)
console.log(doo.attributes[0]);                     // Output: id="judul"
console.log(doo.attributes[1]);                     // Output: title="Sedang belajar"
console.log(doo.attributes.length);                 // Output: 2

doo.removeAttribute("title");                       // Menghapus sebuah atribut + nilainya (Mempengaruhi baris kode diatasnya ⚠️)
                                                    // ⤷ Note: Meskipun atribut "title" di hapus di baris ini, namun saat check
                                                    //         di tag HTML-nya melalui console.log(doo) (lihat di baris atas),
                                                    //         maka atribut "title" sudah dianggap tidak ada.
console.log(doo);                                   // Output: <𝗵𝟭 id="judul">Belajar JavaScript</𝗵𝟭>

// E3. Memanipulasi Style CSS di tag HTML

let foo = document.querySelector("p:nth-child(3)"); // Let foo berisi <𝗽 style="color: blue;"> ... </𝗽>
                                                    // ⤷ Cara baca: Cari tag <p> yang berada pada urutan ke 3 dalam
                                                    //              sebuah parent element (dalam kasus ini: <body>)

console.log(foo.style);                             // Output: ▶𝗖𝗦𝗦𝗦𝘁𝘆𝗹𝗲𝗗𝗲𝗰𝗹𝗮𝗿𝗮𝘁𝗶𝗼𝗻 [0: "color"]  ⇨ Menampilkan seluruh 𝗜𝗻𝗹𝗶𝗻𝗲
console.log(foo.style[0]);                          // Output: color                               𝗖𝗦𝗦 dari sebuah tag HTML
console.log(foo.style[1]);                          // Output: undefined
console.log(foo.style.color);                       // Output: blue                             ⇨ Menampilkan secara spesifik
console.log(foo.style.backgroundColor);             // Output: (kosong)                            𝗜𝗻𝗹𝗶𝗻𝗲 𝗖𝗦𝗦 tertentu
console.log(foo.style.textDecoration);              // Output: (kosong)

foo.style.backgroundColor = "salmon";               // Menambah/menimpa sebuah 𝗜𝗻𝗹𝗶𝗻𝗲 𝗖𝗦𝗦 di tag HTML
foo.style.fontSize = "1.4em";                       // ⤷ Jalankan Script di tab console, dan lihat perubahannya secara live! 🔔

let goo = getComputedStyle(foo);                    // Manampilkan seluruh Style CSS (bukan hanya dari inline CSS saja)
                                                    // ⤷ Method getComputedStyle() milik Window Object (lihat bagian A di atas)

console.log(goo);                                   // Output: ▶𝗖𝗦𝗦𝗦𝘁𝘆𝗹𝗲𝗗𝗲𝗰𝗹𝗮𝗿𝗮𝘁𝗶𝗼𝗻 [0: "align-content", ...]
console.log(goo.length);                            // Output: 325 (Total 325 Style CSS sebagai nilai awal bawaan browser)
console.log(goo[0]);                                // Output: align-content
console.log(goo[324]);                              // Output: -webkit-writing-mode
console.log(goo.color);                             // Output: rgb(0, 0, 255)                   (Format yang dipakai: RGB)
console.log(goo.backgroundColor);                   // Output: rgba(0, 0, 0, 0)                 (Format yang dipakai: RGB)
console.log(goo.textDecoration);                    // Output: underline solid rgb(0, 0, 255)   (Format yang dipakai: RGB)

// E4. Memanipulasi Class CSS di tag HTML

let hoo = document.querySelector("div:nth-child(4)");   // Let hoo berisi <𝗱𝗶𝘃 class="merah tebal"> ... </𝗱𝗶𝘃>
let joo = document.querySelector("div:nth-child(5)");   // Let hoo berisi <𝗱𝗶𝘃 class="merah"> ... </𝗱𝗶𝘃>

                                                    // Menampilkan seluruh Class CSS yang digunakan sebuah tag HTML:
console.log(hoo.className);                         // Output: merah tebal
console.log(hoo.classList);                         // Output: ▶𝗗𝗢𝗠𝗧𝗼𝗸𝗲𝗻𝗟𝗶𝘀𝘁(𝟮) ["merah", "tebal"]
console.log(hoo.classList[0]);                      // Output: merah
console.log(hoo.classList[1]);                      // Output: tebal
console.log(hoo.classList.length);                  // Output: 2                ⇨ Memeriksa jumlah Class yang digunakan
console.log(hoo.classList.contains("tebal"));       // Output: true             ⇨ Memeriksa apakah memakai Class tertentu

hoo.className = "hijau";                            // Menimpa Class terdahulu  (dalam kasus ini: merah tebal 🡲 hijau)
console.log(hoo.className);                         // Output: hijau

console.log(joo.className);                         // Output: merah
console.log(joo.classList);                         // Output: ▶𝗗𝗢𝗠𝗧𝗼𝗸𝗲𝗻𝗟𝗶𝘀𝘁 ["merah"]
console.log(joo.classList[0]);                      // Output: merah
console.log(joo.classList[1]);                      // Output: undefined
console.log(joo.classList.length);                  // Output: 1
console.log(joo.classList.contains("tebal"));       // Output: false

joo.classList.add("tebal");                         // Menambah Class tertentu
console.log(joo.className);                         // Output: merah tebal
joo.classList.remove("merah");                      // Menghapus Class tertentu
console.log(joo.className);                         // Output: tebal

                                                    // 📚 Referensi node property & method lainnya:
                                                    // https://www.w3schools.com/jsref/dom_obj_all.asp
                                                    // https://developer.mozilla.org/en-US/docs/Web/API/Node
                                                    // https://developer.mozilla.org/en-US/docs/Web/API/Element
```

<br>
<div id="bab15"></div>

# 15. DOM Event <a href="#daftarisi">🡹</a>

1. Di dalam DOM, event adalah segala sesuatu yang bisa kita lakukan dengan halaman web, seperti men-klik sebuah tombol, klik kanan paragraf, menggeser cursor mouse ke atas sebuah menu, menginput sesuatu ke dalam form, menekan tombol tab atau enter, dll.
2. Ketika event terjadi, kita bisa menyiapkan kode JavaScript untuk melakukan sesuatu, yakni sebagai respon dari event tersebut. Misalnya saat sebuah tombol di klik, tampilkan pesan ```alert()```, atau ketika cursor mouse berada di atas menu, ubah warna background menu tersebut. Secara teknis, kode program yang dibuat untuk “menangkap” event ini dikenal dengan istilah **Event Handler** atau **Event Listener**.
3. Jumlah DOM event yang tersedia sangat banyak, lebih dari 200 dan terus bertambah. Secara garis besar di kelompokkan dalam beberapa tipe (mouse, keyboard, form, drag and drop, wheel, touch, gestures, gamepad, virtual reality, speech, mutation, svg, dll), yang paling banyak digunakan adalah event mouse, keyboard, dan form. Ke tiga event inilah yang akan dibahas di buku ini.

```Javascript
// =============================
// A. 3 Cara Input Event Handler
// =============================
```

```HTML
<!-- A1. Event Handler dari atribut HTML -->

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <span onclick="alert('Saya di klik');">Click</span><br>
    <span ondblclick="alert('Saya di double klik');">Double Click</span><br>
    <span oncontextmenu="alert('Saya di klik kanan');">Right Click</span><br>
    <span onmouseenter="alert('Pointer masuk ke element');">Mouse Enter</span><br>
    <span onmouseover="alert('Pointer berada di atas element');">Mouse Over</span><br>
    <span onmouseleave="alert('Pointer keluar dari element');">Mouse Leave</span><br>

    <h1 onclick="document.querySelector('p').innerHTML='Paragraf 1 muncul!';">Klik saya</h1>
    <p></p> <!-- tag p sebagai placeholder/penampung hasil ketika event terjadi-->

    <h1 onclick="tampilkan();">Klik saya juga</h1>
    <p></p> <!-- tag p sebagai placeholder/penampung hasil ketika event terjadi-->
    
    <script>
      function tampilkan(){
        document.querySelector("p:nth-child(16)").innerHTML="Paragraf 2 muncul!";
      }
    </script>
  </body>
</html>
```

```HTML
<!-- A2. Event Handler dari property Element -->

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1 id="judul1">Klik saya</h1>
    <p></p>

    <h1 id="judul2">Klik saya juga</h1>
    <p></p>

    <h1 id="judul3">Klik saya juga dong</h1>
    </p></p>

    <script>
      // ➊ Cara penulisan 1: Dengan input Function ke property
      function tampilkan1(){
        document.querySelector("p").innerHTML="Paragraf 1 muncul!";
      }
      let nodeH1A = document.getElementById("judul1");
      nodeH1A.onclick = tampilkan1;

      // ➋ Cara penulisan 2: Dengan Anonymous Function
      let nodeH1B = document.getElementById("judul2");
      nodeH1B.onclick = function(){
        document.querySelector("p:nth-child(4)").innerHTML="Paragraf 2 muncul!";
      }

      // ➌ Menambahkan beberapa event berbeda sekaligus (Contoh disini memakai cara penulisan 1)
      function tampilkanClick(){
        nodeP3.innerHTML="Saya di klik";
      }
      function tampilkanDoubleClick(){
        nodeP3.innerHTML="Saya di double klik";
      }
      function tampilkanContextMenu(){
        nodeP3.innerHTML="Saya di klik kanan";
      }

      let nodeH1C = document.getElementById("judul3");     
      let nodeP3  = document.querySelector("p:nth-child(6)");
      nodeH1C.onclick       = tampilkanClick;
      nodeH1C.ondblclick    = tampilkanDoubleClick;
      nodeH1C.oncontextmenu = tampilkanContextMenu;

      // ➍ Menghapus event tertentu yang dipilih
      // nodeH1C.onclick       = null;   // Berikan nilai null ke property untuk menghapus event
      // nodeH1C.ondblclick    = null;   // Saat ini dilakukan maka event tidak akan berjalan
      // nodeH1C.oncontextmenu = null;   // Coba jalankan Script di tab console 🔔
    </script>
  </body>
</html>
```

```HTML
<!-- A3. Event Handler dari method Element (✔️ Recommended) -->

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Belajar JavaScript</title>
  </head>
  <body>
    <h1 id="judul1">Klik saya</h1>
    <p></p>

    <h1 id="judul2">Klik saya juga</h1>
    <p></p>

    <h1 id="judul3">Klik saya juga dong</h1>
    <p></p>
    <p></p>
    <p></p>

    <script>
      // ➊ Cara penulisan 1: Dengan input Function sebagai argument
      function tampilkanClick(){
        nodeP1.innerHTML="Saya di klik";
      }
      function tampilkanDoubleClick(){
        nodeP1.innerHTML="Saya di double klik";
      }
      function tampilkanContextMenu(){
        nodeP1.innerHTML="Saya di klik kanan";
      }

      let nodeH1A = document.getElementById("judul1");
      let nodeP1  = document.querySelector("p");
      nodeH1A.addEventListener("click", tampilkanClick);
      nodeH1A.addEventListener("dblclick", tampilkanDoubleClick);
      nodeH1A.addEventListener("contextmenu", tampilkanContextMenu);

      // ➋ Cara penulisan 2: Dengan Anonymous Function
      let nodeH1B = document.getElementById("judul2");
      let nodeP2  = document.querySelector("p:nth-child(4)");
      
      nodeH1B.addEventListener("click", function() {
        nodeP2.innerHTML="Saya di klik";
      });
      nodeH1B.addEventListener("dblclick", function() {
        nodeP2.innerHTML="Saya di double klik";
      });
      nodeH1B.addEventListener("contextmenu", function() {
        nodeP2.innerHTML="Saya di klik kanan";
      });

      // ➌ Menggabungkan multiple event yang sama (Contoh disini memakai cara penulisan 1)
      function tampilkanPAtas(){
        nodeP3.innerHTML="P atas muncul!";
      }
      function tampilkanPTengah(){
        nodeP4.innerHTML="P tengah muncul!";
      }
      function tampilkanPBawah(){
        nodeP5.innerHTML="P bawah muncul!";
      }
      let nodeH1C = document.getElementById("judul3");
      let nodeP3  = document.querySelector("p:nth-child(6)");
      let nodeP4  = document.querySelector("p:nth-child(7)");
      let nodeP5  = document.querySelector("p:nth-child(8)");
      nodeH1C.addEventListener("click", tampilkanPAtas);
      nodeH1C.addEventListener("click", tampilkanPTengah);
      nodeH1C.addEventListener("click", tampilkanPBawah);

      // ➍ Menghapus event tertentu yang dipilih
      // nodeH1C.removeEventListener("click", tampilkanPTengah); // Menghapus event tertentu yang dipilih
      // nodeH1C.removeEventListener("click", tampilkanPBawah);  // Coba jalankan Script di tab console 🔔
    </script>
  </body>
</html>
```

```Javascript
// ===============
// B. Event Object
// ===============

// ...

// ========================
// C. Event Prevent Default
// ========================

// ...
```

<br>
<div id="babxx"></div>

# XX. Tambahan Materi: Advanced JavaScript <a href="#daftarisi">🡹</a>

```Javascript
/*
Beberapa fitur ES6+ sebenarnya sudah dibahas di BAB-BAB sebelumya secara singkat saja.
Di BAB ini, akan kembali membahas fitur ES6+ lebih banyak lagi dan secara mendetail.
*/

// ==================
// A. Template String
// ==================

let number  = 24;                                         // Template String bisa dipakai untuk expressions kompleks
console.log(`${(number%2==0) ? "genap":"ganjil" }`);      // Output: genap
console.log(`${alert("Hello!")}`);                        // Output: Muncul Popup "Hello!"

let multiln = `String baris 1
String baris 2
String baris 3`;                      // Template String bisa digunakan untuk membuat multi-line String
console.log(multiln);                 // Output: String baris 1
                                      //         String baris 2
                                      //         String baris 3

let fragmen = `<div>
  <h1>${number*10}</h1>
  <h2>WOW!</h2>
</div>`;                              // Bahkan juga bisa digunakan untuk membuat HTML Fragments
console.log(fragmen);                 // Output: <div>
                                      //           <h1>240</h1>
                                      //           <h2>WOW!</h2>
                                      //         </div>

/*
📚 Selain manfaat yang disebutkan di atas, Template String juga dapat digunakan sebagai Tagged Templates Literals.
Selebihnya mengenai Tagged Templates Literals, simak video berikut: https://www.youtube.com/watch?v=sbjkjjCcz8M
*/

// ==================
// B. ...............
// ==================

/*
Semua fitur di E6+:
- Kembali bahas template string, arrow function, dll secara detail
- Inheritance, Encapsulation, dll
- Promise, Fetch, Async Await, dll
- Ambil dari bukureact.id (intisari dari modern JavaScript)
- ...

TOP JS Library berdasarkan topik:
- Urusan Date               : moment.js
- Urusan Grafik             : chart.js
- Urusan Visualisasi Data   : D3.js
- ...
*/
```
