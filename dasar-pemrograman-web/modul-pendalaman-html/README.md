# List

Pada HTML terdapat tiga tipe list.

1. **Unordered lists**: daftar yang ditampilkan tidak memiliki urutan. Penulisan menggunakan tag `<ul><li> ... </li></ul>`.
2. **Ordered lists**: daftar yang ditampilkan secara terurut. Penulisan menggunakan tag `<ol><li> ... </li></ol>`. Berikut adalah nilai-nilai yang dapat digunakan pada atribut type pada elemen `<ol>`.
   a. `1` : Menggunakan angka dalam urutan item (default).
   b. `a` : Menggunakan huruf kecil dalam urutan item.
   c. `A` : Menggunakan huruf besar dalam urutan item.
   d. `i` : Menggunakan huruf romawi kecil dalam urutan item.
   e. `I` : Menggunakan huruf romawi besar dalam urutan item.
3. **Description lists**: daftar yang terbuat dari beberapa istilah diikuti dengan deskripsi dari istilah tersebut.

# Gambar

Pada HTML untuk menampilkan sebuah gambar kita bisa menggunakan tag `<img>`. Berbeda dengan elemen lain, elemen `<img>` tidak menuliskan konten di antara tag pembuka dan tag penutup. Namun, untuk menetapkan gambar yang ditampilkan kita gunakan sebuah atribut. Contohnya berikut.

<img src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/dicoding-logo.jpg" alt="Dicoding Logo" width="250" />

```
<img
    src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/dicoding-logo.jpg"
    alt="Dicoding Logo"
    width="250"
/>
```

Dari kode di atas terdapat dua attributes yang harus kita gunakan ketika menerapkan elemen `<img>`.

1. **`src`** : Atribut ini berfungsi sebagai sumber dari gambar yang ditampilkan. Atribut ini dapat bernilai url gambar atau path gambar local dari gambar yang digunakan.
2. **`alt`** : Atribut ini sebenarnya tidak wajib untuk diterapkan, hanya saja atribut ini akan sangat berguna ketika gambar tidak berhasil ditampilkan. Nilai atribut ini merupakan tampilan dari gambar yang ditampilkan dalam bentuk tulisan. Jadi, ketika gambar gagal ditampilkan akan memunculkan teks alternatif yang dapat mewakili arti dari gambar tersebut.

### Jenis Format Gambar

Berikut adalah jenis format gambar yang umum digunakan pada pembuatan website.

1. Graphics Interchange Format (.gif)
   - Dapat digunakan untuk gambar animasi.
   - Ukuran file biasanya kecil.
   - Kualitas gambar terbatas.
2. Joint Photographic Expert Group image (.jpg, .jpeg, .jfif, .pjpeg, .pjp)
   - Kualitas teks pada gambar dapat menjadi buruk.
   - Ukuran file lumayan kecil.
   - Pada website biasanya digunakan untuk gambar yang tidak banyak teks.
3. Portable Network Graphics (.png)
   - Teks lebih bisa terbaca dibandingkan jenis jpeg.
   - Ukuran file dapat menjadi besar sehingga mengurangi kecepatan memuat situs.
4. WebP (.webp)
   - Dibandingkan dengan gambar berkualitas sama pada jpeg atau png, ukuran file pada webp dapat menjadi lebih kecil.
   - Namun, tidak semua web browser dapat membaca webp.
5. Scalable Vector Graphics (.svg)
   - Kualitas gambar terjaga dan ukuran file kecil.
   - Namun, tidak cocok untuk gambar yang terlalu kompleks, seperti foto.
   - Pada website biasanya digunakan untuk logo atau ikon.

# Inline Formating Text

### 1. Long Quotations

Jika memiliki sebuah kutipan ataupun sebuah testimonial, dapat gunakan format long quotations dengan menggunakan tags `<blockquote>`. Konten di dalam elemen `<blockquote>` ini dapat berupa sebuah paragraf, heading, ataupun list.

Pada elemen ini, kita dapat menggunakan atribut cite untuk menentukan sumber URL dari sebuah kutipan (jika kutipan tersebut bersumber dari sebuah situs website). Namun, tidak ada tampilan yang berbeda pada browser secara kasat mata.

<blockquote cite="https://id.wikipedia.org/wiki/Situs_web">
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>

```
<blockquote cite="https://id.wikipedia.org/wiki/Situs_web">
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>
```

### 2. Preformatted Text

HTML akan mengabaikan spasi yang dituliskan secara berulang dan juga line breaks (garis baru). Namun, pada beberapa tipe konten, seperti contoh kode atau puisi hal tersebut sangat berarti.

