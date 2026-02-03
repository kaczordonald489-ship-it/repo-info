## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:3dfe5b789845e9c0e6bb7b01139c856cd12ba295bd170371083ad0ef09b55bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:de3d1803d449ab02b73296f3ed11e210b30b0e3f7b83665bd85cae0ec1049175
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1513252253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24887a74e96798d4529e46beae49f382b1a10d043a14d7bca49b4cecbdca5dbd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 21:47:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 21:47:44 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 16 Jan 2026 21:47:45 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 16 Jan 2026 21:48:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 16 Jan 2026 21:48:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 16 Jan 2026 21:48:11 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 16 Jan 2026 21:48:11 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 16 Jan 2026 21:48:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 16 Jan 2026 21:48:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 16 Jan 2026 21:48:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 16 Jan 2026 21:48:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jan 2026 21:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 16 Jan 2026 21:48:16 GMT
EXPOSE 80
# Fri, 16 Jan 2026 21:48:17 GMT
EXPOSE 443
# Fri, 16 Jan 2026 21:48:18 GMT
EXPOSE 443/udp
# Fri, 16 Jan 2026 21:48:19 GMT
EXPOSE 2019
# Fri, 16 Jan 2026 21:48:26 GMT
RUN caddy version
# Fri, 16 Jan 2026 21:48:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b7436bdde4954ab997653ca362b6410146a18fcf3b8b83a54c551cf59c9c73`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8984e104b3c0ff05fa60406f16ff2c4a2f58af5476a4da8460d993e5b15c54`  
		Last Modified: Fri, 16 Jan 2026 21:48:36 GMT  
		Size: 400.1 KB (400124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d50d69015e54959d508b06414479a76601f3f1c0c143302fa9815426f0ecdb`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd758177c1c66b62710c9ed34334f9a3b5978222bc6019718dfae6fd235898`  
		Last Modified: Fri, 16 Jan 2026 21:48:38 GMT  
		Size: 16.7 MB (16685267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6469db906ffeec163dc378daa88374a7395d787fbd64478d4a423691f7aa1c6`  
		Last Modified: Fri, 16 Jan 2026 21:48:35 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460c8b42281a2a84615f002cbb6533907bb7414d370ba83f99b09259c4b8577`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6125a52e3a7563428016564d117f80bd877e38a7a37181bab82f031fc024b8`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f6273de3485d3093bea4161194792b0a4895d56b17d19ea0ae955de131723`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb815f2b06c4f07495bb86c150cb225f1e14a30832c182218467729a2c22cd`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3bb0e23239e46f5ac1baf3505b72062c5c1b0a2b56accf494255279b81dc6c`  
		Last Modified: Fri, 16 Jan 2026 21:48:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a0214cac497353d4d26a9e5729390a85a2cb4422324ad1a8dc9b7cbc10c883`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a97fe8c2c247a6fcaf584e485cc9b3d5bc584d4f0b7e97ca098fd712ffcc10e`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe22cb691633447fd4bb8f450aa6f4382ed47bc70c2f393e6eec96f267f6872`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3985fbe8b539cb8a152f3c35d7e7df4d60e2640770f2aa39f00fe07553a32e4`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e323161037befd8a9185eb6af7db6e238ccb4451b0f64284a255f3062f58ac`  
		Last Modified: Fri, 16 Jan 2026 21:48:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852fd37e891f32ad639c4d4d7f6645b31ca2efe1e9bc6b7b588d6046bce65ab`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1abadcb16f8b7383029dbb8f7528efb9cddedd7ff75d0847ef53f11e744b75c`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e8ff0c84b5e9acf20fae62134d7bb0807d09f14fe921287c0ca135f987422`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa1ae318ebbfdc86e2311719b9629cade532ac567939ea85a8dd9fd1f236062`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 384.3 KB (384316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e746bfff6a737ce01c0ec0226a66bf3b12acfd3f6c44c2fd4fc4809d15811`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
