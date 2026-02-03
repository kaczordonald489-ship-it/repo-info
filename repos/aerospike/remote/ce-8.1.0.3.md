## `aerospike:ce-8.1.0.3`

```console
$ docker pull aerospike@sha256:09e6a449646758001dd1b5ca127e042098acf4960cb29d06723cc9656a3d0c0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:fa382b4cb9a341e123c926f7336f3e9d2643bf236c7c0aea6e5555235e0b4ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81502269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f7c313b6ee21b6a813dc716ddac8c31937593b5d17f84fb02642469a45ecbf`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:13 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 15 Jan 2026 22:08:13 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 15 Jan 2026 22:08:13 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 15 Jan 2026 22:08:13 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Thu, 15 Jan 2026 22:08:13 GMT
ARG AEROSPIKE_SHA_X86_64=2454a4cf88502754ba93281092d57620b8e882611aa2c3c94f89331adb145932
# Thu, 15 Jan 2026 22:08:13 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Thu, 15 Jan 2026 22:08:13 GMT
ARG AEROSPIKE_SHA_AARCH64=4d3582d8af215f58b1d4dd88f9249fec70d583f92a4ee98ecb9472ac6e2f3fb6
# Thu, 15 Jan 2026 22:08:13 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 15 Jan 2026 22:08:13 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=2454a4cf88502754ba93281092d57620b8e882611aa2c3c94f89331adb145932 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=4d3582d8af215f58b1d4dd88f9249fec70d583f92a4ee98ecb9472ac6e2f3fb6
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 15 Jan 2026 22:08:13 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 15 Jan 2026 22:08:13 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 15 Jan 2026 22:08:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:08:13 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 15 Jan 2026 22:08:13 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b8511f6375ab84f476184b27ed6e8e1dc9e9546f1e5ab4acd8e7c0852150d2`  
		Last Modified: Thu, 15 Jan 2026 22:08:26 GMT  
		Size: 51.8 MB (51773957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3682aef4f8dd955856de80d0b0d9a41e997c8a73f9f3fefcad270f955592ee6a`  
		Last Modified: Thu, 15 Jan 2026 22:08:24 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd80a23defd4dd4a1e7194cbd183de33ded34cc1b3671667da48bc4a61029f58`  
		Last Modified: Thu, 15 Jan 2026 22:08:24 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:69fb3c2cd871bc32dab5b3ee3dbe9ebe120940dd500e249366515e45db838316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e36ecf9105e3b6803956e5fcc1b9027483d4ff6859109356d978500aa8eb2ce`

```dockerfile
```

-	Layers:
	-	`sha256:a44f6fd922922f40580d5890c3d4d0d62a867ea6bcb24b51945abe1e47eb233a`  
		Last Modified: Thu, 15 Jan 2026 22:08:24 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a9fa3c675043db3c91df4df76ff857d5f53f38923456acf8faaaea021c749c`  
		Last Modified: Thu, 15 Jan 2026 22:08:24 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:e4f38d757ff4bf333b3f2f177dc9568923ca73314067b37027df0aec7c4809f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79865138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c098703ff8d5a8ce005829deeae9d2a7977a2765f9f87e9d63a80f8409830`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:18 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 15 Jan 2026 22:08:18 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 15 Jan 2026 22:08:18 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 15 Jan 2026 22:08:18 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Thu, 15 Jan 2026 22:08:18 GMT
ARG AEROSPIKE_SHA_X86_64=2454a4cf88502754ba93281092d57620b8e882611aa2c3c94f89331adb145932
# Thu, 15 Jan 2026 22:08:18 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Thu, 15 Jan 2026 22:08:18 GMT
ARG AEROSPIKE_SHA_AARCH64=4d3582d8af215f58b1d4dd88f9249fec70d583f92a4ee98ecb9472ac6e2f3fb6
# Thu, 15 Jan 2026 22:08:18 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 15 Jan 2026 22:08:18 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=2454a4cf88502754ba93281092d57620b8e882611aa2c3c94f89331adb145932 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.3/aerospike-server-community_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=4d3582d8af215f58b1d4dd88f9249fec70d583f92a4ee98ecb9472ac6e2f3fb6
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 15 Jan 2026 22:08:18 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 15 Jan 2026 22:08:18 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 15 Jan 2026 22:08:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:08:18 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 15 Jan 2026 22:08:18 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021bd27dca920305bdea6980d957f70b54b9e54869fb55817559b1dfe6a91ed3`  
		Last Modified: Thu, 15 Jan 2026 22:08:31 GMT  
		Size: 51.0 MB (50999016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31650bc093697c08efe6da002287c689dbff1503a01c0d81bb8c7f57476a48e5`  
		Last Modified: Thu, 15 Jan 2026 22:08:30 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c01b77e708d628a761deb5959601b22db4503271565e9a36e44738486f677b`  
		Last Modified: Thu, 15 Jan 2026 22:08:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:51e70f63781d509f72af8dd6c785d24700a64981ce1bffcc23daca7c9bb6d15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76ba472ec952ae118867fd75e129fa9c67a69551efe0d0360dcce47439896f`

```dockerfile
```

-	Layers:
	-	`sha256:e937f64aeaf824250030df117b6d60d8f9e9b53b95f14167412ce515597d1a4f`  
		Last Modified: Thu, 15 Jan 2026 22:08:30 GMT  
		Size: 2.2 MB (2184592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4b0c0eed6809ade50599c336b88190ab383fec9f9f6768996485056dd37f15`  
		Last Modified: Thu, 15 Jan 2026 22:08:30 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json
