# Selector Dasar

Ada banyak jenis selector untuk menargetkan aturan ke elemen tertentu dalam dokumen HTML.

### 1. Type Selector

Type Selector menggunakan nama elemen sebagai target untuk diterapkannya rule. Dalam kata lain, ketika menggunakan selector ini tentu rule akan diterapkan pada seluruh elemen target yang ada pada dokumen HTML.

| index.html |
| ---------- |

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Judul Dokumen</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <span>
      Ini merupakan sebuah teks yang berada pada elemen span. Seharusnya elemen ini ditampilkan dengan warna teks merah.
    </span>
    <p>
      Ini merupakan sebuah teks yang berada pada elemen paragraf, teks ini tidak seharusnya tidak akan terpengaruh oleh rule.
    </p>
    <span>
      Ini merupakan sebuah teks yang berada pada elemen span lainnya. Seharusnya elemen ini ditampilkan dengan warna teks merah juga.
    </span>
  </body>
</html>
```

| style.css |
| --------- |

```
/* Semua elemen span */
span {
    color: red;
}
```

Hasil di atas akan membuat teks yang berada pada setiap elemen `<span>` akan berwarna merah.

### 2. Class Selector

Class selector menetapkan target elemen berdasarkan nilai dari atribut class yang diterapkan pada elemennya. Untuk penulisan selector-nya diawali dengan tanda titik (.) dan dilanjutkan dengan nama class-nya.

> Class bersifat shareable sehingga dapat diterapkan pada banyak elemen dengan tipe elemen yang berbeda-beda.

```
<h1 class="red">Heading dengan teks berwarna merah</h1>
<p class="red">Paragraf dengan teks berwarna merah</p>
```

Tidak hanya itu, sebuah elemen juga memungkinkan memiliki banyak nilai class sehingga kita dapat menerapkan lebih dari satu rule atau gabungan rule pada elemen target. Untuk menggunakannya, pada atribut class kita cukup tuliskan nama kelasnya dan dipisahkan dengan spasi untuk tiap nilai kelasnya.

```
<h1 class="red skyblue-bg">Heading dengan teks berwarna merah dan background biru langit</h1>
<p class="red fancy">Paragraf dengan teks berwarna merah dan bergaya fancy</p>
```

### 3. ID Selector

ID selector menetapkan target elemen berdasarkan nilai dari atribut id yang diterapkan pada elemennya. Mirip dengan class, atribut id dapat diterapkan pada seluruh elemen HTML dan kebanyakan atribut ini digunakan untuk memberikan sebuah arti pada generic element, seperti `<div>` dan `<span>`. Namun, atribut id ini tidak bersifat shareable. Artinya, nilai id harus unik dan digunakan pada satu elemen saja.

Untuk menetapkan selector dengan menggunakan id, kita gunakan tanda octothorpe (#) atau lebih familiar disebut dengan hash.

| index.html |
| ---------- |

```
  <body>
    <div id="special">
      <p>Ini merupakan konten di dalam sebuah div yang diberi id special.</p>
    </div>
    <div>
      <p>Ini merupakan konten di dalam sebuah div biasa.</p>
    </div>
  </body>
```

| style.css |
| --------- |

```
#special {
  background-color: skyblue;
}
```

> Hal yang harus ditekankan lagi adalah id ini bersifat unik. Jika ingin menerapkan sebuah rule pada banyak elemen, sebaiknya gunakan atribut class dibandingkan dengan id.

### 4. Attribute Selector

Attribute selector merupakan cara menetapkan target elemen berdasarkan sebuah atribut yang digunakan atau bahkan bisa lebih spesifik dengan nilainya.

| index.html |
| ---------- |

```
  <body>
    <ul>
      <li><a href="#internal">Internal link</a></li>
      <li><a href="http://example.com">Example link</a></li>
      <li><a href="#InSensitive">Insensitive internal link</a></li>
      <li><a href="http://example.org">Example org link</a></li>
    </ul>
  </body>
