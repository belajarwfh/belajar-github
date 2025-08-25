# cara menampilkan gambar
Kalau gambar ada di folder project, bisa pakai path relatif:
```md
![Deskripsi](./images/foto.png)
```

Kalau gambar dari internet, pakai URL langsung.

Markdown asli biasanya tidak mendukung pengaturan ukuran, tapi kalau pakai GitHub / VSCode preview / beberapa parser, kamu bisa selipkan HTML untuk atur lebar/tinggi:
```html
<img src="./images/foto.png" alt="deskripsi" width="200">
```
