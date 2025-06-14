# Penjelasan

Digunakan untuk menjalankan perintah terminal dari container

## Entrypoint

berisi command yang menerima argumen (CMD atau default argument).

```dockerfile
ENTRYPOINT ["executable", "param1", "param2"]
```

## CMD

Dijalankan ketika container start. Provides default arguments to ENTRYPOINT or sets the default command if ENTRYPOINT is not defined.

```dockerfile
ENTRYPOINT ["echo"]
CMD ["Hello from CMD"]

# result
$ echo "Hello from CMD"
```

>Jika ada beberapa CMD dalam Dockerfile, hanya CMD terakhir yang akan digunakan, yang sebelumnya akan diabaikan.
