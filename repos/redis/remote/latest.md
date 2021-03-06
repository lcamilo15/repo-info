## `redis:latest`

```console
$ docker pull redis@sha256:1b358a2b0dc2629af3ed75737e2f07e5b3408eabf76a8fa99606ec0c276a93f8
```

-	Platforms:
	-	linux; amd64

### `redis:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74409376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d6014ac5c8193fa43dd16b161f0e524141800f10cff44d7bad3b637991cf16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Wed, 22 Mar 2017 00:04:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 22 Mar 2017 15:06:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Mar 2017 15:06:51 GMT
ENV GOSU_VERSION=1.7
# Wed, 22 Mar 2017 15:06:56 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 22 Mar 2017 15:06:56 GMT
ENV REDIS_VERSION=3.2.8
# Wed, 22 Mar 2017 15:06:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.8.tar.gz
# Wed, 22 Mar 2017 15:06:57 GMT
ENV REDIS_DOWNLOAD_SHA1=6780d1abb66f33a97aad0edbe020403d0a15b67f
# Wed, 22 Mar 2017 15:07:41 GMT
RUN set -ex 		&& buildDeps=' 		gcc 		libc6-dev 		make 	' 	&& apt-get update 	&& apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL" 	&& echo "$REDIS_DOWNLOAD_SHA1 *redis.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/redis 	&& tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1 	&& rm redis.tar.gz 		&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h 	&& sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h 	&& grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h 		&& make -C /usr/src/redis 	&& make -C /usr/src/redis install 		&& rm -r /usr/src/redis 		&& apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Mar 2017 15:07:42 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 22 Mar 2017 15:07:43 GMT
VOLUME [/data]
# Wed, 22 Mar 2017 15:07:43 GMT
WORKDIR /data
# Wed, 22 Mar 2017 15:07:44 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 22 Mar 2017 15:07:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Mar 2017 15:07:44 GMT
EXPOSE 6379/tcp
# Wed, 22 Mar 2017 15:07:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787f13ab8ea910bcc271068eab4c454ed8c5ba45156dd3e393a742a4826ebfad`  
		Last Modified: Fri, 24 Mar 2017 00:29:12 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14faf2bdac07deb52fa72e15675bbef90c4da9fb5c6ac5d52f7ad568fb5719bb`  
		Last Modified: Fri, 24 Mar 2017 00:29:17 GMT  
		Size: 16.7 MB (16689642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52905ba81f398b8d62f1a7f7d30f40aa08f0984955fa240256eb909f8a84cdd`  
		Last Modified: Fri, 24 Mar 2017 00:29:11 GMT  
		Size: 807.9 KB (807927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de079db59e0eb783f8c44a1b94733cb5b32916297a558a019c2e8522a2996bd5`  
		Last Modified: Fri, 24 Mar 2017 00:30:48 GMT  
		Size: 5.5 MB (5470795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34450ffcb858c9f4a1ca4f15df048b93ab28a70e199d65bddd8242d22c699ddd`  
		Last Modified: Fri, 24 Mar 2017 00:30:46 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a08f1c245e8ae4ddc5d652cf82a8fc6be2c4d68f54254be5cd496c89fe47667`  
		Last Modified: Fri, 24 Mar 2017 00:30:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
