## `couchbase:enterprise-7.6.4`

```console
$ docker pull couchbase@sha256:e7cbdc8f52a154f77be22e2eeb8dea0ca9b30ecc7f4d32be809ab1149913a3db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:3cc07c7422b38f8900fcb7e1a7e7a06cb9c86c12a55794f1843d35d9cf84894f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771642681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939f798f6f0c932856d8cb002e5c5ff865b4069004bf7420ffef10633622c991`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:15:13 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:15:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:15:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:15:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:15:39 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:17:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 13 Nov 2025 23:18:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:18:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:18:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:18:14 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:18:14 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:18:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246400c3a2b2827551a23aa3aacbe819f03469e524fa46832607becb66036975`  
		Last Modified: Thu, 13 Nov 2025 23:17:05 GMT  
		Size: 39.3 MB (39298958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87d80ddd3a9982b19e2e61b1173aaf3f20cff7d73526ef0fd2f56c00fa06c53`  
		Last Modified: Thu, 13 Nov 2025 23:16:58 GMT  
		Size: 926.8 KB (926777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b828b4ceeecce6d495e26b1476c39631751797e91659a9cdb0051c44b050c`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86ef83caa6e635fca885692a22479f526062cf7dfc2c209b9b325621892a66b`  
		Last Modified: Fri, 14 Nov 2025 08:30:46 GMT  
		Size: 701.9 MB (701874965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ea14f014cc8c162c7c88e965dfad0b4c41b453861db8a976982c69bd29fe8a`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d499cc07c09e723c3beb5b9809359ff7d78b3f2fdc0d924b0b2f5bec889f9c58`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a4ec4e4b6234acb5719cb16128791633b57b420a88275cf7b4d9a843f11362`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c8caea9a3e8c5ebe191c43369e5ad0e76baee95c3497d254a350ca9761f4bd`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986066036434256e35688cf6becb5f854def278c3c77b93173aa70437ee10d1`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe779cd0a3a1af07366815edd9b89020711526eb9d95466222f5bc7aa1853568`  
		Last Modified: Thu, 13 Nov 2025 23:19:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:4edf4892a559453483cdb0ae5bbdc126817ad1a527fbb6251cbc2bd49dc3e9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e130141905bebd604bc4891d0cd1a5b76269a466ece2ea202045e109ed4bdf5`

```dockerfile
```

-	Layers:
	-	`sha256:47c186aea6b466c7eb3bf46153d92596948466a7595a901c3669e2809b27e44d`  
		Last Modified: Fri, 14 Nov 2025 03:35:18 GMT  
		Size: 35.8 KB (35773 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:024899a81a4eb57812094752b2978e382e9da8828f55214347857a638cfcd4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.6 MB (742593712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6299ae352f581d04b26582dd8fbbe9743b71ee49e9a0f0adca0fbf4701d20137`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:14:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:14:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:14:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:14:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:15:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Thu, 13 Nov 2025 23:15:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:15:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 13 Nov 2025 23:16:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:16:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:16:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:16:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:16:07 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:16:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:16:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf24b459cdfde9988843d90f46292625fc991bcbe4e12a72ab3a4635fd0776`  
		Last Modified: Thu, 13 Nov 2025 23:17:22 GMT  
		Size: 38.9 MB (38872023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e259ba7db1b9866f2c7cc3171eed892b14011f71b62f9a841d607e2d5df6631`  
		Last Modified: Thu, 13 Nov 2025 23:17:18 GMT  
		Size: 775.2 KB (775240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4340f5ad404a2216b8b723effb87c6259a85515a2854712eb6816858d058d`  
		Last Modified: Thu, 13 Nov 2025 23:17:17 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91210cad7e31438e9b72319213204c290c84c9b69943c07c752e757f4b8a0460`  
		Last Modified: Fri, 14 Nov 2025 22:07:02 GMT  
		Size: 675.6 MB (675557386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6032a5629f3f03cb3341a6f3bebc6b556f5a18f4438e6378f63281fe1cd7c6c`  
		Last Modified: Thu, 13 Nov 2025 23:17:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24d9ce5a9121a1ea24c17c6b1ed6355203a5489f43aed1526df4520199c4069`  
		Last Modified: Thu, 13 Nov 2025 23:17:18 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b53569ed277df154cb198875310d096fc43c1e771ca16ff03b2a2ee7f0f4f0`  
		Last Modified: Thu, 13 Nov 2025 23:17:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518ca0486100357fcd0d79add20c1f5d871f0ce0a56082f1191e7a23ba2a7c9`  
		Last Modified: Thu, 13 Nov 2025 23:17:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a06736050ad40b3577437a39a296f8ffa6c39449c8917dd2727a0185373916`  
		Last Modified: Thu, 13 Nov 2025 23:17:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f815dbad41aefe7c6384715dcf45359af39d021e5452c32d1def716dc4cb20`  
		Last Modified: Thu, 13 Nov 2025 23:16:57 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:f069ae08bc54edbbc564579050aa7eb4f38c4fa986d4e736f55043a62de3e426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902c39bbede7786d96f53a3c1e13c66d80ab0595e5dac1cf1abdcbfb4544a5d`

```dockerfile
```

-	Layers:
	-	`sha256:3fba57769b6cad14758fcabb68af3d0f603f90da55013049136175e612171804`  
		Last Modified: Fri, 14 Nov 2025 03:35:21 GMT  
		Size: 36.0 KB (35958 bytes)  
		MIME: application/vnd.in-toto+json
