## `elasticsearch:latest`

```console
$ docker pull elasticsearch@sha256:a85104366d28f5b758680a449f281369cbcb0fdb96f4ce217204bdaa18572e38
```

-	Platforms:
	-	linux; amd64

### `elasticsearch:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159640463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0206b7302cfeb1b3296ed980d732c517bddc0d18b84edbfed7fd2461b5e86351`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["elasticsearch"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:49:14 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 21 Mar 2017 22:49:15 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 22:49:16 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 21 Mar 2017 22:49:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
# Tue, 21 Mar 2017 22:49:17 GMT
ENV JAVA_VERSION=8u121
# Tue, 21 Mar 2017 22:49:18 GMT
ENV JAVA_DEBIAN_VERSION=8u121-b13-1~bpo8+1
# Tue, 21 Mar 2017 22:49:18 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20161107~bpo8+1
# Tue, 21 Mar 2017 22:51:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 21 Mar 2017 22:51:35 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 22 Mar 2017 18:13:12 GMT
ENV GOSU_VERSION=1.7
# Wed, 22 Mar 2017 18:13:17 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 22 Mar 2017 18:13:18 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 22 Mar 2017 18:13:59 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends apt-transport-https && rm -rf /var/lib/apt/lists/* 	&& echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/elasticsearch.list
# Wed, 22 Mar 2017 18:13:59 GMT
ENV ELASTICSEARCH_VERSION=5.2.2
# Wed, 22 Mar 2017 18:14:00 GMT
ENV ELASTICSEARCH_DEB_VERSION=5.2.2
# Wed, 22 Mar 2017 18:14:07 GMT
RUN set -x 		&& dpkg-divert --rename /usr/lib/sysctl.d/elasticsearch.conf 		&& apt-get update 	&& apt-get install -y --no-install-recommends "elasticsearch=$ELASTICSEARCH_DEB_VERSION" 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Mar 2017 18:14:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Mar 2017 18:14:08 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Mar 2017 18:14:09 GMT
RUN set -ex 	&& for path in 		./data 		./logs 		./config 		./config/scripts 	; do 		mkdir -p "$path"; 		chown -R elasticsearch:elasticsearch "$path"; 	done
# Wed, 22 Mar 2017 18:14:10 GMT
COPY dir:c3faa196a3b1c87063ffe0be6ee20b5f2b36a9589fd93336acab4ba1aa6f6855 in ./config 
# Wed, 22 Mar 2017 18:14:10 GMT
VOLUME [/usr/share/elasticsearch/data]
# Wed, 22 Mar 2017 18:14:11 GMT
COPY file:251082110c6dbdf83c7e443f9451d18e88f56dde65a4e4cbf7b58db1440ef558 in / 
# Wed, 22 Mar 2017 18:14:11 GMT
EXPOSE 9200/tcp 9300/tcp
# Wed, 22 Mar 2017 18:14:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 18:14:13 GMT
CMD ["elasticsearch"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e483851652b9825b74947a58f00868b38247c47aa454d09adcbc42ca5a4404`  
		Last Modified: Thu, 23 Mar 2017 18:42:42 GMT  
		Size: 567.0 KB (566964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef624abeb7b86d6e49695d5e19f510137408c991650ff916ccf1d613aa8924a3`  
		Last Modified: Thu, 23 Mar 2017 18:50:10 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e108ce2208d5e025afd56527699370e2c719b307767fa724af487b796cb1579`  
		Last Modified: Thu, 23 Mar 2017 18:50:07 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a77bcb48281269d007610db1bdef9ab31529861d13edd629ed65e8098c6fc4b`  
		Last Modified: Thu, 23 Mar 2017 18:50:25 GMT  
		Size: 53.6 MB (53590203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016fd08a71c81e3ed7358c4856c567a2571f98e8a2953f672d81c5e964a2262c`  
		Last Modified: Thu, 23 Mar 2017 18:50:13 GMT  
		Size: 289.0 KB (289029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae28fdc2aee4647c43f0898653c1ad8011aaa51886d7d38fa51be1705d79b18`  
		Last Modified: Fri, 24 Mar 2017 01:49:29 GMT  
		Size: 807.9 KB (807927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d01e9bc296af56cf592d4a0be1a33b6fa9c761e23325581d2b7d83b2e17854`  
		Last Modified: Fri, 24 Mar 2017 01:49:28 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af4e4a260e6d4bb0b5a9aea266b43906e8a3122c199efafa7c2faedf51604cf`  
		Last Modified: Fri, 24 Mar 2017 01:51:42 GMT  
		Size: 536.2 KB (536245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3bd02b07c559facd0359432024754e3b85f17e8f02ff13c8d890dec20c2c26`  
		Last Modified: Fri, 24 Mar 2017 01:51:45 GMT  
		Size: 33.8 MB (33802042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ee26cdb5d333f54b536df008099f3dce7c2ad648608827177e819160bfaeca`  
		Last Modified: Fri, 24 Mar 2017 01:51:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cc86817cba25ac3e658ab87c614e73e0b1953c0c268d10f821ca17bc3d7aff`  
		Last Modified: Fri, 24 Mar 2017 01:51:42 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e8c2ea96f4ca917e24a9a38a80c48135d19f981487401882482abeae8beaa6`  
		Last Modified: Fri, 24 Mar 2017 01:51:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
