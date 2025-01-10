
FROM mcr.microsoft.com/dotnet/sdk:8.0

WORKDIR /App

COPY . ./
RUN dotnet restore 

RUN dotnet publish -c Release -o out

WORKDIR /App/out

ENTRYPOINT ["dotnet", "App.dll"]

EXPOSE 8080 

ENV ASPNETCORE_URLS=http://+:8080