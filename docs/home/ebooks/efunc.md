---
title: fEx
---

<script src="https://kit.fontawesome.com/76d9b5d027.js" crossorigin="anonymous"></script>

![fperl-banner](../../assets/fex-home-banners.gif)
#λex-ebook | Programming Entrance
###### Author: [Yatsugi Saiba](../../about/me.md)
---

## Part One: Introductions
### I. Untuk siapa materi ini?

Di halaman pembuka ini Anda mungkin pernah melihat ini:

Joy of Elixir adalah pengantar yang lembut untuk pemrograman, ditujukan bagi orang-orang yang sudah tahu beberapa hal tentang komputer, tetapi memiliki sedikit hingga tidak ada pengalaman pemrograman. Jika Anda merasa tidak tahu cukup banyak tentang komputer, yah, Anda sudah sampai di sini dan itu sudah cukup!

Atau mungkin Anda langsung menuju tautan "baca online" dan melewatkan itu. Bagaimanapun, sekarang setelah saya mendapatkan perhatian Anda dan Anda telah membaca paragraf kecil itu, Anda mungkin berpikir: tetapi untuk siapa site ini, sebenarnya? Baiklah, biarkan saya menjelaskannya dengan jelas dan sederhana:

Site ini adalah untuk Anda.

Site ini adalah untuk siapa saja yang pernah ingin belajar pemrograman. Anda mungkin pernah mencoba sebelumnya. Anda mungkin belum pernah. Anda mungkin telah membaca beberapa site pemrograman yang sangat kaku dan menjadi tidak tertarik dengan pemrograman sama sekali, tetapi sekarang Anda kembali di sini. Saya senang Anda masih bersama kami. Terima kasih telah memberi kami kesempatan lain.

Jika sejauh mana pengalaman pemrograman Anda adalah menggunakan fungsi seperti SUM(A1:A23) di Microsoft Excel untuk menjumlahkan semua angka dalam beberapa baris, maka itu baik-baik saja. Jika Anda tidak tahu apa yang saya bicarakan, itu juga tidak masalah.

Sejauh mana pengetahuan pemrograman Anda mungkin hanya memberi tahu komputer untuk selalu menempatkan tanda tangan di akhir email Anda. Sesuatu yang terlihat resmi dengan nama Anda, jabatan, dan nomor telepon. Mungkin juga ada kutipan yang menarik di akhir. Ya, bahkan itu adalah pemrograman. Anda telah memberikan instruksi kepada komputer dan ia dengan setia melaksanakannya sampai diberi tahu sebaliknya.

Anda membaca site ini di perangkat komputer dengan beberapa deskripsi dan itu adalah awal yang sempurna. Anda mungkin tahu apa itu browser web. Anda memiliki beberapa ide bahwa pemrograman memungkinkan Anda mengatur komputer dan mengurangi repetisi beberapa tugas berbasis komputer. Itu luar biasa. Anda akan melakukan dengan baik di sini.

Sekarang setelah itu teratasi, mari kita lihat apa itu Elixir.

--- 

### II. Elixir? Bukankah itu sejenis minuman?

Elixir, bahasa pemrograman, sangat berbeda dari elixir yang didefinisikan Wikipedia sebagai:

cairan jernih berasa manis yang digunakan untuk tujuan medis.

Dan untuk varian bahasa pemrograman, ia mengatakan:

Elixir adalah bahasa pemrograman fungsional, bersamaan, dan umum yang berjalan di mesin virtual Erlang (BEAM).

Penjelasan pertama tampaknya ditulis dalam bahasa Inggris yang mudah dipahami dan jelas. Anda membaca setiap kata dan memahaminya sama seperti kata lainnya. Penjelasan kedua adalah deretan kata yang akan diungkapkan oleh teman nerdy Anda tepat setelah mendorong kacamata mereka dan mungkin mereka akan memulai kalimat dengan "Yah, sebenarnya [tunggu efek dramatis]".

Tentu, beberapa kata mungkin Anda pahami, tetapi sisanya adalah omong kosong nerdy.

Apa sebenarnya arti "fungsional"? Apakah itu berarti bahwa itu bekerja? Yah, saya berharap itu bekerja! Jika tidak, apa gunanya site ini? Lebih baik tutup sekarang. Tidak ada gunanya menggunakan bahasa pemrograman yang tidak fungsional!

Bersamaan? Apa? Hal-hal terjadi pada saat yang sama? Mengapa itu penting?

Apa itu Erlang? Apakah itu seperti Klingon?

Selain itu, apa itu mesin virtual dan apa yang membedakannya dari mesin biasa? Apakah itu ada hubungannya dengan realitas virtual?

Apa itu BEAM? Saya telah melihat Olimpiade, apakah itu seperti balance beam? Atau apakah itu seperti sinar cahaya? Atau apakah itu membantu dalam arsitektur bangunan? Anda akan menemukan nanti apa artinya, tetapi saat ini tidak sepenting deskripsi yang terlihat.

Ini adalah kalimat yang sangat jelas ditulis oleh salah satu rekan nerdy Anda untuk semua orang nerdy lainnya agar dapat dipahami. Mereka semua akan membaca kalimat itu dan mengangguk bijak serta mengatakan hal-hal seperti "ahhh ya, itu benar dan singkat dan mudah dipahami". Itu karena mereka adalah nerd dan mereka menjalani hal ini. Anda adalah orang baru dan kita setidaknya harus berusaha agar tidak menakut-nakuti Anda dengan pembicaraan semacam itu!

Penjelasan yang ramah bagi manusia diperlukan
Tidak perlu mempedulikan penjelasan yang kompatibel dengan nerd tentang apa itu Elixir-bahasa-pemrograman. Itu ditulis untuk para nerd. Mari kita coba yang ini:

Elixir adalah bahasa pemrograman yang digunakan manusia untuk meminta komputer melakukan tindakan tertentu.
Itu adalah penjelasan yang cukup baik. Saya bisa mengatakan itu karena saya yang menulis site ini. Saya bisa menulis apa pun yang saya mau: begitulah cara ini bekerja. Saya menulis, Anda membaca.

Penjelasan baru ini menggunakan kata-kata bahasa Inggris yang sederhana untuk menjelaskan apa yang Anda gunakan Elixir untuk lakukan. Ini tidak menjelaskan fitur-fitur canggihnya dengan menggunakan kata-kata seperti "fungsional" dan "bersamaan", dan tentu saja tidak menyebutkan apa pun tentang BEAM atau mesin, virtual atau tidak.

Penjelasannya sangat bagus sehingga bisa digunakan untuk menjelaskan bahasa pemrograman mana pun yang ada. Jadi, mungkin terlalu umum. Ini seperti makanan yang diberi label hitam-putih yang Anda temukan di rak bawah di supermarket seharga satu dolar. Itu menjalankan tugasnya, tetapi tidak terasa enak di perut Anda setelah itu.

Oke, jadi mari kita perbarui! Penjelasan Sederhana Tentang Elixir Bahasa Pemrograman, Versi Dua, mari kita mulai:

Elixir adalah bahasa pemrograman yang sangat menyenangkan dan mudah digunakan yang manusia gunakan untuk meminta komputer melakukan sesuatu. Anda dapat menulis program yang mudah dipahami oleh manusia dan komputer. Menulis Elixir adalah suatu kebahagiaan.
Oh ya! Itu jauh lebih baik. Ini membuat orang-orang bersemangat. Ngomong-ngomong, sekelompok kecil beberapa ratus orang telah berkumpul di sekitar. "Kebahagiaan? Saya suka kebahagiaan!", teriak mereka. Lalu mereka berkata: "Kami ingin melihat beberapa kode Elixir! Cukup bicara!". Uh oh, kerumunan mulai gaduh. Saya harus memberikan apa yang mereka mau.

--- 

## Part Two: And away we go
#### 1. Appeasing the masses with code

Masyarakat telah menyimak bagian terbaik dari sebuah bab (setidaknya) menyerap semua yang telah kita bicarakan. Namun, mereka sedikit gelisah karena kita telah membahas bahasa pemrograman tanpa benar-benar melakukan pemrograman. Yah, itu sepenuhnya dapat dimengerti! Saya juga akan merasa terganggu jika saya bukan orang yang menulis site ini. Saya tahu apa yang akan datang, tetapi mereka tidak.

Oke, mari kita coba menenangkan masyarakat. Berikut adalah beberapa kode:

```elixir linenums="1"
"Hello, World!"
```

Masyarakat menjadi diam. Tatapan mereka mengeras. Juru bicara mereka — yang telah mereka tunjuk saat saya memikirkan cuplikan ini — berkata (sambil merobohkan dinding keempat secara sistematis): "Itu hanya sekumpulan kata yang dikutip! Sama seperti ini yang saya ucapkan."

Kerumunan setuju.

Oke, Anda benar. Itu adalah beberapa kata yang dikutip, tetapi itu adalah kata-kata yang bisa dipahami oleh manusia dan komputer. Itu cukup keren. Yah, saya menganggapnya demikian, setidaknya.

Kerumunan manusia di depan kita tahu kata-kata tersebut dan bahwa kata-kata itu memiliki makna di baliknya dan membentuk kalimat yang dapat dipahami. Komputer hanya tahu huruf atau simbol individual dalam kata-kata tersebut, dan tidak peduli bahwa kata-kata itu memiliki makna atau bahwa kata-kata itu membentuk kalimat yang dapat dipahami. "Hal-hal itu hanya penting bagi manusia," pikirnya, tanpa mengakui zeitgeist Machine Learning yang telah muncul baru-baru ini.

Ketika kita mengucapkan kalimat itu kepada masyarakat, mereka dapat dengan mudah mengulangnya kembali kepada kita. Untuk berbicara dengan komputer, kita perlu membuka prompt untuk bahasa tertentu yang ingin kita gunakan untuk berkomunikasi. Berbagai bahasa memiliki prompt yang berbeda. Kita tidak bisa hanya berbicara dengan komputer untuk memprogramnya. Belum saatnya, setidaknya.

##### Menginstal Elixir
Anda mungkin belum menginstal Elixir dan kita hampir membutuhkannya untuk diinstal. Jika Anda tidak menginstalnya, hampir semua yang terjadi setelah titik ini tidak akan berfungsi.

Salah satu cara baik untuk memeriksa apakah Elixir telah diinstal adalah dengan menjalankan perintah ini di terminal Anda:

```bash
elixir -v
```

Jika perintah ini mengatakan sesuatu seperti ini:

```bash
Erlang/OTP 23 [erts-11.1.1] [source] [64-bit] [smp:16:16] [ds:16:16:10] [async-threads:1] [hipe] [dtrace]

Elixir v1.10.4
```

Maka itu berarti Elixir telah diinstal dan Anda dapat melanjutkan. Jika mengatakan sesuatu seperti "perintah tidak ditemukan", maka pergilah ke Lampiran A: Pengaturan dan Instal dan ikuti langkah-langkah di sana terlebih dahulu.

Dalam hal ini, kita ingin berbicara Elixir, jadi kita bisa membuka prompt dengan perintah `iex`. `iex` adalah singkatan dari "Interactive EliXir". Untuk membuka prompt, kita perlu terlebih dahulu membuka aplikasi terminal atau command prompt kita. Setelah itu terbuka, kita bisa mengetik `iex` ke jendela itu dan tekan Enter untuk memulai prompt `iex` kita.

Ketika dimulai, prompt akan mengatakan:

```bash
Erlang/OTP 23 [erts-11.1.1] [source] ...

Interactive Elixir (v1.10.4) - ⏎
  tekan Ctrl+C untuk keluar (ketik h() ENTER untuk bantuan)
```

##### Karakter kecil ⏎
Anda tidak akan melihat ⏎ di prompt `iex` Anda, tetapi Anda melihatnya di sini. Jadi, apa yang terjadi?

Saya meletakkannya di sana untuk menunjukkan bahwa baris tersebut terpisah menjadi dua baris di site ini. Ini dilakukan agar seluruh baris muat di dalam site. Jika saya tidak melakukan ini, bagian akhir output akan tersembunyi oleh margin halaman. Itu tidak menyenangkan bagi siapa pun! Anda seharusnya melihatnya sebagai satu baris yang terus menerus di prompt `iex` Anda.

Jadi ketika Anda melihat ⏎, anggaplah itu sebagai "ini semua satu baris dalam kehidupan nyata, tetapi tersebar di dua baris di site."

Kita dapat dengan aman mengabaikan output dari prompt sejauh ini. Ini hanya memberikan kita beberapa informasi nerdy. Baris terakhir yang ditunjukkan di sini memberi tahu kita bahwa kita menjalankan Interactive Elixir "v1.10.4". Ini memberi tahu kita bahwa kita dapat menekan Ctrl+C untuk keluar -- ini akan menghentikan prompt `iex` dan mengembalikan kita ke prompt terminal kita.

Hal berikutnya yang dikatakan komputer adalah:

```
iex(1)>
```

Ini memberi tahu kita bahwa komputer sekarang mendengarkan instruksi kita, dengan penuh semangat menunggu mereka. Ini meminta kita untuk memberikan input. Mari kita berikan kalimat kita lagi kepada komputer, dengan menekan enter di akhir baris:

```elixir linenums="1"
iex(1)> "Hello, World!"
"Hello, World!"
```

Di baris pertama di sini, kita memberikan instruksi kepada komputer yang terlihat seperti kalimat biasa. Ini karena ini adalah kalimat biasa. Dalam terminologi nerd komputer, kita merujuk pada kumpulan simbol yang diberi tanda kutip ganda ini sebagai string. Lebih mudah untuk memikirkannya seperti string jika Anda memikirkan semua bagian kalimat yang terhubung oleh string nyata:

String terhubung dengan string
Contoh bagian 1.1: String, terhubung dengan string!
Komputer kemudian menerima string ini, menginterpretasikannya dan memberi tahu kita bagaimana ia menginterpretasikan string tersebut. Dalam hal ini, komputer hanya mengulang kembali kalimat/string kita. Komputer dapat melakukan jauh lebih banyak daripada ini, percayalah. Komputer tidak akan sangat baik jika semua yang dilakukannya hanya mengulang kembali kepada kita.

Masyarakat kini mulai gelisah. Sejauh ini kita hanya menunjukkan satu baris kode. Dua kali, ya, tetapi tetap saja hanya satu baris kode. Dan komputer terus meminta kita dengan baris ini.

```bash
iex(2)>
```

Komputer mendambakan lebih banyak input. Masyarakat juga mendambakan itu. Untungnya bagi saya (dan Anda), Elixir dapat melakukan jauh lebih banyak daripada hanya mengulang.

##### "Kita baru saja melihat REPL!" "Apa itu sekarang?"

Tipe nerd yang lebih nerdy akan menyebut "prompt" kita ini sebagai REPL. Jika tipe nerd yang lebih nerdy telah menggunakan kata "REPL" untuk menggambarkan prompt seperti `iex`, Anda sekarang tahu apa artinya: REPL = prompt. Anda tahu bahwa ini tidak ada hubungannya dengan turun dari ketinggian yang tergantung dengan tali yang digulung ganda (rappel).

"Tapi hei, REPL terlihat seperti akronim!" Saya mendengar Anda berkata. Bintang emas untuk Anda. Ini adalah akronim dan singkatan dari Read, Evaluate, Print, dan Loop.

Prompt `iex` meminta kita untuk memberikan input. Ini adalah langkah "read". Ini akan membaca input kita. Setelah kita memberikannya input, ia kemudian mengevaluasi apa yang telah kita berikan untuk menentukan apakah komputer dapat menjalankan program kita. Jika iya, maka komputer menjalankan program kita dan "mencetak" output dari program kita kembali ke prompt untuk menunjukkan kepada kita apa yang telah dilakukan komputer. Dan kemudian ia meminta kita lagi karena ia sedang looping. Jadi: baca, evaluasi, cetak, loop: REPL. Dan sekarang Anda tahu!

##### Tidak ada lagi angka di prompt `iex`
Hai, ini saya lagi. Pasti Anda tidak berharap mendengar dari saya lagi begitu cepat. Nah, di sinilah kita lagi. Ini hanya akan memakan waktu sesaat. Kemudian kita bisa kembali belajar tentang Elixir. Janji.

Sekadar catatan: contoh yang menggunakan `iex` mulai dari sini tidak akan memiliki angka di prompt. Alih-alih menunjukkan `iex(3)>` untuk prompt berikutnya, Anda hanya akan melihat `iex>`. Ini memudahkan penulis ini untuk memindahkan contoh kode di site tanpa harus memberi nomor ulang pada baris `iex(3)`. Saya harap Anda tidak keberatan.

##### Matematis!
Oke, jadi komputer bisa mengulang hal-hal. Tapi apa lagi yang bisa dilakukannya? Bagaimana jika kita meminta komputer untuk melakukan beberapa perhitungan sederhana?

```elixir linenums="1"
iex> 2 + 4
6
iex> 3 - 6
-3
iex> 4 * 12345
49380
iex> 1234 / 4 + 2 - 12 * 3
274.5
```

Ini sedikit menenangkan masyarakat. Mereka adalah sekelompok yang tidak stabil. Komputer sekarang tidak lagi mengulang hal-hal kepada kita. Sebaliknya, ia menghitung persamaan matematika yang tidak terlalu rumit yang kita berikan, dan kemudian memberikan kita angka yang benar. Jika Anda tidak yakin angka-angka ini benar, saya mendorong Anda untuk mengambil pena dan kertas dan memecahkannya sendiri. Anda akan menemukan bahwa komputer benar. Komputer yang baik!

Masyarakat menyadari bahwa Elixir sekarang dibangun untuk lebih dari sekadar pengulangan sederhana. Elixir juga dapat melakukan perhitungan! Kita telah menggunakan simbol +, -, *, dan / di sini, meminta komputer untuk menjumlahkan, mengurangi, mengalikan, dan membagi, dalam urutan itu. Anda

 mungkin berpikir untuk menggunakan x untuk mengalikan, tetapi itu memiliki arti yang berbeda seperti yang akan kita lihat nanti. Anda harus menggunakan * ketika Anda ingin mengalikan sesuatu, karena itulah yang diharapkan Elixir dari Anda.

##### Mengapa angka berwarna merah, tetapi string berwarna hijau?
Anda mungkin telah memperhatikan bahwa string muncul dalam warna hijau di prompt `iex`:

```elixir linenums="1"
iex> "Hello World!"
"Hello World"
```

Tetapi angka muncul dalam warna merah:

```elixir linenums="1"
iex> 2 + 4
6
```

Dan Anda mungkin bertanya-tanya mengapa.

Nah, tidak ada alasan khusus untuk string berwarna hijau dan angka berwarna kuning; warna-warna tersebut tidak memiliki makna lain selain untuk menjadi indikator berguna dari berbagai jenis data. String adalah satu jenis data, dan angka adalah jenis yang berbeda. Kita akan melihat lebih banyak jenis saat kita melanjutkan perjalanan kita. Warna yang berbeda ini hanya membantu membedakan tipe nilai yang kita lihat di prompt.

##### Apa yang ingin kita capai di site ini
Oke, sekarang setelah masyarakat puas, mari kita luangkan waktu sejenak untuk membahas apa yang akan dibahas di site ini dan apa yang akan Anda dapatkan darinya.

12 bab pertama akan membahas beberapa dasar-dasar Elixir. Ya, itu terlihat seperti banyak bab tetapi sebagian besar dari bab-bab ini cukup pendek; hanya beberapa halaman. Ini sekitar 50 halaman secara total. Bab-bab ini akan mencakup hal-hal yang perlu Anda ketahui sebelum Anda dapat menulis program Elixir yang layak, dan memberi Anda tur yang baik tentang bahasa ini. Bab-bab ini penting karena akan membangun dasar yang kokoh untuk pengalaman Elixir Anda.

Bab 13 dan seterusnya akan fokus pada membangun program yang lebih besar menggunakan teknik yang telah kita pelajari di 12 bab pertama. Kita akan menggabungkan hal-hal dari bab-bab sebelumnya dan menggunakannya semua bersama-sama dan kita bahkan akan diperkenalkan pada lebih banyak hal yang dilakukan bahasa Elixir.

Di akhir setiap bab, akan ada serangkaian latihan (opsional) yang bisa Anda lakukan, menggunakan hal-hal yang telah Anda pelajari di bab tersebut. Saya sangat mendorong Anda untuk mencobanya setidaknya. Jika Anda tidak dapat melakukannya, jangan khawatir. Coba lagi nanti.

Dengan semua itu dikatakan, mari kita terus melihat apa yang bisa dilakukan Elixir untuk kita, dimulai dengan membuat Elixir mengingatkan kita tentang hal-hal.

