# Vue.js in One Page

Markdown ini ditulis oleh <a href="https://alamehan.github.io/">alamehan.github.io</a>.

## **0. Template Koding**

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

## **1. Object Vue**

```HTML
<!-- Container (mount point), sebagai hasil kompilasi Vue -->
<div id="app">
  <h1>{{ `Name: ${name}` }}</h1>
  <h1>{{ `Age: ${age}` }}</h1>
  <h1>{{ `Gender (Pria): ${gender}` }}</h1>
  <h1>{{ `Hobby: ${hobby[0]} ${hobby[1]}` }}</h1>
  <h1>{{ `Children: ${children[1]} & ${children[2]}` }}</h1>
</div>
```

```Javascript
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
<div id="app">
  <h1>{{ message }}</h1>
</div>
```

```Javascript
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

```CSS
.title {
  color: green;
}
```

```HTML
<div id="app">
  <h1>{{ message }}</h1> <!-- Baca data text -->
  <h1 v-once>{{ message }}</h1> <!-- Agar nilai tidak dapat diubah -->
  <h1 v-html="message_html"></h1> <!-- Baca data RAW HTML -->
  <h1 v-bind:class="class_h1">{{ message }}</h1> <!-- Baca data attribute -->
  <h1 :class="class_h1">{{ message }}</h1> <!-- Shorthand untuk v-bind -->
</div>
```

```Javascript
vm = new Vue({
  el: '#app',
  data: {
    message: 'Hello World!', // Data text
    message_html: "<span style='color:red'>Hello World!</span>", // Data RAW HTML
    class_h1: 'title', // Data attribute (class CSS)
  },
});
```

Template Vue (mustache ```{{ ... }}```) mendukung JavaScript Expressions, seperti ```{{ `Diskon: ${total * 10%}` }}```, ```{{ ok ? 'YES' : 'NO' }}```, ```{{ message.split('').reverse().join('') }}```. Atau jika dalam bentuk atribut HTML maka penulisannya sebagai berikut ```<h1 :id="`product-${index}`"></h1>```.

## **3. Penulisan Template**

```HTML

```

```Javascript

```

## **3. Penulisan Template**

```HTML

```

```Javascript

```

## **3. Penulisan Template**

```HTML

```

```Javascript

```

## **3. Penulisan Template**

```HTML

```

```Javascript

```

## **3. Penulisan Template**

```HTML

```

```Javascript

```
