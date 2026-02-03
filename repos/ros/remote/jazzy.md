## `ros:jazzy`

```console
$ docker pull ros@sha256:af9454f13d342c58bb9f3364424e3e7026184e59a47de75f915d241cb7ec6666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:f3dba6618d45181f7a68cb3f2b9a9da9d52c3315d805fb99687123a80eff10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296053963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fbe811330cd2f7e3c52c4a6d4369c0581f7679d8b5d48c8cd6e5f20c017302`
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
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:34 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:11 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:07 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:09 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:489faad951607a6a8c266763d0b39d81613d6c0d08896cb14c2cad83a06b29de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24561461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44151c680004f3aef9280bfa546fa843c046063206bb85940671f664c80d210`

```dockerfile
```

-	Layers:
	-	`sha256:efcf6f164767bef316bca6384f77c11bf81a593e100ed0155c2e78cbecd59ea9`  
		Last Modified: Fri, 16 Jan 2026 00:58:09 GMT  
		Size: 24.5 MB (24544841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8acd13b1ba88981339bf29e7b8665c281a468711d5d8e259e6fd22a3713d0`  
		Last Modified: Fri, 16 Jan 2026 00:58:07 GMT  
		Size: 16.6 KB (16620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93482033b6cf937dcc1e404218b02213b008f7036e4aa2add797dbef8b63f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284482132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98deedb66635f35717a5c1b6b33bf4b90b9b61668da1541760a28bc494f25da5`
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
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:33 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:25 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:22 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:24 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:ba47a82a66bf9e3371eec41b3ec9dfb28946205921edc356aa608730d92d45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5ec4280e4f026f58488178410f21315f441a865dd169e428cc9b45d79f1262`

```dockerfile
```

-	Layers:
	-	`sha256:1fe22c8f0fdab48afe6837bd75771d82729a93a29acc734e78affd64a685e1ec`  
		Last Modified: Fri, 16 Jan 2026 01:01:23 GMT  
		Size: 24.6 MB (24567114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf5e37218976a68acdbf1ed803bbb3f4e017f73018f64b38c22700e39db988f`  
		Last Modified: Fri, 16 Jan 2026 01:01:22 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json
