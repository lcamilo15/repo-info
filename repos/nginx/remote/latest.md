## `nginx:latest`

```console
$ docker pull nginx@sha256:52a189e49c0c797cfc5cbfe578c68c225d160fb13a42954144b29af3fe4fe335
```

-	Platforms:
	-	linux; amd64

### `nginx:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71605546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b914bbcb89e49851990e064568dceee4d53a462f316ec36207599c12ae9ba65`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 15:14:51 GMT
MAINTAINER NGINX Docker Maintainers "docker-maint@nginx.com"
# Tue, 28 Feb 2017 15:14:51 GMT
ENV NGINX_VERSION=1.11.10-1~jessie
# Tue, 28 Feb 2017 15:15:06 GMT
RUN apt-key adv --keyserver hkp://pgp.mit.edu:80 --recv-keys 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 	&& echo "deb http://nginx.org/packages/mainline/debian/ jessie nginx" >> /etc/apt/sources.list 	&& apt-get update 	&& apt-get install --no-install-recommends --no-install-suggests -y 						ca-certificates 						nginx=${NGINX_VERSION} 						nginx-module-xslt 						nginx-module-geoip 						nginx-module-image-filter 						nginx-module-perl 						nginx-module-njs 						gettext-base 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 15:15:07 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log 	&& ln -sf /dev/stderr /var/log/nginx/error.log
# Tue, 28 Feb 2017 15:15:08 GMT
EXPOSE 443/tcp 80/tcp
# Tue, 28 Feb 2017 15:15:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6decb850d2bc195e977880bcec1d4466ceb6ca0c48d1fa7a2efc7dd43595a44f`  
		Last Modified: Thu, 02 Mar 2017 02:17:55 GMT  
		Size: 20.2 MB (20241978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e19f087ed6e9f950779e85e7ee0198b25eb8063a98df13ad2a951f83ccdc3b`  
		Last Modified: Thu, 02 Mar 2017 02:17:47 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
