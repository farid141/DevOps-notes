# Penjelasan

Docker container selalu berasal dari image
selama kita sudah memiliki docker image, kita tidak memerlukan dockerfile

## Commands

- Create and run container from image `docker run [image-tag]`
- Create only `docker container create [image-tag]`
- Delete containers `docker container rm cont1 cont2 cont3`
- `docker run -it [image-tag] [cmd]` = override CMD dengan cmd
- `docker container ps`

## Additional Info

- Ketika sebuah image dari perintah pembuatan container tidak ditemukan di local, maka akan pull dari docker registry.

## Some additional attributes

Ketika menjalankan sebuah container, kita dapat mengirim beberapa attribute.

- port:  `-p 8080:80 nginx` atau `-P` untuk port random
