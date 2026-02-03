## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:0f56da780742496b9388894ae0a4641f78b81329f1b85ce620555804dbf862ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:a0fb78c7308ff5eaec5562fb7ddc316068c8e3a2e0b5dd00fe7e982c10f91441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109467363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60c136623b07d9e5e2bdd3fc60c30c3f936ce642f7f3745a8defc296c5b27f`
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
# Fri, 16 Jan 2026 00:58:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:58:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:25:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:81f49599d4013baaab168de3657e56f1a064b0c2b3905abef079ce53580b55fc`  
		Last Modified: Fri, 16 Jan 2026 00:59:38 GMT  
		Size: 110.2 MB (110187905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803c8199c566f7183c9af620273eaa14079f91449307d2f85488be3e5b8e31c`  
		Last Modified: Fri, 16 Jan 2026 00:59:34 GMT  
		Size: 364.1 KB (364083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037797cc4818e4cb6c652d9119165eb136a640dc847c7a40b2a255d82140d78`  
		Last Modified: Fri, 16 Jan 2026 00:59:34 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e075818bb92799b42233693868bc52253c0460cd5c0e34ea859c07eb2f032`  
		Last Modified: Fri, 16 Jan 2026 00:59:36 GMT  
		Size: 27.8 MB (27830020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b226b53e47fd3107e4210955e250d6e9a4fb56ed999834cf4460aebfbb5d701`  
		Last Modified: Fri, 16 Jan 2026 02:28:28 GMT  
		Size: 784.6 MB (784572225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7b795ba54b4a8f8026d40de5f2b5f9e69c454fc7403db628d2d60274908155a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61873356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500771f9e92118c5ab4462f33e40fbea8411190490ff0b43d136cc5ae738a7ba`

```dockerfile
```

-	Layers:
	-	`sha256:9bafe87557aa1248b96768e77e3c0038986b3639f8ec7c2aca5d300ddde693b8`  
		Last Modified: Fri, 16 Jan 2026 02:28:16 GMT  
		Size: 61.9 MB (61863995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74883d54707697ecc2759108ed4081003f9a7dbb7e8d7cae89c78bede4458ad`  
		Last Modified: Fri, 16 Jan 2026 02:28:14 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:45a6cf5a9c6c3d1bb91064e6f0a46faf9ecb8022c5d41344a336c4c7491a7302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007486150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ecac7e9b659abc45941eca0f154df844321c98981efcd62d67a6c728880bc`
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
# Fri, 16 Jan 2026 01:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:40:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d9d0315754ad467c0f84a51bcca420f9d00efc89dd6b14a66ca9b67d15cc1515`  
		Last Modified: Fri, 16 Jan 2026 01:02:36 GMT  
		Size: 105.6 MB (105595993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98324865d792dbec7fdb6bca34a68a242ff693752ea91e79792218d79eb584`  
		Last Modified: Fri, 16 Jan 2026 01:02:33 GMT  
		Size: 364.1 KB (364075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a40e53a65c744875af2e18cbb0eaa9054b3b722a5cbb8ead531fbd150be6f`  
		Last Modified: Fri, 16 Jan 2026 01:02:33 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63502b76303910712c34ce860754310acbc8ecacdb2103d23eda093422cc82fe`  
		Last Modified: Fri, 16 Jan 2026 01:02:34 GMT  
		Size: 26.9 MB (26911011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b00cc6026e7050c1219ca4091bd5f2446007a90f6b90440c902e85e6b24511`  
		Last Modified: Fri, 16 Jan 2026 02:43:15 GMT  
		Size: 694.6 MB (694610257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:46aa9129e2776a6fe4acd8fce2c5611d8270139fecce6f39bf748b7044baf19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61804158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4788c78fc085ad86a89b870cdaf737c441ac96437acad0e9773501fd3691df97`

```dockerfile
```

-	Layers:
	-	`sha256:4d8445159f6b4af698ba4e5213cc243732b3f769c6d4f13643bcb18de335ea7c`  
		Last Modified: Fri, 16 Jan 2026 02:43:03 GMT  
		Size: 61.8 MB (61794717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8482d3269e034a1843ad6b615e9425b859a5e39403e747a8698c3e55357fd5c`  
		Last Modified: Fri, 16 Jan 2026 02:43:00 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
