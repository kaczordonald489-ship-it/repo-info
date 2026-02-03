## `debian:testing-backports`

```console
$ docker pull debian@sha256:cb0f0efdecef8a5f04b37a5310fe044f1820e9bf6832bd152349710c3116ff57
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:b4dba44fa79a015fbf598cbafa23b83525da70fe5b64e9fdc937e957af37dd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48655962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9c3dc4ce410e1055a1f9230bc0653f1be768973cd8706266569f7981077bda`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:16:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5195bf09170e6f427c63401408925ebdcc18df14385049cc0921fa4e070abc9b`  
		Last Modified: Tue, 03 Feb 2026 01:15:55 GMT  
		Size: 48.7 MB (48655738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeb5b6fac0721e70ff83131c0cf92062ce3201db242d84d8e6faef3d8c7d8c5`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c6f18a6efb24929fe99039c37135ef1024ea1679e8bd715357becbce9adc55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca473c0244c6dfdfd9c7fa8c11b29c518b825afa7265b0aeb732897fc5f6643`

```dockerfile
```

-	Layers:
	-	`sha256:3b26be81976499a28dc5633f7dc88cd6e0323f933f34a16e4144a9f7fee125cd`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 3.2 MB (3150961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26973b037160741872bd240349349d5afc45c97d9b353c541d50482e13f2b4df`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a9439ee2f2b333243be32065f0ea1ae183ccb6bfd97d2d2a6cd0b3fbe65a0797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45620843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5b725796bb3234c0a5f169d452c932b5e70abba2357cd0400c8cb48e0ccb69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:951b19b5fc00b9ea855495c7cf3c9e2a0f61a59fd9eff7f35835a29ff7aaceea`  
		Last Modified: Tue, 03 Feb 2026 01:14:25 GMT  
		Size: 45.6 MB (45620619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cc1ddb73d687aa2a7e9c59d420f31ce5401c87c109e031ecbd36669ccbdc09`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:06a575b4c9c4b24bf8c9ff0fc7f2862f9c0183b7a897c6e69e6dacb975364f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a6b0d61436ff2ed78dafb1d98951d06ff86ed3b65102b0f9a7476bbc338812`

```dockerfile
```

-	Layers:
	-	`sha256:2b0f8f9fb6c39b71c367910740efbebf6c1f5c0a9a9fbdb1215e31841fffe0e5`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 3.2 MB (3152329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb9701dab348926b4fe6c50a0c63f64cf34ea95a13d88fc09c15f95a39f6674`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0855d830b64f3535c5fc66f553f6ccd19ce402729d67f3c944a90c7ba70705b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48678750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe623b16249462116749a199807497b52cfe6d3d4b0a865767b57adfc6cc7337`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:123ecc6af9e1da19ff84499fdeec8618c28ddf6a280f4f81cc8a607c8f700da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 48.7 MB (48678526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5ca368e2b2af980b1ffe1fb99941cdcf7c5fc6ca0e56fad7021e9688fe6787`  
		Last Modified: Tue, 03 Feb 2026 02:15:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8126290869e58bebc83da69c297f2b45d50235fd28da5b0482ae565e0a6ebed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcafdaa55ac0b77271eb8b2c6a238e029e735a51088121c190c45e44ec999bae`

```dockerfile
```

-	Layers:
	-	`sha256:308d7726e434fc7aa1ba46b4b37b019c8ab3cee913f5ad953ac236214a9a88f4`  
		Last Modified: Tue, 03 Feb 2026 02:15:19 GMT  
		Size: 3.2 MB (3159647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04df93838f267c33b3191281122a261ac7964b4b6c3a5450a43237df054a4761`  
		Last Modified: Tue, 03 Feb 2026 02:15:18 GMT  
		Size: 5.9 KB (5861 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:a1b53ec055e305551fbf13630781db20a5103fbad0e9eaff16158711e79af417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49982162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58d050c1900146e5de5216df307351139977acbf6901c3d84cc24fd10b4de65`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:16:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4dcce4e355fad2c7fd0e8ec69a77aee3746f0ada4d551316ebf538af24c1a989`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be1dcd220944f96a9083d89c8a592d8d4aa5fe47881885968ea542fe25c8f16`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f7309c997d51321cce39d7fc315f6c797eda5d2ad3e51802f6f0de2f290cb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e2182852818df69748abc41b5c59276154afcbf62b2caf2b337a64fcff1225`

```dockerfile
```

-	Layers:
	-	`sha256:e86cb1033d4c0b760955e989cae59a02f716e9b63431df05b6c48ce2c498e490`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 3.1 MB (3148155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70b4e122a608927fa25f8b132614551305d1059a7dca83efdb7839a946fa1ba`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f2d65d0a8ac7d2cad503f7ae2c4973243786fa3c0f599c630154510a509b00bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9230452c0aa9121a5a70e663c545c3cbc9c204fc9bb72f90b27707c4576d5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a1783231c3dd75846ddfd4277f3f207d78dec75ee1f53161099a048c12db614`  
		Last Modified: Tue, 03 Feb 2026 01:15:51 GMT  
		Size: 53.6 MB (53582668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4828c6891dfeb4ef0889a1b9dcc9f4a1dd627fa33cb7a8232e5156e08ef3290`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c74cd72fa9c1fb7ad9a7bbb49b5c3824cf299ec87ff6ff7df80ceb443ef3d8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b39ff77f1a2d5e9fdbd9195ebddf399e5d0442ad7b3bad79a73ece219779d6`

```dockerfile
```

-	Layers:
	-	`sha256:6ac561648b9eda39d0fb18867cf944b36d19bbee15c2b5d5e8759b6859f6b00b`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 3.2 MB (3154484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c294d0594236016888344d28c5255a99bb11d1dd67f78968fe06e8114e6ff4f`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:fb3f274ed7839886023de45dc2e02c7fdbaef052f60338203d6fca695c8392a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868dd2984733b77251c787ed941b6b31341ab68d2280c7358f98a18d6fea2cee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1768176000'
# Wed, 14 Jan 2026 04:07:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91e82f1d58406699b930594305527c53618f59da57e5326a595907e3493b82f0`  
		Last Modified: Tue, 13 Jan 2026 01:02:49 GMT  
		Size: 46.9 MB (46854468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e2f7e7862637d229f9598e10597a1261ad3a4fbd1b8e34660be054d5f706b`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eeca3de25934e33c48334a219c81a6ed7497c2dbf5dee16f46cf2c5428f39e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c940681b5da64f7be4126ba2ff8167e8ceb76e21df52d370d7be2311bc6486`

```dockerfile
```

-	Layers:
	-	`sha256:eb8e91d8af3f130cba6082e1c93e4347b17a4220046c6896cc6a97f6d8d50dc7`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 3.1 MB (3133541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7710d291674518d0f94515c05703921690d4d88554ecc3e1ae239f4a7b92f9`  
		Last Modified: Wed, 14 Jan 2026 04:08:12 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:7a042ed704bbeadb38a07cece688f5d3c79e87258f62a991195518985f7aa7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48429555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205eaa55ab56f13a9cdb78e8f2af2568ee60a9d5ca09a7317ef2543b4dd06c07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 02:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:307dd5b030418664167d57cabfead401f56d4230a8297dc01ed7acc18877867e`  
		Last Modified: Tue, 03 Feb 2026 01:13:49 GMT  
		Size: 48.4 MB (48429333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd79bad1ad762151b8c7b086243ebd0e52cad48c8b8770a70730e59c0672e00e`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3321ab52b828dc50d8860119c8ecd6d864460f204dde9ae122fa498bb1cea5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a1328352e2bcbeebf35d0d44b207da54fceeda85104f4c379bab545a3796b4`

```dockerfile
```

-	Layers:
	-	`sha256:553e74b41eb49cb895120ce9fce94ba2e4e33c65e01ffd1d0f31846e920d36e7`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 3.2 MB (3152410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efebee0847ad6a7750646df91d272977abf6e3f978b523ee0396ce017a976c3`  
		Last Modified: Tue, 03 Feb 2026 02:15:55 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json
