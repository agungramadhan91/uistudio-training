# Training Notes - CSS Layouting

### Display
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

### Flexbox
Model layout 1D (horizontal atau vertical dalam 1 bagian) yang dapat mengatur jarak dan penajajaran antar item dalam sebuah container. Sifatnya memiliki container(parent tag) dan items(child tag)

```css
.container{
    display: flex /* atau inline-flex */
}
```

