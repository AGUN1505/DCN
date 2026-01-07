# Expression dan Statement

Pemrograman pada dasarnya adalah cara kita berkomunikasi dengan komputer. Komunikasi ini dilakukan dengan memberikan instruksi agar komputer dapat menjalankan tugas tertentu dengan benar. Tentu saja, instruksi tersebut harus mengikuti aturan yang telah ditentukan.

Dalam pemrograman, **satu instruksi umumnya ditulis dalam satu baris kode**. Jadi, jika ada tiga instruksi, biasanya ditulis dalam tiga baris kode. Istilah untuk “instruksi” dalam bahasa pemrograman disebut **statement**.

**Kesimpulan:**

> **Statement** adalah instruksi yang akan dieksekusi oleh komputer.

---

## Expression

Selain statement, ada istilah penting lainnya, yaitu **expression**. Expression adalah bagian dari sebuah statement yang **menghasilkan nilai**. Hampir setiap statement minimal memiliki satu expression.

Contoh:

```javascript
const age = 10;
const name = 'Dicoding';
console.log(`Aku ${name}, umurku ${age} tahun.`);
```

Expression pada kode di atas antara lain:

* Nilai `10`
* Teks `'Dicoding'`
* Teks `Aku Dicoding, umurku 10 tahun.`

Expression inilah yang diolah oleh komputer untuk menghasilkan output.

---

# Comment

**Comment (komentar)** adalah teks penjelasan dalam kode yang ditujukan untuk programmer, bukan untuk dieksekusi oleh komputer. Komentar akan diabaikan oleh interpreter.

Pada JavaScript, komentar dapat ditulis dengan dua cara:

---

## Single-line Comment (`//`)

```javascript
// Teks ini akan diabaikan oleh interpreter
console.log('Hai, Readers!');
console.log('Hai, JavaScript!');
// console.log('Hai, Dicoding!');
```

---

## Multi-line Comment (`/* */`)

```javascript
/*
 TODO
 1. Buatlah variabel bernama PI dan isikan dengan nilai 3.14
 2. Cetak nilai variabel PI di terminal menggunakan console.log
*/
 
const PI = '3.14';
console.log(PI);
```

---

# Variabel

**Variabel** adalah wadah untuk menyimpan sebuah nilai. Nilai tersebut bisa berupa angka, teks, atau hasil dari expression.

Dalam JavaScript, variabel dapat dibuat menggunakan:

* `const`
* `let`

### Perbedaan `const` dan `let`

* `const` → nilai **tidak bisa diubah**
* `let` → nilai **bisa diubah**

Variabel yang dibuat dengan `const` sering disebut **constant (konstanta)** karena nilainya tetap.

---

## Aturan Penamaan Variabel

Dalam JavaScript, nama variabel **tidak boleh sembarangan**. Aturannya:

1. Tidak boleh memiliki nama yang sama dalam cakupan (scope) yang sama
2. Hanya boleh terdiri dari karakter tertentu
3. Tidak boleh diawali dengan angka

---

# Mengubah Nilai Antar Tipe Data

JavaScript adalah bahasa yang **dinamis dan fleksibel**, sehingga menyediakan berbagai cara untuk mengonversi tipe data.

Konversi tipe data terbagi menjadi:

* **Konversi Eksplisit**
* **Konversi Implisit**

---

## Konversi Eksplisit

Konversi eksplisit dilakukan secara sadar oleh programmer dengan instruksi yang jelas.

### Number ke String

```javascript
const number = 123;
const boolean = true;

const strNumber = String(number);
const strBoolean = boolean.toString();

console.log(strNumber);   // "123"
console.log(strBoolean);  // "true"
```

---

### String ke Number

```javascript
const strNumber = '123';
const strFloat = '3.14';
const boolean = true;

const numFromString = Number(strNumber);
const floatFromString = Number(strFloat);
const numFromBoolean = Number(boolean);

console.log(numFromString);     // 123
console.log(floatFromString);   // 3.14
console.log(numFromBoolean);    // 1
```

---

### `parseInt()` dan `parseFloat()`

```javascript
const cm = '20cm';
const px = '64px';

const intFromCM = parseInt(cm);
const intFromPX = parseInt(px);

console.log(intFromCM); // 20
console.log(intFromPX); // 64
```

```javascript
const fCm = '20.55cm';
const fPx = '64.23px';

const floatFromCM = parseFloat(fCm);
const floatFromPX = parseFloat(fPx);

console.log(floatFromCM); // 20.55
console.log(floatFromPX); // 64.23
```

---

### Konversi ke Boolean

```javascript
const number = 123;
const string = 'Dicoding';
const empty = null;

const boolFromNumber = Boolean(number);
const boolFromString = Boolean(string);
const boolFromNull = Boolean(empty);

console.log(boolFromNumber); // true
console.log(boolFromString); // true
console.log(boolFromNull);   // false
```

---

### Truthy dan Falsy

* **Truthy** → nilai yang dikonversi menjadi `true`
* **Falsy** → nilai yang dikonversi menjadi `false`

Daftar nilai **falsy** di JavaScript:

* `false`
* `0`
* `-0`
* `0n`
* `''`
* `null`
* `undefined`
* `NaN`

Selain itu? **Truthy semua** 😎

---

## Konversi Implisit

Konversi implisit terjadi ketika JavaScript **otomatis mengubah tipe data** tanpa instruksi eksplisit.

```javascript
const age = 20;
const message = 'Umurku: ' + age;

console.log(message); // Umurku: 20
```

```javascript
const strNumber = '123';
const result = strNumber * 2;

console.log(result); // 246
```

```javascript
const bool = true;
const result = 1 + bool;

console.log(result); // 2
```

---

# Operator

Dalam operasi pemrograman, terdapat dua istilah penting:

* **Operator** → simbol untuk melakukan operasi
* **Operand (operan)** → nilai yang dikenai operasi

---

## Jenis Operator Berdasarkan Jumlah Operan

JavaScript membagi operator menjadi:

* **Unary** → 1 operan
* **Binary** → 2 operan
* **Ternary** → 3 operan

Contoh:

```javascript
let age = 25;

// Unary operator
typeof age;

// Binary operator
5 + 4;
10 / 2;
age = 30;

// Ternary operator
(age < 18) ? 'You are too young!' : 'Welcome onboard!';
```

---

## Macam-Macam Operator di JavaScript

* **Assignment**
  Digunakan untuk memberikan atau mengubah nilai variabel.

* **Arithmetic**
  Digunakan untuk operasi matematika seperti `+`, `-`, `*`, `/`.

* **Comparison**
  Digunakan untuk membandingkan dua nilai dan menghasilkan `true` atau `false`.

* **Logical**
  Digunakan untuk operasi logika antar nilai boolean.

* **String Operator**
  Digunakan untuk menggabungkan string.



## Test Coding
 * TODO: buatlah variabel (konstan) bernama `currency` dan isi dengan nilai "IDR".

 * TODO: buatlah variabel bernama `value` dan isi dengan nilai 10000.

 * TODO: tambahkan nilai di dalam variabel `value` sebesar 5000.

 * TODO: buatlah variabel (konstan) bernama `money`, isi dengan penambahan string dari nilai `currency` + " " + `value`.
