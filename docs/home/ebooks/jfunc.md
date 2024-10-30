---
title: fjs
---

<script src="https://kit.fontawesome.com/76d9b5d027.js" crossorigin="anonymous"></script>

![fperl-banner](../../assets/fjs-home-banners.gif)
#fjavascript | Functional Programming
### Think functionally

---

Sangat mungkin bahwa sebagian besar pengalaman Anda dalam membangun aplikasi profesional menggunakan bahasa pemrograman berorientasi objek. Anda mungkin pernah mendengar atau membaca tentang pemrograman fungsional di situs lain, blog, forum, dan artikel majalah, tetapi Anda mungkin belum pernah menulis kode fungsional. Jangan khawatir; ini adalah hal yang wajar. Saya juga telah melakukan sebagian besar pengembangan saya di lingkungan berorientasi objek. Menulis kode fungsional tidak sulit, tetapi belajar untuk berpikir secara fungsional dan melepaskan kebiasaan lama adalah tantangan. Tujuan utama bagian 1 dari situs ini adalah untuk meletakkan dasar dan mempersiapkan pikiran Anda untuk menerima teknik fungsional yang dibahas di bagian 2 dan 3.

Bagian 1 membahas apa itu pemrograman fungsional dan pola pikir yang perlu Anda miliki untuk menerimanya; Bagian ini juga memperkenalkan beberapa teknik terpenting yang berdasarkan pada fungsi murni, ketidakberubahan, efek samping, dan transparansi referensial. Ini menjadi tulang punggung semua kode fungsional dan akan membantu Anda bertransisi ke pemrograman fungsional dengan lebih mudah. Selain itu, prinsip-prinsip ini akan menjadi pedoman yang menetapkan dasar untuk banyak keputusan desain yang akan kita buat di bagian-bagian berikutnya.

Bagian 2 memberikan pandangan pertama tentang JavaScript sebagai bahasa fungsional. Karena bahasa ini sangat umum dan mainstream, JavaScript adalah bahasa yang ideal untuk mengajarkan pemrograman fungsional. Jika Anda bukan pengembang JavaScript yang kuat, Bagian ini akan membantu Anda memahami semua yang perlu diketahui untuk memahami JavaScript fungsional, seperti fungsi tingkat tinggi, closure, dan aturan pengaturan variabel.

---

### Becoming functional

Bagian ini mencakup:

- Berpikir dalam istilah fungsional
- Memahami apa dan mengapa pemrograman fungsional
- Memahami prinsip ketidakberubahan dan fungsi murni
- Teknik pemrograman fungsional dan dampaknya terhadap desain secara keseluruhan

---
Jika Anda membaca situs ini, kemungkinan besar Anda adalah pengembang JavaScript dengan pengetahuan yang cukup tentang desain berorientasi objek atau terstruktur, dan Anda penasaran tentang pemrograman fungsional. Mungkin Anda pernah mencoba mempelajarinya sebelumnya tetapi belum dapat menerapkannya dengan sukses di tempat kerja atau pada proyek pribadi Anda. Dalam hal ini, tujuan utama Anda adalah untuk meningkatkan keterampilan pengembangan Anda dan memperbaiki kualitas kode Anda. Situs ini dapat membantu Anda mencapainya.

Kecepatan perkembangan platform web, evolusi browser, dan—yang paling penting—tuntutan dari pengguna akhir semua memiliki pengaruh yang mendalam terhadap cara kita mendesain aplikasi web saat ini. Pengguna menginginkan aplikasi web terasa lebih seperti aplikasi desktop atau aplikasi mobile dengan widget yang kaya dan responsif. Tuntutan ini secara alami memaksa pengembang JavaScript untuk berpikir lebih luas tentang ruang solusi dan mengadopsi paradigma pemrograman serta praktik terbaik yang memberikan solusi terbaik.

