![GitHub forks][forks-badge]
![GitHub Repo stars][stars-badge]
![GitHub contributors][contributors-badge]
![GitHub][license-badge]
[![NuGet][nuget-badge]][nuget-url]

# About

WeasyprintTool is a repackaging of the [Weasyprint][weasyprint-url] document factory as a [.NET tool][dotnet-tools-url].

Weasyprint is already available in numerous formats for [installation][weasyprint-install-url].
Packaging it as a .NET tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[.NET tool manifest file][dotnet-manifest-url].

# Installation & Usage

The following will add WeasyprintTool to a .NET tool manifest file:

```bash
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.WeasyprintTool
```

The tool can then be executed by:

```bash
dotnet weasyprint <arguments>
```

# Contributing

We welcome contributions! Please see our [Contributing Guide][contributing-url] for details.

# Code of Conduct

This project has adopted a Code of Conduct. Please see [CODE_OF_CONDUCT.md][code-of-conduct-url] for details.

# Security

For information on reporting security vulnerabilities, please see our [Security Policy][security-url].

# License

This project is licensed under the BSD-3-Clause License - see the [LICENSE][license-url] file for details.

[forks-badge]: https://img.shields.io/github/forks/demaconsulting/WeasyprintTool?style=plastic
[stars-badge]: https://img.shields.io/github/stars/demaconsulting/WeasyprintTool?style=plastic
[contributors-badge]: https://img.shields.io/github/contributors/demaconsulting/WeasyprintTool?style=plastic
[license-badge]: https://img.shields.io/github/license/demaconsulting/WeasyprintTool?style=plastic
[nuget-badge]: https://img.shields.io/nuget/v/DEMAConsulting.WeasyprintTool?style=plastic&logo=nuget
[nuget-url]: https://www.nuget.org/packages/DEMAConsulting.WeasyprintTool/
[weasyprint-url]: https://weasyprint.org/
[weasyprint-install-url]: https://doc.courtbouillon.org/weasyprint/stable/first_steps.html#installation
[dotnet-tools-url]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[dotnet-manifest-url]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool
[contributing-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/CONTRIBUTING.md
[code-of-conduct-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/CODE_OF_CONDUCT.md
[security-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/SECURITY.md
[license-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/LICENSE