```

| style.css |
| --------- |

```
ul {
  font-size: 18px;
}

/* <a> element yang menerapkan href attribute */
a[href] {
  color: blue;
}

/* <a> element yang menerapkan nilai pada href dengan awalan "#" */
a[href^='#'] {
  background-color: gold;
}

/* <a> element yang menerapkan nilai pada href yang mengandung teks "example" */
a[href*='example'] {
  background-color: silver;
}

/* <a> element yang menerapkan nilai pada href yang mengandung teks "insensitive" tidak mementingkan huruf kapital*/
a[href*='insensitive' i] {
  color: cyan;
}

/* <a> element yang menerapkan nilai pada href dengan akhiran ".org" */
a[href$='.org'] {
  color: red;
}
```

kondisi yang dapat diterapkan pada attribut selector.

| Syntax          | Description                                                                              |
| --------------- | ---------------------------------------------------------------------------------------- |
| `[attr]`        | Menargetkan elemen yang menerapkan atribut attr.                                         |
| `[attr=value]`  | Menargetkan elemen yang menerapkan atribut attr dengan nilai value.                      |
| `[attr~=value]` | Menargetkan elemen yang menerapkan atribut attr dan salah satu nilainya adalah value.    |
| `[attr^=value]` | Menargetkan elemen yang menerapkan atribut attr dan nilainya diawali dengan nilai value. |
| `[attr$=value]` | Menargetkan elemen yang menerapkan atribut attr dan nilainya diakhiri dengan value.      |
| `[attr*=value]` | Menargetkan elemen yang menerapkan atribut attr dan nilainya mengandung value.           |

### 5. Universal Selector

Universal selector digunakan untuk diterapkan pada seluruh elemen. Namun, selector ini juga bisa secara spesifik menargetkan sebuah elemen dengan menggabungkannya bersama selector yang lain.

| index.html |
| ---------- |

```
  <body>
    <p>
      Ini merupakan paragraf biasa atau tidak menerapkan atribut apapun. Maka
      teks pada paragraf ini akan berwarna hijau
    </p>
    <p lang="en-us">
      This is an English paragraph contains en-us value of lang attribute, so
      this text will be green and italic.
    </p>

    <h1>Ini merupakan sebuah header biasa</h1>
    <h1 lang="en-us">This is an English Header</h1>

    <p class="warning">
      Perhatikan paragraf ini! Paragraf ini merupakan paragraf yang memiliki
      kelas bernilai warning, sehingga teks dari paragraf ini akan berwarna
      merah
    </p>

    <div id="content">
      <p>
        Ini merupakan sebuah teks di dalam sebuah div yang memiliki id bernilai
        "content", seharusnya paragraf ini dibungkus dalam border yang memiliki
        padding 20px
      </p>
    </div>
  </body>
```

| style.css |
| --------- |

```
/* Menargetkan seluruh tipe elemen */
* {
  color: green;
}

/* Menargetkan seluruh tipe elemen yang mengandung nilai "en" pada atribut lang */
*[lang^='en'] {
  font-style: italic;
}

/* Menargetkan seluruh tipe elemen yang memiliki nilai "warning" pada atribut class */
*.warning {
  color: red;
}

