![GitHub forks](https://img.shields.io/github/forks/demaconsulting/WeasyprintTool?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/demaconsulting/WeasyprintTool?style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/demaconsulting/WeasyprintTool?style=plastic)
![GitHub](https://img.shields.io/github/license/demaconsulting/WeasyprintTool?style=plastic)

# About

WeasyprintTool is a repackaging of the [Weasyprint](https://weasyprint.org/) document factory as a [Dotnet tool](https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools).

Weasyprint is already available in numerous formats for [installation](https://doc.courtbouillon.org/weasyprint/stable/first_steps.html#installation).
Packaging it as a Dotnet tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[Dotnet tool manifest file](https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool).


# Installation & Usage

The following will add WeasyprintTool to a Dotnet tool manifest file:

```
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.WeasyprintTool
```

The tool can then be executed by:

```
dotnet weasyprint <arguments>
```