Dengan begitu, terdapat sebuah elemen yang dapat digunakan untuk menampilkan konten sesuai yang kita tulis pada text editor. Untuk menggunakannya, kita gunakan elemen `<pre>` sebagai pembungkus kontennya.

<pre>
  SAJAK PUTIH

Bersandar pada tari warna pelangi
Kau depanku bertudung sutra senja
Di hitam matamu kembang mawar dan melati
Harum rambutmu mengalun bergelut senda

Sepi menyanyi, malam dalam mendoa tiba
Meriak muka air kolam jiwa
Dan dalam dadaku memerdu lagu
Menarik menari seluruh aku

Hidup dari hidupku, pintu terbuka
Selama matamu bagiku menengadah
Selama kau darah mengalir dari luka
Antara kita Mati datang tidak membelah

                  Karya: Chairil Anwar
</pre>

```
<pre>
  SAJAK PUTIH

Bersandar pada tari warna pelangi
Kau depanku bertudung sutra senja
Di hitam matamu kembang mawar dan melati
Harum rambutmu mengalun bergelut senda

Sepi menyanyi, malam dalam mendoa tiba
Meriak muka air kolam jiwa
Dan dalam dadaku memerdu lagu
Menarik menari seluruh aku

Hidup dari hidupku, pintu terbuka
Selama matamu bagiku menengadah
Selama kau darah mengalir dari luka
Antara kita Mati datang tidak membelah

                  Karya: Chairil Anwar
</pre>
```

### 3. Figure

Elemen `<figure>` digunakan untuk mempresentasikan konten tersendiri (self-contained content), seperti ilustrasi, diagram, foto, atau bisa juga sebuah baris kode. Banyak hal yang dapat digunakan dalam elemen ini.

Elemen ini digunakan untuk mengelompokkan blok konten yang dapat dipindahkan posisinya dari blok utama sebuah dokumen tanpa mempengaruhi arti dari induk dokumen.

Dalam elemen figure, kita dapat menuliskan elemen `<figcaption>` sebagai sebuah caption (judul) untuk konten tersebut. Berikut adalah contoh penggunaan figure pada sebuah konten gambar.

---

<p>
  Dicoding adalah sebuah perusahaan startup ...
</p>
<br>
<figure>
  <img
    src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/g-dicoding-logo.png"
    alt="g Dicoding Logo"
    width="200px"
  />
  <figcaption>Dicoding</figcaption>
</figure>
<br>
<p>
  Materi perdana yang menjadi ...
</p>

---

```
<p>
  Dicoding adalah sebuah perusahaan startup ...
</p>

<figure>
  <img
    src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/g-dicoding-logo.png"
    alt="g Dicoding Logo"
    width="200px"
  />
  <figcaption>Dicoding</figcaption>
</figure>

<p>
  Materi perdana yang menjadi ...
</p>
```

Contoh lainnya, elemen figure dapat digunakan untuk me-_markup_ sebuah konten puisi.

<figure>
  <pre>
          SAJAK PUTIH

      Bersandar pada tari warna pelangi
      Kau depanku bertudung sutra senja
      Di hitam matamu kembang mawar dan melati
      Harum rambutmu mengalun bergelut senda

      Sepi menyanyi, malam dalam mendoa tiba
      Meriak muka air kolam jiwa
      Dan dalam dadaku memerdu lagu
      Menarik menari seluruh aku

      Hidup dari hidupku, pintu terbuka
      Selama matamu bagiku menengadah
      Selama kau darah mengalir dari luka
      Antara kita Mati datang tidak membelah

  </pre>
  <figcaption>Sajak Putih oleh Charil Anwar</figcaption>
</figure>

```
<figure>
  <pre>
          SAJAK PUTIH

      Bersandar pada tari warna pelangi
      Kau depanku bertudung sutra senja
      Di hitam matamu kembang mawar dan melati
      Harum rambutmu mengalun bergelut senda

      Sepi menyanyi, malam dalam mendoa tiba
      Meriak muka air kolam jiwa
      Dan dalam dadaku memerdu lagu
      Menarik menari seluruh aku

      Hidup dari hidupku, pintu terbuka
      Selama matamu bagiku menengadah
      Selama kau darah mengalir dari luka
      Antara kita Mati datang tidak membelah...
  </pre>
  <figcaption>Sajak Putih oleh Charil Anwar</figcaption>
</figure>
```

### 4. Anchor

