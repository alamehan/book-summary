<div id="top"></div>

# The Only Vue.js

Markdown ini ditulis oleh <a href="https://alamehan.github.io/">alamehan.github.io</a>.

## **1. Object Vue** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <!-- Container (mount point), sebagai hasil kompilasi Vue -->
    <div id="app">
      <h1>Name: {{ name }}</h1> <!-- Cara 1 -->
      <h1>Age: {{ age }}</h1>
      <h1>{{ `Gender (Pria): ${gender}` }}</h1> <!-- Cara 2 -->
      <h1>{{ `Hobby: ${hobby[0]} ${hobby[1]}` }}</h1>
      <h1>{{ `Children: ${children[1]} & ${children[2]}` }}</h1>
    </div>

    <script>
      // Inisiasi object Vue (yang disimpan ke dalam variable vm)
      vm = new Vue({
        el: '#app',   // el merupakan property
        data: {       // begitupula dengan data
          name: 'Raihan Allaam',
          age: 30,
          gender: true,
          hobby: ['Design', 'Coding', 'Reading'],
          children: {
            1: 'Said',
            2: 'Nabila',
            3: 'Aisyah',
          },
        },
      });
    </script>
  </body>
</html>
```

Mengakses Properti didalam Object Vue menggunakan ```this.$data.name``` atau bisa langsung ```this.name```. Mengakses Properti diluar Object Vue menggunakan ```vm.$data.name``` atau bisa langsung ```vm.name```. Selain mount ditulis dengan cara:

```Javascript
vm = new Vue({ 
  el: '#app' ,
  ...
})
```

Bisa juga dengan cara berikut:

```Javascript
vm = new Vue({
  ...
})
vm.$mount('#app')
```

</details>

## **2. Siklus Object Vue** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app">
      <h1>{{ message }}</h1>
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          message: 'Hello World!',
        },
        beforeCreate() {
          console.log(`1. Before Create: message = ${this.message}`);
        },
        created() {
          console.log(`2. Created: message = ${this.message}`);
        },
        beforeMount() {
          console.log(`3. Before Mount: el = ${this.$el.textContent}`);
        },
        mounted() {
          console.log(`4. Mounted: el = ${this.$el.textContent}`);
        },
        beforeUpdate() {
          console.log(`5. Before Update: el = ${this.$el.textContent}`);
        },
        updated() {
          console.log(`6. Updated: el = ${this.$el.textContent}`);
        },
        beforeDestroy() {
          console.log(`7. Before Destroy`);
        },
        destroyed() {
          console.log(`8. Destroyed`);
        },
      });

      // Jika perintah di bawah ini diaktifkan, HOOK 5 & 6 akan ke-trigger
      // vm.message = 'Selamat Datang!';

      // Jika perintah di bawah ini diaktifkan, HOOK 7 & 8 akan ke-trigger
      // vm.$destroy()
    </script>
  </body>
</html>
```

Gunakan Console di Developer Tools-nya Google Chrome. Siklus Object Vue terdiri dari CREATE-MOUNT-UPDATE-DESTROY:
1. HOOK 1: ```beforeCreate()``` ➜ Belum bisa mengakses variabel message
2. HOOK 2: ```created()``` ➜ Sudah bisa mengakses & memanipulasi variabel message
3. HOOK 3: ```beforeMount()``` ➜ Sudah bisa mengakses DOM, namun Data belum dirender dengan Template
4. HOOK 4: ```mounted()``` ➜ Sudah bisa mengakses DOM & Data sudah dirender dengan Template
5. HOOK 5: ```beforeUpdate()``` ➜ Disini variabel message masih bernilai 'Hello World!' Padahal sudah diupdate dengan perintah vm.message = "Selamat Datang!" (lihat dibawah Object Vue ini)
6. HOOK 6: ```updated()``` ➜ Disini variabel message sudah terupdate menjadi 'Selamat Datang!'
7. HOOK 7: ```beforeDestroy()``` ➜ Terjadi sebelum Component dihapus
8. HOOK 8: ```destroyed()``` ➜ Terjadi setelah Object Vue dihapus

Nantinya masing-masing hook dapat dimanfaatkan untuk menjalankan suatu perintah tertentu.

</details>

## **3. Penulisan Template** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .title {
        color: green;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <h1>{{ message }}</h1> <!-- Baca data text -->
      <h1 v-once>{{ message }}</h1> <!-- Agar nilai tidak dapat diubah -->
      <h1 v-html="message_html"></h1> <!-- Baca data RAW HTML -->
      <h1 v-bind:class="class_h1">{{ message }}</h1> <!-- Baca data attribute -->
      <h1 :class="class_h1">{{ message }}</h1> <!-- Shorthand untuk v-bind -->
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          message: 'Hello World!', // Data text
          message_html: "<span style='color:red'>Hello World!</span>", // Data RAW HTML
          class_h1: 'title', // Data attribute (class CSS)
        },
      });
    </script>
  </body>
</html>
```

Template Vue (mustache ```{{ ... }}```) mendukung JavaScript Expressions, seperti ```{{ `Diskon: ${total * 10%}` }}```, ```{{ ok ? 'YES' : 'NO' }}```, ```{{ message.split('').reverse().join('') }}```. Atau jika dalam bentuk atribut HTML maka penulisannya dengan cara di-binding, contohnya sebagai berikut ```<h1 :id="'product-'+index"></h1>```.

</details>

## **4. Properti Template** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app"></div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          message1: 'Hello World!',
          message2: 'Halo Dunia!',
        },
        template: `<h1>{{ message1 }}</h1>`, // Properti Template
        render(createElement) { // Method Render
          return createElement('h1', this.message2);
        },
      });
    </script>
  </body>
</html>
```

