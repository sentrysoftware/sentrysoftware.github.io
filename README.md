# [metricshub.org](https://metricshub.org) Web Site

![Build](https://img.shields.io/github/actions/workflow/status/MetricsHub/metricshub.github.io/deploy.yml)
![GitHub top language](https://img.shields.io/badge/language-Markdown-blue)
![License](https://img.shields.io/github/license/MetricsHub/metricshub.github.io)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://metricshub.org/code-of-conduct.html)

Source repository for the Web site hosted at [metricshub.org](https://metricshub.org).

## Build instructions

This is a simple Maven documentation project. Build with:

```bash
mvn site
```

## Deploy instructions

Anything merged in the `main` branch is automatically deployed in GitHub Pages.

## License

License is MIT. Each source file must include the MIT header (build will fail otherwise).
To update source files with the proper header, simply execute the below command:

```bash
mvn license:update-file-header
```
