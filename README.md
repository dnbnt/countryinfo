# Country Info
Country data library implemented in various languages:

| Path   | Language   | Type  | Output  | Output Name | Description
|--|--|--|--|--|--|
| [DNB.CountryInfo](https://github.com/dnbnt/countryinfo/blob/main/src/dotnet/DBN.CountryInfo/README.md)  | .NET  | Class Library  | nuget package  | DNB.CountryInfo.nupkg | .NET library that contains country data and flags |
| [DNB.CountryInfo.Service](https://github.com/dnbnt/countryinfo/blob/main/src/dotnet/DBN.CountryInfo.Service/README.md)  | .NET  | Web API  | docker image  | dnbnt/countryinfo:1.0-net | Dockerized REST service that provides country data and flags |
| [DNB.CountryInfo.Angular](https://github.com/dnbnt/countryinfo/blob/main/src/dotnet/DBN.CountryInfo.Angular/README.md)  | .NET  | Angular  | docker image  | dnbnt/countryinfo:1.0-net-angular | Dockerized Angular web application to show country data and flag images |
| [DNB.CountryInfo.React](https://github.com/dnbnt/countryinfo/blob/main/src/dotnet/DBN.CountryInfo.React/README.md)  | .NET  | React  | docker image  | dnbnt/countryinfo:1.0-net-react | Dockerized React web application to show country data and flag images |
| [server](https://github.com/dnbnt/countryinfo/blob/main/src/nodejs/server/README.md) | Node.js  | REST API  | docker image  | dnbnt/countryinfo:1.0-nodejs | Dockerized REST service that provides country data and flags |
| [server](https://github.com/dnbnt/countryinfo/blob/main/src/go/server/README.md) | Go  | REST API  | docker image  | dnbnt/countryinfo:1.0-go | Dockerized REST service that provides country data and flags |

DBN.CountryInfo is available as Nuget package here: [https://www.nuget.org/packages/DBN.CountryInfo](https://www.nuget.org/packages/DBN.CountryInfo)

## Build
The project contains a `Makefile` which uses `docker` to download country data, flag images files and build all projects in a container.
```
make all
```

### Makefile
The `Makefile` supports the following parameters:
| Name  | Description |
|--|--|
| `help` | Show help (default) |
| `all` | Build everything (`init`, `build`) |
| `init` | Download countries resource files from [https://restcountries.com/v3/all](https://restcountries.com/v3/all) and copy `countries.json` and flag image files to project directories |
| `build` | Build all projects |
| `dotnet-lib` | Build .NET class library |
| `dotnet-service` | Build .NET rest webapi docker image |
| `dotnet-angular` | Build .NET Angular docker image |
| `dotnet-react` | Build .NET React docker image |
| `nodejs-service` | Build Node.js rest webservice docker image |
| `go-service` | Build Go rest webservice docker image |
| `test` | Test all projects |

## License
The MIT License (MIT) see [License file](https://github.com/dnbnt/countryinfo/blob/main/LICENSE)