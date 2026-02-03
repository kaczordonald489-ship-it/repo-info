## `openjdk:26-ea-jdk`

```console
$ docker pull openjdk@sha256:fa8b1459aae3f5103032a2dc74952a40f9f965ee00ff36e597c657b1e619abe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b2e2309cba1701086e81177bfb0a7e1a333787d6a84a2d796cff7b48204829ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313480294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9066ae383c3c30fca58e78b9f176b4192f7676bb19464896a7dbe2ef422e2f4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:45 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:45 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 31 Jan 2026 00:12:37 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:37 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:37 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:12:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c21bb7e51cd3b6a6786c5cece22bd0b261e4bf013a53ecb6f4dce35d38c40f23`  
		Last Modified: Fri, 30 Jan 2026 23:39:56 GMT  
		Size: 47.3 MB (47313808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e17583089494c0004a8a6d29cd8dee1e937c78a90941033e785c35ff443798`  
		Last Modified: Sat, 31 Jan 2026 00:13:01 GMT  
		Size: 38.3 MB (38297911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61030c8b1f5865b4d106632166341d13875e933c8e8a8eedb7840a31946d53`  
		Last Modified: Sat, 31 Jan 2026 00:13:06 GMT  
		Size: 227.9 MB (227868575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:11196353163042c105d14b1d7ac16151dc010b0b49077b6f01ac858fe570356f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c258b3a17a0412944a1873a1ccf2c1e41a03126c2ea0ee3e08bbd42300586a6`

```dockerfile
```

-	Layers:
	-	`sha256:f1332ed3e8fee039e8bb00e12ca04caede9e3bc2e8438018a1739d03b07d5fb5`  
		Last Modified: Sat, 31 Jan 2026 00:13:00 GMT  
		Size: 3.7 MB (3655391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9168f1633642457f2e87bb274e9a8e92c5759e8d0ff47f42fb996858ed3473c9`  
		Last Modified: Sat, 31 Jan 2026 00:12:59 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f4baeadc5367b5a5fe3778f6dd876c3427b6ca7ae4c3e7a691036d035e898864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310379910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95daa2ab27f8ad25a3baf7336542c7048dd09b1b5f4725a55d02bb4235d0362f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 Jan 2026 23:39:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 Jan 2026 23:39:10 GMT
CMD ["/bin/bash"]
# Sat, 31 Jan 2026 00:12:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 31 Jan 2026 00:12:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 31 Jan 2026 00:12:41 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 31 Jan 2026 00:12:41 GMT
ENV LANG=C.UTF-8
# Sat, 31 Jan 2026 00:12:41 GMT
ENV JAVA_VERSION=26-ea+33
# Sat, 31 Jan 2026 00:12:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 31 Jan 2026 00:12:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9490d79385bda9b2c792f8c72c8b1a55f5d14188d676eda2ed07199c47f59396`  
		Last Modified: Fri, 30 Jan 2026 23:39:22 GMT  
		Size: 45.9 MB (45901641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9235c10a46cdf0d1a0979d60b325ded20728f66c0dd28f7ee80374f3fee9c32`  
		Last Modified: Sat, 31 Jan 2026 00:13:04 GMT  
		Size: 38.7 MB (38693764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef027fbf950aadf2db1fa014f00ceb33469ef8a4817392c542a47e4e945575aa`  
		Last Modified: Sat, 31 Jan 2026 00:13:07 GMT  
		Size: 225.8 MB (225784505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:af8071d64d439669c022671449ea357a75f47e03e10c28b1394101d4eb03a829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee5423a82af3b5f492fd987d2b3c56a15f553df7fe8644f078d2e5d99d12914`

```dockerfile
```

-	Layers:
	-	`sha256:2eb23639ed01ae364f976645f7bec05b8af2eb0639ec501c62c0be581732ed22`  
		Last Modified: Sat, 31 Jan 2026 00:13:02 GMT  
		Size: 3.7 MB (3653081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c995dcb08e45c352e5382e75be2cd2a84dd3b992f11d20f4751c979b15d875`  
		Last Modified: Sat, 31 Jan 2026 00:13:02 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:26729fbb19a4dadc5e6b522ee4595ebabd6dfabb6ce89481ae06c6b9eef7d72f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720897038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de885a2f00bbf11e302617f7c24851f2eed6f0c135d63adf74b1722fb4a41591`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 30 Jan 2026 23:39:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:39:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:39:28 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 30 Jan 2026 23:39:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:39:35 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:39:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:39:36 GMT
ENV JAVA_SHA256=1613acc47081355dcb54aca5db4a0cc088734861b42bd254657ab88fd50944ec
# Fri, 30 Jan 2026 23:40:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6d232d985647bac5bb6eb0323db9939978fe35ce0400678ab358bb526cbbf6`  
		Last Modified: Fri, 30 Jan 2026 23:40:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b8329748e243b493f5f5841dcae9b09c85e7ed14c65a0e712c34f7fb05072d`  
		Last Modified: Fri, 30 Jan 2026 23:40:23 GMT  
		Size: 416.9 KB (416880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706ba72d33ad14c1e782a84ded0723ca55fccda4e202a29137e634a99469292`  
		Last Modified: Fri, 30 Jan 2026 23:40:22 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb2831b370174c7dd2acdaf6674ebebf64c87ce135b0bf93f0be2ad538de9b`  
		Last Modified: Fri, 30 Jan 2026 23:40:23 GMT  
		Size: 401.0 KB (401039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0250baab51d53441f7e2fd1ce28b784c9d54a751e17fef8a73af06783510a1cc`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c81b233b494a09ad1fc903642ffb0fd16b1920990675e33121899fb876b9d5`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd73c7832edd93b2f1eed1f16b8df0712688604d326a2b5271494ee9df802a4`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc74dd3f905a5624dbc9e410ba273338c8db410e063d54a81b0d7a4150bc496`  
		Last Modified: Fri, 30 Jan 2026 23:40:36 GMT  
		Size: 224.3 MB (224310912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfba226fa310cccf26760ee72738e8d5d8ef91dd20d7a6862c7cd61e2be1543`  
		Last Modified: Fri, 30 Jan 2026 23:40:21 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:65c3c46583d86ee7e71d869b007a3a8f8d58766344b310b13d2fb77fc4264f1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060828234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf5d89d3e7e8a3ec85b952c5dd3b2fc9226e240560ed8fbf7df510e8600dc3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Fri, 30 Jan 2026 23:39:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 30 Jan 2026 23:40:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:36 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 30 Jan 2026 23:40:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:40:43 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_windows-x64_bin.zip
# Fri, 30 Jan 2026 23:40:45 GMT
ENV JAVA_SHA256=1613acc47081355dcb54aca5db4a0cc088734861b42bd254657ab88fd50944ec
# Fri, 30 Jan 2026 23:42:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Jan 2026 23:42:15 GMT
CMD ["jshell"]
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
	-	`sha256:5bf12dbbc63ade9ffa2bc8a97522ec0c9b93b94327d9d4d29b884d5562aad768`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ee7c5e9acd94a15471693e7c33250c1f40aefbf482cd02643fa42837823b54`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 512.6 KB (512605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f00ae2fa10bcf5329922222393accd763a60505a0ec64762c77a94c47eb78`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566c6287bc76d30a151af0b81f492aa72ba379b10b405776dda15f8650607635`  
		Last Modified: Fri, 30 Jan 2026 23:42:25 GMT  
		Size: 360.4 KB (360395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016069b05e82df74afcb392c6275dc7fc7028e2b5d80cc1989245efdedc6de3d`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d663aea12bc6c12ce098ed928c6a394935463f99431072dba8242a9f792ba23`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e1c2842a2b8b5c68d9d5dda9b03b8444904fdc8217cd5419183e31323bbf88`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8445808894c0c536502816e0d02fa3aaf47b40a34dc4c219a44352b9af76c496`  
		Last Modified: Fri, 30 Jan 2026 23:42:39 GMT  
		Size: 224.3 MB (224288220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628ff06d5628fdbd128982c385f15f8b390733f29b5e7d3ef4608edc1da749d`  
		Last Modified: Fri, 30 Jan 2026 23:42:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
