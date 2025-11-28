## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:e15e22a7b12d83bd8e74a87010080adb9c697187a4e7919b3f1107b0dec458f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:be9194c01daebb513760ea0807f691b37f62841a4a5be177ec3222524e330fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b2635343eeff54fff474edeafc2f1dadfc528f4d028fd9c95b354832a3130`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9384e3c026a30291bf2ecbebae43f7737e26f758c5e65826a7d7988f7ac77`  
		Last Modified: Fri, 14 Nov 2025 07:35:37 GMT  
		Size: 784.5 MB (784531548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8ca951d20e89c222764cbcb0b4331902ba1c3b085a4bf2f39dd6365614ed4b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61913258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2947e13ed1bac2da29d09b83220014ae1b8a2ededb2169110dc3fd7a4c1db3`

```dockerfile
```

-	Layers:
	-	`sha256:52578280739f10315a8e65bdc4774e09575922556d6a284cdd6e14c9d8b27acf`  
		Last Modified: Fri, 14 Nov 2025 05:18:20 GMT  
		Size: 61.9 MB (61903897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf96a68f2d59ab1e7f9f8918eddc4c5eac8939a3bf23497a75c3746d4467f6f`  
		Last Modified: Fri, 14 Nov 2025 05:18:22 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74c1149c7a5c1bef22da018fae466515e000a344da879394d76676e2c69b76ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007216187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bda908390a724e838225ade5c6d650df196f05eb7cf27a5828bb628444179b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce4a548a9e278afac869dc062059bbbf762381ef3136c4835c8f663eddb426`  
		Last Modified: Fri, 14 Nov 2025 15:50:51 GMT  
		Size: 694.6 MB (694565732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ed822594c7d69eb4c75dabd13d741dd7cc5b5eb3949da7e742836660fcbcccf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f4f20ea9d6203be5ef243fa96c9321d6ce00d17aa52eecdd9449ed120bd00`

```dockerfile
```

-	Layers:
	-	`sha256:a42fa6f66f50eaaf261bb413c076f2545dfc6ff742ef782c9f519d25ba3e9d10`  
		Last Modified: Fri, 14 Nov 2025 05:20:09 GMT  
		Size: 61.8 MB (61834619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ed22bcee0de118946955cada52b3078043306650cacd0d92f09dd9b709e64f`  
		Last Modified: Fri, 14 Nov 2025 05:20:11 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