Anchor (jangkar) merupakan elemen yang digunakan untuk membuat sebuah hyperlink ke halaman atau website lain, file, alamat email, atau URL lainnya. Untuk menggunakan elemen ini kita gunakan `<a>` sebagai tag pembuka dan `</a>` sebagai tag penutup. Selain itu, ada atribut wajib agar elemen ini berfungsi dengan baik, yaitu `href` untuk menetapkan sebuah target yang dituju.

Contoh:

---

<p>Hubungi kami di</p>
<ul>
  <li><a href="https://example.com">Website</a></li>
  <li><a href="mailto:info@example.com">Email</a></li>
  <li><a href="tel:+62123456">Telepon</a></li>
  <li><a href="#address">Alamat</a></li>
</ul>

---

```
<p>Hubungi kami di</p>
<ul>
  <li><a href="https://example.com">Website</a></li>
  <li><a href="mailto:info@example.com">Email</a></li>
  <li><a href="tel:+62123456">Telepon</a></li>
  <li><a href="#address">Alamat</a></li>
</ul>
```

Berikut adalah daftar atribut khusus yang dapat digunakan pada elemen ini.

|  **Atribut**   |                                                   **Nilai**                                                   |                                          **Deskripsi**                                          |
| :------------: | :-----------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------: |
|    download    |                                                   filename                                                    |                     Menyuruh browser untuk mengunduh pada URL yang terkait                      |
|      href      |                                                      URL                                                      |                      Menetapkan target ketika pengguna meng-klik hyperlink                      |
| referrerpolicy |             no-referrer, no-referrer-when-downgrade, origin, origin-when-cross-origin, unsafe-url             |                         Menetapkan referensi untuk dikirim pada target                          |
|      rel       | alternate, author, bookmark, external, help, license, next, nofollow, noreferrer, noopener, prev, search, tag |                Menetapkan hubungan antara halaman yang ditampilkan dengan target                |
|     target     |                                       \_blank, \_parent, \_self, \_top                                        | Menetapkan lokasi ketika membuka target contohnya pada sebuah tab, window, atau tab itu sendiri |
|     media      |                                                  media_type                                                   |                        Menetapkan tipe media yang digunakan pada target                         |

### 5. Emphasized Text

Gunakan elemen `<em>` untuk menunjukkan bagian kata yang perlu kita tekankan. Elemen ini menunjukkan _stress emphasis_ atau konten/kata yang perlu mendapatkan penekanan atau perhatian khusus.

Contoh:

---

<p><em>Oding</em> adalah seorang pelajar</p>
<p>Dia adalah seorang <em>pelajar</em></p>

---

```
<p><em>Oding</em> adalah seorang pelajar</p>
<p>Dia adalah seorang <em>pelajar</em></p>
```

### 6. Important Text

Gunakan elemen `<strong>` untuk menunjukkan sebuah teks yang begitu penting (strong importance), serius ataupun mendesak. Artinya, teks tersebut harus dapat perhatian lebih dari teks biasa lainnya.

Contoh:

---

<p>Kesehatan merupakan hal yang penting, jaga pola makan yang teratur dan <strong>jangan sampai makan tengah malam!</strong></p>

---

```
<p>Kesehatan merupakan hal yang penting, jaga pola makan yang teratur dan <strong>jangan sampai makan tengah malam!</strong></p>
```

### 7. Short Quotations

Gunakan elemen `<q>` untuk menandai sebuah kutipan dalam sebuah teks. Elemen ini berbeda dengan `<blockquote>`.

Contoh:

---

<p>Sebelum pulang kerja, ia berkata kepadaku: <q>Maaf saya tidak bisa hadir dalam pertemuan nanti</q></p>

---

```
<p>Sebelum pulang kerja, ia berkata kepadaku: <q>Maaf saya tidak bisa hadir dalam pertemuan nanti</q></p>
```

Elemen quotation marks memiliki atribut cite untuk menentukan sumber URL dari sebuah kutipan (jika kutipan tersebut bersumber dari sebuah situs website). Namun, tidak ada perbedaan yang terlihat secara kasat mata jika dijalankan di browser.

### 8. Citation

`<cite>` juga merupakan sebuah elemen yang digunakan untuk sebuah rujukan pada sebuah dokumen, contohnya sebuah buku, majalah, artikel, dan lainnya.

Contoh:

---

<p>Informasi selengkapnya bisa Anda dapatkan di <cite><a href="https://dicoding.com">dicoding.com</a></cite>.</p>

---

