<div id="top"></div>

# Vue.js in One Page

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
      <h1>{{ `Name: ${name}` }}</h1>
      <h1>{{ `Age: ${age}` }}</h1>
      <h1>{{ `Gender (Pria): ${gender}` }}</h1>
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

Template Vue (mustache ```{{ ... }}```) mendukung JavaScript Expressions, seperti ```{{ `Diskon: ${total * 10%}` }}```, ```{{ ok ? 'YES' : 'NO' }}```, ```{{ message.split('').reverse().join('') }}```. Atau jika dalam bentuk atribut HTML maka penulisannya dengan cara di-binding, contohnya sebagai berikut ```<h1 :id="`product-${index}`"></h1>```.

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
        template: '<h1>{{ message1 }}</h1>', // Properti Template
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
4. ```v-show:``` ➜ Untuk show/hide suatu elemen DOM. Proses on/off pada directive ini menggunakan properti ```display``` pada CSS.
5. ```v-if:```, ```v-else-if```:, ```v-else```: ➜ Untuk merender/tidak merender suatu elemen DOM.
6. ```v-on:``` ➜ Berperan sebagai sebuah event listener pada elemen HTML/komponen Vue.
7. ```v-bind:``` ➜ Untuk mem-binding atribut HTML atau komponen agar nilainya terupdate secara reactive sesuai dengan datanya.

Catatan:
1. Penulisan directive ```v-on:``` dapat disingkat menjadi ```@```
2. Penulisan directive ```v-bind:``` dapat disingkat menjadi ```:```

Ragam directive event:
1. ```@click``` ➜ Ketika mouse diklik
2. ```@mouseover``` ➜ Ketika mouse berada di area elemen
3. ```@mouseenter``` ➜ Ketika mouse masuk ke area elemen
4. ```@mouseout``` ➜ Ketika mouse keluar dari area elemen
5. ```@mousedown``` ➜ Sama dengan v-on:click
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
      <img v-bind:src="imageSrc" />
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

## **8. List** <a href="#top">⟲</a>

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

## **9. Form** <a href="#top">⟲</a>

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

## **10. Components** <a href="#top">⟲</a>

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