##### Latihan
1. Buat Elixir menghitung jumlah detik dalam sehari dengan mengalikan jam dalam sehari dua kali. Berapa banyak detik dalam sehari?
2. Hitung rata-rata dari angka-angka ini: 4, 8, 15, 16, 23 dan 42.
Catatan: Anda dapat menemukan solusi untuk semua latihan di site ini di bagian solusi di belakang site ini.

---

#### 2. Now, where did I put that value?

Kita sekarang telah melihat bahwa Elixir dapat menangani kata-kata dan angka dengan mudah. Tapi, apa lagi yang bisa dilakukannya? Nah, Elixir dapat mengingat hal-hal.

```elixir linenums="1"
iex> sentence = "A really long and complex ⏎
sentence we'd rather not repeat."
```

```elixir linenums="1"
"A really long and complex ⏎
sentence we'd rather not repeat."
```

```elixir linenums="1"
iex> score = 2 / 5 * 100
40
```

```elixir linenums="1"
iex> x = "not for multiplication"
"not for multiplication"
```

Selama kita membiarkan `iex` berjalan, Elixir akan mengingat bahwa `sentence` adalah "A really long and complex sentence we'd rather not repeat.", `score` adalah 40, dan `x` adalah "not for multiplication". Pada titik mana pun, kita dapat menanyakan apa itu `sentence`, `score`, atau `x`, dan ia akan memberi tahu kita:

```elixir linenums="1"
iex> sentence
"A really long and complex sentence we'd rather not repeat."
```

```elixir linenums="1"
iex> score
40
```

```elixir linenums="1"
iex> x
"not for multiplication"
```

`sentence`, `score`, dan `x` di sini adalah variabel, dan mereka diberikan nama tersebut karena sesuatu yang diingat komputer dengan nama `sentence`, `score`, atau `x` dapat bervariasi. Ingat ketika kita berbicara tentang mengalikan angka dan kita melihat bahwa kita tidak bisa menggunakan `x` untuk mengalikan? Alasan untuk ini adalah karena Elixir akan membaca `x` sebagai variabel, bukan sebagai saran untuk mengalikan angka di kedua sisi. Jadi, kita akan terus menggunakan `*` sebagai gantinya.

Kita dapat memberi tahu komputer untuk mengganti definisi variabel dengan yang lain. Ini sering disebut sebagai penugasan ulang. Mari kita ganti (atau penugasan ulang) definisi variabel `sentence`:

```elixir linenums="1"
iex> sentence = "An even longer and significantly more complex sentence ⏎
that we might be ok with repeating, if the mood takes us."
```

```bash
"An even longer and significantly more complex sentence ⏎
that we might be ok with repeating, if the mood takes us."
```

Kemudian, ketika kita menanyakan kepada komputer apa itu `sentence`, ia akan melupakan kalimat lama dan hanya akan mengetahui yang baru:

```elixir linenums="1"
iex> sentence
"An even longer and significantly more complex sentence ⏎
that we might be ok with repeating, if the mood takes us."
```

Sekarang masyarakat terlihat lebih ceria. Beberapa bahkan tersenyum! Bukankah itu luar biasa? Mari kita buat variabel lain yang disebut `place`:

```elixir linenums="1"
iex> place = "World"
"World"
```

Komputer sekarang akan mengingat bahwa `place` adalah "World". "Tapi, apa gunanya hanya mengatur variabel seperti ini? Mengapa membuat komputer mengingat sama sekali?", kata Isodora (juru bicara). "Juru bicara, terima kasih", kata Isodora, merobohkan dinding keempat lagi. Oke, Isodora (juru bicara) mengucapkan hal-hal itu. Ngomong-ngomong, kita sekarang sudah mengetahui nama juru bicara tersebut adalah Isodora, dan kita telah melakukan sedikit penciptaan variabel di otak kita sendiri: `spokesperson` = "Isodora". Woah. "Sebut saja saya Izzy", kata IsodoraIzzy. Oke, kita akan -- membuat otak kita mengubah penugasan variabel juru bicara: `spokesperson` = "Izzy".

Oke, Izzy benar. Kita harus melakukan sesuatu yang berarti dengan variabel ini. Oke, Izzy, bagaimana dengan ini? [memijat jari]

```elixir linenums="1"
iex> "Hello, #{place}!"
"Hello, World!"
```

Masyarakat menjadi heboh. Ini adalah kekacauan! Kemudian setelah beberapa gerakan menenangkan dengan tangan saya (yang sama sekali tidak berfungsi) dan cepat "OI!" dari Izzy, mereka (sebagian besar) kembali tenang.

"Apa yang baru saja terjadi?", tanya Izzy. Tapi Anda, Pembaca Yang Budiman, sudah mengajukan pertanyaan itu. Izzy tidak mendengar karena kerumunan dan kekacauan yang luar biasa.

Apa sebenarnya karakter aneh di sekitar `place` itu? Anda bisa menganggapnya sebagai placeholder. Tipe nerd yang lebih nerdy akan menyebutnya interpolasi. Ini memberi tahu komputer bahwa kita ingin menempatkan variabel `place` tepat di sini, tepat setelah Hello dan spasi, dan tepat sebelum !.

Interpolasi variabel ke dalam string
Contoh Bagian 2.1: Interpolasi variabel ke dalam string
Komputer mengambil kalimat yang kita berikan, menyadari bahwa ada indikator placeholder aneh #{} itu, dan ia mengingat apa itu `place` dan menempatkannya tepat di sana. Cukup keren, bukan?

##### Latihan
1. Jika kita menyimpan jumlah detik dalam sehari menggunakan kode ini: `seconds = 86400`, hitung menggunakan variabel tersebut berapa jam dalam 30 hari.
2. Buat variabel yang disebut `name`, simpan string di dalamnya, dan tempatkan nilai variabel tersebut dalam string lain.
3. Baris `5 / "four"` menunjukkan kesalahan. Pikirkan tentang mengapa kesalahan ini bisa terjadi.

---

#### 3. Lovely lists

Tapi, apa lagi yang bisa dilakukan Elixir? Kita telah melihat bahwa ia dapat menangani string dan dapat mengatasi persamaan matematis dengan mudah, serta dapat mengingat hal-hal. Tapi, apa lagi? Nah, bagaimana jika kita memiliki daftar hal-hal yang ingin kita ingatkan kepada komputer? Dan kita ingin komputer mengingat daftar hal-hal ini dalam urutan tertentu?

Kita bisa melakukan ini dengan menetapkan setiap hal ke variabel yang unik:

```elixir linenums="1"
iex> first = "fish"
"fish"
```

```elixir linenums="1"
iex> second = "ham"
"ham"
```

```elixir linenums="1"
iex> third = "eggs"
"eggs"
```

Tapi kemudian kita harus mengingat bahwa hal-hal yang kita inginkan disimpan dalam variabel `first`, `second`, dan `third`. Dan bagaimana jika kita — sebagai manusia — lupa posisi mana yang kita inginkan?

```elixir linenums="1"
iex> fifth = "bread"
"bread"
```

Bencana! Ini tidak akan berhasil.

Solusi yang lebih baik untuk membuat komputer mengingat daftar di Elixir adalah dengan memberi tahu bahwa yang kita simpan adalah sebuah daftar. Untuk melakukannya, kita membungkus daftar kita dalam tanda kurung siku ([]) dan memisahkan setiap item dalam daftar dengan koma:

```elixir linenums="1"
iex> shopping_list = ["fish", "ham", "eggs", "bread"]
["fish", "ham", "eggs", "bread"]
```

Sama seperti kita perlu memulai dan mengakhiri string dengan tanda kutip ganda, kita perlu memulai dan mengakhiri daftar dengan tanda kurung siku ([]).

Komputer sekarang akan mengingat seluruh daftar belanja kita dalam satu variabel (`shopping_list`), daripada mengingatnya di beberapa variabel. Sekarang kita memiliki satu tempat untuk pergi untuk daftar belanja kita.

Kita juga dapat menggunakan lebih dari sekadar string saat kita membuat daftar. Misalkan kita ingin memiliki daftar suhu terakhir (dalam celsius) dari lima hari terakhir. Kita bisa merepresentasikan data ini seperti ini:

```elixir linenums="1"
iex> temperatures = [15, 17, 19, 20, 20]
```

Faktanya, apa pun di Elixir bisa menjadi item dalam sebuah daftar.

Izzy, yang terkesan dengan kemampuan Elixir untuk menyimpan daftar apa pun yang diinginkannya, mulai mencatat nama-nama orang yang ada di kerumunan. Komputernya muncul entah dari mana, atau mungkin dari suatu tempat di kerumunan terdekat. Terlalu cepat untuk benar-benar diperhatikan. Ia mulai mencatat nama, jarinya meluncur di atas keyboard:

```elixir linenums="1"
iex> those_who_are_assembled = [
"Izzy",
"The Author",
"The Reader",
"Juliet",
"Mary",
"Bobalina",
"Charlie",
"Charlie (no relation)"
]
["Izzy", ...]
```

##### Apakah Anda melihat apa yang Izzy lakukan di sana?
  
Ia memulai daftar dalam satu baris dan kemudian melanjutkannya pada baris berikutnya. Ketika ia menyelesaikan daftarnya, komputer kemudian mengambil semua baris, memprosesnya sebagai satu instruksi besar dan mempersembahkan kita dengan daftar yang sudah jadi. Elixir memungkinkan kita menulis daftar dalam beberapa baris seperti ini, yang sangat berguna karena membantu keterbacaan!

Dan demikianlah Izzy terus melanjutkan. Ia menghilang ke kerumunan langsung di sebelah kanan kita, dan entah bagaimana muncul kembali dalam beberapa detik di sebelah kiri kita. Ini terjadi meskipun kerumunan sangat padat. Hal yang menakjubkan. Ia kemudian bertanya: "Hey Mr. Author Guy, saya juga ingin melacak usia orang-orang supaya saya bisa melakukan statistik tentang siapa yang sebenarnya berkumpul di sini. Oh, dan saya juga ingin melacak gender mereka. Tapi daftar tampaknya tidak terlalu cocok untuk ini. Bagaimana saya bisa melakukannya?"

Nah Izzy, ada lebih dari satu cara untuk melakukan ini. Jika yang ingin Anda lacak tentang seseorang hanyalah nama, usia, dan gender mereka, Anda bisa membuat setiap item dalam daftar menjadi daftarnya sendiri:

```elixir linenums="1"
iex> those_who_are_assembled = [
...> ["Izzy", "30ish", "Female"],
...> ["The Author", "30ish", "Male"],
...> ]
```

Daftar-di-dalam-daftar ini akan disebut sub-daftar. Anda kemudian harus ingat bahwa item pertama dalam setiap sub-daftar adalah nama, yang kedua adalah usia, dan yang ketiga adalah gender. Bagaimana jika Anda (atau orang lain yang menggunakan komputer Anda) lupa urutan dan mulai menambahkan orang, dengan usia dan gender yang bertukar posisi?

```elixir linenums="1"
iex> those_who_are_assembled = [
...> ["Izzy", "30ish", "Female"],
  ... a long time passes ...
...> ["Izzy the Younger", "Female", "20ish"],
...> ]
```

Kekacauan lagi! Kita perlu cara yang lebih baik untuk menegakkan data apa yang kita kumpulkan untuk setiap orang. Kita perlu struktur data yang lebih baik daripada daftar dalam daftar. Baca terus untuk mengetahui apa struktur data itu!

---

#### 4. Marvellous maps

Kembali di bab sebelumnya, Izzy mencoba melacak informasi tentang orang-orang yang berkumpul menggunakan beberapa daftar di dalam daftar lain:

```elixir linenums="1"
those_who_are_assembled = [
  ["Izzy", "30ish", "Female"],
  ... waktu berlalu lama ...
  ["Izzy the Younger", "Female", "20ish"],
]
```

Namun seperti yang kita lihat di sini, urutan item dalam daftar bisa salah input karena kesalahan manusia. Kita memerlukan sesuatu yang membantu mencegah kesalahan manusia seperti ini, dan jika sesuatu itu bisa membantu menunjukkan apa masing-masing item dalam daftar — dengan memberikan semacam nama — maka itu juga akan sangat baik.

Untuk itu, kita bisa menggunakan sebuah peta. Sama seperti peta biasa, peta di Elixir dapat memberi tahu kita di mana menemukan sesuatu, jika saja kita tahu di mana mencarinya.

Mari kita lihat bagaimana kita bisa mengumpulkan data seorang individu menggunakan peta, menggunakan anggota acak dari kerumunan sebagai contoh:

```elixir linenums="1"
person = %{"name" => "Roberto", "age" => 56, "gender" => "Male"}
%{"age" => 56, "gender" => "Male", "name" => "Roberto"}
```

Peta dimulai dengan `%` dan mengurung datanya dalam kurung kurawal. Dalam peta, kita menyusun data menggunakan kunci dan nilai. Hal di sebelah kiri dari `=>` disebut kunci dan hal di sebelah kanan disebut nilai.

**sebuah kunci dan nilainya**  
*Contoh bagian 4.1: Sebuah kunci dan nilainya*  
Seperti di peta sesuatu seperti kota atau jalur berjalan, kunci di sini memberi tahu kita di mana menemukan nilai tertentu. Jika, misalnya, kita ingin tahu usia orang ini, kita bisa menggunakan kunci "age" untuk mengambil nilai itu. Kita akan melihat itu dalam sekejap.

Berbeda dengan string dan daftar di mana kita bisa menggunakan satu karakter di awal dan akhir untuk menunjukkan kepada Elixir di mana awal dan akhirnya -- tanda kutip ganda untuk string, kurung siku untuk daftar -- kita perlu menggunakan "pelukan kurung kurawal" untuk peta. Kita perlu menggunakan `%{` untuk memberi tahu Elixir di mana peta dimulai dan `}` untuk menunjukkan di mana berakhir.

Anda mungkin memperhatikan di sini bahwa komputer telah mengambil peta kita dan mengembalikan kunci dalam urutan yang berbeda dari yang kita tentukan. Urutan kunci tidak penting dalam peta sama sekali, berbeda dengan daftar di mana urutan memang penting. Akan sangat aneh menghabiskan waktu untuk mengurutkan daftar hanya agar Elixir mengembalikannya dalam urutan yang tidak masuk akal. Misalnya, jika kita memiliki daftar seperti ini:

```elixir linenums="1"
favourite_people = ["The Reader", "Izzy", ...]
```

Daftar ini menunjukkan bahwa "The Reader" adalah orang favorit pertama, dan bahwa Izzy adalah yang kedua (dekat). Urutan di sini penting. Untuk peta, tidak masalah urutan kunci dan nilai yang sesuai karena peta tersebut tetap sama:

```elixir linenums="1"
person = %{"gender" => "Male", "age" => 56, "name" => "Roberto"}
%{"age" => 56, "gender" => "Male", "name" => "Roberto"}
```

Posisi kunci "name" dalam peta tidak memiliki makna. Kunci untuk peta bisa dalam urutan apapun.

Anda mungkin sekarang berpikir tentang bagaimana mendapatkan data kembali dari peta setelah Anda memasukkannya. Kita sudah membicarakan tentang bagaimana "mengambil" nilai itu sebelumnya, tetapi belum melihat contohnya. Untuk mengakses nilai dari peta kita perlu mengetahui kunci yang sesuai. Setelah kita tahu kunci yang sesuai, maka kita bisa menggunakan `[]` untuk mengambil nilai itu dari peta. Pikirkan ini seperti cakar dari sebuah mesin pengambil, yang menyelam untuk mengambil nilai.

**mesin pengambil**  
*Contoh bagian 4.2: Mesin pengambil*  
Berbeda dengan mesin pengambil biasa, kurung siku ini tidak dipasang untuk menjatuhkan nilai beberapa inci dari saluran; kurung siku ini memiliki cengkeraman yang kuat. Misalnya, jika kita ingin mendapatkan nilai "name" untuk orang tersebut kita bisa melakukan:

```elixir linenums="1"
person["name"]
"Roberto"  
```
Dan jika kita ingin mendapatkan usia, kita akan menggunakan kunci "age":

```elixir linenums="1"
person["age"]
56
```
  
Izzy mengeluarkan suara berpikir "Mmmmmmmmmm" yang sangat dekat dengan persetujuan. Dia menyukai peta. Sekarang Izzy bisa tahu data tepat yang kita kumpulkan tentang massa yang berkumpul, tanpa khawatir tentang bagaimana data itu terurut, dan kemudian menggunakannya untuk nanti. Kita belum tahu apa yang ada di pikiran Izzy untuk data tersebut, tetapi dia mengumpulkannya untuk suatu alasan. Atau setidaknya, sepertinya begitu.

Untuk mengumpulkan data tentang semua orang yang berkumpul di sini di depan kita, kita bisa membuat daftar peta:

```elixir linenums="1"
those_who_are_assembled = [
  %{"name" => "Izzy", "age" => "30ish", "gender" => "Female"},
  %{"name" => "The Author", "age" => "30ish", "gender" => "Male"},
  %{"name" => "The Reader", "age" => "Unknowable", "gender" => "Unknowable"},
]
```

Seperti yang kita lihat dari contoh ini, daftar bisa berisi lebih dari sekedar angka dan string: kita bisa menggunakan peta juga!

Daftar peta yang berisi informasi kerumunan ini kebal terhadap masalah yang kita lihat di awal bab ini. Tidak masalah urutan kombinasi kunci-nilai dari usia, nama, atau gender ditempatkan -- peta akan berisi informasi yang tepat di tempat yang tepat. Sebagai bonus tambahan, kita bisa merujuk nilai-nilai ini dengan kunci mereka, alih-alih harus mengingat posisinya.

##### Other types of keys

Sebelum kita melanjutkan, saya ingin kita merenung sedikit lebih lama tentang peta. Sejauh ini, kita telah melihat bahwa peta terdiri dari serangkaian kunci dan nilai. Kunci-kunci dalam peta kita hanya berupa string, tetapi nilai-nilainya telah berupa campuran string (untuk nama dan gender) dan angka (untuk usia). Ini memberikan petunjuk tentang apa yang bisa disimpan oleh peta, tetapi saya ingin membahas beberapa kasus lagi agar kita benar-benar memahami tentang peta ini.

Sebenarnya, di Elixir, kunci dan nilai bisa berupa apa saja yang Anda inginkan. Kunci bisa berupa angka, string, daftar, dan lainnya. Nilai juga bisa berupa apa saja. Mari kita katakan kita meminta sepuluh orang untuk memilih angka dalam rentang 1 hingga 5. Anda bisa menggunakan kunci angka untuk mewakili angka yang dipilih orang-orang tersebut:

```elixir linenums="1"
choices = %{
  1 => 4,
  2 => 1,
  3 => 2,
  4 => 2,
  5 => 1,
}
%{1 => 4, 2 => 1, 3 => 2, 4 => 2, 5 => 1}
```

Kemudian Anda bisa dengan mudah mengetahui berapa banyak orang yang memilih angka 1 atau 2 dengan menggunakan kurung siku seperti cakar mesin pengambil:

```elixir linenums="1"
choices[1]
4  
```
```elixir linenums="1"
choices[2]
1  
```
Jadi seperti yang kita lihat di sini, kita bisa dengan mudah menggunakan angka sebagai kunci dan nilai dalam peta, dan Elixir sama sekali tidak masalah dengan itu. Sama seperti kita bisa menggunakan apa saja sebagai item dalam daftar, Elixir juga memungkinkan kita menggunakan apa saja sebagai kunci dan nilai dalam peta.

Sekarang kita telah menetapkan itu, saya ingin memperkenalkan Anda pada satu tipe data lagi dalam Elixir melalui sedikit contoh kode. Salah satu kejadian umum dalam kode Elixir yang mungkin Anda lihat adalah peta yang terlihat seperti ini:

```elixir linenums="1"
person = %{
  name: "Izzy",
  age: "30ish",
  gender: "Female"
}
```

Ini adalah cara singkat untuk menulis:

```elixir linenums="1"
person = %{
  :name => "Izzy",
  :age => "30ish",
  :gender => "Female"
}
```

Kunci di kedua contoh ini bukan angka, string, daftar, atau peta. Tapi mereka terlihat sedikit seperti string, bukan? Jadi, apa mereka? Kunci-kunci ini disebut atom. Mereka adalah tipe data di Elixir yang umum digunakan untuk merepresentasikan nama-nama sesuatu, seperti dalam kasus ini. Mereka adalah nama sederhana, dan tidak lebih dari itu. Kita akan melihat lebih banyak dari mereka saat kita melanjutkan materi ini, jadi sangat berguna untuk tahu apa mereka sekarang.

Sama seperti kita dapat mengakses nilai yang terkait dengan string dan angka, kita juga dapat mengakses nilai yang terkait dengan kunci atom dengan menggunakan kurung siku seperti ini:

