<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:0.57.1`](#rocketchat0571)
-	[`rocket.chat:0.57`](#rocketchat057)
-	[`rocket.chat:0`](#rocketchat0)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:0.57.1`

```console
$ docker pull rocket.chat@sha256:2757b636135d04b84f64b87cca20e5e9a3b5fdbd9edbba2daedbf8013526b920
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0.57.1` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189266841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7deae78ecf4c42eb0a7c088cf133e794a1acbe59ffbb5851fba304c24ee18`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Jul 2017 22:11:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 08 Jul 2017 04:20:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 08 Jul 2017 04:23:56 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Sat, 08 Jul 2017 04:23:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 11 Jul 2017 23:27:37 GMT
ENV NODE_VERSION=4.8.4
# Tue, 11 Jul 2017 23:27:49 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 11 Jul 2017 23:27:50 GMT
ENV YARN_VERSION=0.24.4
# Tue, 11 Jul 2017 23:27:53 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 11 Jul 2017 23:27:54 GMT
CMD ["node"]
# Wed, 12 Jul 2017 16:31:50 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 12 Jul 2017 16:31:51 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat.rocketchat /app/uploads
# Wed, 12 Jul 2017 16:31:51 GMT
VOLUME [/app/uploads]
# Wed, 12 Jul 2017 16:31:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 12 Jul 2017 16:31:53 GMT
ENV RC_VERSION=0.57.1
# Wed, 12 Jul 2017 16:31:54 GMT
WORKDIR /app
# Wed, 12 Jul 2017 16:32:39 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 12 Jul 2017 16:32:41 GMT
USER [rocketchat]
# Wed, 12 Jul 2017 16:32:41 GMT
WORKDIR /app/bundle
# Wed, 12 Jul 2017 16:32:42 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 12 Jul 2017 16:32:43 GMT
EXPOSE 3000/tcp
# Wed, 12 Jul 2017 16:32:43 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405c8e05a47440060907f35b13c15d3346452f19cf1db17c659568eb3391e90`  
		Last Modified: Mon, 10 Jul 2017 18:16:29 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eeeb57a2cd360c68be9ca1a01878bf2be388153a1874b87c2dd1a19a0ae79d`  
		Last Modified: Mon, 10 Jul 2017 18:16:26 GMT  
		Size: 119.2 KB (119157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fdfa03cee406af9161ee7783cfd9d9e09c6495280dba0f99032350d0e7d9aa`  
		Last Modified: Tue, 11 Jul 2017 23:43:12 GMT  
		Size: 12.4 MB (12420659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35934788e1f4f8661ea49c2b728356a69498ec68f4ded86f3ef3ae7779c9fa1`  
		Last Modified: Tue, 11 Jul 2017 23:43:05 GMT  
		Size: 900.6 KB (900598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16cf98e3d7ab167b663f3d76743d84537d8d0d1b7726ca1dc90c1c66d61f93`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7294826e2fb9e19c7814832b2413f506d42029239123b21060c70c98d6680e9e`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 127.2 KB (127205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc40f9bb83064f019be73d49157c39dc4eb16f56a7c63f200205bb83c1f3ab12`  
		Last Modified: Wed, 12 Jul 2017 16:33:15 GMT  
		Size: 103.8 MB (103813521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:0.57`

```console
$ docker pull rocket.chat@sha256:2757b636135d04b84f64b87cca20e5e9a3b5fdbd9edbba2daedbf8013526b920
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0.57` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189266841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7deae78ecf4c42eb0a7c088cf133e794a1acbe59ffbb5851fba304c24ee18`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Jul 2017 22:11:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 08 Jul 2017 04:20:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 08 Jul 2017 04:23:56 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Sat, 08 Jul 2017 04:23:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 11 Jul 2017 23:27:37 GMT
ENV NODE_VERSION=4.8.4
# Tue, 11 Jul 2017 23:27:49 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 11 Jul 2017 23:27:50 GMT
ENV YARN_VERSION=0.24.4
# Tue, 11 Jul 2017 23:27:53 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 11 Jul 2017 23:27:54 GMT
CMD ["node"]
# Wed, 12 Jul 2017 16:31:50 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 12 Jul 2017 16:31:51 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat.rocketchat /app/uploads
# Wed, 12 Jul 2017 16:31:51 GMT
VOLUME [/app/uploads]
# Wed, 12 Jul 2017 16:31:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 12 Jul 2017 16:31:53 GMT
ENV RC_VERSION=0.57.1
# Wed, 12 Jul 2017 16:31:54 GMT
WORKDIR /app
# Wed, 12 Jul 2017 16:32:39 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 12 Jul 2017 16:32:41 GMT
USER [rocketchat]
# Wed, 12 Jul 2017 16:32:41 GMT
WORKDIR /app/bundle
# Wed, 12 Jul 2017 16:32:42 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 12 Jul 2017 16:32:43 GMT
EXPOSE 3000/tcp
# Wed, 12 Jul 2017 16:32:43 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405c8e05a47440060907f35b13c15d3346452f19cf1db17c659568eb3391e90`  
		Last Modified: Mon, 10 Jul 2017 18:16:29 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eeeb57a2cd360c68be9ca1a01878bf2be388153a1874b87c2dd1a19a0ae79d`  
		Last Modified: Mon, 10 Jul 2017 18:16:26 GMT  
		Size: 119.2 KB (119157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fdfa03cee406af9161ee7783cfd9d9e09c6495280dba0f99032350d0e7d9aa`  
		Last Modified: Tue, 11 Jul 2017 23:43:12 GMT  
		Size: 12.4 MB (12420659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35934788e1f4f8661ea49c2b728356a69498ec68f4ded86f3ef3ae7779c9fa1`  
		Last Modified: Tue, 11 Jul 2017 23:43:05 GMT  
		Size: 900.6 KB (900598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16cf98e3d7ab167b663f3d76743d84537d8d0d1b7726ca1dc90c1c66d61f93`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7294826e2fb9e19c7814832b2413f506d42029239123b21060c70c98d6680e9e`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 127.2 KB (127205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc40f9bb83064f019be73d49157c39dc4eb16f56a7c63f200205bb83c1f3ab12`  
		Last Modified: Wed, 12 Jul 2017 16:33:15 GMT  
		Size: 103.8 MB (103813521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:0`

```console
$ docker pull rocket.chat@sha256:2757b636135d04b84f64b87cca20e5e9a3b5fdbd9edbba2daedbf8013526b920
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189266841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7deae78ecf4c42eb0a7c088cf133e794a1acbe59ffbb5851fba304c24ee18`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Jul 2017 22:11:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 08 Jul 2017 04:20:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 08 Jul 2017 04:23:56 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Sat, 08 Jul 2017 04:23:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 11 Jul 2017 23:27:37 GMT
ENV NODE_VERSION=4.8.4
# Tue, 11 Jul 2017 23:27:49 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 11 Jul 2017 23:27:50 GMT
ENV YARN_VERSION=0.24.4
# Tue, 11 Jul 2017 23:27:53 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 11 Jul 2017 23:27:54 GMT
CMD ["node"]
# Wed, 12 Jul 2017 16:31:50 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 12 Jul 2017 16:31:51 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat.rocketchat /app/uploads
# Wed, 12 Jul 2017 16:31:51 GMT
VOLUME [/app/uploads]
# Wed, 12 Jul 2017 16:31:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 12 Jul 2017 16:31:53 GMT
ENV RC_VERSION=0.57.1
# Wed, 12 Jul 2017 16:31:54 GMT
WORKDIR /app
# Wed, 12 Jul 2017 16:32:39 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 12 Jul 2017 16:32:41 GMT
USER [rocketchat]
# Wed, 12 Jul 2017 16:32:41 GMT
WORKDIR /app/bundle
# Wed, 12 Jul 2017 16:32:42 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 12 Jul 2017 16:32:43 GMT
EXPOSE 3000/tcp
# Wed, 12 Jul 2017 16:32:43 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405c8e05a47440060907f35b13c15d3346452f19cf1db17c659568eb3391e90`  
		Last Modified: Mon, 10 Jul 2017 18:16:29 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eeeb57a2cd360c68be9ca1a01878bf2be388153a1874b87c2dd1a19a0ae79d`  
		Last Modified: Mon, 10 Jul 2017 18:16:26 GMT  
		Size: 119.2 KB (119157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fdfa03cee406af9161ee7783cfd9d9e09c6495280dba0f99032350d0e7d9aa`  
		Last Modified: Tue, 11 Jul 2017 23:43:12 GMT  
		Size: 12.4 MB (12420659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35934788e1f4f8661ea49c2b728356a69498ec68f4ded86f3ef3ae7779c9fa1`  
		Last Modified: Tue, 11 Jul 2017 23:43:05 GMT  
		Size: 900.6 KB (900598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16cf98e3d7ab167b663f3d76743d84537d8d0d1b7726ca1dc90c1c66d61f93`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7294826e2fb9e19c7814832b2413f506d42029239123b21060c70c98d6680e9e`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 127.2 KB (127205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc40f9bb83064f019be73d49157c39dc4eb16f56a7c63f200205bb83c1f3ab12`  
		Last Modified: Wed, 12 Jul 2017 16:33:15 GMT  
		Size: 103.8 MB (103813521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:2757b636135d04b84f64b87cca20e5e9a3b5fdbd9edbba2daedbf8013526b920
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189266841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c7deae78ecf4c42eb0a7c088cf133e794a1acbe59ffbb5851fba304c24ee18`
-	Default Command: `["node","main.js"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Jul 2017 22:11:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 08 Jul 2017 04:20:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 08 Jul 2017 04:23:56 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Sat, 08 Jul 2017 04:23:57 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 11 Jul 2017 23:27:37 GMT
ENV NODE_VERSION=4.8.4
# Tue, 11 Jul 2017 23:27:49 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 11 Jul 2017 23:27:50 GMT
ENV YARN_VERSION=0.24.4
# Tue, 11 Jul 2017 23:27:53 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 11 Jul 2017 23:27:54 GMT
CMD ["node"]
# Wed, 12 Jul 2017 16:31:50 GMT
MAINTAINER buildmaster@rocket.chat
# Wed, 12 Jul 2017 16:31:51 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat.rocketchat /app/uploads
# Wed, 12 Jul 2017 16:31:51 GMT
VOLUME [/app/uploads]
# Wed, 12 Jul 2017 16:31:53 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Wed, 12 Jul 2017 16:31:53 GMT
ENV RC_VERSION=0.57.1
# Wed, 12 Jul 2017 16:31:54 GMT
WORKDIR /app
# Wed, 12 Jul 2017 16:32:39 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Wed, 12 Jul 2017 16:32:41 GMT
USER [rocketchat]
# Wed, 12 Jul 2017 16:32:41 GMT
WORKDIR /app/bundle
# Wed, 12 Jul 2017 16:32:42 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Wed, 12 Jul 2017 16:32:43 GMT
EXPOSE 3000/tcp
# Wed, 12 Jul 2017 16:32:43 GMT
CMD ["node" "main.js"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405c8e05a47440060907f35b13c15d3346452f19cf1db17c659568eb3391e90`  
		Last Modified: Mon, 10 Jul 2017 18:16:29 GMT  
		Size: 4.4 KB (4374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eeeb57a2cd360c68be9ca1a01878bf2be388153a1874b87c2dd1a19a0ae79d`  
		Last Modified: Mon, 10 Jul 2017 18:16:26 GMT  
		Size: 119.2 KB (119157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fdfa03cee406af9161ee7783cfd9d9e09c6495280dba0f99032350d0e7d9aa`  
		Last Modified: Tue, 11 Jul 2017 23:43:12 GMT  
		Size: 12.4 MB (12420659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35934788e1f4f8661ea49c2b728356a69498ec68f4ded86f3ef3ae7779c9fa1`  
		Last Modified: Tue, 11 Jul 2017 23:43:05 GMT  
		Size: 900.6 KB (900598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16cf98e3d7ab167b663f3d76743d84537d8d0d1b7726ca1dc90c1c66d61f93`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 2.2 KB (2151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7294826e2fb9e19c7814832b2413f506d42029239123b21060c70c98d6680e9e`  
		Last Modified: Wed, 12 Jul 2017 16:32:55 GMT  
		Size: 127.2 KB (127205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc40f9bb83064f019be73d49157c39dc4eb16f56a7c63f200205bb83c1f3ab12`  
		Last Modified: Wed, 12 Jul 2017 16:33:15 GMT  
		Size: 103.8 MB (103813521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
