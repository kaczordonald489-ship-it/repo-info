## `debian:forky-backports`

```console
$ docker pull debian@sha256:e4ddd01dc619962c54e1a23df6bd4517830f43df03ccddde98f8afad24b66707
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:193950c20dd20080b13ad0b4edb75b60bb5345f4610a47904afa72dacae11776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca45331eca5f7ea18713f8265a6bc06bf7cf538dc6a09e0689116421da3d9cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:55:10 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a834c6cce5faeb3d4b1cc06b10bd92ff4478b882f26346a9667cb363be4a5c74`  
		Last Modified: Tue, 18 Nov 2025 03:55:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:da3a9db176f628122b6afc5998618133fedc452b488b29617fad14fce460218e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc1141c711d680e09d71311a84eff4db864b28b142af6deedb3fc9ec1c29bcd`

```dockerfile
```

-	Layers:
	-	`sha256:a1f13be9c52659a50cc284471e0ceb02a79e3edcbadaf1718f021c7c90874e32`  
		Last Modified: Tue, 18 Nov 2025 04:28:02 GMT  
		Size: 3.1 MB (3129533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8698b5f3abae2b9eb867aa876e0154473d798a38fcbb1a7a63b62703719bcdfa`  
		Last Modified: Tue, 18 Nov 2025 04:28:03 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b7194f9b0f5f22489c90fb94005a3b7b2ec7f4d4d60f6781ca0c60eec4478431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb676a40a6ede704d05047269e16bb61699af335fb2e292ef1688506320c38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:16:32 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe080826e475ec9da871d0dc5307b4af9c595b2a375eea367c2e2fdba5488c1`  
		Last Modified: Tue, 18 Nov 2025 02:16:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7dbb41f0d9ffb3d25a4badfa49063ecbdabbf7e157d36fcecbd3cc2afaeb5c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7750ec20b6bbfe2295b219d5e9b6e0635565da4701ad43143ace02bea8dc3324`

```dockerfile
```

