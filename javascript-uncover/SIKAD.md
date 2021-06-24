<div id="top"></div>

# JavaScript Uncover

Materi utama di page ini diambil dari buku <a href="https://www.duniailkom.com/javascript-uncover-panduan-belajar-javascript-untuk-pemula/">JavaScript Uncover by Duniailkom.com</a>. Selebihnya merupakan materi tambahan (pelengkap), gabungan dari website <a href="https://www.youtube.com/channel/UCkXmLjEr95LVtGuIm3l2dPg">Web Programming UNPAS</a>, <a href="https://www.youtube.com/channel/UC14ZKB9XsDZbnHVmr4AmUpQ">Programmer Zaman Now</a>, <a href="https://bukureact.id/">BukuReact.id</a>, <a href="https://www.w3schools.com/">W3Schools</a> dan <a href="https://www.w3docs.com/">W3Docs</a>. Untuk Cheat Sheet dapat diakses di <a href="https://www.w3schools.com/jsref/default.asp">W3Schools: JavaScript Reference</a>. Semoga bermanfaat 😊

**Markdown ini ditulis oleh**: <a href="https://alamehan.github.io/">alamehan.github.io</a><br><br>
**Note**: Semua keterangan terkait mengacu ke bab sekian, segera perbaiki, karena strukturnya udah berubah (!!!)

## ① 𝒫𝑒𝓇𝓀𝑒𝓃𝒶𝓁𝒶𝓃 👋 <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
<div id="daftar_isi_bab1"></div>
<br>
  
| Bab 1                                            	    | Estimasi Baca 	|
|------------------------------------------------------	|---------------	|
| <a href="#bab1_1">1-1. Kenalan dengan JavaScript</a> 	| X Menit       	|
| <a href="#bab1_2">1-2. Sejarah & Perkembangan</a>    	| X Menit       	|
| <a href="#bab1_3">1-3. Menjalankan Kode</a>          	| X Menit       	|
| <a href="#bab1_4">1-4. Aturan Dasar</a>              	| X Menit       	|
| <a href="#bab1_5">1-5. Variable</a>                  	| X Menit       	|
  
<hr>
<div id="bab1_1"></div>
  
## 1-1. Kenalan dengan JavaScript <a href="#daftar_isi_bab1">🡅</a>

JavaScript merupakan bagian dari 5 materi dasar web programming, yakni: HTML, CSS, PHP, MySQL dan JavaScript. Bersama-sama dengan HTML dan CSS, ketiganya berbagi peran masing-masing. HTML digunakan untuk membuat struktur dan isi dari halaman web (content). CSS untuk mempercantik tampilan website (design). Sedangkan JavaScript berfungsi menangani interaksi (behavior).**“HTML for content, CSS for presentation and JavaScript for behavior”**.

HTML, CSS dan JavaScript sama-sama termasuk ke dalam kelompok “client side programming language”, yakni bahasa pemrograman yang dijalankan di sisi client (web browser). PHP juga merupakan bahasa pemrograman web, tapi berada di dalam server, sehingga disebut sebagai “server side programming language”.

**Client Side Programming**: Ini artinya, untuk menjalankan JavaScript kita hanya butuh 2 aplikasi, yakni text editor dan web browser. Text editor digunakan membuat kode JavaScript, dan kode JavaScript tersebut bisa langsung diakses dari web browser. Kita pun bisa melihat kode JavaScript yang digunakan dari sebuah website (sama seperti HTML dan CSS). Silahkan buka website apa saja, klik kanan lalu pilih View Page Source.

**Server Side Programming**: Untuk menjalankan kode program PHP kita harus menggunakan aplikasi seperti Apache web server (yang merupakan bagian dari XAMPP). Kita tidak bisa melihat kode PHP yang digunakan sebuah website secara langsung layaknya HTML, CSS dan JavaScript.

Perkembangan JavaScript yang sangat pesat akhir-akhir ini melahirkan banyak penerapan lain dari JavaScript. Sebagai contoh, **Node.js** adalah penggunaan JavaScript di sisi server. Dalam buku ini kita hanya fokus membahas penggunaan JavaScript di sisi client (di dalam web browser).

Apa yang akan kita pelajari dalam buku ini terdiri dari 2 kelompok besar: JavaScript dan **DOM (Document Object Model)**. JavaScript adalah bahasa pemrograman, sedangkan DOM merupakan objek HTML yang akan kita manipulasi, seperti teks, gambar, form, tombol, title bar web browser, event, dll. Bahasa pemrograman JavaScript dikembangkan oleh ECMA, sedangkan DOM dikembangkan oleh W3C (organisasi yang juga membuat standar HTML dan CSS). Bisa dibilang, JavaScript sepenuhnya terpisah dari HTML.

