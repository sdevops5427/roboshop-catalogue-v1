FROM      redhat/ubi9
COPY      mongo.repo /etc/yum.repos.d/mongo.repo
RUN       dnf install mongodb-mongosh -y
COPY      master-data.js run.sh /
ENTRYPOINT  ["bash", "/run.sh"]