```elixir linenums="1"
person[:name]
"Izzy"  
```
Ini sedikit lebih sedikit pengetikan dibandingkan `person["name"]`, dan cara kita mendefinisikan peta juga sedikit lebih pendek, jadi umumnya lebih disukai menggunakan atom dibandingkan string untuk kunci dalam peta. Ini adalah alasan mengapa Anda mungkin sering melihatnya dalam kode Elixir orang lain juga.

Ada satu keuntungan lagi menggunakan atom sebagai kunci dibandingkan string: kita dapat menggunakan sintaks yang bahkan lebih pendek untuk membaca nilai-nilai tersebut:

```elixir linenums="1"
person.name
"Izzy"  
```
Ini adalah tiga karakter lebih pendek daripada cara lain yang telah kita lihat untuk bekerja dengan peta. Mengurangi pengetikan selalu hal yang baik. Dan kode terlihat lebih rapi tanpa semua tanda baca yang mengganggu.

Jadi mulai dari sini, kita akan sebagian besar menggunakan atom untuk kunci dalam peta hanya karena ini mengurangi pengetikan dan membuat kode kita sedikit lebih bersih untuk dikerjakan.

Dan sekarang, untuk kembali ke pengumpulan informasi tentang siapa yang berkumpul di sini hari ini. Untuk ini, kita bisa menggunakan daftar peta dan membuat peta-peta tersebut memiliki kunci yang merupakan atom, dan nilai yang berupa string:

```elixir linenums="1"
those_who_are_assembled = [
  %{name: "Izzy", age: "30ish", gender: "Female"},
  %{name: "The Author", gender: "Male", age: "30ish"},
  %{name: "The Reader", gender: "Unknowable", age: "Unknowable"},
]
```

Izzy dengan bersemangat menghilang ke dalam kerumunan lagi dengan pengetahuan peta baru ini dan mulai mengumpulkan informasi orang-orang lagi.

---

#### 5. Funky functions

Setelah sekitar setengah jam, Izzy muncul kembali dari tempat yang tampaknya entah di mana. Layar komputernya bersinar dengan informasi yang telah dia kumpulkan dari kerumunan. Kami tidak yakin seberapa lama dia sudah kembali, tetapi begitu perhatian kami tertuju padanya, dia berbicara: "Oke, jadi kamu dapat mewakili berbagai... jenis hal di Elixir — string, angka, daftar, peta — tetapi apa gunanya semua itu? Apa yang bisa kamu lakukan dengan mereka? Apakah saya perlu menulis kode untuk bekerja dengan berbagai jenis hal ini sepanjang waktu? Bisakah komputer juga mengingat kode?"

Nah, Izzy, itu adalah transisi yang sangat cerdas dan sepenuhnya tidak disengaja menuju bagian berikutnya dari materi ini. Terima kasih telah melakukannya.

Ya, sebenarnya kamu bisa memberi tahu komputer untuk mengingat beberapa kode juga. Ini menghemat banyak pengetikan. Sangat banyak hal. Kamu akan mendapatkan bertahun-tahun hidupmu kembali!

Oke, cukup berbasa-basi. Mari kita lihat satu cara kita bisa menggunakan untuk membuat komputer mengingat beberapa kode:

```elixir
iex> greeting = fn (place) -> "Hello, #{place}!" end
#Function<6.52032458/1 in :erl_eval.expr/5>
```

Ini disebut fungsi dan kita bisa menulis kode apa pun yang kita inginkan agar komputer mengingatnya untuk nanti, sama seperti kita bisa memberi tahu komputer untuk mengingat sebuah string, angka, daftar, atau peta. Kode Elixir sepenuhnya tentang fungsi, dan sekarang kita mengerti mengapa Wikipedia menyebutnya sebagai bahasa "fungsional". Itu tidak berarti bahwa itu fungsional dalam arti operasional, tetapi lebih pada fakta bahwa ia menggunakan fungsi untuk menyelesaikan tugas. Kamu akan melihat banyak fungsi dalam kode Elixir dari sini ke depan.

`fn` memberi tahu komputer bahwa kita akan mendefinisikan sebuah fungsi — karena mengetikkan "fungsi" setiap kali hanya akan terlalu banyak untuk kita tanggung — dan mendefinisikan fungsi tidak berhenti sampai kita mencapai akhir. Sama seperti kamu tidak akan berhenti sampai kamu mencapai akhir sesuatu — misalnya, sebuah buku — kan?

`(place)` di sini mendefinisikan argumen untuk fungsi; anggap saja seperti variabel yang hanya tersedia di dalam fungsi ini dan bukan di dalam pertengkaran yang biasa bisa terjadi pada argumen yang normal. `->` memberi tahu komputer bahwa kita telah selesai mendefinisikan argumen untuk fungsi, dan apa pun setelah ini tetapi sebelum akhir adalah kode yang akan dijalankan.

