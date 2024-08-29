ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
CMD ["bash"]
/bin/sh -c set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
/bin/sh -c set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
/bin/sh -c apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
/bin/sh -c set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
COPY multi:be7bd55eef9abcbdac65ce36ba8b1f780cbefd83348cc99144474f53050ee1a2 in /usr/bin/ 
ARG DEBIAN_FRONTEND=noninteractive
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c yes | unminimize     && install-packages         zip         unzip         bash-completion         build-essential         ninja-build         htop         jq         less         locales         man-db         nano         ripgrep         software-properties-common         sudo         time         emacs-nox         vim         multitail         lsof         ssl-cert         fish         zsh     && locale-gen en_US.UTF-8
ENV LANG=en_US.UTF-8
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c upgrade-packages
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c add-apt-repository -y ppa:git-core/ppa     && install-packages git git-lfs
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c useradd -l -u 33333 -G sudo -md /home/gitpod -s /bin/bash -p gitpod gitpod     && sed -i.bkp -e 's/%sudo\s\+ALL=(ALL\(:ALL\)\?)\s\+ALL/%sudo ALL=NOPASSWD:ALL/g' /etc/sudoers
ENV HOME=/home/gitpod
WORKDIR /home/gitpod
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c { echo && echo "PS1='\[\033[01;32m\]\u\[\033[00m\] \[\033[01;34m\]\w\[\033[00m\]\$(__git_ps1 \" (%s)\") $ '" ; } >> .bashrc
USER [gitpod]
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c sudo echo "Running 'sudo' for Gitpod: success" &&     mkdir -p /home/gitpod/.bashrc.d &&     (echo; echo "for i in \$(ls -A \$HOME/.bashrc.d/); do source \$HOME/.bashrc.d/\$i; done"; echo) >> /home/gitpod/.bashrc
|1 DEBIAN_FRONTEND=noninteractive /bin/sh -c sudo git lfs install --system
USER root
RUN /bin/sh -c apt-get update # buildkit
RUN /bin/sh -c apt-get install -y strace # buildkit
USER gitpod
