# Vue.js in One Page

Markdown ini ditulis oleh <a href="https://alamehan.github.io/">alamehan.github.io</a>.

## **1. Object Vue**

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

## **2. Siklus Object Vue**

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
- HOOK 1: beforeCreate ➜ Belum bisa mengakses variabel message
- HOOK 2: created ➜ Sudah bisa mengakses & memanipulasi variabel message
- HOOK 3: beforeMount ➜ Sudah bisa mengakses DOM, namun Data belum dirender dengan Template
- HOOK 4: mounted ➜ Sudah bisa mengakses DOM & Data sudah dirender dengan Template
- HOOK 5: beforeUpdate ➜ Disini variabel message masih bernilai 'Hello World!' Padahal sudah diupdate dengan perintah vm.message = "Selamat Datang!" (lihat dibawah Object Vue ini)
- HOOK 6: updated ➜ Disini variabel message sudah terupdate menjadi 'Selamat Datang!'
- HOOK 7: beforeDestroy ➜ Terjadi sebelum Component dihapus
- HOOK 8: destroyed ➜ Terjadi setelah Object Vue dihapus

Nantinya masing-masing hook dapat dimanfaatkan untuk menjalankan suatu perintah tertentu.

## **3. Penulisan Template**

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

## **4. Properti Template**

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

## **5. Properti Lainnya**

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

## **6. Directive**

```HTML

```

## **7. Dynamic Argument**

```HTML

```

## **8. List**

```HTML

```

## **9. Form**

```HTML

```

## **8. Components**

```HTML

```
