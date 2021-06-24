```JavaScript
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
```

# JavaScript Mastery

## ① 𝒫𝑒𝓇𝓀𝑒𝓃𝒶𝓁𝒶𝓃 👋

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
| <a href="#bab1_5">1-5. Variabel</a>                  	| X Menit       	|
  
<div id="bab1_1"></div>
  
### 1-1. Kenalan dengan JavaScript <a href="#daftar_isi_bab1">🡅</a>

JavaScript merupakan bagian dari 5 materi dasar web programming, yakni: HTML, CSS, PHP, MySQL dan JavaScript. Bersama-sama dengan HTML dan CSS, ketiganya berbagi peran masing-masing. HTML digunakan untuk membuat struktur dan isi dari halaman web (content). CSS untuk mempercantik tampilan website (design). Sedangkan JavaScript berfungsi menangani interaksi (behavior).“HTML for content, CSS for presentation and JavaScript for behavior”.

<div id="bab1_2"></div>
  
### 1-2. Sejarah & Perkembangan <a href="#daftar_isi_bab1">🡅</a>
  
<div id="bab1_3"></div>
  
### 1-3. Menjalankan Kode <a href="#daftar_isi_bab1">🡅</a>
  
<div id="bab1_4"></div>
  
### 1-4. Aturan Dasar <a href="#daftar_isi_bab1">🡅</a>

<div id="bab1_5"></div>
  
### 1-5. Variabel <a href="#daftar_isi_bab1">🡅</a>
  
</details>

## ② 𝒦𝑜𝓃𝓈𝑒𝓅 𝒟𝒶𝓈𝒶𝓇 👨‍💻

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
  
### 2-1. Tipe Data <a href="#daftar_isi_bab2">🡅</a>
  
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
  
<div id="bab2_2"></div>
  
### 2-2. Operator <a href="#daftar_isi_bab2">🡅</a>
  
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
  
### 2-3. Struktur Logika <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. If & Else
> - [X] 𝐁. Switch
> - [X] 𝐂. Operator Conditional Ternary
> - [X] 𝐃. Operator Nullish Coalescing
  
<div id="bab2_4"></div>

### 2-4. Perulangan <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. For
> - [X] 𝐁. While
> - [X] 𝐂. Do While
> - [X] 𝐃. For of
> - [X] 𝐄. For in
  
<div id="bab2_5"></div>
  
### 2-5. Function <a href="#daftar_isi_bab2">🡅</a>
  
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
  
### 2-6. Object <a href="#daftar_isi_bab2">🡅</a>
  
> - [X] 𝐀. Object Sebagai Tipe Data
> - [X] 𝐁. Nested Object
> - [X] 𝐂. Object Reference
  
</details>

## ③ 𝒦𝑜𝓃𝓈𝑒𝓅 𝒪𝒪𝒫 🚀

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
  
### 3-1. Object Oriented Programming <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Prosedural VS OOP
> - [X] 𝐁. Object Sebagai OOP
> - [X] 𝐂. Pengantar Native Object
  
<div id="bab3_2"></div>
  
### 3-2. JavaScript Native Object <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Number Object
> - [X] 𝐁. Math Object
> - [X] 𝐂. String Object
> - [X] 𝐃. RegExp Object
> - [X] 𝐄. Array Object
> - [X] 𝐅. Date Object

#### 𝐀. Number Object

```JavaScript
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
```

#### 𝐁. Math Object

#### 𝐂. String Object

#### 𝐃. RegExp Object

#### 𝐄. Array Object

#### 𝐅. Date Object
  
<div id="bab3_3"></div>
  
### 3-3. Global Property & Function <a href="#daftar_isi_bab3">🡅</a>
  
> - [X] 𝐀. Global Property
> - [X] 𝐁. Global Function
  
</details>

## ④ 𝒦𝑜𝓃𝓈𝑒𝓅 𝒟𝒪𝑀 🧩

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
  
### 4-1. Pengantar DOM <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_2"></div>
  
### 4-2. Window Object <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_3"></div>
  
### 4-3. Document Object (Part 1) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_4"></div>
  
### 4-4. Node Object (Part 1) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_5"></div>
  
### 4-5. Document Object (Part 2) <a href="#daftar_isi_bab4">🡅</a>
  
<div id="bab4_6"></div>
  
### 4-6. Node Object (Part 2) <a href="#daftar_isi_bab4">🡅</a>
  
</details>

## ⑤ 𝑀𝑜𝒹𝑒𝓇𝓃 𝒥𝒶𝓋𝒶𝒮𝒸𝓇𝒾𝓅𝓉 🦸‍♂️

<details>
<summary>Klik untuk membuka!</summary>
  
</details>

## ⑥ 𝒥𝒶𝓋𝒶𝒮𝒸𝓇𝒾𝓅𝓉 𝐿𝒾𝒷𝓇𝒶𝓇𝒾𝑒𝓈 🤖

<details>
<summary>Klik untuk membuka!</summary>
  
</details>
