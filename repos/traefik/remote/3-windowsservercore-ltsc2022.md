## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:79b2025b7d238aa41d8cabb5c2674ce17684f2e2c17d4fbc36ad994a31efe445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:8f0d8aa2608f41e1b601b075a9b3535795280272407c1f7d97825d4c1ff08ef6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884911035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a359eedbf0b5c515de4b8003fd3e8fa547612e264f5a27aed9e4ee811107d9a9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 14 Jan 2026 17:59:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jan 2026 18:00:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.7/traefik_v3.6.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jan 2026 18:00:38 GMT
EXPOSE 80
# Wed, 14 Jan 2026 18:00:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jan 2026 18:00:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.7 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:da514748adfff9162afb82a5e173a1f4956342c2df6f4d67f8f35c179a194dad`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a749938bb7b5a06cc2f67ac1364aa4234922c4886f713e2770fd96742bee0267`  
		Last Modified: Wed, 14 Jan 2026 18:01:30 GMT  
		Size: 49.2 MB (49246641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc889e1add3b8c266a0712f9b48042bc365689b50ca9c731956128931c503f2f`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73599d855ab87f421baa5690a5ed8e0d2fb66e9674cb49fa735a8beab7da0975`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946a446d038d8b6b091d6801fd71d504167daf6fe24ee3c406dc0d2a1922c6d7`  
		Last Modified: Wed, 14 Jan 2026 18:00:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
