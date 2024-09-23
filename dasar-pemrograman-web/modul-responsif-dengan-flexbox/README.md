# Pengantar Flexbox

Flexible box layout adalah model layout satu dimensi guna menyusun elemen-elemen (flex items) dalam posisi rows atau columns. Hal ini membuat flexbox disebut dengan direction-agnostic atau mengatur tata letak di banyak arah. Hal menarik dari flexbox adalah ia menawarkan penyusunan layout dengan fleksibel karena flex container atau flexbox dapat mengatur dimensi setiap flex-items (child element) sehingga layout yang diinginkan dapat tercapai dengan mudah.

Flex container memperluas flex items untuk mengisi ruang kosong atau menciutkannya sehingga menghindari overflow (dimensi child element yang keluar dari parent element-nya). Dengan hadirnya flexbox, perancangan layout dalam skala yang kecil dapat dilakukan dengan mudah pada halaman web.

Flex container adalah parent element dari seluruh flex items, sedangkan flex items adalah elemen yang secara langsung merupakan child dari parent element.

# Properti-Properti pada Flex Container

Dalam penerapan flexbox, ada properti-properti yang terlibat pada dua hal, yaitu flex container (parent element) dan flex item. Properti-properti pada flex container akan berpengaruh secara langsung kepada flex item dalam menampilkan susunannya. Berikut daftar dan penjelasannya.

1. `display`: mendefinisikan elemen agar disusun sebagai flexible box.
2. `flex-direction`: menentukan arah susunan flex item dijajarkan.
   <br> Berikut adalah penjelasan value dari properti flex-direction.
   - `Row`: flex items akan disusun secara horizontal dari kiri ke kanan.
   - `Row-reverse`: flex items akan disusun secara horizontal, tetapi berarah terbalik (kanan ke kiri).
   - `Column`: flex items akan disusun secara vertikal dari atas ke bawah.
   - `Column-reverse`: flex items akan disusun secara vertikal, tetapi dengan arah terbalik (bawah ke atas).
3. `flex-wrap`: mengubah perilaku susunan flex item menjadi dua dimensi (jika dibutuhkan).
   <br> Berikut adalah penjelasan setiap value dari properti flex-wrap.
   - `nowrap`: seluruh flex items hanya akan ditempatkan dalam satu baris meskipun sangat banyak jumlahnya.
   - `wrap`: nilai ini menyebabkan flex items akan diletakkan ke baris yang baru (berikutnya) sehingga menjadi multiple lines.
   - `wrap-reverse`: meskipun mirip dengan wrap, nilai ini akan menyebabkan beberapa flex items ditempatkan dengan menambahkan baris sebelumnya.
4. `justify-content`: mengatur tata letak dari flex item pada main axis.
   <br> Berikut adalah penjelasan setiap value dari properti justify-content.
   - `Flex-start`: peletakan child element akan dimulai dari main-start.
   - `Flex-end`: peletakan child element dimulai dari main-end.
   - `Center`: child element akan diletakkan di tengah parent child.
   - `Space-between`: child element akan tersusun secara merata, elemen pertama berada di tepi main-start dan elemen kedua berada di tepi main-end. Jika child element lebih dari dua, elemen lainnya akan didistribusikan berada di tengah dengan jarak yang sama.
   - `Space-around`: setiap child element akan memiliki panjang celah yang sama pada sisi horizontal.
   - `Space-evenly`: setiap child element akan memiliki jarak yang setara, termasuk jarak ke tepi main-start dan main-end.
5. `align-items`: mirip seperti justify-content, tetapi mengatur child element dalam satu baris pada cross axis.
   <br> Berikut adalah penjelasan setiap value dari properti align-items.
   - `Stretch`: melebar hingga memenuhi container dalam cross axis. Setiap child element akan memiliki nilai height yang sama, meskipun isi konten berbeda.
   - `Flex-start`: setiap child element akan memiliki ukuran height sesuai dengan isi konten serta seluruhnya akan berada di tepi cross-start.
   - `Flex-end`: setiap child element akan memiliki ukuran height sesuai dengan isi konten serta seluruhnya akan berada di tepi cross-end.
   - `Center`: setiap child element memiliki ukuran height sesuai dengan isi konten dan secara vertikal posisi elemen berada di tengah.
   - `Baseline`: nilai pada asalnya akan menyerupai flex-start. Namun, jika konten pertama pada masing-masing child element memiliki ukuran height yang berbeda, child element lainnya akan menyesuaikan posisinya secara cross axis dari cross-start.
6. `align-content`: melakukan perataan terhadap flex item pada setiap baris dalam cross-axis.
   <br> Berikut adalah penjelasan setiap value dari properti ini.
   - `Normal (default)`: Jika kita tidak menerapkan value pada align content, flex items akan diposisikan secara default.
   - `Flex-start`: flex items ditata pada permulaan flex container.
   - `Flex-end`: flex items ditata pada akhir flex container.
   - `Center`: flex items diposisikan di tengah flex container.
   - `Space-between`: flex items akan disebar secara merata, item pertama akan diposisikan pada cross-start dan item terakhir akan diposisikan pada cross-end.
   - `Space-around`: flex items akan disebar secara merata dengan jarak celah yang sama juga.
   - `Space-evenly`: flex items akan disebar secara merata dengan jarak yang merata juga.
7. `gap`: memberikan jarak atau celah pada flex item.

# Properti-Properti pada Flex Items

Setelah mempelajari properti-properti pendukung pada flex container, kita akan membahas properti-properti yang digunakan pada flex item. Ingat! Properti yang ditujukan pada flex item hanya akan berpengaruh pada flex item yang ditarget, bukan elemen pembungkusnya (flex container).

1. `order`: mengatur urutan susunan flex item.
2. `flex-grow`: melakukan grow (pelebaran ukuran) dari flex item yang ditarget pada main axis.
3. `flex-shrink`: menyusutkan atau menciutkan ukuran child element jika ukurannya tidak mencukupi ruang container.
4. `flex-basis`: memberikan ukuran default sebelum sisa ruang container didistribusikan kepada flex item.
5. `align-self`: mengatur posisi child element secara cross-axis.
