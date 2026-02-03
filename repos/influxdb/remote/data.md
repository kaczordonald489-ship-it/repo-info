## `influxdb:data`

```console
$ docker pull influxdb@sha256:6ee054f5264bdf35995032887a42b386ae922ccfe379ea754afecbc2e73bf52a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:bd87962f04b5e5fd56acf0f5935868b4efca456b6fb8d1b3a6174d7151b0a8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114841526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d161b120e02516f0496e96c28167299a89d72e9f3a72d706593bd1360db73bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 03 Feb 2026 03:32:49 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 03 Feb 2026 03:32:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 03 Feb 2026 03:32:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 03 Feb 2026 03:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:49 GMT
CMD ["influxd"]
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
	-	`sha256:3acf28d2500a471d1dfc3178dfb606f71b5e9ed292e422655433c53cbe73a6ca`  
		Last Modified: Tue, 03 Feb 2026 03:33:03 GMT  
		Size: 42.3 MB (42319821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13e3563e88a57ac2dbc95ecc269722c6eef212fb6a2aa36dc48ea85181dc9c9`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecebd9eeb3c29a4676848dfc8b528ad9036268a2b9d18f75976e281547931e6`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d318862ee1f525bef0688496e8db3ece435fa6af7bda0b6725f96fe856f198`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b708c6661337b3f859fd3a36f053b9ab9a12fbb2cf84b2ca62c18c9b8db5ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a28e355e551d575ad6a0d1cf2a567adf5be90a12bb7ea104cdd2c409a90c30`

```dockerfile
```

-	Layers:
	-	`sha256:5cafb353c28ab90688350fab88cecccd4ed633f9a275142cfc1fb890ad0925a0`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf37ce8ad2d98b4f978727f83d07f5c90f5f2ed44eccf2ffdc8e4769d81d91`  
		Last Modified: Tue, 03 Feb 2026 03:33:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json