```
<p>Informasi selengkapnya bisa Anda dapatkan di <cite><a href="https://dicoding.com">dicoding.com</a></cite>.</p>
```

### 9. Defining Terms

Elemen `<dfn>` digunakan ketika mendefinisikan sebuah istilah (term).

Contoh:

---

<p><dfn>Website</dfn> merupakan halaman yang menampilkan informasi melalui teks atau gambar.</p>

---

```
<p><dfn>Website</dfn> merupakan halaman yang menampilkan informasi melalui teks atau gambar.</p>
```

### 10. Subscript dan Superscript

Subscript `<sub>` dan superscript `<sup>` adalah elemen yang dapat membuat teks yang ditampilkan tampak kecil, dengan posisi di bawah (sub) atau di atas (sup) dari teks biasanya.

Contoh:

---

<p>
  Sukrosa dengan rumus molekul C<sub>12</sub>H<sub>22</sub>O<sub>11</sub>.
</p>

<p>Salah satu persamaan paling umum dalam semua fisika adalah E=MC<sup>2</sup></p>

---

```
<p>
  Sukrosa dengan rumus molekul C<sub>12</sub>H<sub>22</sub>O<sub>11</sub>.
</p>

<p>Salah satu persamaan paling umum dalam semua fisika adalah E=MC<sup>2</sup></p>
```

### 11. Highlighted Text

Untuk menandai atau menyorot sebuah teks kita bisa menggunakan elemen `<mark>`.

Contoh:

---

<p>
  Ini adalah periode perang saudara. Pesawat ruang angkasa pemberontak, menyerang dari pangkalan
  tersembunyi, telah memenangkan kemenangan pertama mereka melawan Kekaisaran Galactic yang jahat.
  Selama pertempuran,
  <mark>mata-mata Pemberontak berhasil mencuri rencana rahasia </mark>
  ke senjata pamungkas Kekaisaran, STAR DEATH, stasiun ruang angkasa berlapis baja dengan kekuatan
  yang cukup untuk menghancurkan seluruh planet.
</p>

---

```
<p>
  Ini adalah periode perang saudara. Pesawat ruang angkasa pemberontak, menyerang dari pangkalan
  tersembunyi, telah memenangkan kemenangan pertama mereka melawan Kekaisaran Galactic yang jahat.
  Selama pertempuran,
  <mark>mata-mata Pemberontak berhasil mencuri rencana rahasia </mark>
  ke senjata pamungkas Kekaisaran, STAR DEATH, stasiun ruang angkasa berlapis baja dengan kekuatan
  yang cukup untuk menghancurkan seluruh planet.
</p>
```

### 12. Line Break

_Inline line break element_ (`<br>`) dapat digunakan untuk memberitahu browser untuk memberikan sebuah garis baru pada baris teks.

Contoh:

---

<p>
   Dicoding Space,<br>
   Jln. Batik Kumeli No. 50.<br>
   Bandung.<br>
   40123
</p>

---

```
<p>
   Dicoding Space,<br>
   Jln. Batik Kumeli No. 50.<br>
   Bandung.<br>
   40123
</p>
```

# Semantic HTML

### 1. Header dan Footer

Sebuah header dan footer utama yang muncul pada awal dan akhir di sebuah halaman (`<body>`).

- Header: pengantar atau pembuka konten dalam sebuah elemen `<article>` atau `<section>`.
- Footer: catatan kaki pada sebuah elemen `<article>` atau `<section>`.

Selain itu, elemen `<header>` dan `<footer>` dapat digunakan pada sebuah elemen `<article>` atau `<section>`. Header biasanya menampung judul dan penulis, footer dapat menampung sebuah link untuk membagikan artikel pada sebuah sosial media.

> Catatan bahwa elemen <header> dan <footer> tidak boleh ditulis di dalam elemen <header> dan <footer> lainnya (bertumpuk/nested).

### 2. Main

Element `<main>` digunakan untuk menampung/mewadahi konten utama (dominan) dalam `<body>`. Konten main dapat terdiri dari banyak section, ataupun artikel, atau konten apa pun di dalam elemen main, selama ia termasuk konten utama yang dimiliki oleh website.

> Karena elemen <main> berisi inti konten pada website, jangan gunakan elemen main lebih dari satu pada berkas HTML.

### 3. Nav

Elemen `<nav>` digunakan untuk menampung sebuah navigasi yang sifatnya penting (mayor), contohnya navigasi utama pada sebuah website.

