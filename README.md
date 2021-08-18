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
