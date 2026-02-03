## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:2c488b6a47f71f273cab828711a6d9b2edc1199b125ff4b3ebb507d3e625cdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull hello-world@sha256:363d48fad0375afeefe80725848f9be7852dbcfd66925ffe7769655bc9f556ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199079434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db2a8deea7512a811a59540521710b7c5b04f3e648ce654fe182deb7bfc0150`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:51:36 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 13 Jan 2026 22:51:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed73112c5616c68180a5c6e55b20325dd0eb4fc7b46c97538891336f1414ed`  
		Last Modified: Tue, 13 Jan 2026 22:51:41 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee475e8bafa70cbef4d4ef986e76320897144a97d0b4383066599834204f8a27`  
		Last Modified: Tue, 13 Jan 2026 22:51:41 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