Namun, tidak menjamin pada sebuah website hanya ada satu navigasi. Contohnya, sebuah akhir artikel pada blog terdapat tautan navigasi menuju artikel yang dianggap relevan dengan artikel yang telah kita baca. Navigasi tersebut tidak dianggap sebagai navigasi yang penting sehingga kita tidak perlu menggunakan elemen `<nav>` untuk menampilkannya.

Sebuah navigation pada dasarnya sangat berguna untuk aksesibilitas website kita. Contohnya ketika pengguna website kita menggunakan screen reader dalam mengunjungi website, pengguna akan mudah mencari bagian yang dia inginkan tanpa harus menelusuri seluruh konten website.

### 4. Articles

Elemen `<article>` bertindak sebagai container untuk independent content pada sebuah halaman, artinya konten utuh yang tidak terkait dengan konten lain, bisa saja sebuah artikel blog, komentar, forum post dan konten lainnya.

Jika dalam sebuah halaman terdapat beberapa artikel, tiap artikel tersebut seharusnya berada pada elemen `<article>`-nya masing-masing.

> Elemen <article> dapat berada pada elemen <article> lainnya (nested) selama artikel tersebut berkaitan dengan induk elemen <article> yang menampungnya.

### 5. Aside

Elemen `<aside>` memiliki dua tujuan, tergantung kita menempatkannya di dalam sebuah elemen `<article>` atau tidak.

Ketika elemen ini ditempatkan di dalam elemen `<article>`, elemen ini dapat berisi informasi yang berhubungan dengan artikel tersebut, tetapi bukan bagian dari konten artikelnya itu sendiri (dipisahkan dari konten utama).

Ketika ditempatkan di luar elemen `<article>`, elemen ini dapat berisi informasi yang berhubungan pada keseluruhan halaman.

Elemen `<aside>` biasanya terletak di samping dari sebuah elemen yang menampungnya.

### 6. Section

Sebuah elemen yang memiliki kesamaan konten dan sebuah heading di dalamnya dapat dikelompokkan dengan menggunakan elemen `<section>`. Dengan begitu elemen ini dapat digunakan pada sebuah elemen `<article>` yang memiliki konten panjang dan berpotensi untuk dikelompokkan.

Dalam sebuah `<section>` sebaiknya terdapat elemen heading (h1-h6), yang menjadi elemen pertama yang dituliskan pada sebuah section untuk menunjukkan judul atau tema dari bagian konten yang dikelompokkan.

# Generic Element

### 1. Div

Elemen `<div>` merupakan sebuah wadah (container) yang bersifat umum untuk menampung beberapa konten. Elemen ini tidak akan memberikan efek apa pun pada konten atau layout sebelum menerapkan sebuah style menggunakan CSS.

Elemen `<div>` tidak merepresentasikan apa pun sebagai sebuah wadah yang murni. Elemen ini lebih sering digunakan untuk mengelompokkan sebuah konten sehingga dapat memudahkan styling dengan menggunakan atribut class atau id.

### 2. Span

Elemen `<span>`, elemen ini memberikan manfaat yang sama seperti `<div>`, bedanya elemen ini digunakan sebagai phrase elements dan tidak terdapat line breaks ketika menggunakannya. Sederhananya, `<span>` merupakan sebuah `<div>` yang digunakan dalam sebuah baris teks yang dapat diwadahi oleh paragraf, list, heading, atau lainnya.

# Tabel

Elemen `<table>` pada HTML merepresentasikan data tabular, yaitu informasi yang disajikan dalam sebuah tabel. Tabel sendiri disajikan dalam dua dimensi terdiri dari baris dan kolom (_cell_) yang berisikan sebuah data.

Tabel pada HTML disusun dari tiga buah elemen, yaitu `<table>`, `<tr>` dan `<td>` atau `<th>`. Elemen `<table>` digunakan untuk menandakan dimulainya dan diakhirinya sebuah konten tabel dan juga sebagai wadah untuk tabel itu sendiri. Kemudian elemen `<tr>` digunakan untuk membuat sebuah baris baru yang di dalamnya terdapat elemen `<td>` atau `<th>` sehingga menghasilkan sebuah sel.

Elemen `<td>` berarti _“table data”_. Selain membuat sel, elemen ini juga merupakan tempat menampung data pada tabel, dan elemen `<th>` atau _“table header”_ digunakan untuk menentukan sebuah header pada kolom datanya.

Contoh:

---

<h1>Pemenang Piala Dunia Tiga Tahun Terakhir</h1>

