## `influxdb:meta`

```console
$ docker pull influxdb@sha256:595d3bf0fcbdaa44860691745361c22257a432d7498691e180afec4cf3038ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cf5db12b97a9cff6ccc66d57f091f8e942dec53d549a3c4327f74c5513fb5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91301354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d9d34df08484050b015bb39f36ca5833ca36a069fc2521171ac563a18089a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:45 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 03 Feb 2026 03:32:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c301e5663c93730e853c177c2921beb662e8af6fd669efac8f485fcab5976e52`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 18.8 MB (18780858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52acbb2fe909f154b6eea1c07a48fd8e021e522282b1ad8d2d8a0896f8c940a3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edea7eb3d12825920978031ef043c87591be9a1d18d4da302b7f5f32ef553b3`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ae9375a3129de2c571770f01c081367e812da11a7784f6ff1d6d479656df566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6630862709599dc01c2841fc7a2a536d1fe8edefdb660b018644dda299f27`

```dockerfile
```

-	Layers:
	-	`sha256:741f6b7444af98584961f6b6ddab2d605dc0082a3e1fdc69ad7638fcdab8291e`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727c7e09de0e967fbf5e91d8496e43c8ff8199c68a6f024a0136754d2fa2e610`  
		Last Modified: Tue, 03 Feb 2026 03:32:54 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json