Sebagai pengembang, kita cenderung tertarik pada kerangka kerja yang membantu kita menciptakan arsitektur aplikasi yang bersih dan dapat diperluas. Namun, kompleksitas basis kode kita seringkali keluar dari kendali, dan kita ditantang untuk meninjau kembali prinsip desain dasar dari kode kita. Selain itu, web saat ini sangat berbeda dibandingkan dengan beberapa tahun lalu bagi pengembang JavaScript, karena kita dapat melakukan banyak hal sekarang yang sebelumnya tidak mungkin dilakukan secara teknis. Kita bisa memilih untuk menulis aplikasi sisi server yang besar dengan Node.js atau memindahkan sebagian besar logika bisnis ke klien, meninggalkan server yang tipis. Dalam kedua kasus, kita perlu berinteraksi dengan teknologi penyimpanan, menjalankan proses asinkron, menangani peristiwa, dan banyak lagi.

Desain berorientasi objek membantu menyelesaikan sebagian dari masalah ini; tetapi karena JavaScript adalah bahasa yang sangat dinamis dengan banyak keadaan yang dibagikan, tidak butuh waktu lama sebelum kita mengumpulkan cukup kompleksitas yang membuat kode kita sulit diatur dan dipelihara. Desain berorientasi objek memang menggerakkan kita ke arah yang benar, tetapi kita membutuhkan lebih banyak dari itu. Mungkin Anda pernah mendengar istilah pemrograman reaktif dalam beberapa tahun terakhir. Paradigma pemrograman ini memfasilitasi kerja dengan aliran data dan propagasi perubahan. Dalam JavaScript, ini sangat penting ketika berhadapan dengan kode asinkron atau berbasis peristiwa. Secara keseluruhan, apa yang kita butuhkan adalah paradigma pemrograman yang mendorong kita untuk berpikir dengan hati-hati tentang data kita dan fungsi-fungsi yang berinteraksi dengannya. Ketika memikirkan tentang desain aplikasi, tanyakan pada diri sendiri pertanyaan-pertanyaan berikut terkait dengan prinsip desain ini:

- Ekstensibilitas—Apakah saya terus-menerus memperbaiki kode saya untuk mendukung fungsionalitas tambahan?
- Kemudahan modulasi—Jika saya mengubah satu file, apakah file lain terpengaruh?
- Dapat digunakan kembali—Apakah ada banyak duplikasi?
- Dapat diuji—Apakah saya kesulitan untuk melakukan pengujian unit pada fungsi saya?
- Mudah dipahami—Apakah kode saya tidak terstruktur dan sulit diikuti?

Jika kamu menjawab "Ya" atau "Saya tidak tahu" pada salah satu pertanyaan ini, maka kamu telah memilih situs yang tepat sebagai panduan di jalan menuju produktivitas. Pemrograman fungsional (FP) adalah paradigma pemrograman yang kamu butuhkan. Meskipun berdasarkan konsep yang sederhana, FP memerlukan perubahan cara kamu berpikir tentang masalah. FP bukanlah alat baru atau API, melainkan pendekatan berbeda untuk pemecahan masalah yang akan menjadi intuitif setelah kamu memahami prinsip-prinsip dasarnya.

Di Bagian ini, saya mendefinisikan apa itu pemrograman fungsional dan menjelaskan bagaimana dan mengapa pemrograman ini berguna dan penting. Saya memperkenalkan prinsip inti dari ketidakberubahan (immutability) dan fungsi murni (pure functions) serta membahas teknik-teknik FP dan bagaimana teknik-teknik tersebut mempengaruhi pendekatan kamu dalam merancang program. Teknik-teknik ini memungkinkan kamu untuk dengan mudah mengadopsi pemrograman reaktif dan menggunakannya untuk menyelesaikan tugas-tugas JavaScript yang kompleks. Namun sebelum kita membahas semua ini, kamu perlu belajar mengapa berpikir secara fungsional itu penting dan bagaimana hal ini dapat membantumu mengatasi kompleksitas program JavaScript.

#### 1.1 Can functional programming help?

