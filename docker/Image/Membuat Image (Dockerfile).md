# Penjelasan

Dockerfile merupakan sebuah file yang berisi kumpulan instruksi untuk menggenerate sebuah image baru.

## Kamu membutuhkan Dockerfile ketika

- Kamu ingin membuat custom image ,
- Memodifikasi image dasar (base image),
- Menambahkan aplikasi, konfigurasi, atau dependensi tertentu.

### Membuat images dari dockerfile

> docker build -t img_name .

## Commands

Digunakan untuk menjalankan perintah terminal dari container. Dieksekusi saat runtime.

### Entrypoint

berisi command yang menerima argumen (CMD atau default argument) yang dieksekusi ketika container akan berjalan (runtime).

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

### ADD

sedangkan ADD selain melakukan copy, dia bisa mendownload source dari URL dan secara otomatis melakukan extract file kompres

### COPY

melakukan copy file dari direktori ke container. Sebisa mungkin menggunakan COPY, jika memang butuh melakukan extract file kompres, gunakan perintah RUN dan jalankan aplikasi untuk extract file kompres tersebut.

> perintah COPY dan ADD akan mengexlude nama file yang ada di `.dockerignore`

### ENV

sebuah variabel yang diakses saat build dan run time.

### ARG

sebuah variabel yang diakses saat build image.

### RUN

Menjalankan perintah saat build time, (akan berpengaruh terhadap image layer caching)

Tips menjalankan RUN multi commands

```bash
# gunakan heredocs
RUN <<EOF
apt-get update
apt-get install -y curl
EOF

# atau escape character
RUN apt-get update\
apt-get install -y curl

```
