FROM mcr.microsoft.com/dotnet/sdk:6.0-jammy as BASE

WORKDIR /app

COPY . .

RUN ["dotnet", "restore"]
RUN ["dotnet", "build", "-o", "dist"]

FROM  mcr.microsoft.com/dotnet/aspnet:6.0-jammy
WORKDIR /app
COPY --from=BASE /app/dist/ .
EXPOSE 80
ENTRYPOINT [ "dotnet", "app1.dll" ]