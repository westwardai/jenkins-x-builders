FROM gcr.io/jenkinsxio/builder-base:0.0.14

RUN rpm -Uvh https://packages.microsoft.com/config/rhel/7/packages-microsoft-prod.rpm \
    && yum update \
    && yum -y install dotnet-sdk-2.1 \
    && yum clean all

# jx
ENV JX_VERSION 1.3.1011
RUN curl -f -L https://github.com/jenkins-x/jx/releases/download/v${JX_VERSION}/jx-linux-amd64.tar.gz | tar xzv && \
  mv jx /usr/bin/
