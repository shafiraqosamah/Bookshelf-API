# Bookshelf-API
Terdapat 7 kriteria utama yang harus Anda penuhi dalam membuat proyek Bookshelf API.

Kriteria 1 : Aplikasi menggunakan port 9000
Aplikasi yang Anda buat harus menggunakan port 9000. Jika komputer yang Anda gunakan untuk membuat submission tidak bisa memakai port 9000,  buatlah submission dengan port lain, lalu ketika submission hendak dikirimkan silakan ganti portnya ke 9000.

Kriteria 2 : Aplikasi dijalankan dengan perintah npm run start.
Aplikasi yang Anda buat harus memiliki runner script start. Cara membuatnya, Anda tambahkan properti start ke dalam properti scripts pada package.json.
Pastikan aplikasi tidak dijalankan dengan menggunakan nodemon. Jika Anda ingin menggunakan nodemon dalam proses development, masukkan nodemon kedalam runner script lain.

Kriteria 3 : API dapat menyimpan buku
API yang Anda buat harus dapat menyimpan buku melalui route:
Method : POST
URL : /books
Body Request:

Server harus merespons gagal bila:
Client tidak melampirkan properti name pada request body. Bila hal ini terjadi, maka server akan merespons dengan:
Status Code : 400
Response Body:
Client melampirkan nilai properti readPage yang lebih besar dari nilai properti pageCount. Bila hal ini terjadi, maka server akan merespons dengan:
Status Code : 400
Response Body:
Bila buku berhasil dimasukkan, server harus mengembalikan respons dengan:
Status Code : 201
Response Body:

Kriteria 4 : API dapat menampilkan seluruh buku
API yang Anda buat harus dapat menampilkan seluruh buku yang disimpan melalui route:
Method : GET
URL: /books
Server harus mengembalikan respons dengan:
Status Code : 200
Response Body:
Jika belum terdapat buku yang dimasukkan, server bisa merespons dengan array books kosong.

Kriteria 5 : API dapat menampilkan detail buku
API yang Anda buat harus dapat menampilkan seluruh buku yang disimpan melalui route:
Method : GET
URL: /books/{bookId}
Bila buku dengan id yang dilampirkan oleh client tidak ditemukan, maka server harus mengembalikan respons dengan:
Status Code : 404
Response Body:
Bila buku dengan id yang dilampirkan ditemukan, maka server harus mengembalikan respons dengan:
Status Code : 200
Response Body:

Kriteria 6 : API dapat mengubah data buku
API yang Anda buat harus dapat mengubah data buku berdasarkan id melalui route:
Method : PUT
URL : /books/{bookId}
Body Request:
Server harus merespons gagal bila:
Client tidak melampirkan properti name pada request body. Bila hal ini terjadi, maka server akan merespons dengan:
Status Code : 400
Response Body:
Client melampirkan nilai properti readPage yang lebih besar dari nilai properti pageCount. Bila hal ini terjadi, maka server akan merespons dengan:
Status Code : 400
Response Body:
Id yang dilampirkan oleh client tidak ditemukkan oleh server. Bila hal ini terjadi, maka server akan merespons dengan:
Status Code : 404
Response Body:
Bila buku berhasil diperbarui, server harus mengembalikan respons dengan:
Status Code : 200
Response Body:

Kriteria 7 : API dapat menghapus buku
API yang Anda buat harus dapat menghapus buku berdasarkan id melalui route berikut:
Method : DELETE
URL: /books/{bookId}
Bila id yang dilampirkan tidak dimiliki oleh buku manapun, maka server harus mengembalikan respons berikut:
Status Code : 404
Response Body:
Bila id dimiliki oleh salah satu buku, maka buku tersebut harus dihapus dan server mengembalikan respons berikut:
Status Code : 200
Response Body:

Pengujian
Ketika membangun Bookshelf API, tentu Anda perlu menguji untuk memastikan API berjalan sesuai dengan kriteria yang ada. Kami sudah menyediakan berkas Postman Collection dan Environment yang dapat Anda gunakan untuk pengujian. Silakan unduh berkasnya pada tautan berikut: Postman Bookshelf API Test Collection dan Environment
