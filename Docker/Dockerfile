FROM ubuntu
WORKDIR /home/jenkins
# jenkins port
EXPOSE 8080
RUN apt update -y && apt install -y openjdk-17-jdk wget gnupg2
RUN wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | apt-key add - \
    && sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' \
    && apt update -y && apt install -y jenkins
CMD ["jenkins", "foreground"]
