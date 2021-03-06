## `vault:latest`

```console
$ docker pull vault@sha256:4c71b6e03293cbc976c070ad0fb8533b48b253c0667c0eabde2a002ae6f45f98
```

-	Platforms:
	-	linux; amd64

### `vault:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17960498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ce90cea20a8e4565eeea80d02b6a8e34ce85b84e9158ebc7e56f31828e23dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Thu, 29 Jun 2017 00:37:25 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Thu, 29 Jun 2017 00:38:58 GMT
ENV VAULT_VERSION=0.7.3
# Thu, 29 Jun 2017 00:38:59 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Thu, 29 Jun 2017 00:39:01 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 29 Jun 2017 00:39:11 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 29 Jun 2017 00:39:12 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 29 Jun 2017 00:39:13 GMT
VOLUME [/vault/logs]
# Thu, 29 Jun 2017 00:39:14 GMT
VOLUME [/vault/file]
# Thu, 29 Jun 2017 00:39:15 GMT
EXPOSE 8200/tcp
# Thu, 29 Jun 2017 00:39:17 GMT
COPY file:98bcd0ef55bd9ba781f5f486eef8d94bca7953eea74d785ef2b77818ebda7972 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 29 Jun 2017 00:39:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jun 2017 00:39:19 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9926af1e09d1d370190587595052b97607c1ce30045af63fc2ff6f6418fe1e8f`  
		Last Modified: Fri, 30 Jun 2017 19:05:59 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449ea5b2c4ebac9539712d5c5a610a18ce22acb9601155c2084755cdf9903e99`  
		Last Modified: Fri, 30 Jun 2017 19:06:03 GMT  
		Size: 16.0 MB (15966927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc231cac3d8326ccc23fa9e4afbb55e48b1865cdcac7d9141151f2a649cfeed`  
		Last Modified: Fri, 30 Jun 2017 19:05:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baedace0936190039336683a5e50fcbd49f2207deca5dfb80297c0a3511bb7e`  
		Last Modified: Fri, 30 Jun 2017 19:05:59 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