/* Menargetkan seluruh tipe elemen yang memiliki nilai "content" pada atribut id */
*#content {
  border: 1px solid blue;
  padding: 20px;
}
```

# Combinators

Ada empat kombinator yang dapat kita gunakan, yaitu Adjacent Sibling Selector, General Sibling Selector, Child Selector, dan Descendant Selector.

### 1. Adjacent Sibling Selector (+)

**Adjacent Sibling Selector** menggabungkan dua buah basic selector dengan menggunakan tanda + di antara keduanya. **Adjacent Sibling Selector** terdiri dari dua buah target elemen, tetapi hanya elemen kedua yang menerapkan rule selama elemen tersebut dituliskan langsung setelah elemen pertama pada berkas HTML. Selain itu, kedua elemen tersebut harus berada dalam induk elemen yang sama.

```
/* Rule akan diterapkan pada elemen paragraf yang berada tepat setelah elemen img */
img + p {
  color: green;
}
```

### 2. General Sibling Selector (~)

Mirip seperti Adjacent Sibling Selector, tetapi rules akan diterapkan pada seluruh elemen kedua yang berada setelah elemen pertama selama masih memiliki induk yang sama, walaupun posisi dari elemen kedua tidak berada tepat setelahnya. General Sibling Selector menggunakan simbol tilda (~) untuk menetapkan elemennya.

```
img ~ p {
  color: green;
}
```

> Rule di atas akan diterapkan pada elemen paragraf yang berada setelah elemen img selama masih di dalam induk yang sama.

### 3. Child Selector (>)

Child Selector menggabungkan dua buah basic selector dengan menggunakan tanda greater than (>) di antara basic selectornya.

```
div > p {
  background-color: yellow;
}
```

Sebagaimana contoh di atas, CSS rule akan diterapkan pada seluruh elemen paragraf yang berada dalam elemen div secara langsung. Dalam arti lain, elemen paragraf merupakan child dari elemen div, bukan hanya sebuah turunannya.

### 4. Descendant Selector (space)

Descendant Selector mirip seperti child selector, tetapi hierarkinya lebih luas karena rule akan diterapkan pada seluruh elemen yang menjadi turunannya walaupun secara tidak langsung. Basic selector pertama yang dituliskan pada selector ini menjadi induknya dan basic selector yang kedua akan menerapkan rule. Selector ini menggunakan spasi dalam menggabungkan dua basic selector.

```
div p {
  background-color: yellow;
}
```

# Pseudo Selector

### 1. Pseudo-class Selector

Pseudo-class merupakan sebuah class “semu” yang sebenarnya ada pada tiap elemen HTML. Untuk menggunakan pseudo-class, kita gunakan tanda titik dua (:) pada basic selector dan diikuti dengan pseudo-class-nya.

| index.html |
| ---------- |

```
  <body>
    <p>
      Dapatkan pekerjaan impian di
      <a target="_blank" href="https://jobs.dicoding.com/">
        Dicoding Jobs
      </a>.
    </p>
  </body>
```

| style.css |
| --------- |

```
/* rule akan diterapkan pada sebuah tautan yang belum pernah dikunjungi */
a:link {
   color: red;
}

/* rule akan diterapkan pada sebuah tautan yang sudah pernah dikunjungi */
a:visited {
   color: green;
}

/* rule akan diterapkan pada sebuah tautan ketika diarahkan dengan kursor */
a:hover {
   color: pink;
}

/* rule akan diterapkan pada sebuah tautan ketika ditekan */
a:active {
   color:orange;
}
```

### 2. Pseudo-elemen Selector

Pseudo-element merupakan sebuah elemen “semu” yang sebenarnya ada, tetapi tidak tampak secara tertulis pada berkas HTML. Selector ini biasa digunakan ketika kita ingin menambahkan konten tepat sebelum dan setelah sebuah elemen paragraf. Pseudo-element yang dimaksud adalah `::before` dan `::after`.

| index.html |
| ---------- |

```
  <body>
    <blockquote>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut eius error
      explicabo ipsum molestiae necessitatibus nesciunt possimus reprehenderit sed
      voluptates. Aliquam aspernatur autem est nobis officia praesentium quas
      recusandae rem.
    </blockquote>
  </body>
```

| style.css |
| --------- |

```
blockquote::before,
blockquote::after {
  content: '"';
  font-size: 24px;
  font-style: italic;
  font-weight: bold;
}
```

Pseudo-element tidak hanya `::before` dan `::after`. Ada pseudo-element lainnya yang dapat menentukan rule pada awal karakter konten elemen.

| index.html |
| ---------- |

```
  <body>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto
      deserunt, dicta laudantium quae quam sequi soluta vitae! A, architecto
      beatae, consequuntur et eveniet fuga laudantium molestias praesentium
      temporibus, unde velit.
    </p>
  </body>