Mempelajari pemrograman fungsional (FP) tidak pernah sepenting sekarang. Komunitas pengembangan dan perusahaan perangkat lunak besar mulai menyadari manfaat menggunakan teknik FP untuk mendukung aplikasi bisnis mereka. Saat ini, sebagian besar bahasa pemrograman utama (Scala, Java 8, F#, Python, JavaScript, dan banyak lagi) menyediakan dukungan fungsional baik secara native maupun berbasis API. Oleh karena itu, keterampilan FP saat ini sangat dibutuhkan dan akan terus dicari di tahun-tahun mendatang.

Dalam konteks JavaScript, pola pikir FP dapat digunakan untuk membentuk sifat ekspresif yang luar biasa dari bahasa ini dan membantumu menulis kode yang bersih, modular, dapat diuji, dan singkat agar kamu dapat lebih produktif dalam bekerja. Selama bertahun-tahun, kita telah mengabaikan fakta bahwa JavaScript dapat ditulis dengan lebih efektif dalam gaya fungsional. Pengabaian ini sebagian disebabkan oleh kesalahpahaman umum tentang bahasa JavaScript, dan juga karena kurangnya konstruk native JavaScript untuk mengelola keadaan dengan baik; ini adalah platform dinamis yang membebankan tanggung jawab pengelolaan keadaan ini pada kita (yang bertanggung jawab memperkenalkan bug ke dalam aplikasi kita). Ini mungkin berjalan dengan baik untuk skrip kecil, tetapi menjadi lebih sulit untuk dikendalikan seiring pertumbuhan basis kode kamu. Dalam hal ini, saya pikir FP melindungimu dari JavaScript itu sendiri. Saya akan membahas ini lebih lanjut di Bagian 2.

Menulis kode JavaScript secara fungsional mengatasi sebagian besar kekhawatiran ini. Dengan menggunakan serangkaian teknik dan praktik terbukti berdasarkan fungsi murni, kamu dapat menulis kode yang mudah dipahami meskipun menghadapi kompleksitas yang semakin meningkat. Menulis JavaScript secara fungsional adalah tawaran dua untuk satu, karena kamu tidak hanya meningkatkan kualitas seluruh aplikasi, tetapi juga memperoleh lebih banyak kemampuan dan pemahaman yang lebih baik tentang bahasa JavaScript.

Karena pemrograman fungsional bukanlah kerangka kerja atau alat, tetapi cara menulis kode, berpikir secara fungsional sangat berbeda dari berpikir dalam istilah berorientasi objek. Tetapi bagaimana cara kamu menjadi fungsional? Bagaimana kamu mulai berpikir secara fungsional? Pemrograman fungsional bersifat intuitif setelah kamu memahami intinya. Mencabut kebiasaan lama adalah bagian tersulit dan bisa menjadi perubahan paradigma yang besar bagi kebanyakan orang yang berasal dari latar belakang berorientasi objek. Sebelum kamu bisa belajar berpikir secara fungsional, pertama-tama kamu harus memahami apa itu FP.

#### 1.2 What is functional programming?

Dalam istilah sederhana, pemrograman fungsional adalah gaya pengembangan perangkat lunak yang sangat menekankan pada penggunaan fungsi. Kamu mungkin berkata, “Ya, saya sudah menggunakan fungsi setiap hari di tempat kerja; apa bedanya?” Seperti yang saya sebutkan sebelumnya, pemrograman fungsional mengharuskan kamu untuk berpikir sedikit berbeda tentang bagaimana cara menghadapi tugas yang kamu hadapi. Ini bukan sekadar menerapkan fungsi untuk mendapatkan hasil; tujuannya adalah untuk mengabstraksi aliran kontrol dan operasi pada data dengan fungsi guna menghindari efek samping dan mengurangi mutasi status dalam aplikasi kamu. Saya tahu ini terdengar rumit, tetapi saya akan menjelaskan masing-masing istilah ini lebih lanjut dan membangunnya sepanjang site ini.

Biasanya, buku tentang pemrograman fungsional dimulai dengan menghitung angka Fibonacci, tetapi saya lebih suka memulai dengan program JavaScript sederhana yang menampilkan teks di halaman HTML. Teks apa yang lebih baik untuk dicetak daripada “Hello World” yang sudah klasik:

```javascript linenums="1"
document.querySelector('#msg').innerHTML = '<h1>Hello World</h1>';
```

Saya telah menyebutkan sebelumnya bahwa karena pemrograman fungsional bukanlah alat spesifik, tetapi cara menulis kode, kamu dapat menerapkannya untuk menulis aplikasi sisi klien (berbasis browser) maupun aplikasi sisi server (Node.js). Membuka browser dan mengetikkan beberapa kode mungkin adalah cara termudah untuk menjalankan JavaScript, dan itu semua yang kamu butuhkan untuk site ini.

**CATATAN**  
Program ini sederhana, tetapi karena semuanya dikodekan secara statis, kamu tidak dapat menggunakannya untuk menampilkan pesan secara dinamis. Katakanlah kamu ingin mengubah format, konten, atau mungkin elemen target; kamu perlu menulis ulang seluruh ekspresi ini. Mungkin kamu memutuskan untuk membungkus kode ini dengan fungsi dan menjadikan titik perubahan sebagai parameter, sehingga kamu dapat menulisnya sekali dan menggunakannya dengan konfigurasi apa pun:

```javascript linenums="1"
function printMessage(elementId, format, message) {
    document.querySelector(`#${elementId}`).innerHTML =
    `<${format}>${message}</${format}>`;
}
printMessage('msg', 'h1','Hello World');
```

Ini adalah peningkatan, memang, tetapi masih bukan potongan kode yang sepenuhnya dapat digunakan kembali. Anggaplah kamu ingin menulis ke file alih-alih halaman HTML. Kamu perlu membawa pemikiran sederhana tentang membuat fungsi parametrik ke tingkat yang berbeda, di mana parameter tidak hanya merupakan nilai skalar tetapi juga dapat berupa fungsi itu sendiri yang memberikan fungsionalitas tambahan. Pemrograman fungsional sedikit seperti menggunakan fungsi dengan kekuatan ekstra, karena tujuan utamamu adalah untuk mengevaluasi dan menggabungkan banyak fungsi dengan lainnya untuk mencapai perilaku yang lebih besar. Saya akan melompat sedikit dan menunjukkan sekilas tentang program yang sama ini dengan pendekatan fungsional.

**Listing 1.1 Functional printMessage**  
```javascript linenums="1"
var printMessage = run(addToDom('msg'), h1, echo);
printMessage('Hello World');
```

Tanpa diragukan lagi, ini terlihat sangat berbeda dari yang asli. Untuk memulai, h1 bukan lagi skalar; itu adalah fungsi seperti addToDom dan echo. Secara visual, rasanya seolah-olah kamu sedang membuat fungsi dari fungsi yang lebih kecil.

Ada alasan untuk kekacauan ini. Listing 1.1 menangkap proses memecah program menjadi potongan-potongan yang lebih kecil yang lebih dapat digunakan kembali, lebih dapat diandalkan, dan lebih mudah dipahami, dan kemudian menggabungkannya untuk membentuk keseluruhan program yang lebih mudah untuk dipahami secara keseluruhan. Setiap program fungsional mengikuti prinsip dasar ini. Untuk saat ini, kamu akan menggunakan fungsi ajaib, run, untuk memanggil serangkaian fungsi secara berurutan, seperti addToDom, h1, dan echo. Saya akan menjelaskan run secara detail nanti. Di balik layar, fungsi ini pada dasarnya menghubungkan setiap fungsi dalam urutan seperti rantai dengan mengirimkan nilai kembali satu sebagai masukan untuk yang berikutnya. Dalam kasus ini, string “Hello World” yang dikembalikan dari echo diteruskan ke h1, dan hasilnya akhirnya diteruskan ke addToDom.

Mengapa solusi fungsional terlihat seperti ini? Saya suka menganggapnya sebagai cara untuk memparameterisasi kode kamu sehingga kamu dapat dengan mudah mengubahnya dengan cara yang tidak mengganggu—seperti menyesuaikan kondisi awal dari suatu algoritma. Dengan fondasi ini, kamu sekarang dapat dengan mudah memperluas printMessage untuk mengulangi pesan dua kali, menggunakan header h2, dan menulis ke konsol alih-alih DOM, semua tanpa harus menulis ulang logika internalnya.

**Listing 1.2 Extending printMessage**  
```javascript linenums="1"
var printMessage = run(console.log, repeat(3), h2, echo);
printMessage('Get Functional');
```

Pendekatan yang secara visual berbeda ini bukan kebetulan. Ketika membandingkan solusi fungsional dengan nonfungsional, kamu mungkin telah memperhatikan bahwa ada perbedaan gaya yang radikal. Keduanya mencetak output yang sama, namun terlihat sangat berbeda. Ini disebabkan oleh mode pengembangan deklaratif yang melekat pada pemrograman fungsional. Untuk sepenuhnya memahami pemrograman fungsional, pertama-tama kamu harus mempelajari konsep-konsep dasar yang menjadi dasarnya:

- Declarative programming
- Pure functions
- Referential transparency
- Immutability

Berikut adalah terjemahan yang sesuai dengan instruksi yang kamu berikan:

---

##### 1.2.1 Functional programming is declarative

Pemrograman fungsional termasuk dalam payung paradigma pemrograman deklaratif: ini adalah paradigma yang mengekspresikan serangkaian operasi tanpa mengungkapkan bagaimana cara implementasinya atau bagaimana aliran data melewatinya. Namun, model yang lebih populer digunakan saat ini adalah imperatif atau prosedural, dan didukung di sebagian besar bahasa terstruktur dan berorientasi objek seperti Java, C#, C++, dan lainnya. Pemrograman imperatif memperlakukan program komputer sebagai sekadar urutan pernyataan dari atas ke bawah yang mengubah status sistem untuk menghitung hasil.

Mari kita lihat contoh imperatif yang sederhana. Misalkan kamu perlu mengkuadratkan semua angka dalam sebuah array. Program imperatif mengikuti langkah-langkah ini:

```javascript linenums="1"
var array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
for(let i = 0; i < array.length; i++) {
    array[i] = Math.pow(array[i], 2);
}
array; //-> [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Pemrograman imperatif memberitahu komputer, secara detail, bagaimana melakukan tugas tertentu (melalui pengulangan dan menerapkan rumus kuadrat ke setiap angka, dalam hal ini). Ini adalah cara paling umum untuk menulis kode ini dan kemungkinan besar akan menjadi pendekatan pertamamu dalam menyelesaikan masalah ini.