Setelah mempelajari JavaScript, barulah kita masuk ke DOM. Disinilah JavaScript digunakan untuk mengubah total tampilan halaman web. Jadi, jika anda merasa jenuh dengan pembahasan dari bab 2 hingga 13, tahan dulu! Paksakan untuk terus mempelajarinya. Dengan pemahaman JavaScript yang cukup, kita memiliki pondasi yang kuat untuk memanipulasi objek HTML yang nantinya diakses lewat DOM mulai dari bab 14 hingga akhir buku.

<hr>
<div id="bab1_2"></div>

## 1-2. Sejarah & Perkembangan <a href="#daftar_isi_bab1">🡅</a>

<img src="assets/brendan-eich.png"><br>

**Brendan Eich** membuat prototype bahasa baru dalam 10 hari. Pada Mei 1995, bahasa pemrograman “Mocha” lahir. Bahasa pemrograman inilah yang diputuskan untuk digunakan Netscape. Bahasa pemograman Mocha dirilis pertama kali ke dalam versi beta Netscape Navigator 2.0 di bulan September 1995, tetapi dengan menggunakan nama baru: LiveScript. Umur dari LiveScript ternyata tidak lama. 3 bulan kemudian, tepatnya Desember 1995, hadir Netscape Navigator 2.0 beta 3 dengan sebuah bahasa baru: JavaScript. Sebenarnya ini bukanlah bahasa pemrograman baru, tapi perubahan nama dari LiveScript. Nama JavaScript dipilih agar Netscape bisa ‘nompang tenar’ dari bahasa pemrograman JAVA milik Sun Microsystems, yang pada masa itu sangat populer di kalangan programmer.

“The first browser war”, perang web browser pertama antara Internet Explorer buatan Microsoft vs Netscape Navigator buatan Netscape Communications.

**ECMAScript** adalah sebuah standar bahasa pemrograman komputer, dimana JavaScript merupakan salah satu implementasi dari ECMAScript. JavaScript tidak bisa dijadikan standar karena masalah merk “JAVA” yang merupakan trademark SUN Micosystem (sekarang sudah diakuisisi Oracle). Intinya: Standarisasi **JavaScript = ECMAScript**. EMCAScript digunakan hanya saat merujuk ke versi dari JavaScript.

Pengembangan ECMAScript 4 berhenti di tengah jalan, ini disebabkan perbedaan pendapat antar anggota **komite TC39**, terutama mengenai fitur apa yang harus ada di ECMAScript 4. Proses “perseteruan” berlangsung cukup lama, memakan waktu hingga 10 tahun (sampai dengan 2009). Selama jangka waktu tersebut, tidak ada versi baru dari ECMAScript.

Di pasar web browser, Internet Explorer menjadi sangat dominan, menguasai lebih dari 80% -90% market share dari tahun 2001 hingga 2009. Netscape Navigator bisa dibilang sudah punah pada tahun 2004. Web browser Opera hadir sebagai alternatif, tapi tidak bisa berbuat banyak.

**AJAX**, singkatan dari **(Asynchronous JavaScript and XML)**. AJAX memungkinkan sebuah halaman web berkomunikasi langsung dengan server tanpa harus di-reload. Komunikasi antara web browser dengan web server berlangsung di latar belakang (background) secara asynchronous, hasilnya website menjadi lebih dinamis. Sebagai contoh, halaman registrasi bisa langsung mengecek apakah username yang diinput sudah ada di database atau belum. Ini dapat dilakukan sesaat setelah user berpindah dari kolom input username ke kolom dibawahnya. Tanpa menggunakan AJAX, proses pengecekan baru berlangsung saat user selesai mengisi form dan men-klik tombol submit (karena pengecekan harus dilakukan ke database yang ada di server).

Selain AJAX, berkembang juga berbagai komunitas dan library JavaScript seperti Prototype, **jQuery**, Dojo Toolkit, dan MooTools. Masa-masa ini bisa dibilang awal kebangkitan JavaScript. Dengan menggunakan library seperti jQuery, perbedaan implementasi ECMAScript dari berbagai web browser bisa diatasi dengan mudah. jQuery menyediakan ‘abstraction layer’ agar web programmer bisa berfokus kepada fitur yang ingin dicapai. Programmer yang sebelumnya “anti” dengan JavaScript (karena susahnya mengatasi perbedaan fitur web browser), mulai melirik library seperti jQuery.

Setelah perang web browser pertama berakhir dengan kekalahan telak Netscape, perang kedua segera mulai dengan dirilisnya Mozilla Firefox (sebagai "Reingkarnasi Netscape"). Dengan cepat Firefox menjadi web browser favorit yang sepertinya akan segera menggusur IE. Puncaknya di tahun 2010 Firefox menguasai sekitar 30% pasar web browser, walaupun IE masih tetap dominan tapi setiap tahun mengalami tren penurunan. Tidak lama lagi sepertinya Firefox bisa menjadi web browser paling populer menggantikan IE. Namun harapan ini pupus karena muncul web browser baru dari raja mesin pencari: Google Chrome yang dirilis pada Desember 2008. Didukung dengan promosi gencar, nama besar Google, fitur menawan, dan eksekusi yang cepat, membuat Google Chrome segera menjadi web browser paling banyak digunakan hingga saat ini, mengalahkan IE, Firefox, dan Opera.

