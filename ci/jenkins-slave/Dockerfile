FROM alpine:3.3

RUN apk --no-cache add bash openssh

# Add user jenkins to the image
RUN adduser -S jenkins
# Set password for the jenkins user (you may want to alter this).
RUN echo "jenkins:jenkins" | chpasswd

# Create host key for sshd. Require to start sshd
RUN /usr/bin/ssh-keygen -A

# Standard SSH port
EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]