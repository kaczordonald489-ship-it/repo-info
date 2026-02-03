## `caddy:2-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:e51c12b08f0532442910c04ee72dcea308a7afa40f88024ffb1483755d567742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:2-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:83d7f1db219eba84bfd9eeffeb70cb9ad4f83777df81768a4477d0c5b5094541
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215734784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875083e097f368650436e70e38b243079572b383b1d5ae798cccdc560cac96f9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 22:10:26 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Fri, 16 Jan 2026 22:10:27 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Fri, 16 Jan 2026 22:10:30 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Fri, 16 Jan 2026 22:10:34 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Fri, 16 Jan 2026 22:10:34 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 22:10:35 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 22:10:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 22:10:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 22:10:37 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 22:10:37 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 22:10:38 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 22:10:39 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 22:10:39 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 22:10:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 22:10:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 16 Jan 2026 22:10:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Fri, 16 Jan 2026 22:10:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Fri, 16 Jan 2026 22:10:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Fri, 16 Jan 2026 22:10:46 GMT
RUN caddy version
# Fri, 16 Jan 2026 22:10:47 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583c8efc88613ab537d0abf5ed4dafa4c4b46e2329b042c6c2e02850f9b4c918`  
		Last Modified: Fri, 16 Jan 2026 22:10:56 GMT  
		Size: 69.9 KB (69928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1baedeb368ef34357f14e70433098a747c14f70534c9ae0b558b1ac678c6977`  
		Last Modified: Fri, 16 Jan 2026 22:10:58 GMT  
		Size: 16.2 MB (16217735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcac5b63dc24d69b4d4131331d323b434c2b26d2e456487738cc7c5c541a68b`  
		Last Modified: Fri, 16 Jan 2026 22:10:56 GMT  
		Size: 129.8 KB (129813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b79e0fe6da3a19cdf3ad5e69546f9a6b541884b29770051e0a59c7135f7201`  
		Last Modified: Fri, 16 Jan 2026 22:10:56 GMT  
		Size: 113.7 KB (113663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f227b18bb7b0de42624d8a591c23c465d0f43385fe6a6755f443c5b066e473d5`  
		Last Modified: Fri, 16 Jan 2026 22:10:56 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c6053bd4011c04cc6556ed2d37fc4863b80e331c0dc36e406d7c380c539321`  
		Last Modified: Fri, 16 Jan 2026 22:10:54 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471e8a6ef7f95868d769c8702839099ecd4ad6086972edb8f3256d3f059426dd`  
		Last Modified: Fri, 16 Jan 2026 22:10:54 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3b08f10395d880c2090e4193dec50c5ab8d9b2ba32dbd58049ef4d8fdf1a31`  
		Last Modified: Fri, 16 Jan 2026 22:10:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff592fec5763fabe58bcb0bd4d736b37067b179eb227e3dc80f85e23b09d1b17`  
		Last Modified: Fri, 16 Jan 2026 22:10:54 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9553b79e5363f50d8413dfdfcc4f8a6c03e336bfa85a3491e41bf9330e3c6b2`  
		Last Modified: Fri, 16 Jan 2026 22:10:54 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe7c63a2bcd13a8af9c4549ab79e193dee7c5152c868d2b80ac9a9ec694d55`  
		Last Modified: Fri, 16 Jan 2026 22:10:53 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb853e06ab9837fa591891fca121923e8e522279a7cbfe9312e1809201410b4c`  
		Last Modified: Fri, 16 Jan 2026 22:10:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60897b4c69bd52742f05d73e743232aa9bd7c2d3fe6798f191bd4464fafd354`  
		Last Modified: Fri, 16 Jan 2026 22:10:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d3ca87d23420048b4d5b0b14178a72962d7dda6271b9dfb61f107547cf5f9`  
		Last Modified: Fri, 16 Jan 2026 22:10:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0eb1715ec58c47dc64144f79b9a7928705281ee846a6ca73c504d73e326ec6`  
		Last Modified: Fri, 16 Jan 2026 22:10:52 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4a6c17f333c57f6ebd5a9a83bd6c54bde0920410c2d76447e575e1a3ef44b7`  
		Last Modified: Fri, 16 Jan 2026 22:10:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f2edb46026033eba2e98a7dc777c522a0593a8462fc244c53d35edef63e9f9`  
		Last Modified: Fri, 16 Jan 2026 22:10:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658d692fefe8b56a46fa0361f3df974f009c9dc3e5e84ee07c23a99218df120b`  
		Last Modified: Fri, 16 Jan 2026 22:10:51 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708c60f8b1951fa04abbb857254502d29fffe27e30b9ace4c803f90e465c99cf`  
		Last Modified: Fri, 16 Jan 2026 22:10:51 GMT  
		Size: 111.2 KB (111192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e72f27d970141b92741ae95763911cd61b34241c9c627bfdbb392d3ea14bf87`  
		Last Modified: Fri, 16 Jan 2026 22:10:51 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
