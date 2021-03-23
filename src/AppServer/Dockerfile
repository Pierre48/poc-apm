FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app

FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /src
COPY ["src/AppServer/AppServer.csproj", "src/AppServer/"]
RUN dotnet restore "src/AppServer/AppServer.csproj"
COPY . .
WORKDIR "/src/src/AppServer"
RUN dotnet build "AppServer.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "AppServer.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "AppServer.dll"]
