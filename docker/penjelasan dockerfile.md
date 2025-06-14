merupakan sebuah file yang berisi rangkaian instruksi yang digunakan untuk membuat docker image

beberapa instruksi dockerfile:


ADD vs COPY
COPY hanya melakukan copy file saja, sedangkan ADD selain melakukan copy, dia bisa mendownload source dari URL dan secara otomatis melakukan extract file kompres

sebisa mungkin menggunakan COPY, jika memang butuh melakukan extract file kompres, gunakan perintah RUN dan jalankan aplikasi untuk extract file kompres tersebut

.dockerignore: digunakan untuk exclude file host pada saat copy/add

ENV vs ARG
keduanya merupakan sebuah variabel. Bedanya, ARG hanya akan dijalankan ketika build time saja, sedangkan ENV dapat berjalan ketika sudah menjadi container. ARG dapat diatur ketika membuat container dari sebuah image: --arg=asdd