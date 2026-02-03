## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:c450e30428d9dffbb52e82d77fa57f08fd2b0cbd1721d85426f0346dd6170779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:4414971f5ba776be6949205af31c175460c08a41fe5e6aa69086e636ee56e008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186510618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f565248a907b92a0f6c34420b8df6821862f65fd82ab4405571a012c39529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

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
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:35 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b5c81055704fce3b7ee80b28a937e91c0ed9242e28ec80dca2261cde40d08431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19476848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a542861638fd5e676f82fa7b504c53dcf9acd0bba27a875dbf6afa99cb3ed97`

```dockerfile
```

-	Layers:
	-	`sha256:f1dfcc508e0530ba986bad5d0dfa8b3eacf5b1fdd09cbe2c0c993723a4f1d6ee`  
		Last Modified: Thu, 15 Jan 2026 22:42:32 GMT  
		Size: 19.5 MB (19462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb6aca053d64d959a9bfb9a9023c16453c90588ee55d26ae9f46a43e5ce2d71`  
		Last Modified: Thu, 15 Jan 2026 22:42:30 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bdb6c79e51eeb3cd62a34f7638349f2e3e7506be37296da98f13627cb347cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180002320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad93554f7b9323204a37820ef6a7dbab75033c4de7285a53a0deff6d47ca7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

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
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:15 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:15 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:19 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3726244eac85e63f8332f9aa5f98da0985cf301242acb7ce7510418098691967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9afb3630348f57d5e7a27b2c5680abcccb7cf1d3e836ccd3383de79c8ffc04`

```dockerfile
```

-	Layers:
	-	`sha256:5826054e3a58ccce8bdae4e8589aa61bb8718823c53f76cb2918cd81cae9bb7b`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 19.4 MB (19436430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa80eef061cda18f04b7734dd969bc324d502fd5f74d136f2c435ce0d487bb8`  
		Last Modified: Thu, 15 Jan 2026 22:45:15 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
