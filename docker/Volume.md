# Mounts

Terdapat 2 jenis mount:

- volume: seperti disk yang dapat di hubungkan ke container agar dapat diakses.
- bind: link dari sistem host ke container, sistem host dapat diubah baik dari host maupun container.

## mounts dapat dilakukan dengan 2 cara

```bash
docker run --mount type=bind,src=<host-path>,dst=<container-path>
docker run --volume <host-path>:<container-path>

# atau

docker run -v /path/host:/path/container ...
docker run -v nama-volume:/path/container ...
```