Properti Template: Sejauh ini kita menulis template langsung di kode HTML. Namun Vue juga menyediakan cara lain untuk mendefinisikan Template yang menyatu dengan Object Vue itu sendiri, melalui Properti ```template```.

Method Render: Alternatif lain kita bisa juga menggunakan Method Render yang berfungsi menampilkan konten yang didefinisikan.

Catatan: Dalam contoh diatas Method Render mengembalikan fungsi ```createElement``` untuk menciptakan elemen HTML ```h1``` yang berisi nilai dari variabel ```message2```. Jika Properti Template & Method Render dua-duanya ada, maka Properti Template diabaikan.

</details>

## **5. Properti Lainnya** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <div id="app">
      <!-- Implementasi properti methods -->
      <h1>{{ counter }}</h1>
      <button onclick="vm.decrement()">-</button>
      <button onclick="vm.increment()">+</button><hr>

      <!-- Implementasi properti computed -->
      {{ fullName }}<hr>

      <!-- Implementasi properti filters -->
      <h1>Upper: {{ message | upper() }}</h1> <!-- Atau bisa juga hanya 'upper' saja -->
      <h1>Reverse: {{ message | reverse }}</h1>
      <h1>Upper & Reverse: {{ message | upper | reverse }}</h1><hr>
      <h1>{{ price | formatCurrency('USD') }}</h1>
      <h1>{{ price | formatCurrency('IDR') }}</h1>
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          counter: 0,
          firstName: 'Raihan',
          lastName: 'Allaam',
          message: 'Hello World!',
          price: 500000,
        },

        methods: { // Properti methods
          increment() {
            this.counter++;
          },
          decrement() {
            this.counter--;
          },
        },

        computed: { // Properti computed
          fullName() {
            return `${this.firstName} ${this.lastName}`;
          },
        },

        filters: { // Properti filters
          upper(text) {
            return text.toUpperCase();
          },
          reverse(text) {
            return text.split('').reverse().join('');
          },
          formatCurrency(value, currency) {
            var formatter = new Intl.NumberFormat('id-ID', {
              style: 'currency',
              currency: currency,
              minimumFractionDigits: 2,
            });
            return formatter.format(value);
          },
        },
      });
    </script>
  </body>
