# Penjelasan

Merupakan sebuah lingkungan yang bisa digunakan/direferensi berkali-kali untuk membuat container.

## Layer Caching

Sebuah image memiliki base layer atau history. Dapat dicek dengan
>docker image history node-base

Docker caching memanfaatkan urutan tersebut untuk caching agar ketika build dengan step yang sama image tersebut akan mengcopy dari yang ada.

## Mengelola Image

- hapus image yang tidak direferensi container mati/hidup `docker image purne`
- cek list image `docker image ls`
