# List

Pada HTML terdapat tiga tipe list.

1. Unordered lists: daftar yang ditampilkan tidak memiliki urutan. Penulisan menggunakan tag `<ul><li> ... </li></ul>`.
2. Ordered lists: daftar yang ditampilkan secara terurut. Penulisan menggunakan tag `<ol><li> ... </li></ol>`. Berikut adalah nilai-nilai yang dapat digunakan pada atribut type pada elemen `<ol>`.
   a. `1` : Menggunakan angka dalam urutan item (default).
   b. `a` : Menggunakan huruf kecil dalam urutan item.
   c. `A` : Menggunakan huruf besar dalam urutan item.
   d. `i` : Menggunakan huruf romawi kecil dalam urutan item.
   e. `I` : Menggunakan huruf romawi besar dalam urutan item.
3. Description lists: daftar yang terbuat dari beberapa istilah diikuti dengan deskripsi dari istilah tersebut.

# Gambar

Pada HTML untuk menampilkan sebuah gambar kita bisa menggunakan tag `<img>`. Berbeda dengan elemen lain, elemen `<img>` tidak menuliskan konten di antara tag pembuka dan tag penutup. Namun, untuk menetapkan gambar yang ditampilkan kita gunakan sebuah atribut. Contohnya berikut.

<img src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/dicoding-logo.jpg" alt="Dicoding Logo" width="250" />

`<img src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/dicoding-logo.jpg" alt="Dicoding Logo" width="250" />`

Dari kode di atas terdapat dua attributes yang harus kita gunakan ketika menerapkan elemen `<img>`.

1. `src` : Atribut ini berfungsi sebagai sumber dari gambar yang ditampilkan. Atribut ini dapat bernilai url gambar atau path gambar local dari gambar yang digunakan.
2. `alt` : Atribut ini sebenarnya tidak wajib untuk diterapkan, hanya saja atribut ini akan sangat berguna ketika gambar tidak berhasil ditampilkan. Nilai atribut ini merupakan tampilan dari gambar yang ditampilkan dalam bentuk tulisan. Jadi, ketika gambar gagal ditampilkan akan memunculkan teks alternatif yang dapat mewakili arti dari gambar tersebut.

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

### Long Quotations

Jika memiliki sebuah kutipan ataupun sebuah testimonial, dapat gunakan format long quotations dengan menggunakan tags `<blockquote>`. Konten di dalam elemen `<blockquote>` ini dapat berupa sebuah paragraf, heading, ataupun list.

<blockquote cite="https://id.wikipedia.org/wiki/Situs_web">
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>

```
<blockquote>
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>
```
