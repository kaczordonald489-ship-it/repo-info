## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:c2872a10c9d0906c281c3bfb6e8bb7624f4db9e8ae170458220573187379974f
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
$ docker pull couchdb@sha256:f91985796d271187f35f76bf08306d130d6cf3c062f8b113bbbf092231db206a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0f21da0e98ad7db726cca7f638833b17fd724957b9a40f42d953da9558ed08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:12:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 05:12:56 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 05:13:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:13:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:13:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 05:13:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 05:13:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:13:15 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 05:13:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 05:13:21 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 05:13:21 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 05:13:21 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 05:13:21 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6228c009e91bf667f82c41db51eaea2b6f3beed5a93c33f5bb173b3069297d`  
		Last Modified: Tue, 18 Nov 2025 05:13:45 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da6e9afc51e0f46ebf19787901b6f37f5455931f1828ee7c9460b961c605513`  
		Last Modified: Tue, 18 Nov 2025 05:13:46 GMT  
		Size: 7.9 MB (7881789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ced51fe2197e90d075690df1b22e8b44f2b069b17132cc012a36119e36113`  
		Last Modified: Tue, 18 Nov 2025 05:13:55 GMT  
		Size: 77.4 MB (77380487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb7b9035a9203616dc756d46c1abc2f1cf850eb204771c1b32c9c95ab0613d`  
		Last Modified: Tue, 18 Nov 2025 05:13:45 GMT  
		Size: 424.1 KB (424108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a798e33b014c7450212f47a7220c4172994c060da8d8005c1019bcbdf606a7d`  
		Last Modified: Tue, 18 Nov 2025 05:13:45 GMT  
		Size: 99.5 KB (99512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01906cc27664d889d594ebe981231d4527154da71014eb855c0410640da1f799`  
		Last Modified: Tue, 18 Nov 2025 05:13:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caab9315a79d0bfba1892d76d9adfcc1c0ae29799a54a2ac1b3dc5c06b3f75`  
		Last Modified: Tue, 18 Nov 2025 05:13:54 GMT  
		Size: 42.4 MB (42436380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd6d941e34fc34f1e286e108b2ab40af7f8061e6ee74a432feb22a87a88613`  
		Last Modified: Tue, 18 Nov 2025 05:13:45 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a90fd1884986a2e37f4ec74d45a031d5460b1eea15c6bf7be5079380d0a10f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1ed4de0bed5378e4fdabc6f24f8b5630a65407a8694679dd647be474da277a`

```dockerfile
```

-	Layers:
	-	`sha256:1dc8d6bd5b33d39d5a4ccbfc1ddad822c61f247ba793b913e9029f020c9db955`  
		Last Modified: Tue, 18 Nov 2025 08:33:48 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f29b40dd78ddc0a8cd507cc01f658fc3cf9ed5dcdc161d8dffa4f640810c348`  
		Last Modified: Tue, 18 Nov 2025 08:33:48 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:544fd2610735f66997f2dc3ea47343f29126794307217fdab34cc896292886fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53dda8263a1e2cced1df9591e99bf4e8de27559768d24d1a53dcdf6a6bcf9fc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 03:33:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 03:33:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 03:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 03:34:00 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:34:00 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 03:34:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 03:34:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 03:34:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d170929f5122b754e9c3b75c81f5ccce945c639b120cf7fd9f04de497d3351`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d122aab947d7f0b37352ff25d869519635be1a0e7861aea35a7607930d7048`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 7.7 MB (7692053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712de1723319370a513b2ce6b80dfe68316e938066ef53bd751fb7913363595`  
		Last Modified: Tue, 18 Nov 2025 03:34:37 GMT  
		Size: 76.7 MB (76691571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbab553627aa3a0f31a1a13d6435b96fa20c948bb8f0a06acd9ce3af5ee46c`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 392.7 KB (392661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4afbad864dfc76385d9a0180412ac0f75762270e3310fb788e9fd11f3b4c72`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 99.4 KB (99437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5123d1a7c8c978a9b8d8ea941fa30415dee531acb7551c51886b2c3eb5403a1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0409338ca2ef2307306a8c6ce9d0553d3e006645a788373fa0b84faac326d9a`  
		Last Modified: Tue, 18 Nov 2025 03:34:36 GMT  
		Size: 42.3 MB (42339007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341e7b0042637cf21bf2c7c5d35faa8cf23612d5f81cf113f113d3a1cf06fe1`  
		Last Modified: Tue, 18 Nov 2025 03:34:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7fb5776f8220586ddd041b8b27727ad9eb417b5ae49c98b78444d6d0ed4f4ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08692c5b65246b53c1db3b39b2d49b3982af4f0b68425f674dad749cd5907123`

```dockerfile
```

-	Layers:
	-	`sha256:5b6483cab95ef058cfba5af9eedba8c2f72f1ebc0ee7a7359369b99d70242044`  
		Last Modified: Tue, 18 Nov 2025 05:34:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc566dff9630765cf5b25f3bb6027d91360ac02f2b43f545da39a7656afd750`  
		Last Modified: Tue, 18 Nov 2025 05:34:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:6d105ae4c3cfb487453dc42ebb84bca2d760070072cd8b8ba81a7f2c31a0dadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb4ce24ab1a4f47af64aee459172c19dc5667f1c122869b8bbc9af97e1a28a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:07:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 18 Nov 2025 04:07:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 18 Nov 2025 04:07:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 18 Nov 2025 04:07:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 18 Nov 2025 04:07:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 18 Nov 2025 04:07:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 18 Nov 2025 04:07:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 18 Nov 2025 04:07:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e87e61b486b2674141864f4363d98ded26c8f54e991336ad1d12e326c3a16`  
		Last Modified: Tue, 18 Nov 2025 04:08:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b605a2e7b31da747e5753f0ddab47bf42a62e40cee69c1047dc0c2d30f6b1`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 7.4 MB (7398114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d58478a99282a2368ea67171ded7641e1b0038caa802b2fe1670fb2deb9f8d`  
		Last Modified: Tue, 18 Nov 2025 04:08:30 GMT  
		Size: 73.1 MB (73143056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06a849564a0186d5596762b9c12ee8747f037baef6d3e1ba2c83a743389eb0`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 394.4 KB (394411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0e427d83599ac4b811cfd58210ecdb8178a62036d472729b26fc7d415de53`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 99.6 KB (99624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9210fddd0e0bc63c40f7d261245d3fbd05b4d939788283eb1d1a8daa30f9785d`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d59dccc95cb6f79dba3e6eb7001aedb61689abf7d6a7615729fad6451968d2`  
		Last Modified: Tue, 18 Nov 2025 04:08:25 GMT  
		Size: 42.2 MB (42164660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e79e6b7ddf0949aaf0d3c54dcebc276d1c2bf91c6cd77d8b0a437ebe5ffc4`  
		Last Modified: Tue, 18 Nov 2025 04:08:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:65e9e7614841fe27093ee627cfd01d6cc4373d76d7d6ee532430ce5c714310cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889ef69b339c0e8c0d511f4836014ae41b4de63f97c676e2e651ea26f39787e6`

```dockerfile
```

-	Layers:
	-	`sha256:949aba49bddf11115bacb751c3bd35f64dd18029e6a267d5bbdffd283f33afd6`  
		Last Modified: Tue, 18 Nov 2025 05:34:46 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6e59512c24b1e04b0c745da36168da8df9ae6ba95ba224c9ebd714bafbffa0`  
		Last Modified: Tue, 18 Nov 2025 05:34:47 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json
