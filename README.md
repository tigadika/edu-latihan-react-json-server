# Latihan Live Code 1 Phase 1 Batch 06

Dalam latihan ini, tugas kalian adalah membuat aplikasi movie seperti contoh dibawah ini (layout dan styling tidak perlu sama)

![movie app](/movie.png)

- Terdapat Navbar
- Terdapat List Movie
- Terdapat Tombol Filter Movie

## Data dan server

Agar aplikasi kalian dapat memunculkan data, maka kalian membutuhkan server. Disini telah disediakan file .json yang dapat menjadi mock server dan database kalian. Kalian hanya perlu setup menggunakan json server

> Langkah-langkah:
>
> - buka terminal di folder server
> - jalankan `npm init -y` (untuk inisiasi npm)
> - install json server `npm install json-server`
> - jalankan json server `npx json-server db.json`
> - rest api kalian sudah siap. Jangan tutup terminalnya!

## Client

Setelah kalian mempunyai rest api, maka selanjutnya adalah membuat aplikasinya menggunakan React

> Langkah-langkah setup:
>
> - buka terminal yang baru (jangan tutup terminal server yang tadi karena kita butuh servernya tetap berjalan)
> - `npm create vite@latest`
> - masukan nama project, pilih react, pilih Javascript
> - setelah beres, ikuti petunjuk selanjutnya (`cd <nama_project>`, `npm install`, `npm run dev`)
> - install css kesayangan kalian
> - install axios `npm i axios`
> - install react router `npm i react-router-dom@6.28.2`
> - mulai ngoding!

Untuk mengambil data dari json server, biasanya urlnya akan berbentuk seperti ini `http://localhost:3000/movies`

Dengan `http://localhost:3000` sebagai host/base urlnya dan `/movies` sebagai routes/endpointnya

### Mengambil semua data movies

Ambillah semua data movies dari endpoint `/movies` lalu tampilkan di halaman home dengan method `GET`

contoh cara axios:

```js
const response = await axios('http://localhost:3000/movies' {
  method: 'GET'
})
```

### Mengambil data berdasarkan genre

Dalam data json tersebut terdapat genre, kalian bisa melakukan filter di dalam json server tersebut dengan menambahkan `?genre=<nama_genre>` setelah endpointnya

> `http://localhost:3000/movies?genre=Action`

contoh cara axios:

```js
const genre = 'Action'
const response = await axios(`http://localhost:3000/movies?genre=${genre}` {
  method: 'GET'
})
```