<table>
  <tr>
    <th>Tahun</th>
    <th>Juara 1</th>
    <th>Juara 2</th>
    <th>Juara 3</th>
  </tr>
  <tr>
    <td>2018</td>
    <td>Prancis</td>
    <td>Kroasia</td>
    <td>Belgium</td>
  </tr>
  <tr>
    <td>2014</td>
    <td>Jerman</td>
    <td>Argentina</td>
    <td>Belanda</td>
  </tr>
  <tr>
    <td>2010</td>
    <td>Spanyol</td>
    <td>Belanda</td>
    <td>Jerman</td>
  </tr>
</table>

---

```
<h1>Pemenang Piala Dunia Tiga Tahun Terakhir</h1>

<table>
  <tr>
    <th>Tahun</th>
    <th>Juara 1</th>
    <th>Juara 2</th>
    <th>Juara 3</th>
  </tr>
  <tr>
    <td>2018</td>
    <td>Prancis</td>
    <td>Kroasia</td>
    <td>Belgium</td>
  </tr>
  <tr>
    <td>2014</td>
    <td>Jerman</td>
    <td>Argentina</td>
    <td>Belanda</td>
  </tr>
  <tr>
    <td>2010</td>
    <td>Spanyol</td>
    <td>Belanda</td>
    <td>Jerman</td>
  </tr>
</table>
```

## Spaning Cell

Spanning cell, yang artinya menjangkau atau merentangkan sebuah ukuran sel lebih dari ukuran yang biasanya. Dengan spanning cell, kita dapat membuat sebuah tabel yang lebih kompleks, tetapi akan membuat markup yang kita tulis menjadi sedikit sulit dibaca.

### Column Span

Untuk merentangkan sebuah kolom (_column spanning_) kita bisa menggunakan atribut `colspan` pada elemen `<td>` atau `<th>`.

Contoh:

---

<table border="1">
  <tr>
    <th>18:00</th>
    <th>19:00</th>
    <th>20:00</th>
  </tr>
  <tr>
    <td colspan="2">Avenger Infinity Wars</td>
    <td>It Chapter 2</td>
  </tr>
  <tr>
    <td>One Piece: Stampede</td>
    <td>Weathering With You</td>
    <td>Gundala</td>
  </tr>
  <tr>
    <td>Gundala</td>
    <td colspan="2">Avenger Infinity Wars</td>
  </tr>
</table>

---

```
<table border="1">
  <tr>
    <th>18:00</th>
    <th>19:00</th>
    <th>20:00</th>
  </tr>
  <tr>
    <td colspan="2">Avenger Infinity Wars</td>
    <td>It Chapter 2</td>
  </tr>
  <tr>
    <td>One Piece: Stampede</td>
    <td>Weathering With You</td>
    <td>Gundala</td>
  </tr>
  <tr>
    <td>Gundala</td>
    <td colspan="2">Avenger Infinity Wars</td>
  </tr>
</table>
```

### Row Span

Untuk merentangkan sebuah baris (_row spanning_) kita dapat menggunakan atribut `rowspan`. Mirip seperti column spanning, tetapi atribut ini akan merentangkan sebuah sel ke bawah.

Contoh:

---

<table border="1">
  <tr>
    <th rowspan="3">18:00</th>
    <td>Avenger Infinity Wars</td>
  </tr>
  <tr>
    <td>One Piece: Stampede</td>
  </tr>
  <tr>
    <td>Gundala</td>
  </tr>
</table>

---

```
<table border="1">
  <tr>
    <th rowspan="3">18:00</th>
    <td>Avenger Infinity Wars</td>
  </tr>
  <tr>
    <td>One Piece: Stampede</td>
  </tr>
  <tr>
    <td>Gundala</td>
  </tr>
</table>
```

# Form / Input User

Elemen `<input>` merupakan elemen yang sangat sering dipakai untuk mendapatkan data dari user. Ada banyak sekali tipe-tipe input selengkapnya ada di tabel berikut.