</html>
```

Properti methods: Cocok untuk kasus jika ada Action/Event yang memanggil fungsi. Contohnya: fungsi untuk mengevaluasi suatu nilai, menampilkan pesan, mengubah variabel, dll.

Properti computed: Cocok untuk kasus mengembalikan nilai (Return Value), memakai/bergantung pada property data yang didefinisikan. Meskipun bentuknya fungsi, namun fungsi pada Computed tidak memiliki parameter dan oleh Vue tidak dianggap sebagai fungsi. Artinya kita tidak bisa memanggilnya dengan ```this.fullName()``` melainkan ```this.fullName``` layaknya variabel. Jadi Computed ini tepat digunakan sebagai variabel yang nilainya berasal dari variabel lain.

Properti filters: Cocok untuk kasus memanipulasi tampilan/format text pada suatu Template. Filter ditulis dengan menggunakan simbol ```|``` atau "pipe". Hal ini berbeda dengan Methods: ```vm.upper()``` & Computed: ```vm.fullName```, Filters tidak bisa dipanggil dari Object Vue.

Catatan: Deklarasi Filters juga bisa dilakukan diluar Object Vue (terpisah), contoh:

```Javascript
Vue.filter('upper', function(value) {
  return value.toUpperCase()
}) 
var vm = new Vue({
  // ...
})
```

</details>

## **6. Directive** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

Directive merupakan atribut khusus yang disematkan pada elemen atau markup HTML sebagai penanda bahwa elemen DOM tersebut akan dikenai perlakuan tertentu oleh Vue.

1. ```v-html:``` ➜ Untuk menampilkan data berupa kode HTML.
2. ```v-text:``` ➜ Untuk menampilkan string biasa, sama dengan mustache ```{{ }}```.
3. ```v-once:``` ➜ Agar nilai variabel pada template tidak bisa diubah-ubah lagi (constant).
4. ```v-show:``` ➜ Untuk show/hide suatu elemen DOM. Dibalik layar pakai properti ```display``` pada CSS.
5. ```v-if:```, ```v-else-if```:, ```v-else```: ➜ Untuk merender/tidak merender suatu elemen DOM.
6. ```v-on:``` ➜ Berperan sebagai sebuah event listener pada elemen HTML/komponen Vue.
7. ```v-bind:``` ➜ Untuk mem-binding atribut HTML/komponen agar nilainya terupdate secara reactive sesuai dengan datanya.

Catatan:
1. Penulisan directive ```v-on:``` dapat disingkat menjadi ```@```
2. Penulisan directive ```v-bind:``` dapat disingkat menjadi ```:```

Ragam directive event:
1. ```@click``` ➜ Ketika mouse diklik
2. ```@mouseover``` ➜ Ketika mouse berada di area elemen
3. ```@mouseenter``` ➜ Ketika mouse masuk ke area elemen
4. ```@mouseout``` ➜ Ketika mouse keluar dari area elemen
5. ```@mousedown``` ➜ Sama dengan ```v-on:click```
6. ```@keyup``` ➜ Ketika keyboard up pada elemen (biasanya digunakan pada elemen input)
7. ```@keydown``` ➜ Ketika keyboard down pada elemen (biasanya digunakan pada elemen input)
8. ```@submit``` ➜ Ketika form di submit

Ragam modifier:
1. ```.once``` ➜ hanya boleh dilakukan sekali saja (misalnya klik, enter, dll)
2. ```.prevent``` ➜ Modifier ini berfungsi agar halaman tidak di-redirect
3. ```.enter``` ➜ Modifier ini akan bereaksi ketika keyboard Enter ditekan
4. ```.tab``` ➜ Modifier ini akan bereaksi ketika keyboard Tab ditekan
5. ```.delete``` ➜ mMdifier ini akan bereaksi ketika keyboard Delete atau Backspace ditekan
6. ```.esc``` ➜ Modifier ini akan bereaksi ketika keyboard Escape ditekan
7. ```.space``` ➜ Modifier ini akan bereaksi ketika keyboard Spasi ditekan
8. ```.native``` ➜ Modifier ini akan listen native event pada elemen root dari komponen
9. ```.ctrl``` ➜ Modifier ini akan bereaksi ketika keyboard Ctrl ditekan
10. ```.alt``` ➜ Modifier ini akan bereaksi ketika keyboard Alt ditekan
11. ```.shift``` ➜ Modifier ini akan bereaksi ketika keyboard Shift ditekan

Kita juga bisa menangani klik kiri/kanan/tengah pada mouse dengan modifier ```.left```, ```.right```, dan ```.middle```.
  
Sejak versi 2.5.0+, Vue menambahkan modifier ```.exact``` untuk memastikan bahwa event hanya akan dijalankan ketika key tersebut saja yang diklik. Dalam contoh (lihat di bawah) Button tanpa modifier ```.exact``` akan menjalankan ```info()``` ketika SHIFT ditekan meskipun saat yang bersamaan ALT/dll juga di tekan. Sedangkan Button dengan modifier ```.exact``` akan menjalankan ```info()``` HANYA ketika SHIFT ditekan, tidak menekan key lainnya.

> ⚠️ Source code di bawah ini menggunakan assets gambar

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .title {
        color: green;
        font-weight: bold;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <p v-html="message_html"></p> <!-- 1. v-html -->
      <p v-text="message_text "></p> <!-- 2. v-text -->
      <p v-once>{{ message_text }}</p> <!-- 3. v-once -->
      <p v-show="displayMessage">Message Show {{ message_show }}</p> <!-- 4. v-show -->
      <hr>

      <!-- 5. v-if, v-else-if, v-else -->
      <div v-if="content">
        <h2>Judul</h2>
        <p>Paragraph 1</p>
        <p>Paragraph 2</p>
        <div>
          <div v-if="nilai === 'A'">Sempurna</div>
          <div v-else-if="nilai === 'B'">Bagus</div>
          <div v-else-if="nilai === 'C'">Cukup</div>
          <div v-else>Kurang</div>
        </div>
      </div>
      <hr>

      <!-- 6. v-on -->
      <p>Jumlah Klik: {{ counter }}x</p>
      <button v-on:click="counter += 1">Counter</button><br>
      <button v-on:click="info('Selamat Datang!')">Alert</button>
      <button @click.once="info('1X Klik Saja')">Alert + Modifier .once</button>
      <hr>
      <a href="http://google.com" @click="info('Go to link')">Tanpa Prevent</a><br>
      <a href="http://google.com" @click.prevent="info('Hold!')">Dengan Prevent</a><br>
      <hr>
      <input @keyup.enter="info('BOOOM! ' + $event.target.value)" value="Tekan enter" /><br>
      <button @click.ctrl="info('BOOOM!')">CTRL + CLICK</button>
      <br>
      <button @click.shift="info('BOOOM!')">SHIFT + CLICK</button>
      <button @click.shift.exact="info('BOOOM!')">SHIFT + CLICK</button>
      <br>
      <button @click.left="info('BOOOM!')">Klik Kiri</button>
      <button @click.right="info('BOOOM!')">Klik Kanan</button>
      <button @click.middle="info('BOOOM!')">Klik Tengah</button>
      <br>

      <!-- 7. v-bind -->
      <img v-bind:src="`assets/${imageSrc}`" />
      <div :class="classA">BINDING! STYLE CSS!</div>
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          message_html: "<span style='color:red'>Hello HTML!</span>",
          message_text: 'Hello World!',
          message_show: 'ON',
          displayMessage: true, // Coba ganti dengan false
          content: true, // Coba ganti dengan false
          nilai: 'A',
          counter: 0,
          imageSrc: 'logo1.png',
          classA: 'title',
        },
        methods: {
          info(text) {
            alert(text);
          },
        },
      });

      // Update data message (tidak berpengaruh pada v-once)
      vm.message_text = 'Halo Dunia! (Updated)';

      // Dalam 3 detik, 'logo1.png' akan berubah menjadi 'logo2.png'
      setTimeout(() => {
        vm.imageSrc = 'logo2.png';
      }, 3000);
    </script>
  </body>
</html>
```

Contoh ```v-bind``` lainnya:

```HTML
<a :href="url"></a>
<img :src="'images/' + imageSrc">
<div :class="[classA, classB]"></div>
<div :class="{ red: isRed }"></div>
<div :style="{ fontSize: size + 'px' }"></div>
<img v-bind="{ id: imageID, src: imageSrc }" />
```

</details>

## **7. Dynamic Argument** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