<img src="assets/chrome-winner.png"><br>

ECMAScript 6 atau ES6 atau ECMAScript 2015 dirilis pada bulan Juni 2015. Cukup banyak penambahan baru pada versi ini, sebagian besar merupakan fitur lanjutan untuk membuat aplikasi yang memiliki kompleksitas tinggi, seperti penggunaan **JavaScript di server menggunakan Node.js**. Mulai dari ECMAScript 6 dan selanjutnya, penamaan ECMAScript akan menggunakan nama tahun saat standar tersebut dirilis, seperti ECMAScript 2015, ECMAScript 2016, dst. Banyak perdebatan mengenai pilihan nama ini, sehingga masih sering disebut sebagai ECMAScript 6 (ES6). Dalam buku ini kita lebih banyak membahas ECMAScript 5. Walaupun menggunakan ECMAScript 5, dasar JavaScript yang ada di buku ini tetap valid untuk versi 6 dan versi 7. Fitur tambahan yang ada di ECMAScript 6 dan ECMAScript 7 juga lebih banyak ke materi lanjutan yang terlalu kompleks jika dimasukkan ke buku JavaScript untuk pemula. ES6 dan ES7 lebih cocok jika anda berniat mempelajari JavaScript sebagai bahasa pemrograman server menggunakan Node.js.

**JavaScript Engine** adalah mekanisme internal yang dimiliki oleh web browser untuk menjalankan kode JavaScript. JavaScript Engine dapat disamakan dengan compiler dalam bahasa pemograman lain, yakni algoritma yang digunakan untuk menjalankan JavaScript. Semakin cepat sebuah web browser menjalankan JavaScript akan semakin baik. **V8** adalah nama JavaScript Engine untuk Google Chrome, **SpiderMonkey** untuk Mozilla Firefox, dan **Chakra** untuk Internet Explorer.

Perkembangan JavaScript Saat Ini: Website yang tidak berbentuk “website”, tetapi menyerupai aplikasi desktop yang dikenal sebagai **Single-page Application (SPA)**. Contoh dari Single-page Application ini seperti aplikasi Google: Gmail, GDrive, Google Doc, dll. Di website tersebut, halamannya akan tetap sama, tidak di reload seperti layaknya sebuah website.

Namun perlu juga dipahami bahwa walaupun materi di eBook JavaScript Uncover sudah lumayan rumit, ini barulah dasar dari JavaScript. Jika anda serius ingin mempelajari JavaScript lebih jauh lagi, bisa lanjut ke library seperti **jQuery**, framework seperti **AngularJS**, **ReactJS** maupun **VueJS**, atau ke server menggunakan **Node.js**.

Timeline sejarah JavaScript dari awal lahir hingga saat ini secara ringkas dapat diakses <a href="https://www.jetbrains.com/lp/javascript-25/">disini</a>. Daftar feature baru dari mulai **ES6 hingga ES.Next** dapat diakses di <a href="https://en.wikipedia.org/wiki/ECMAScript">Wikipedia</a>, <a href="https://www.javascripttutorial.net/es-next/">JavaScriptTutorial</a>, <a href="https://jsfeatures.in/">JSFeatures</a>, <a href="https://www.freecodecamp.org/news/es5-to-esnext-heres-every-feature-added-to-javascript-since-2015-d0c255e13c6e/">FreeCodeCamp</a>, <a href="https://github.com/daumann/ECMAScript-new-features-list">GitHub</a>, <a href="https://javascript.info/">JavaScriptInfo</a>.
  
<hr>
<div id="bab1_3"></div>
  
## 1-3. Menjalankan Kode <a href="#daftar_isi_bab1">🡅</a>

> - [X] 𝐀. Inline JavaScript
> - [X] 𝐁. Internal JavaScript
> - [X] 𝐂. External JavaScript
> - [X] 𝐃. Posisi Terbaik JavaScript
> - [X] 𝐄. Tag No-Script

### 𝐀. Inline JavaScript

```HTML
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

### 𝐁. Internal JavaScript

```HTML
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

### 𝐂. External JavaScript

```HTML
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

Menempatkan kode JavaScript di bagian atas banyak ditemukan. Namun berkaitan dengan masalah performa, beberapa developer web menyarankan meletakkan JavaScript dibagian bawah tag ```<body>```, yakni sebelum tag penutup ```</body>```, sebagaimana yang dijelaskan dari sebuah artikel di Yahoo Developer Network: Best Practices for Speeding Up Your Web Site. 

Cara web browser dalam menampilkan sebuah halaman web, yakni secara berurutan dari atas ke bawah, mulai dari baris pertama hingga baris terakhir. Fitur **cache** dari web browser bisa mempercepat pengaksesan website dengan cara menyimpan file JavaScript di dalam cache.

Dengan memanggil file external JavaScript dari bagian bawah tag ```<body>```, memberi kesempatan web browser untuk memproses kode HTML terlebih dahulu, baru kemudian mendownload file JavaScript. Efeknya, pengujung web bisa langsung melihat tampilan web selama proses ini, tidak hanya halaman kosong. 

### 𝐃. Posisi Terbaik JavaScript

```HTML
<html>
  <head>
    ...
    <!-- External JavaScript -->
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

