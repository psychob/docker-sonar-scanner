FROM debian:9
MAINTAINER Andrzej Budzanowski <kontakt@andrzej.budzanowski.pl>

RUN apt-get update                                                                                                      && \
    apt-get install -y wget zip                                                                                         && \
    wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-3.3.0.1492-linux.zip            \
         -O /sonar.zip --progress=dot:giga                                                                              && \
    unzip /sonar.zip "sonar-scanner-3.3.0.1492-linux/*" -d /sonar/                                                      && \
    mv /sonar/sonar-scanner-3.3.0.1492-linux/* /sonar/                                                                  && \
    rm -rf /sonar/sonar-scanner-3.3.0.1492-linux/                                                                       && \
    apt-get clean

