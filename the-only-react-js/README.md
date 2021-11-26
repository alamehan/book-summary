<div id="top"></div>

# 𝐓𝐡𝐞 𝐎𝐧𝐥𝐲 𝐑𝐞𝐚𝐜𝐭.𝐣𝐬

Markdown ini ditulis oleh <a href="https://alamehan.github.io/">alamehan.github.io</a>.

## **0. Notes** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

### A. Setup Project

1. Install <a href="https://nodejs.org/en">Node.js</a>
2. Install React App
```
npx create-react-app my-app
cd my-app
npm start
```
3. Install Prettier ESLint (VSCode Extension)

- Install Depedencies: ```npm i prettier prettier-eslint -D``` (untuk eslint sudah include saat menginstall create-react-app)
- Install Extension <a href="https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint">Prettier ESLint</a> & Restart VSCode
- Buka File > Preferences > Settings > User > Ketik "Editor: Default Formatter" lalu pilih Prettier ESLint
- Buka File > Preferences > Settings > User > Ketik "Editor: Format on" lalu ceklis "Editor: Format on Save" & "Editor: Format on Type"

### B. Catatan Penting

1. Jika component Anda tidak membutuhkan state (data yang nilainya berubah-ubah) & life cycle method, maka gunakan Functional Component. Sebaliknya, jika component Anda membutuhkan state & life cycle method, gunakan Classes Component. [Sebagai catatan: di React Hook nanti, Functional Component bisa menggunakan state & life cycle method]
2. Component itu sesimple class/fungsi yang menerima props (data dari luar) dan me-return HTML (JSX).
3. "npm audit fix" akan memperbarui/menimpa package ke versi yang aman, yang tidak memiliki masalah keamanan (security). untuk menghilangkan "vulnerabilities".
4. Catatan di package.json
```
"react": "16.8.6" berarti versi react yang digunakan yaitu tepat 16.8.6.
"react": "^16.8.6", tanda ^ berarti versi react yang digunakan minimal 16.8.6.

Artinya jika ada versi react terbaru bisa diupdate secara otomatis menggunakan perintah "npm update". Untuk proses update versi
package, lebih baik gunakan "npm update" dibandingkan "npm install".
```

</details>

## **1. Hello World** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root"></div>

  <script type="text/babel">

    ReactDOM.render(<h1>Hello, world!</h1>, document.getElementById('root'))

  </script>
</body>

</html>
```

</details>

## **2. Memperkenalkan JSX** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <div id="root2"></div>
  <div id="root3"></div>
  <div id="root4"></div>

  <script type="text/babel">

    const name = "John Doe";
    const age = 24;

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 1                                 */
    /* ----------------------------------------------------------------------- */

    // Tanpa JSX
    const elementA1 = React.createElement(
      'h1',
      { className: 'my-style', style: { marginBottom: 100 } },
      `Halo ${name} ${age}!`
    )
    // Dengan JSX
    const elementA2 = (
      <h1 className='my-style' style={{ marginBottom: 100 }}>
        Halo {name} {age}!
      </h1>
    )

    ReactDOM.render(elementA1, document.getElementById('root1'))
    ReactDOM.render(elementA2, document.getElementById('root2'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 2                                 */
    /* ----------------------------------------------------------------------- */

    // Tanpa JSX: Nested
    const elementB1 = React.createElement(
      'div',
      {},
      [
        React.createElement('h1', {}, `Name: ${name}`),
        React.createElement('h2', {}, `Age: ${age}`),
        React.createElement('h3', {}, `No: ${9 * 9}`),
      ]
    )
    // Dengan JSX: Nested
    const elementB2 = (
      <div>
        <h1>Name: {name}</h1>
        <h2>Age: {age}</h2>
        <h3>No: {9 * 9}</h3>
      </div>
    )

    ReactDOM.render(elementB1, document.getElementById('root3'))
    ReactDOM.render(elementB2, document.getElementById('root4'))

  </script>
</body>

</html>
```

</details>

## **3. Merender Elements** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <div id="root2"></div>

  <script type="text/babel">

    // 1. Penulisan Function biasa
    function tick1() {
      const element1 = (
        <div>
          <h1>It's {new Date().toLocaleTimeString()}</h1>
        </div>
      )
      ReactDOM.render(element1, document.getElementById('root1'))
    }

    // 2. Penulisan Arrow Function
    let tick2 = () => {
      const element2 = (
        <div>
          <h1>It's {new Date().toLocaleTimeString()}</h1>
        </div>
      )
      ReactDOM.render(element2, document.getElementById('root2'))
    }

    // ReactDOM.render akan dipanggil setiap detiknya dari sebuah callback setInterval()
    setInterval(tick1, 1000)
    setInterval(tick2, 1000)

  </script>
</body>

</html>
```

</details>

## **4. Komponen dan Props** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <div id="root2"></div>

  <script type="text/babel">

    /*  
      Komponen mirip dengan fungsi pada JavaScript. Komponen menerima beberapa 
      masukan (biasa disebut “props”) dan mengembalikan element React yang 
      mendeskripsikan apa yang seharusnya tampil pada layar. Sebagai catatan,
      props bersifat read-only, artinya nilai dari props tidak bisa ditimpa.
      Juga, secara default jika Anda tidak mengoper nilai apapun ke sebuah
      props maka nilainya adalah "true".
    */

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 1                                 */
    /* ----------------------------------------------------------------------- */

    // Cara 1: Function Components (dimana props sebagai parameter)
    function ComponentA(props) { // <- Nama component harus diawali huruf kapital
      return (
        <div>
          <h1>Halo {props.name}</h1>
          <h2>Umur Anda {props.age}</h2>
        </div>
      )
    }

    // Cara 2: Class Components (dimana props sebagai property)
    class ComponentB extends React.Component { // <- Nama component harus diawali huruf kapital
      render() {
        return (
          <div>
            <h1>Halo {this.props.name}</h1>
            <h2>Umur Anda {this.props.age}</h2>
          </div>
        )
      }
    }

    // Memberikan nilai default untuk props
    ComponentA.defaultProps = { name: "Anonim", age: 0 }
    ComponentB.defaultProps = { name: "Anonim", age: 0 }

    // Gabungkan kedalam satu element (contoh saja) & Oper nilai ke props-nya (name & age)
    const element = (
      <div>
        <ComponentA name="Raihan" age={21} />
        <ComponentB name="Allaam" age={24} />
        <ComponentA />
        <ComponentB />
      </div>
    )
    // Pada contoh di atas komponen yang tidak mengoper nilai props akan secara otomatis
    // menggunakan nilai default dari props (defaultProps)

    ReactDOM.render(element, document.getElementById('root1'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 2                                 */
    /* ----------------------------------------------------------------------- */

    // 1. Contoh data untuk props
    const data = {
      author: {
        name: 'Hello Kitty',
        avatarUrl: 'https://placekitten.com/g/64/64',
      },
      text: 'I hope you enjoy learning React!',
      date: new Date(),
    };

    // 2. Komponen Avatar
    function Avatar(props) {
      return <img src={props.attExamp.avatarUrl} alt={props.attExamp.name} />
    }

    // 3. Komponen UserInfo (didalamnya memakai komponen Avatar)
    function UserInfo(props) {
      return (
        <div>
          <Avatar attExamp={props.attUser} />
          <p>{props.attUser.name}</p>
        </div>
      )
    }

    // 4. Komponen Comment (didalamnya memakai komponen UserInfo)
    function Comment(props) {
      return (
        <div>
          <UserInfo attUser={props.attAuthor} />
          <p>{props.attText}</p>
          <p>{props.attDate.toLocaleDateString()}</p>
        </div>
      )
    }

    // 5, Render Komponen Comment & Oper nilai props-nya
    ReactDOM.render(

      // Alur data props yaitu satu arah, turun dari parent ke child,
      // dimulai dari sini <Comment /> ke <UserInfo /> ke <Avatar /> 
      <Comment attAuthor={data.author} attText={data.text} attDate={data.date} />,
      document.getElementById('root2')
    )

  </script>
</body>

</html>
```

</details>