Atribut **async** dan **defer**: kita bisa mengatur kapan dan bagaimana file external JavaScript diproses. Kedua atribut ini memungkinkan penulisan tag ```<script>``` tidak harus di bawah tag ```<body>```. Jika atribut **async** ditambahkan ke dalam tag ```<script>```, file JavaScript akan diproses pada saat yang bersamaan dengan kode HTML (secara simultan). Dengan kata lain, web browser tidak “terkunci” untuk menjalankan kode JavaScript. Metode ini juga dikenal dengan istilah **Asynchronous JavaScript** (Di proses secara bersamaan = Asynchronous). 

Dengan tambahan atribut **async**, kode HTML tetap diproses sembari mendownload file JavaScript. Dengan kata lain, web browser tidak masuk ke dalam Render-Blocking JavaScript. Atribut **defer** digunakan untuk mengatur kapan file JavaScript dijalankan. Dengan atribut ini, file JavaScript baru di download dan dieksekusi setelah seluruh kode HTML selesai diproses. Efek dari atribut **async** dan **defer** mungkin terdengar sama. Perbedaaan mendasar adalah, **async** digunakan untuk mengatur cara eksekusi kode JavaScript, sedangkan **defer** untuk mengatur kapan file JavaScript tersebut di download dan diproses.

Tambahan atribut **async** dan **defer** dari HTML5 membawa perubahan terkait posisi terbaik peletakan kode JavaScript. Standar saat ini adalah menempatkan kode JavaScript di bagian ```<head>``` dengan tambahan atribut **async**. Alasannya, web browser bisa langsung mengeksekusi file JavaScript pada saat yang bersamaan dengan proses kode HTML, sehingga website dapat ditampilkan dengan lebih cepat (tidak mengalami Render-Blocking JavaScript). Untuk kode JavaScript yang tidak terlalu penting (dan bisa menunggu), tambahkan atribut **defer**. Sebagai tambahan, atribut **async** dan **defer** hanya berlaku untuk external JavaScript. Untuk internal JavaScript, atribut ini akan diabaikan dan posisi terbaik tetap di bagian bawah tag ```<body>```.

Berbeda dengan mayoritas bahasa pemrograman lain, secara default kita tidak bisa melihat pesan error dari JavaScript. Padahal ini sangat penting selama pembuatan kode program. Tidak ada yang lebih membuat pusing dari program yang tidak berjalan, namun tidak tahu salahnya dimana. Untuk menampilkan pesan error JavaScript, kita bisa menggunakan menu **Web developer tools** bawaan web browser. Setiap web browser modern memiliki tools seperti ini.

<img src="assets/developer-tools.png"><br>

Tab Inspector (1) bisa digunakan untuk menelusuri seluruh kode HTML yang terdapat di dalam halaman web (2), di sisi kanan kita bisa melihat kode CSS yang digunakan oleh tag HTML tersebut (3). Jika anda sering mengedit kode CSS, tab Inspector ini sangat bermanfaat untuk melihat dan menjalankan (mengedit) kode CSS tanpa perlu mengubah file asli.

Tab yang sering kita akses selama membuat kode program JavaScript adalah **Tab Console**, yang berada di sebelah kanan tab Inspector. Apabila kode yang anda buat tidak berjalan sebagaimana mestinya, hal pertama yang harus dilakukan adalah memeriksa tab Console ini. Selain menampilkan pesan error, di dalam tab Console kita juga bisa menjalankan kode program JavaScript secara langsung, tanpa harus menulisnya di dalam file HTML. Fungsi ```console.log()``` berguna untuk menampilkan hasil kode program ke tab Console.

### 𝐄. Tag No-Script

