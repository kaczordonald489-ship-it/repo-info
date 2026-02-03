## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:b97bfa2fa95443d80c05ebb793b6e5e659f24bd6975535d74369b0dfd883084d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:2b64016ceeedcbe65bec9fdf719a6f0520cfdeda292899f948b6f02ecd72aa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156454720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f8c67278d19a9a18cdec7e5a892300ef237a9fcb7816241ddfc8788de4735`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:43:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:43:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:44:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:44:07 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:44:07 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:44:13 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:44:13 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:44:13 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f1fc1251780f2123a88ec6b1625b1f161e25efd41504f70275dd8f31e9329`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5b07b90d99f75c07ac2962182cea4a914e329742759219dfe660055213a6b0`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 7.9 MB (7883128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83372eb1b6397a36f36e6013bece01cee7cedc014fe3c311f470925ff65780d2`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a88a440b80b25b36f61a176bd75bbc21ca304a8472923e1fb782a959cdcd37`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 424.2 KB (424191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7794c0a906c77aa52409af359f9083b620d147ff60ced85f511e3c9efbf7b`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 99.6 KB (99598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f1ccbf7f15bb9c4d67592591c93463832f045a5095f2390029a39828fe5b01`  
		Last Modified: Tue, 03 Feb 2026 02:44:31 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db2487c03661363dca2d3abbff43337442842d60496b36cf89965c61b4b675`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 42.4 MB (42436519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df68ccc130acb38f0147f5f25e98e16307e733aafc12d8fe390c61eeeec70d`  
		Last Modified: Tue, 03 Feb 2026 02:44:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e8e6d0b224a88404c2c544ef4ec64038b9451cf97397e54bcc80ffe6a324fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5b9b18ba252c2abc60b8ed958e735792e18d91541469a84c2ed7c00a35615`

```dockerfile
```

-	Layers:
	-	`sha256:326038181cc4d4767c5270a11f64e357cb051045d992d4f641600a02521311fa`  
		Last Modified: Tue, 03 Feb 2026 02:44:30 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84365dc8ddfed096f5d9a6f1a58b73cd21db638f5ff79daa6bb9be0048d37fd7`  
		Last Modified: Tue, 03 Feb 2026 02:44:29 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d1f2650c9099d0f2f6ba848301bfab15a269904a6bc5c36217153ccddec4fbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155332410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8094fff0d459a58514c533022b063c4ce73d30c1f56ecfce1549f313a16db815`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 02:46:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 02:46:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:47:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:47:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 02:47:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 02:47:07 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:47:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 02:47:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 02:47:14 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 02:47:14 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 02:47:14 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 02:47:14 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36344971d8a5ea00751efabaab342b256be3d9a7fc9b2d7db15df72db6f37d`  
		Last Modified: Tue, 03 Feb 2026 02:47:29 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e4cfb8b1fc58b427d0889b41eeef003f5d82452a52094a14f3fef7427f3ad1`  
		Last Modified: Tue, 03 Feb 2026 02:47:29 GMT  
		Size: 7.7 MB (7692623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d65cbc4b39fbbcf4a3203aa042533154fcb3bd35204a7605abc4bcc7aa62db5`  
		Last Modified: Tue, 03 Feb 2026 02:47:31 GMT  
		Size: 76.7 MB (76698762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f615ef6ce1a8b1fc5344e856282d74abf6b8881c683e97e27f970d63f63633b0`  
		Last Modified: Tue, 03 Feb 2026 02:47:29 GMT  
		Size: 392.8 KB (392759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ff03a9c29f4c483d899ab97898021ecb4cefe2e0181940c5b927ea2034d004`  
		Last Modified: Tue, 03 Feb 2026 02:47:30 GMT  
		Size: 99.5 KB (99488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997bd60bddec417c39c3a7402c6734c9855caccf6d385a68eb586a1431e166ba`  
		Last Modified: Tue, 03 Feb 2026 02:47:30 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3cf188abf72e41933a91a609363dee6ece8562259de5b26042731c41228921`  
		Last Modified: Tue, 03 Feb 2026 02:47:32 GMT  
		Size: 42.3 MB (42339071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbedbc14c8468772460a13602b14a305864d6a59bf933fe9905f8f5497eefabf`  
		Last Modified: Tue, 03 Feb 2026 02:47:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c024542f5640a3abba6562ec5aa1f83f475df6f5f64316309735cd289aa576de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccc1cede2e123dd27f46d87ed053eb3a23baf5e1e89afad1d1c5bb883054c15`

```dockerfile
```

-	Layers:
	-	`sha256:cc045ed98eee443ed7e0fadf31ba054a759f7ff0523dc92b7efb48029da2af89`  
		Last Modified: Tue, 03 Feb 2026 02:47:29 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0b2ed159e8385feece6b22ea67472dcf38bd04c2bde96f4dbfa5dd4b97ac01`  
		Last Modified: Tue, 03 Feb 2026 02:47:29 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:22dc44a88a0371f80361ab6f85a5b7d39458b202c85522dc7ebc658ded7ae3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150097020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09c5eaf4739c8c3e5790287157dc7d86b0374248f3234dcc0a370df426bfb5a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:45:47 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 03 Feb 2026 03:45:47 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 03 Feb 2026 03:45:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 03 Feb 2026 03:46:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 03 Feb 2026 03:46:08 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:08 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 03 Feb 2026 03:46:16 GMT
VOLUME [/opt/nouveau/data]
# Tue, 03 Feb 2026 03:46:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 03 Feb 2026 03:46:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb860f9d20bff7fff3a85718356f5a554630a0edef1b792a07e2f891c31e2e47`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bfe0ea53c745bcc02b9c320ebc361f18862f770f2a63f769ff6c59bc52096`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 7.4 MB (7398867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df89cda60390f6a4bc70aa899d6a3ad5c95a3be0e9e4be9b6dfef46b249e25b`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 73.2 MB (73153103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698866ee0126f695019926dac18f75d2468d0db7629c0a629c305e05daaef1f`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 394.5 KB (394482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc97975a9bb1f45325c001458ab917b47dd350cbd5f3a01066d5e0360dcf257`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 99.7 KB (99657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c10d1aa33dbbc68010a89d231eed3c5338967ea2aa309234c6729fbead0b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ec97a4a96a0cad87e65c19bae5cb4476e8a753023ce27074575c2f8e103b0`  
		Last Modified: Tue, 03 Feb 2026 03:46:40 GMT  
		Size: 42.2 MB (42164646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62682c9cfe85a9b667830d2cf0305ef7b2324664f19e6e84de8eb123d94b481d`  
		Last Modified: Tue, 03 Feb 2026 03:46:39 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:86dfe5c4619f7a3ff038b187699a59be7c657c4d7b11872406fac86e1f8ec333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb2292c9e53fad4174e4281b6cd5aec35a6c3ab33f6700814b6d62030254abf`

```dockerfile
```

-	Layers:
	-	`sha256:33c40b2d5f4d455f3d140993dc0be02e39beed228047c960ed3c21c55c8db8d9`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a7bb80c2b3c2960a931b6888cee83ac2e0223bb152adb2f5f1cba40b708861`  
		Last Modified: Tue, 03 Feb 2026 03:46:37 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json