## **5. State dan Lifecycle** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <div id="root2"></div>

  <script type="text/babel">

    /*  
      Baris kode ini merupakan perbaikan dari fille "3-merender-elements.html",
      alih-alih hanya sebagai function biasa, disini kita akan membuat komponen 
      Clock yang benar-benar dapat digunakan kembali (reusable) dan terenkapsulasi.
      Hal ini akan mengatur timer-nya sendiri dan memperbaruiya setiap detik.

      Mulanya hanya Class Components yang dapat menggunakan state & lifecycle method,
      namun semenjak adanya Hook (fitur baru), Function Components pun punya cara
      tersendiri untuk menggunakan state & lifecycle method (dibahas nanti).

      State adalah data private sebuah component. D̶a̶t̶a̶ ̶i̶n̶i̶ ̶h̶a̶n̶y̶a̶ ̶t̶e̶r̶s̶e̶d̶i̶a̶ ̶u̶n̶t̶u̶k̶
      c̶o̶m̶p̶o̶n̶e̶n̶t̶ ̶t̶e̶r̶s̶e̶b̶u̶t̶ ̶d̶a̶n̶ ̶t̶i̶d̶a̶k̶ ̶b̶i̶s̶a̶ ̶d̶i̶ ̶a̶k̶s̶e̶s̶ ̶d̶a̶r̶i̶ ̶c̶o̶m̶p̶o̶n̶e̶n̶t̶ ̶l̶a̶i̶n̶. Component dapat
      merubah statenya sendiri (tujuan state memang untuk berubah-ubah nilainya).
    */

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 1                                 */
    /* ----------------------------------------------------------------------- */

    class Clock extends React.Component {

      // 𝐒𝐓𝐄𝐏 𝟑: Constructor dipanggil, state di inisialisasi
      constructor(props) {
        super(props)
        this.state = {
          date: new Date(),
          name: `Saya nomor ${Math.floor(Math.random() * 100) + 1}` // 1-100
        }
      }

      // 𝐒𝐓𝐄𝐏 𝟒: Method tick() disini berfungsi untuk memperbarui state
      // date & name yang nanti akan dijalankan di componentDidMount()
      tick() {

        /*
          Agar lebih mudah dibaca, baris di bawah idenya adalah: 
          ➜ this.state.date = new Date()
          ➜ this.state.name = `Saya ${Math.floor(Math.random() * 11)}`
          
          hanya saja di aturan React kita tidak bisa memperbarui state 
          dengan statement tersebut, sebagai gantinya gunakan setState()
        */

        this.setState({
          date: new Date(),
          name: `Saya nomor ${Math.floor(Math.random() * 100) + 1}` // 1-100
        })
      }

      // 𝐒𝐓𝐄𝐏 𝟔: Saat sudah terjadi render DOM pertama kalinya, React
      // kemudian akan memanggil method lifecycle componentDidMount()
      componentDidMount() {

        /* 
          timerID (nama "new state" bebas saja, bisa langsung dipanggil tanpa 
          perlu inisialisasi di constructor) akan menyuruh browser untuk memanggil
          method tick() setiap detik. Sebenarnya baris di bawah idenya adalah:
          ➜ setInterval(() => this.tick(), 1000)
          
          Hanya saja selain setInterval langsung dijalankan, kita simpan terlebih 
          dahulu ke dalam this.timerID untuk nantinya dipakai di componentWillUnmount()
        */

        this.timerID = setInterval(() => this.tick(), 1000)

        /*
          Selain itu, jika Anda bertanya mengapa tidak langsung ditulis:
          ➜ setInterval(this.tick, 1000) saja?
          
          Mengapa malah dibuatkan bentukArrow Function-nya? hal tersebut dilakukan
          agar konteks this-nya sesuai/berfungsi dengan baik. Sebenarnya bisa saja
          langsung ditulis "setInterval(this.tick, 1000)", hanya saja konteks this
          untuk tick() perlu di binding terlebih dahulu di constructor (selebihnya,
          lihat contoh pada Bagian 2 di bawah)
        */
      }

      // 𝐒𝐓𝐄𝐏 𝟖: Jika komponen Clock dihapus dari DOM, React akan memanggil method
      // lifecycle componentWillUnmount(), sehingga timer akan berhenti
      componentWillUnmount() {
        clearInterval(this.timerID)
      }

      // 𝐒𝐓𝐄𝐏 𝟓: React me-render DOM sesuai nilai state saat ini (state saat inisialisasi)
      // 𝐒𝐓𝐄𝐏 𝟕: Setiap detik React akan re-render spesifik DOM sesuai nilai state terbaru
      render() {
        return (
          <div>
            <h1>Date: {this.state.date.toLocaleTimeString()}</h1>
            <h2>{this.state.name}</h2>
          </div>
        )
      }
    }

    // 𝐒𝐓𝐄𝐏 𝟏: Komponen App yang menampilkan 3 komponen Clock di dalamnya
    function App() {
      return (

        /*
          Perhatikan bahwa hasilnya nanti, ke 3 komponen Clock benar-benar terisolasi,
          setiap Clock membuat timer-nya sendiri dan memperbaruinya secara independen
        */

        <div>
          <Clock />
          <Clock />
          <Clock />
        </div>
      )
    }

    // 𝐒𝐓𝐄𝐏 𝟐: Komponen App diberikan ke ReactDOM.render()
    ReactDOM.render(<App />, document.getElementById("root1"))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 2                                 */
    /* ----------------------------------------------------------------------- */

    class Counter extends React.Component {
      constructor(props) {
        super(props)
        this.state = {
          value: 0,
        }

        // Untuk penulisan Function Definitions (ES6+) di dalam sebuah Class, lihat nomor 4 di bawah,
        // keyword this perlu di binding terlebih dahulu agar konteksnya sesuai/berfungsi dengan baik
        this.incrementA = this.incrementA.bind(this)
        this.incrementB = this.incrementB.bind(this)
      }

      /*
        Note: Perhatikan bahwa penulisan Arrow Function di dalam sebuah Class tidak perlu menyertakan keyword
        var/let/const. Berbeda dengan jika didefinisikan di global, tentunya keyword var/let/const disertakan.
      */

      // 1. Mungkin saja props & state diperbarui secara Asynchronous, maka penulisan di bawah ini kurang tepat:
      handleIncrement1 = () => this.setState({ value: this.state.value + this.props.step })
      handleDecrement1 = () => this.setState({ value: this.state.value - this.props.step })

      // 2. Sebagai gantinya, pakai setState() yang menerima fungsi daripada sebuah object langsung:
      handleIncrement2 = () => this.setState((state, props) => ({ value: state.value + props.step }))
      handleDecrement2 = () => this.setState((state, props) => ({ value: state.value - props.step }))

      /*
        Note: Return object di Arrow Function tidak bisa langsung ditulis (state, props) => { ... },
        karena tanda {} akan dianggap sebagai pembuka Function oleh JavaScript. Solusinya bungkus
        terlebih dahulu object-nya menggunakan tanda (), menjadi (state, props) => ({ ... }).
      */

      // 3. Function yang menjadi argument pada setState juga bisa ditulis dengan Function biasa:
      handleIncrement3 = () => this.setState(function (state, props) { return { value: state.value + props.step } })
      handleDecrement3 = () => this.setState(function (state, props) { return { value: state.value - props.step } })

      // 4. Ketiga contoh Function di atas bisa juga ditulis menggunakan Function Definitions (ES6+):
      incrementA() { this.setState((state, props) => ({ value: state.value + props.step })) }
      incrementB() { this.setState(function (state, props) { return { value: state.value + props.step } }) }

      /*
        Note: Jangan lupa! seperti catatan yang ditulis pada bagian constructor, bahwa jika menggunakan
        Function Definitions (ES6+), terdapat sebuah syarat, yaitu keyword this-nya perlu di binding
        terlebih dahulu di constructor, agar konteksnya sesuai/berfungsi dengan baik.
      */

      render() {
        return (

          /*
            Terdapat perbedaan cara penulisan penanganan events antara HTML dengan React, simak contoh berikut:
            HTML biasa          : <button onclick="handleEvent()">Click me</button>
            React (JSX) cara 1  : <button onClick={this.handleEvent}>Click me</button>
            React (JSX) cara 2  : <button onClick={() => this.handleEvent()}>Click me</button>
          */

          <div>
            <h1>{this.state.value}</h1>
            <button onClick={this.handleIncrement2}>+</button>
            <button onClick={() => this.handleDecrement2()}>-</button>
          </div>
        )
      }
    }

    ReactDOM.render(<Counter step={5} />, document.getElementById("root2"))

  </script>
</body>

</html>
```

</details>

## **6. Penanganan Events** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <div id="root2"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                       Bagian 1: Contoh State saja                       */
    /* ----------------------------------------------------------------------- */

    class Toggle1 extends React.Component {
      constructor() {   // <- Tidak perlu disisipkan props
        super()         // <- Tidak perlu disisipkan props
        this.state = {
          isToggleOn: true
        }

        // Ingat: Binding diperlukan agar konteks this 
        // pada Function Definitions (ES6+) berfungsi
        this.handleClick = this.handleClick.bind(this)
      }

      handleClick() {
        // Nama parameter "state" bisa bebas (misalnya data, status, dll)
        this.setState(state => ({ isToggleOn: !state.isToggleOn }))
      }

      render() {
        return (
          <div>
            <h1>Status click : {this.state.isToggleOn ? "ON" : "OFF"}</h1>
            <button onClick={this.handleClick}>Click me</button>
          </div>
        )
      }
    }

    ReactDOM.render(<Toggle1 />, document.getElementById('root1'))

    /* ----------------------------------------------------------------------- */
    /*                     Bagian 2: Contoh State & Props                      */
    /* ----------------------------------------------------------------------- */

    class Toggle2 extends React.Component {
      constructor(props) {  // <- Perlu disisipkan props
        super(props)        // <- Perlu disisipkan props
        this.state = {
          isToggleOn: true,
          totalClick: 0,
        }

        this.handleClick = this.handleClick.bind(this)
      }

      handleClick() {
        this.setState((state, props) => ({
          isToggleOn: !state.isToggleOn,
          totalClick: state.totalClick + props.counter,
        }))
      }

      render() {
        return (
          <div>
            <h1>Status click : {this.state.isToggleOn ? "ON" : "OFF"}</h1>
            <h3>Total click  : {this.state.totalClick}</h3>
            <button onClick={this.handleClick}>Click me</button>
          </div>
        )
      }
    }

    ReactDOM.render(<Toggle2 counter={1} />, document.getElementById('root2'))

  </script>
</body>

</html>
```

</details>