```

| style.css |
| --------- |

```
/* Rule styling akan diterapkan pada karakter pertama di sebuah paragraf */
p::first-letter {
  font-size: 32px;
  font-weight: bold;
  color: saddlebrown;
}
```

# Formating Text

## 1. Font Styling

### 1. Font-family

```
p {
    font-family: Arial, Verdana, sans-serif;
  }
```

- Seluruh nilai font yang bukan merupakan generic font families harus dituliskan secara kapital. Contohnya, “Arial” bukan dituliskan “arial”.
- Gunakan tanda koma (,) untuk memisahkan antara nilai font yang digunakan.
- Selalu tanda kutip (“) untuk membungkus nilai font yang memiliki spasi pada namanya. Contohnya “Open Sans”.

Mungkin kita bertanya-tanya mengapa perlu memberikan lebih dari satu nilai pada font-family? Hal tersebut penting karena tidak semua browser mendukung semua jenis font. Jadi, menambahkan lebih dari satu nilai font dapat memberikan alternatif pada browser dalam menampilkan font jika font utama yang diterapkan tidak didukung oleh browser.

Berikut adalah nilai-nilai generic font families yang dapat kita gunakan untuk fallback mechanism.

- `Serif`: jenis font yang memiliki runcing pada garis akhir karakternya. Times New Roman merupakan salah satu jenis serif font.
- `Sans-serif`: jenis font yang tidak meruncing pada garis akhir karakternya. Contohnya, “Open Sans”, “Fira Sans” dan lainnya.
- `Monospace`: jenis font yang memiliki nilai lebar tiap karakternya sama. Consolas merupakan salah satu jenisnya.
- `Cursive`: jenis font yang tampak seperti handwriting atau hasil tulisan tangan.
- `Fantasy`: jenis font yang merepresentasikan karakteristik yang menyenangkan.
- `System-ui`: jika menerapkan nilai ini maka font yang diterapkan akan sama seperti font yang digunakan pada sistem operasi kita.
- `Math`: jenis font yang digunakan untuk penulisan rumus-rumus matematika.
- `Emoji`: jenis font yang digunakan untuk menampilkan emoji.
- `Fangsong`: jenis font yang menampilkan gaya penulisan Chinese.

> Untuk CSS memiliki fitur yang digunakan untuk memasukkan font eksternal ke dalam CSS, yakni menggunakan @font-face.
>
> ```
> @font-face {
>   font-family: "Dicoding Font";
>   src: url('FILE-FONT.TTF');
> }
> ```

### 2. Font-size

```
h1 {
  font-size: 1.5em;
}
```

Satuan dalam menetapkan ukuran font terbagi dua jenis.

#### 1. Relative Unit

Satuan yang nilainya tergantung pada suatu hal. Contohnya, ukuran viewport, induk elemen, atau ukuran teks standar.

| Satuan | Relative to     | Fungsi                                                                                                                                         |
| ------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `em`   | Font size       | Satuan relatif terhadap ukuran font yang sedang digunakan pada elemen (contohnya, 2em berarti 2 kali lebih besar dari ukuran font seharusnya). |
| `ex`   | Font height     | Satuan relatif terhadap tinggi font saat ini, satuan ini sangat jarang sekali digunakan.                                                       |
| `rem`  | Font size       | Mirip seperti `em`, tetapi `rem` merupakan satuan relatif terhadap ukuran font dari root element.                                              |
| `ch`   | Font width      | Satuan relatif terhadap lebar dari karakter “0” nol.                                                                                           |
| `vw`   | Viewport width  | Satuan relatif terhadap 1% lebar viewport. Contoh 1vw = 1% dari lebar viewport. Satuan ini tidak didukung pada browser IE8 ke bawah.           |
| `vh`   | Viewport height | Satuan relatif terhadap 1% tinggi viewport. Contoh 1vh = 1% dari tinggi viewport. Satuan ini tidak didukung pada browser IE8 ke bawah.         |

#### 2. Absolute Unit

Satuan yang nilainya telah ditentukan atau digunakan dalam dunia nyata.

| Satuan | Fungsi                                                          |
| ------ | --------------------------------------------------------------- |
| `px`   | Menetapkan nilai font berdasarkan ukuran pixel.                 |
| `pt`   | Menetapkan nilai font berdasarkan points (1/72 inch di CSS2.1). |
| `pc`   | Menetapkan nilai font berdasarkan picas (1 pica = 12 point).    |
| `mm`   | Menetapkan nilai font berdasarkan millimeters.                  |
| `cm`   | Menetapkan nilai font berdasarkan centimeters.                  |
| `in`   | Menetapkan nilai font berdasarkan inches.                       |

Selain dengan menetapkan nilai dan satuannya secara langsung, kita juga bisa menggunakan nilai persentase untuk mengatur ukuran font.

```
body {
  font-size: 16px;
}

