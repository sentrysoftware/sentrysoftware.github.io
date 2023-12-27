# [sentrysoftware.org](https://sentrysoftware.org) Web Site

![GitHub release (with filter)](https://img.shields.io/github/v/release/sentrysoftware/sentrysoftware.github.io)
![Build](https://img.shields.io/github/actions/workflow/status/sentrysoftware/sentrysoftware.github.io/deploy.yml)
![GitHub top language](https://img.shields.io/github/languages/top/sentrysoftware/oss-maven-template)
![License](https://img.shields.io/github/license/sentrysoftware/sentrysoftware.github.io)

Source repository for the Web site hosted at [sentrysoftware.org](https://sentrysoftware.org).

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