Sejak versi 2.6.0, kita bisa menggunakan argumen dinamis pada sebuah directive:

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .title {
        color: red;
        font-weight: bold;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <button v-on:click="info('Hello World!')">Button 1</button>
      <button v-on:[nama_event]="info('Hello World!')">Button 2</button> <!-- Dinamis -->
      <br>
      <button @click="info('Hello World!')">Button 3</button>
      <button @[nama_event]="info('Hello World!')">Button 4</button> <!-- Dinamis -->
      <hr>
      <div v-bind:class="classA">STANDARD 1</div>
      <div v-bind:[nama_atribut]="classA">DYNAMIC 1</div> <!-- Dinamis -->
      <br>
      <div :class="classA">STANDARD 2</div>
      <div :[nama_atribut]="classA">DYNAMIC 2</div> <!-- Dinamis -->
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          nama_event: 'click', // Coba ganti dengan "mouseover"
          nama_atribut: 'class', // Coba ganti dengan "style"
          classA: 'title',
        },
        methods: {
          info(text) {
            alert(text);
          },
        },
      });
    </script>
  </body>
</html>
```

</details>

## **8. List** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

Data dalam bentuk list/daftar yang bisa berupa array, objek atau collection (array dari objek) bisa kita tampilkan dengan mudah menggunakan Vue. Vue mempunyai directive v-for yang berfungsi untuk melakukan perulangan.

> ⚠️ Source code di bawah ini menggunakan assets gambar

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app">
      <!-- 1A. Menampilkan data Array -->
      <ul>
        <li v-for="buku in books_array">{{ buku }}</li><br>
      </ul>

      <!-- 1B. Menampilkan data Array + Index -->
      <ul>
        <li v-for="(buku, index) in books_array">{{ `${index+1}: ${buku}` }}</li><br>
      </ul>

      <!-- 1C. Menggunakan tag template (Array) -->
      <ul>
        <template v-for="buku in books_array">
          <li>{{ buku }}</li>
        </template>
      </ul>
      <hr>

      <!-- 2A. Menampilkan data Object -->
      <ul>
        <li v-for="buku of books_object">{{ buku }}</li><br>
      </ul>

      <!-- 2B. Menampilkan data Object + Key -->
      <ul>
        <li v-for="(buku, key) of books_object">{{ `${key}: ${buku}` }}</li><br>
      </ul>

      <!-- 2C. Menggunakan tag template (Object) -->
      <ul>
        <template v-for="buku of books_object">
          <li>{{ buku }}</li>
        </template>
      </ul>
      <hr>

      <!-- 3A. Menampilkan data Collection -->
      <table border=1>
        <tr v-for="buku of books_collection">
          <td>
            <img :src="`assets/${buku.img}`" width="100">
          </td>
          <td>
            {{ `ID: ${buku.id}` }}<br>
            {{ `Judul: ${buku.judul}` }}<br>
            {{ `Harga: ${buku.harga}` }}<br>
          </td>
        </tr>
      </table>
      <hr>

      <!-- 3B. Menampilkan data Collection + Kondisi -->
      <table border=1>
        <tr v-for="buku of books_collection" v-if="buku.harga>60000">
          <td>
            <img :src="`assets/${buku.img}`" width="100">
          </td>
          <td>
            {{ `ID: ${buku.id}` }}<br>
            {{ `Judul: ${buku.judul}` }}<br>
            {{ `Harga: ${buku.harga}` }}<br>
          </td>
        </tr>
      </table>
      <hr>

      <!-- 3C. Menampilkan data Collection + Filter -->
      <table border=1>
        <tr v-for="buku of lebihDari70Ribu">
          <td>
            <img :src="`assets/${buku.img}`" width="100">
          </td>
          <td>
            {{ `ID: ${buku.id}` }}<br>
            {{ `Judul: ${buku.judul}` }}<br>
            {{ `Harga: ${buku.harga}` }}<br>
          </td>
        </tr>
      </table>
      <hr>
    </div>

    <script>
      vm = new Vue({
        el: '#app',
        data: {
          books_array: ['Buku A', 'Buku B', 'Buku C', 'Buku D'],

          books_object: {
            id: 99,
            judul: 'Buku Koding',
            harga: 50000
          },

          books_collection: [
            { id: 1, judul: 'Buku Koding A', harga: 50000, img: 'cover-1.jpg' },
            { id: 2, judul: 'Buku Koding B', harga: 60000, img: 'cover-2.jpg' },
            { id: 3, judul: 'Buku Koding C', harga: 70000, img: 'cover-3.jpg' },
            { id: 4, judul: 'Buku Koding D', harga: 80000, img: 'cover-4.jpg' },
          ]
        },

        computed: {
          lebihDari70Ribu() {
            return this.books_collection.filter((buku) => {
              return buku.harga > 70000
            })
          }
        }
      });

      // 4A. Mengubah data pada Array
      vm.$set(vm.books_array, 1, 'Buku B (NEW)');

      // 4B. Mengubah data pada Object
      vm.$set(vm.books_object, 'judul', 'Buku Koding (NEW)')
    </script>
  </body>
</html>
```

</details>

## **9. Form** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

**⚠️ BELUM DIRANGKUM ⚠️**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <!-- ⚠️ Kode HTML disimpan disini -->

    <script>
      /* ⚠️ Script (Vue) disimpan disini */
    </script>
  </body>
</html>
```

</details>

## **10. Components** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>

### **👉 10-1. Global Component**

Bisa dipakai di mana saja, di ```<div id="app1">...</div>```, ```<div id="app2">...</div>```, dst.

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app1">
      <component-a></component-a>
      <component-b></component-b>
    </div>

    <script>
      Vue.component('component-a', {
        template: `<h1>Component A</h1>`
      })

      Vue.component('component-b', {
        data() {
          return {
            message: 'Component B'
          }
        },
        template: `<h1>{{ message }}</h1>`
      })

      new Vue({
        el: '#app1'
      })
    </script>
  </body>
</html>
```

### **👉 10-2. Local Component**

