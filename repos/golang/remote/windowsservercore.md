## `golang:windowsservercore`

```console
$ docker pull golang@sha256:2fcc41d39cad75db024f8e324cba5874476be5f397b85d9595e3c4de5e311660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:5f6958ea91abc3143040e63d0cd2b46856c1d46ec0d07d7d5f0313bfe0e8df7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1609984458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ab35dddf263a786bc4738f2813cf63f3b1ccc1bf79f4001cddbf507970c49a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 15 Jan 2026 19:34:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 19:34:24 GMT
ENV GIT_VERSION=2.48.1
# Thu, 15 Jan 2026 19:34:25 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 15 Jan 2026 19:34:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 15 Jan 2026 19:34:27 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 15 Jan 2026 19:35:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:35:08 GMT
ENV GOPATH=C:\go
# Thu, 15 Jan 2026 19:35:14 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 15 Jan 2026 19:35:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:36:38 GMT
RUN $url = 'https://dl.google.com/go/go1.25.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '19b4733b727ba5c611b5656187f3ac367d278d64c3d4199a845e39c0fdac5335'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:36:39 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a519eaac22a8e810614a54d1ecd7e172debe7d71f6e27ca1ba91bdc6a0f9e`  
		Last Modified: Thu, 15 Jan 2026 19:36:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484d141a3d44935a72760270d4f6787bbe4cb0a32e834e840563a8475284d24`  
		Last Modified: Thu, 15 Jan 2026 19:36:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4d7e64245aaea9d2fb7e300b6b88fcfa0ab8772b159b7fa10c961614f009f`  
		Last Modified: Thu, 15 Jan 2026 19:36:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b180294a8ef453ef91144aefda6c2e229b04efcfbdb95eab84205d8a65efd9`  
		Last Modified: Thu, 15 Jan 2026 19:36:53 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf89600227a0242479da3c0ae3a845b2b51c2833a42c2472f7e2b259315f5ca`  
		Last Modified: Thu, 15 Jan 2026 19:36:53 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5964e8cbe72df39254ea3c852054cd26c479539b1e7559f92f1864adc4f0fe3`  
		Last Modified: Thu, 15 Jan 2026 19:37:00 GMT  
		Size: 51.2 MB (51244732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bc7300c1c68770859c4873c9728130f2acab3a6b69c81c88a3851fa61b7e70`  
		Last Modified: Thu, 15 Jan 2026 19:36:51 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783588cc72ed2dde28deae4066216333e60f144bed1e46a6a1371f44f8c9d7d`  
		Last Modified: Thu, 15 Jan 2026 19:36:52 GMT  
		Size: 373.9 KB (373923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd53c6443492192c1e4fb1d656f1a9f1df39d5baa327d49554328c37470b032`  
		Last Modified: Thu, 15 Jan 2026 19:36:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad2e2cac32485cbbf78ff68f8d974f3149d95c10d58c27c9f46fe3d5cdba801`  
		Last Modified: Thu, 15 Jan 2026 19:37:03 GMT  
		Size: 62.6 MB (62594900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ebd4c763d8b6cd3b0be5903a8169fce4c2a3b16ed7198f56bccc2f2ce70802`  
		Last Modified: Thu, 15 Jan 2026 19:36:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:e1e18dacd7adf4add2a92b430d2621d557642ee5f7ee14d1d74c74d03018d9fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1949861460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c31a38ccbe1df3dfd43cb0ea6c5a478451e019fbff2ddaf95ff22979d6e1a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 15 Jan 2026 19:34:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Jan 2026 19:34:57 GMT
ENV GIT_VERSION=2.48.1
# Thu, 15 Jan 2026 19:34:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 15 Jan 2026 19:35:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 15 Jan 2026 19:35:02 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 15 Jan 2026 19:36:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:36:28 GMT
ENV GOPATH=C:\go
# Thu, 15 Jan 2026 19:36:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 15 Jan 2026 19:36:35 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:38:18 GMT
RUN $url = 'https://dl.google.com/go/go1.25.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '19b4733b727ba5c611b5656187f3ac367d278d64c3d4199a845e39c0fdac5335'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 15 Jan 2026 19:38:21 GMT
WORKDIR C:\go
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
	-	`sha256:e0a9355121c1c656746840ac1667840551ca50eb91ad0fdd5998abd9d407f7ec`  
		Last Modified: Thu, 15 Jan 2026 19:38:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e650ad6dc6e066ce5e98eae46bc7fdc181bb94897c176a9fac4e5c33d06274`  
		Last Modified: Thu, 15 Jan 2026 19:38:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0059e169699b2133b64196e2053a699198a865461c46920627374ed91ae3e3b`  
		Last Modified: Thu, 15 Jan 2026 19:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c3479ac13b4f0fad21eaa97d5868653c2de98db906e73faf9af41936565c85`  
		Last Modified: Thu, 15 Jan 2026 19:38:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2f972e1fb7c232eee99601e54d6ba5a085c78284136a04bd1997110e6ed0e0`  
		Last Modified: Thu, 15 Jan 2026 19:38:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dded11f6514d2c10ac7774fdc2b1aed3edd4b6df953de96fe28c8747242f052`  
		Last Modified: Thu, 15 Jan 2026 19:38:33 GMT  
		Size: 51.4 MB (51350079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5035611c4ee80cdb6260d1bf9958289618852a8c763eaa2d57a2879e6190a300`  
		Last Modified: Thu, 15 Jan 2026 19:38:25 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12f97a129fa2c30c4b78a7bbde3cc80c9b460cbadb80e26d8d224325a16b0b`  
		Last Modified: Thu, 15 Jan 2026 19:38:25 GMT  
		Size: 306.4 KB (306414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c766b55e02ffebe111ee9e49a75c64daea8c2f1b370a37e3e6251fb947b14a3b`  
		Last Modified: Thu, 15 Jan 2026 19:38:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dac534bccb1f1636aff5bafa24595f20ebd2580f7bc281d5ae023b536612b9`  
		Last Modified: Thu, 15 Jan 2026 19:38:36 GMT  
		Size: 62.5 MB (62535180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0430c60056b7aed784a829b8b012a32c9aa85cae0a1930bc8aa2684258b53de4`  
		Last Modified: Thu, 15 Jan 2026 19:38:25 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
