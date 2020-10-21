# Setup a local Git server using Docker

0. Install a local linux environment (e.g. ubuntu server 20.04) through virtual machine (VirtualBox or Hyper-V Manager)
1. Install Docker based on the instructions from docker.com (https://docs.docker.com/install/).
2. Get latest version of gitlab community edition from Docker Hub.
docker image pull gitlab/gitlab-ce
3. Following the instructions from https://docs.gitlab.com/omnibus/docker/ to setup the gitlab server locally. 
docker run --detach --hostname localhost --publish 443:443 --publish 80:80 --publish 22:22 --name gitlab-ce --restart always --volume /home/user/vic/gitlab-cc/config:/etc/gitlab --volume /home/user/vic/gitlab-cc/logs:/var/log/gitlab --volume /home/user/vic/gitlab-cc/data:/var/opt/gitlab gitlab/gitlab-ce
4. Go to https://localhost/