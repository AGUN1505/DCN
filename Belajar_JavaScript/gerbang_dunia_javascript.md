# Apa Itu Pemrograman

Pemrograman adalah proses atau kegiatan membuat instruksi yang sistematis untuk berinteraksi dengan komputer dalam memecahkan permasalahan. Manusia membuat beberapa instruksi yang harus dieksekusi oleh komputer dalam bahasa yang dimengertinya, yaitu **bahasa pemrograman**.

Masih ada banyak hal lainnya yang bisa dilakukan oleh komputer melalui programming. Tingkat kompleksitas program berbanding lurus dengan jumlah instruksi. Artinya, semakin besar tugas komputer, semakin banyak instruksi yang harus disusun. Bahkan, tidak jarang sebuah program memiliki **ratusan, ribuan, hingga jutaan instruksi** yang terstruktur.

---

# Scripting dan Compiled Language

Komputer memerlukan bahasa khusus agar perintah dapat dieksekusi dengan benar. Perintah-perintah tersebut ditulis oleh developer dalam bentuk **kode**. Kode ini dipahami oleh manusia dan disebut sebagai **bahasa tingkat tinggi**.

Beberapa contoh bahasa pemrograman:

* JavaScript
* Java
* C
* C++
* Python
* Matlab

Hasil dari kegiatan menulis kode disebut **source code**. Selanjutnya, source code akan diubah menjadi **bahasa tingkat rendah (bahasa mesin)** agar bisa dipahami dan dieksekusi oleh komputer. Bahasa mesin sangat sulit dipahami manusia dan hanya dimengerti oleh komputer.

Dalam proses perubahan dari bahasa tingkat tinggi ke bahasa tingkat rendah, terdapat dua mekanisme utama:

* **Compiler**
* **Interpreter**

---

## Compiled Language

Pada compiled language, source code harus melalui proses **kompilasi** terlebih dahulu sebelum dijalankan oleh mesin. Proses ini akan mengubah kode menjadi bahasa mesin secara keseluruhan sebelum dieksekusi.

---

## Scripting Language

Berbeda dengan compiled language, scripting language **tidak memerlukan proses kompilasi terlebih dahulu**. Source code akan langsung diterjemahkan dan dijalankan oleh mesin menggunakan **interpreter**.

Contoh yang paling dekat dengan kehidupan sehari-hari adalah **browser**.

---

# Pengenalan JavaScript

JavaScript merupakan salah satu bahasa pemrograman yang menggunakan **interpreter (scripting language)**. Artinya, kode JavaScript dapat langsung dijalankan tanpa proses kompilasi.

Kode akan diterjemahkan dan dieksekusi **baris demi baris**. Jika terjadi kesalahan, error akan langsung muncul saat **runtime** (program sedang berjalan).

Seiring perkembangan teknologi, JavaScript kini tidak hanya digunakan di browser, tetapi juga di berbagai platform lain, seperti:

* Server
* Desktop
* Database

Hal ini dimungkinkan berkat **JavaScript runtime**, seperti:

* Node.js
* Bun

Bahkan, beberapa **DBMS** seperti **MongoDB** menggunakan JavaScript sebagai bahasa scripting dan query.

---

# Sejarah JavaScript

Berdasarkan survei **Statista tahun 2023**, JavaScript menempati peringkat teratas sebagai bahasa pemrograman yang paling banyak digunakan developer.

JavaScript pertama kali dikembangkan pada **tahun 1995** oleh **Brendan Eich** dari perusahaan **Netscape**. Awalnya, bahasa ini diberi nama **LiveScript**, namun kemudian diubah menjadi **JavaScript** agar lebih populer dengan memanfaatkan nama bahasa Java.

JavaScript kemudian distandardisasi oleh organisasi **ECMA** dalam bentuk standar **ECMAScript**, yang mengatur spesifikasi dan cara kerja JavaScript agar konsisten di berbagai platform.

### Perkembangan ECMAScript

| Tahun         | Keterangan                                                                                                     |
| ------------- | -------------------------------------------------------------------------------------------------------------- |
| 2000–2010     | ECMAScript 3 menjadi versi yang paling banyak digunakan. Pengembangan ECMAScript 4 dihentikan pada tahun 2008. |
| 2009          | Dirilis ECMAScript 5 dengan perbaikan yang tidak kontroversial.                                                |
| 2015          | Dirilis ECMAScript 6 dengan peningkatan besar dan fitur baru.                                                  |
| 2015–sekarang | ECMAScript terus diperbarui setiap tahun dengan peningkatan kecil.                                             |

---

# JavaScript Runtime Environment

**Runtime environment** adalah tempat sebuah program JavaScript dieksekusi. Runtime ini menentukan **global object** yang dapat diakses oleh program.

Tiga runtime environment JavaScript yang umum digunakan:

* Browser
* Node.js
* Bun

---

## Browser

Sebagian besar program JavaScript dijalankan di browser. Contoh penggunaan JavaScript secara langsung di dalam HTML (**embedded JavaScript**):

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My Website</h1>

    <script>
      window.alert('Hello, world!');
    </script>
  </body>
</html>
```

Kode JavaScript tersebut dibungkus dalam elemen `<script>` dan akan dijalankan saat halaman dibuka.

---

## External JavaScript

JavaScript juga dapat ditulis dalam berkas terpisah dengan ekstensi `.js`.

**index.html**

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>My Website</h1>

    <script src="index.js"></script>
  </body>
</html>
```

**index.js**

```javascript
window.alert('Hello, world!');
```

Pendekatan ini membuat kode lebih rapi dan mudah dikelola.

---

## REPL Versi Browser

Browser juga menyediakan **REPL (Read-Eval-Print-Loop)** melalui **Developer Tools**.

Langkah-langkah:

1. Buka browser
2. Buka Developer Tools
3. Masuk ke tab **Console**
4. Tulis kode JavaScript dan tekan Enter

---

## Node.js

Node.js adalah runtime JavaScript di luar browser. Semua fitur dasar JavaScript tetap tersedia, tetapi tidak memiliki akses ke global object browser seperti `window` atau `alert`.

Sebagai gantinya, Node.js menyediakan akses ke:

* File system
* Database
* Sistem operasi

Contoh kode:

```javascript
console.log(process.platform);
```

Kode tersebut mengakses global object `process` untuk mengetahui sistem operasi yang digunakan.

Untuk menjalankan berkas JavaScript:

```bash
node app.js
```

Node.js juga menyediakan **REPL**:

1. Buka terminal
2. Jalankan perintah `node`
3. Tulis kode JavaScript
4. Tekan Enter

---

## Bun

**Bun** adalah JavaScript runtime modern yang mengutamakan kecepatan dan kompatibilitas dengan ekosistem Node.js.

Untuk menjalankan berkas JavaScript:

```bash
bun run app.js
```

Atau langsung:

```bash
bun app.js
```

Untuk menggunakan REPL:

```bash
bun repl
```
