FROM microsoft/dotnet:1.1.1-sdk

WORKDIR /code

ADD src/worker /code/src/worker

RUN dotnet restore -v minimal src/worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

CMD dotnet src/worker/worker.dll
