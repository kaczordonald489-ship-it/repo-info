## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:3b2031f3e7211aeda15e1a346dba08ca40d8c3eaed7f68649e50dbefd481c260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:ccaa6f44bb6543305056958567a8ebba7ddf065b0f1a5fff08b3361205a4dd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f06769f43a6813b7f42ba251a46efbb2685c5f0fbf074c7e1d935c9238911f`
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
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:05 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:85b7e6cd34c91543e0f0ffcb7f8fa9f61f3b12feb6a692745d79f5b3ca18c10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e21f669779c98ec19bb21942417dd61ddef48f8dbbfadc4bea62294a961b7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d7c40d424370efa0acc5aecc4219175171e6e03118b0a7d8b55ceedd852d5882`  
		Last Modified: Thu, 15 Jan 2026 22:42:03 GMT  
		Size: 18.3 MB (18333431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830fb208c958f36b2165a2897f06eab6e7d1c92c665b3cd56c4fbf3c97b0ad24`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fad38bb0bc4e1350966b47502c707f6f61fc390a54596713a0f777249956d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152146193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d8114399e27e481f4ca8cee2610b3271c3204d53b453244a025f9cf4758397`
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
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:44:53 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:44:56 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:44:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:22f1afcce613dc8e7d6f964acb72a975b5fb8a8cbf9d4913257327ae7c2655e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe5d10b04fb69189179c45c43b71b7adff576ed6fc6b80262a27ab0ef1c69a5`

```dockerfile
```

-	Layers:
	-	`sha256:c3fe08ae49d307ea43de5ad84e7dc36726df01168a389a3744bd98c0f2597479`  
		Last Modified: Thu, 15 Jan 2026 22:44:53 GMT  
		Size: 18.3 MB (18307437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214cbfdb1bb403257859a5c52d342af1acefab9e254a3ee9eacb419462ce31b`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json
