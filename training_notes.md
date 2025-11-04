# Training Notes - CSS Layouting

### 1. Display
Tampilan CSS secara standar hanya 2: `inline` dan `block`
> display: inline | inline-blok | block | none 

- *inline*: tidak bisa mengatur luas dan hanya sesuai elementnya
- *inline-block*: element inline yang dapat diatur luasnya
- *block*: dapat mengatur luas element
- *none*: menghilangkan display pada element

Elemen pengguna alami:
- *inline*: button, input, label, b, strong, i, em, a, span, sub, sup, select, textarea
- *block*: h1-h6, p, ol, ul, li, form, hr, div, 

```css
a {
    display: inline-block
    width: 600px
    height: 200px 
}
```

### 2. Dimensi & Overflow
#### Dimensi
Satuan ukuran untuk `width` dan `height`:
- *0px* : Satuan absolute
- *0%*  : Satuan relative terhadap pembungkusnya
- *0in | cm | pt | mm | pc* : Satuan didunia nyata

#### Overflow
Overflow akan menyembunyikan elemen diluar dimensi yang ditentukan.

ada beberapa value untuk `overflow`:
- *visible* : Menampilkan elemen lebih tanpa menyembunyikan
- *auto*    : Menyembunyikan element lebih ke dalam scroll
- *hidden*  : Menyembunyikan element lebih tanpa scroll
- *scroll*  : Memberikan fitur scroll pada element baik lebih ataupun tidak

Pengunaan:
```css
{
    overflow: visible | auto | hidden | scroll
}
```

### 3. Box Model
Semua element HTML adalah sebuah Box / Kotak, Box model memiliki beberapa properti:
- *margin*, area transparan diluar kotak
- *border*, batas disekeliling content dan padding
- *padding*, area transparan didalam kotak
- *content*, konten sebenarnya didalam kotak

    #### Margin
    > margin: 10px 20px

    Memiliki sifat jika bertemu dengan box lain:
    - Ukuran vertikal (top/bottom): area kotak yang memiliki ukuran margin lebih besar yang akan digunakan
    - Ukuran horizontal (left/right): Ukuran area kedua kotak akan digabung
    - Bisa menerima nilai negative

    #### Padding
    > padding:20px

    Memiliki sifat:
    - Menambah ukuran box dari yang sudah ditentukan
    - Nilai negative tidak berpengaruh

    #### Border
    > border: width style color;

    Memiliki sifat:
    - Menambah ukuran box dari yang sudah ditentukan

    <br>
    
    **Total dimensi = width/height + padding + border**

    <hr>

    #### Box Sizing
    > box-sizing: border-box;


    Akan memaksa `padding` dan `border` menyesuaikan ukuran `width` dan `height`nya

    ```css
    {
        width: 600px;
        box-sizing: border-box; 
    }
    ```




### Flexbox
Model layout 1D (horizontal atau vertical dalam 1 bagian) yang dapat mengatur jarak dan penajajaran antar item dalam sebuah container. Sifatnya memiliki container(parent tag) dan items(child tag)

```css
.container{
    display: flex /* atau inline-flex */
}
```

