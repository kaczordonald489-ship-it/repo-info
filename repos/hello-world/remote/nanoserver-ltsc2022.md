## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:8983411e30daa9e5b5aaee1925ad2cad0d6862bb6e8f71e53cf234d42787eb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull hello-world@sha256:786cc036abc9d6a94c2ea8236e1f6b9d26bfee45ad08ace9984c971e848827b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126699645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd9431e2a6dd3f11c3a1e6379e079832db9ecf16af38323dc9aec50eeecd2c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 22:51:49 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 13 Jan 2026 22:51:50 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21249f42e73ea398b459db4050433677ad7cfb68c1df80882324ceedaf735e15`  
		Last Modified: Tue, 13 Jan 2026 22:51:54 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6a4774598b1f1ac6f645433ff932b4a3925d075e11febf3cc85158cdde2db0`  
		Last Modified: Tue, 13 Jan 2026 22:51:54 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