Pemrograman deklaratif, di sisi lain, memisahkan deskripsi program dari evaluasi. Ini berfokus pada penggunaan ekspresi untuk menggambarkan apa logika dari sebuah program tanpa harus menentukan aliran kontrol atau perubahan statusnya. Contoh pemrograman deklaratif dapat ditemukan dalam pernyataan SQL. Kuery SQL terdiri dari pernyataan yang menggambarkan seperti apa hasil dari kuery tersebut, mengabstraksi mekanisme internal untuk pengambilan data. Di Bagian 3, saya menunjukkan contoh penggunaan overlay mirip SQL di atas kode fungsional kamu untuk memberikan makna baik pada aplikasi maupun data yang mengalir di dalamnya.

Berpindah ke pendekatan fungsional untuk menyelesaikan tugas yang sama ini, kamu hanya perlu khawatir tentang menerapkan perilaku yang tepat pada setiap elemen dan menyerahkan kontrol pengulangan kepada bagian lain dari sistem. Kamu dapat membiarkan `Array.map()` melakukan sebagian besar pekerjaan berat:

```javascript linenums="1"
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9].map(
    function(num) {
        return Math.pow(num, 2);
    });
```

Map mengambil fungsi yang menghitung kuadrat dari setiap angka.

```javascript linenums="1"
//-> [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Dibandingkan dengan contoh sebelumnya, kamu melihat bahwa kode ini membebaskan kamu dari tanggung jawab untuk mengelola penghitung loop dan akses indeks array dengan benar; sederhana saja, semakin banyak kode yang kamu miliki, semakin banyak tempat bagi bug untuk muncul. Selain itu, loop standar bukanlah artefak yang dapat digunakan kembali kecuali mereka diabstraksi dengan fungsi. Dan itulah yang akan kita lakukan. Di Bagian 3, saya akan menunjukkan cara menghapus loop manual sepenuhnya dari kode kamu demi fungsi tingkat satu dan fungsi urutan tinggi seperti map, reduce, dan filter, yang menerima fungsi sebagai parameter sehingga kode kamu lebih dapat digunakan kembali, dapat diperluas, dan deklaratif.

Inilah yang saya lakukan dengan fungsi ajaib `run` di listing 1.1 dan 1.2. Mengabstraksi loop dengan fungsi memungkinkan kamu memanfaatkan ekspresi lambda atau fungsi panah, yang diperkenalkan dalam JavaScript ES6. Ekspresi lambda memberikan alternatif singkat untuk fungsi anonim yang dapat diteruskan sebagai argumen fungsi, dalam semangat menulis lebih sedikit:

```javascript linenums="1"
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9].map(num => Math.pow(num, 2));
//-> [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

