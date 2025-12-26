# Security Policy

## Supported Versions

We provide security updates for the following versions of WeasyprintTool:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| < Latest| :x:                |

We recommend always using the latest version of WeasyprintTool to ensure you have the most recent security patches and improvements.

## Reporting a Vulnerability

If you discover a security vulnerability in WeasyprintTool, please report it by following these steps:

1. **Do NOT** open a public issue on GitHub
2. Report the vulnerability privately through [GitHub Security Advisories][security-url]
3. Provide a detailed description of the vulnerability including:
   - Steps to reproduce the issue
   - Potential impact of the vulnerability
   - Suggested fix (if available)

We take all security reports seriously and will respond as quickly as possible to address the issue.

## Security Update Process

When a security vulnerability is reported:

1. We will acknowledge receipt of your report within 48 hours
2. We will investigate and validate the vulnerability
3. We will develop and test a fix
4. We will release a new version with the security fix
5. We will publicly disclose the vulnerability after the fix is available

## Dependencies

WeasyprintTool wraps the [Weasyprint][weasyprint-url] document factory. Security vulnerabilities in Weasyprint should be reported to the Weasyprint project directly:

- [Weasyprint Security Information][weasyprint-security-url]

We monitor Weasyprint releases and update WeasyprintTool when security fixes are available.

## Best Practices

When using WeasyprintTool:

- Always use the latest version
- Review the release notes for security updates
- Use [.NET tool manifests][tool-manifest-url] to manage versions in your projects
- Monitor [GitHub Security Advisories][security-url] for this repository

[security-url]: https://github.com/demaconsulting/WeasyprintTool/security/advisories
[weasyprint-url]: https://weasyprint.org/
[weasyprint-security-url]: https://github.com/Kozea/WeasyPrint/security
[tool-manifest-url]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
