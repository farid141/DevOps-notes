# Docker network

## membuat network

- `docker network create -d bridge net_name`

## beberapa opsi driver yang umum

- `bridge` The default network driver.
- `host` Remove network isolation between the container and the Docker host.
- `none` Completely isolate a container from the host and other containers.

Kontainer yang terhubung ke bridge network yang sama dapat berkomunikasi menggunakan alamat IP internal jaringan bridge tersebut. Kita tidak perlu tahu alamat IP internal tersebut, melainkan langsung dapat mengakses localhost:port pada aplikasi container

## Connect and Disconnect

network bisa dicopot/pasang ketika container sudah/akan dibuat:

### Akan dibuat

- `docker run --network=my-net -itd --name=container3 busybox`

### Sudah dibuat

- `docker network disconnect net_name cont_name`
- `docker network connect net_name cont_name`
