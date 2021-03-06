## `nginx:stable`

```console
$ docker pull nginx@sha256:d2e97f203a5ae23d64ca5b6d98e0c5bdbe3b93d0733d18cc311aaed8a9874886
```

-	Platforms:
	-	linux; amd64

### `nginx:stable` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44025712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cd30abd3d93274542281d0bed6bec90fd76c067a3d1118905a7f83d9d7f1c0`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 20 Jun 2017 20:25:26 GMT
ADD file:54d82a3a8fe8d47aaa58650783f2a7198891e89ca95d6e7455f8999651c2fc98 in / 
# Tue, 20 Jun 2017 20:25:27 GMT
CMD ["bash"]
# Fri, 23 Jun 2017 00:54:51 GMT
MAINTAINER NGINX Docker Maintainers "docker-maint@nginx.com"
# Tue, 11 Jul 2017 18:59:46 GMT
ENV NGINX_VERSION=1.12.1-1~stretch
# Tue, 11 Jul 2017 18:59:46 GMT
ENV NJS_VERSION=1.12.1.0.1.10-1~stretch
# Tue, 11 Jul 2017 19:00:01 GMT
RUN apt-get update 	&& apt-get install --no-install-recommends --no-install-suggests -y gnupg1 	&& 	NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62; 	found=''; 	for server in 		ha.pool.sks-keyservers.net 		hkp://keyserver.ubuntu.com:80 		hkp://p80.pool.sks-keyservers.net:80 		pgp.mit.edu 	; do 		echo "Fetching GPG key $NGINX_GPGKEY from $server"; 		apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break; 	done; 	test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1; 	apt-get remove --purge -y gnupg1 && apt-get -y --purge autoremove && rm -rf /var/lib/apt/lists/* 	&& echo "deb http://nginx.org/packages/debian/ stretch nginx" >> /etc/apt/sources.list 	&& apt-get update 	&& apt-get install --no-install-recommends --no-install-suggests -y 						nginx=${NGINX_VERSION} 						nginx-module-xslt=${NGINX_VERSION} 						nginx-module-geoip=${NGINX_VERSION} 						nginx-module-image-filter=${NGINX_VERSION} 						nginx-module-njs=${NJS_VERSION} 						gettext-base 	&& rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2017 19:00:04 GMT
RUN ln -sf /dev/stdout /var/log/nginx/access.log 	&& ln -sf /dev/stderr /var/log/nginx/error.log
# Tue, 11 Jul 2017 19:00:05 GMT
EXPOSE 80/tcp
# Tue, 11 Jul 2017 19:00:05 GMT
STOPSIGNAL [SIGTERM]
# Tue, 11 Jul 2017 19:00:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e6e142a992028745fdbaf21d647cd3c61086cd0c1b50a25f07a5d7dbaa446cdd`  
		Last Modified: Tue, 20 Jun 2017 20:56:34 GMT  
		Size: 22.5 MB (22501182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f66c1e7639e59fb3dce1b96098afe8bc5b64c371bccac1e90454df7b2deb445`  
		Last Modified: Tue, 11 Jul 2017 19:09:48 GMT  
		Size: 21.5 MB (21524336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77192c2820af07da56435e5a3bf9145e896fdc0f3d0491bf680c575cf914f44f`  
		Last Modified: Tue, 11 Jul 2017 19:09:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
