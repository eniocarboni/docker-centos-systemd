# Centos 8 Docker Image with systemd

[![Build](https://github.com/eniocarboni/docker-centos-systemd/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/eniocarboni/docker-centos-systemd/actions/workflows/build.yml) [![GPL License](https://img.shields.io/badge/license-GPL-blue.svg)](https://www.gnu.org/licenses/) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/EnioCarboni)

Centos 8 Docker container with systemd, useful for tests with `ansible` especially with `molecule`

## Tags

  - `centos8`, `latest` on main branch
  - `centos7` on centos7 branch


## How to Build

  * Verify if [Docker is installed](https://docs.docker.com/install/).
  * Run on main branch: `docker build -t docker-centos-systemd:centos8 -t docker-centos-systemd:latest .`
  * Run on 18.04 branch: `docker build -t docker-centos-systemd:centos7 .`
  * Verify image: `docker images`

## How to Use

  * `docker pull eniocarboni/docker-centos-systemd:latest` (or use the image you built earlier).
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro eniocarboni/docker-centos-systemd:latest`

View the run container with

  * `docker ps`

Enter in the container with:

  * `docker exec -it <container_id> bash`

Kill container with:

  * `docker kill <container_id>`

Remove container with:

  * `docker image rm -f <container_id>` 

## Author

Created in 2022 by Enio Carboni

## License

GNU GENERAL PUBLIC LICENSE (see [LICENSE](LICENSE) file)
