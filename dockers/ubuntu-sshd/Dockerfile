# This docker file packages a bunch of useful system services
# to make local testing and developing more seamless.

FROM ubuntu:15.04

RUN apt-get update && apt-get install -y openssh-server sudo python vim
RUN mkdir /var/run/sshd
RUN echo 'root:test' | chpasswd
RUN sed -i 's/PermitRootLogin without-password/PermitRootLogin yes/' /etc/ssh/sshd_config
# RUN sed -i 's/#AuthorizedKeysFile/AuthorizedKeysFile/' /etc/ssh/sshd_config

RUN mkdir /root/.ssh
ADD id_rsa.pub /root/.ssh/authorized_keys
RUN chmod 755 /root/.ssh/authorized_keys

# SSH login fix. Otherwise user is kicked off after login
RUN sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd

ENV NOTVISIBLE "in users profile"
RUN echo "export VISIBLE=now" >> /etc/profile

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]

