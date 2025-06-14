# Penjelasan

Dockerfile merupakan sebuah file yang berisi kumpulan instruksi untuk menggenerate sebuah image baru.

## Kamu membutuhkan Dockerfile ketika

- Kamu ingin membuat custom image ,
- Memodifikasi image dasar (base image),
- Menambahkan aplikasi, konfigurasi, atau dependensi tertentu.

### Membuat images dari dockerfile

> docker build -t img_name .

## Commands

Digunakan untuk menjalankan perintah terminal dari container

### Entrypoint

berisi command yang menerima argumen (CMD atau default argument) yang dieksekusi ketika container akan berjalan.

```dockerfile
ENTRYPOINT ["executable", "param1", "param2"]
```

### CMD

Dieksekusi ketika container akan berjalan. Provides default arguments to ENTRYPOINT or sets the default command if ENTRYPOINT is not defined.

```dockerfile
ENTRYPOINT ["echo"]
CMD ["Hello from CMD"]

# result
$ echo "Hello from CMD"
```

>Jika ada beberapa CMD dalam Dockerfile, hanya CMD terakhir yang akan digunakan, yang sebelumnya akan diabaikan.

### ADD vs COPY

COPY hanya melakukan copy file saja, sedangkan ADD selain melakukan copy, dia bisa mendownload source dari URL dan secara otomatis melakukan extract file kompres

sebisa mungkin menggunakan COPY, jika memang butuh melakukan extract file kompres, gunakan perintah RUN dan jalankan aplikasi untuk extract file kompres tersebut

.dockerignore: digunakan untuk exclude file host pada saat copy/add

ENV vs ARG
keduanya merupakan sebuah variabel. Bedanya, ARG hanya akan dijalankan ketika build time saja, sedangkan ENV dapat berjalan ketika sudah menjadi container. ARG dapat diatur ketika membuat container dari sebuah image: --arg=asdd
