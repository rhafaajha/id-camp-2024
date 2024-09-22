# Selector Dasar

Ada banyak jenis selector untuk menargetkan aturan ke elemen tertentu dalam dokumen HTML.

### 1. Type Selector

Type Selector menggunakan nama elemen sebagai target untuk diterapkannya rule. Dalam kata lain, ketika menggunakan selector ini tentu rule akan diterapkan pada seluruh elemen target yang ada pada dokumen HTML.

| index.html |
| ---------- |

| ```html

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Judul Dokumen</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <span>
      Ini merupakan sebuah teks yang berada pada elemen span. Seharusnya elemen
      ini ditampilkan dengan warna teks merah.
    </span>
    <p>
      Ini merupakan sebuah teks yang berada pada elemen paragraf, teks ini tidak
      seharusnya tidak akan terpengaruh oleh rule.
    </p>
    <span>
      Ini merupakan sebuah teks yang berada pada elemen span lainnya. Seharusnya
      elemen ini ditampilkan dengan warna teks merah juga.
    </span>
  </body>
</html>
``` |

| style.css |
| --------- |

| ```
/_ Semua elemen span _/
span {
color: red;
}

```|
```

Hasil di atas akan membuat teks yang berada pada setiap elemen `<span>` akan berwarna merah.


