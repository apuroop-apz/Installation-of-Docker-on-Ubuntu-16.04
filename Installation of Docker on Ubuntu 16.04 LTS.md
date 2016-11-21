# Installation of Docker on Ubuntu 16.04 LTS

Docker provides a way to run applications securely isolated in a container, packaged with all its dependencies and libraries. Because your application can always be run with the environment it expects right in the build image, testing and deployment is simpler than ever, as your build will be fully portable and ready to run as designed in any environment.

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/docker_logo-1455828502290.png?raw=true)

# Prerequisites:

Docker is supported on these Ubuntu operating systems:

Ubuntu Xenial 16.04 (LTS)

Ubuntu Wily 15.10

Ubuntu Trusty 14.04 (LTS)

Ubuntu Precise 12.04 (LTS)

---

Docker requires a 64-bit installation regardless of your Ubuntu version. Additionally, your kernel must be 3.10 at minimum. The latest 3.10 minor version or a newer maintained version are also acceptable.

Kernels older than 3.10 lack some of the features required to run Docker containers. These older versions have known bugs which cause data loss and frequently panic under certain conditions.

---

#Step 1

To check your current kernel version,

Open the terminal from the Dash

Type:

_uname -r _

This will display your kernel version.

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/1.png?raw=true)

---

#Step 2

## Updating the APT sources

Log into your machine as a user with _**sudo**_ or _**root**_ privileges.

Open a terminal window.

Type:

_sudo apt-get update_

_sudo apt-get install apt-transport-https ca-certificates_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/2.png?raw=true)

Adding a GPG key.

In the terminal,

Type:

_sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/3.png?raw=true)

In the terminal,

Type:

_cd /etc/apt/sources.list.d/_

_sudo apt-get install vim_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/4.png?raw=true)

In the terminal,

Type:

_sudo vim docker.list_

_deb https://apt.dockerproject.org/repo ubuntu-xenial main_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/5.png?raw=true)

---

In the terminal,

Type:

_sudo apt-get update_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/6.png?raw=true)

In the terminal,

Type:

_apt-cache policy docker-engine_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/7.png?raw=true)

---

In the terminal,

Type:

_sudo apt-get update_

_$ sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/8.png?raw=true)

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/9.png?raw=true)

In the terminal,

Type:

_sudo apt-get install docker-engine_

_docker --version_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/10.png?raw=true)

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/11.png?raw=true)

---

In the terminal,

Type:

_sudo groupadd docker_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/12.png?raw=true)

In the terminal,

Type:

_sudo usermod -aG docker $USER_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/13.png?raw=true)

**LOG OFF from the system and LOG back IN.**

---

In the terminal,

Type:

_docker --version_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/15.png?raw=true)

In the terminal,

Type:

_docker run hello-world_

![](https://github.com/apuroop-apz/docker-install/blob/master/figures/16.png?raw=true)

---