```HTML
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

Salah satu kelemahan (sekaligus keunggulan) dari JavaScript adalah, pengunjung web bisa mematikan JavaScript yang ada di web browser mereka. Tag ```<noscript>``` bisa digunakan untuk menampilkan teks keterangan yang hanya bisa terlihat pada web browser yang tidak memiliki JavaScript (atau JavaScriptnya dimatikan).
  
<hr>
<div id="bab1_4"></div>
  
## 1-4. Aturan Dasar <a href="#daftar_isi_bab1">🡅</a>

> - [X] 𝐀. Statement
> - [X] 𝐁. Case Sensitive
> - [X] 𝐂. Whitespace
> - [X] 𝐃. Indenting
> - [X] 𝐄. Comment

### 𝐀. Statement

**Statement** adalah sebutan untuk sebuah baris perintah JavaScript. Walaupun saya menggunakan kata “baris”, bisa saja sebuah Statement butuh beberapa baris (seperti Function). Atau dalam 1 baris bisa terdiri dari beberapa Statement. Setiap Statement diakhiri dengan tanda titik koma (semi colon): ‘ ; ‘. Sebenarnya, tanda titik koma untuk mengakhiri Statement JavaScript ini adalah opsional. Artinya, boleh tidak ditulis sepanjang Statement tersebut harus berada dalam baris baru (1 Statement, 1 baris). Sebaiknya kita tetap menambahkan tanda titik koma untuk mengakhiri setiap Statement di dalam JavaScript.

### 𝐁. Case Sensitive

**Case Sensitivity**: JavaScript termasuk bahasa pemrograman yang bersifat case sensitif, artinya huruf besar dan huruf kecil dianggap berbeda. Salah menulis huruf sangat sering terjadi, misalnya pada saat pendefinisian Variable.

### 𝐂. Whitespace

**Whitespace** mengacu pada karakter yang digunakan untuk memberikan ruang horizontal atau vertikal antara karakter lain, atau dengan kata lain karakter “kosong” seperti spasi, tab, atau baris baru (new line). Secara umum di dalam JavaScript whitespace akan diabaikan.

### 𝐃. Indenting

**Indenting** adalah istilah yang digunakan untuk menambahkan spasi atau tab diawal baris kode program. Tujuannya agar kode program lebih mudah dibaca terutama jika kode program tersebut sudah mencapai puluhan atau ratusan baris kode program. 

### 𝐄. Comment

**Comment** atau baris komentar adalah sebutan untuk kode program yang tidak akan di eksekusi oleh JavaScript. Selain sebagai dokumentasi, komentar juga sering digunakan untuk menghentikan sementara baris kode program. Di JavaScript, Comment ditulis menggunakan karakter ```// komentar``` (untuk single line) & ```/* komentar */``` (untuk multi line). Di sepanjang contoh kode yang disertakan di bab-bab selanjutnya, penggunaan Comment akan banyak sekali ditemukan (sebagai keterangan baris sebuah kode).

<hr>
<div id="bab1_5"></div>
  
## 1-5. Variable <a href="#daftar_isi_bab1">🡅</a>

