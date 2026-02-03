## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f5ae05094d839e794e60dd5b43902cf2b0847133968f966e20e6d6b1bd20fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8653957c0f5c9070b1cc253d0fff7874ea96ac9b942df6143f0176fae0f5b0ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883927849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5392885a1064167c35d7f80232afa958cd7e327c6d4b7c648baaeb12ffa5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 02 Feb 2026 19:22:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 02 Feb 2026 19:23:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.36/traefik_v2.11.36_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 02 Feb 2026 19:23:27 GMT
EXPOSE 80
# Mon, 02 Feb 2026 19:23:28 GMT
ENTRYPOINT ["/traefik"]
# Mon, 02 Feb 2026 19:23:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.36 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51645fde7b24e956e6c4f21d112a0c167604c40e6f16f2719875f8823c70e648`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89321d5ed9879a208f5c3d42052e67bc3fe7d845de95cb0dc7a068212c74dcf`  
		Last Modified: Mon, 02 Feb 2026 19:24:07 GMT  
		Size: 48.3 MB (48263436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32dc420d8e23df65a1a7c70f6165cc0dcfdf26bd9698aee5ae28835317d014`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921f73b1b6557d210849c413be9e44da91ae1fde7b5b2a14351591031731f3e9`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d5674fad81db68a74b7d2ca0616018cbd0cd856f4697fdcf70547188ae707`  
		Last Modified: Mon, 02 Feb 2026 19:23:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
