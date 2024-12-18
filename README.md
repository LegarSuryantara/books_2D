# books

A new Flutter project.

## Getting Started

Soal 1
 ![screensoot](assets/images/002.JPG)
Soal 2
 ![screensoot](assets/images/001.JPG)
Soal 3
 1. Substring adalah bagian dari string yang diambil dari string yang lebih besar. Dalam banyak bahasa pemrograman, Anda dapat menggunakan fungsi atau metode untuk mengekstrak substring dari string. </br>
 CatchError adalah operator yang digunakan untuk menangani kesalahan (error) yang mungkin terjadi dalam aliran data. Dengan catchError, dapat menangkap kesalahan dan memberikan penanganan alternatif, sehingga program tidak terhenti secara tiba-tiba. </br>
![screensoot](assets/images/003.gif)

Soal 4
1. Langkah 1 dalam kode yang diberikan mendefinisikan tiga fungsi asinkron: returnOneAsync(), returnTwoAsync(), dan returnThreeAsync(), yang masing-masing mengembalikan nilai integer 1, 2, dan 3 setelah menunggu selama 3 detik. Fungsi-fungsi ini menggunakan await Future.delayed(const Duration(seconds: 3)); untuk mensimulasikan operasi yang memerlukan waktu, seperti pengambilan data dari server. </br>
langkah 2 mendefinisikan fungsi asinkron count(), yang bertujuan untuk menjumlahkan hasil dari ketiga fungsi tersebut. Di dalam fungsi ini, variabel total diinisialisasi dengan nilai 0, kemudian diisi dengan hasil dari masing-masing fungsi secara berurutan menggunakan await, sehingga setelah menjalankan ketiga fungsi, total akan berisi nilai 6. Terakhir, fungsi setState() dipanggil untuk memperbarui state dari widget, sehingga hasil penjumlahan yang baru dapat ditampilkan kepada pengguna. </br>
![screensoot](assets/images/004.gif)

Soal 5

1. Langkah ke-2 menggunakan objek Completer untuk mengelola operasi asinkron dan menghasilkan nilai di masa depan. Dalam fungsi getNumber(), Completer<int> diinisialisasi, dan fungsi calculate() dipanggil untuk menjalankan operasi asinkron. Fungsi calculate() menunggu selama 5 detik sebelum menyelesaikan completer dengan nilai 42. Fungsi getNumber() kemudian mengembalikan completer.future, yang merupakan objek Future yang akan berisi nilai 42 setelah proses selesai. Dengan demikian, pola ini memungkinkan pengelolaan hasil dari operasi asinkron tanpa memblokir eksekusi program lainnya. </br>
![screensoot](assets/images/005.gif)

Soal 6

1. Perbedaan antara langkah 2 dan langkah 5-6 terletak pada penanganan kesalahan dan pengelolaan hasil dari operasi asinkron. Pada langkah 2, fungsi calculate() hanya menunggu selama 5 detik sebelum menyelesaikan completer dengan nilai 42, tanpa penanganan kesalahan, sehingga jika terjadi masalah, tidak ada mekanisme untuk menangani situasi tersebut. Sebaliknya, langkah 5-6 menambahkan blok try-catch di dalam calculate(), yang memungkinkan penanganan kesalahan dengan memanggil completer.completeError({}) jika terjadi kesalahan. Selain itu, pemanggilan getNumber() juga dilengkapi dengan penanganan hasil yang berhasil menggunakan then dan penanganan kesalahan dengan catchError. </br>
![screensoot](assets/images/005.gif)

Soal 7

![screensoot](assets/images/007.gif)

Soal 8 

Perbedaan antara kode pada langkah 1 dan langkah 4 terletak pada cara pengelolaan dan penggabungan beberapa Future untuk mendapatkan hasil secara bersamaan. Pada langkah 1, fungsi returnFG() menggunakan objek FutureGroup untuk menambahkan beberapa Future (dari returnOneAsync(), returnTwoAsync(), dan returnThreeAsync()), yang kemudian ditutup dengan futureGroup.close() sebelum hasilnya diproses dalam callback then. Ini membutuhkan lebih banyak langkah dan pengelolaan manual untuk menunggu semua Future. Sebaliknya, langkah 4 menggunakan Future.wait<int>(), yang secara langsung mengeksekusi semua Future dalam daftar secara paralel dan mengembalikan hasilnya dalam bentuk daftar ketika semuanya selesai, sehingga menawarkan cara yang lebih ringkas dan efisien untuk mencapai hasil yang sama tanpa perlu mengelola grup Future secara manual.

Soal 9

![screensoot](assets/images/008.gif)