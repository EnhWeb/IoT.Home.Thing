# IoT.Home.Thing

#### IoT Home Intelligence with Raspberry Pi

### Home of Things based on Raspberry Pi, Linux, Swagger, Docker & .NET Core.

## Introduction

After building IoT embryos at [IoT.Starter.Pi.Thing](https://github.com/josemotta/IoT.Starter.Pi.Thing) series, we are now ready to climb one more step towards IoT Home Intelligence. The development strategy and environment are based on the following tools:  

- **Raspberry Pi with Linux**: Raspbian GNU/Linux 9.1 Lite is installed at RPI host and [debian:stretch-slim](https://github.com/dotnet/dotnet-docker/blob/master/2.1/runtime/stretch-slim/arm32v7/Dockerfile) equip docker images based on [.NET Core 2.1 Preview 1](https://blogs.msdn.microsoft.com/dotnet/2018/02/27/announcing-net-core-2-1-preview-1/).
- **Swagger**: the API First Design strategy is used to develop an ASP.NET Core Web Server automatically generated by SwaggerHub. The [Thing specification](https://github.com/josemotta/IoT.Starter.Pi.Thing/wiki/2.-IoT.Starter.Pi.Thing#1-specs) exhibits the minimal requirements for `Thing` embryos used at Home Intelligence applications. After each change on the API, SwaggerHub automatically generates updated code to build the `home-srv` docker image that is finally pushed to DockerHub.
- **Docker**: A multi-stage docker image build is accomplished at a speedy Windows x64 machine, generating code of linux-arm framework. The images are pushed to the cloud and then pulled back into the Raspberry Pi with Linux.
- **Lirc**: The Linux Infrared Remote Control for Raspberry Pi is installed at `home-srv`, extending the `Thing` web service to support IR remotes and their respective codes.
- **Raspberry# IO**: [Raspberry# IO](https://github.com/raspberry-sharp/raspberry-sharp-io) is a .NET/Mono IO Library for Raspberry Pi, an initiative of the Raspberry# Community. It was updated to [.Net Standard](https://github.com/Ramon-Balaguer/raspberry-sharp-io) by Ramon Balaguer. I just updated it one more time, to [.NET Core 2.1 Preview 1](https://blogs.msdn.microsoft.com/dotnet/2018/02/27/announcing-net-core-2-1-preview-1/), as you can check at [home/src](https://github.com/josemotta/IoT.Home.Thing/tree/master/home/src).



*Did you like? Please :star: me!*