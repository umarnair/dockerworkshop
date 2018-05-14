FROM ubuntu:17.10
ARG PASSWORD
ENV PASSWORD=$PASSWORD
RUN apt-get update
RUN apt-get -y install wget
RUN wget https://packages.microsoft.com/config/ubuntu/17.10/packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN apt-get -y install apt-transport-https
RUN apt-get update
RUN apt-get -y install dotnet-runtime-2.0.5
RUN apt-get -y install dotnet-sdk-2.1.200
RUN apt-get update
RUN apt-get -y install git
RUN git clone https://umarnair:$PASSWORD@github.com/sequoiaat/UmaStudies.git
WORKDIR /UmaStudies/helloworldwebapp
RUN dotnet restore
RUN dotnet run