## `jetty:9-jre8`

```console
$ docker pull jetty@sha256:ba36bb44f5871dd61045d2c4d4bda4b81e79fa85461b7405798a27705a6a6157
```

-	Platforms:
	-	linux; amd64

### `jetty:9-jre8` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132523261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daf7c9293500da304fbd7324929026dcc8fed47a327c50e24a886f557875470`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

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
# Wed, 22 Mar 2017 21:13:52 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 22 Mar 2017 21:13:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Mar 2017 21:13:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Mar 2017 21:13:53 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 22 Mar 2017 21:13:54 GMT
WORKDIR /usr/local/jetty
# Wed, 22 Mar 2017 21:13:54 GMT
ENV JETTY_VERSION=9.4.2.v20170220
# Wed, 22 Mar 2017 21:13:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.2.v20170220/jetty-home-9.4.2.v20170220.tar.gz
# Wed, 22 Mar 2017 21:13:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D
# Wed, 22 Mar 2017 21:14:01 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -r "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 22 Mar 2017 21:14:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Mar 2017 21:14:02 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 22 Mar 2017 21:14:02 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Mar 2017 21:14:05 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket,setuid" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 22 Mar 2017 21:14:05 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Mar 2017 21:14:06 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 22 Mar 2017 21:14:07 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Wed, 22 Mar 2017 21:14:07 GMT
EXPOSE 8080/tcp
# Wed, 22 Mar 2017 21:14:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Mar 2017 21:14:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
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
	-	`sha256:6744b2582cf711157f9f5e8df751e0c5736c2b2f4e434cfc7304dbeb224c058e`  
		Last Modified: Fri, 24 Mar 2017 02:14:54 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e04f4415c940f3389af6cc1bdabf42acb2a513656c568cb14d3730bab35993`  
		Last Modified: Fri, 24 Mar 2017 02:14:56 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47495766333e608c974ef27b91b99361bfa68af950065ebd581a62f587a9773`  
		Last Modified: Fri, 24 Mar 2017 02:19:09 GMT  
		Size: 8.0 MB (8026351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85522928607c407d156d3e459c8b8c22bcba1e3e769d557d90f7b8542752d435`  
		Last Modified: Fri, 24 Mar 2017 02:19:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b37d307f99c40bc9512823d9ce706b57d9d3b9766ec5937970d4375fd0c1a4`  
		Last Modified: Fri, 24 Mar 2017 02:19:08 GMT  
		Size: 2.2 KB (2239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc17d2b76930397b73ebfec563b9630033b4689d18cfc5a0de3d8f350caaac2f`  
		Last Modified: Fri, 24 Mar 2017 02:19:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dcf24f246d41629fa1089c229685874cd0f80fe7df8ea6a3bf14f269c047f2`  
		Last Modified: Fri, 24 Mar 2017 02:19:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
