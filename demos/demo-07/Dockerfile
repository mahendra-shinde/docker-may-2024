# Download the base image Window Server Core
FROM mcr.microsoft.com/windows/servercore:ltsc2022

## Install IIS Server using Powershell command 'Install-WindowsFeature'
RUN powershell -command Install-WindowsFeature -Name Web-Server

## Download the Service Monitor for Launching IIS inside a container
ADD "https://dotnetbinaries.blob.core.windows.net/servicemonitor/2.0.1.10/ServiceMonitor.exe" "C:\ServiceMonitor.exe" 

WORKDIR /inetpub/wwwroot

COPY index.html .
COPY main.css .

ENTRYPOINT ["C:\\ServiceMonitor.exe", "w3svc"]