**Menerjemahkan notasi lambda ke notasi fungsi biasa**

Ekspresi lambda memberikan keuntungan sintaksis yang besar dibandingkan dengan notasi fungsi biasa karena mereka mengurangi struktur pemanggilan fungsi menjadi bagian-bagian yang paling penting. Ekspresi lambda ES6 ini:

```javascript linenums="1"
num => Math.pow(num, 2)
```

setara dengan fungsi berikut:

```javascript linenums="1"
function(num) {
    return Math.pow(num, 2);
}
```

Mengapa menghapus loop dari kode kamu? Loop adalah struktur kontrol imperatif yang sulit untuk digunakan kembali dan sulit untuk dipasangkan dengan operasi lain. Selain itu, ini menyiratkan kode yang terus-menerus berubah atau bermutasi sebagai respons terhadap iterasi baru. Kamu akan belajar bahwa program fungsional bertujuan untuk tidak memiliki status dan ketidakberubahan sebanyak mungkin. Kode tanpa status memiliki peluang nol untuk berubah atau merusak status global. Untuk mencapai ini, kamu akan menggunakan fungsi yang menghindari efek samping dan perubahan status, yang dikenal sebagai fungsi murni.

##### 1.2.2 Pure functions and the problem with side effects

Pemrograman fungsional didasarkan pada premis bahwa kamu membangun program yang tidak dapat diubah berdasarkan blok bangunan fungsi murni. Fungsi murni memiliki kualitas-kualitas berikut:

