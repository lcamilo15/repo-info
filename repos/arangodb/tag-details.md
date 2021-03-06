<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:2.8`](#arangodb28)
-	[`arangodb:2.8.11`](#arangodb2811)
-	[`arangodb:3.1`](#arangodb31)
-	[`arangodb:3.1.15`](#arangodb3115)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:2.8`

```console
$ docker pull arangodb@sha256:17cf67234a2168b502e372ff50cad58815019c00fc2d17e345429dcd9747ed49
```

-	Platforms:
	-	linux; amd64

### `arangodb:2.8` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110329817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca336d6bb6a1edc68396955640387950ffce2643ff2e25aeef9a6da9a222a3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:06:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Mar 2017 20:06:16 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 21 Mar 2017 20:06:17 GMT
ENV ARCHITECTURE=amd64
# Tue, 21 Mar 2017 20:06:18 GMT
ENV ARANGO_VERSION=2.8.11
# Tue, 21 Mar 2017 20:06:18 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0
# Tue, 21 Mar 2017 20:06:19 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Tue, 21 Mar 2017 20:06:20 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Tue, 21 Mar 2017 20:06:20 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Tue, 21 Mar 2017 20:07:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 21 Mar 2017 20:07:04 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Tue, 21 Mar 2017 20:07:05 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Tue, 21 Mar 2017 20:07:06 GMT
COPY file:d5e2df43b028efe92b9f4dc2dfd67aa54840beb1e09b6c23c32ae8403b0ae7e4 in /entrypoint.sh 
# Tue, 21 Mar 2017 20:07:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:07:08 GMT
EXPOSE 8529/tcp
# Tue, 21 Mar 2017 20:07:08 GMT
USER [arangodb]
# Tue, 21 Mar 2017 20:07:09 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a8c4a5ee51c8937b0f67690a5fcfe004947319831e056b656b94eca2fa54bc`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 7.4 KB (7375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5368df4dd868f3471e46bf093a1d4cc50cde817f30fc8dd447cae6a9225a6`  
		Last Modified: Thu, 23 Mar 2017 17:05:06 GMT  
		Size: 58.9 MB (58882704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a7adeea9e791a44310c30b958fdd65790d28a8077803ee240cc35c8ab1de`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229a514e232b0b96473fed7d860d79ee91e90df7bf95c950100fe74eff2b121e`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:2.8.11`

```console
$ docker pull arangodb@sha256:17cf67234a2168b502e372ff50cad58815019c00fc2d17e345429dcd9747ed49
```

-	Platforms:
	-	linux; amd64

### `arangodb:2.8.11` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110329817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca336d6bb6a1edc68396955640387950ffce2643ff2e25aeef9a6da9a222a3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:06:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Mar 2017 20:06:16 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 21 Mar 2017 20:06:17 GMT
ENV ARCHITECTURE=amd64
# Tue, 21 Mar 2017 20:06:18 GMT
ENV ARANGO_VERSION=2.8.11
# Tue, 21 Mar 2017 20:06:18 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0
# Tue, 21 Mar 2017 20:06:19 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Tue, 21 Mar 2017 20:06:20 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Tue, 21 Mar 2017 20:06:20 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Tue, 21 Mar 2017 20:07:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 21 Mar 2017 20:07:04 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Tue, 21 Mar 2017 20:07:05 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Tue, 21 Mar 2017 20:07:06 GMT
COPY file:d5e2df43b028efe92b9f4dc2dfd67aa54840beb1e09b6c23c32ae8403b0ae7e4 in /entrypoint.sh 
# Tue, 21 Mar 2017 20:07:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:07:08 GMT
EXPOSE 8529/tcp
# Tue, 21 Mar 2017 20:07:08 GMT
USER [arangodb]
# Tue, 21 Mar 2017 20:07:09 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a8c4a5ee51c8937b0f67690a5fcfe004947319831e056b656b94eca2fa54bc`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 7.4 KB (7375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5368df4dd868f3471e46bf093a1d4cc50cde817f30fc8dd447cae6a9225a6`  
		Last Modified: Thu, 23 Mar 2017 17:05:06 GMT  
		Size: 58.9 MB (58882704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a7adeea9e791a44310c30b958fdd65790d28a8077803ee240cc35c8ab1de`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229a514e232b0b96473fed7d860d79ee91e90df7bf95c950100fe74eff2b121e`  
		Last Modified: Thu, 23 Mar 2017 17:04:44 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.1`

```console
$ docker pull arangodb@sha256:17cfd33adf62682705acd9e70cc26f8b1ef1391167c901541801354db28aa3ec
```

-	Platforms:
	-	linux; amd64

### `arangodb:3.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127455943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b70531700323a39562a5cabe524228ed40fc09c50a2a83f553abcaf0a183af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:06:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Mar 2017 20:07:10 GMT
ENV ARCHITECTURE=amd64
# Tue, 21 Mar 2017 20:07:11 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_VERSION=3.1.15
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0
# Tue, 21 Mar 2017 20:07:13 GMT
ENV ARANGO_PACKAGE=arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb.asc
# Tue, 21 Mar 2017 20:07:16 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 21 Mar 2017 20:07:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1 	libsnappy1         ca-certificates         pwgen         curl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:07:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Mar 2017 20:08:03 GMT
RUN curl -O ${ARANGO_SIGNATURE_URL} &&           curl -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb3/arangod.conf     &&     DEBIAN_FRONTEND="noninteractive" apt-get purge -y --auto-remove ca-certificates &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 21 Mar 2017 20:08:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Mar 2017 20:08:05 GMT
COPY file:9f20ed9a2181af8ddc12371a0082e7645aa20b1008b5f484851bcc399e64801e in /entrypoint.sh 
# Tue, 21 Mar 2017 20:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:08:07 GMT
EXPOSE 8529/tcp
# Tue, 21 Mar 2017 20:08:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aac3f5a389f61371e927fe497e7885f75a1e04bfbf6b33b2fcf54e63c71e6d`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 7.4 KB (7372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72be309340ae1172e9643de72f5b42db7f747d52d4947614fbecd955edd919`  
		Last Modified: Thu, 23 Mar 2017 17:06:08 GMT  
		Size: 6.8 MB (6763631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d871105121328db1c3fdb6a6534a93524ef4040751cdc2e35e387628290a7a`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d5919206fc813a8f4af7edfcd7444148bb847ee2e3a1617e5ae42428060c67`  
		Last Modified: Thu, 23 Mar 2017 17:06:31 GMT  
		Size: 69.2 MB (69244913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563b6199fa247c7c147d08390142b572c96eabec54e6a11340fa25b859bd47e`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.1.15`

```console
$ docker pull arangodb@sha256:17cfd33adf62682705acd9e70cc26f8b1ef1391167c901541801354db28aa3ec
```

-	Platforms:
	-	linux; amd64

### `arangodb:3.1.15` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127455943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b70531700323a39562a5cabe524228ed40fc09c50a2a83f553abcaf0a183af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:06:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Mar 2017 20:07:10 GMT
ENV ARCHITECTURE=amd64
# Tue, 21 Mar 2017 20:07:11 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_VERSION=3.1.15
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0
# Tue, 21 Mar 2017 20:07:13 GMT
ENV ARANGO_PACKAGE=arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb.asc
# Tue, 21 Mar 2017 20:07:16 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 21 Mar 2017 20:07:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1 	libsnappy1         ca-certificates         pwgen         curl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:07:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Mar 2017 20:08:03 GMT
RUN curl -O ${ARANGO_SIGNATURE_URL} &&           curl -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb3/arangod.conf     &&     DEBIAN_FRONTEND="noninteractive" apt-get purge -y --auto-remove ca-certificates &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 21 Mar 2017 20:08:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Mar 2017 20:08:05 GMT
COPY file:9f20ed9a2181af8ddc12371a0082e7645aa20b1008b5f484851bcc399e64801e in /entrypoint.sh 
# Tue, 21 Mar 2017 20:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:08:07 GMT
EXPOSE 8529/tcp
# Tue, 21 Mar 2017 20:08:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aac3f5a389f61371e927fe497e7885f75a1e04bfbf6b33b2fcf54e63c71e6d`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 7.4 KB (7372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72be309340ae1172e9643de72f5b42db7f747d52d4947614fbecd955edd919`  
		Last Modified: Thu, 23 Mar 2017 17:06:08 GMT  
		Size: 6.8 MB (6763631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d871105121328db1c3fdb6a6534a93524ef4040751cdc2e35e387628290a7a`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d5919206fc813a8f4af7edfcd7444148bb847ee2e3a1617e5ae42428060c67`  
		Last Modified: Thu, 23 Mar 2017 17:06:31 GMT  
		Size: 69.2 MB (69244913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563b6199fa247c7c147d08390142b572c96eabec54e6a11340fa25b859bd47e`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:17cfd33adf62682705acd9e70cc26f8b1ef1391167c901541801354db28aa3ec
```

-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127455943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b70531700323a39562a5cabe524228ed40fc09c50a2a83f553abcaf0a183af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 20:06:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Mar 2017 20:07:10 GMT
ENV ARCHITECTURE=amd64
# Tue, 21 Mar 2017 20:07:11 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_VERSION=3.1.15
# Tue, 21 Mar 2017 20:07:12 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0
# Tue, 21 Mar 2017 20:07:13 GMT
ENV ARANGO_PACKAGE=arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb
# Tue, 21 Mar 2017 20:07:14 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.15-1_amd64.deb.asc
# Tue, 21 Mar 2017 20:07:16 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 21 Mar 2017 20:07:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1 	libsnappy1         ca-certificates         pwgen         curl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:07:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 21 Mar 2017 20:08:03 GMT
RUN curl -O ${ARANGO_SIGNATURE_URL} &&           curl -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb3/arangod.conf     &&     DEBIAN_FRONTEND="noninteractive" apt-get purge -y --auto-remove ca-certificates &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 21 Mar 2017 20:08:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Mar 2017 20:08:05 GMT
COPY file:9f20ed9a2181af8ddc12371a0082e7645aa20b1008b5f484851bcc399e64801e in /entrypoint.sh 
# Tue, 21 Mar 2017 20:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Mar 2017 20:08:07 GMT
EXPOSE 8529/tcp
# Tue, 21 Mar 2017 20:08:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0aac3f5a389f61371e927fe497e7885f75a1e04bfbf6b33b2fcf54e63c71e6d`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 7.4 KB (7372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72be309340ae1172e9643de72f5b42db7f747d52d4947614fbecd955edd919`  
		Last Modified: Thu, 23 Mar 2017 17:06:08 GMT  
		Size: 6.8 MB (6763631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d871105121328db1c3fdb6a6534a93524ef4040751cdc2e35e387628290a7a`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d5919206fc813a8f4af7edfcd7444148bb847ee2e3a1617e5ae42428060c67`  
		Last Modified: Thu, 23 Mar 2017 17:06:31 GMT  
		Size: 69.2 MB (69244913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563b6199fa247c7c147d08390142b572c96eabec54e6a11340fa25b859bd47e`  
		Last Modified: Thu, 23 Mar 2017 17:06:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
