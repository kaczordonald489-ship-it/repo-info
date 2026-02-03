## `aerospike:ee-8.1.0.3`

```console
$ docker pull aerospike@sha256:054add84a704eabaa06730eca9211d51aab2534aca5cced087c9a22295ffd1bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:73bb4c8cc6dff1fa30b44d0bff07f3eac16212ed841f38568a5cfadadce7fba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83603822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d204f4913b9cf7af8c7102352ce9a5cb7b640d4bfa7839c2b16a140795e2624`
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
# Thu, 15 Jan 2026 22:07:49 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 15 Jan 2026 22:07:49 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 15 Jan 2026 22:07:49 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 15 Jan 2026 22:07:49 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Thu, 15 Jan 2026 22:07:49 GMT
ARG AEROSPIKE_SHA_X86_64=f027dbb12535b466fa391785fe4b1d644fc34af1c1693d0410947e0e8b9fab28
# Thu, 15 Jan 2026 22:07:49 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Thu, 15 Jan 2026 22:07:49 GMT
ARG AEROSPIKE_SHA_AARCH64=bffddf8919a801788bf005c626d4780528374f8ffa51ae1c18ae57008148f1ff
# Thu, 15 Jan 2026 22:07:49 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 15 Jan 2026 22:07:49 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f027dbb12535b466fa391785fe4b1d644fc34af1c1693d0410947e0e8b9fab28 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=bffddf8919a801788bf005c626d4780528374f8ffa51ae1c18ae57008148f1ff
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 15 Jan 2026 22:07:49 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 15 Jan 2026 22:07:49 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 15 Jan 2026 22:07:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:07:49 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 15 Jan 2026 22:07:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588ca00b11840bdb10b4443964f03ddc09126080b87e9979819494e8b36cb84b`  
		Last Modified: Thu, 15 Jan 2026 22:08:02 GMT  
		Size: 53.9 MB (53875513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c021f62c861db42667b263e2ee708cd8fdbf51894035fe22bdf7b62b76677967`  
		Last Modified: Thu, 15 Jan 2026 22:08:00 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675ff4125cdca37eb2fe69625c5ba256c6ec97ce823147dd8706b39a1716f818`  
		Last Modified: Thu, 15 Jan 2026 22:08:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:9013a1e8371b157b7c8c15d22740605a5449ff3a78714c944348c1d4b12c78c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0ea6fce080b62f14a3d8e9bae09031ae4bce06825f8880f2c5bbc9b0200512`

```dockerfile
```

-	Layers:
	-	`sha256:84a1a49113022e86aceabd707813a06bb8ac16a5dac7838e74022aab2fc1ff8a`  
		Last Modified: Thu, 15 Jan 2026 22:08:00 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79fe64a0a58b957876e976ae11160d19aa2438ba9bb46c993e55f1cd4291f76`  
		Last Modified: Thu, 15 Jan 2026 22:08:00 GMT  
		Size: 29.0 KB (28984 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:420137f9e28d64292751ac57f1dfc66a70f101922d16ad7dcc4f3d20842737bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81957401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4975af760ae9fd971c761c2309153989f47cca39a87255d2e01aea6f926aa12b`
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
# Thu, 15 Jan 2026 22:07:41 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 15 Jan 2026 22:07:41 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 15 Jan 2026 22:07:41 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 15 Jan 2026 22:07:41 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Thu, 15 Jan 2026 22:07:41 GMT
ARG AEROSPIKE_SHA_X86_64=f027dbb12535b466fa391785fe4b1d644fc34af1c1693d0410947e0e8b9fab28
# Thu, 15 Jan 2026 22:07:41 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Thu, 15 Jan 2026 22:07:41 GMT
ARG AEROSPIKE_SHA_AARCH64=bffddf8919a801788bf005c626d4780528374f8ffa51ae1c18ae57008148f1ff
# Thu, 15 Jan 2026 22:07:41 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 15 Jan 2026 22:07:41 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f027dbb12535b466fa391785fe4b1d644fc34af1c1693d0410947e0e8b9fab28 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.3/aerospike-server-enterprise_8.1.0.3_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=bffddf8919a801788bf005c626d4780528374f8ffa51ae1c18ae57008148f1ff
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 15 Jan 2026 22:07:41 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 15 Jan 2026 22:07:41 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 15 Jan 2026 22:07:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:07:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 15 Jan 2026 22:07:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85767701148ead146ecce1bb3878b9f59ddf28dc01039872e7fddb33b6b6c2b3`  
		Last Modified: Thu, 15 Jan 2026 22:07:54 GMT  
		Size: 53.1 MB (53091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8cfe174dc56bbf6bd161f3a715751a825d3a223bf6711f1ecb43700a778fe3`  
		Last Modified: Thu, 15 Jan 2026 22:07:52 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91303030313c32f3e5728921f984a12249922e16dda17b0d09779187cb926dbe`  
		Last Modified: Thu, 15 Jan 2026 22:07:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:8f9a95c2ef565f31dfc6d375a3160285f60785c18548aa6cd9108bb5db497160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4dcd06787034cbe88d29e8bd8d12dd3bd25b5573895dd17403d9449aafd907`

```dockerfile
```

-	Layers:
	-	`sha256:28f1d1e58f814a4f025ffcee7e1eff57ccb92af0af0a442037a6cc1b6f2b2faf`  
		Last Modified: Thu, 15 Jan 2026 22:07:52 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fb90ce224dca96bf9dbf4b2f06082a27a0c661982cf7bb895e2f20d7a1f6aa`  
		Last Modified: Thu, 15 Jan 2026 22:07:52 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json
