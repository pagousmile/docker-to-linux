FROM amd64/debian:bullseye
LABEL com.iximiuz-project="docker-to-linux"
RUN apt-get -y update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
  systemd gnome-shell gdm3 sudo
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
  linux-image-amd64
RUN echo "root:root" | chpasswd
RUN useradd -m -U -G sudo -s /bin/bash user
RUN echo "user:user" | chpasswd
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends \
  gnome-terminal network-manager \
  gnome-control-center locales
RUN rm /etc/apt/apt.conf.d/docker-*
