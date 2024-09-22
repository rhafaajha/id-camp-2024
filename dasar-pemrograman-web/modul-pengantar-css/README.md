# Pengantar CSS

CSS atau Cascading Style Sheet adalah standar dari W3C untuk mengatur visualisasi berkas yang ditulis pada HTML.

CSS bukanlah sebuah bahasa pemrograman karena tidak ada logika, tidak ada sintaks pengondisian, tidak ada proses iterasi, dsb. padanya. CSS hanya sebuah declarative language yang digunakan untuk mendeklarasikan suatu nilai yang nantinya digunakan untuk mengatur tampilan sebuah elemen HTML pada browser.

# Keuntungan CSS

- Dapat mengontrol dan menerapkan layout secara presisi.
  <br> Dengan menggunakan CSS kita bisa membuat sebuah website terlihat seperti dokumen cetak dengan desain yang menarik dan presisi.

- Menghindari pekerjaan yang berulang-ulang dalam menerapkan styling.
  <br> Kita dapat menetapkan styling pada beberapa berkas HTML hanya dengan menggunakan satu berkas CSS.

- Didukung banyak browser.
  <br> Seluruh browser saat ini minimal sudah mendukung CSS versi 2. Untuk browser yang populer, seperti Chrome dan Firefox, sudah mendukung CSS versi 3.

# Cara Kerja CSS

1. Dimulai dari sebuah dokumen yang telah ditandai dengan tag elemen HTML.
2. Menuliskan aturan styling untuk menentukan tampilan elemen HTML.
3. Melampirkan aturan styling yang sudah dibuat pada dokumen HTML. Ketika browser memuat dokumen, tampilan elemen akan menyesuaikan dengan aturan styling yang sudah ditetapkan.

# Menulis Aturan Styling

Sebuah style sheet dibuat terdiri dari satu atau lebih aturan styling (biasa disebut dengan rules atau rule-sets) yang mendeskripsikan cara sebuah elemen atau sebuah kelompok elemen ditampilkan dalam jendela browser.

Contoh penulisan CSS adalah

```
h1 {
  color: green;
}

p {
  font-size: small;
  font-family: sans-serif;
}
```

Dalam penggunaan CSS, terdapat dua bagian pada sebuah rule. Bagian pertama adalah identitas elemen atau elemen yang akan menerapkan rule (singkatnya kita akan sebut `selector`) dan kedua adalah `deklarasi` atau instruksi yang akan diterapkan pada sebuah selector.

<img src="https://d17ivq9b7rppb3.cloudfront.net/original/academy/20191206154352e89d6a0d2ec386b3da42d877ce0278c1.png" alt="" width="300">

# Melampirkan Styling pada Dokumen HTML

Ada tiga cara untuk menerapkan styling pada elemen HTML.

### 1. External Style Sheet

_External Style Sheet_ adalah berkas terpisah yang di dalamnya hanya ada CSS rules. Berkas harus berekstensi .css dan akan dihubungkan dengan dokumen HTML. Cara ini merupakan yang paling powerful dalam menerapkan styling. Dengan cara ini, satu berkas styling (.css) dapat digunakan oleh banyak berkas HTML.

Contoh pemanggilan berkas css.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Judul Dokumen</title>

    <!-- Impor berkas CSS Anda -->
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <!-- konten di sembunyikan -->
  </body>
</html>
```

Pada contoh di atas, berkas css yang digunakan adalah berkas lokal. Nilai atribut href berupa berkas .css yang tersedia melalui sebuah URL/Path berkas disimpan.

Tak jarang banyak pengembang menggunakan bootstrap.min.css untuk membantu penyusunan layout website-nya. Kita bisa menggunakannya pada berkas HTML dengan langsung menuliskan URL untuk berkas tersebut.

```
<head>
  <title>Document Title</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
</head>
```

> Catatan:
> Nama berkas yang mengandung “min.css” adalah penamaan format berkas CSS yang sudah di-minify atau diminimalkan dengan menghilangkan white space yang tidak digunakan.

### 2. Embedded Style Sheet

_Embedded Style Sheet_ adalah kumpulan rules yang dituliskan dalam berkas HTML dengan menggunakan elemen `<style>`. Dengan demikian, CSS rules yang dituliskan hanya dapat dicakup oleh satu berkas HTML. Penulisan rules harus dituliskan dalam elemen `<style>` dan biasanya ditempatkan dalam `<head>` pada berkas HTML.

Contoh:

```
<head>
  <title>Document Title</title>
  <style>
    /*
    * Rules styling dituliskan di sini
    */
  </style>
</head>
```

### 3. Inline Style

_Inline Style_ adalah styling yang diterapkan secara langsung pada elemen HTML dengan menggunakan atribut `style`.

Contoh:

```
<h1 style="color: green; margin-top: 2em">Kota Bandung</h1>
```

> Inline styles hanya diterapkan pada elemen tempat atribut style diterapkan. Teknik ini seharusnya dihindari, terkecuali benar-benar diperlukan untuk menggantikan sebuah styling yang ditetapkan pada Embedded Style Sheet atau External Style Sheet.

# CSS Conception

### 1. Inheritance

Styling HTML bersifat _inheritance_ yang berarti dapat mewarisi properti style “tertentu” dari suatu elemen ke elemen-elemen di dalamnya (_child-elements_).

Contohnya, CSS rules yang ditetapkan untuk elemen `<body>` akan diterapkan pada seluruh _child-elements_ secara otomatis.

```
body {
  font-family: sans-serif;
}
```

### 2. Group Selector

Jika beberapa selector yang berbeda memiliki penerapan properti-properti yang sama, kita dapat menggabungkannya menggunakan group selector. Hal ini dapat meminimalkan penulisan kode yang berulang.

Contohnya berikut. Gunakan tanda koma (,) untuk memisahkan tiap selector-nya.

```
h2,
h3 {
  color: #00A2C6;
}
```

### 3. Rule Order

Cascading artinya “mengalir”. Demikian halnya dengan alur kerja CSS dalam membaca kode, mengalir dari atas ke bawah. Oleh karena itu, kita harus memperhatikan urutan dalam penulisan rules, terutama saat terjadi sebuah konflik.

```
p {
  color: red;
}

p {
  color: blue;
}
```

Namun, kita bisa membuat sebuah property styling agar dianggap penting oleh browser untuk diterapkan dan urutan tidak diperhatikan. Kita bisa menambahkan keyword `!important` pada akhir nilai propertinya.

```
p {
  color: red;
}

p {
  color: blue !important;
}
```

> Gunakan `!important` ketika memang benar-benar dibutuhkan saja.