-	Layers:
	-	`sha256:e46a0119a2572b43248de21559629b28356551f8a0e19af359e279d4ed199ad4`  
		Last Modified: Tue, 18 Nov 2025 04:28:07 GMT  
		Size: 3.1 MB (3130901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b78dfdc726fc26b94c4594322490f952439de4b0989701c6f86332f00baad2`  
		Last Modified: Tue, 18 Nov 2025 04:28:08 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:40a2f5112c18822c0123cdfcbf0e8ba3dab0ed66e85324f0e3cfea8ac2c307dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf1e6085e0da4b9af4171e0f323e01a669e75dead3ab8c76cba47951a86776d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:15:37 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525cf0e6042d0d5e996c12ba22c67d19c0b3db9d0739d036b6368e2ebd8d4262`  
		Last Modified: Tue, 18 Nov 2025 02:15:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f07be029bec5b80957fbf7912e4c24975fd053500cd188bd3d29fed01f4af1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869929ab260970b95ec0c3a6ba4d8d9cffee28f3e1f525945708f9527f3ab89d`

```dockerfile
```

-	Layers:
	-	`sha256:b32c903777da15fdc3815f6ec4cd88a0e3536aa92c621a3eac77d3d4144586fe`  
		Last Modified: Tue, 18 Nov 2025 04:28:15 GMT  
		Size: 3.1 MB (3130374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddcacf83e44cd26f4e2a6c41d4871a26abf3989c54fd0b9f2b70dd3900fbfe7`  
		Last Modified: Tue, 18 Nov 2025 04:28:21 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:b89cc231528bc86029e92cb0a03ae1764291921121d6e0b2142dac221a6795df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49832460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a201b6b7e42784086f1ff3356209e4b7526b451bb888a60188cd6829d03eea3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cd47c9c5c4b0fc105c1fecba2752f6b14781d650e3463bc680163110a765`  
		Last Modified: Tue, 18 Nov 2025 02:15:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:092ae1c52b09d09a8069bcafc4ea14f27dc17050277c3252aa078b4c9b5b458c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523c59999526007262771f20f345a07632ef7c03037b08bcadfee555b5693606`

```dockerfile
```

-	Layers:
	-	`sha256:cee5a134d82cda21470ee5a2f915ab14d4484637cf29c9a608e26bfa9995e209`  
		Last Modified: Tue, 18 Nov 2025 04:28:24 GMT  
		Size: 3.1 MB (3126742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52fb7dfc84d95a8347ec0ea2cfba4ecd44315e951a3ccf0265db212fd9540ff`  
		Last Modified: Tue, 18 Nov 2025 04:28:25 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ab6083edea256660a48a5d12519f9d0980063b52f25072175b397db63deb8c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53334856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c9e2c0a2cadda7a90c57968f698963640ca329c5cec002fb03792e03f64e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 14:56:23 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:56aec8ed2c7425bd4d962ece466e2022cf4900d838eb52bfdf10fe6e2569b4bf`  
		Last Modified: Tue, 18 Nov 2025 12:56:44 GMT  
		Size: 53.3 MB (53334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9283f7dd16526616012e5907bd5f4ca40ff84db112b9c55e6b11696a759da860`  
		Last Modified: Tue, 18 Nov 2025 14:57:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56cbd4fe559b4f3b7dbfddd0adbb840b3698442e65501b8d4610e8be29b74f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a9233b42c06026e0514ee087b0b6702f2b480c45e07b480766f618f34c974`

```dockerfile
```

-	Layers:
	-	`sha256:b65fc596440858aa4e26260ff3d35397595db0b759690678d444bb08e3703af9`  
		Last Modified: Tue, 18 Nov 2025 16:25:20 GMT  
		Size: 3.1 MB (3133022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34eb8ec380ed6ec3e61fcfb5e95f1a07ea2e68f2605a918e1862cf2158f35702`  
		Last Modified: Tue, 18 Nov 2025 16:25:21 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2f35c3bc09fb9282eb06391d691af44d506cee37922f491c7c09e7513f0bb49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46806556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92804e70b0205e0f2a05657094e3b09cf9751c43feff26fa85eb1fa6bfeaa463`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 07:54:26 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5f062c29e53f6114ba8255e90dca3ce517e3e0563bbe15af71540ba740a9253d`  
		Last Modified: Tue, 18 Nov 2025 01:31:28 GMT  
		Size: 46.8 MB (46806333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721f83fb750d36a41a024cc9d0d93c488e6c56981515b48add5c33780b407bb`  
		Last Modified: Tue, 18 Nov 2025 07:55:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82389819cdddcbc09b0f90d28ffbc3cc522b9e4772a1f56af3867d7bb0a9b7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21648f36b672aea4784e6a0f173b427bf65acb3d678fa2cd6ebcb07376cedf14`

```dockerfile
```

-	Layers:
	-	`sha256:fe330058d959bd5e9473d30f440091d57f7079618f5db56b8c88328b6161bcd8`  
		Last Modified: Tue, 18 Nov 2025 10:25:38 GMT  
		Size: 3.1 MB (3121832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef1ade6960a1b6362caf119639d36db6915eb701b5650c3a4eecf2eff7bc6cc`  
		Last Modified: Tue, 18 Nov 2025 10:25:39 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:241d4825f3da4cd1d9aec1a928f0c705fc0f6ab9263affca0f8a81a207ab9d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48371154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c989d615cdd268f97ad6830e8a52e307801ba79d7e002517f4d69fe04c189787`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 08:13:51 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bb1941d24f39dbf96b6d3045499ee523d7b760b1ecc1834da461428a6b3f02c0`  
		Last Modified: Tue, 18 Nov 2025 07:24:21 GMT  
		Size: 48.4 MB (48370930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff7f960fb3186ea21a0666f9ccb823eaab8e48b707a6f8f770052332d644b86`  
		Last Modified: Tue, 18 Nov 2025 08:14:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f717c90171989d651f56a3e0ee65ce20891afe6736a749de520f12435ba4aa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ce5a467c59fe6a88351fa57de44ec400d4e96c5058ab883438d5757e08bbd9`

```dockerfile
```

-	Layers:
	-	`sha256:46bf9ac8ac9231ec11ebc89b8a78943df92e0e628960bbd241f3099090916c37`  
		Last Modified: Tue, 18 Nov 2025 10:25:43 GMT  
		Size: 3.1 MB (3130982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6037cc9d0af2f4eac2a1fe8818a8a5d2b03830302f506f061386466ecfd3a6e`  
		Last Modified: Tue, 18 Nov 2025 10:25:44 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
