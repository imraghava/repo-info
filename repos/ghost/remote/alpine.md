## `ghost:alpine`

```console
$ docker pull ghost@sha256:e7909ecd536e13d73b2f1239aedfc2371244647ac6f78207ab9384762ce9ea4b
```

-	Platforms:
	-	linux; amd64

### `ghost:alpine` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40964484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2320a2cfdf957f86e927cf0e1a45a7b13eef6f456c308aa77f8fb2244f09278b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 27 Jun 2017 18:37:38 GMT
ADD file:89e72bfc19e81624ba6a34bd5cecdf258750dc569ba03e17e3f4a286b1526461 in / 
# Tue, 27 Jun 2017 18:38:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jun 2017 18:32:43 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 11 Jul 2017 23:20:01 GMT
ENV NODE_VERSION=4.8.4
# Tue, 11 Jul 2017 23:27:09 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 11 Jul 2017 23:27:09 GMT
ENV YARN_VERSION=0.24.4
# Tue, 11 Jul 2017 23:27:18 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 11 Jul 2017 23:27:18 GMT
CMD ["node"]
# Wed, 12 Jul 2017 16:27:43 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 12 Jul 2017 16:27:47 GMT
RUN apk add --no-cache 		bash 		tar
# Wed, 12 Jul 2017 16:27:48 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 12 Jul 2017 16:27:48 GMT
WORKDIR /usr/src/ghost
# Wed, 12 Jul 2017 16:27:49 GMT
ENV GHOST_VERSION=0.11.10
# Wed, 12 Jul 2017 16:28:28 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 12 Jul 2017 16:28:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 12 Jul 2017 16:28:29 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 12 Jul 2017 16:28:30 GMT
VOLUME [/var/lib/ghost]
# Wed, 12 Jul 2017 16:28:31 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Wed, 12 Jul 2017 16:28:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jul 2017 16:28:32 GMT
EXPOSE 2368/tcp
# Wed, 12 Jul 2017 16:28:32 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:90f4dba627d65ea3223761bcfe54e726337a919fe98117ef107914f91be657c9`  
		Last Modified: Tue, 27 Jun 2017 18:47:56 GMT  
		Size: 2.4 MB (2385007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302ce48cc18573629a7038cc1dc77c9308a93680ed8657560090d50c7aa64589`  
		Last Modified: Tue, 11 Jul 2017 23:41:38 GMT  
		Size: 10.5 MB (10549466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c17ba3935d6420981a057d8afb8bb2728c77ecca498088a9e17dbd595df019`  
		Last Modified: Tue, 11 Jul 2017 23:41:36 GMT  
		Size: 908.0 KB (907953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86fd5d5e80035eb3ca0541f22236b30988a7d1daeb1c1642f69eaf428b2bda`  
		Last Modified: Wed, 12 Jul 2017 16:29:33 GMT  
		Size: 8.3 KB (8314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6139c361248ab8a8bcd75289e71dfeaf1698a44ec2cf12ced72593d8ef9e84d`  
		Last Modified: Wed, 12 Jul 2017 16:29:33 GMT  
		Size: 1.3 MB (1340408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a700ec450ffcebc177ab43e3ffdd9f5f49723afe7473558a1dbece42fff5646`  
		Last Modified: Wed, 12 Jul 2017 16:29:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bfb4c3ffa1617e3fd6288349b520f1ec7dffd60e1092d548e48488eff52610`  
		Last Modified: Wed, 12 Jul 2017 16:29:39 GMT  
		Size: 25.8 MB (25772396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090e5d8bb33f26a99815d9a1fa968d39e6c5d2bd7074d0c3827020b7460930ed`  
		Last Modified: Wed, 12 Jul 2017 16:29:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986075aca768e492354176fcf88dac60eb235d4e6e1b5112670d6dab2818ddfe`  
		Last Modified: Wed, 12 Jul 2017 16:29:33 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