Hanya bisa dipakai di ```<div id="app1">...</div>```, sesuai dengan yang ditargetkan.

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app2">
      <component-c></component-c>
      <component-d></component-d>
      <component-e></component-e>
    </div>

    <script>
      var ComponentC = {
        template: `<h1>Component C</h1>`,
      }

      var ComponentD = {
        data() {
          return {
            message: 'Component D'
          }
        },
        template: `<h1>{{ message }}</h1>`
      }

      new Vue({
        el: '#app2',
        data: {
          message: "Component F"
        },
        components: {
          // "Import" component dari luar ke dalam Object Vue
          'component-c': ComponentC,
          'component-d': ComponentD,

          // Atau langsung dibuat di dalam Object Vue pun bisa. Namun kekurangannya tidak 
          // bisa menggunakan data melalui {{ message }} maupaun {{ this.message }}, jadi
          // hanya berupa template HTML saja. Dan sebagai catatan, template harus dibungkus
          // dengan menggunakan 1 tag terluar, misalnya <div> ...konten... </div>.
          'component-e': {
            template: `
                <div>
                  <h1>Component E</h1>
                </div>
              `
          }, 
        }
      })
    </script>
  </body>
</html>
```

### **👉 10-3. Kirim Data ke Component (Props) - Hardcode**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        height: 280px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app3">
      <book judul="Buku A" deskripsi="Koding Easy" img="cover-1.jpg"></book>
      <book judul="Buku B" deskripsi="Design Easy" img="cover-2.jpg"></book>
    </div>

    <script>
      var BookComponent1 = {
        data() {
          return {
            classCard: 'card'
          }
        },
        props: ['judul', 'deskripsi', 'img'], // Note: Tidak bisa menggunakan CamelCase
        template: `
          <div :class=" classCard">
            <h3>{{ judul }}</h3>
            <img :src="'assets/'+img" width=100>
            <p v-html="deskripsi"></p>
          </div>
        `
      }

      new Vue({
        el: '#app3',
        components: {
          'book': BookComponent1,
        }
      })
    </script>
  </body>
</html>
```

### **👉 10-4. Kirim Data ke Component (Props) - Dinamis**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        height: 280px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app4">
      <book v-for="buku in books_collection" :key="buku.id" :judul="buku.judul" :deskripsi="buku.deskripsi" :img="buku.img"></book>
    </div>

    <script>
      var BookComponent1 = {
        data() {
          return {
            classCard: 'card'
          }
        },
        props: ['judul', 'deskripsi', 'img'], // Note: Tidak bisa menggunakan CamelCase
        template: `
          <div :class=" classCard">
            <h3>{{ judul }}</h3>
            <img :src="'assets/'+img" width=100>
            <p v-html="deskripsi"></p>
          </div>
        `
      }

      new Vue({
        el: '#app4',
        components: {
          'book': BookComponent1,
        },
        data: {
          books_collection: [
            { id: 1, judul: 'Buku A', deskripsi: "Koding Easy", img: 'cover-1.jpg' },
            { id: 2, judul: 'Buku B', deskripsi: "Design Easy", img: 'cover-2.jpg' },
            { id: 3, judul: 'Buku C', deskripsi: "Gaming Easy", img: 'cover-3.jpg' },
            { id: 4, judul: 'Buku D', deskripsi: "Living Easy", img: 'cover-4.jpg' },
          ]
        }
      })
    </script>
  </body>
</html>
```

### **👉 10-5. Update Data Parent dari Component**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        height: 280px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app5">
      <h1>Selected: {{ selected_book }}</h1>
      <book v-for="buku in books_collection" :key="buku.id" :book="buku" @dipilih="selected_book = $event"></book>
    </div>

    <script>
      var BookComponent2 = {
        data() {
          return {
            classCard: 'card'
          }
        },
        props: ['book'],
        template: `
          <div :class="classCard">
            <h3>{{ book.judul }}</h3>

            <img :src="'assets/'+book.img" width=100>
            <p v-html="book.deskripsi"></p>
            <p>Rp.{{ book.harga }}</p><br>
            
            <button @click="$emit('dipilih', book.judul)">Select</button>
          </div>
        `
        // @click="$emit('dipilih', book.judul)" ➜ Saat di klik, nilai "book.judul" akan di-emit/
        // di-set ke event "dipilih", dengan demikian @dipilih="selected_book = $event" ➜ (di HTML)
        // artinya selected_book diisi dengan nilai dari $event, yaitu "book.judul".
      }

      new Vue({
        el: '#app5',
        components: {
          'book': BookComponent2,
        },
        data: {
          books_collection: [
            { id: 1, judul: 'Buku A', deskripsi: "Koding Easy", harga: 50000, img: 'cover-1.jpg' },
            { id: 2, judul: 'Buku B', deskripsi: "Design Easy", harga: 60000, img: 'cover-2.jpg' },
            { id: 3, judul: 'Buku C', deskripsi: "Gaming Easy", harga: 70000, img: 'cover-3.jpg' },
            { id: 4, judul: 'Buku D', deskripsi: "Living Easy", harga: 80000, img: 'cover-4.jpg' },
          ],
          selected_book: '',
        }
      })
    </script>
  </body>
</html>
```

### **👉 10-6. Two Way Data Binding di Component**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>
    <div id="app6">
      <h1>{{ searchText }}</h1>
      <custom-input :value="searchText" @input="searchText = $event"></custom-input> <!-- CARA RIBET -->
      <custom-input v-model="searchText"></custom-input> <!-- CARA MUDAH -->
    </div>

    <script>
      Vue.component('custom-input', {
        props: ['value'],
        template: `
          <input :value="value" @input="$emit('input', $event.target.value)">
        `
      })

      new Vue({
        el: '#app6',
        data: {
          searchText: "Contoh"
        }
      })
    </script>
  </body>