|  **Input Type**  |                                                                      **Keterangan**                                                                      |
| :--------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      `text`      |                                      Input teks yang berisi satu baris. Ini adalah tipe default dari input elemen.                                       |
|     `number`     |                                                     Input teks yang hanya mengizinkan format angka.                                                      |
|    `password`    |                                    Sama seperti input text, tetapi setiap karakter akan ditampilkan sebagai bintang.                                     |
|     `email`      |                                        Sama seperti teks biasa, tetapi input ini dikhususkan untuk format email.                                         |
|     `search`     |            Input untuk melakukan pencarian berdasarkan kata kunci. Input ini memiliki ikon ✕ di tepi kanan elemen untuk melakukan clear text.            |
|      `date`      |                          Untuk mengambil data tanggal. Tipe ini akan menyediakan popup penanggalan untuk mempermudah pengisian.                          |
|      `time`      |                            Menentukan waktu (jam) yang ingin user isi. Tipe input ini juga akan menampilkan visual dari jam.                             |
| `datetime-local` |                                             Sama seperti tipe date, tetapi ia menambahkan data waktu (jam).                                              |
|    `checkbox`    |                                              Di-render sebagai sebuah kotak yang dapat dicek untuk active.                                               |
|     `radio`      | Digunakan untuk melakukan pemilihan dari sekian opsi (radio button) yang ada. Untuk melakukannya, input ini akan dikelompokkan dalam sebuah radio group. |
|     `range`      |                                           Menentukan nilai angka berdasarkan jangkauan nilai yang ditentukan.                                            |
|     `color`      |               User dapat menentukan warna dengan tipe ini, baik menggunakan color picker atau memasukkan format nilai warna secara manual.               |
|      `file`      |                                        Melakukan input satu atau lebih berkas dari penyimpanan data perangkatnya.                                        |
|     `submit`     |   Input yang di-render sebagai tombol submit. Jika tombol ini ditekan, formulir akan ter-submit dan dikirimkan ke tujuan pengiriman (atribut action).    |
|     `hidden`     |              Biasanya, tipe ini tidak terlihat oleh user. Namun, input ini akan sangat berguna bagi developer untuk memasukkan suatu data.               |

Adapun atribut dalam elemen input adalah sebagai berikut.

| Atribut        | Tipe                                                                  | Deskripsi                                                                                                                                                                                                       |
| -------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`         | semua tipe                                                            | Menamai elemen input. Data yang diisikan oleh user akan dikirimkan saat formulir di-submit. Atribut ini memiliki peran yang sangat penting. Jika tidak menyertakannya, data input tidak akan dikirim ke server. |
| `placeholder`  | text, search, url, tel, email, password, number                       | Teks “samar” yang muncul pada kolom input. Teks ini biasanya digunakan sebagai petunjuk atau contoh data yang perlu diisi.                                                                                      |
| `required`     | semua tipe, kecuali hidden, range, color, dan button                  | Atribut ini menyebabkan elemen input wajib diisi untuk di-submit. Ia merupakan atribut boolean.                                                                                                                 |
| `value`        | semua tipe, kecuali image                                             | Memberikan data awal atau default pada elemen input.                                                                                                                                                            |
| `autocomplete` | semua tipe, kecuali checkbox, radio, dan button                       | Fitur melengkapi input secara otomatis. Biasanya, ini terjadi ketika kita pernah meng-input sesuatu dan pada kesempatan berikutnya, data tersebut akan ditampilkan lagi oleh browser sebagai autocomplete.      |
| `maxlength`    | text, search, url, tel, email, password                               | Menentukan maksimal panjang karakter yang diperbolehkan pada kolom input.                                                                                                                                       |
| `max`          | date, month, week, time, datetime-local, number, range                | Menentukan maksimal nilai yang diperbolehkan.                                                                                                                                                                   |
| `minlength`    | text, search, url, tel, email, password                               | Menentukan minimal panjang karakter yang diperbolehkan pada kolom input.                                                                                                                                        |
| `min`          | date, month, week, time, datetime-local, number, range                | Menentukan minimal nilai yang diperbolehkan.                                                                                                                                                                    |
| `checked`      | checkbox, radio                                                       | Mengaktifkan atau mencentangkan input checkbox.                                                                                                                                                                 |
| `accept`       | file                                                                  | Panduan atau batasan format berkas apa yang diperbolehkan pada input berkas.                                                                                                                                    |
| `multiple`     | email, file                                                           | Memungkinkan pemilihan ganda pada elemen input.                                                                                                                                                                 |
| `pattern`      | text, search, url, tel, email, password                               | Menentukan pola yang wajib dipatuhi pada data yang diisi agar dapat valid.                                                                                                                                      |
| `readonly`     | semua tipe, kecuali hidden, range, color, checkbox, radio, dan button | Tidak memiliki akses edit nilai.                                                                                                                                                                                |
| `disabled`     | semua tipe                                                            | Memberikan efek tidak aktif pada elemen input.                                                                                                                                                                  |

### Text Area

HTML memiliki elemen khusus yang memungkinkan user menuliskan teks dalam banyak baris. Mari kita berkenalan dengan `<textarea>`. Elemen `<textarea>` ini berbeda dengan elemen input sebelumnya. Selain nama elemen yang menjadi pembeda, elemen textarea memiliki tag penutup agar dapat berfungsi dengan baik.

Contoh:

---

<textarea rows="6" cols="16">
Belajar
Dasar
Pemrograman
Web
</textarea>

---

```
<textarea rows="6" cols="16">
Belajar
Dasar
Pemrograman
Web
</textarea>
```

### Label

Ada banyak sekali keuntungan jika memberikan keterangan–dengan kata lain, kita bisa menyebutnya caption–pada masing-masing elemen input. Tidak hanya elemen input, elemen lainnya seperti textarea juga perlu disandingkan dengan elemen label.

Beberapa keuntungan penerapan label untuk elemen input sebagai berikut.

- Elemen input yang berasosiasi dengan elemen label akan memberikan kemampuan bagi screen reader untuk menjelaskan fungsi dari elemen input tersebut. Dalam hal ini, ia akan meningkatkan aksesibilitas. Tentunya, ini akan sangat bermanfaat bagi penyandang disabilitas.
- Memberikan kemampuan bagi browser untuk mengalihkan langsung pada elemen input saat elemen label yang berasosiasi dengannya ditekan atau klik.

Contoh:

---

<div>
  <label for="email">Email</label>
  <br>
  <input type="email" id="email" />
</div>

<div>
  <label for="password">Password</label>
  <br>
  <input type="password" id="password" />
</div>

---

```
<div>
  <label for="email">Email</label>
  <br>
  <input type="email" id="email" />