- **Bergantung Hanya pada Input yang Diberikan:** Fungsi murni hanya bergantung pada input yang diberikan dan tidak pada status tersembunyi atau eksternal yang mungkin berubah selama evaluasinya atau di antara pemanggilan.
- **Tidak Mengubah Hal di Luar Ruang Lingkupnya:** Fungsi murni tidak melakukan perubahan di luar ruang lingkupnya, seperti memodifikasi objek global atau parameter yang diteruskan dengan referensi.

Secara intuitif, setiap fungsi yang tidak memenuhi persyaratan ini dianggap "tidak murni." Pemrograman dengan ketidakberubahan bisa terasa aneh pada awalnya. Lagipula, seluruh tujuan desain imperatif, yang biasa kita lakukan, adalah untuk menyatakan bahwa variabel akan bermutasi dari satu pernyataan ke pernyataan berikutnya (mereka “variabel,” setelah semua). Ini adalah hal yang alami bagi kita untuk lakukan. Pertimbangkan fungsi berikut:

```javascript linenums="1"
var counter = 0;
function increment() {
    return ++counter;
}
```

Fungsi ini tidak murni karena ia membaca/memodifikasi variabel eksternal, `counter`, yang tidak bersifat lokal dalam ruang lingkup fungsi. Secara umum, fungsi memiliki efek samping ketika membaca dari atau menulis ke sumber daya eksternal, seperti yang ditunjukkan pada Contoh 1.1. Contoh lainnya adalah fungsi populer `Date.now();` hasilnya tentu tidak dapat diprediksi dan konsisten, karena selalu bergantung pada faktor yang terus-menerus berubah: waktu.

**Variabel Global**  
```javascript linenums="1"
var counter = 0;
```

**Batasan Fungsi**  
```javascript linenums="1"
function increment() {
    return ++counter;
}
```

**Efek Samping:**  
Referensi global telah diubah

*Contoh 1.1* Fungsi `increment()` menyebabkan efek samping dengan membaca/memodifikasi variabel eksternal, `counter`. Hasilnya tidak dapat diprediksi karena `counter` dapat berubah kapan saja di antara pemanggilan.

Dalam hal ini, `counter` diakses melalui variabel global implisit (di JavaScript berbasis browser, itu adalah objek `window`). Efek samping umum lainnya terjadi ketika mengakses data instance melalui kata kunci `this`. Perilaku `this` di JavaScript berbeda dari bahasa pemrograman lainnya karena menentukan konteks runtime dari sebuah fungsi. Ini sering kali menyebabkan kode yang sulit dipahami, itulah sebabnya saya menghindarinya jika memungkinkan. Saya akan membahas topik ini lagi di bab berikutnya. Efek samping dapat terjadi dalam banyak situasi, termasuk yang berikut ini:

