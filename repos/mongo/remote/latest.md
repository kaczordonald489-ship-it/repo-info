## `mongo:latest`

```console
$ docker pull mongo@sha256:6f55a078e025aa29fea2826c82f67ff2f774b82efd816c4c30bbfe67904f0bb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:f480daf5d2787802b36bb879f113bdf25029e2ab701ff68b3c4e8dc7a66b7ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330002116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45787d3b0f929dcf0d2708e49957282a491813e1bf01287f2d044814d090ac37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Wed, 28 Jan 2026 18:56:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 28 Jan 2026 18:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 18:56:56 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 28 Jan 2026 18:56:56 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 28 Jan 2026 18:56:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 28 Jan 2026 18:56:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 28 Jan 2026 18:56:56 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 28 Jan 2026 18:56:56 GMT
ENV MONGO_MAJOR=8.2
# Wed, 28 Jan 2026 18:56:56 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 18:57:13 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 28 Jan 2026 18:57:13 GMT
VOLUME [/data/db /data/configdb]
# Wed, 28 Jan 2026 18:57:13 GMT
ENV HOME=/data/db
# Wed, 28 Jan 2026 18:57:13 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 28 Jan 2026 18:57:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:57:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:57:13 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 28 Jan 2026 18:57:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17b8d43140946731389bf3cc1ca05847a9c488a9603a1abdb2448df5fd24a99`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d2ce657269c2f06466e8da040935392c4f8d6ee561f43bd8cd2362ba04c56`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 3.9 MB (3914676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a440936c320dc21725487831f112a53d43704f67ae4c7059b14d88be53655`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 933.9 KB (933850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46608f94114e4075284ad00f4468543d985faa144907a1381a586343674e36`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389db226dfbc6c51694a5f4ce48341dc20ca22903da4145d3d631af0dff6d2e1`  
		Last Modified: Wed, 28 Jan 2026 18:57:53 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36be6857282d0119eb6c56dccb98a19eff518c5c496b5dde9da24613554f4f3f`  
		Last Modified: Wed, 28 Jan 2026 18:57:59 GMT  
		Size: 295.4 MB (295420979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f646e1be2da4fda569d96c41dd8bbe92bf130a73de172afeb871ebb8f29f3a4`  
		Last Modified: Wed, 28 Jan 2026 18:57:53 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:32913891f90f154049a788c8caafb2877b5acd5eee19ca2d1dacd8685c24eb53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3815d2579e28cba53e6432d24b63c9416baccb2d3a9f95c5e8f6dda8cc0ab05`

```dockerfile
```

-	Layers:
	-	`sha256:fe85ec8682863d64dd496ae6c74dcc065ba4d8fe1f8d5901dce43b35e593cd5b`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 2.7 MB (2668907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137621e4efe4fd5d00196718a22a0d7a75d9578d655b78084cc7c78c884b93b2`  
		Last Modified: Wed, 28 Jan 2026 18:57:52 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:504380f4c62e0c739f9d72d1fcb49063df201cde7574244d11025c5ab38318e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315314947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623d32aa78781190c17dc37ce59cc8b4d855708908004caef29aadf2dddb7030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Wed, 28 Jan 2026 18:55:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 28 Jan 2026 18:55:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Jan 2026 18:55:52 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 18:55:52 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 28 Jan 2026 18:55:52 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 28 Jan 2026 18:55:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 18:55:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 18:55:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 28 Jan 2026 18:55:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 28 Jan 2026 18:55:52 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 28 Jan 2026 18:55:52 GMT
ENV MONGO_MAJOR=8.2
# Wed, 28 Jan 2026 18:55:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 28 Jan 2026 18:55:52 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 18:56:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 28 Jan 2026 18:56:14 GMT
VOLUME [/data/db /data/configdb]
# Wed, 28 Jan 2026 18:56:14 GMT
ENV HOME=/data/db
# Wed, 28 Jan 2026 18:56:14 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 28 Jan 2026 18:56:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 18:56:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 18:56:14 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 28 Jan 2026 18:56:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411027bc9289ea4dbed790e42d507968e722de74cca7410705a959f9d7c99402`  
		Last Modified: Wed, 28 Jan 2026 18:56:49 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aeb6b2a490943953de009a654249c428823db85f27ee5f85600f3c3953b0bc`  
		Last Modified: Wed, 28 Jan 2026 18:56:49 GMT  
		Size: 3.7 MB (3710407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764839961a06d4eb88352bbb1b2e914675d72e09ea5bef592e069e00a0e4779`  
		Last Modified: Wed, 28 Jan 2026 18:56:49 GMT  
		Size: 886.2 KB (886170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28f8eedb6731a95ce1899522eb53ed07c9f89e7c95e244cf0bf6f4f13c6a0c`  
		Last Modified: Wed, 28 Jan 2026 18:56:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d578ae46bd59dde1f85cbb691fb30c7caaf10e9328cdc5f417ebfbbe35ea7aff`  
		Last Modified: Wed, 28 Jan 2026 18:56:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe46713a2678c3dbe3a9181a34cef62bc90319b99dc68e05751c1328f9604b4`  
		Last Modified: Wed, 28 Jan 2026 18:56:55 GMT  
		Size: 281.8 MB (281847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1943cd0c486967d3fd800f8daa5c0bf8af56cce692ca6f32cd12a6b7e995393b`  
		Last Modified: Wed, 28 Jan 2026 18:56:50 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:4bde84dcfaa7d31519ef6489958bad4584e2e67e912c7ced37b63806935882ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ab36b3c0360a411ba014deff889e155e00682d06cec2804b1b6d1de7049f2e`

```dockerfile
```

-	Layers:
	-	`sha256:fffa55f150d2442fb6a5a3a8a9ab623bddb4e6613055749407207df7ec4ccabe`  
		Last Modified: Wed, 28 Jan 2026 18:56:49 GMT  
		Size: 2.7 MB (2670043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9859aea83ee00c0be9834800f2ac11774f4c104e7653fa4915b0ecabc7cd70a`  
		Last Modified: Wed, 28 Jan 2026 18:56:48 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:885898ea952b08bfa12beb4c90511eddb64730343f1c164ed14351fc4ecbd5a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311750359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ea64da91af98b52526d741b5e96e5287ebbb31557fba3c34fbbe375a583c4d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 28 Jan 2026 18:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 28 Jan 2026 18:58:35 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 18:58:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.4-signed.msi
# Wed, 28 Jan 2026 18:58:36 GMT
ENV MONGO_DOWNLOAD_SHA256=f8a7d1f49890ea91842d7eface71ff789a2e797fbd225ba31d3b65a4c878603e
# Wed, 28 Jan 2026 19:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 28 Jan 2026 19:01:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:01:23 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:01:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8daa8a1404dec4f1e9a3005a32988319fdc5e5fcc909140238e26b3c70230`  
		Last Modified: Wed, 28 Jan 2026 19:01:30 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50cbb425f028c17f8d9a26ac41c19c716f5c5918d7518d2c4303aba86261377`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec9ebddac805fb002aa0e3f4ba846601f2fb446f15d42c865211003946a032c`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6cdd26d44185eec53f156a8ec8148d43bc21eb7e443561fcebacf01d8ea536`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daebb594b16e19977462c0a163b3d4e651b0172802afb6731999940a6db5c0e`  
		Last Modified: Wed, 28 Jan 2026 19:02:47 GMT  
		Size: 816.0 MB (815980810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01b5c045f4676fd6d6d04d308622dca6afe8febf9f3d674e9faa8d823b336`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1800d63e94b9cec5ec1e63f5e16b5362740a49bc702eeb66829e33301fdcf589`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bed320bf1a1ae25616896b7ca10a25765357b8c99cb598f8442cf8439e9722`  
		Last Modified: Wed, 28 Jan 2026 19:01:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:1676059fd323be60849af220a71a0db149ea8aecfef4f6ce2544a97db2725f8e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651721087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5335a3e6564e25cc343a2fc6fad7abf3e45ef9a644592f0646e2b3e0df9d550b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Wed, 28 Jan 2026 19:00:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 28 Jan 2026 19:00:22 GMT
ENV MONGO_VERSION=8.2.4
# Wed, 28 Jan 2026 19:00:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.4-signed.msi
# Wed, 28 Jan 2026 19:00:25 GMT
ENV MONGO_DOWNLOAD_SHA256=f8a7d1f49890ea91842d7eface71ff789a2e797fbd225ba31d3b65a4c878603e
# Wed, 28 Jan 2026 19:06:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 28 Jan 2026 19:06:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 28 Jan 2026 19:06:39 GMT
EXPOSE 27017
# Wed, 28 Jan 2026 19:06:40 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:463ab9bfe56c2e9d2d3d44b25195d169f9711260d3b4a879439fe93bb1095cd4`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec5ae53ef72313c0fb49c34b02a9918b027f4931fec4770b53382e6b5c9be3`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1c9d139d270aa46dafd2cdcb29dda37038d230daf1496a4ab5e8bf087ed22`  
		Last Modified: Wed, 28 Jan 2026 19:06:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c700b1bd57dc3e7d1285b7863e3367061065d883aba7ea92799c5f3ae6a881df`  
		Last Modified: Wed, 28 Jan 2026 19:06:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fb072183face6f1e128eb488322cf98dce3315dc6db179568cf3e39ae0fb6d`  
		Last Modified: Wed, 28 Jan 2026 19:08:04 GMT  
		Size: 816.1 MB (816052765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d2d5a66924a5df39f36420c58b0d3dee745c6419e372391c635a4af2cebf73`  
		Last Modified: Wed, 28 Jan 2026 19:06:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2172cf867119eddf2a4a1bd61de98da8bfd8822e39d83e7c05226582fc76c4`  
		Last Modified: Wed, 28 Jan 2026 19:06:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8a823447dc089db4d16fae5338d7f42338147e7c9c69a8bde01b4ea15a3064`  
		Last Modified: Wed, 28 Jan 2026 19:06:44 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