</html>
```

### **👉 10-7. Kirim Konten ke dalam Component (Slots)**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        height: 120px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app7">
      <!-- Bagian A -->
      <kartu-a>
        <p>Tag p ini menimpa slots</p>
      </kartu-a>
      <kartu-a>
        <h4>Tag h4 ini menimpa slots</h4>
        <h5>Tag h5 ini juga menimpa slots</h5>
      </kartu-a>

      <!-- Bagian B -->
      <kartu-b></kartu-b> <!-- Diisi konten default -->
      <kartu-b>Hello Wolrd!</kartu-b> <!-- Konten default tertimpa -->

      <!-- Bagian C -->
      <!-- Jika multiple slots, bungkus dulu menggunakan template -->
      <kartu-c>
        <template v-slot:judul>
          <h4>Ini Judul</h4>
        </template>
        <template #isi>
          <!-- # merupakan shorthand untuk v-slot: -->
          <h4>Ini Isi</h4>
        </template>
      </kartu-c>

      <!-- Bagian D -->
      <!-- Jika single slots, tidak perlu dibungkus template -->
      <kartu-d #judul></kartu-d> <!-- Diisi konten default -->
      <kartu-d #judul>Bandung</kartu-d> <!-- Konten default tertimpa -->
    </div>

    <script>
      // A. Elemen <slot></slot> akan di-replace/di-timpa
      // dengan konten di component (di HTML)
      Vue.component('kartu-a', {
        template: `
          <div class="card">
            <strong>Informasi A</strong>
            <hr>
            <slot></slot>
          </div>
        `
      })

      // B. Jika di component (di HTML) tidak membuat konten
      // tertentu maka akan diisi oleh konten default slots
      Vue.component('kartu-b', {
        template: `
          <div class="card">
            <strong>Informasi B</strong>
            <hr>
            <slot>Ini menjadi konten default</slot>
          </div>
        `
      })

      // C. Multiple slots ditulis dengan menyertakan
      // atribut "name" di dalam tag slot
      Vue.component('kartu-c', {
        template: `
          <div class="card">
            <strong>Informasi C</strong>
            <hr>
            <slot name="judul">Judul Default</slot>
            <slot name="isi">Isi Default</slot>
          </div>
        `
      })

      // D. Mengakses property data dari component
      // pada slots harus di-binding terlebih dahulu
      Vue.component('kartu-d', {
        data() {
          return {
            message: "Hello"
          }
        },
        template: `
          <div class="card">
            <strong>Informasi D</strong>
            <hr>
            <slot name="judul" :defaultJudul="message">{{ message }}</slot>
          </div>
        `
      })

      new Vue({
        el: '#app7'
      })
    </script>
  </body>
</html>
```

### **👉 10-8. Dynamic Components**

Idenya: Kita memuat suatu component yang sudah diregister secara dinamis, atau hanya akan kita muat jika diperlukan saja.

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app8">
      <button @click="currentComponent='item-a'">Item A</button>
      <button @click="currentComponent='item-b'">Item B</button>
      <button @click="currentComponent='item-c'">Item C</button>
      <button @click="currentComponent='item-d'">Item D</button>
      <hr>
      <!-- <component> memiliki directive v-bind:is untuk memantau pergantian component yang dimuat -->
      <component :is="currentComponent"></component>
    </div>

    <script>
      var itemA = {
        template: `
          <div class="card">
            <strong>Isi Item A ...</strong>
          </div>
        `
      }

      var itemB = {
        template: `
          <div class="card">
            <strong>Isi Item B ...</strong>
          </div>
        `
      }

      var vm = new Vue({
        el: '#app8',
        data: {
          currentComponent: 'item-a' // Isi dengan nilai default, atau bisa juga dikosongkan.
        },
        components: {
          'item-a': itemA,
          'item-b': itemB,
          'item-c': {
            template: `
              <div class="card">
                <strong>Isi Item C ...</strong>
              </div>
            `
          },
          'item-d': {
            template: `
              <div class="card">
                <strong>Isi Item D ...</strong>
              </div>
            `
          },
        }
      })
    </script>
  </body>
</html>
```

</details>

## **11. Transition Effect** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

Efek animasi transisi bawaan Vue, pada contoh di bawah ini merupakan animasi pergantian component.

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        float: left;
      }

      .component-fade-enter-active,
      .component-fade-leave-active {
        transition: opacity .3s ease;
      }

      .component-fade-enter,
      .component-fade-leave-to {
        opacity: 0;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <button @click="currentComponent='item-a'">Item A</button>
      <button @click="currentComponent='item-b'">Item B</button>
      <hr>
      <transition name="component-fade" mode="out-in">
        <component :is="currentComponent"></component>
      </transition>
      <!-- Coba ganti "out-in" menjadi "in-out", lalu lihat efeknya -->
    </div>

    <script>
      var itemA = {
        template: `
          <div class="card">
            <strong>Isi Item A ...</strong>
          </div>
        `
      }

      var itemB = {
        template: `
          <div class="card">
            <strong>Isi Item B ...</strong>
          </div>
        `
      }

      var vm = new Vue({
        el: '#app',
        data: {
          currentComponent: 'item-a',
        },
        components: {
          'item-a': itemA,
          'item-b': itemB,
        }
      })
    </script>
  </body>
</html>
```

</details>

## **12. Mixins** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

Mixins: Reusable data, methods, template, etc. Saat Object Vue atau Component menggunakan mixins maka semua option (data, methods, template, dll) dari mixin tersebut akan digabungkan ke dalam Component yang menggunakannya tersebut.

