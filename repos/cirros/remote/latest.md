## `cirros:latest`

```console
$ docker pull cirros@sha256:9aef66b2a694f8cd31bd5c334419a0c75dc7f4c869931087c04ea9b2cfbdebaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `cirros:latest` - linux; amd64

```console
$ docker pull cirros@sha256:bcaa15243a65a89a2647593774048f6bc5a07ecbe31326fc80ba8cf94067eca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034699397d020a464e833ca011ec36928c2dad564690572e7e4f542d4ba58bf5`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 25 Sep 2024 10:32:49 GMT
ADD rootfs-x86_64.tar.xz / # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN rm /etc/rc3.d/S40-network # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:57744a926da1c44122a6ef5cb4fc3e18f84f8b715cf407b9d1f49145f97fca55`  
		Last Modified: Thu, 26 Sep 2024 23:57:56 GMT  
		Size: 7.4 MB (7413980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f17ab44c36fc4848662143b4e22abc3dcb3ea2f72c2478b694daa1b29d228`  
		Last Modified: Thu, 26 Sep 2024 23:57:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e515d9888048df66351e2a33db97996c388dba76b12d10d8bf669de6227493f3`  
		Last Modified: Thu, 26 Sep 2024 23:57:56 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cirros:latest` - unknown; unknown

```console
$ docker pull cirros@sha256:d0884c82a60f26d02b36413ec5b80643383196156b08f31d42db6c5bfb723e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d937a1ff0ff073bf31283b40f468f28454e02113b3e13b0daff5f2e9e0557ecf`

```dockerfile
```

-	Layers:
	-	`sha256:9cff5790e12d94517b5aa89f689a070404995d1faf54e7503a547720a585c8fe`  
		Last Modified: Thu, 26 Sep 2024 23:57:56 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.in-toto+json

### `cirros:latest` - linux; arm variant v7

```console
$ docker pull cirros@sha256:a8ab401ed65f66eb9ba3bc41c0b1ccdd23c06bf4673ea90694ba492f5fa9a4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6917508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10064890c068d7af673f69b30ef9d35ea9f3d888811ddac5f5eec6d35bd0959`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 25 Sep 2024 10:32:49 GMT
ADD rootfs-arm.tar.xz / # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN rm /etc/rc3.d/S40-network # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:859a63370c800364a8b46597556a1def8f86dd1c9a3234235cb9ab2796cf8797`  
		Last Modified: Fri, 27 Sep 2024 10:21:33 GMT  
		Size: 6.9 MB (6916072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc8558494c81739dbd5516e1c317c4cd9ebd08fa8a23a06dd7ae846a9598505`  
		Last Modified: Fri, 27 Sep 2024 10:21:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d39b9020a5a1701d7002d70869f306d79a54f817f21150ea75a8884afddfa0a`  
		Last Modified: Fri, 27 Sep 2024 10:21:32 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cirros:latest` - unknown; unknown

```console
$ docker pull cirros@sha256:2d5d76a715653151f91cbbff3abcd2b3fe4e6c4b04bb5e38252670305f79aa06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2a4bf4614a9c2e721ac038b3c506ec469467033f7ad60e72a68aa4692851d8`

```dockerfile
```

-	Layers:
	-	`sha256:558bdd82c3a5506301b5b68875cf22cb9a373650dc2614056366c6ad939b6a7d`  
		Last Modified: Fri, 27 Sep 2024 10:21:32 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.in-toto+json

### `cirros:latest` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:df6600fb2518df7b0bd6da32063671b1a5322a6dbb0134390dd1e3f7b7c704b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dab2758ee2687902d4c8b4602445a3a2affbafc45e2a96e5780c550caec048`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 25 Sep 2024 10:32:49 GMT
ADD rootfs-aarch64.tar.xz / # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN rm /etc/rc3.d/S40-network # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:6820a8cb9922e3940bb262942d79d60e49d9b1c1db965f1ac6cad44cf34325f5`  
		Last Modified: Fri, 27 Sep 2024 10:13:23 GMT  
		Size: 7.5 MB (7511647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8566350e002db7e1b401774232d9d3abd66e19b43f32dcefd8189d170b2ca961`  
		Last Modified: Fri, 27 Sep 2024 10:13:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b13aa03454ef35a27f068e54f558f77fbe141c63a3fa3b3ca6380e5f8bcfe7`  
		Last Modified: Fri, 27 Sep 2024 10:13:23 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cirros:latest` - unknown; unknown

```console
$ docker pull cirros@sha256:745351deff6c03aa6cf482971a3cb74112f7ec1c585229c0b68ce5f60a5219c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c3045fab38aae671bccc38848ad9d64c28ca274306b6bab32e9a8dcc0dc6f0`

```dockerfile
```

-	Layers:
	-	`sha256:202e6337da159219bf6038f0160e186ba44b129a39984dcc256c177d1135878b`  
		Last Modified: Fri, 27 Sep 2024 10:13:23 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `cirros:latest` - linux; ppc64le

```console
$ docker pull cirros@sha256:88da8f89c29a6a873b1e80dc65a21f8007acff329782181babc9623d66f02373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7893988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723a0809e554be72e52f9a5802a6dd24217bca42d121bae1f3950edd807baeec`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 25 Sep 2024 10:32:49 GMT
ADD rootfs-ppc64le.tar.xz / # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN rm /etc/rc3.d/S40-network # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit # buildkit
# Wed, 25 Sep 2024 10:32:49 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:6309759136f87e6c03b33561dc8fef075f252e80359c9e16e671e61d7059a194`  
		Last Modified: Fri, 27 Sep 2024 01:15:53 GMT  
		Size: 7.9 MB (7892552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025f3f60d4175e61b5e11adec222b7231c075cf43c195cdc95b457b59ee3627`  
		Last Modified: Fri, 27 Sep 2024 01:15:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddbac8f167ab38f54f00e2d037c25508dcb9e907910086ea3413036b005089e`  
		Last Modified: Fri, 27 Sep 2024 01:15:52 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `cirros:latest` - unknown; unknown

```console
$ docker pull cirros@sha256:e2d148fd8cc279b79d9bcf8af8c548003748b14a30c38e64a9103d7df7ab1584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cf48bd47bc9b402e2422078d2d75337f064623b9683f121bf9f08902125869`

```dockerfile
```

-	Layers:
	-	`sha256:da9f93cb29361a87fb9f2afdd2f7175e2801f6b538a2c28d47a9891598e890b0`  
		Last Modified: Fri, 27 Sep 2024 01:15:52 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json