</div>

<div>
  <label for="password">Password</label>
  <br>
  <input type="password" id="password" />
</div>
```

# Spesial Karakter

Ada beberapa karakter spesial seperti copyright symbol (©) yang tidak termasuk ke dalam standar kelompok ASCII characters. ASCII characters hanya menyediakan karakter seperti huruf, nomor, dan beberapa simbol dasar lainnya. Karakter lain, seperti lebih besar dari (>) atau lebih kecil dari (<), tidak dapat digunakan secara langsung sebagai konten pada HTML meskipun tersedia dalam ASCII character. Hal ini karena karakter tersebut akan terbaca sebagai sebuah tag.

Ada dua cara untuk melakukannya, yakni menetapkan nilai numerik (_numeric entity_) atau menggunakan nama singkatan yang sudah ditetapkan untuk masing-masing karakternya (_named entity_). Semua referensi karakter dimulai dengan “&” dan diakhiri dengan “;”.

Contoh:

```
<p>Belajar Dasar Pemrograman Web &copy; 2024, Dicoding</p>
<p>Belajar Dasar Pemrograman Web &#169; 2024, Dicoding</p>
```

Hasilnya akan sama seperti berikut:

---

<p>Belajar Dasar Pemrograman Web &copy; 2024, Dicoding</p>
<p>Belajar Dasar Pemrograman Web &#169; 2024, Dicoding</p>

---

Adapun referensinya adalah sebagai berikut.
| Karakter | Deskripsi | Named Entity | Numeric Entity |
|----------|-----------------------------------------|--------------|----------------|
| ` ` | Non-breaking space | `&nbsp;` | `&#160;` |
| `&` | Ampersand | `&amp;` | `&#038;` |
| `'` | Apostrophe | `&apos;` | `&#039;` |
| `<` | Kurang dari (less-than) | `&lt;` | `&#060;` |
| `>` | Lebih dari (greater-than) | `&gt;` | `&#062;` |
| `©` | Hak cipta (copyright) | `&copy;` | `&#169;` |
| `®` | Merek dagang terdaftar (registered trademark) | `&reg;` | `&#174;` |
| `™` | Merek dagang (trademark) | `&trade;` | `&#8482;` |
| `£` | Pound | `&pound;` | `&#163;` |
| `¥` | Yen | `&yen;` | `&#165;` |
| `€` | Euro | `&euro;` | `&#8364;` |
| `–` | En-dash | `&ndash;` | `&#8211;` |
| `—` | Em-dash | `&mdash;` | `&#8212;` |
| `‘` | Kutip tunggal kiri | `&lsquo;` | `&#8216;` |
| `’` | Kutip tunggal kanan | `&rsquo;` | `&#8217;` |
| `“` | Kutip ganda kiri | `&ldquo;` | `&#8220;` |
| `”` | Kutip ganda kanan | `&rdquo;` | `&#8221;` |
| `•` | Bullet | `&bull;` | `&#8226;` |
| `...` | Horizontal ellipsis | `&hellip;` | `&#8230;` |
