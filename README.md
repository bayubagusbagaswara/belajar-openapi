# Open API

## Pengenalan OpenAPI

- OpenAPI merupakan standar spesifikasi, tidak tergantung bahasa pemrograman apapun. Digunakan untuk membuat dokumentasi RESTful API
- OpenAPI dibuat agar pengguna RESTful API tidak perlu mengakses kode aplikasi dan membaca dokumen manual (misal dalam bentuk doc, pdf) untuk memahami RESTful API yang dibuat
- OpenAPI bisa menggunakan tool untuk menampilkan secara visual, bahkan untuk membuat kode program client atau server

## Tipe Data

- Dalam data request dan response pasti terdapat detail data
- Misalnya jika terdapat data Product, pasti ada id, name, price, dan lain-lain
- Semua detail data tersebut pasti memiliki tipe data
- OpenAPI memiliki tipe data general yang bisa dimengerti semua bahasa pemrograman

  - integer (int32)
  - integer (int64) alias long
  - number (float)
  - number (double)
  - string
  - string (byte)
  - string (binary)
  - boolean
  - string (date)
  - string (date-time)
  - string (password)

## Document

- Hanya perlu membuat satu file berisi semua data OpenAPI nya
- OpenAPI memiliki struktur yang sudah ditentukan ketika membuat document nya
- Kita bisa menggunakan JSON atau YAML untuk file nya

## Info

- Info merupakan bagian dari informasi metadata tentang API yang kita buat
- Bisa memasukkan author, lisensi, dan lain-lain

## Server

- Sudah pasti terdapat server RESTful API yang akan dibuat
- Kita bsa memberitahu server yang tersedia di OpenAPI
- Misal, terdapat server development, staging, production, dan lain-lain

## External Documentation

- Merupakan bagian dalam OpenAPI jika kita ingin menambahkan link tambahan dalam OpenAPI
- Bisa menuju link documentation lain, atau mungkin link menuju website

## Path

- Merupakan representasi endpoint API di OpenAPI
- Pada Path, kita tidak perlu menuliskan seluruh URL, cukup URL di belakang setelah lokasi server
- Path Operation mengikuti HTTP Method (GET, POST, PUT, DELETE, PATCH)

## Operation

- Setiap Path yang kita buat di OpenAPI, bisa memiliki lebih dari satu Operation
- Hal ini dikarenakan di dalam HTTP satu URL bsia memiliki beberapa HTTP Method
- Misal URL untuk mengambil semua data dan membuat data baru, mungkin url nya sama, yang membedakan adalah HTTP Method nya, GET untuk mengambil data, POST untuk membuat data
- Inti dari API Documentation adalah dokumentasi operation yang terdapat pada RESTful API yang kita buat

## Parameter

- Parameter adalah data yang dikirim tidak melalu Request Body
- Operation bisa memiliki parameter lebih dari satu
- OpenAPI mendukung beberapa jenis parameter, yaitu Query Parameter, Path Variable, Header, dan Cookie
- Kita bisa menambahkan parameter pada Operation, sehingga pengguna bisa tahu bahwa ada parameter yang perlu dikirim ketika memanggil Operation tersebut

## Schema

- Saat kita membuat parameter, kita mungkin ingin memberitahu tentang tipe data untuk parameter tersebut
- Parameter memiliki attribute bernama schema, dimana schema sebenarnya sangat kompleks

### JSON Schema Specification

- Schema menggunakan JSON Schema untuk mendefinisikan struktur datanya
- JSON Schema bisa berisikan tipe data sederhana, seperti number, string, boolean, dan lain-lain. Bahkan tipe data kompleks, seperti Object dan Array

### JSON Schema Validation

- Schema mendukung JSON Schema Validation
- Hal ini membuat kita bisa memberitahu validasi yang diperlukan ketika pengguna membaca OpenAPI kita
- Dengan kita tambahkan Schema Validation, pengguna RESTful API kita bisa tahu validation yang kita buat tanpa harus kita buat dokumentasi secara terpisah

## Request Body

- Dengan ini, kita memberitahu tentang schema request body yang harus dikirim ketika menggunakan RESTful API kita
- Request Body mendukung schema, sehingga kita memberitahu bentuk schema format data, bahkan validasi yang diperlukan

## Object Schema

- Spesifikasi di JSON Schema juga mendukung pembuatan schema berupa objek, yaitu data yang memiliki attribute lebih dari satu

## Array Schema

- Selain tipe data object, Schema juga mendukung tipe data array
- Saat membuat tipe data array, kita juga bisa menentukan tipe data items yang terdapat di array, bisa tipe data sederhana, bisa tipe data kompleks seperti object atau array lagi

## Example

- OpenAPI mendukung example data
- Example data merupakan data contoh yang bisa kita tambahkan baik itu di Parameter, Request Body dan Response Body