![functional definition example](https://joyofelixir.com/5-funky-functions/images/function-definition.png)

Begitu kita menekan enter di akhir baris ini, komputer memberi kita beberapa output untuk menunjukkan bahwa ia telah menerima fungsi kita. Ini bukan output yang paling ramah, tetapi setidaknya ini memberi tahu kita bahwa komputer telah melakukan sesuatu.

```elixir linenums="1"
greeting = fn (place) -> "Hello, #{place}!" end
#Function<6.52032458/1 in :erl_eval.expr/5>  
```

Kita telah menetapkan fungsi kita ke variabel `greeting`, dan itulah yang akan diingat komputer sebagai fungsi tersebut. "Bagaimana kita menggunakan fungsi ini?", tanya Izzy dengan penuh perhatian, tiba-tiba terkesan dengan kemampuan komputer untuk mengingat fungsi. Saya yakin kamu juga bertanya hal yang sama, pembaca yang terhormat.

Nah, Izzy (dan pembaca terkasih), kita perlu menggunakan kode baru dan menarik yang belum kita lihat:

```elixir linenums="1"
greeting.("World")
"Hello, World!"  
```

Inilah cara kita membuat fungsi berjalan. Kita menjalankan fungsi ini dengan menambahkan titik setelah namanya. Kurung setelah titik ini mewakili argumen untuk fungsi. Kali ini kita memanggil fungsi, `place` akan menjadi "World". Tetapi itu tidak selalu harus "World". Itu bisa berupa apa pun yang kamu inginkan:

```elixir linenums="1"
greeting.("Mars")
"Hello, Mars!"  
greeting.("Narnia")
"Hello, Narnia!"  
greeting.("Motherland")
"Hello, Motherland!"  
```

Setiap kali kita menjalankan fungsi di sini, kita memberikan nilai baru untuk `place`. Kita tidak perlu mengatur `place` sendiri, karena fungsi itu mengurusnya. Tetapi bagaimana dengan variabel `place` kita dari tahun lalu (baris 9 di iex)? Apakah itu berubah?

```elixir linenums="1"
place
"World"  
```

Komputer tahu bahwa `place` dari luar fungsi berbeda dengan `place` di dalam fungsi, sehingga menjaga keduanya terpisah. Komputer cukup pintar untuk tahu bahwa `place` di luar mungkin tidak ada, dan oleh karena itu tidak seharusnya bergantung pada keberadaannya. Fungsi tersebut mengandung semua yang dibutuhkan untuk dijalankan di dalam dirinya sendiri.

Fungsi-fungsi kita sejauh ini hanya mengambil string dan menempatkannya di dalam string lain, tetapi fungsi mampu mengeksekusi kode apa pun, jadi mari kita lihat dengan cepat fungsi lain. Fungsi ini akan mengonversi suhu dalam unit Celsius yang masuk akal ke dalam ekuivalen Fahrenheit yang aneh, menggunakan angka alih-alih string:

```elixir linenums="1"
c_to_f = fn (c) -> c * 1.8 + 32 end
```

Persamaan matematis untuk mengonversi Celsius ke Fahrenheit adalah dengan mengalikan dengan 1.8 dan kemudian menambahkan 32, yang persis seperti yang kita lakukan dalam fungsi kita: kita mengambil `c` yang mewakili angka dalam Celsius, mengalikannya (*) dengan 1.8, dan kemudian menambahkan (+) 32.

Mari kita jalankan fungsi kita dengan beberapa suhu Celsius:

```elixir linenums="1"
c_to_f.(20)
68.0  
c_to_f.(24)
75.2  
c_to_f.(40)
104.0  
```

Jika kamu ingin memeriksa ini, masukkan angka-angka ini ke dalam Google yang tahu segalanya menggunakan pencarian seperti "20 Celsius dalam Fahrenheit", dan Google akan mengonfirmasi jawaban ini.

##### Multiple-argument functions

Satu lagi hal yang berguna tentang fungsi adalah bahwa mereka tidak terbatas pada satu argumen saja. Kamu dapat mendefinisikan fungsi yang menerima sebanyak mungkin argumen yang kamu inginkan:

```elixir linenums="1"
greeting = fn (name, gender, age) ->
  "Hello, #{name}! I see you're #{gender} and you're #{age} years old."
end
#Function<18.52032458/3 in :erl_eval.expr/5>  
```

Fungsi ini memiliki 3 argumen, jadi ketika kita menjalankannya, kita perlu memberinya ketiga argumen tersebut. Untuk melakukannya, kita hanya memisahkan mereka menggunakan koma, mirip dengan cara kita memisahkan item dalam daftar sebelumnya, hanya tanpa kurung siku ([]) di sekitar argumen ini.

```elixir linenums="1"
greeting.("Izzy", "Female", "30ish")
"Hello, Izzy! I see you're Female and you're 30ish years old!"  
```

Kita bisa melakukan banyak hal dengan jumlah argumen yang didefinisikan dalam sebuah fungsi. Namun, kita perlu berhati-hati saat menjalankan fungsi-fungsi tersebut. Jika kita menyebutkan jumlah argumen yang salah, Elixir akan memberi tahu kita dengan teks merah besar:

```elixir linenums="1"
greeting.("Izzy")
** (BadArityError) #Function<18.52032458/3 in :erl_eval.expr/5>⏎  
  with arity 3 called with 1 argument ("Izzy")  
```

Oh tidak, komputer marah pada kita. Yah, jika komputer merasakan emosi dari ketidakpedulian brutal, mungkin itu adalah beberapa versi kemarahan, atau setidaknya kekecewaan. Kita baru saja membuat kesalahan kecil yang menyenangkan dengan menyebutkan 3 argumen. Komputer sedang memperingatkan kita: memberi tahu kita bahwa kita telah menyebabkan `BadArityError` dan itu berarti kita memiliki "<function> with arity 3 called with 1 argument".

"Apa itu 'arity'?" tanya Izzy, jelas bingung (dan mungkin sedikit tersinggung) oleh kata tersebut. Berbeda dengan komputer, Izzy tidak bersikap acuh tak acuh terhadap hal-hal ini. Setelah semua, Izzy berpikir dia sudah memahami hal ini dalam Elixir.

**Arity** adalah istilah komputer yang berarti "argumen". Kesalahan ini menyatakan bahwa meskipun fungsi greeting didefinisikan dengan 3 argumen ("dengan arity 3"), kita hanya menjalankannya ("memanggil") dengan 1 argumen. Untungnya, ini memberi tahu kita argumen apa yang kita coba berikan pada fungsi tersebut. Untuk menghindari komputer memperingatkan kita, kita harus memastikan untuk memanggil fungsi dengan jumlah argumen yang tepat.

##### Capture operator

Elixir menyediakan kita dengan konstruk `fn` sehingga kita bisa menulis fungsi, dan kita sudah melihat beberapa contoh itu sejauh ini. Ada satu konstruk lain yang mungkin kamu lihat jika kamu membaca kode orang lain, dan itu disebut **capture operator**, dan ini terlihat seperti ini:

```elixir linenums="1"
captured_greeting = &("Hello #{&1}!")
```

Kita harus membungkus seluruh isi fungsi dengan kurung, dan kemudian di dalam kurung tersebut kita bisa menggunakan `&1` untuk menangkap argumen pertama yang diteruskan ke fungsi ini, `&2` untuk menangkap argumen kedua, dan seterusnya. Untuk saat ini, kita hanya menangkap satu.

Fungsi ini secara fungsional (ahem) setara dengan fungsi greeting pertama kita:

```elixir linenums="1"
greeting = fn (name) -> "Hello #{name}!" end
```

Kita bisa melihat ini jika kita memanggil kedua fungsi dengan argumen yang sama:

```elixir linenums="1"
captured_greeting.("World")
"Hello World!"  
greeting.("World")
"Hello World!"  
```

Seperti yang saya sebutkan sebelumnya, kamu dapat menangkap sebanyak mungkin argumen yang kamu inginkan. Kita bisa mengambil fungsi greeting dengan 3 argumen dari sebelumnya:

```elixir linenums="1"
greeting = fn (name, gender, age) ->
  "Hello, #{name}! I see you're #{gender} and you're #{age} years old."
end
```

Dan kita bisa menulisnya dengan cara yang sedikit lebih pendek menggunakan **capture operator**:

```elixir linenums="1"
captured_greeting = &("Hello, #{&1}! I see you're #{&2} and you're #{&3} years old.")
```

Kemudian kita bisa memanggilnya dengan tiga argumen juga:

```elixir linenums="1"
captured_greeting.("Izzy", "Female", "30ish")
"Hello, Izzy! I see you're Female and you're 30ish years old!"  
```

Fungsi yang ditulis dengan konstruk `fn` dan capture operator berperilaku identik. Satu-satunya perbedaan adalah bahwa sintaks capture operator lebih pendek, dan kamu merujuk pada argumen berdasarkan posisinya, bukan berdasarkan nama.

##### Saving code for later

Sementara semuanya baik dan benar untuk menjalankan kode melalui prompt iex, kamu mungkin ingin menyimpan beberapa kode untuk dijalankan nanti. Mungkin pada titik ini kamu memiliki ide tentang sesuatu yang ingin dicoba dan ingin menyimpannya di suatu tempat untuk nanti karena prompt iex hanya akan mengingat apa yang kamu ketik selama terbuka. Begitu ditutup, kode itu hilang selamanya dan kamu perlu mengetiknya semua lagi.

Untuk menyimpan kode Elixir kamu, kamu bisa membuat file baru di editor teks favoritmu, masukkan kode yang kamu inginkan, dan kemudian simpan dengan nama seperti `hello.exs`. Akhiran `.exs` menandakan bahwa file tersebut adalah file Elixir Script.

Untuk menjalankan kode di dalam file, cukup jalankan `elixir hello.exs`. Tidak perlu lagi prompt sekarang!

##### Exercises

- Buatlah fungsi yang mengubah suhu Fahrenheit menjadi Celsius.
- Buatlah fungsi yang mengembalikan jumlah detik dalam jumlah hari yang ditentukan. Misalnya, `seconds.(2)` harus memberi tahu kita berapa detik ada dalam 2 hari.
- Buatlah fungsi yang mengambil dua peta dengan kunci "age" di dalamnya dan mengembalikan rata-rata usia.
- Simpan salah satu dari tiga solusi ini di file mereka sendiri dan jalankan melalui alat baris perintah Elixir.

---

#### 6. Pattern Matching

Kembali di Bab 2, kamu melihat bahwa tanda sama dengan (`=`) membuat komputer mengingat sesuatu.

```elixir linenums="1"
sentence = "A really long and complex ⏎
sentence we'd rather not repeat."

"A really long and complex ⏎
sentence we'd rather not repeat."

score = 2 / 5 * 100
40  
```

Meskipun ini memang masih benar, tanda sama dengan (`=`) dapat melakukan lebih dari sekadar menetapkan satu nilai pada satu waktu. (Izzy terkejut dengan kalimat terakhir, sementara kerumunan berbisik.) Ada fitur tersembunyi dari Elixir yang belum kita tunjukkan, dan fitur tersebut disebut **pattern matching**. Kamu akan sering menggunakan fitur ini saat memprogram dengan Elixir — sebanyak fungsi! — jadi kita akan menghabiskan waktu membahasnya di sini juga di bab ini.

##### Equals is not just for equality

Tanda sama dengan (`=`) tidak hanya tentang menetapkan sesuatu untuk membuat komputer mengingatnya, tetapi juga dapat digunakan untuk mencocokkan sesuatu. Kamu bisa memikirkan ini seperti tanda sama dengan dalam matematika, di mana sisi kiri harus sama dengan (atau "cocok") dengan sisi kanan agar persamaan itu valid.

Misalnya, jika kita mencoba membuat `2 + 2 = 5`, mirip dengan apa yang diinginkan Partai dalam *Nineteen Eighty Four* untuk kita percayai, Elixir tidak akan mengizinkannya:

```elixir linenums="1"
5 = 2 + 2
** (MatchError) no match of right hand side value: 4  
```

Berbeda dengan Mr. Winston Smith yang terkenal, Elixir tidak dapat dipaksa untuk tidak percaya pada kenyataan. Di sini, Elixir memberi tahu kita bahwa `2 + 2` memang bukan `5`. Dalam Elixir, sisi kiri harus dievaluasi menjadi nilai yang sama dengan sisi kanan. Ini akan membuat komputer senang:

```elixir linenums="1"
4 = 2 + 2
4  
```

Demikian pula, memiliki dua string identik di kedua sisi tanda sama dengan juga akan membuat komputer senang:

```elixir linenums="1"
"dog" = "dog"
"dog"  
```

Mari kita lakukan sesuatu yang lebih kompleks daripada memiliki hal yang sama di kedua sisi tanda sama dengan. Mari kita lihat bagaimana kita dapat melakukan pattern matching pada daftar.

##### Pattern matching with lists

Misalkan kita memiliki daftar semua orang yang berkumpul di sini, seperti yang kita miliki di akhir Bab 4:

```elixir linenums="1"
those_who_are_assembled = [
  %{age: "30ish", gender: "Female", name: "Izzy"},
  %{age: "30ish", gender: "Male", name: "The Author"},
  %{age: "56", gender: "Male", name: "Roberto"},
  %{age: "38", gender: "Female", name: "Juliet"},
  %{age: "21", gender: "Female", name: "Mary"},
  %{age: "67", gender: "Female", name: "Bobalina"},
  %{age: "54", gender: "Male", name: "Charlie"},
  %{age: "10", gender: "Male", name: "Charlie (no relation)"},
]
```

Dan katakanlah kita ingin mengambil tiga orang pertama dalam daftar ini, tetapi kemudian mengabaikan sisanya — mengingat bahwa ketiga orang ini jelas merupakan orang-orang terpenting di sini. Kita dapat menggunakan pattern matching pada daftar ini:

```elixir linenums="1"
[first, second, third | others] = those_who_are_assembled
```

Dengan kode ini, kita memberi tahu Elixir untuk menetapkan item pertama, kedua, dan ketiga dari daftar ke variabel `first`, `second`, dan `third`. Kita juga memberitahu untuk menetapkan sisa daftar ke variabel `others`, dan kita menyebutkan ini dengan menggunakan simbol pipa (`|`). Dalam kode ini kita telah memilih 3 item pertama dari daftar, tetapi kita juga bisa memilih yang pertama, atau yang pertama hingga 5. Itu tidak harus tepat 3.

Kita dapat memeriksa apa yang telah dilakukan ini dengan melihat nilai masing-masing variabel ini di `iex`:

```elixir linenums="1"
first
%{age: "30ish", gender: "Female", name: "Izzy"}
second
%{age: "30ish", gender: "Male", name: "The Author"}
third
%{age: "56", gender: "Male", name: "Roberto"}
others
[%{age: "38", gender: "Female", name: "Juliet"}, ...]
```

"Apakah ini berarti saya bisa melakukan hal yang sama untuk daftar `others` untuk mendapatkan 3 orang berikutnya?" tanya Izzy. Ya, itu berarti kamu bisa melakukannya:

```elixir linenums="1"
[first, second, third | remainder] = others
[%{age: "38", gender: "Female", name: "Juliet"}, ...]
```

Sekarang ketika kita memeriksa nilai `first`, `second`, dan `third`, mereka akan menjadi nama 3 orang berikutnya dalam daftar:

```elixir linenums="1"
first
%{age: "38", gender: "Female", name: "Juliet"},
second
%{age: "21", gender: "Female", name: "Mary"},
third
%{age: "67", gender: "Female", name: "Bobalina"},
```

Dan variabel `remainder` kita akan menjadi nama-nama yang tersisa dalam daftar, yaitu dua Charlie:

```elixir linenums="1"
remainder
[
  %{age: "54", gender: "Male", name: "Charlie"},
  %{age: "10", gender: "Male", name: "Charlie (no relation)"},
]
```

Jika kita sekarang mencoba menarik 3 orang berikutnya dalam daftar, Elixir tidak akan bisa melakukan itu karena hanya ada dua nama tersisa dalam daftar `remainder`. Saya telah mempersingkat output dalam contoh di bawah, tetapi saya rasa kamu akan mengerti maksudnya:

```elixir linenums="1"
[first, second, third | those_still_remaining] = remainder
** (MatchError) no match of right hand side value: ... ⏎  
   [%{name: "Charlie"}, %{name: "Charlie (no relation)"}]  
```

Selalu merupakan ide yang baik untuk berhati-hati di sini dengan pattern matching daftar dengan jumlah item yang diharapkan yang benar untuk menghindari MatchErrors seperti ini. Biasanya ketika kita akan bekerja melalui setiap item dalam daftar, kita akan melakukannya bukan dalam kelompok tiga, tetapi satu per satu.

Kita akan melihat dua contoh cara bekerja melalui setiap item dalam daftar satu per satu, sekali di Bab 9 dan sekali di Bab 10. Kita perlu membangun untuk itu, jadi mari kita tidak terlalu khawatir tentang itu untuk saat ini.

Itu sudah cukup tentang daftar untuk saat ini. Kita akan mengunjungi kembali pattern matching di dalamnya sedikit kemudian dalam materi ini. Mari kita lihat bagaimana kita dapat bekerja dengan peta.

##### Pattern Matching with Maps

Mari kita katakan bahwa kita memiliki sebuah peta (map) yang berisi informasi tentang seseorang:

```elixir linenums="1"
person = %{name: "Izzy", age: "30ish"}
%{name: "Izzy", age: "30ish"}
```

Kita sudah melihat sebelumnya bahwa kita dapat mengambil nilai yang terhubung dengan `name:` atau `age:` sesuka hati dengan menggunakan sintaks ini:

```elixir linenums="1"
person.name
"Izzy"
person.age
"30ish"
```

Tetapi bagaimana jika kita ingin mengambil kedua nilai ini sekaligus? Atau bahkan dalam kode yang paling singkat? Nah, untuk itu kita memiliki fitur **pattern matching** yang telah saya bicarakan selama lebih dari satu halaman ini. Mari kita lihat bagaimana pattern matching dapat membantu mengambil baik nama maupun usia dari peta `person`.

```elixir linenums="1"
%{name: name, age: age} = person
```

"Hai, apa yang terjadi di sini? Sisi kiri di sini jelas tidak sama dengan sisi kanan!", teriak Izzy. Ya, kamu benar sekali. Di sisi kanan di sini kita memiliki sebuah peta yang memiliki kunci "name" yang menunjuk pada nilai "Izzy", tetapi di sisi kiri kunci "name" itu menunjuk pada nilai `name`. Ini adalah trik dari pattern matching: sisi kiri dapat digunakan untuk menetapkan beberapa variabel; tidak harus cocok persis dengan sisi kanan.

Jika kita memeriksa nilai dari `name` dan `age` di sini, kita akan melihat bahwa nilai-nilai tersebut adalah nilai dari peta kita.

```elixir linenums="1"
name
"Izzy"
age
"30ish"
```

Nah, lihat itu! Kita bisa mengambil dua nilai ini sekaligus. Kerumunan bersorak seolah-olah kita baru saja melakukan trik sulap. Tunggu sampai kamu melihat trik kita berikutnya!

Mari kita lihat contoh sebelumnya, di mana kita memiliki peta di dalam daftar:

```elixir linenums="1"
those_who_are_assembled = [
  %{age: "30ish", gender: "Female", name: "Izzy"},
  %{gender: "Male", name: "The Author", age: "30ish"},
  %{name: "The Reader", gender: "Unknowable", age: "Unknowable"},
]
```

Misalkan kita ingin mendapatkan nama orang pertama dari daftar ini. Kita dapat menggabungkan pattern matching pada daftar dan peta bersama-sama:

```elixir linenums="1"
[first_person = %{name: first_name} | others] = those_who_are_assembled
```

Di sini kita mencocokkan item pertama dari daftar, dan menempatkan sisanya dalam variabel `others`. Kita mengambil hanya orang pertama dari daftar mereka yang berkumpul. Di dalam kecocokan itu, kita menetapkan orang pertama tersebut ke `first_person`. Kita kemudian mengharapkan bahwa item pertama dari daftar ini cocok dengan pola `%{name: first_name}`. Ini akan menetapkan variabel `first_name` menjadi nilai dari kunci `name` pada item pertama. Phew, itu adalah deskripsi yang panjang. Mari kita lihat apa yang sekarang kita miliki di konsol:

```elixir linenums="1"
first_person
%{age: "30ish", gender: "Female", name: "Izzy"}
first_name
"Izzy"
```

Ini bisa jadi sulit untuk dipahami pada awalnya karena banyak yang terjadi di sini. Mungkin perlu beberapa kali untuk membacanya dan memahaminya. Itu juga yang saya alami ketika pertama kali membaca contoh seperti ini! Luangkan waktu kamu, tidak apa-apa jika tidak memahaminya pada percobaan pertama.

Apa yang kita lakukan di sini adalah mengambil 3 nilai berbeda dari satu baris kode ini:

![Complex pattern matching within a list](https://joyofelixir.com/images/6/complex-matching.png)

Variabel `first_person`, yang berisi semua informasi yang kita miliki tentang Izzy dalam bentuk peta.  
Variabel `first_name`, yang telah menyimpan string "Izzy".  
Variabel `others`, yang menyimpan orang-orang yang tersisa dalam daftar.

Seperti yang dapat kamu lihat dari contoh singkat ini, pattern matching sangat fleksibel dan memungkinkan kamu untuk mencocokkan lebih dari satu hal sekaligus, serta memungkinkan kamu untuk menetapkan lebih dari satu variabel. Para programmer sering menyebut hal ini sebagai **destructuring**: kamu melihat ke dalam struktur data dan kemudian mengambil hanya hal-hal yang kamu inginkan.

Pattern matching dapat digunakan untuk lebih banyak hal daripada hanya memilih kunci dari peta atau item dari daftar. Kita juga dapat menggunakannya di dalam fungsi!

##### Pattern matching inside functions
Kita dapat menggunakan pola pencocokan di dalam fungsi kita agar berfungsi berbeda tergantung pada argumen yang diberikan. Misalnya, kita bisa mendefinisikan sebuah fungsi yang mengambil jenis jalan yang kita pilih; baik jalan "tinggi" atau jalan "rendah", dan membuatnya merespons secara berbeda tergantung pada mana yang diberikan.

```elixir linenums="1"
road = fn
  "high" -> "You take the high road!"
  "low" -> "I'll take the low road! (and I'll get there before you)"
end
```

Ketika kita memanggil fungsi ini dengan argumen "tinggi", argumen tersebut akan cocok dengan baris fungsi pertama di sini, dan "You take the high road" akan dikembalikan. Demikian juga, ketika kita memberikannya "rendah", itu akan mengembalikan "I'll take the low road! (and I'll get there before you)". Setiap baris di dalam fungsi ini disebut sebagai klausa. Kita bisa terus membicarakan teori di balik ini, atau kita bisa mencobanya langsung di prompt iex kita:

```elixir linenums="1"
road.("high")
"You take the high road!"
road.("low")
"I'll take the low road! (and I'll get there before you)"
```

Ini bekerja karena bagaimana kita mendefinisikan fungsi jalan tersebut. Dalam fungsi itu, kita telah mendefinisikan dua klausa fungsi terpisah. Klausa fungsi pertama mengatakan bahwa ketika argumennya "tinggi", maka fungsi harus mengeluarkan baris tentang "jalan tinggi". Klausa fungsi kedua mengatakan bahwa ketika kita menyediakan argumen "rendah", maka harus mengeluarkan baris tentang "jalan rendah".

Anggap saja seperti ini: Elixir sedang mencocokkan nilai argumen dengan klausa fungsi. Jika Elixir dapat melihat bahwa argumen tersebut sama dengan "tinggi", maka akan menggunakan fungsi pertama. Jika tidak sama dengan "tinggi", maka Elixir akan mencoba mencocokkan dengan "rendah". Jika argumennya adalah "rendah", maka klausa kedua akan digunakan.

Tapi apa yang terjadi jika itu bukan keduanya? Kita bisa mengetahuinya dengan sedikit percobaan di prompt iex kita:

```elixir linenums="1"
road.("middle")
** (FunctionClauseError) no function clause matching in :erl_eval."-inside-an-interpreted-fun-"/1

    The following arguments were given to :erl_eval."-inside-an-interpreted-fun-"/1:

        # 1
        "middle"
```

Elixir di sini menunjukkan kepada kita sebuah kesalahan yang belum pernah kita lihat sebelumnya: FunctionClauseError. Kesalahan ini terjadi ketika kita memanggil sebuah fungsi memberikannya argumen yang tidak diharapkan. Dalam kasus fungsi jalan kita, ini mengharapkan baik "tinggi" atau "rendah", tetapi kita memberikannya "tengah". Kedua klausa fungsi tidak mencocokkan nilai "tengah", dan sehingga kita melihat kesalahan ini. Untuk lebih membantu, Elixir menunjukkan argumen yang kita berikan di sini.

Mencocokkan pada string dalam fungsi itu hebat, tetapi seperti yang kita lihat sebelumnya dengan tanda sama dengan (=), kita dapat mencocokkan lebih dari sekadar string.

##### Matching maps inside functions
Kita juga dapat mencocokkan kunci yang terdapat dalam sebuah peta dan mendapatkan kode untuk berfungsi berbeda tergantung pada kunci apa yang ada. Mari kita ambil fungsi sapaan kita dari Bab 5 dan mengubahnya sedikit sehingga berfungsi berbeda tergantung pada jenis peta yang kita berikan:

```elixir linenums="1"
greeting = fn
  %{name: name} -> "Hello, #{name}!"
  %{} -> "Hello, Anonymous Stranger!"
end
```

"Oh itu keren! Apa yang terjadi jika peta kosong?", tanya Izzy. Segera, Izzy. Segera. Mari kita lihat apa yang terjadi jika kita memanggil fungsi sapaan ini dengan peta yang memiliki kunci "name":

```elixir linenums="1"
greeting.(%{name: "Izzy"})
"Hello, Izzy!"
```

Di sini, klausa fungsi pertama mencocokkan karena peta yang kita berikan berisi kunci yang "name", dan itu juga yang diharapkan oleh klausa fungsi pertama (ditandai di bawah dalam hijau): sebuah peta yang memiliki kunci bernama "name". Jadi ketika kita memanggil fungsi ini dengan peta ini dengan kunci "name", kita melihat string "Hello, Izzy!" dikeluarkan dari fungsi.

```elixir linenums="1"
greeting = fn
  %{name: name} -> "Hello, #{name}!"
  %{} -> "Hello, Anonymous Stranger!"
end
```

Sekarang mari kita lihat apa yang terjadi jika kita memanggil fungsi ini dengan peta kosong:

```elixir linenums="1"
greeting.(%{})
"Hello, Anonymous Stranger!"
```

Elixir masih berfungsi seperti yang kita harapkan: kita menyediakan peta kosong dan klausa fungsi kedua mencocokkan peta kosong, dan jadi itulah klausa yang akan digunakan di sini.

```elixir linenums="1"
greeting = fn
  %{name: name} -> "Hello, #{name}!"
  %{} -> "Hello, Anonymous Stranger!"
end
```

Oke, jadi apa yang Anda harapkan terjadi di sini jika Anda tidak menyediakan peta dengan kunci "name" atau peta kosong, tetapi peta dengan kunci berbeda di dalamnya? "Berdasarkan tes string, saya berharap itu gagal dengan FunctionClauseError!", kata Izzy dengan bangga. Sepertinya seseorang telah memperhatikan. Sayang Izzy, itu juga yang saya harapkan terjadi ketika saya belajar Elixir. Namun, peta dicocokkan dengan cara yang berbeda dengan string di Elixir. Mari kita lihat:

```elixir linenums="1"
greeting.(%{age: "30ish"})
"Hello, Anonymous Stranger!"
```

Fungsi sapaan tetap menampilkan "Hello, Anonymous Stranger!" Jadi apa yang terjadi di sini?

Nah, di Elixir ketika Anda mencocokkan dua peta bersama, itu akan selalu mencocokkan pada subset peta. Mari kita lihat menggunakan tanda sama dengan (=) kita yang terpercaya lagi:

```elixir linenums="1"
%{} = %{name: "Izzy"}
%{"name" => "Izzy"}
```

Sama seperti dalam klausa kedua dari fungsi di atas, kita membandingkan peta kosong di sisi kiri dengan peta dari sisi kanan. Ketika mencocokkan pola peta seperti ini, sangat berguna untuk berpikir bahwa sisi kiri menunjukkan kunci yang benar-benar diperlukan agar pencocokan berhasil. Sisi kanan harus berisi kunci yang sama seperti sisi kiri, tetapi sisi kanan dapat berisi lebih banyak kunci daripada yang ada di sisi kiri.

Pencocokan ini akan berhasil karena tidak ada kunci yang diperlukan oleh sisi kiri dari pencocokan ini. Cerita ini berbeda jika kita memiliki peta di sisi kiri dengan kunci, seperti yang telah kita lihat sebelumnya dengan klausa pertama dari fungsi sapaan kita:

```elixir linenums="1"
greeting = fn
  %{name: name} -> "Hello, #{name}!"
  %{} -> "Hello, Anonymous Stranger!"
end
```

Dalam kasus klausa pertama, itu hanya akan mencocokkan jika argumen yang diberikan kepada fungsi sapaan adalah peta yang berisi kunci "name"; kunci ini diperlukan untuk pencocokan. Jika peta tidak berisi kunci "name", maka klausa ini tidak akan mencocokkan. Klausa kedua mencocokkan peta mana pun, dan jadi itulah klausa yang akan digunakan untuk peta mana pun yang tidak mengandung kunci "name".

##### Matching anything
Sekarang satu hal lagi yang ingin saya tunjukkan adalah bagaimana menghindari FunctionClauseErrors yang menyebalkan ketika semua klausa fungsi di dalam sebuah fungsi tidak cocok. Mari kita lihat lagi fungsi jalan:

```elixir linenums="1"
road = fn
  "high" -> "You take the high road!"
  "low" -> "I'll take the low road! (and I'll get there before you)"
end
```

Jika argumen yang diberikan kepada fungsi ini bukan "high" atau "low", maka Elixir akan menunjukkan kepada kita sebuah FunctionClauseError:

```elixir linenums="1"
road.("middle")
** (FunctionClauseError) no function clause matching in ⏎
:erl_eval."-inside-an-interpreted-fun-"/1
```

Bagaimana jika alih-alih kesalahan ini kita bisa membuat fungsi untuk memberi tahu siapa pun yang menjalankannya bahwa mereka harus memberikan "high" atau "low" sebagai argumen? Elixir memungkinkan kita untuk melakukan ini dengan menggunakan garis bawah (_) sebagai argumen di klausa fungsi baru:

```elixir linenums="1"
road = fn
  "high" -> "You take the high road!"
  "low" -> "I'll take the low road! (and I'll get there before you)"
  _ -> "Take the 'high' road or the 'low' road, thanks!"
end
```

Garis bawah (_) ini mencocokkan apa pun dan sering digunakan dalam kasus seperti ini di mana kita ingin menunjukkan pesan jika tidak ada klausa fungsi lain yang cocok. Mari kita lihat ini dalam tindakan:

```elixir linenums="1"
road.("middle")
"Take the 'high' road or the 'low' road, thanks!"
```

Garis bawah ini tidak hanya mencocokkan string, tetapi juga akan mencocokkan argumen lain yang bisa kita berikan kepada fungsi:

```elixir linenums="1"
road.(%{})
"Take the 'high' road or the 'low' road, thanks!"
road.(["high", "low"])
"Take the 'high' road or the 'low' road, thanks!"
```

Apa yang dilakukan ini adalah melewatkan dua klausa pertama dari fungsi, dan jadi klausa ketiga yang akan digunakan sebagai gantinya:

```elixir linenums="1"
road = fn
  "high" -> "You take the high road!"
  "low" -> "I'll take the low road! (and I'll get there before you)"
  _ -> "Take the 'high' road or the 'low' road, thanks!"
end
```

Ini membantu menjaga agar orang tetap dalam jalur ketika memberikan argumen yang tepat kepada fungsi, tanpa Elixir meledak di wajah mereka ketika mereka memberikan argumen yang salah.

##### Latihan
Buatlah sebuah fungsi yang menerima peta yang berisi "name" dan "age", atau hanya peta yang berisi "name". Ubah output tergantung pada apakah "age" ada. Apa yang terjadi jika Anda membalik urutan klausa fungsi? Apa yang bisa Anda pelajari dari ini?

---

#### 7. Part 2: Recap

Elixir akan cukup sulit jika Anda harus menulis semua kode untuk program Anda sendiri. Kita sudah melihat bahwa jika Anda ingin menambah, mengurang, mengalikan, atau membagi angka, Elixir sudah mendukungnya:

```elixir linenums="1"
iex> 2 + 4
6
iex> 3 - 6
-3
iex> 4 * 12345
49380
iex> 1234 / 4
308.5
```

Kita juga melihat bahwa Elixir dapat menjalankan kode di dalam kode lain, melalui interpolasi string:

```elixir linenums="1"
iex> place = "World"
iex> "Hello #{place}!"
"Hello, World!"
```

Kita melihat bahwa Elixir dapat menangani daftar:

```elixir linenums="1"
iex> ["chicken", "beef", "and so on"]
["chicken", "beef", "and so on"]
```

Dan juga dapat menangani peta:

```elixir linenums="1"
iex> person = %{name: "Izzy", age: "30ish", gender: "Female"}
```

Kita juga melihat bahwa Elixir bisa mengingat fungsi untuk kita:

```elixir linenums="1"
iex> greeting = fn (name) -> "Hello, #{name}!" end
#Function<6.52032458/1 in :erl_eval.expr/5>
```

Dan di bab terakhir, kita melihat bahwa kita bisa melakukan pattern matching:

```elixir linenums="1"
iex> %{name: name, age: age} = %{name: "Izzy", age: "30ish"}
%{name: "Izzy", age: "30ish"}
iex> name
"Izzy"
iex> age
"30ish"
```

Tapi bagaimana jika saya memberi tahu Anda bahwa Elixir dapat melakukan lebih dari sekadar matematika sederhana, interpolasi string, mengingat fungsi, dan pattern matching? Bagaimana jika saya memberi tahu Anda bahwa Elixir sudah menyediakan beberapa fungsi yang menggunakan semua hal di atas untuk membantu Anda membangun program, asalkan Anda hanya perlu memintanya untuk menggunakannya?

Nah, yang perlu Anda lakukan hanyalah meminta, dan Elixir akan menyediakan.

---

## Part Three: Building on the foundations
#### 8. Working with strings, input and output

Dalam bab ini, kita akan membahas beberapa fungsi bawaan yang dimiliki Elixir. Kita akan fokus khususnya pada string, input, dan output. Elixir memiliki beberapa fungsi yang sangat berguna yang sudah tersedia, dan kita akan melihat sedikit contohnya di sini.

##### Working with strings

Kita akan mulai dengan melihat fungsi-fungsi untuk bekerja dengan string. String adalah tempat kita mulai di Bab 1, jadi masuk akal untuk memulai dengan mereka di sini juga.

###### Reversing string

Pernahkah Anda ingin membalik sebuah kalimat, tetapi tidak ingin mengetik semua karakter yang berbeda secara manual? Elixir memiliki fungsi yang berguna untuk ini yang disebut `String.reverse`. Berikut cara kerjanya:

```elixir linenums="1"
iex> String.reverse("reverse this")
"siht esrever"
```

##### Lihat Mah, Tanpa Tanda Kurung!

Saat kita memanggil fungsi di Elixir, kita biasanya membungkus argumen dengan tanda kurung. Kita melakukan ini untuk membuatnya sangat jelas di mana akhir dari fungsi tersebut.

Namun, Anda mungkin juga melihat kode seperti ini, tanpa tanda kurung:

```elixir linenums="1"
iex> String.reverse "reverse this"
```

Elixir cukup pintar untuk mengetahui bahwa "reverse this" adalah argumen untuk fungsi `String.reverse`. Namun, secara umum, praktik terbaik yang diterima adalah selalu menggunakan tanda kurung.

Izzy memberikan respons "wooooowww, keren sekali" yang terlihat jelas terhadap hal ini. "Apa lagi yang dimiliki Elixir?" tanyanya dengan cepat. Kita akan sampai ke sana, Izzy. Mari kita pahami dulu apa yang terjadi di sini.

Fungsi-fungsi yang disediakan oleh Elixir dipisahkan ke dalam sesuatu yang mirip dengan laci dapur atau kotak peralatan, yang disebut modul. Di mana di laci dapur Anda mungkin memiliki garpu, pisau, sendok, dan spork (seperti dapur setiap orang yang masuk akal), dan di laci lain Anda mungkin memiliki cangkir pengukur, dan di laci lain handuk teh, di Elixir, fungsi untuk bekerja dengan jenis data yang berbeda dipisahkan ke modul yang berbeda. Ini membuat mencari fungsi untuk bekerja dengan jenis data tertentu di Elixir menjadi sangat mudah.

Di sini, kita menggunakan fungsi `reverse` dari modul `String` ("laci" / "kotak peralatan"). Kita tahu bahwa ini adalah modul karena huruf pertamanya adalah huruf besar. Kita mengoper fungsi `String.reverse` satu argumen, yaitu string "reverse this". Fungsi ini mengambil string dan membaliknya, menghasilkan string yang terbalik: "siht esrever".

Perhatikan di sini bahwa kita tidak perlu meletakkan titik antara nama fungsi dan argumennya, seperti yang kita lakukan dengan fungsi yang kita definisikan sendiri. Anda tidak perlu melakukan ini saat menjalankan fungsi dari modul. Anda hanya perlu titik jika Anda telah mendefinisikan fungsi dan menetapkannya ke variabel. Misalnya, dengan fungsi `greeting` kita sebelumnya:

```elixir linenums="1"
iex> greeting = fn (place) -> "Hello, #{place}!" end
#Function<6.52032458/1 in :erl_eval.expr/5>
iex> greeting.("world")
```

Saat memanggil fungsi `String.reverse`, Elixir tahu bahwa itu adalah fungsi karena awalan `String.`. Kita tidak perlu titik tepat setelah nama fungsi:

```elixir linenums="1"
iex> String.reverse("reverse this")
"siht esrever"
```

###### Splitting a string

Bagaimana jika kita ingin membagi sebuah string ke dalam kata-kata individual? Untuk itu, kita bisa menggunakan fungsi `String.split`:

```elixir linenums="1"
iex> String.split("split my string into pieces")
["split", "my", "string", "into", "pieces"]
```

Sekarang kita memiliki daftar kata-kata di dalam string. Kita akan melihat apa yang bisa kita lakukan dengan daftar seperti itu di bab berikutnya. Untuk sekarang, mari kita lihat apa lagi yang ada di modul `String`.

###### Mengganti bagian dari string

Bagaimana jika kita ingin mengganti semua kemunculan huruf tertentu dalam sebuah string dengan huruf lain? Untuk itu, Elixir memiliki fungsi `String.replace`:

```elixir linenums="1"
iex> String.replace("moo", "o", "e")
"mee"
```

Fungsi ini mengambil tiga argumen:
1. String yang ingin kita modifikasi
2. Bagian dari string yang ingin kita ubah
3. Apa yang ingin kita ubah menjadi

Cara kita menggunakan fungsi di sini berarti bahwa itu akan mengubah semua huruf "o" dalam string menjadi "e".

Perlu dicatat bahwa kita bisa mengubah lebih dari satu karakter pada satu waktu juga:

```elixir linenums="1"
iex> String.replace("the cow jumped over the moon", "oo", "ee")
"the cow jumped over the meen"
```

Perhatikan di sini bahwa itu tidak mengubah huruf "o" dalam kata "cow" atau huruf "o" lain dalam kata "over". Ini karena kita memberi tahu fungsi untuk mencari dua huruf "o" berturut-turut.

###### Membuat semua huruf dalam string menjadi huruf besar

Bagaimana jika kita ingin membuat komputer mengubah sebuah string menjadi variannya yang berteriak? Kita bisa menggunakan `upcase` untuk ini:

```elixir linenums="1"
iex> String.upcase("not so quiet any more")
"NOT SO QUIET ANY MORE"
```

###### Membuat semua huruf dalam string menjadi huruf kecil

Di sisi spektrum yang berlawanan, ada `downcase`:

```elixir
iex> String.downcase("LOUD TO QUIET")
"loud to quiet"
```

Jadi seperti yang Anda lihat, modul `String` memiliki beberapa fungsi yang berguna yang dapat membantu kita kapan saja kita perlu membagi string, mengubah semuanya menjadi huruf besar / kecil. Masih banyak fungsi lainnya di modul `String`, dan kita akan melihat beberapa di antaranya nanti.

##### Input and output

Input dan output adalah dua hal mendasar yang akan Anda kerjakan saat pemrograman. Pemrograman pada dasarnya tentang mengambil beberapa data sebagai input dan mengubahnya menjadi semacam output. Kita sudah melihat ini berkali-kali dengan fungsi-fungsi yang kita definisikan dan gunakan sepanjang site ini. Misalnya, dalam fungsi `String.downcase` yang disebutkan di atas, string "LOUD TO QUIET" adalah input, dan "loud to quiet" yang dihasilkan oleh metode tersebut adalah output.

Apa yang akan kita bahas di bagian ini adalah mendapatkan input dari sumber yang berbeda: sebuah prompt baru. Kita akan meminta pengguna untuk nama mereka, dan kemudian kita akan menggunakan apapun yang mereka masukkan untuk mengeluarkan pesan yang berisi input tersebut.

###### Making our own prompts

Misalkan kita ingin meminta orang untuk nama mereka dan kita ingin melakukannya dengan cara yang tidak mengharuskan mereka membaca Joy of Elixir untuk memahami bahwa string harus dibungkus dalam tanda kutip ganda dan mereka harus memasukkan input mereka ke dalam prompt `iex`.

Untungnya, Elixir memiliki sebuah modul yang menyediakan fungsi untuk melakukan hal ini. Modul tersebut disebut IO (Input / Output) dan fungsinya disebut `gets`. Nama `gets` berarti "get string" dan akan memungkinkan kita melakukan hal itu. Mari kita lihat fungsi ini dalam praktik:

```elixir linenums="1"
iex> name = IO.gets "What is your name?"
What is your name?
```

"Izzy bertanya, "Apa yang terjadi dengan prompt iex> kita?" Pertanyaan bagus! Kita sedang menggunakan `gets` dan memberikannya sebuah string. String ini kemudian menjadi prompt baru. Prompt ini meminta nama kita. Mari kita masukkan nama kita dan tekan enter:

```elixir linenums="1"
iex> name = IO.gets "What is your name?"
What is your name?The Reader
"The Reader\n"
```

Ok, jadi ada output di sini. Tapi apa artinya? Jika kita memeriksa isi variabel `name`, kita akan melihat bahwa variabel itu berisi string "The Reader\n".

```elixir linenums="1"
iex> name
"The Reader\n"
```

Izzy melanjutkan pertanyaan hebatnya: "Apa itu \n di akhir?". Itu adalah karakter baris baru dan memberi tahu komputer bahwa kita telah menekan enter. Meskipun fungsi `IO.gets` berhenti meminta setelah kita menekan enter, fungsi ini tetap menyimpan enter jika kita menginginkannya. Dalam kasus ini, kita sebenarnya tidak menginginkan karakter tersebut. Kita bisa menghilangkannya dengan menggunakan fungsi lain dari modul `String`, yang disebut `trim`.

```elixir linenums="1"
iex> name = String.trim(name)
"The Reader"
```

Itu jauh lebih baik! Sekarang kita memiliki nama kita tanpa karakter baris baru yang mengganggu. Apa yang dilakukan `String.trim` adalah menghilangkan semua spasi ekstra dari akhir string, memberi kita hanya bagian-bagian pentingnya.

##### Taking input and making it output

Kita sekarang telah mendapatkan input, tapi apa gunanya mengambil input jika kita tidak melakukan apa-apa dengannya? Jadi mari kita lakukan sesuatu dengannya! Apa yang akan kita lakukan dengan input ini adalah mengeluarkan pesan sapaan.

Mari kita sedikit menyimpang dari penggunaan prompt `iex` dan sebagai gantinya menulis kode kita di salah satu file Elixir Script (.exs) yang kita sebutkan di akhir Bab 5. Mari kita beri nama file ini `greet.exs` dan masukkan konten ini di dalamnya:

```elixir linenums="1"
name = IO.gets "What is your name? "
age = IO.gets "And what is your age? "
IO.puts "Hello, #{String.trim(name)}! You're #{String.trim(age)}? That's so old!"
```

Well, itu agak licik dari `IO.puts` untuk muncul begitu saja dari mana-mana! Sama seperti `gets` berarti "get string", `puts` berarti "put string". Fungsi ini akan menghasilkan output saat script kita dijalankan. Jika kita tidak memiliki `IO.puts` di sini, program kita hanya akan mengambil input, dan tidak akan menghasilkan output.

Dalam fungsi ini kita menginterpolasi output dari fungsi `String.trim` dua kali. Ingat: kita melakukan ini untuk menghapus karakter baris baru (`\n`) dari hasil panggilan `IO.gets`.

Ada beberapa sintaks baru yang belum pernah kita lihat sebelumnya. Kita sudah melihat bahwa kita bisa menginterpolasi variabel ke dalam string, tapi kita belum pernah melihat bahwa kita juga bisa memanggil fungsi saat menginterpolasi. Ini sepenuhnya bisa dilakukan di Elixir. Saat menginterpolasi di dalam string, Anda bisa memasukkan kode apapun ke dalam tanda kurung interpolasi (`#{}`) — tetapi sebagai aturan praktis, sebaiknya jaga agar kode yang diinterpolasi tetap pendek dan sederhana. Biasanya, Anda hanya akan menginterpolasi variabel. Di sini, kita membuat pengecualian kecil untuk menginterpolasi sebuah fungsi.

Mari kita jalankan script `greet.exs` kita sekarang. Pertama, kita harus menghentikan prompt `iex` kita, yang bisa kita lakukan dengan menekan Ctrl+C dua kali. Kemudian kita bisa menjalankan script dengan perintah ini:

```bash
elixir greet.exs
```

Berikut adalah yang akan kita lihat awalnya:

```bash
What is your name?
```

Script ini meminta kita untuk nama kita, dan hal itu terjadi karena baris pertama kode dalam script tersebut menjalankan fungsi `IO.gets`. Mari kita masukkan nama kita lagi dan tekan enter.

```bash
What is your name? Reader
And what is your age?
```

Script kecil ini sekarang meminta kita untuk usia kita. Ini terjadi karena baris kedua memanggil `IO.gets` lainnya. Mari kita masukkan usia kita dan kemudian tekan enter lagi.

```bash
What is your name? Reader
And what is your age? 30ish
Hello, Reader! You're 30ish? That's so old!
```

Script kita mencapai baris ketiga dan terakhir, di mana ia menjalankan fungsi `IO.puts` dan menghasilkan pesan bercandanya. Ternyata menjadi 30-an itu tua! Anak-anak zaman sekarang tidak punya rasa hormat.

Ini hanyalah contoh kecil dari apa yang bisa kita lakukan dengan `IO.gets` dan `IO.puts`. Kita bisa menggunakan sejumlah panggilan fungsi `IO.gets` dan `IO.puts` untuk membangun sebuah program yang mengambil input pengguna dan menghasilkan output darinya.

##### The unchanging world

Sekarang adalah waktu yang tepat untuk memperkenalkan Anda pada fitur lain dari Elixir, yang disebut immutability (ketidakberubahan). **Immutability** adalah salah satu dari kata-kata besar dalam ilmu komputer yang digunakan untuk menggambarkan hal-hal yang tidak berubah seiring waktu. "Tidak berubah seiring waktu" jauh lebih masuk akal bagi saya daripada "immutability" ketika pertama kali saya mendengar kata itu, jujur saja.

Kita membahas ini di bab ini karena hampir semua hal yang Anda kerjakan sejauh ini di Elixir bersifat immutable; tidak berubah dan tidak bisa diubah. Sebagian besar hal di Elixir tidak dapat diubah, dimodifikasi, diotak-atik, atau istilah lain untuk itu, dan cara kita menyebut atribut khusus ini adalah dengan mengatakan bahwa hal-hal ini bersifat **immutable**.

Ketika kita memanggil fungsi seperti `String.downcase` atau `String.upcase`, kita memberikan string kepada fungsi-fungsi ini sebagai argumen, lalu kita mendapatkan kembali string lain dari fungsi tersebut; dua string yang sepenuhnya berbeda. Semua fungsi di Elixir berperilaku seperti ini: mereka tidak dapat mengubah apa yang diberikan kepada mereka. Mari kita lihat contoh singkat:

```elixir linenums="1"
iex> sentence = "perfectly normal sentence"
"perfectly normal sentence"
iex> upcased_sentence = String.upcase(sentence)
"PERFECTLY NORMAL SENTENCE"
iex> sentence
"perfectly normal sentence"
```

Dengan menjalankan `String.upcase` pada `sentence`, itu tidak mengubah apa yang ada di dalam `sentence` — `sentence` tetap persis seperti yang kita definisikan. Data yang disimpan dalam variabel `sentence` bersifat immutable. Satu-satunya cara kita dapat mengubah apa yang ada dalam variabel itu adalah jika kita menetapkan ulang variabel tersebut:

```elixir linenums="1"
iex> sentence = "another, even more perfectly normal sentence"
"another, even more perfectly normal sentence"
```

Penting untuk diketahui di Elixir bahwa memanggil fungsi pada data tidak akan pernah mengubah data tersebut. Sebaliknya, kita akan mendapatkan sesuatu yang baru sebagai hasil dari fungsi itu. Ini akan menjadi lebih jelas semakin banyak kode Elixir yang Anda tulis, tetapi saya pikir sebaiknya menyebutkannya di sini sebelum Anda terlalu jauh dan seseorang menyebutkan kata besar itu — "immutable". Sekarang Anda, seperti yang mereka katakan, sudah "tahu juga."

##### Exercises

- Buat program yang menghasilkan cerita sangat pendek. Gunakan `IO.gets/1` untuk mengambil input berupa nama orang, tempat, dan objek — lalu gabungkan ketiganya menjadi sebuah kalimat kecil, outputkan menggunakan `IO.puts/1`.
- Pikirkan tentang apa yang terjadi ketika Anda menghapus `IO.puts` dari awal Baris 3 dalam `greet.exs` dan kemudian jalankan program dengan perintah `elixir greet.exs`. Pikirkan bagaimana ini akan berbeda jika Anda memasukkan kode itu ke dalam prompt `iex`.
- Kita telah banyak bekerja dengan string sejauh ini di bab ini. Mari kita lihat lagi list dan map di bab berikutnya dan fungsi bawaan yang bisa kita gunakan dengannya.

---

#### 9. Working with lists

Pada ini, kita akan membahas beberapa fungsi yang telah disediakan Elixir secara bawaan untuk membantu kita bekerja dengan list.

Sama seperti ada modul String untuk bekerja dengan string, ada juga modul List untuk bekerja dengan list. Modul ini mencakup fungsi seperti first yang akan memberi tahu Anda item pertama dalam list:

```elixir linenums="1"
List.first([1, 2, 3, 4])
1  
```
Dan juga memungkinkan Anda mengetahui item terakhir:

```elixir linenums="1"
List.last([1, 2, 3, 4])
4  
```
Kita sudah melihat sebelumnya bagaimana kita bisa membalikkan sebuah string, tetapi bagaimana jika kita ingin membalikkan sesuatu yang lain, seperti list ini?

```elixir linenums="1"
iex> animals_or_derivatives_of_animals = ["cat", "dog", "cow", "turducken"]
```
Kita mungkin berpikir bahwa sama seperti first dan last, pasti ada fungsi reverse juga! Kita bisa berpikir demikian karena Elixir menyediakan cara untuk membalikkan string — dengan `String.reverse("string")` — jadi kenapa tidak untuk list juga? Mari kita coba:

```elixir linenums="1"
iex> List.reverse(animals_or_derivatives_of_animals)
List.reverse(animals_or_derivatives_of_animals)
** (UndefinedFunctionError) function List.reverse/1 is undefined or private  
    (elixir) List.reverse(["cat", "dog", "cow", "turducken"])  
```
Uh oh, ada teks merah lagi. Sepertinya fungsi ini tidak ada, meskipun kita mengira itu ada. Kita tidak memiliki kekuatan super untuk menghadirkan fungsi-fungsi ke dunia saat ini, jadi kita harus menyelidiki untuk mencari tahu mengapa fungsi itu hilang.

Komputer memberi tahu kita bahwa Elixir tidak mengetahui fungsi yang disebut `List.reverse`, atau fungsi tersebut "privat". Komputer (dengan licik) tidak akan告 kita mana yang tidak ada atau privat, tetapi kita akan mengasumsikan kasus pertama di sini: bahwa fungsi itu tidak terdefinisi. (Kita akan kembali ke fungsi privat sedikit lebih lanjut di site ini.)

##### Izzy bertanya: "Hei, apa itu /1 setelah fungsi?"  
Senang Anda bertanya! Itu menunjukkan arity dari fungsi tersebut. Kita melihat kata arity di Bab 5, dan untuk menyegarkan ingatan Anda, arity adalah cara lain untuk mengatakan "jumlah argumen".

Fungsi Elixir tidak hanya dapat berbeda berdasarkan nama, tetapi juga berdasarkan jumlah argumen yang diterima fungsi tersebut. Pesan kesalahan ini memberi tahu kita bahwa kita mencoba memanggil fungsi `List.reverse/1`. Itu menunjukkan /1 di akhir karena kita hanya mengirim satu argumen. Jika kita mengirim dua argumen alih-alih satu, maka akan memberi tahu kita bahwa kita mencoba memanggil fungsi `List.reverse/2`.

```elixir linenums="1"
iex> List.reverse(animals_or_derivatives_of_animals, [1, 2, 3])
List.reverse(animals_or_derivatives_of_animals, [1, 2, 3])
** (UndefinedFunctionError) function List.reverse/2 is undefined or private  
    (elixir) List.reverse(["cat", "dog", "cow", "turducken"], [1, 2, 3])  
```
Contoh yang baik dari ini adalah fungsi `String.split` yang kita lihat sebelumnya. Itu memiliki dua varian, satu yang menerima satu argumen (`String.split/1`) dan satu yang menerima dua argumen (`String.split/2`). Kita hanya melihat versi dengan satu argumen sebelumnya:

```elixir linenums="1"
iex> String.split("Hello, World!")
["Hello,", "World!"]
```
Namun, jika kita menyediakan argumen kedua untuk fungsi ini, maka itu akan berfungsi berbeda:

```elixir linenums="1"
iex> String.split("Hello, World!", "o")
["Hell", ", W", "rld!"]
```
Nama fungsi tidak berubah, tetapi jumlah argumen berubah, dan itu mengubah cara fungsi berfungsi.

Argumen kedua untuk `String.split/2` memberi tahu komputer di mana harus memisahkan string. Dengan versi satu argumen, komputer mengasumsikan kita ingin memisahkan pada spasi antara kata-kata. Dengan versi dua argumen — yaitu, versi /2 — kita memberi tahu bahwa kita ingin memisahkan pada karakter "o" sebagai gantinya.

Pada titik ini juga penting untuk menyebutkan bahwa fungsi `String.upcase` yang kita gunakan di bab sebelumnya memiliki nama resmi `String.upcase/1`. Sama seperti /2 menunjukkan bahwa fungsi tersebut mengambil dua argumen, /1 di sini menunjukkan bahwa fungsi ini mengambil satu argumen. Ketika merujuk pada fungsi Elixir, pastikan untuk menyertakan arity serta nama fungsi tersebut.

Ini adalah perbedaan penting yang perlu dibuat dalam Elixir, jadi saya akan mengulanginya, kali ini sedikit lebih besar:

##### **Fungsi tidak hanya berbeda berdasarkan nama, tetapi juga berdasarkan jumlah argumen yang mereka terima.**

Oke, jadi kita sudah membahas apa itu /1 (Izzy sekarang dalam pemikiran mendalam), jadi mari kita bicarakan mengapa `List.reverse/1` tidak ada.

##### Terima kasih Pembaca, tetapi fungsi <s>princess</s> kami ada di modul <s>kastil</s> lain
  
Versi singkat mengapa fungsi `List.reverse/1` tidak ada adalah karena ia hidup di modul terpisah; ia ada di modul Enum. Nama Enum adalah singkatan dari Enumerable, dan dilakukan seperti itu karena tidak ada yang punya waktu untuk menulis Enumerable dengan benar setiap kali. Bahkan sebagai penulis site ini, saya kesulitan mengejanya dengan benar setiap kali! Terima kasih kepada autocompletion.

"Apa sebenarnya yang dimaksud dengan enumerable?" Izzy berteriak. Tunggu sebentar, Izzy. Kita akan sampai di situ.

List adalah tipe data di Elixir yang disebut enumerable. Maps juga merupakan enumerable. Ini berarti bahwa mereka dapat diiterasi; yang berarti Anda dapat melakukan sesuatu dengan setiap item di objek enumerable (sebuah list atau map). Misalnya, jika kita menuliskan list kita di selembar kertas, itu mungkin terlihat seperti ini:

- Cat  
- Dog  
- Cow  
- Turducken
  
Mungkin saja untuk menulis setiap item dari list secara terpisah dari item lainnya dalam list. Karena kita dapat melakukan ini, kita dapat dengan aman mengatakan bahwa list ini adalah enumerable. Kita bisa mencoba melakukan hal yang sama untuk sebuah angka (seperti 1,354), tetapi itu tidak masuk akal:

- 1  
- 3  
- 5  
- 4
  
Angka tidak dapat diiterasi karena tidak masuk akal untuk ditulis seperti ini, tidak seperti list kita.

Mirip dengan ini, kita bisa mengiterasi melalui map. Jika kita mengambil salah satu map kita dari sebelumnya...

```elixir linenums="1"
%{name: "Izzy", age: "30ish", gender: "Female"}
```
...dan menuliskan setiap pasangan kunci dan nilai, mungkin terlihat seperti ini:

```
Nama  
	Izzy  
Usia  
	30ish  
Jenis Kelamin  
	Female
```
  
Sekali lagi, masuk akal bagi map untuk menjadi enumerable karena Anda dapat *enumerate* melalui setiap pasangan kunci dan nilai dalam map.

##### And now for the big reveal

Kita perlu ingat bahwa ketika kita bekerja dengan hal-hal enumerable di Elixir, fungsi yang kita butuhkan mungkin berada di tempat lain. Meskipun ada modul List dan Map (yang akan kita lihat di bab selanjutnya) — terkadang, kita perlu melihat di modul Enum juga untuk fungsi yang kita inginkan.

Kita mencoba mencari di modul List untuk menemukan fungsi `reverse/1` agar kita bisa membalikkan list kita, tetapi tidak ada di sana. Kita menemukan bahwa fungsi tersebut sebenarnya ada di dalam modul Enum, jadi mari kita coba menggunakan fungsi tersebut. Sebelum itu, mari kita dapatkan list kita dalam bentuk Elixir lagi. Sudah lama sejak kita melihatnya dengan cara itu:

```elixir linenums="1"
iex> animals_or_derivatives_of_animals = ["cat", "dog", "cow", "turducken"]
```

Karena kita sekarang tahu bahwa list adalah enumerable, dan bahwa fungsi `List.reverse/1` tidak ada tetapi kita juga (sekarang) tahu bahwa ada modul Enum untuk bekerja dengan hal semacam ini, kita bisa menebak bahwa akan ada fungsi `Enum.reverse/1`. Mari kita coba dan lihat:

```elixir linenums="1"
iex> Enum.reverse(animals_or_derivatives_of_animals)
["turducken", "cow", "dog", "cat"]
```
Hore! Kita berhasil membalikkan list kita.

Fitur-fitur Izzy relaks dari konsentrasi yang intens menjadi lebih netral dan dia bertanya, "Hei, Anda menyebutkan sebelumnya bahwa Anda bisa mengiterasi melalui list atau map, tetapi Anda tidak menunjukkan contoh tentang itu. Kenapa?" Anda benar sekali, Izzy. Saya terlalu teralihkan dengan menjelaskan mengapa `List.reverse/1` tidak ada untuk menjelaskan bagaimana cara mengiterasi melalui enumerable. Saya senang ada yang memperhatikan.

Mari kita lihat sekarang bagaimana cara melakukannya sebelum kita beralih ke fungsi lainnya. Kita sudah berbicara tentang enumerable secara singkat, dan akan sangat disayangkan untuk berhenti begitu awal ketika Anda bisa melakukan lebih banyak hal dengan mereka selain membalikkan.

##### Enumerating the enumerables

Untuk memuaskan Izzy (dan banyak orang yang dia pimpin) sekali lagi, kita akan perlu melihat bagaimana cara mengiterasi melalui enumerable. Apa yang dimaksud dengan ini adalah kita akan mendapatkan sebuah enumerable (sebuah list atau map) dan kita akan melalui setiap item dari enumerable dan melakukan sesuatu dengan mereka.

Mari kita mulai dengan sebuah list. Bagaimana jika kita menggunakan list dari lima kota paling layak huni di dunia, hanya untuk sesuatu yang berbeda?

```elixir linenums="1"
iex> cities = ["vienna", "melbourne", "osaka", "calgary", "sydney"]
```

Cara termudah untuk mengiterasi melalui sebuah list di Elixir adalah dengan menggunakan fungsi `Enum.each/2`. Ingat bahwa /2 di sini berarti bahwa fungsi tersebut menerima dua argumen. Dua argumen tersebut adalah:

1. Hal yang ingin kita iterasi; dan
2. Sebuah fungsi yang akan dijalankan untuk setiap item.

Mari kita lihat contoh:

```elixir linenums="1"
iex> Enum.each(cities, &IO.puts/1)
```

Argumen pertama di sini adalah list kota kita. Argumen kedua adalah fungsi yang ingin kita jalankan untuk setiap item dalam list ini: khususnya fungsi bawaan `IO.puts/1`. Simbol & sebelum nama fungsi ini disebut sebagai "capture operator". Kita telah melihat ini di Bab 5, tetapi kita menggunakannya untuk membangun fungsi kita sendiri saat itu:

```elixir linenums="1"
iex> greeting = &("Hello #{&1}")
```

Simbol & memiliki kegunaan lain, yaitu untuk menangkap fungsi dari modul sehingga kita dapat menggunakannya nanti. Dalam contoh ini, kita menangkap `IO.puts/1` sehingga `Enum.each/2` dapat memanggil fungsi itu pada setiap item dalam list kota.

Mari kita lihat apa yang dilakukan kombinasi `Enum.each`, `cities`, dan `&IO.puts/1`:

```elixir
iex> Enum.each(cities, &IO.puts/1)
vienna
melbourne
osaka
calgary
sydney
:ok
```

Kombinasi khusus dari ketiga hal ini membuat Elixir mengeluarkan setiap kota dalam satu baris di prompt iex kita. Kemudian ada satu lagi hal: nilai atom kecil :ok di akhir output kita. Itu adalah nilai atom kecil yang menunjukkan kepada kita bahwa iterasi dengan `Enum.each/2` berhasil. Kita telah melihat atom seperti ini digunakan untuk kunci dalam map di bab sebelumnya, tetapi mereka juga bisa digunakan dalam kode Elixir seperti ini.

Mari kita lihat lebih dekat apa yang dilakukan kode `Enum.each/2` ini. Khususnya: apa yang dilakukan `&IO.puts/1`. Anda tahu di Elixir bahwa fungsi bisa menerima argumen dan Anda mungkin memikirkan bahwa argumen-argumen tersebut bisa berupa string, list, atau map karena ini adalah yang telah kita lihat sebelumnya. Tetapi argumen fungsi juga bisa berupa fungsi lain. Inilah yang terjadi di sini ketika kita menggunakan `&IO.puts/1`. Kita mengoper fungsi itu sebagai argumen ke `Enum.each/2`.

Untuk mendapatkan gambaran tentang bagaimana `Enum.each/2` mampu menerima fungsi `IO.puts/1` dan melakukan sesuatu dengan itu, kita bisa menggunakan kode ini di prompt iex:

```elixir linenums="1"
iex> puts = &IO.puts/1
puts.("melbourne")
"melbourne"
:ok
```

Dengan kode ini, kita telah menetapkan fungsi `IO.puts/1` ke variabel bernama `puts`. Ini mirip dengan apa yang terjadi di dalam fungsi `Enum.each/2`: fungsi apapun yang kita oper sebagai argumen kedua akan disimpan dengan nama tertentu. Kemudian `Enum.each/2` pergi melalui setiap item dan memanggil fungsi yang disediakan padanya, sama seperti yang telah kita lakukan di atas.

##### Cobalah contoh ini sebagai program juga

Anda harus mencoba menjalankan contoh di atas sebagai skrip Elixir juga. Simpan file ini sebagai `cities.exs` dan jalankan dengan `elixir cities.exs`.

Apa yang akan Anda lihat sebagian besar sama: semua kota akan ditampilkan pada baris mereka sendiri. Apa yang tidak akan Anda lihat adalah `:ok` terakhir. Ini karena ketika kita menjalankan fungsi di prompt `iex`, fungsi tersebut akan selalu memberi tahu kita apa hasilnya.

Namun, ketika kita masuk ke "waktu besar" menjalankan program yang sebenarnya, Elixir hanya akan menghasilkan output setelah kita memberitahunya untuk melakukannya; dengan sesuatu seperti `IO.puts/1`. Inilah sebabnya mengapa ketika Anda menjalankan skrip ini Anda tidak akan melihat `:ok`.

"Baris terakhir terlihat persis seperti bagaimana kita menjalankan fungsi kembali di Bab 5", seru Izzy. Ya, Izzy! Itu benar sekali. Kembali di bab itu kita mendefinisikan fungsi greeting seperti ini:

```elixir linenums="1"
iex> greeting = fn (place) -> "Hello, #{place}!" end
#Function<6.52032458/1 in :erl_eval.expr/5>
```
Kita kemudian membuat Elixir menjalankan fungsi ini menggunakan sintaks ini:

```elixir linenums="1"
iex> greeting.("World")
"Hello, World!"
```

Apa yang kita lakukan berbeda di sini dengan `puts = &IO.puts/1` adalah kita menggunakan fungsi bawaan daripada menyusun salah satu fungsi kita sendiri. Kita bisa melakukan ini dengan fungsi bawaan apapun yang kita mau. Berikut adalah contoh lain, menggunakan `String.capitalize/1`:

```elixir
iex> cap = &String.capitalize/1
cap.("melbourne")
"Melbourne"
```

Di sini, fungsi `String.capitalize/1` mengambil sebuah string dan mengubah huruf pertamanya menjadi huruf kapital. Dalam contoh kode ini, kita membuatnya sehingga kita bisa memanggil `String.capitalize/1` seolah itu adalah fungsi yang disebut `cap`. Namun, jika kita ingin mengkapitalisasi nama-nama kota kita menggunakan fungsi `String.capitalize/1` dengan `Enum.each/2`, itu tidak akan banyak berfungsi:

```elixir
iex> Enum.each(cities, &String.capitalize/1)
:ok
```

Tidak ada output di sini selain :ok karena kita tidak memberitahu Elixir untuk menampilkan apa pun. Ia dengan patuh menjalankan fungsi `String.capitalize/1` untuk setiap item dalam list, dan kemudian dengan patuh "melupakan" untuk memberitahu kita apa hasilnya.

Jika kita ingin melihat apa hasilnya dari mengevaluasi `String.capitalize/1` untuk setiap item dalam list, kita perlu menggunakan fungsi lain.

##### Map, but not the kind that you know already

Nama-nama kota ini harus ditulis dengan huruf kapital karena mereka adalah nama-nama yang tepat, tetapi siapa pun yang membuat daftar ini telah mengabaikan untuk menuliskannya dengan huruf kapital. Ups! Yang seharusnya kita miliki adalah daftar dengan penulisan yang benar:

```elixir linenums="1"
["Vienna", "Melbourne", "Osaka", "Calgary", "Sydney"]
```

Kami mencoba menggunakan `Enum.each/2` untuk memberikan kami daftar kota yang telah ditulis dengan huruf kapital, tetapi itu hanya memberi tahu kami :ok dan tidak memberikan kembali daftar nama kota yang ditulis dengan huruf kapital.

Kami memerlukan sebuah fungsi yang melalui setiap item dalam daftar dan menerapkan `String.capitalize/1`, dan kemudian menunjukkan kepada kami hasil dari setiap penerapan fungsi itu. Sesuatu yang akan mengubah daftar kota kami yang ada menjadi daftar seperti ini:

```elixir linenums="1"
iex> cities = [
    String.capitalize("vienna"),
    String.capitalize("melbourne"),
    String.capitalize("osaka"),
    String.capitalize("calgary"),
    String.capitalize("sydney"),
]
["Vienna", "Melbourne", "Osaka", "Calgary","Sydney"]
```

Tetapi karena kami sudah memiliki daftar, kami perlu melakukan sesuatu untuk daftar tersebut agar dapat mengubahnya menjadi apa yang kami inginkan. Sesuatu itu adalah menggunakan fungsi lain dari modul Enum yang disebut `Enum.map/2`. Fungsi map ini berbeda dari jenis data map (%{name: "Izzy"}), di mana fungsi yang dipanggil map akan mengambil enumerable yang ditentukan dan fungsi lain sebagai argumen, kemudian mengulangi setiap item dalam daftar dan menjalankan fungsi lain itu untuk setiap item, dan kemudian mengembalikan hasil dari setiap eksekusi fungsi.

Cukup banyak omong kosong. Mari kita lihat ini dalam praktik nyata:

```elixir linenums="1"
iex> Enum.map(cities, &String.capitalize/1)
["Vienna", "Melbourne", "Osaka", "Calgary","Sydney"]
```

Hore! Setiap kota kami sekarang memiliki nama yang ditulis dengan huruf kapital dengan benar. Apa yang terjadi di sini adalah bahwa kami telah memberi tahu fungsi map bahwa kami ingin menjalankan fungsi lain — yaitu fungsi `String.capitalize/1` — pada setiap item dalam daftar kota. Inilah cara kami dapat beralih dari daftar kami yang ada dengan nama kota yang tidak ditulis dengan huruf kapital menjadi daftar baru dengan nama-nama yang ditulis dengan huruf kapital.

##### Tapi mengapa ini disebut "map"?
Sejujurnya, saya tidak terlalu memikirkan nama "map" sebelum saya menulis bagian ini di site. Saya selalu tahu bahwa itu disebut "map", tetapi tidak pernah benar-benar memikirkan alasannya. Saya ingin menjawabnya di sini, tetapi saya juga tidak tahu dan jadi saya bertanya tentang mengapa ini disebut map di X.

Konsensus dari komunitas X tampaknya adalah bahwa ini adalah istilah matematis yang mendapatkan maknanya dari peta kartografer — di mana dimensi Bumi diwakili secara grafis pada sebuah peta. Ketika Anda mengubah ukuran satu bagian dari peta, Anda harus mengubah ukuran semua bagian lainnya dengan membuat transformasi yang sama, jika tidak peta itu tidak akan masuk akal. Saya menemukan itu cukup menarik, jujur.

Dalam matematika, istilah "map" berarti mengambil sekumpulan angka dan kemudian menerapkan fungsi yang sama pada mereka untuk mengubahnya menjadi sekumpulan angka baru. Hei, itu mirip dengan apa yang kami lakukan di sini — kecuali kami memiliki sekumpulan kata, dan bukan angka. Kami mengambil daftar string dan kemudian mengubahnya menjadi daftar string yang baru.

##### BYO functions
Satu contoh cepat lagi. Ketika menggunakan `Enum.each/2` atau `Enum.map/2`, kami tidak perlu selalu memberikan fungsi bawaan sebagai argumen kedua. Kami bisa memilih untuk memberikan fungsi kami sendiri sebagai gantinya. Katakanlah kami memiliki daftar angka seperti ini:

```elixir linenums="1"
iex> numbers = [4, 8, 15, 16, 23, 42]
```

Dan kemudian kami ingin mengalikan setiap angka dengan angka yang berbeda, katakanlah 2. Kami malas dan kami ingin komputer yang melakukan pekerjaan berat, jadi kami bisa memberikan `Enum.map/2` fungsi desain kami sendiri untuk mencapai tujuan ini:

```elixir linenums="1"
iex> Enum.map(numbers, fn (number) -> number * 2 end)
[8, 16, 30, 32, 46, 84]
```

Dengan fungsi kami sendiri di sini, kami mengambil setiap elemen dari daftar — yang diwakili di dalam fungsi sebagai variabel `number` — dan kemudian mengalikannya dengan 2. Ketika `Enum.map/2` telah selesai melalui daftar, itu mengeluarkan daftar baru yang menunjukkan kepada kami hasil dari menjalankan fungsi tersebut pada semua item dalam daftar.

##### Mengurangi Sebuah Enumerable
Kami sekarang telah melihat cara menggunakan dua fungsi dari `Enum`, `each/2` dan `map/2`. Ini adalah dua fungsi yang paling sering digunakan dari modul ini, dan itulah sebabnya kami melihatnya. Tetapi ada fungsi ketiga yang ingin saya ceritakan kepada Anda juga: `Enum.reduce/2`. Ini adalah fungsi yang sangat berguna!

`Enum.reduce/2` memungkinkan kami untuk mengulangi daftar dan secara bertahap menerapkan fungsi pada setiap elemen dalam daftar itu untuk mendapatkan nilai akhir. Pikirkan tentang ini seperti saat Anda memasak: Anda mengurangi semua bahan menjadi satu hidangan. Anda tidak berpikir tentang spaghetti bolognese sebagai kombinasi bawang, bawang putih, daging cincang, tomat, rempah-rempah, dan spaghetti. Anda memikirkannya sebagai satu hidangan lengkap. Ketika kami ingin menggabungkan nilai-nilai di Elixir untuk menghasilkan satu nilai akhir, kami akan menggunakan `Enum.reduce/2`. Mari kita lihat sekarang.

Kami mungkin ingin Elixir memberi tahu kami berapa rata-rata dari daftar angka. Misalnya, kami mungkin ingin menghitung rata-rata dari beberapa skor, katakanlah untuk sebuah ujian. Hei, lihat, di sini ada beberapa angka skor yang berguna (dari 100):

```elixir linenums="1"
iex> scores = [74, 79, 89, 32, 79, 70, 32, 69, 76, 73, 88, 73, 82, 31]
```

Saya ingin terus menulis angka di atas tetapi 14 angka terasa tepat untuk beberapa alasan. Sepertinya sebagian besar orang dalam ujian ini melakukan dengan sangat baik. Bagus untuk mereka! Beberapa tidak terlalu baik dan hanya mendapatkan skor 32 dan satu mendapat skor 31. Bagaimanapun, mari kita tidak melihat data terlalu dekat. Apa yang ingin kami lakukan adalah menghitung rata-rata untuk skor-skor ini dan untuk itu kami mungkin mencoba menjumlahkan angka-angka ini sendiri di selembar kertas.

![Adding together numbers manually](https://joyofelixir.com/9-lists/images/reduce-sum.png)

Atau kita mungkin mencoba menggunakan kalkulator sebagai alternatif, karena itu lebih sedikit berisiko untuk kesalahan. Cara kami melakukan perhitungan ini di kalkulator persis seperti di atas: kami akan menjumlahkan setiap angka satu per satu untuk menghitung total. Input kami ke dalam kalkulator akan seperti ini:

```bash
74 + 79 + 89 + 32 + 79 + 70 + 32 + 69 + 76 + 73 + 88 + 73 + 82 + 31
```

Kalkulator kemudian akan memberi tahu kami bahwa total dari angka-angka ini adalah 947, seperti yang seharusnya ditunjukkan oleh perhitungan kami di kertas. Silakan periksa ini di konsol iex Anda juga jika Anda mau; lagipula, ini hanya kalkulator yang lebih kuat.

Setelah kami mendapatkan totalnya, kami perlu membagi total tersebut dengan jumlah angka yang telah kami jumlahkan untuk mendapatkan rata-ratanya. Di sini, kami memiliki 14 angka. Jadi rata-ratanya adalah `947 / 14`, yang dapat diberitahukan oleh kalkulator atau prompt iex kepada Anda: `67.64285714285714`. Kalkulator mungkin tidak memiliki banyak tempat desimal. Jika kami ingin menulis seluruh operasi ini dalam kode Elixir, itu sangat sederhana:

```elixir linenums="1"
iex> (74 + 79 + 89 + 32 + 79 + 70 + 32 + 69 + 76 + 73 + 88 + 73 + 82 + 31) / 14
```

Kami menjumlahkan semua angka, kemudian membaginya dengan berapa banyak skor yang kami miliki. Mudah! Ini mudah di sini karena hanya ada 14 angka. Tapi bagaimana jika kami memiliki skor dari ratusan orang? Kami tidak ingin memasukkan semua ini ke kalkulator atau prompt iex, kan? "Tidak mungkin!", kata Izzy. Tepat sekali! Jadi mari kita lihat bagaimana kami bisa menggunakan `Enum.reduce/2` untuk melakukan penjumlahan untuk kami, agar kami tidak perlu menghitung semuanya sendiri.

```elixir linenums="1"
iex> scores = [74, 79, 89, 32, 79, 70, 32, 69, 76, 73, 88, 73, 82, 31]
[74, 79, 89, 32, 79, 70, 32, 69, 76, 73, 88, 73, 82, 31]
iex> Enum.reduce(scores, fn (score, sum) -> sum + score end)
```

Fungsi `reduce/2` di sini melakukan perhitungan yang sama persis seperti yang kami lakukan sebelumnya: ia mengembalikan 947. Itu dilakukan dengan mengambil angka pertama, kemudian menjumlahkan angka kedua, ketiga, keempat, dan seterusnya untuk mendapatkan total. Bagaimana cara kerjanya? Mari kita telusuri apa yang dilakukan fungsi ini.

Pertama, kami mengirimkan `reduce/2` daftar skor yang ingin kami jumlahkan. Kemudian kami memberikannya fungsi lain yang mengambil dua argumen: `score` dan `sum`. Di dalam fungsi ini, kami menjumlahkan kedua argumen tersebut. Tetapi nilai apa yang dimiliki `score` dan `sum` di dalam fungsi ini? Salah satu cara mudah untuk mengetahuinya adalah dengan meminta Elixir untuk menampilkan nilai-nilai mereka setiap kali fungsi ini di dalam `reduce/2` digunakan:

```elixir linenums="1"
iex> Enum.reduce(scores, fn (score, sum) ->
  IO.puts(sum)
  IO.puts(score)
  IO.puts("---")
  sum + score
end)
```

Meskipun urutan argumen di dalam fungsi adalah `score` dan `sum`, kami menampilkannya di sini sebagai `sum` dan `score` karena alasan yang akan menjadi jelas segera. Ketika kami menjalankan varian baru dari fungsi `reduce/2` ini, hasilnya akan seperti ini:

```
74
79
---
153
89
---
242
32
---
274
79
---
353
70
---
423
32
---
455
69
---
524
76
---
600
73
---
673
88
---
761
73
---
834
82
---
916
31
---
947
```

Angka pertama yang kami tampilkan adalah `sum` dan angka kedua adalah `score`. Jika kita melihat empat baris pertama dari output kami, kita akan melihat tiga angka: 74, 79, dan 153.

```
74
79
---
153
```

Jika kita melihat kembali pada definisi daftar skor kami, kita dapat melihat bahwa dua angka pertamanya adalah 74 dan 79.

```elixir linenums="1"
iex> scores = [74, 79, ...]
```

Jadi, dari mana asal 153? Jawabannya sederhana: `74 + 79 = 153`. Jadi, kita bisa melihat dari output di sini bahwa fungsi `reduce/2` kita mengambil item pertama dari daftar kita dan menjadikannya argumen `sum` awal untuk fungsi di dalamnya. Item kedua kemudian menjadi argumen `score`. Di dalam fungsi, kita menjumlahkan kedua nilai ini, dan itu menghasilkan 153. Fungsi `reduce/2` terus melanjutkan melalui angka-angka yang tersisa di dalam daftar, menjumlahkannya satu per satu hingga kita mendapatkan hasil akhir.

Jadi, itulah fungsi `reduce/2` yang menakjubkan, atau setidaknya salah satu contohnya. Seperti yang Anda lihat, ini sangat berguna ketika kita ingin menggabungkan (atau mengurangi) beberapa item menjadi satu item.

##### Menjumlahkan Daftar
Saatnya saya mungkin harus menyebutkan satu fungsi lagi di dalam toolbox `Enum` yang disebut `sum/1`. Fungsi ini mengambil daftar dan menjumlahkan semua item di dalamnya, persis seperti fungsi `reduce/2` kita. Kedua fungsi ini identik dalam cara kerjanya:

```elixir
iex> scores = [74, 79, 89, 32, 79, 70, 32, 69, 76, 73, 88, 73, 82, 31]
[74, 79, 89, 32, 79, 70, 32, 69, 76, 73, 88, 73, 82, 31]
iex> Enum.sum(scores)
947
iex> Enum.reduce(scores, fn (score, sum) -> sum + score end)
947
```

Jadi jika Anda ingin menjumlahkan daftar angka, lebih baik menggunakan `Enum.sum/1` daripada menggunakan `Enum.reduce/2`, karena itu memerlukan kode yang lebih sedikit. Jika Anda ingin melakukan operasi lain selain penjumlahan, seperti pengurangan, perkalian, pembagian, dan sebagainya, maka lebih baik menggunakan `Enum.reduce/2`.

##### Latihan
1. Gunakan kombinasi `Enum.map/2` dan `String.replace/3` untuk mengganti semua huruf `e` dalam kata-kata ini dengan huruf lain yang Anda pilih: `["a", "very", "fine", "collection", "of", "words", "enunciated"]`
2. Gunakan `Enum.reduce/2` untuk mengalikan angka-angka ini: `[5, 12, 9, 24, 9, 18]`

---

#### 10. Working with maps

Pada bab sebelumnya, kita melihat beberapa fungsi yang bisa kita gunakan untuk bekerja dengan `list`. Kita melihat beberapa fungsi dari modul `List`, tetapi sebagian besar waktu dihabiskan membahas modul `Enum`. Di bab ini, kita akan membahas bagaimana menggunakan `Enum.each/2` dan `Enum.map/2` pada maps alih-alih list. Lalu kita akan membahas beberapa fungsi dari modul `Map`.

Kita sudah membahas di bab sebelumnya tentang menggunakan fungsi `Enum.each/2` untuk bekerja dengan maps:

Mirip dengan ini, kita bisa melakukan enumerasi melalui sebuah map. Jika kita mengambil salah satu dari map yang kita gunakan sebelumnya...

```elixir
%{name: "Izzy", age: "30ish", gender: "Female"}
```

...dan menuliskan setiap pasangan kunci dan nilai, hasilnya mungkin terlihat seperti ini:

```
Nama  
	Izzy  
Umur  
	30ish  
Jenis Kelamin  
	Female  
```

Namun kita belum pernah benar-benar menunjukkan cara melakukannya! Nah, inilah contohnya:

```elixir linenums="1"
iex> person = %{name: "Izzy", age: "30ish", gender: "Female"}
 %{age: "30ish", gender: "Female", name: "Izzy"}
iex> Enum.each(person, fn ({key, value}) -> IO.puts value end)
```

Sebelum saya melanjutkan, Izzy menyela. "Hei, kurung kurawal di dalam fungsi yang dilewatkan ke `each` itu aneh! Itu terlihat seperti map, tetapi bukan map karena tidak ada `%` di depannya. Dan itu bukan list karena kurungnya; list memiliki kurung siku. Jadi apa itu?". Izzy sedang membicarakan kode ini secara khusus:

```elixir linenums="1"
fn ({key, value}) ...
```

`{key, value}` di sini menunjukkan jenis data dalam Elixir yang belum kita lihat sebelumnya, yaitu *tuple*. Tuple berfungsi seperti list dalam arti bahwa urutan elemen di dalamnya penting, tetapi Anda tidak bisa melakukan enumerasi melalui mereka seperti Anda bisa dengan list; dengan kata lain: tuple tidak dapat dienumerasi. Tuple digunakan untuk mewakili data yang terurut dan terhubung. Dalam contoh ini, setiap tuple mewakili kunci dan nilai yang terhubung dengannya.

Dalam fungsi yang dilewatkan ke `each`, tuple digunakan sebagai pengganti dua argumen fungsi (yaitu `fn(key, value) ->`) untuk menunjukkan bahwa `key` dan `value` tersebut memiliki hubungan. `key` dan `value` ini tidak direpresentasikan sebagai list (yaitu `fn([key, value]) ->`) karena adanya hubungan ini. (Selain itu: Elixir dalam "pemikirannya" sendiri menganggap maps sebagai daftar tuple, jadi ini adalah alasan lain mengapa mereka tuple, dan bukan list!)

Mari kita lihat lagi bagaimana kita menggunakan `Enum.each/2` dan apa outputnya:

```elixir linenums="1"
iex> Enum.each(person, fn ({key, value}) -> IO.puts value end)
30ish
Perempuan
Izzy
:ok
```

Penggunaan `Enum.each/2` kita melalui setiap `key` dan `value`, mengabaikan kunci dan mengeluarkan nilai dengan `IO.puts/1`. Ini hampir identik dengan contoh sebelumnya dari `Enum.each/2`, di mana kita menggunakan list kota dengan fungsi `IO.puts/1`:

```elixir linenums="1"
iex> Enum.each(cities, &IO.puts/1)
```

Dalam contoh list, kita bisa menggunakan `&IO.puts/1`. Namun dalam contoh map, kita harus mengeluarkan nilai dengan menggunakan tuple, dan kemudian kita perlu menggunakan versi panjang dari `IO.puts/1` (`IO.puts(value)`) untuk mengeluarkan nilai tersebut. Mari kita lihat apa yang terjadi jika kita tidak menggunakan versi panjang tersebut.

```elixir linenums="1"
iex> Enum.each(person, &IO.puts/1)
** (Protocol.UndefinedError) protocol String.Chars tidak diimplementasikan untuk {"age", "30ish"}
```

Uh oh, komputer marah lagi. Pesan error yang samar ini adalah cara yang rumit untuk mengatakan bahwa `IO.puts/1` tidak tahu cara untuk mengeluarkan tuple. Kita hanya perlu berhati-hati bahwa kita hanya memberikan `IO.puts/1` hal-hal yang bisa ditangani. Jika kita memberikan sesuatu yang tidak bisa ditangani oleh `IO.puts/1`, maka akan muncul error seperti ini.

Sekarang kita sudah melihat bagaimana menggunakan `Enum.each/2` untuk maps, sama seperti bagaimana kita melihatnya di bab sebelumnya untuk list. Di bab sebelumnya kita juga melihat `Enum.map/2` dan `Enum.reduce/2`, jadi wajar jika kita membahasnya di sini juga.

##### Mapping over maps

Saya penasaran dengan map apa yang bisa kita gunakan kali ini. Kita sudah menggunakan map person beberapa kali:

```elixir linenums="1"
iex> person = %{name: "Izzy", age: "30ish", gender: "Female"}
```

Kita sebaiknya mencoba menggunakan map lain untuk bagian ini. Hmmm. Bagaimana dengan map yang berisi hari-hari dalam seminggu dan suhu yang diharapkan? Inilah tampilan minggu depan di Melbourne pada saat penulisan ini:

```elixir linenums="1"
%{
  "Senin" => 28,
  "Selasa" => 29,
  "Rabu" => 29,
  "Kamis" => 24,
  "Jumat" => 16,
  "Sabtu" => 16,
  "Minggu" => 20
}
```

Suhu yang diharapkan ini bukan hanya angka acak. Begitulah Melbourne, selalu berubah-ubah. Sekarang, bagaimana jika kita mengonversi suhu-suhu ini dari derajat celsius ke fahrenheit untuk teman-teman kita di Amerika? Jika tidak, mereka mungkin akan membaca angka-angka tersebut dan berpikir bahwa Melbourne adalah neraka dingin, padahal sebenarnya tidak.

Jadi kita ingin mengonversi suhu-suhu ini dari derajat celsius menjadi fahrenheit, mengubah map menjadi seperti ini:

```elixir linenums="1"
%{
  "Senin" => 82.4,
  "Selasa" => 84.2,
  "Rabu" => 84.2,
  "Kamis" => 75.2,
  "Jumat" => 60.8,
  "Sabtu" => 60.8,
  "Minggu" => 68
}
```

Kita sudah tahu bagaimana mengonversi angka-angka ini jika hanya berupa daftar angka, tanpa hari-hari dalam seminggu, seperti ini:

```elixir linenums="1"
[28, 29, 29, 24, 16, 16, 20]
```

Kita akan menggunakan `Enum.map/2` untuk menjalankan fungsi pada setiap angka untuk mengonversi angka-angka tersebut ke fahrenheit (menggunakan fungsi yang sudah kita lihat di Bab 5):

```elixir linenums="1"
iex> forecast = [28, 29, 29, 24, 16, 16, 20]
  [28, 29, 29, 24, 16, 16, 20]
  iex> Enum.map(forecast, fn (temp) -> temp * 1.8 + 32 end)
  [82.4, 84.2, 84.2, 75.2, 60.8, 60.8, 68.0]
```

Jadi, bagaimana jika kita mencoba menggunakan `Enum.map/2` pada map ramalan cuaca kita alih-alih pada list? Apa yang akan terjadi? Mari kita lihat:

```elixir linenums="1"
iex> forecast = %{
  "Senin" => 28,
  "Selasa" => 29,
  "Rabu" => 29,
  "Kamis" => 24,
  "Jumat" => 16,
  "Sabtu" => 16,
  "Minggu" => 20
}
%{"Jumat" => 16, ...}
iex> Enum.map(forecast, fn ({hari, suhu}) -> {hari, suhu * 1.8 + 32} end)
[
  {"Jumat", 60.8},
  {"Senin", 82.4},
  {"Sabtu", 60.8},
  {"Minggu", 68.0},
  {"Kamis", 75.2},
  {"Selasa", 84.2},
  {"Rabu", 84.2}
]
```

"Hei, itu bukan map! Itu daftar!" seru Izzy, tampaknya mengadaptasi kutipan dari serial opera luar angkasa yang relatif terkenal. Benar sekali, Izzy. Ketika kita memanggil `Enum.map/2` pada list atau map, kita akan mendapatkan kembali list terlepas dari jenis data yang kita gunakan. Ini berkaitan dengan bagaimana Elixir memandang maps: Elixir menganggapnya sebagai daftar tuple key-value, bukan sebagai sintaks `%{}` yang kita kenal dan sukai. Untuk mengembalikan data ini ke format yang kita kenal, kita perlu menggunakan fungsi lain dari kotak alat `Enum`, yaitu `Enum.into/2`.

Mari kita jalankan kembali baris `Enum.map/2` kita, tetapi kali ini kita akan menetapkan outputnya ke variabel.

```elixir linenums="1"
iex> new_forecast = Enum.map(forecast, fn ({hari, suhu}) -> {hari, suhu * 1.8 + 32} end)
[
  {"Jumat", 60.8},
  {"Senin", 82.4},
  {"Sabtu", 60.8},
  {"Minggu", 68.0},
  {"

Kamis", 75.2},
  {"Selasa", 84.2},
  {"Rabu", 84.2}
]
```

Kemudian kita bisa menggunakan `Enum.into/2` untuk mengonversi daftar tuple ini kembali menjadi map:

```elixir linenums="1"
iex> Enum.into(new_forecast, %{})
%{"Jumat" => 60.8, "Senin" => 82.4, "Sabtu" => 60.8, "Minggu" => 68.0,
  "Kamis" => 75.2, "Selasa" => 84.2, "Rabu" => 84.2}
```

Itu lebih baik! Data kita kembali ke bentuk map... tetapi urutan hari dalam seminggu telah hilang. Tapi tidak apa-apa karena kita tidak peduli dengan urutan dalam maps: kita mengakses nilai dalam maps berdasarkan kuncinya, bukan posisinya.

Jadi di sini kita telah melihat bagaimana menggunakan fungsi `Enum.map/2` dan `Enum.into/2` untuk mengiterasi elemen-elemen dalam map dan menjalankan fungsi pada masing-masing elemen tersebut.

Namun, ada cara yang lebih bersih untuk menulis kode di atas, dan itu dengan bantuan salah satu fitur terbaik dari Elixir: operator pipe. Mari kita luangkan sedikit waktu untuk melihat operator pipe ini sekarang.

##### The wonderful pipe operator

Saya baru saja menunjukkan satu cara menggunakan `Enum.map/2` untuk menjalankan nilai-nilai dalam map dan menerapkan fungsi pada setiap nilai tersebut. Berikut adalah contohnya, jika kamu melewatkannya:

```elixir linenums="1"
iex> forecast = %{
  "Monday" => 28,
  "Tuesday" => 29,
  "Wednesday" => 29,
  "Thursday" => 24,
  "Friday" => 16,
  "Saturday" => 16,
  "Sunday" => 20
}
%{"Friday" => 16, ...}

iex> new_forecast = Enum.map(forecast, fn ({day, temp}) -> {day, temp * 1.8 + 32} end)
  [
    {"Friday", 60.8},
    {"Monday", 82.4},
    {"Saturday", 60.8},
    {"Sunday", 68.0},
    {"Thursday", 75.2},
    {"Tuesday", 84.2},
    {"Wednesday", 84.2}
  ]

iex> Enum.into(new_forecast, %{})
%{
  "Friday" => 60.8,
  "Monday" => 82.4,
  "Saturday" => 60.8,
  "Sunday" => 68.0,
  "Thursday" => 75.2,
  "Tuesday" => 84.2,
  "Wednesday" => 84.2
}
```

Apa yang kita lakukan di sini bisa diuraikan menjadi beberapa langkah:

1. Kita mendefinisikan sebuah variabel bernama `forecast`, yang merupakan sebuah map yang berisi hari-hari dalam seminggu dan suhu yang diperkirakan.
2. Kemudian kita mengambil variabel `forecast` ini, dan meneruskannya sebagai argumen pertama ke `Enum.map/2`. Argumen kedua yang diberikan ke `Enum.map/2` adalah sebuah fungsi yang berjalan pada setiap pasangan key-value dalam map. Fungsi ini mengambil suhu -- yang merupakan nilai -- dan mengubahnya menjadi Fahrenheit.
3. Kita menetapkan hasil dari pemanggilan `Enum.map/2` ini ke sebuah variabel bernama `new_forecast`, dan kemudian langsung meneruskannya ke `Enum.into/2` sebagai argumen pertama. Argumen kedua yang diberikan ke `Enum.into/2` adalah sebuah map kosong. Ini mengubah output dari `Enum.map/2` -- sebuah daftar tuple key-value -- menjadi sebuah map yang lebih ramah.

Elixir memiliki cara untuk menulis kode ini dengan lebih singkat, yang ingin saya tunjukkan sekarang karena saya percaya ini dapat menghasilkan kode Elixir yang lebih singkat dan bersih. Kita mungkin akan menemukan lebih banyak kegunaan untuk itu seiring berjalannya waktu, dan ini sepertinya merupakan saat yang tepat untuk memperkenalkan konsep ini.

Cara menulis kode yang lebih singkat di sini adalah dengan menggunakan operator pipe, `|>`. Operator pipe memungkinkan kita untuk menghubungkan beberapa aksi dalam Elixir, meneruskan hasil dari satu fungsi ke fungsi berikutnya. Disebut operator pipe karena ia menghubungkan fungsi-fungsi bersama secara linear, dengan data yang mengalir dari satu fungsi ke fungsi berikutnya; seperti air melalui pipa. Sayangnya, tidak seperti di permainan Tony Hawk's Pro Skater, kita tidak mendapatkan ribuan poin karena menghubungkan combo yang keren. Tetapi kita masih mendapatkan kepuasan besar ketika semuanya bekerja bersama!

Mari kita lihat contoh kecil operator pipe menggunakan fungsi dari modul `String` terlebih dahulu sebelum kita menggunakannya pada data `forecast` ini.

```elixir linenums="1"
iex> "hello pipe operator" |> String.upcase() |> String.reverse()
"ROTAREPO EPIP OLLEH"
```

Kita bisa menganggap operator pipe sebagai "dan kemudian". Dalam contoh di atas, kita:

1. Memiliki sebuah string
2. Dan kemudian kita memanggil `String.upcase()`
3. Dan kemudian kita memanggil `String.reverse()`

Berikut adalah versi ilustrasinya:

![How data flows from one function to another](https://joyofelixir.com/10-maps/images/pipe-flow-strings.png)

Kode ini mengambil string, lalu meneruskannya ke `String.upcase()`. Hasil dari operasi tersebut adalah `"HELLO PIPE OPERATOR"`. Kemudian, kita mengambil string yang sudah diubah menjadi huruf besar dan meneruskannya ke `String.reverse()`, yang kemudian mengubahnya menjadi `"ROTAREPO EPIP OLLEH"`.

Tanpa operator pipe, kita harus menulis kode ini seperti:

```elixir linenums="1"
iex> String.reverse(String.upcase("hello pipe operator"))
```

Kode ini lebih sulit dibaca dan dipahami, karena kita harus membacanya dari dalam ke luar. Dengan operator pipe, kita membaca kode seperti kita membaca kalimat ini: dari kiri ke kanan. Kita bisa lebih mudah memahami transformasi data kita dengan menggunakan operator pipe di Elixir.

Sekarang mari kita gunakan operator pipe pada data `forecast` kita. Berikut adalah beberapa kode yang menggunakan operator pipe ("dan kemudian") yang secara fungsional identik dengan kode dari bagian sebelumnya, di mana kita memiliki data perkiraan suhu dalam Celsius dan mengonversinya ke Fahrenheit:

```elixir linenums="1"	
%{
  "Monday" => 28,
  "Tuesday" => 29,
  "Wednesday" => 29,
  "Thursday" => 24,
  "Friday" => 16,
  "Saturday" => 16,
  "Sunday" => 20
}
|> Enum.map(fn ({day, temp}) -> {day, temp * 1.8 + 32} end)
|> Enum.into(%{})
|> IO.inspect
```

Silakan masukkan kode ini ke dalam file bernama `forecast.exs` dan jalankan dengan perintah `elixir forecast.exs`. Inilah yang akan kamu lihat sebagai output:

```bash
%{
  "Friday" => 60.8,
  "Monday" => 82.4,
  "Saturday" => 60.8,
  "Sunday" => 68.0,
  "Thursday" => 75.2,
  "Tuesday" => 84.2,
  "Wednesday" => 84.2
}
```

Saya telah meletakkan setiap kunci dan nilai pada barisnya masing-masing, tetapi kamu bisa melihat bahwa outputnya sama seperti sebelumnya di konsol `iex`, dan kodenya juga terlihat lebih rapi! "Luar biasa," kata Izzy. Jadi, apa yang terjadi di sini? Mari kita lihat langkah-langkahnya:

1. Kita mendefinisikan sebuah map yang berisi hari-hari dalam seminggu dan suhu yang diperkirakan. Kita tidak menetapkannya ke sebuah variabel.
2. Dan kemudian kita mengalirkan map ini menggunakan operator pipe (`|>`) ke dalam `Enum.map/2`. Ini membuat map menjadi argumen pertama dari `Enum.map/2`, sehingga kita tidak perlu lagi mendefinisikan variabel `forecast` dan meneruskannya sebagai argumen pertama. Operator pipe secara otomatis memberikan map ke fungsi. Satu-satunya argumen pada `Enum.map/2` di sini adalah fungsi yang kita gunakan untuk mengonversi nilai suhu. Kita masih menyebut fungsi ini sebagai `Enum.map/2`, karena ia menerima dua argumen: nilai yang di-pipe dan fungsinya.
3. Dan kemudian kita meneruskan hasil dari pemanggilan `Enum.map/2` ini ke `Enum.into/2`, dan hasil dari `Enum.map/2` menjadi argumen pertama dari `Enum.into/2`. Argumen kedua untuk `Enum.into/2` masih berupa map kosong.
4. Terakhir, kita mengalirkan hasil dari `Enum.into/2` ke dalam sebuah fungsi yang belum kita lihat sebelumnya, yaitu `IO.inspect/1`. Ini akan menampilkan map dalam bentuk yang mudah dibaca manusia. Kita tidak menggunakan `IO.puts/1` di sini karena itu hanya berfungsi dengan string, sedangkan yang kita miliki pada titik ini setelah `Enum.into/2` adalah sebuah map, bukan string. `IO.inspect/1` akan bekerja dengan semua bentuk data yang kita berikan.

"Wow, ini banyak teks!", kata Izzy, terlihat sedikit terkejut. "Apakah kamu punya contoh bagian yang bisa saya lihat sebagai gantinya?". Tentu saja!

![How data flows from one function to another](https://joyofelixir.com/10-maps/images/pipe-flow.png)

Kamu bisa menganggap operator pipe tidak hanya sebagai operator "dan kemudian", tetapi juga seperti tahapan pada air terjun — atau "datafall" — di mana data mengalir dari satu fungsi ke fungsi berikutnya.

Setiap operasi yang kita lakukan di `forecast.exs` meneruskan hasilnya ke baris berikutnya, dalam rangkaian operasi. Elixir memungkinkan kita untuk merangkai operasi-operasi ini dengan mulus menggunakan operator pipe. Semuanya mengalir dari satu baris ke baris berikutnya sampai kita mencapai akhir. Tidak perlu menyimpan data ke dalam variabel sementara seperti `new_forecast`; kamu hanya perlu mem-pipe output dari satu fungsi ke fungsi berikutnya.

Jadi, itulah operator pipe yang luar biasa! Sangat berguna, bukan?

Kita memulai bagian ini dengan membuat beberapa janji. Kita sudah menepati satu janji — kita sudah membahas fungsi `each/2` dan `map/2` dari modul `Enum`. Namun, kita juga berjanji untuk membahas beberapa fungsi dari modul `Map`. Mari kita bahas itu sekarang. Mungkin kita bahkan akan menemukan alasan lain untuk menggunakan operator pipe.

##### The marvellous Map module and its fantastic contraptions

Baiklah, kita telah menghabiskan beberapa halaman terakhir untuk melihat dua modul: `List` dan `Enum`. Saatnya untuk udara segar — saatnya keluar dari zona nyaman `Enum` yang telah kita masuki dan saatnya merasa tidak nyaman lagi! Mari kita lihat modul baru bagi kita: modul `Map`.

Jika kamu ingin melakukan hampir apa saja dengan `map` yang tidak melibatkan enumerasi, kamu akan menggunakan modul `Map` ini. Mari kita lihat beberapa aksi umum yang mungkin kamu lakukan pada `map`.

###### Menemukan nilai sebuah kunci

Di Bab 4: *Marvellous Maps* kita melihat bahwa kita bisa mengambil nilai dari kunci tertentu dengan menggunakan tanda kurung siku.

```elixir linenums="1"
iex> person = %{"gender" => "Female", "age" => "30an", "name" => "Izzy"}
%{"age" => "30an", "gender" => "Female", "name" => "Izzy"}

iex> person["name"]
"Izzy"
```

Kita membandingkannya dengan skilltester yang mengambil barang yang relevan:

![](https://joyofelixir.com/images/4/skilltester.png)

The Map module provides us another way to get that value out: `Map.get/2`.

```elixir linenums="1"
iex> Map.get(person, "name")
```

Sekarang, ini mungkin tidak terlihat terlalu berguna. Lagi pula, mengapa tidak menggunakan cara lama: `person["name"]`? Nah, satu situasi di mana ini bisa berguna adalah jika kamu ingin menemukan kunci tertentu di tengah-tengah rangkaian pipe. Bayangkan kamu memiliki variabel bernama `get_attendees` yang memberikan data seperti ini:

```elixir linenums="1"
%{
  "people" => ["Izzy", "The Author"],
  "robots" => ["Roboto", "TARS"]
}
```

Kemudian dari data ini, kamu ingin mendapatkan orang pertama dari daftar `people`. Kamu bisa menulisnya seperti ini:

```elixir linenums="1"
attendees = get_attendees()
List.first(attendees["people"])
```

Namun, kode ini terlihat membingungkan. Urutannya terlihat seperti:

1. Dapatkan daftar attendees
2. Dapatkan yang pertama dari daftar itu...
3. Daftar tersebut adalah `attendees["people"]`

Baik Elixir maupun otak kita harus menafsirkan apa yang ada di dalam tanda kurung `List.first/1` terlebih dahulu, lalu menafsirkan `List.first/1`. Ini mengharuskan kita untuk sedikit melompat di dalam kode karena kode ini tidak dijalankan dalam urutan yang kita baca.

Jika kita menggunakan operator pipe (`|>`) dan `Map.get/2`, kita bisa merapikan kode ini dan membuatnya lebih mudah dibaca. Ini contohnya:

```elixir linenums="1"
get_attendees() |> Map.get("people") |> List.first
```

Itu jauh lebih rapi dan dibaca dalam urutan operasi yang tepat:

1. Dapatkan `attendees`
2. Kemudian, dapatkan nilai yang ditunjuk oleh kunci "people"
3. Kemudian, jalankan `List.first/1` pada nilai tersebut

Jadi, `Map.get/2` memiliki manfaatnya saat melakukan pipe chaining. Namun, jika kamu hanya ingin mengakses nilai dalam sebuah `map` secara normal, saya masih akan mengatakan tetap gunakan kode seperti `people["name"]`.

##### Pattern matching juga bisa digunakan di sini

Pembaca dengan ingatan yang kuat mungkin ingat sebuah contoh di Bab 6 yang menggunakan pattern matching untuk menemukan nama seseorang dari daftar orang. Saya telah mempersingkat contoh di bawah ini menjadi hanya bagian-bagian penting:

```elixir linenums="1"
iex> those_who_are_assembled = [
  %{age: "30an", gender: "Female", name: "Izzy"}
]
iex> [first_person = %{name: first_name} | others] = those_who_are_assembled
[%{age: "30an", gender: "Female", name: "Izzy"}]
iex> first_name
"Izzy"
```

Kita bisa saja melakukan hal yang sama di sini untuk mengambil nama manusia pertama dari daftar attendees, alih-alih menggunakan `Map.get/2`:

```elixir linenums="1"
iex> %{"people" => [first_person | others]} = get_attendees()
%{"people" => ["Izzy", "The Author"], "robots" => ["Roboto", "TARS"]}
iex> first_person
"Izzy"
```

Namun kemudian... apakah ini benar-benar lebih sederhana daripada `Map.get/2` dan `List.first/1`? Mari kita lihat keduanya secara berdampingan:

```elixir linenums="1"
get_attendees() |> Map.get("people") |> List.first
```

Saya akan berargumen bahwa ini tidak lebih sederhana, dan karena itu tidak "lebih baik" daripada `Map.get/2` dan `List.first/1`. Ini menyelesaikan tugas yang sama, tetapi kompleksitas kodenya berarti bahwa menggunakan pattern matching di sini tidaklah sepadan. Contoh "get and first" lebih mudah dibaca, mengalir dengan sangat baik dari kiri ke kanan.

Keterbacaan kode adalah sesuatu yang sangat berharga dalam semua bahasa pemrograman. Versi pipe di sini jelas lebih mudah dibaca. Kamu akan melihat kasus seperti ini dalam kode Elixir apa pun yang kamu tulis. Hampir selalu ada lebih dari satu cara menulis kode, dan dalam beberapa kasus ada lebih dari satu cara yang benar untuk menulis kode yang melakukan hal yang sama. Saat kamu menulis lebih banyak kode sendiri, kamu akan mulai mengembangkan penilaian tentang hal-hal semacam ini juga.

Saya ingin menunjukkan tiga fungsi lagi dari `Map` yang menurut saya sama pentingnya untuk diketahui seperti `Map.get/2`, yaitu `Map.put/3`, `Map.merge/2`, dan `Map.delete/2`.

###### Put

Fungsi `Map.put/3` mengambil tiga argumen: sebuah map, sebuah kunci, dan sebuah nilai. Ini akan mengembalikan versi map yang diperbarui. Bagaimana map tersebut diperbarui tergantung pada kuncinya: jika kunci tersebut sudah ada, hanya nilai untuk kunci itu yang diperbarui. Jika ini adalah kunci baru, maka baik kunci maupun nilai ditambahkan. Mari kita lihat beberapa contoh untuk memahami lebih jelas.

Kamu mungkin ingin menggunakan fungsi ini jika kamu memiliki map yang berisi data yang ingin kamu perbarui. Misalnya, data yang kita miliki tentang Izzy sejauh ini:

```elixir linenums="1"
iex> izzy = %{"name" => "Izzy", "age" => "30ish", "gender" => "Female"}
```

Baru-baru ini, kita menemukan bahwa Izzy berasal dari Australia. Itu menjelaskan aksennya dan topi cork yang dipakainya. Kita juga menemukan bahwa Izzy sebenarnya `"40ish"` daripada `"30ish"`. Ini mengejutkan kami, mengingat penampilannya yang muda. Berdasarkan informasi baru ini, kita akan menambahkan kunci baru ke map kita yang disebut `country` dan memperbarui kunci `age` dengan nilai yang lebih benar. Kita bisa mengetik semuanya dari awal:

```elixir linenums="1"
iex> izzy = %{
  "name" => "Izzy",
  "age" => "40ish",
  "gender" => "Female",
  "country" => "Australia",
}
```

Tapi itu terasa seperti banyak mengetik hanya untuk memperbarui satu kunci. Mari kita lihat bagaimana kita bisa memperbarui kunci `age` dan menambahkan kunci `country` dengan menggunakan `Map.put/3`:

```elixir linenums="1"
iex> izzy = Map.put(izzy, "age", "40ish")
%{"age" => "40ish", "gender" => "Female", "name" => "Izzy"}
```

Ah, itu jauh lebih baik daripada menulis seluruh map dari awal! Sekarang kita dapat memperbarui kunci "age" tanpa harus menulis ulang seluruh map.

Sekarang katakanlah kita ingin memperbarui kunci `age` dan kunci `country` sekaligus. Kita bisa menggunakan `Map.put/3` dan operator pipe untuk menggabungkan kedua operasi tersebut:

```elixir linenums="1"
izzy |> Map.put("age", "40ish") |> Map.put("country", "Australia")
%{"age" => "40ish", "country" => "Australia", "gender" => "Female", "name" => "Izzy"}
```

Kali ini, kita telah memperbarui nilai di bawah kunci `age`, dan kita juga menambahkan kunci baru yang disebut `country`. Penting untuk dicatat di sini bahwa map `izzy` yang asli tidak berubah sama sekali:

```elixir linenums="1"
izzy
%{"age" => "30ish", "gender" => "Female", "name" => "Izzy"}
```

Ini karena sifat *immutability* yang kita bicarakan beberapa bab lalu. Data dalam Elixir tidak pernah berubah kecuali kita menugaskan ulang variabel yang terkait dengannya. Dalam kode `Map.put/3` di atas, `izzy` tetap sama, meskipun fungsi dijalankan. Jika kita ingin memperbarui variabel `izzy` dengan data baru, kita bisa menugaskan ulang variabel tersebut:

```elixir linenums="1"
izzy = izzy |> Map.put("age", "40ish") |> Map.put("country", "Australia")
%{"age" => "40ish", "country" => "Australia", "gender" => "Female", "name" => "Izzy"}
```

Dari titik ini, kode kita akan tahu bahwa Izzy berusia 40an dan berasal dari Australia. Phew.

Cara kita menggunakan `Map.put/3` di sini adalah contoh bagus lainnya dari tindakan operator pipa, namun kita dapat menulis kode dengan cara yang lebih singkat dengan fungsi `Map` berikutnya: `merge/2`.

###### Merge

Mari kita ubah data yang kita miliki tentang Izzy kembali ke apa yang semula di awal bab ini:

```elixir linenums="1"
izzy = %{"name" => "Izzy", "age" => "30ish", "gender" => "Female"}
```

Ini akan mempermudah untuk menunjukkan apa yang dilakukan `Map.merge/2`. `Map.merge/2` mengambil dua map dan menggabungkannya. Mari kita ambil contoh terakhir kita dengan `Map.put/3` dan tulis ulang dengan `Map.merge/2` untuk mendemonstrasikan hal ini:

```elixir linenums="1"
izzy = Map.merge(izzy, %{"age" => "40ish", "country" => "Australia"})
%{
  "age" => "40ish",
  "country" => "Australia",
  "gender" => "Female",
  "name" => "Izzy"
}
```

Hasilnya adalah map yang sama seperti contoh `Map.put/3` kita, kecuali kita hanya perlu memanggil satu fungsi sekali alih-alih dua kali. Fungsi `Map.merge/2` mengambil dua map sebagai argumen, dan kemudian:

- Mengambil kunci dari map kedua yang tidak ada di map pertama dan menambahkannya ke map pertama.
- Menimpa kunci di map pertama yang ada di map kedua.

Dalam contoh ini, ia telah mengganti nilai `age` yang "lama" ("30ish") dengan yang "baru" ("40ish"), dan telah menambahkan kunci yang disebut `country` ke dalam map ini.

###### Pipe Merging

Sementara kita bisa menggunakan `Map.merge/2` untuk menggabungkan dua map untuk memperbarui map yang ada, ada juga cara yang lebih pendek, yang akan kita sebut *pipe merging*. Sintaksisnya seperti ini:

```elixir linenums="1"
iex> izzy = %{"name" => "Izzy", "age" => "30ish", "gender" => "Female"}
%{"age" => "30ish", "gender" => "Female", "name" => "Izzy"}
iex> %{izzy | "age" => "40ish", "name" => "Isadora"}
%{"age" => "40ish", "gender" => "Female", "name" => "Isadora"}
```

Sintaksis ini terlihat seperti sebuah map, tetapi terpisah menjadi dua. Di sisi kiri, di dalam sintaksis map, kita memiliki variabel yang mewakili sebuah map yang ada. Di sisi kanan, kita memiliki kunci yang ingin kita perbarui dalam map tersebut, bersama dengan nilai barunya. Seperti yang kita lihat, kunci `"age"` dan `"name"` di map tersebut berubah, mengambil nilai dari sisi kanan.

Namun, penting untuk dicatat bahwa jika kita mencoba menambahkan kunci baru ke dalam map ini, itu tidak akan berhasil dengan sintaksis ini:

```elixir linenums="1"
iex> izzy = %{"name" => "Izzy", "age" => "30ish", "gender" => "Female"}
%{"age" => "30ish", "gender" => "Female", "name" => "Izzy"}
iex> %{izzy | "country" => "Australia"}
** (KeyError) key "country" not found in: %{"age" => "30ish", "gender" => "Female", "name" => "Izzy"}
    (stdlib) :maps.update("country", "Australia", %{"age" => "30ish", "gender" => "Female", "name" => "Izzy"})
```

Fitur *pipe merging* ini hanya akan berfungsi dengan kunci yang ada dalam map, dan ini adalah perbedaan penting untuk dicatat dari `Map.merge/2`, yang akan bekerja dengan kedua jenis kunci: baru dan sudah ada.

###### Delete

Sekarang kita telah melihat bagaimana menambahkan kunci baru atau memperbarui kunci dalam sebuah map. Satu-satunya hal yang tersisa untuk dilihat adalah bagaimana menghapusnya. Kita dapat menghapus kunci dalam sebuah map dengan menggunakan fungsi `Map.delete/2`. Mari kita katakan bahwa kita tidak terlalu peduli dari negara mana Izzy berasal. Kita dapat menghapus data itu, tetapi menyimpan yang lainnya, dengan menggunakan `Map.delete/2`:

```elixir linenums="1"
izzy = Map.delete(izzy, "country")
%{"age" => "40ish", "gender" => "Female", "name" => "Izzy"}
```

Fungsi ini mengambil sebuah map sebagai argumen pertamanya, dan kemudian sebuah kunci sebagai argumen keduanya. Ketika fungsi ini dijalankan, ia akan menghapus kunci tersebut dari map.

##### Summary

Dalam bab ini, kita telah melihat beberapa cara untuk bekerja dengan map. Kita melihat bahwa kita dapat melalui setiap pasangan kunci-nilai dalam map dengan `Enum.each/2`. Kita juga menggunakan `Enum.map/2` dan `Enum.into/2` untuk mengubah nilai di dalam map menjadi nilai lain, mengonversi angka suhu menjadi fahrenheit.

Ketika kita melihat `Enum.map/2` dan `Enum.into/2`, kita menemukan bahwa kita dapat menulis kode dengan cara yang lebih pendek menggunakan operator pipe: `|>`. Operator ini memungkinkan kita untuk meneruskan hasil dari satu panggilan fungsi ke yang berikutnya, memungkinkan kita untuk menulis kode Elixir yang lebih bersih.

Kita menutup bab ini dengan melihat beberapa fungsi umum dari modul Map.

Kita melihat `Map.get/2` yang memungkinkan kita untuk memilih nilai tertentu berdasarkan nama kuncinya. Kita tahu kita sudah bisa melakukan ini dengan kode seperti `person["name"]`, tetapi seperti yang kita lihat, `Map.get/2` berguna jika kita berada di tengah operasi piping dan perlu memilih nilai dari sebuah map.

Kemudian kita melihat `Map.put/3` yang memberi kita kemampuan untuk membuat map baru dengan kunci baru dari map yang ada. Fungsi ini mengambil sebuah map, sebuah kunci, dan sebuah nilai dan kemudian memberikan kita kembali map baru dengan perubahan yang kita minta.

Jika kita menerapkan beberapa perubahan dengan `Map.put/3` sekaligus, kita belajar bahwa itu tidaklah bijak untuk melakukannya dan kemudian kita belajar tentang `Map.merge/2`. Kita melihat bahwa fungsi ini mengambil dua map dan menggabungkannya, dengan kunci dari map kedua mengambil prioritas atas kunci dari map pertama.

Hal terakhir yang kita lihat dalam bab ini adalah bagaimana mendapatkan kembali sebuah map tanpa kunci tertentu dengan `Map.delete/2`. Ini adalah cara yang baik untuk menghapus data dari sebuah map jika kita tidak membutuhkannya lagi.

Kita sekarang beranjak dari hutan `Enum`, `List`, dan `Map` menuju sesuatu yang benar-benar baru bagi kita: menggunakan Elixir untuk berinteraksi dengan file di komputer kita.

##### Latihan
Gunakan pengetahuan baru Anda tentang operator pipe untuk menulis ulang solusi Anda untuk latihan pertama Bab 8.

---

next - 11. Working with files