Secara sederhana, Variable adalah “wadah/penampung” dari sebuah data. Disebut Variable karena data yang kita simpan bisa berubah-ubah sepanjang kode program (isinya tidak tetap). ```var angka = 192;``` **Operasi Assignment** atau memberikan nilai ke sebuah Variable dibaca dari kanan ke kiri (right-to-left, baca selengkapnya <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence">disini</a>). Artinya, 192 “dimasukkan” sebagai nilai ke Variable ```angka```.

JavaScript termasuk ke dalam bahasa pemrograman **Typeless Programming Language**, yakni kelompok bahasa pemrograman yang Variablenya bisa diisi dengan tipe data apa saja tanpa harus dideklarasikan terlebih dahulu.

Apabila anda sering mengikuti tutorial programming dari situs berbahasa inggris, nama Variable **foo**, **bar**, dan **baz** sering digunakan. Ketiganya dikenal sebagai **dummy Variable**, yakni Variable yang fungsinya hanya sebagai contoh. Mirip seperti teks “Lorem Ipsum dolor sit amet” dalam bidang design.

Kita bisa memberi nama apa saja untuk Variable, apakah itu ```angka```, ```foo```, ```bar```, ```andi```, atau ```username```. Selain Variable (Var), kita juga bebas untuk membuat nama Konstanta (Const), Function, maupun Object. Semua inilah yang termasuk ke dalam kelompok **Identifier**. Identifier di dalam JavaScript memiliki aturan sebagai berikut:
   - Bersifat case sensitive, dimana huruf besar dan kecil dianggap berbeda.
   - Bisa terdiri dari huruf, angka, underscore “_”, dan tanda dollar “$“. Selain itu, dianggap sebagai karakter ilegal.
   - Karakter pertama dari Identifier tidak boleh berupa angka. Angka hanya bisa digunakan sebagai karakter kedua dan seterusnya.
   - Harus selain dari **reserved keyword**, yakni kata khusus yang berfungsi sebagai perintah di dalam JavaScript, seperti ```var```, ```while```, dll.

Di CSS kita menggunakan cara penulisan selector yang dipisah dengan tanda “ - ”, seperti ```main-box```, ```left-sidebar```, dan ```single-post```. Di PHP kita mengenal **Snake Case**, yakni menggunakan huruf kecil dan tanda underscore sebagai pemisah Variable, seperti ```jumlah_barang```, ```nama_dosen```, dan ```alamat_siswa```. Di JavaScript menggunakan **CamelCase**. CamelCase adalah cara penulisan Variable dimana jika sebuah Variable terdiri dari beberapa kata, huruf pertama dari kata kedua dan seterusnya diubah menjadi huruf besar, seperti: ```banyakAnggota```, ```totalBiaya```, ```mainBox```, atau ```jumlahKlikSatuHari```. Jika Variable tersebut hanya terdiri dari 1 kata, ditulis dengan huruf kecil semua.

**Strict Mode** memaksa JavaScript menampilkan error (di Tab Console) pada kode program yang seharusnya bisa berjalan “normal”. Tujuannya, meminimalisir kemungkinan bug karena penulisan yang salah, typo, dan berbagai hal lain. Strict mode sepenuhnya opsional dan mungkin tidak bisa selalu anda gunakan, terutama jika terdapat kode JavaScript pendahulu yang terlalu rumit untuk diubah semuanya. Strict Mode akan membuat web browser menampilkan error dimana sebelumnya hanya ada **“silent error”**. Salah satunya ketika membuat Variable tanpa perintah ```var```. Untuk masuk ke dalam Strict Mode, tambahkan String ```"use strict";``` di baris pertama kode JavaScript atau di baris paling awal dari sebuah Function.

EcmaScript 6 membawa fitur baru ke dalam JavaScript, yakni menggunakan perintah ```let``` untuk membuat Variable (sebagai alternatif dari ```var```). Perbedaan mendasar dari ```var``` dan ```let``` adalah terkait dengan **Variable scope**, yakni di bagian mana sebuah Variable masih bisa diakses. Penjelasan mengenai Variable scope akan dibahas pada bab tentang Function. Selain Let, ada juga Konstanta (```const```) yaitu Variable yang nilainya tidak bisa diubah sepanjang kode program. Setelah Konstanta ditulis dan diberi nilai awal, isi Konstanta tersebut tidak bisa diubah.

Format penulisan: Var/Let diawali huruf kecil (```total```, ```totalBiaya```, dst), Const huruf besar semua (```PI```, ```RUMUS_A```, dst), dan Class diawali huruf besar (```Mobil```, ```MobilBaru```, dst). **Class dibahas di bab 11**. Tujuan dari format penulisan ini yaitu agar programmer dapat dengan mudah membedakan mana Variable/Let, Konstanta maupun Class.

Pada contoh di bawah: Var ```harga```, Let ```namaLengkap```, dan Const ```NILAI_PI``` adalah **Identifier**. Sedangkan ```12000```, ```"Rudi Siswoyo"```, dan ```3.14``` adalah **Literal**.

```HTML
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

</details>

## ② 𝒦𝑜𝓃𝓈𝑒𝓅 𝒟𝒶𝓈𝒶𝓇 👨‍💻 <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
<div id="daftar_isi_bab2"></div>
<br>
  
| Bab 2                                 	    | Estimasi Baca 	|
|--------------------------------------------	|---------------	|
| <a href="#bab2_1">2-1. Tipe Data</a><br>   	| X Menit       	|
| <a href="#bab2_2">2-2. Operator</a>        	| X Menit       	|
| <a href="#bab2_3">2-3. Struktur Logika</a> 	| X Menit       	|
| <a href="#bab2_4">2-4. Perulangan</a>      	| X Menit       	|
| <a href="#bab2_5">2-5. Function</a>        	| X Menit       	|
| <a href="#bab2_6">2-6. Object</a>          	| X Menit       	|
  
<div id="bab2_1"></div>
  
## 2-1. Tipe Data <a href="#daftar_isi_bab2">🡅</a>
  
> 𝐓𝐢𝐩𝐞 𝐃𝐚𝐭𝐚 𝐏𝐫𝐢𝐦𝐢𝐭𝐢𝐟
> > - [X] 𝐀. Number
> > - [X] 𝐁. NaN & Infinity
> > - [X] 𝐂. String
> > - [X] 𝐃. Boolean
> > - [X] 𝐄. Null & Undefined
> > - [ ] 𝐅. Symbol

> 𝐓𝐢𝐩𝐞 𝐃𝐚𝐭𝐚 𝐎𝐛𝐣𝐞𝐜𝐭
> > - [X] 𝐆. Array
> > - [X] 𝐇. Object (Bab ...)
> > - [X] 𝐈. RegExp (Bab ...)
> > - [X] 𝐉. Date (Bab ...)
> > - [ ] 𝐊. Map & WeakMap
> > - [ ] 𝐋. Set & WeakSet

Secara garis besar, tipe data dalam JavaScript terdiri dari 2 kelompok, yakni tipe data primitif, dan tipe data object. Tipe data primitif disebut demikian karena tipe data ini “sederhana” dan hanya terdiri dari 1 nilai. Yang termasuk ke dalam **tipe data primitif**, yaitu: **Number, NaN, Infinity, String, Boolean, Null, Undefined, dan Symbol**. Sedangkan tipe data object, bisa disebut sebagai tipe data “khusus” yang prilaku dan isinya beragam. Adapun yang termasuk ke dalam **tipe data object**, yaitu: **Array, Object, RegExp, Date, Map, WeakMap, Set, dan WeakSet.**

### 𝐀. Number

```Javascript
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
```

### 𝐁. NaN & Infinity

```JavaScript
var numK = 9/"a"; console.log(numK);  // Output: NaN (Not a Number)
var numL = 9/0; console.log(numL);    // Output: Infinity (Tak Hingga)
```

### 𝐂. String

```Javascript
var strA = "Hello World!";            // String dengan kutip dua
var strB = 'Hello World!';            // String dengan kutip satu
var strC = "Hari Jum'at";             // Kutip satu di dalam kutip dua
var strD = 'Dia berkata: "Hey"';      // Kutip dua di dalam kutip satu
var strE = "Dia berkata: \"Hey\"";    // Kutip dua di dalam kutip dua, pakai escape character (\)
var strF = 'Hari Jum\'at';            // Kutip satu di dalam kutip satu, pakai escape character (\)
var strG = "\u2764 You!"              // Contoh pemakaian Unicode ⇨ Hasilnya: ❤ You!
var strH = `Hello World!`;            // String dengan backtick (Template String ES6)
```

| Escape Characters 	| Kegunaan                                                       	|
|-------------------	|----------------------------------------------------------------	|
| \0                	| Karakter NUL                                                   	|
| \b                	| Backspace                                                      	|
| \t                	| Horizontal tab                                                 	|
| \n                	| Newline                                                        	|
| \v                	| Vertical tab                                                   	|
| \f                	| Form feed                                                      	|
| \r                	| Carriage return                                                	|
| \"                	| Tanda kutip dua (double quote)                                 	|
| \'                	| Tanda kutip satu (apostrophe atau single quote)                	|
| \\                	| Garis miring (backslash)                                       	|
| \xXX              	| Karakter Latin-1 dengan menggunakan dua digit heksa desimal XX 	|
| \uXXXX            	| Karakter Unicode dengan menggunakan empat digit heksa XXXX     	|
| 📚 Bonus           	| Daftar Karakter Latin-1 & Unicode: http://unicode-table.com/   	|

### 𝐃. Boolean

```Javascript
var bolA = true;                      // Bernilai true, biasanya di pakai di if, else, while, dan do while
var bolB = false;                     // Bernilai false, biasanya di pakai di if, else, while, dan do while
```

### 𝐄. Null & Undefined

```Javascript
var nudA = null;                      // Keadaan dimana data "kosong", biasanya sengaja diinput oleh programmer
var nudB = undefined;                 // Keadaan dimana data "tidak terdefinisi", biasanya terjadi karena error
```

#### Kasus yang menghasilkan Undefined:

```Javascript
var und1;
console.log(und1);                    // Output: undefined (Var yang dibuat tanpa langsung diisi nilai, menjadi Undefined)

var und2 = [1, 2, 3];
console.log(und2[3]);                 // Output: undefined (Mengakses Array diluar indeks yang dibuat, menjadi Undefined)

var und3 = {nama: "iyan", umur: 24};
console.log(und3["alamat"]);          // Output: undefined (Mengakses Object diluar key yang dibuat, menjadi Undefined)
```

### 𝐅. Symbol

> 🚧 Tidak dibahas.

### 𝐆. Array

### 𝐇. Object (Bab ...)

### 𝐈. RegExp (Bab ...)

### 𝐉. Date (Bab ...)

### 𝐊. Map & WeakMap

### 𝐋. Set & WeakSet
  
<div id="bab2_2"></div>
  
## 2-2. Operator <a href="#daftar_isi_bab2">🡅</a>
  
> 𝐏𝐞𝐧𝐭𝐢𝐧𝐠 𝐔𝐧𝐭𝐮𝐤 𝐃𝐢𝐤𝐞𝐭𝐚𝐡𝐮𝐢
> > - [X] 𝐀. Operator Precedence
> > - [X] 𝐁. Falsy & Truthy Value
  
> 𝐎𝐩𝐞𝐫𝐚𝐭𝐨𝐫 𝐝𝐢 𝐉𝐚𝐯𝐚𝐒𝐜𝐫𝐢𝐩𝐭
> > - [X] 𝐂. Operator typeof
> > - [X] 𝐃. Operator instanceof (Bab ...)
> > - [X] 𝐄. Operator Aritmatika
> > - [X] 𝐅. Operator Assignment
> > - [X] 𝐆. Operator Increment & Decrement
> > - [X] 𝐇. Operator Perbandingan
> > - [X] 𝐈. Operator Logika
> > - [X] 𝐉. Operator String
> > - [X] 𝐊. Operator Spread
> > - [ ] 𝐋. Operator Bitwise
  
<div id="bab2_3"></div>
  
## 2-3. Struktur Logika <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. If & Else
> - [X] 𝐁. Switch
> - [X] 𝐂. Operator Conditional Ternary
> - [X] 𝐃. Operator Nullish Coalescing
  
<div id="bab2_4"></div>

## 2-4. Perulangan <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. For
> - [X] 𝐁. While
> - [X] 𝐂. Do While
> - [X] 𝐃. For of
> - [X] 𝐄. For in
  
<div id="bab2_5"></div>
  
## 2-5. Function <a href="#daftar_isi_bab2">🡅</a>
  
> 𝐊𝐨𝐧𝐬𝐞𝐩 𝐔𝐭𝐚𝐦𝐚
> > - [X] 𝐀. Function Declaration
> > - [X] 𝐁. Parameter, Argument & Return
> > - [X] 𝐂. Default Parameter
> > - [X] 𝐃. Arguments Object
> > - [X] 𝐄. Rest Parameter
> > - [X] 𝐅. Variable Scope
> > - [X] 𝐆. Var, Let & Const
> > - [X] 𝐇. JavaScript Hoisting

> 𝐅𝐢𝐫𝐬𝐭-𝐂𝐥𝐚𝐬𝐬 𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧
> > - [X] 𝐈. Function Expressions & Anonymous Function
> > - [X] 𝐉. Callback & Higher Order Function
> > - [X] 𝐊. Function as Return Value
  
> 𝐊𝐨𝐧𝐬𝐞𝐩 𝐋𝐚𝐧𝐣𝐮𝐭𝐚𝐧
> > - [X] 𝐋. Inner & Outer Function
> > - [X] 𝐌. Closures (Function)
> > - [X] 𝐍. Factory Function
> > - [X] 𝐎. IImmediately-invoked Function Expression (IIFE)
> > - [X] 𝐏. Arrow Function
  
<div id="bab2_6"></div>
  
## 2-6. Object <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. Object Sebagai Tipe Data
> - [X] 𝐁. Nested Object
> - [X] 𝐂. Object Reference
  
</details>

## ③ 𝒦𝑜𝓃𝓈𝑒𝓅 𝒪𝒪𝒫 🚀 <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
<div id="daftar_isi_bab3"></div>
<br>

| Bab 3                                                      	| Estimasi Baca 	|
|------------------------------------------------------------	|---------------	|
| <a href="#bab3_1">3-1. Object Oriented Programming</a><br> 	| X Menit       	|
| <a href="#bab3_2">3-2. JavaScript Native Object</a>        	| X Menit       	|
| <a href="#bab3_3">3-3. Global Property & Function</a>      	| X Menit       	|
  
<div id="bab3_1"></div>
  
## 3-1. Object Oriented Programming <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Prosedural VS OOP
> - [X] 𝐁. Object Sebagai OOP
> - [X] 𝐂. Pengantar Native Object
  
<div id="bab3_2"></div>
  
## 3-2. JavaScript Native Object <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Number Object
> - [X] 𝐁. Math Object
> - [X] 𝐂. String Object
> - [X] 𝐃. RegExp Object
> - [X] 𝐄. Array Object
> - [X] 𝐅. Date Object

### 𝐀. Number Object

```Javascript
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

### 𝐁. Math Object

```Javascript
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

### 𝐂. String Object

```Javascript
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

### 𝐃. RegExp Object

```Javascript
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

### 𝐄. Array Object

```Javascript
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

let arrSiswa = ["Andri", "Joko", "Sukma", "Rina", "Sari"];  // Contoh ini sama seperti di bab 8 (D3). Kondisi (n<arrSiswa.length)
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

### 𝐅. Date Object

```Javascript
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
  
<div id="bab3_3"></div>
  
## 3-3. Global Property & Function <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Global Property
> - [X] 𝐁. Global Function
  
</details>

## ④ 𝒦𝑜𝓃𝓈𝑒𝓅 𝒟𝒪𝑀 🧩 <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
<div id="daftar_isi_bab4"></div>
<br>
  
| Bab 4                                               	| Estimasi Baca 	|
|-----------------------------------------------------	|---------------	|
| <a href="#bab4_1">4-1. Pengantar DOM</a><br>        	| X Menit       	|
| <a href="#bab4_2">4-2. Window Object</a>            	| X Menit       	|
| <a href="#bab4_3">4-3. Document Object (Part 1)</a> 	| X Menit       	|
| <a href="#bab4_4">4-4. Node Object (Part 1)</a>     	| X Menit       	|
| <a href="#bab4_5">4-5. Document Object (Part 2)</a> 	| X Menit       	|
| <a href="#bab4_6">4-6. Node Object (Part 2)</a>     	| X Menit       	|

<div id="bab4_1"></div>
  
## 4-1. Pengantar DOM <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_2"></div>
  
## 4-2. Window Object <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_3"></div>
  
## 4-3. Document Object (Part 1) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_4"></div>
  
## 4-4. Node Object (Part 1) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_5"></div>
  
## 4-5. Document Object (Part 2) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_6"></div>
  
## 4-6. Node Object (Part 2) <a href="#daftar_isi_bab4">🡅</a>
  
</details>

## ⑤ 𝑀𝑜𝒹𝑒𝓇𝓃 𝒥𝒶𝓋𝒶𝒮𝒸𝓇𝒾𝓅𝓉 🦸‍♂️ <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
</details>

## ⑥ 𝒥𝒶𝓋𝒶𝒮𝒸𝓇𝒾𝓅𝓉 𝐿𝒾𝒷𝓇𝒶𝓇𝒾𝑒𝓈 🤖 <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>
  
</details>