### **👉 12-1. Konsep Dasar**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  </head>

  <body>

    <script>
      var MixinHello = {
        data(){
          return{
            message: "hello from mixin",
            foo: "abc"
          }
        },
        methods: {
          pagi(){
            console.log("Selamat pagi!");
          },
          sore(){
            console.log("Selamat sore!");
          }
        }
      }

      var vm1 = new Vue({
        mixins: [MixinHello], // "Import" option dari MixinHello
        data(){
          return{
            message: "hello from vm1",
            bar: "def"
          }
        },
        methods: {
          siang(){
            console.log("Selamat siang!");
          },
        }
      })

      console.log(vm1.message) // Output: hello from vm1  (karena conflict, akan diambil yang asli)
      console.log(vm1.foo)     // Output: abc             (berasal dari mixins)
      console.log(vm1.bar)     // Output: def

      vm1.pagi()   // Output: Selamat pagi!  (berasal dari mixins)
      vm1.sore()   // Output: Selamat sore!  (berasal dari mixins)
      vm1.siang()  // Output: Selamat siang!

      var vm2 = new Vue({
        mixins: [MixinHello], // "Import" option dari MixinHello
        data(){
          return{
            bar: "def"
          }
        },
        methods: {
          malam(){
            console.log("Selamat malam!");
          }
        }
      })

      console.log(vm2.message) // Output: hello from mixin  (berasal dari mixins)
      console.log(vm2.foo)     // Output: abc               (berasal dari mixins)
      console.log(vm2.bar)     // Output: def

      vm2.pagi()   // Output: Selamat pagi!  (berasal dari mixins)
      vm2.sore()   // Output: Selamat sore!  (berasal dari mixins)
      vm2.malam()  // Output: Selamat malam!
    </script>
  </body>
</html>
```

### **👉 12-2. Implementasi di Component (Global)**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <component-a ></component-a>
      <component-b data_props="Ini dari props"></component-b>
    </div>

    <script>
      MixinHeader = {
        data() {
          return {
            dataMixinA: 'Header',
            dataMixinB: 'Body',
          };
        },
        provide() { 
          return { 
            child: this 
          } 
        },
        components: {
          super: {
            inject: ['child'],
            template: `
              <div class="card">
                <h4>{{ child.dataMixinA }}</h4>
                <hr>
                <slot></slot>
              </div>`,
          }
          // <slot></slot> nantinya akan di-timpa
        },
      }

      Vue.component('component-a', {
        mixins: [MixinHeader],
        data(){
          return{
            message: "Coding Lover"
          }
        },
        template: `
          <super>
            <h6>{{ dataMixinB }}</h6>
            <h6>{{ message }}</h6>
          </super>
        `
        // <super></super> dan isi kontennya menimpa <slot></slot> di MixinHeader
      })

      Vue.component('component-b', {
        mixins: [MixinHeader],
        data(){
          return{
            message: "Design Lover"
          }
        },
        created() {
          this.dataMixinA = "Header New"; // Menimpa "dataMixinA" dari MixinHeader
          this.dataMixinB = "Body New";   // Menimpa "dataMixinB" dari MixinHeader
        },
        props: ["data_props"],            // Menggunakan props
        template: `
          <super>
            <h6>{{ dataMixinB }}</h6>
            <h6>{{ data_props }}</h6>
            <h6>{{ message }}</h6>
          </super>
        `
      })

      var vm = new Vue({
        el: '#app'
      });
    </script>
  </body>
</html>
```

### **👉 12-3. Implementasi di Component (Local)**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      .card {
        background: #efefef;
        border: 1px solid #ddd;
        margin: 3px;
        padding: 6px;
        float: left;
      }
    </style>
  </head>

  <body>
    <div id="app">
      <component-c ></component-c>
      <component-d data_props="Ini dari props"></component-d>
    </div>

    <script>
      MixinHeader = {
        data() {
          return {
            dataMixinA: 'Header',
            dataMixinB: 'Body',
          };
        },
        provide() { 
          return { 
            child: this 
          } 
        },
        components: {
          super: {
            inject: ['child'],
            template: `
              <div class="card">
                <h4>{{ child.dataMixinA }}</h4>
                <hr>
                <slot></slot>
              </div>`,
          }
          // <slot></slot> nantinya akan di-timpa
        },
      }

      var ComponentC = Vue.extend({
        mixins: [MixinHeader],
        data(){
          return{
            message: "Coding Lover"
          }
        },
        template: `
          <super>
            <h6>{{ dataMixinB }}</h6>
            <h6>{{ message }}</h6>
          </super>
        `
        // <super></super> dan isi kontennya menimpa <slot></slot> di MixinHeader
      })

      var ComponentD = Vue.extend({
        mixins: [MixinHeader],
        data(){
          return{
            message: "Design Lover"
          }
        },
        created() {
          this.dataMixinA = "Header New"; // Menimpa "dataMixinA" dari MixinHeader
          this.dataMixinB = "Body New";   // Menimpa "dataMixinB" dari MixinHeader
        },
        props: ["data_props"],            // Menggunakan props
        template: `
          <super>
            <h6>{{ dataMixinB }}</h6>
            <h6>{{ data_props }}</h6>
            <h6>{{ message }}</h6>
          </super>
        `
      })

      var vm = new Vue({
        el: '#app',
        components: {
          'component-c': ComponentC,
          'component-d': ComponentD,
        }
      })
    </script>
  </body>
</html>
```

</details>

## **13. Plugins** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

**⚠️ BELUM DIRANGKUM ⚠️**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <!-- ⚠️ Kode HTML disimpan disini -->

    <script>
      /* ⚠️ Script (Vue) disimpan disini */
    </script>
  </body>
</html>
```

</details>

## **14. Routing** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary>

