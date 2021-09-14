FROM mcr.microsoft.com/dotnet/core/sdk:3.1 as build

WORKDIR /cloud

COPY src/cartservice.csproj .

RUN dotnet restore

COPY src/ .

RUN dotnet publish -c Release -o /out /cartservice.csproj

FROM mcr.microsoft.com/dotnet/core/runtime:3.1 

WORKDIR /cloud

COPY --from=build /out .

CMD ["dotnet", "cartservice.dll"]