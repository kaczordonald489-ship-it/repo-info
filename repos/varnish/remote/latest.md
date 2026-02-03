## `varnish:latest`

```console
$ docker pull varnish@sha256:226a23129ecf7c69d670e409fc8be49d1c1bfc2fad8557f66f62dd8dbdcc3fe1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:d352c9681d9a8ba5e56689cafcdeaf13be9b4f3eb50702e8cdf60aa2462e8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121962336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d60cea63dbf0bfb59e087cd0da723866bb4b226c32f3e2bde8235fed975db9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:42:21 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:42:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:42:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:42:21 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:42:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:42:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:42:21 GMT
USER varnish
# Tue, 03 Feb 2026 02:42:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:42:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ce5385998e16a6fb7ef0226d1f20b45298bed9dc060e1bf28d50b55ab6b44`  
		Last Modified: Tue, 03 Feb 2026 02:42:36 GMT  
		Size: 92.2 MB (92180627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975aae4b8d991a67a2469a23763d6acfdf59ac627560c2f790c080c24018d71`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850971c09b6d0682278837f5c6a4e9d01b30dccf52df0692fdf7a668c729420a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f107400f6a38a9314a93b12c9392f94b30b5f795125cf51885a1dbe8c0c49a`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:362009b8c48f6e6c1df889fed612bea5e9606c328aa1844be7840919bae04d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e6c2c755a94af44f9b0afc723c139b2357ebdcd63288ebae6773749f97cdf`

```dockerfile
```

-	Layers:
	-	`sha256:d5d34eb7eddcf079b45cf5c06eebd4f2d4f2e58f53d5cd95788bbd42eb37fb80`  
		Last Modified: Tue, 03 Feb 2026 02:42:34 GMT  
		Size: 21.5 KB (21545 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cf120eda11e2042d4d3b042a843ba90d71839f7ea5da41b44631b161444b5138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12599516796d11291cda900c5d30ad79d4ffb66b35e6a2cdb49dac94423d3a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:45:15 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 03 Feb 2026 02:45:15 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VARNISH_VERSION_NUMBER=8.0.0-4
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 03 Feb 2026 02:45:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 03 Feb 2026 02:45:15 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 03 Feb 2026 02:45:15 GMT
ENV VSM_NOPID=1
# Tue, 03 Feb 2026 02:45:15 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.0-4 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         if [ "$(dpkg --print-architecture)" = "amd64" ]; then         EXTRA_VMODS="vmod-cfg=${VARNISH_VERSION}";     else         EXTRA_VMODS= ;     fi;     apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				${EXTRA_VMODS} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
WORKDIR /etc/varnish
# Tue, 03 Feb 2026 02:45:15 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 03 Feb 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 03 Feb 2026 02:45:15 GMT
USER varnish
# Tue, 03 Feb 2026 02:45:15 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 03 Feb 2026 02:45:15 GMT
CMD []
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd55ca0600e6a3e876c49088103397b7b05e6094487e7a60107919cd3051bd`  
		Last Modified: Tue, 03 Feb 2026 02:45:29 GMT  
		Size: 84.5 MB (84532762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66978ff33f084ea694488f026f19a130f485eb75eb669ee030fb8248faef72af`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad63af1ab6603e791221ce68a695341b32ed14e8a5be37150f8c6a65a50df61`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278d8bcf8a98fe62140fe7ddf9d61e65feef87d547df1c78ea939529cf33bb3`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:c782dfe175af659dbef2371903f4af0180af017bc4eb89ea45965a4f385f8b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de953c67739aa87eb699753315560c3e5f898d721b253a78ee9b0bece90d32`

```dockerfile
```

-	Layers:
	-	`sha256:76d12f419243f487cfd1893ef954181ed8dbeaeb13f0ff1923e98d6f37cf3ad0`  
		Last Modified: Tue, 03 Feb 2026 02:45:27 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json