### **👉 14-1. Konsep Dasar**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <!-- 1. Tambahkan pustaka vue-router.js -->
    <script src="https://cdn.jsdelivr.net/npm/vue-router@3.5.2/dist/vue-router.js"></script>
  </head>

  <body>
    <div id="app">
      <!-- 7B. Mengakses path di template -->
      <h4>Current route: {{ $route.path }}</h4>
      <hr>

      <!-- 2. Deklarasi router di template -->
      <p>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </p>
      <router-view></router-view>
    </div>

    <script>
      // 3. Definisikan konfigurasi component
      const Home = {template: `<div>Ini halaman home</div>`}
      const About = {template: `<div>Ini halaman about</div>`}

      // 4. Mapping route path dengan componentnya
      const routes = [
        {path:'/', component: Home, alias: '/home'},
        {path:'/about', component: About},
        {path:'*', redirect: '/'} // Redirect ke home jika URL tidak valid
      ]

      // 5. Register routing app pada Object dari Class VueRouter
      const router = new VueRouter({
        routes // Shorthand dari 'routes: routes'
      })

      // 6. Register Object router pada Object Vue
      var vm = new Vue({
        el: '#app',
        router,
        methods: {
          showCurrentRoute(){
            console.log(this.$route.path) // 7A. Mengakses path di dalam Object Vue
          }
        }
      })
    </script>
  </body>
</html>
```

### **👉 14-2. Dynamic Routing**

𝑩𝒐𝒐𝒌𝒔𝑪𝒐𝒎𝒑𝒐𝒏𝒆𝒏𝒕.𝒋𝒔:

```Javascript
export const BooksComponent = {
  data() {
    return {
      books: [
        { id: 1, judul: "Buku A" },
        { id: 2, judul: "Buku B" },
        { id: 3, judul: "Buku C" },
        { id: 4, judul: "Buku D" },
        { id: 5, judul: "Buku E" },
      ]
    }
  },
  template: `
    <div>
      <h3>Daftar Buku</h3>
      <ul>
        <li v-for="buku of books">
          <router-link :to="'/book/'+buku.id">
            {{ buku.judul }}
          </router-link>
        </li>
      </ul>
    </div>
  `
}
```

𝑩𝒐𝒐𝒌𝑪𝒐𝒎𝒑𝒐𝒏𝒆𝒏𝒕.𝒋𝒔:

```Javascript
// Method untuk membuat huruf pertama dari sebuah kata menjadi huruf kapital
String.prototype.capitalize = function () {
    return this.charAt(0).toUpperCase() + this.slice(1);
}

export const BookComponent = {
  data() {
    return {
      books: [
        { id: 1, judul: 'Buku A', deskripsi: "Koding Easy", harga: 50000, img: 'cover-1.jpg' },
        { id: 2, judul: 'Buku B', deskripsi: "Design Easy", harga: 60000, img: 'cover-2.jpg' },
        { id: 3, judul: 'Buku C', deskripsi: "Gaming Easy", harga: 70000, img: 'cover-3.jpg' },
        { id: 4, judul: 'Buku D', deskripsi: "Living Easy", harga: 80000, img: 'cover-4.jpg' },
      ]
    }
  },
  computed: {
    book() {
      return this.books.filter((buku) => {
        return buku.id === parseInt(this.$route.params.id)
      })[0]
    }
  },
  template: `
    <div v-if="book">
      <h3>{{ book.judul }}</h3>
      <ul>
        <li v-for="(value, key) of book">
          {{ key.capitalize() + ' : ' + value }}<br>
        </li>
      </ul>
    </div>
  `
}
```

𝑰𝒏𝒅𝒆𝒙.𝒉𝒕𝒎𝒍:

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue-router@3.5.2/dist/vue-router.js"></script>
  </head>

  <body>
    <div id="app">
      <h4>Current route: {{ $route.path }}</h4>
      <hr>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/books">Books</router-link>
      <hr>
      <router-view></router-view>
    </div>

    <script type="module">                                  // type="module" artinya memakai file dari luar
      import { BooksComponent } from './BooksComponent.js'  // "Import" BooksComponent dari luar file
      import { BookComponent } from './BookComponent.js'    // "Import" BookComponent dari luar file

      const Home = { template: `<div>Ini halaman home</div>` }
      const About = { template: `<div>Ini halaman about</div>` }

      const routes = [
        { path: '/', component: Home, alias: '/home' },
        { path: '/about', component: About },
        { path: '/books', component: BooksComponent },
        { path: '/book/:id', component: BookComponent },    // :id merupakan path dinamis sesuai dengan
        { path: '*', redirect: '/' },                       // link pada <router-link> nya.
      ]

      const router = new VueRouter({
        routes
      })

      var vm = new Vue({
        el: '#app',
        router,
      })
    </script>
  </body>
</html>
```

### **👉 14-3. Programmatic Navigation**

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue-router@3.5.2/dist/vue-router.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <!-- ⚠️ Kode HTML disimpan disini -->

    <script>
      /* ⚠️ Script (Vue) disimpan disini */
    </script>
  </body>
</html>
```

</details>

## **15. State Management** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <!-- ⚠️ Kode HTML disimpan disini -->

    <script>
      /* ⚠️ Script (Vue) disimpan disini */
    </script>
  </body>
</html>
```

</details>

## **16. ...** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<html>
  <head>
    <title>Belajar Vue.js</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <style>
      /* ⚠️ Style disimpan disini (jika ada) */
    </style>
  </head>

  <body>
    <!-- ⚠️ Kode HTML disimpan disini -->

    <script>
      /* ⚠️ Script (Vue) disimpan disini */
    </script>
  </body>
</html>
```

</details>
