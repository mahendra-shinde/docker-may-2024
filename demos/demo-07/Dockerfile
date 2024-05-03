# Download the base image Window Server Core
FROM mcr.microsoft.com/windows/servercore:ltsc2022

RUN powershell -command Install-WindowsFeature -Name Web-Server; Invoke-WebRequest -UseBasicParsing -Uri https://dotnetbinaries.blob.core.windows.net/servicemonitor/2.0.1.10/ServiceMonitor.exe -OutFile C:\ServiceMonitor.exe

WORKDIR /inetpub/wwwroot

COPY index.html .
COPY main.css .

ENTRYPOINT ["C:\\ServiceMonitor.exe", "w3svc"]