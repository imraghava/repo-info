## `docker:stable-git`

```console
$ docker pull docker@sha256:1334596561b0d545a0f9829f7a6901f452700c3adb5ca8997c17f042f163c6e7
```

-	Platforms:
	-	linux; amd64

### `docker:stable-git` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41422683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988e1d2f18e1f65e51eaf064302c7b39d15f39189a17e5353442ad75e4a84071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Jun 2017 18:39:21 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Tue, 27 Jun 2017 18:39:45 GMT
CMD ["/bin/sh"]
# Tue, 27 Jun 2017 20:09:43 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 27 Jun 2017 20:15:25 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 29 Jun 2017 21:39:59 GMT
ENV DOCKER_VERSION=17.03.2-ce
# Thu, 29 Jun 2017 21:40:06 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Thu, 29 Jun 2017 21:40:08 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Thu, 29 Jun 2017 21:40:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jun 2017 21:40:34 GMT
CMD ["sh"]
# Thu, 29 Jun 2017 21:43:01 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9253de26747cb9ad807096c7779b82609261ad1c5cbee1e502a86c9b0af4da`  
		Last Modified: Thu, 29 Jun 2017 19:08:48 GMT  
		Size: 350.6 KB (350624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d097821ea2c9d225166fe3401d4fb3539096cd03f47ecf2605fcb5c6583a9e92`  
		Last Modified: Thu, 29 Jun 2017 22:13:16 GMT  
		Size: 28.1 MB (28110648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f5b9db32b4c9eec4278d5c656bf09154420adf7a44292a765d216de6df08eb`  
		Last Modified: Thu, 29 Jun 2017 22:13:08 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9ba40f5a0e21be49c372df884a6587f602bdffecc8f9fcd6a785c4ad46e9a1`  
		Last Modified: Thu, 29 Jun 2017 22:20:16 GMT  
		Size: 11.0 MB (10990411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
