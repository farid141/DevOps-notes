# Pendahuluan

Container berasal dari sebuah image, dimana sebuah image dapat berisi serangkaian eksekusi command yang dapat dijalankan ketika runtime (container start) dan build time.

Untuk membuat sebuah environment variabel, kita dapat menggunakan `ENV` dan `ARG`.

```bash
docker run -e PORT=3000 myimage
```
