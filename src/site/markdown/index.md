keywords: metricshub,maven,gsf,asf,lf,cncf
description: Home for open-source projects from Sentry Software, including MetricsHub.
<!--
  ╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲
  Open Sentry Web Site
  ჻჻჻჻჻჻
  Copyright 2023 - 2024 Sentry Software
  ჻჻჻჻჻჻
  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
  ╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱
  -->
# Open Source Home

This is the home for [Sentry Software](https://sentrysoftware.com)'s open-source projects, all hosted [on GitHub](https://github.com/sentrysoftware): the directory of [repositories](repos.html), [how to contribute](contributing.html), etc.

<!-- MACRO{toc|fromDepth=1|toDepth=2|id=toc} -->

## Notable Internal Projects

### MetricsHub

The most significant open-source project that Sentry Software is working on is [MetricsHub](https://metricshub.com). MetricsHub is a universal metrics collection agent for OpenTelemetry. This solution is designed to be extensible, and we hope to build a community around it so that all users can benefit from the extensions made by others.

![Diagram showing MetricsHub, a universal metrics collection agent for OpenTelemetry — our first open-source project.](images/metricshub-diagram.png)

This is the first time we are publishing an entire software solution in open source. The main challenge has been to migrate a significant part of internal libraries from closed source to open source: [various protocol clients](#java-libraries), Maven [plugins](#sentry-maven-skin), etc. Ensuring that the entire project can build on GitHub or anyone's system took us a considerable amount of time, but we're proud of the result!

The MetricsHub project consists of three main repositories:

* [MetricsHub Community Connectors](https://github.com/sentrysoftware/metricshub-community-connectors), where anyone can easily contribute with new connectors to collect metrics from anywhere!
* [MetricsHub](https://github.com/sentrysoftware/metricshub), the main OpenTelemetry collection agent.
* [MetricsHub Connector Maven Plugin](https://github.com/sentrysoftware/metricshub-connector-maven-plugin), the Maven plugin to build the documentation for the Community Connectors project.

### Sentry Maven Skin

The [Sentry Maven Skin](https://sentrysoftware.github.io/sentry-maven-skin) is a skin used when building a [documentation site with Maven](https://maven.apache.org/plugins/maven-site-plugin/examples/creating-content.html). This skin provides a stylish design, an excellent Lighthouse score, and features not available in other Maven skins. This site is, in fact, built with Maven and the Sentry Maven Skin!

![Screenshot of an example Maven project using the Sentry Maven Skin to build its site.](images/sentry-maven-skin.png)

The initial internal versions of this skin did not fulfill all the requirements of standard Maven skins (like customizing the logo, links, etc.). Open-sourcing this project forced us to comply with all requirements so that anyone could use this (very nice) skin to build the site of their Maven project.

### Java Libraries

While working on open-sourcing [MetricsHub](https://metricshub.com), we first had to publish a collection of Java libraries to handle various instrumentation protocols and operations, notably:

* [ipmi](https://github.com/sentrysoftware/ipmi), a Java library to connect to IPMI (forked from [Verax Systems](https://veraxsystems.com/ipmi-library-for-java/)).
* [winrm](https://github.com/sentrysoftware/winrm), a Java library to execute commands or WMI queries on a remote Windows system through WinRM.
* [wbem](https://github.com/sentrysoftware/wbem), a Java library to perform WBEM operations.
* [wmi](https://github.com/sentrysoftware/wmi), a Java library to execute commands or WMI queries on a remote Windows system, through WMI (on Windows only).

## Sentry Contributions to Other Projects

Before open-sourcing our own products, we contributed to third-party open-source projects that we were relying on (and we keep contributing!):

* [OpenTelemetry Semantic Conventions](https://github.com/open-telemetry/semantic-conventions), where we defined semantic conventions for hardware metrics ([see documentation](https://opentelemetry.io/docs/specs/semconv/system/hardware-metrics/)).
* [OpenTelemetry Collector Contrib](https://github.com/open-telemetry/opentelemetry-collector-contrib), where we added proper Otel-to-Prometheus conversion for metrics and attributes. Our code even ended up in [Prometheus](https://github.com/prometheus/prometheus) itself!
* [Apache Maven Doxia](https://github.com/sentrysoftware/maven-doxia) and [Apache Maven Site Plugin](https://github.com/apache/maven-site-plugin), where we improved the rendering of Markdown documents.

A special project we've contributed to is [Jawk](https://sentrysoftware.github.io/Jawk/), a Java implementation of the famous [AWK](https://en.wikipedia.org/wiki/AWK) parsing utility. We've forked the original project, and we now maintain our own version, much lighter and faster. We will try to be as compatible as possible with [GNU AWK (gawk)](https://www.gnu.org/software/gawk/).

## Why Open Source

For 20+ years, [Sentry Software](https://sentrysoftware.com) has been developing proprietary software for a proprietary ecosystem. A few years ago, however, we started collaborating with open-source projects that our own products relied on:

* Raising issues we encountered;
* Documenting existing features;
* Fixing bugs;
* Adding features we needed.

And then we realized that if we wanted to fully collaborate with important open-source projects, like [OpenTelemetry](https://opentelemetry.io/), or with the [Green Software Foundation](https://greensoftware.foundation/), we needed to go open source ourselves!

The benefits of open-source software are multiple for end-users as well, as it guarantees our customers that our software products remain open, secure, and will even last long after us!

## Contributing to Sentry Repositories

Please carefully follow some [basic rules we've established](contributing.html) to ensure you don't waste your time while trying to help!

## Licenses

Our open-source projects are released under various licenses, depending on the project's requirements, how it's supposed to be used, and its history. Please refer to the [licenses page](licenses.html) for more details. Check each [repository documentation site](repos.html) for specific information about each repository.

## Acknowledgments

Thank you to the [Apache Software Foundation](https://apache.org/) for leading the way into open source. They truly inspired us!

Thank you to the [Cloud-Native Software Foundation](https://www.cncf.io/) for incubating and nurturing the [OpenTelemetry project](https://www.cncf.io/projects/opentelemetry/).

Thank you to the [Linux Foundation](https://www.linuxfoundation.org/) for hosting the [Green Software Foundation](https://greensoftware.foundation/). Sentry Software is a member of both the [Linux Foundation](https://www.linuxfoundation.org/about/members) and the [Green Software Foundation](https://greensoftware.foundation/team).
