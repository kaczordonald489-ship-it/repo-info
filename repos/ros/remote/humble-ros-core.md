## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:cd9f3331edf8c29d61e091e76654eb1161c7971ff443b1a00e3244bd62e37051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f69b5539fceb0e0129a08a4e5cffc7582b77c0205929d55a6cb3346ebecee432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141544514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cbb3e4dc690aa49ad38bbfad559d3e83e013d9789a378e65126aad5c0f71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:15 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:16 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:15 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:19 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4fc3d5fcfbb3581dce7815009c262c42533eb9c376a299da43240c7034cc07b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ae6d258fc9e421f1f32bde317f386912b70388378ed0f2996dce493e33e66d`

```dockerfile
```

-	Layers:
	-	`sha256:28c9ab24b1fe7b7ba054f5b971dcdb7bb3ba1e4314773cb4c19cec7d0be5ac5c`  
		Last Modified: Thu, 15 Jan 2026 22:41:16 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ca1e20c455cfe5d6984f0d68f5676a5c2dbbf3bccd9b974330e170880b679`  
		Last Modified: Thu, 15 Jan 2026 22:41:15 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ef0f3eb0afa05f59e72564ba6118301accf1df33b16de448e0792364fb0f564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137100411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd15eec77a38217628e23ef12d87b0407c945f512c375f04ea91b271913b32c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:30 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:33 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:967382a1c38611b9bc0172b342bd0c773f400c564463104dca8878394dbc7b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bff8c8c6b1315cebd5e9c254b4c74f23dafc92e2428cf39b498ba788c947232`

```dockerfile
```

-	Layers:
	-	`sha256:3751c79de9911e1a26a0311151c9fcd345deae4e47a1cb73c31798b7d7133bf8`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e6846c0bec695a5b996cbd814e6a782dfcfaee6fe4f04fc6d079242e1ad9ca`  
		Last Modified: Thu, 15 Jan 2026 22:42:30 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json
