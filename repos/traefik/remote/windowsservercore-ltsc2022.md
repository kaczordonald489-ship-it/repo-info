## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e12e63587c16c265ac09e3142b9c425a28c38c852d3dcc1fc1c5284a78cbf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:a60e6c475ff829068f897a350f02c9863c96341c6225451598b9fe20427b4f51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818804346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e07913612a363e8775ab20d3774673bd951b0013fefe59039dc0fc546de299d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 18 Nov 2025 19:30:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 18 Nov 2025 19:32:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.2/traefik_v3.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 18 Nov 2025 19:32:33 GMT
EXPOSE 80
# Tue, 18 Nov 2025 19:32:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 18 Nov 2025 19:32:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3fe2de4763fec9e04965db334b232d2c7bbfc63eca4fbe8cbc6068e5171b33`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088536f0fede38447f8678b24825ac42a819e1b77b1e459216f7271b3132c32e`  
		Last Modified: Tue, 18 Nov 2025 19:44:48 GMT  
		Size: 48.8 MB (48837630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614f0d13bd9f20218c8596fe0eba793f9d9cf81346227974debcf096836e94c0`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf439dae7e13458d64724f68e66fd0f1d2f2789e7f6c67e6f0f1251662c55c49`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9f3f3ef22d42d6cdde8b9ab8046edd3db23793c7177aa4903b83d777c0d72`  
		Last Modified: Tue, 18 Nov 2025 19:44:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