- Changing a variable, property, or data structure globally
- Changing the original value of a function’s argument
- Processing user input
- Throwing an exception, unless it’s caught within the same function
- Printing to the screen or logging
- Querying the HTML documents, browser cookies, or databases

Jika kamu tidak dapat membuat dan memodifikasi objek atau mencetak ke konsol, apa nilai praktis yang bisa kamu dapatkan dari program seperti ini? Memang, fungsi murni bisa sulit digunakan dalam dunia yang penuh dengan perilaku dinamis dan mutasi. Namun, pemrograman fungsional praktis tidak membatasi semua perubahan status; ia hanya menyediakan kerangka kerja untuk membantumu mengelola dan menguranginya, sambil memungkinkan kamu memisahkan yang murni dari yang tidak murni. Kode yang tidak murni menghasilkan efek samping yang terlihat secara eksternal seperti yang disebutkan sebelumnya, dan dalam site ini saya akan membahas cara-cara untuk menghadapinya.

Untuk membicarakan masalah ini secara lebih konkret, anggaplah kamu adalah seorang pengembang dalam sebuah tim yang mengimplementasikan aplikasi untuk mengelola data siswa di sebuah sekolah. Daftar 1.3 menunjukkan program imperatif kecil yang menemukan catatan siswa berdasarkan nomor Jaminan Sosial dan menampilkannya di browser (sekali lagi, penggunaan browser tidak penting; kamu bisa dengan mudah menulis ke konsol, basis data, atau file). Saya merujuk dan mengembangkan program ini sepanjang site sebagai skenario dunia nyata yang tipikal yang melibatkan efek samping dengan berinteraksi dengan penyimpanan objek lokal eksternal (seperti array objek) dan melakukan beberapa level IO.

**Listing 1.3 Fungsi showStudent Imperatif dengan efek samping**  
Mengakses penyimpanan objek untuk mencari siswa berdasarkan SSN. Anggaplah ini adalah operasi sinkron untuk saat ini; saya akan membahas kode asinkron di kemudian hari dalam site ini.

```javascript linenums="1"
function showStudent(ssn) {
    var student = db.get(ssn);
    if (student !== null) {
        document.querySelector(`#${elementId}`).innerHTML =
            `${student.ssn},
            ${student.firstname},
            ${student.lastname}`;
    } else {
        throw new Error('Siswa tidak ditemukan!');
    }
}