## **7. Render Bersyarat** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <hr>
  <div id="root2"></div>
  <hr>
  <div id="root3"></div>
  <hr>
  <div id="root4"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                    Bagian 1: LoginControl Sederhana                     */
    /* ----------------------------------------------------------------------- */

    class LoginControl1 extends React.Component {
      constructor() {
        super()
        this.state = { isLoggedIn: true }
      }

      handleLogin = () => this.setState({ isLoggedIn: true })
      handleLogot = () => this.setState({ isLoggedIn: false })

      render() {
        const status = this.state.isLoggedIn
        let button, greeting

        if (status) {
          button = <button onClick={this.handleLogot}>Logout</button>
          greeting = <h1>Welcome back!</h1>
        } else {
          button = <button onClick={this.handleLogin}>Login</button>
          greeting = <h1>Please sign up.</h1>
        }

        return (
          <div>
            {greeting}
            {button}
          </div>
        )
      }
    }

    ReactDOM.render(<LoginControl1 />, document.getElementById("root1"))

    /* ----------------------------------------------------------------------- */
    /*                         Bagian 2: LoginControl                          */
    /* ----------------------------------------------------------------------- */

    // 1. Komponen Greeting
    function UsersGreeting() { return <h1>Welcome back!</h1> }
    function GuestGreeting() { return <h1>Please sign up.</h1> }

    function Greeting(props) {
      const isLoggedIn = props.masuk

      /*
        Jika kondisi hanya if saja, bisa ditulis 1 baris tanpa tanda {} seperti contoh
        di bawah. Dan sebagai catatan "return" value tidak bisa digunakan di ternary
        operator, oleh karena itu di bawah ini digunakan struktur logika if biasa.
      */

      if (isLoggedIn) return <UsersGreeting />
      return <GuestGreeting />
    }

    // 2. Komponen Button
    function LoginButton(props) { return <button onClick={props.diKlik}>Login</button> }
    function LogotButton(props) { return <button onClick={props.diKlik}>Logout</button> }

    // 3. Komponen LoginControl
    class LoginControl2 extends React.Component {
      constructor() {
        super()
        this.state = { isLoggedIn: true }
      }

      handleLoginClick = () => this.setState({ isLoggedIn: true })
      handleLogotClick = () => this.setState({ isLoggedIn: false })

      render() {
        const isLoggedIn = this.state.isLoggedIn
        let button

        isLoggedIn
          ? button = <LogotButton diKlik={this.handleLogotClick} />
          : button = <LoginButton diKlik={this.handleLoginClick} />

        /*
          Struktur logika di atas menggunakan ternary operator. Namun selain itu,
          bisa juga menggunakan struktur logika if-else biasa maupun operator
          short-circuit-evaluation && atau || (lihat bagian 3 di bawah)
        */

        return (
          <div>
            <Greeting masuk={isLoggedIn} />
            {button}
          </div>
        )
      }
    }

    ReactDOM.render(<LoginControl2 />, document.getElementById('root2'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 3                                 */
    /* ----------------------------------------------------------------------- */

    function MailBox(props) {
      const unreadMsg = props.msg

      return (
        <div>
          {unreadMsg.length > 0 && <h2>You have {unreadMsg.length} unread Messages.</h2>}
        </div>
      )

      /*
        Cara baca operator short-circuit-evaluation && diatas, yaitu:
        Jika (unreadMsg.length > 0) maka artinya "true", akibatnya perintah setelah 
        tanda && akan dieksekusi. Namun sebaliknya, jika "false", tidak dieksekusi.
      */
    }

    const messages = ['lorem', 'ipsum', 'dolor']

    ReactDOM.render(<MailBox msg={messages} />, document.getElementById('root3'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 4                                 */
    /* ----------------------------------------------------------------------- */

    /*
      Pada kasus yang jarang terjadi, Anda mungkin ingin komponen menyembunyikan 
      dirinya sendiri meskipun komponen itu di-render oleh komponen lain. Untuk
      melakukan ini, gunakan return null. Simak contoh dibawah.
    */

    function WarningBanner(props) {

      /*
        Ingat bahwa perintah di bawah ini saling setara:
        1. if (props.warn)  ➜ if (props.warn === true)
        2. if (!props.warn) ➜ if (props.warn !== true) ➜ if (props.warn === false)

        Dengan demikian, perintah "if (!props.warn) return null" di bawah berarti
        jika (props.warn === false) maka jangan render WarningBanner (return null), 
        sebaliknya jika (props.warn === true) maka render <div>Warning!</div>
      */

      if (!props.warn) return null
      return <div>Warning!</div>
    }

    class Page extends React.Component {
      constructor() {
        super()
        this.state = { showWarning: false }
      }

      handleToggleClick = () => this.setState(prevState => ({ showWarning: !prevState.showWarning }))

      render() {
        return (
          <div>
            <WarningBanner warn={this.state.showWarning} />
            <button onClick={this.handleToggleClick}>
              {this.state.showWarning ? "Hide" : "Show"}
            </button>
          </div>
        )
      }
    }

    ReactDOM.render(<Page />, document.getElementById('root4'))

  </script>
</body>

</html>
```

</details>

## **8. Lists dan Keys** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <hr>
  <div id="root2"></div>
  <hr>
  <div id="root3"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 1                                 */
    /* ----------------------------------------------------------------------- */

    function NumberList(props) {
      const numbers = props.nums
      // Dalam element list harus ada atribut key yang berisi string unik. Kenapa? key
      // membatu React mengidentifikasi item mana yang telah diubah, ditambah, dihapus.
      // Hal ini berpengaruh pada proses render DOM agar lebih cepat dan efisien.
      const listItems = numbers.map(number => <li key={number.toString()}>{number}</li>)
      return <ul>{listItems}</ul>
    }

    const numA = [1, 2, 3, 4, 5]

    ReactDOM.render(<NumberList nums={numA} />, document.getElementById('root1'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 2                                 */
    /* ----------------------------------------------------------------------- */

    function ListItem(props) {
      // Penempatan atribut key bukan disini ya. Terdapat sebuah aturan yang mudah 
      // diingat, yaitu atribut key ditempatkan dimana method map() dipanggil.
      return <li>{props.value}</li>
    }

    function NumberList2(props) {
      const numbers = props.nums
      // Method map() dipanggil disini, artinya atribut key disisipkan di <ListItem />
      const listItems = numbers.map(number => <ListItem key={number.toString()} value={number} />)
      return <ul>{listItems}</ul>
    }

    const numB = [6, 7, 8, 9, 10]

    ReactDOM.render(<NumberList2 nums={numB} />, document.getElementById('root2'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 3                                 */
    /* ----------------------------------------------------------------------- */

    /*
      Kita dapat menggunakan key yang sama ketika kita mem-produce 2/lebih Array
      yang berbeda. Misalnya contoh di bawah ini, key={post.id} digunakan di
      list pada sidebar & di div pada content. Dan hal tersebut valid. Sebagai
      catatan, key hanya harus unik antar sibling, bukan unik secara global.
    */

    function Blog(props) {

      // Ingat dalam Arrow Function, jika isi Function hanya berupa return saja, 
      // maka tanda {} serta keyword return tidak perlu ditulis. Contohnya:
      const sidebar = (
        <ul>
          {props.posts.map(post => <li key={post.id}>{post.title}</li>)}
        </ul>
      )

      // Namun jika tanda {} dan keyword return ingin tetap ditulis pun tak apa:
      const content = props.posts.map(post => {
        return (
          <div key={post.id}>
            <h3>{post.title}</h3>
            <p>{post.content}</p>
          </div>
        )
      })

      return (
        <div>
          {sidebar}
          {content}
        </div>
      )
    }

    const postsA = [
      { id: 1, title: 'Hello World', content: 'Welcome to learning React!' },
      { id: 2, title: 'Installation', content: 'You can install React from npm.' }
    ]

    ReactDOM.render(<Blog posts={postsA} />, document.getElementById('root3'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 4                                 */
    /* ----------------------------------------------------------------------- */

    /*
      Key harus stabil, dapat diprediksi, dan unik. Key yang tidak stabil (seperti yang
      diproduksi oleh Math.random()) akan menyebabkan banyak instance komponen dan node
      DOM tidak perlu diciptakan kembali, yang dapat menyebabkan penurunan kinerja.

      Sebisa mungkin hindari penggunaan key menggunakan index, karena dalam beberapa
      kasus, seperti pengurutan kembali item-item pada list akan menjadi lambat.

      - Contoh penggunaan index sebagai key: 
        https://codepen.io/alamehan/pen/JjyQBWv

      - Contoh yang sama namun dengan perbaikan (tanpa index): 
        https://codepen.io/alamehan/pen/dyzBjvg
    */

  </script>
</body>

</html>
```

</details>

## **9. Form di React** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <hr>
  <div id="root2"></div>
  <hr>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                     Bagian 1: handleChange dipisah                      */
    /* ----------------------------------------------------------------------- */

    class NameForm1 extends React.Component {
      constructor() {
        super()
        this.state = {
          name: '',           // Nilai default untuk input text
          age: 0,             // Nilai default untuk input number
          comment: '',        // Nilai default untuk textarea
          category: 'food',   // Nilai default untuk select
          gender: '',         // Nilai default untuk input radio
          isMember: false,    // Nilai default untuk input checkbox
        }
        this.handleSubmit = this.handleSubmit.bind(this)
      }

      // 1. Arrow Function cocok digunakan untuk kebutuhan update state dengan setState()
      handleChangeA = event => this.setState({ name: event.target.value })        // <- value
      handleChangeB = event => this.setState({ age: event.target.value })         // <- value
      handleChangeC = event => this.setState({ comment: event.target.value })     // <- value
      handleChangeD = event => this.setState({ category: event.target.value })    // <- value
      handleChangeE = event => this.setState({ gender: event.target.value })      // <- value
      handleChangeF = event => this.setState({ isMember: event.target.checked })  // <- checked

      // 2. Function Definitions (ES6+) cocok digunakan untuk baris kode yang lebih banyak
      handleSubmit(event) {
        alert(`
          Nama yang diinput : ${this.state.name}
          Umur yang diinput: ${this.state.age}
          Komentar yang diinput : ${this.state.comment}
          Kategori yang dipilih : ${this.state.category}
          Gender yang dipilih: ${this.state.gender}
          Termasuk member : ${this.state.isMember ? "ya" : "tidak"}
        `)

        // Mencegah terjadinya event bawaan dari sebuah DOM (dalam kasus ini pindah halaman)
        event.preventDefault()
      }

      render() {
        return (
          <form onSubmit={this.handleSubmit}>
            <div>1. Name</div>
            <input type="text" value={this.state.name} onChange={this.handleChangeA} />

            <div>2. Age</div>
            <input type="number" value={this.state.age} onChange={this.handleChangeB} />

            <div>3. Comment</div>
            <textarea value={this.state.comment} onChange={this.handleChangeC} />

            <div>4. Category</div>
            <select value={this.state.category} onChange={this.handleChangeD}>
              <option value="food">Food</option>
              <option value="drink">Drink</option>
              <option value="fruit">Fruit</option>
            </select>

            <div>5. Gender</div>
            <div>
              <input type="radio" value="Male" checked={this.state.gender === "Male"} onChange={this.handleChangeE} /> Male
              <input type="radio" value="Female" checked={this.state.gender === "Female"} onChange={this.handleChangeE} /> Female
              <input type="radio" value="Alien" checked={this.state.gender === "Alien"} onChange={this.handleChangeE} /> Alien
            </div>

            <div>6. Member</div>
            <input type="checkbox" checked={this.state.isMember} onChange={this.handleChangeF} />

            <div></div>
            <input type="submit" value="Submit" />
          </form>
        )
      }
    }

    ReactDOM.render(<NameForm1 />, document.getElementById('root1'))

    /* ----------------------------------------------------------------------- */
    /*                    Bagian 2: handleChange disatukan                     */
    /* ----------------------------------------------------------------------- */

    class NameForm2 extends React.Component {
      constructor() {
        super()
        this.state = {
          name: '',
          age: 0,
          comment: '',
          category: 'food',
          gender: '',
          isMember: false,
        }
        this.handleChange = this.handleChange.bind(this)
        this.handleSubmit = this.handleSubmit.bind(this)
      }

      // handleChange disatukan, untuk membedakan setiap field digunakan atribut name
      handleChange(event) {
        const name = event.target.name
        switch (name) {
          case "_name": this.setState({ name: event.target.value }); break;
          case "_age": this.setState({ age: event.target.value }); break;
          case "_comment": this.setState({ comment: event.target.value }); break;
          case "_category": this.setState({ category: event.target.value }); break;
          case "_gender": this.setState({ gender: event.target.value }); break;
          case "_isMember": this.setState({ isMember: event.target.checked }); break;
          default: null;
        }
      }

      handleSubmit(event) {
        alert(`
          Nama yang diinput : ${this.state.name}
          Umur yang diinput: ${this.state.age}
          Komentar yang diinput : ${this.state.comment}
          Kategori yang dipilih : ${this.state.category}
          Gender yang dipilih: ${this.state.gender}
          Termasuk member : ${this.state.isMember ? "ya" : "tidak"}
        `)

        event.preventDefault()
      }

      render() {
        return (
          // Ingat: Atribut "name" diperlukan untuk digunakan di handleChange
          // Nama field pada contoh dibawah mengambil Object Key, tidak lagi ditulis manual
          <form onSubmit={this.handleSubmit}>
            <div>1. {Object.keys(this.state)[0].toLocaleUpperCase()}</div>
            <input name="_name" type="text" value={this.state.name} onChange={this.handleChange} />

            <div>2. {Object.keys(this.state)[1].toLocaleUpperCase()}</div>
            <input name="_age" type="number" value={this.state.age} onChange={this.handleChange} />

            <div>3. {Object.keys(this.state)[2].toLocaleUpperCase()}</div>
            <textarea name="_comment" value={this.state.comment} onChange={this.handleChange} />

            <div>4. {Object.keys(this.state)[3].toLocaleUpperCase()}</div>
            <select name="_category" value={this.state.category} onChange={this.handleChange}>
              <option value="food">Food</option>
              <option value="drink">Drink</option>
              <option value="fruit">Fruit</option>
            </select>

            <div>5. {Object.keys(this.state)[4].toLocaleUpperCase()}</div>
            <div>
              <input name="_gender" type="radio" value="Male" checked={this.state.gender === "Male"} onChange={this.handleChange} /> Male
              <input name="_gender" type="radio" value="Female" checked={this.state.gender === "Female"} onChange={this.handleChange} /> Female
              <input name="_gender" type="radio" value="Alien" checked={this.state.gender === "Alien"} onChange={this.handleChange} /> Alien
            </div>

            <div>6. {Object.keys(this.state)[5].toLocaleUpperCase()}</div>
            <input name="_isMember" type="checkbox" checked={this.state.isMember} onChange={this.handleChange} />

            <div></div>
            <input type="submit" value="Submit" />
          </form>
        )
      }
    }

    ReactDOM.render(<NameForm2 />, document.getElementById('root2'))

    /* ----------------------------------------------------------------------- */
    /*                                Bagian 3                                 */
    /* ----------------------------------------------------------------------- */

    // Gunakan library "Formik" untuk kebutuhan Form yang lebih lengkap dan mudah

  </script>
</body>

</html>
```

</details>

## **10. Memindahkan State ke Atas** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root1"></div>
  <br><br><br>
  <div id="root2"></div>
  <br><br><br>
  <div id="root3"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                       Bagian 1: Contoh Sederhana                        */
    /* ----------------------------------------------------------------------- */

    function Mendidih1(props) {
      if (props.attCelsius >= 100) return <p>Air akan mendidih.</p>
      return <p>Air tidak akan mendidih.</p>
    }

    class Kalkulator1 extends React.Component {
      constructor() {
        super()
        this.state = { temperature: "" }            // <- Nilai default temperature
      }

      handleChange = event => this.setState({ temperature: event.target.value })

      render() {
        const temperature = this.state.temperature  // <- Untuk menyingkat saja

        return (
          <fieldset>
            <legend>Masukkan temperature dalam Celsius:</legend>
            <input value={temperature} onChange={this.handleChange} />
            <Mendidih1 attCelsius={parseFloat(temperature)} />
          </fieldset>
        )
      }
    }

    ReactDOM.render(<Kalkulator1 />, document.getElementById('root1'))

    /* ----------------------------------------------------------------------- */
    /*                       Bagian 2: Contoh 2 Inputan                        */
    /* ----------------------------------------------------------------------- */

    function Mendidih2(props) {
      if (props.attScl == "Celsius" && props.attDeg >= 100) return <p>Air akan mendidih.</p>
      if (props.attScl == "Fahrenheit" && props.attDeg >= 212) return <p>Air akan mendidih.</p>
      return <p>Air tidak akan mendidih.</p>
    }

    class InputTemperatur2 extends React.Component {
      constructor(props) {
        super(props)
        this.state = { temperature: 100 }           // <- Nilai default temperature
      }

      handleChange = event => this.setState({ temperature: event.target.value })

      render() {
        const temperature = this.state.temperature  // <- Untuk menyingkat saja
        const scale = this.props.attScale           // <- Untuk menyingkat saja

        return (
          <fieldset>
            <legend>Masukkan temperature dalam {scale}:</legend>
            <input value={temperature} onChange={this.handleChange} />
            <Mendidih2 attScl={scale} attDeg={parseFloat(temperature)} />
          </fieldset>
        )
      }
    }

    class Kalkulator2 extends React.Component {
      render() {
        return (
          <div>
            <InputTemperatur2 attScale="Celsius" />
            <InputTemperatur2 attScale="Fahrenheit" />
          </div>
        )
      }
    }

    ReactDOM.render(<Kalkulator2 />, document.getElementById('root2'))

    /* ----------------------------------------------------------------------- */
    /*                     Bagian 3: Sinkronasi 2 Inputan                      */
    /* ----------------------------------------------------------------------- */

    /*
      Tujuan: Saat kita memperbarui inputan celsius maka inputan fahrenheit juga
      ikut diperbarui (konversi secara otomatis), dan sebaliknya.

      Dalam react, state bersama dicapai dengan memindahkannya ke komponen induk
      bersama terdekat dari komponen yang membutuhkannya. Hal inilah yang disebut
      dengan "memindahkan state ke atas". 
      
      Dalam contoh di bawah, state temperature yang mulanya didefinisikan di komponen
      InputTemperatur3 akan "dipindahkan ke atas" yaitu ke komponen Kalkulator3.
    */

    // -----------------
    // A. Fungsionalitas
    // -----------------

    const keCelsius = fahrenheit => (fahrenheit - 32) * 5 / 9
    const keFahrenheit = celsius => (celsius * 9 / 5) + 32

    function konversi(temperature, convert) {
      const input = parseFloat(temperature)             // <- String menjadi number
      if (Number.isNaN(input)) return ''                // <- Jika NaN hentikan proses
      const output = convert(input)                     // <- Proses konversi
      const rounded = Math.round(output * 1000) / 1000  // <- Proses pembulatan
      return rounded.toString()                         // <- Return hasil
    }

    // ------------------------------
    // B1. Komponen Cucu (Grandchild)
    // ------------------------------

    function Mendidih3(props) {
      if (props.attDeg >= 100) return <p>Air akan mendidih.</p>
      return <p>Air tidak akan mendidih.</p>
    }

    // -------------------------
    // B2. Komponen Anak (Child)
    // -------------------------

    class InputTemperatur3 extends React.Component {
      constructor(props) {
        super(props)
      }

      // 𝐒𝐓𝐄𝐏 𝟐: Alih-alih memanggil this.setState() saat kita ingin melakukan perubahan, kita sekarang
      // memanggil this.props... yang akan disediakan oleh komponen induk, yaitu Kalkulator3.
      handleChange = event => this.props.onTemperatureChange(event.target.value)

      /*
        Untuk celcius akan menjadi: handleChange = event => this.props.handleCelsiusChange(event.target.value)
        Untuk fahrenheit akan menjadi: handleChange = event => this.props.handleFahrenheitChange(event.target.value)

        Dibelakang layar yang terjadi ialah:
        handleChange = event => (handleCelsiusChange = temperature => this.setState({ scale: "c", temperature }))(event.target.value)
        handleChange = event => (handleFahrenheitChange = temperature => this.setState({ scale: "f", temperature }))(event.target.value)

        Ingat kembali konsep IIFE pada JavaScript, dimana Function didefinisikan + langsung dijalankan. Polanya: (___)(),
        dimana ___ diisi dengan Function yang hendak dibuat dan tanda () kedua sebagai perintah eksekusi Function. Jika
        terdapat parameter & argument maka polanya (___)(argument), dimana argument diisi oleh nilai yang dikirim. 
      */

      render() {
        // 𝐒𝐓𝐄𝐏 𝟏: Sekarang temperature bukan lagi sebagai state lokal, melainkan berasal dari induknya
        // yaitu Kalkulator3, sebagai sebuah props. Dengan demikian, komponen InputTemperatur3
        // tidak memiliki kendali atasnya (ingat bahwa props bersifat read-only).
        const temperature = this.props.attTemperature
        const scale = this.props.attScale

        return (
          <fieldset>
            <legend>Masukkan temperature dalam {scale}:</legend>
            <input value={temperature} onChange={this.handleChange} />
          </fieldset>
        )
      }
    }

    // ------------------------------
    // B3. Komponen Orangtua (Parent)
    // ------------------------------

    class Kalkulator3 extends React.Component {
      constructor() {
        super()
        // 𝐒𝐓𝐄𝐏 𝟑: Sekarang temperature didefinisikan disini (Kalkulator3) sebagai state komponen induk,
        // yang kemudian akan diolah (dikonversi) untuk dikirimkan nantinya ke komponen InputTemperatur3.
        this.state = { scale: "c", temperature: "" }    // <- Nilai default
      }

      // 𝐒𝐓𝐄𝐏 𝟒: Function ini nantinya akan dikirim dan dijalankan di komponen InputTemperatur3.
      // Dalam object, jika "key: value" namanya sama maka cukup tulis salah satunya saja, pada
      // contoh di bawah "temperature: temperature" sebenarnya bisa ditulis "temperature" saja.
      handleCelsiusChange = temperature => this.setState({ scale: "c", temperature: temperature })
      handleFahrenheitChange = temperature => this.setState({ scale: "f", temperature: temperature })

      render() {
        // 𝐒𝐓𝐄𝐏 𝟓: State scale & temperature saat ini
        const scale = this.state.scale
        const temperature = this.state.temperature

        // Jika scale-nya fahrenheit, maka konversi temperature ke celcius, lalu masukkan ke dalam const celcius
        // (Ini berarti kita mendapatkan temperature celcius berdasarkan temperature fahrenheit yang ada saat ini).
        // Namun jika bukan (artinya scale-nya celcius), maka temperature saat ini langsung dimasukkan ke const celcius.
        const celsius = scale === "f" ? konversi(temperature, keCelsius) : temperature

        // Jika scale-nya celcius, maka konversi temperature ke fahrenheit, lalu masukkan ke dalam const fahrenheit.
        // (Ini berarti kita mendapatkan temperature fahrenheit berdasarkan temperature celcius yang ada saat ini).
        // Namun jika bukan (artinya scale-nya fahrenheit), maka temperature saat ini langsung dimasukkan ke const fahrenheit.
        const fahrenheit = scale === "c" ? konversi(temperature, keFahrenheit) : temperature

        // Tujuan dari baris kode di atas tidak lain untuk kebutuhan sinkronasi 2 inputan. Sederhananya: Saat ini kita input
        // temperature dalam scale celcius, maka dapatkan temperature dalam scale fahrenheit-nya, dan begitu sebaliknya.

        return (
          <div>
            <InputTemperatur3 attScale="Celcius" attTemperature={celsius} onTemperatureChange={this.handleCelsiusChange} />
            <InputTemperatur3 attScale="Fahrenheit" attTemperature={fahrenheit} onTemperatureChange={this.handleFahrenheitChange} />
            <Mendidih3 attDeg={parseFloat(celsius)} />
          </div>
        )
      }
    }

    ReactDOM.render(<Kalkulator3 />, document.getElementById('root3'))

  </script>
</body>

</html>
```

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*              Sinkronasi 2 Inputan (Simplified & Explained)              */
    /* ----------------------------------------------------------------------- */

    /* --------------------------------------------------------------------- */
    /* 𝐒𝐓𝐄𝐏 𝟏: Komponen KalkulatorSuhu yang menampilkan 2 komponen InputSuhu */
    /* --------------------------------------------------------------------- */

    class KalkulatorSuhu extends React.Component {
      constructor() {
        super()
        this.state = { skala: "celsius", suhu: "" } // <- Definisikan data state yang dibutuhkan nantinya
      }

      handleCelsiusChange = suhu => this.setState({ skala: "celsius", suhu: suhu })         // <- suhu nantinya akan didapat 
      handleFahrenheitChange = suhu => this.setState({ skala: "fahrenheit", suhu: suhu })   // <- dari event.target.value

      // Ingat: Dalam object jika "key: value" namanya sama, misal "suhu: suhu" maka sebenarnya cukup ditulis "suhu" saja

      render() {
        const skala = this.state.skala // <- Untuk menyingkat saja
        const suhu = this.state.suhu   // <- Untuk menyingkat saja

        /* ----------------------------------------------------------------------------------------------- */
        /* 𝐒𝐓𝐄𝐏 𝟐: Dapatkan data suhu dalam skala celsius & fahrenheit berdasarkan (inputan) suhu saat ini */
        /* ----------------------------------------------------------------------------------------------- */

        const celsius = skala === "fahrenheit" ? konversi(suhu, keCelsius) : suhu
        const fahrenheit = skala === "celsius" ? konversi(suhu, keFahrenheit) : suhu

        /* ----------------------------------------------------------------------------------------- */
        /* 𝐒𝐓𝐄𝐏 𝟒: Pakai komponen InputSuhu serta kirim data props yang diperlukan komponen tersebut */
        /* ----------------------------------------------------------------------------------------- */

        return (
          <div>
            <InputSuhu _title="Celsius" _suhu={celsius} _onSuhuChange={this.handleCelsiusChange} />
            <InputSuhu _title="Fahrenheit" _suhu={fahrenheit} _onSuhuChange={this.handleFahrenheitChange} />
            <h3>{celsius >= 100 ? "Air akan mendidih." : "Air tidak akan mendidih."}</h3>
          </div>
        )
      }
    }

    /* ------------------------------------- */
    /* 𝐒𝐓𝐄𝐏 𝟑: Definisikan function konversi */
    /* ------------------------------------- */

    const keCelsius = fahrenheit => (fahrenheit - 32) * 5 / 9
    const keFahrenheit = celsius => (celsius * 9 / 5) + 32

    function konversi(suhu, keSkala) {
      const input = parseFloat(suhu)        // <- Konversi string menjadi number (pecahan), selain number akan di-remove
      if (Number.isNaN(input)) return ""    // <- Cek apakah hasil konversi (input) berisi NaN, jika iya hentikan proses
      const output = keSkala(input)         // <- Jika skala saat ini celsius maka konversi ke fahrenheit & sebaliknya
      const rounded = Math.round(output * 1000) / 1000  // <- Pembulatan (jika pecahan, dibuat 3 angka di belakang koma)
      return rounded.toString()                         // <- Return hasil (yang sudah dibulatkan) dalam bentuk string
    }

    /* -------------------------------------- */
    /* 𝐒𝐓𝐄𝐏 𝟓: Definisikan komponen InputSuhu */
    /* -------------------------------------- */

    class InputSuhu extends React.Component {
      constructor(props) {
        super(props)
      }

      handleChange = event => this.props._onSuhuChange(event.target.value)

      /*
        A. Untuk celsius akan menjadi: 
        handleChange = event => this.props.handleCelsiusChange(event.target.value)

        B. Dibelakang layar handleCelsiusChange():
        (handleCelsiusChange = suhu => this.setState({ skala: "celsius", suhu: suhu }))(event.target.value)
        
        Dimana event.target.value bertindak sebagai argument dari function handleCelsiusChange(), maka yang
        terjadi ialah nilai state "suhu" akan diisi oleh event.target.value, kurang lebih seperti baris
        berikut -> this.setState({ skala: "celsius", suhu: event.target.value })

        C. Hal yang serupa terjadi juga untuk skala fahrenheit
      */

      render() {
        const title = this.props._title // <- Mengambil data props title
        const suhu = this.props._suhu   // <- Mengambil data props suhu

        return (
          <fieldset>
            <legend>Masukkan suhu dalam {title}:</legend>
            <input value={suhu} onChange={this.handleChange} />
          </fieldset>
        )
      }
    }

    ReactDOM.render(<KalkulatorSuhu />, document.getElementById('root'))

  </script>
</body>

</html>
```

</details>

## **11. Komposisi vs Pewarisan** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML

```

</details>

## **12. Cara Berpikir dengan React** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <title>Hello World</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="root"></div>

  <script type="text/babel">

    /* ----------------------------------------------------------------------- */
    /*                            Thinking in React                            */
    /* ----------------------------------------------------------------------- */

    /*

      𝐒𝐓𝐄𝐏 𝟏: Berangkat dari UI, berikut contoh UI yang digunakan:
      https://id.reactjs.org/static/1071fbcc9eed01fddc115b41e193ec11/d4770/thinking-in-react-mock.png

      𝐒𝐓𝐄𝐏 𝟐: Pecah UI menjadi hierarki komponen, berikut hasil pemecahan komponen:
      https://id.reactjs.org/static/eb8bda25806a89ebdc838813bdfa3601/6b2ea/thinking-in-react-components.png

      Hierarki-nya sebagai berikut:
      - <FilterableProductTable/>    (orange)      komponen utama
        - <SearchBar/>               (biru)        menerima inputan user
        - <ProductTable/>            (hijau)       show & filter data berdasarkan inputan user
          - <ProductCategoryRow/>    (biru muda)   show judul untuk setiap kategori
          - <ProductRow/>            (merah)       show baris untuk setiap produk

      Tips: Setiap komponen idealnya melakukan satu tugas tertentu saja.

      𝐒𝐓𝐄𝐏 𝟑: Buat versi statis (sederhana) terlebih dahulu
      - Gunakan props (sebuah cara mengoper data dari komponen parent ke child).
      - Untuk sementara jangan gunakan state (data yang nilai-nya berubah-ubah).
      - Mulai membangun komponen dari paling bawah ke komponen paling atas (meminimalisir bug).

      𝐒𝐓𝐄𝐏 𝟒: Identifikasi kebutuhan penggunaan state
      - Jika data dioper dari komponen induk melalui props, maka data tersebut bukanlah state.
      - Jika data tidak perlu berubah-ubah nilainya, maka data tersebut bukanlah state.
      
      Hasil identifikasi:
      - Daftar produk dioper ke dalam komponen melalui props, maka data tersebut bukanlah state.
      - Teks pencarian yang diinput user & nilai dari checkbox dapat berubah, maka data tersebut state.

      𝐒𝐓𝐄𝐏 𝟓: Identifikasi dimana state Anda berada
      - Prinsip dasar React yaitu aliran data satu arah yang mengalir ke bawah sejalan dengan hierarki komponen.
      - Cara 1 -> Temukan sebuah komponen yang menjadi pemilik bersama dari state, maka state disimpan disana.
      - Cara 2 -> Jika sulit, cukup buat komponen baru yang bertugas hanya untuk menyimpan state. Gunakan saat perlu.
      
      Hasil identifikasi:
      - <ProductTable/> perlu memfilter dafar produk berdasarkan state.
      - <SearchBar/> perlu menampilkan teks pencarian dan state dari checkbox.
      - Maka akan menjadi masuk akal apabila teks pencarian dan nilai dari checkbox berada di <FilterableProductTable/>.

      Implementasi:
      - Tambahkan this.state = {filterText: "", inStockOnly: false} di method constructor-nya <FilterableProductTable/>.
      - Hal tersebut akan merefleksikan kondisi state awal dari aplikasi Anda. 
      - Lalu oper "filterText" & "inStockOnly" ke <ProductTable/> & <SearchBar/> sebagai sebuah props. 
      - Gunakan props tersebut untuk memfilter baris di <ProductTable/> dan set nilai dari field di <SearchBar/>.

      𝐒𝐓𝐄𝐏 𝟔: Tambahkan aliran data ke arah sebaliknya
      - Komponen form yang berada di bawah hierarki perlu untuk memberbarui state di <FilterableProductTable/>.
      - Artinya saat user mengubah form, state akan di-update sesuai inputan user.
      - Karena state hanya dapat di-update di <FilterableProductTable/>, maka <FilterableProductTable/> akan mengoper
        callback ke <SearchBar/> yang kemudian akan dipanggil kapanpun state harus di-update.

    */

    /* ----------------------------------------------------------------------- */
    /*                     Komponen: <ProductCategoryRow/>                     */
    /* ----------------------------------------------------------------------- */

    class ProductCategoryRow extends React.Component {
      render() {
        const category = this.props.category

        return (
          <tr>
            <th colSpan="2">{category}</th>
          </tr>
        )
      }
    }

    /* ----------------------------------------------------------------------- */
    /*                         Komponen: <ProductRow/>                         */
    /* ----------------------------------------------------------------------- */

    class ProductRow extends React.Component {
      render() {
        const product = this.props.product

        // Jika product.stocked false beri warna merah pada nama produk tersebut
        const name = product.stocked ? product.name : <span style={{ color: "red" }}>{product.name}</span>

        return (
          <tr>
            <td>{name}</td>
            <td>{product.price}</td>
          </tr>
        )
      }
    }

    /* ----------------------------------------------------------------------- */
    /*                        Komponen: <ProductTable/>                        */
    /* ----------------------------------------------------------------------- */

    class ProductTable extends React.Component {
      render() {
        const filterText = this.props.filterText
        const inStockOnly = this.props.inStockOnly

        const rows = []
        let lastCategory = null

        // Jalankan perintah berikut untuk setiap data produk. Setiap produk berisi: category, price, stocked, name.
        this.props.products.forEach(product => {

          /*
            Cek apakah (string) filterText ada di dalam (string) product.name, stop (return) jika tidak ditemukan
            (-1 artinya string tidak ditemukan). Misalnya, filterText berisi string "od" & product.name berisi string 
            "iPod", oleh karena "od" ada di dalam "iPod" maka lolos pengecekan dan lanjut ke baris kode selanjutnya.
            Catatan, dalam contoh disini pencarian bersifat case sensitive, itu berari "foot" dengan "Foot" berbeda.
          */
          if (product.name.indexOf(filterText) === -1) return

          /*
            Cek apakah inStockOnly true (checkbox di centang)? Jika ya, cek lagi apakah product.stocked false? Jika ya lagi
            maka stop (return), artinya produk yang tidak ada stoknya tidak akan ditampilkan (tidak di push ke array rows).
          */
          if (inStockOnly && !product.stocked) return

          /*
            Tujuan baris kode ini untuk menampilkan nama setiap kategori ke dalam tabel agar tampil 1x saja (tidak berulang),
            ini berarti nama setiap kategori hanya akan 1x saja di push ke array rows. Teknisnya, lastCategory berperan
            untuk pengecekan, jika product.category != null (hanya di cek pertama kali, sudah pasti hasilnya true) maka push
            product.category tersebut ke dalam array rows. Jika product.category == lastCategory (artinya product.category
            tersebut sebelumnya sudah di push ke array rows), maka skip, namun jika product.category != lastCategory
            (artinya product.category tersebut memang baru dan belum pernah di push), maka push ke array rows.
          */
          if (product.category !== lastCategory) rows.push(<ProductCategoryRow category={product.category} key={product.category} />)
          lastCategory = product.category

          // Tujuan baris kode ini untuk menampilkan data produk ke dalam tabel (push data produk ke array rows)
          rows.push(<ProductRow product={product} key={product.name} />)
        })

        return (
          <table border="1" width="172px">
            <thead>
              <tr>
                <th>Name</th>
                <th>Price</th>
              </tr>
            </thead>
            <tbody>{rows}</tbody>
          </table>
        )
      }
    }

    /* ----------------------------------------------------------------------- */
    /*                         Komponen: <SearchBar/>                          */
    /* ----------------------------------------------------------------------- */

    class SearchBar extends React.Component {
      
      handleFilterTextChange = event => this.props.onFilterTextChange(event.target.value) // <- value
      handleInStockChange = event => this.props.onInStockChange(event.target.checked)     // <- checked
      
      /*
        Baris kode di atas akan mengupdate state filterText & inStockOnly berdasarkan inputan user saat ini.

        Yang terjadi di belakang layar:
        - handleFilterTextChange = event => this.props.handleFilterTextChangeRoot(event.target.value)
        - handleInStockChange = event => this.props.handleInStockChangeRoot(event.target.checked)

        Dimana handleFilterTextChangeRoot() & handleInStockChangeRoot() berasal dari <FilterableProductTable/>
        yang di oper ke dalam <SearchBar/> melalui props. Dengan inilah state filterText & inStockOnly di 
        <FilterableProductTable/> dapat ter-update melalui komponen <SearchBar/> ini.       
      */

      render() {
        return (
          <form>
            <input type="text" placeholder="Search..." value={this.props.filterText} onChange={this.handleFilterTextChange} />
            <p>
              <input type="checkbox" checked={this.props.inStockOnly} onChange={this.handleInStockChange} />Only show products in stock
            </p>
          </form>
        )
      }
    }

    /* ----------------------------------------------------------------------- */
    /*                   Komponen: <FilterableProductTable/>                   */
    /* ----------------------------------------------------------------------- */

    class FilterableProductTable extends React.Component {
      constructor(props) {
        super(props)
        this.state = {
          filterText: "",
          inStockOnly: false
        }
      }

      handleFilterTextChangeRoot = value => this.setState({ filterText: value })
      handleInStockChangeRoot = value => this.setState({ inStockOnly: value })

      render() {
        return (
          /*
            Props filterText & inStockOnly pada <SearchBar/> digunakan untuk set nilai dari field pada form,
            atau dengan kata lain untuk kebutuhan update state. Proses update state dilakukan di <SearchBar/>.
            Props filterText & inStockOnly pada <ProductTable/> digunakan untuk memfilter baris.
          */
          <div>
            <SearchBar
              filterText={this.state.filterText}
              inStockOnly={this.state.inStockOnly}
              onFilterTextChange={this.handleFilterTextChangeRoot}
              onInStockChange={this.handleInStockChangeRoot}
            />
            <ProductTable
              products={this.props.products}
              filterText={this.state.filterText}
              inStockOnly={this.state.inStockOnly}
            />
          </div>
        )
      }
    }

    /* ----------------------------------------------------------------------- */
    /*                              Data & Render                              */
    /* ----------------------------------------------------------------------- */

    const PRODUCTS = [
      { category: 'Sporting Goods', price: '$49.99', stocked: true, name: 'Football' },
      { category: 'Sporting Goods', price: '$9.99', stocked: true, name: 'Baseball' },
      { category: 'Sporting Goods', price: '$29.99', stocked: false, name: 'Basketball' },
      { category: 'Electronics', price: '$99.99', stocked: true, name: 'iPod Touch' },
      { category: 'Electronics', price: '$399.99', stocked: false, name: 'iPhone 5' },
      { category: 'Electronics', price: '$199.99', stocked: true, name: 'Nexus 7' }
    ]

    ReactDOM.render(<FilterableProductTable products={PRODUCTS} />, document.getElementById("root"))

  </script>
</body>

</html>
```

</details>

## **13. React Advanced Guides [Summary]** <a href="#top">⟲</a>

<details>
<summary>Klik untuk membuka!</summary><br>

## A. Aksesibilitas

### 1. HTML semantik

- Ganti wrapper ```<div></div>``` di return value dari sebuah komponen menjadi ```<React.Fragment></React.Fragment>```.
- Atau jika wrapper tidak membutuhkan props cukup gunakan ```<></>``` saja (a11y best practice).

### 2. Form yang aksesibel

- Berikan pesan kesalahan (error notification/feedback) ke user, misalnya pada saat salah input format di form.
- Setiap element form seperti ```<input>``` dan ```<textarea>``` perlu diberi label (di JSX for menjadi htmlFor), misalnya:

```HTML
<label htmlFor="namedInput">Name:</label>
<input id="namedInput" type="text" name="name">
```

### 3. Focus control, mouse & pointer events

- Pastikan focus keyboard dan garis luar focus terlihat dengan jelas, jangan coba-coba dihilangkan dengan CSS.
- Pastikan fungsionalitas mouse & pointer events juga dapat diakses dengan menggunakan keyboard (Tab & Shift+Tab).
- Uji apakah seluruh web Anda dapat dijangkau hanya dengan menggunakan keyboard (Tab, Shift+Tab, Enter & Arrow keys).

### 4. Widget yang lebih kompleks

- Aksesibilitas paling mudah dicapai dengan menulis kode yang sedekat mungkin dengan HTML.
- Pelajari ARIA in HTML. Kunjungi web berikut ini: https://inclusive-components.design/.

### 5. Hal-hal lain yang perlu dipertimbangkan

- Mengatur bahasa yang digunakan web. Pertimbangkan penggunaan multi-bahasa.
  - Resource: https://react.i18next.com/.
- Mengatur document title ```<title>``` agar menggambarkan dengan tepat isi halaman yang sedang dibuka.
  - Resource: https://github.com/gaearon/react-document-title
- Pastikan seluruh teks yang dapat dibaca di web memiliki kontras warna yang cukup.
  - Resource: http://colorsafe.co/ & https://jxnblk.github.io/colorable/
- Periksa beberapa fitur aksesibilitas secara langsung dalam kode JSX Anda.
  - Resource: https://github.com/jsx-eslint/eslint-plugin-jsx-a11y
- Uji aksesibilitas (teknis kode HTML Anda) di browser secara langsung.
  - Resource: https://www.deque.com/axe/ & https://wave.webaim.org/extension/
- Uji responsive (pengalaman mengakses web yang optimal dalam berbagai device).
  - Resource: http://iloveadaptive.com/, http://responsivetesttool.com/ & https://webmobilefirst.com/
- Uji konten (text) di web Anda menggunakan pembaca layar (screen reader).
  - Resource: https://www.naturalreaders.com/ & https://getpericles.com/

## B. Code-Splitting

Code-splitting pada aplikasi Anda dapat dimanfaatkan untuk melakukan “lazy-load” untuk memuat hanya hal-hal yang sedang dibutuhkan oleh pengguna saja, yang dapat meningkatkan performa aplikasi Anda secara drastis. Pelajari modul ```import()```, ```export()```, dan ```React.lazy()```.

## C. Context
 
Dalam aplikasi React data dioper dari komponen atas ke bawah (parent ke child) melalui props, tetapi ini bisa menjadi rumit untuk tipe props tertentu yang dibutuhkan oleh banyak komponen. **Context** dirancang untuk berbagi data yang dapat dianggap "global", seperti tema, bahasa yang disukai hingga cache data. Terkadang data yang sama harus dapat diakses oleh banyak komponen pada tingkat bersarang yang berbeda. Context memungkinkan Anda “menyiarkan” data tersebut, dan mengubahnya, ke semua komponen di bawah.

Sebelum Anda menggunakan Context: Jika Anda hanya ingin menghindari mengoper beberapa props melalui banyak tingkatan, **Component Composition** seringkali menjadi solusi yang lebih sederhana daripada Context.

**Catatan**: Dalam React terbaru (Hooks), Anda dapat menggunakan ```useContext()``` sebagai pengganti context tradisional.

## D. Error Boundaries

Sebuah class component menjadi komponen error boundary jika komponen tersebut mendefinisikan salah satu (atau kedua) metode lifecycle static: ```getDerivedStateFromError()``` untuk me-render antarmuka darurat saat kesalahan dilontarkan & ```componentDidCatch()``` untuk mencatat informasi kesalahan. Error boundaries bekerja seperti blok JavaScript ```catch {},``` tetapi diperuntukkan bagi komponen. Hanya komponen kelas yang bisa menjadi komponen error boundaries.

## E. Forwarding Refs

Forwarding Refs adalah sebuah teknik untuk meneruskan ref secara otomatis melalui komponen ke salah satu anaknya. Ini biasanya tidak diperlukan untuk sebagian besar komponen dalam aplikasi. Namun, ini bisa berguna untuk beberapa jenis komponen, terutama pada reusable component libraries. Forwarding Refs adalah sebuah fitur keikutsertaan yang memperbolehkan beberapa komponen-komponen mengambil sebuah ref yang didapatkan, dan menurunkannya (dengan kata lain, “meneruskan” nya) kepada child.

## F. Fragments

Salah satu pola umum pada React adalah return banyak elemen sekaligus. Fragments memungkinkan Anda untuk mengelompokkan sejumlah elemen anak tanpa perlu menambahkan lagi node ekstra ke DOM. Teknisnya gunakan ```<React.Fragment></React.Fragment>``` atau ```<></>``` sebagai wrapper untuk return value sebuah komponen. Sebelum ada fragments ini, biasanya menggunakan ```<div></div>``` sebagai wrapper.

## G. Higher-Order Components

Higher-order component (HOC) merupakan teknik lanjutan dalam React untuk menggunakan kembali logika sebuah komponen. Konkritnya, HOC merupakan fungsi yang mengambil sebuah komponen dan mengembalikan sebuah komponen baru. Kita ingin sebuah abstraksi yang mengizinkan kita mendefinisikan logika ini pada satu tempat dan membaginya antar komponen. Dalam kondisi inilah, HOC digunakan.

**Catatan**: Secara tradisional ada 2 solusi untuk masalah menggunakan kembali logika stateful antar komponen, yaitu dengan Higher-Order Components dan Render Props. Namun, dalam React terbaru (Hooks), sebagai gantinya Anda dapat menggunakan Custom Hooks.

## H. Integrasi dengan Library Lain

React dapat digunakan pada web application apapun. React juga dapat ditanamkan di aplikasi lain (misal jQuery dan Backbone), begitu juga sebaliknya, dengan sedikit pengaturan, aplikasi lain dapat ditanamkan di React. Jika tertarik baca di official dokumentasi React.

## I. JSX In Depth

Pada dasarnya, JSX hanya menyediakan sintaksis-sintaksis yang mudah ditulis dan dimengerti (syntatic sugar) untuk fungsi React berikut: ```React.createElement(component, prop, ...children)```. Misalnya kode JSX ```<MyButton color="blue" shadowSize={2}>Klik saya</MyButton>``` akan di-compile menjadi ```React.createElement(MyButton, {color: 'blue', shadowSize: 2}, 'Klik saya')```.

## J. Mengoptimalkan Performa

Secara internal, React menggunakan beberapa teknik cermat untuk meminimalkan jumlah operasi DOM boros yang diperlukan untuk memperbarui UI. Bagi sebagian besar aplikasi, React akan menghasilkan UI yang cepat tanpa harus melakukan pekerjaan tambahan untuk mengoptimalkan performa secara spesifik. Meskipun demikian, ada beberapa cara untuk mempercepat aplikasi React Anda:

1. Gunakan versi produksi. Ingat bahwa hanya file React yang berakhir dengan ```.production.min.js``` yang layak digunakan untuk produksi.
2. Memvirtualisasi Long List. Jika aplikasi Anda me-render list data yang panjang (ratusan/ribuan baris), kami sarankan untuk menggunakan teknik “windowing”. Teknik ini hanya me-render bagian kecil dari baris-baris data Anda dalam waktu tertentu. <a href="https://react-window.vercel.app/">react-window</a> dan <a href="https://bvaughn.github.io/react-virtualized/">react-virtualized</a> merupakan library windowing paling populer yang bisa Anda gunakan.
3. Meskipun React hanya memperbarui simpul DOM yang berubah, me-render ulang tetap memerlukan waktu tambahan. Dalam banyak kasus ini tidak menjadi masalah, namun ketika ada perlambatan yang signifikan, Anda dapat mempercepatnya dengan meng-override lifecycle ```shouldComponentUpdate()``` yang dijalankan sebelum proses render ulang dimulai. Dalam banyak kasus, alih-alih menuliskan ```shouldComponentUpdate()``` secara manual, Anda dapat meng-inherit dari ```React.PureComponent``` (helper khusus yang disediakan React).
4. Ketika berurusan dengan objek bersarang yang dalam, memperbaruinya secara immutable dapat menjadi sulit. Jika Anda memiliki masalah ini, cobalah <a href="https://github.com/immerjs/immer">Immer</a> atau <a href="https://github.com/kolodny/immutability-helper">immutability-helper</a>. Library ini memungkinkan Anda membuat kode yang lebih mudah dibaca tanpa menanggalkan keuntungan-keuntungan immutability.

## K. Portal

Portal menyediakan sebuah cara utama untuk me-render anak ke dalam simpul DOM yang berada di luar hierarki komponen induk. ```ReactDOM.createPortal(child, container)```, dimana Argumen pertama (child) berupa anak React yang bisa di-render, misalnya sebuah elemen, string, atau fragment. Argumen kedua (container) merupakan elemen DOM. Penggunaan umum untuk portal adalah ketika komponen induk memiliki style ```overflow: hidden``` atau ```z-index```, tetapi Anda harus “memisahkan” anak secara visual dari kontainernya. Misal dialog/tooltip.

## L. Profiler

Profiler mengukur seberapa sering aplikasi React dirender dan berapa "cost" renderingnya. Tujuannya adalah untuk membantu meng-identifikasi bagian dari aplikasi yang lambat dan dapat mengambil manfaat dari pengoptimalan seperti memoization. Meskipun Profiler komponen yang ringan, gunkan hanya jika diperlukan; setiap penggunaan menambah beberapa overhead CPU & memori ke aplikasi.

## M. React Tanpa ES6

Jika menemukan syntax/modul berikut dalam sebuah project React, artinya project tersebut belum menggunakan ES6: 
- ```var createReactClass = require('create-react-class')``` ➜ Membuat sebuah komponen class
- ```getDefaultProps()``` ➜ Mendeklarasikan props default
- ```getInitialState()``` ➜ Menyetel state awal
- ```mixins``` ➜ React tidak menyarankan Anda menggunakan mixin

## N. React Tanpa JSX

Jika Anda menemukan syntax/modul ```React.createElement()``` (baris perintah ini bertujuan untuk membuat sebuah element) dalam sebuah project React, artinya project tersebut (atau terdapat bagian dari projecy tersebut) tidak memakai JSX.

## O. Rekonsiliasi

Rekonsilisasi berarti perbuatan menyelesaikan perbedaan. React menyediakan API deklaratif jadi Anda tidak perlu khawatir tentang apa yang pasti berubah pada setiap pembaruan. Ini membuat penulisan aplikasi menjadi lebih mudah. Semua ini karena The Diffing Algorithm-nya React.

## P. Ref dan DOM

Ref menyediakan cara untuk mengakses simpul DOM atau elemen React yang dibuat dalam render method. Dalam aliran data React yang umum, props adalah satu-satunya cara bagi komponen induk untuk berinteraksi dengan anaknya. Untuk memodifikasi anak, Anda me-render ulang dengan props yang baru. Tetapi ada beberapa kasus ketika Anda harus memodifikasi anak secara imperatif di luar aliran data yang umum. Anak yang akan dimodifikasi bisa berupa komponen React atau elemen DOM. Pada kedua kasus ini, React menyediakan jalan keluar. 

Hindari penggunaan ref untuk semua yang bisa dilakukan secara deklaratif, jangan berlebihan menggunakan ref, karena mungkin Anda tergoda menggunakan ref agar aplikasi "dapat berfungsi". Pada React 16.3 diperkenalkan ```React.createRef()``` sebagai cara baru untuk ```callback ref```. Lalu kapan Ref digunakan? Berikut beberapa contoh kasus:
- Mengelola focus, text selection, atau media playback.
- Memicu imperative animations.
- Mengintegrasikan dengan library DOM pihak ketiga.

**Catatan**: Dalam React terbaru (Hooks), Anda dapat menggunakan ```useRef()``` sebagai pengganti ref tradisional.

## Q. Render Props

Istilah ”render props” merujuk kepada sebuah teknik untuk berbagi kode antara komponen React menggunakan suatu prop yang nilainya merupakan suatu fungsi. Sebuah komponen dengan render props mengambil suatu fungsi yang mengembalikan suatu elemen React dan memanggilnya alih-alih mengimplementasikan logika render-nya sendiri. Secara lebih konkrit, sebuah render props adalah suatu prop berupa sebuah fungsi yang digunakan suatu komponen untuk mengetahui apa yang harus ia render. 

Library yang menggunakan render props termasuk <a href="https://reactrouter.com/">React Router</a> dan <a href="https://github.com/downshift-js/downshift">Downshift</a>. Sebagai catatan, berhati-hatilah ketika menggunakan render props dengan ```React.PureComponent()```, karena dapat menghilangkan keuntungan dari ```React.PureComponent()``` itu sendiri.

**Catatan**: Secara tradisional ada 2 solusi untuk masalah menggunakan kembali logika stateful antar komponen, yaitu dengan Higher-Order Components dan Render Props. Namun, dalam React terbaru (Hooks), sebagai gantinya Anda dapat menggunakan Custom Hooks.

## R. Pengecekan Static Type

Pengecekan static type dapat mengidentifikasi jenis masalah tertentu bahkan sebelum kode dijalankan. Secara bawaan React memiliki <a href="https://www.npmjs.com/package/prop-types">propTypes</a> untuk pengecekan type (data). Namun untuk aplikasi yang berukuran besar lebih disarankan menggunakan <a href="https://www.typescriptlang.org/">TypeScript</a> atau <a href="https://flow.org/">Flow</a>. 

Create React App (CRA) mendukung TypeScript secara langsung. Anda dapat membuat sebuah proyek CRA baru dengan dukungan TypeScript atau menambahkan TypesScript pada proyek CRA yang sudah ada, selebihnya kunjungi <a href="https://create-react-app.dev/docs/adding-typescript/">link berikut ini</a>.

## S. Mode Ketat (Strict Mode)

Mode Ketat (Strict Mode) merupakan alat untuk menyoroti potensi masalah dalam aplikasi. Seperti halnya Fragment, ```<React.StrictMode></React.StrictMode>``` tidak me-render antarmuka yang tampak. Mode ini mengaktifkan pemeriksaan dan peringatan ekstra untuk turunannya. Pemeriksaan mode ketat hanya berjalan dalam mode pengembangan. Mode ini tidak berdampak dalam build produksi.

## T. Pengecekan Tipe Dengan propTypes

Dengan berkembangnya aplikasi Anda, Anda dapat menemukan banyak kesalahan atau bugs dengan pengecekan tipe (data). React memiliki kemampuan pengecekan tipe. Untuk menjalankan pengecekan terhadap props disebuah komponen, Anda dapat menggunakan properti khusus ```propTypes```. Berikut contoh penggunaanya:

```JavaScript
import PropTypes from 'prop-types';

class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>
  }
}

Greeting.propTypes = {
  name: PropTypes.string // <- Tipe data String
}
```

Selain String tentunya terdapat banyak validator yang disediakan React, seperti ```array```, ```bool```, ```func```, ```number```, ```object```, ```string```, ```symbol```, ```node``` (any/apapun), ```element``` (element React), ```elementType``` (tipe element React), dan masih banyak lagi, selebihnya kunjungi <a href="https://id.reactjs.org/docs/typechecking-with-proptypes.html">link berikut ini</a>.

## U. Uncontrolled Component

Pada banyak kasus, kami sarankan untuk menggunakan controlled component untuk implementasi form (lihat bagian **9. Form di React**). Pada controlled component, data form ditangani oleh komponen React. Cara alternatifnya adalah menggunakan uncontrolled component, di mana data form akan ditangani oleh DOM-nya sendiri. Untuk menulis uncontrolled component, alih-alih menulis event handler untuk setiap pembaruan state, Anda bisa menggunakan ref untuk mendapatkan nilai form dari DOM. Pelajari lebih lanjut di <a href="https://goshacmd.com/controlled-vs-uncontrolled-inputs-react/">link berikut ini</a> dan <a href="https://id.reactjs.org/docs/uncontrolled-components.html">ini</a>.

Sebagai catatan, pada element form di React gunakan ```defaultValue``` alih-alih ```value```, serta gunakan ```defaultChecked``` alih-alih ```checked```.

## V. Web Components

<a href="https://www.webcomponents.org/introduction">Web Components</a> adalah rangkaian teknologi yang memungkinkan Anda membuat elemen kustom yang dapat digunakan kembali (reusable), layaknya React. Namun, React dan Web Components dibangun untuk menyelesaikan masalah yang berbeda. Web Components menyediakan enkapsulasi yang kuat untuk reusable components, sementara React menyediakan library yang deklaratif untuk menjaga DOM tetap sinkron dengan data Anda. Tujuan keduanya adalah untuk saling melengkapi. 

Sebagai developer, Anda bebas untuk menggunakan React di dalam Web Components Anda, atau menggunakan Web Components di dalam React, ataupun keduanya. Namun kebanyakan orang yang menggunakan React tidak menggunakan Web Components.

</details>
