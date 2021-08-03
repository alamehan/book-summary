# Vue.js in One Page

Markdown ini ditulis oleh <a href="https://alamehan.github.io/">alamehan.github.io</a>.

## **0. Template Koding**

```HTML
<html>

<head>
  <title>Belajar Vue.js</title>
  <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
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
<!-- CONTAINER (MOUNT POINT), SEBAGAI HASIL KOMPILASI VUE -->
<div id="app">
  <h1>{{ `Name: ${name}` }}</h1>
  <h1>{{ `Age: ${age}` }}</h1>
  <h1>{{ `Gender (Pria): ${gender}` }}</h1>
  <h1>{{ `Hobby: ${hobby[0]} ${hobby[1]}` }}</h1>
  <h1>{{ `Children: ${children[1]} & ${children[2]}` }}</h1>
</div>
```

```Javascript
// INISIASI OBJECT VUE (YANG DISIMPAN KEDALAM VARIABEL vm)
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

Mengakses Properti didalam Object Vue menggunakan ```this.$data.name``` atau bisa langsung ```this.name```. Mengakses Properti diluar Object Vue menggunakan ```vm.$data.name``` atau bisa langsung ```vm.name```.

Selain mount ditulis dengan cara:
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