showStudent('444-44-4444');
// Menjalankan program ini dengan
// SSN 444-44-4444 dan
// menambahkan detail siswa ke halaman
```

Mari kita analisis kode ini lebih lanjut. Fungsi ini jelas mengekspos beberapa efek samping yang merembet di luar ruang lingkupnya:

- Ini berinteraksi dengan variabel eksternal (db) untuk akses data karena tanda tangan fungsi tidak menyatakan parameter ini. Pada titik mana pun, referensi ini bisa menjadi null atau berubah dari satu panggilan ke panggilan berikutnya, menghasilkan hasil yang sama sekali berbeda dan mengompromikan integritas program.
- Variabel global elementId dapat berubah kapan saja, di luar kendali kamu.
- Elemen HTML dimodifikasi secara langsung. Dokumen HTML (DOM) itu sendiri adalah sumber daya global yang dapat diubah dan dibagikan.
- Ini bisa berpotensi melemparkan pengecualian jika siswa tidak ditemukan, yang menyebabkan seluruh tumpukan program terurai dan berakhir secara mendadak.

Fungsi dalam listing 1.3 bergantung pada sumber daya eksternal, yang membuat kode menjadi kaku, sulit untuk dikerjakan, dan sulit untuk diuji. Di sisi lain, fungsi murni memiliki kontrak yang jelas sebagai bagian dari tanda tangannya yang menggambarkan semua parameter formal fungsi (set input), membuatnya lebih sederhana untuk dipahami dan digunakan. 

Mari kita kenakan "topi fungsional" kita dan gunakan apa yang kamu pelajari dari program printMessage sederhana dalam skenario kehidupan nyata ini. Saat kamu semakin nyaman dengan pemrograman fungsional di situs ini, kamu akan terus memperbaiki implementasi ini dengan teknik-teknik baru. Saat ini, kamu dapat melakukan dua peningkatan sederhana:

- Pisahkan fungsi panjang ini menjadi fungsi-fungsi yang lebih pendek, masing-masing dengan satu tujuan.
- Kurangi jumlah efek samping dengan secara eksplisit mendefinisikan semua argumen yang dibutuhkan agar fungsi dapat menjalankan tugasnya.

Mari kita mulai dengan memisahkan aktivitas pengambilan catatan siswa dari menampilkannya di layar. Tentu saja, efek samping dari interaksi dengan penyimpanan eksternal.

Berikut adalah terjemahan sesuai instruksi yang kamu berikan:

---

dan DOM tidak dapat dihindari, tetapi setidaknya kamu bisa membuatnya lebih mudah dikelola dan memisahkannya dari logika utama. Untuk melakukan ini, saya akan memperkenalkan teknik FP populer yang disebut currying. Dengan currying, kamu dapat sebagian mengatur beberapa argumen dari sebuah fungsi untuk menguranginya menjadi satu. Seperti yang ditunjukkan dalam daftar berikut, kamu dapat menerapkan curry untuk mengurangi fungsi find dan append menjadi fungsi unary yang dapat dengan mudah digabungkan melalui run.

**Listing 1.4 Decomposing the showStudent program**

```javascript
var find = curry(function (db, id) {
    var obj = db.get(id);
    if (obj === null) {
        throw new Error('Object not found!');
    }
    return obj;
});
```
Fungsi find membutuhkan referensi ke penyimpanan objek dan ID siswa yang dicari.

```javascript
var csv = function (student) {
    return `${student.ssn}, ${student.firstname}, ${student.lastname}`;
};
```
Mengonversi objek siswa menjadi nilai yang dipisahkan koma.

```javascript
var append = curry(function (elementId, info) {
    document.querySelector(elementId).innerHTML = info;
});
```
Untuk menampilkan detail siswa di halaman, kamu membutuhkan ID elemen dan data siswa.

Kamu tidak perlu memahami currying sekarang, tetapi penting untuk melihat bahwa kemampuan untuk mengurangi panjang fungsi-fungsi ini memungkinkan kamu menulis showStudent sebagai kombinasi dari bagian-bagian yang lebih kecil:

```javascript
var showStudent = run(
    append('#student-info'),
    csv,
    find(db)
);
```
**Menetapkan sebagian ID elemen HTML untuk digunakan dalam fungsi.**
**Menetapkan sebagian objek akses data untuk menunjuk ke tabel siswa.**

Meskipun program ini hanya sedikit ditingkatkan, ini mulai menunjukkan banyak manfaat:

- Ini jauh lebih fleksibel, karena sekarang memiliki tiga komponen yang dapat digunakan kembali.
- Penggunaan kembali fungsi yang terperinci ini adalah strategi untuk meningkatkan produktivitas kamu, karena kamu dapat secara dramatis mengurangi jejak kode yang harus dikelola secara aktif.
- Kamu meningkatkan keterbacaan kode dengan mengikuti gaya deklaratif yang memberikan pandangan jelas tentang langkah-langkah tingkat tinggi yang dilakukan oleh program ini.
- Yang lebih penting, interaksi dengan objek HTML dipindahkan ke fungsi terpisah, memisahkan perilaku murni dari yang tidak murni (impur). Saya menjelaskan currying dan pengelolaan bagian murni dan tidak murni secara mendalam di Bagian 4.

Program ini masih memiliki beberapa bagian yang perlu diperbaiki, tetapi mengurangi efek samping akan membuatnya kurang rapuh terhadap perubahan kondisi eksternal. Jika kamu melihat lebih dekat pada fungsi `find`, kamu akan menyadari bahwa ia memiliki pernyataan cabang pemeriksaan null yang dapat menghasilkan pengecualian. Untuk banyak alasan, yang akan kita pelajari nanti, sangat bermanfaat untuk menjamin nilai kembalian yang konsisten dari sebuah fungsi, sehingga hasilnya menjadi konsisten dan dapat diprediksi. Ini adalah kualitas dari fungsi murni yang disebut transparansi referensial.


next - 1.2.3
