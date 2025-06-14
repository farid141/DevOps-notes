# Pendahuluan

docker engine berisi aplikasi client-server:

- server berjalan dengan daemon dockerd
- API untuk berkomunikasi dengan docker daemon
- CLI sebagai client docker

## hal yang dimanage docker

1. image
2. container, berjalan di atas image

bisa dipasang ke container
3. volume
4. network

## Inspect dapat digunakan pada

1. image (perintah apa yang digunakan, Environment variable apa yang digunakan, Atau port apa yang digunakan)
2. container (Volume apa yang digunakan, Environment variable apa yang digunakan, Port forwarding apa yang digunakan)

prune, membersihkan image/container/volume/network

docker image pull image:tag/version,bisa dilihat di hub.docker.com