h1 {
  font-size: 150%; /* 150% dari 16 = 24px */
}
```

kita juga bisa menentukan ukuran font dengan menuliskan kata kunci secara spesifik yang tersedia pada CSS. Kata kunci tersebut: xx-small, x-small, small, medium, large, x-large, dan xx-large.

### 3. Font Weight

Font-weight yang digunakan untuk mengatur ketebalan dari font yang ditampilkan. Nilai dari properti ini dapat ditentukan dengan menggunakan numeric values (100 sampai 900) atau dengan menggunakan descriptive terms (normal, bold, bolder, dan lighter).

### 4. Font-style

Font-style digunakan untuk menentukan postur dari teks yang ditampilkan, yakni bentuknya vertikal (normal) atau miring (italic dan oblique).

Italic dan oblique keduanya menampilkan teks yang miring. Perbedaannya adalah italic menerapkan tipe miring (italic font version) dari suatu font sedangkan oblique adalah font normal yang hanya dibuat miring.

Properti font-style dapat diaplikasikan ke seluruh elemen yang ada di HTML dan nilainya dapat diturunkan pada elemen turunannya.

### 5. Font-variant

Kita yang terbiasa dengan aplikasi document editor seperti Microsoft Word tentu tahu atau sudah mencoba fitur small caps. Fitur ini dapat membuat teks menjadi kapital tetapi dituliskan secara kecil dan merapat.

### 6. Shorthand

Menspesifikasikan masing-masing nilai properti font akan menghasilkan banyak sekali kode repetitif. CSS memiliki properti CSS yang biasa disebut dengan shorthand properti. Ia memberikan suatu “jalan pintas” untuk menuliskan properti-properti tersebut ke dalam satu properti, yaitu font.

Dengan menggunakan properti font, kita dapat menuliskan beberapa properti hanya dalam satu properti pada satu rule.

```
target {
  `font`: style weight variant size font-family;
}
```

## 2. Text Styling

### 1. Line Height

Properti line-height digunakan untuk mengatur jarak minimal dari garis dasar ke garis dasar dalam menampilkannya teks pada halaman.

### 2. Text Indent

Kita dapat menentukan nilai properti ini melalui perhitungan panjang dalam px, em, dan in atau bisa menggunakan nilai persentase (%). Nilai persentase dihitung berdasarkan lebar dari induk elemen. Berikut contoh penggunaannya.

### 3. Text Alignment

Berikut adalah nilai yang dapat digunakan pada properti text-align.

| Nilai Properti      | Fungsi                                                          |
| ------------------- | --------------------------------------------------------------- |
| text-align: left    | Membuat perataan teks pada ujung kiri.                          |
| text-align: right   | Membuat perataan teks pada ujung kanan.                         |
| text-align: center  | Membuat perataan teks secara menengah.                          |
| text-align: justify | Membuat perataan teks yang setara pada ujung kiri dan kanannya. |

### 4. Text Decoration

Beberapa nilai lain yang dapat kita gunakan untuk properti ini.

| Nilai properti                | Fungsi                                            |
| ----------------------------- | ------------------------------------------------- |
| text-decoration: underline    | Memberikan garis bawah (underline) pada teks.     |
| text-decoration: overline     | Memberikan garis atas (overline) pada teks.       |
| text-decoration: line-through | Memberikan efek tulisan dicoret (strikethrough).  |
| text-decoration: none         | Menghilangkan dekorasi teks yang ada pada elemen. |

### 5. Text Transform

Properti ini dapat berisikan nilai sebagai berikut.

| Nilai Properti             | Fungsi                                              |
| -------------------------- | --------------------------------------------------- |
| text-transform: none       | Teks yang ditampilkan sama seperti yang dituliskan. |
| text-transform: capitalize | Membuat huruf pertama besar pada tiap katanya.      |
| text-transform: lowercase  | Membuat seluruh teks menggunakan huruf kecil.       |
| Text-transform: uppercase  | Membuat seluruh teks menggunakan huruf besar.       |

### 6. Word and Letter Spacing

Properti selanjutnya yang bisa kita gunakan untuk memformat teks adalah letter-spacing dan word-spacing. Sebagaimana namanya, properti ini digunakan untuk mengatur spasi atau jarak pada teks.

Properti letter-spacing digunakan untuk mengatur jarak antar huruf.
Properti word-spacing digunakan untuk mengatur jarak antar kata.

### 7. Text Shadow

Memberikan bayangan pada teks telah menjadi hal yang umum digunakan meskipun tidak memiliki dukungan di semua browser. Pada CSS, kita dapat gunakan properti text-shadow untuk membuat bayangan pada teks (atau biasa disebut _drop shadow_).

Nilai dari properti ini cukup rumit karena membutuhkan tiga buah nilai dan satu buah nilai warna sehingga membutuhkan empat nilai dalam satu properti untuk menentukan bayangannya.

- Nilai pertama: menunjukkan seberapa jauh ke kiri atau kanan (horizontal) bayangan harus ditampakkan.
- Nilai kedua: menunjukkan jarak ke atas atau ke bawah (vertical) bayangan harus ditampakkan.
- Nilai ketiga (opsional): menentukan tingkat keburaman yang harus diterapkan pada bayangan.
- Nilai keempat: menentukan warna yang digunakan pada bayangan.

# Pewarnaan

## 1. Text Color

Nilai dari properti color dapat berupa predefined color name atau sebuah numeric value dengan menggunakan RGB, RGBA, Hex, HSL, ataupun HSLA.

## 2. Background Color

CSS memperlakukan setiap elemen HTML seperti berada pada sebuah kotak (kita akan tahu lebih tentang ini pada pembahasan box model) dan properti background-color dapat mengatur warna untuk background dari kotak tersebut.

## 3. Opacity

Opacity adalah seberapa besar tingkat terlihat suatu objek. Semakin besar tingkat transparansi suatu objek, semakin tak terlihat objek tersebut. Namun, semakin besar tingkat opacity suatu objek, semakin terlihat objek tersebut (solid).

| Nilai               | Deskripsi                                             |
| ------------------- | ----------------------------------------------------- |
| 0%                  | Elemen tak akan terlihat.                             |
| 0% < opacity < 100% | Elemen akan tembus cahaya alias masih dapat terlihat. |
| 100%                | Elemen sepenuhnya terlihat (tak transparan).          |

# Box Model

Setiap elemen yang dibuat pada HTML akan menciptakan sebuah kotak untuk menampung kontennya. Layaknya bentuk kotak pada umumnya, ada beberapa nilai atau komponen padanya.

- Lebar dan tinggi pada kotak (konten).
- Ruang kosong antara konten dengan border (padding).
- Garis tepi (border).
- Jarak dari elemen lain (margin). 

Pada CSS, kita dapat mengatur nilai-nilai tersebut. Inilah yang disebut dengan box model.