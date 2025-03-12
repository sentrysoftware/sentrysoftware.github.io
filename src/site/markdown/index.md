keywords: metricshub,maven,gsf,asf,lf,cncf
description: Home for open-source projects from MetricsHub, including MetricsHub.
<!--
  ╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲╱╲
  Open MetricsHub Web Site
  ჻჻჻჻჻჻
  Copyright 2025 MetricsHub
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

This is the home for [MetricsHub](https://metricshub.com)'s open-source projects, all hosted [on GitHub](https://github.com/metricshub): the directory of [repositories](repos.html), [how to contribute](contributing.html), etc.

<!-- MACRO{toc|fromDepth=1|toDepth=2|id=toc} -->

## Notable Internal Projects

### MetricsHub

![inline](images/metricshub-logo-only.png)

The most significant open-source project that [MetricsHub](https://metricshub.com) is working on is a universal metrics collection agent for OpenTelemetry. This solution is designed to be extensible, and we hope to build a community around it so that all users can benefit from the extensions made by others.

This is the first time we are publishing an entire software solution in open source. The main challenge has been to migrate a significant part of internal libraries from closed source to open source: [various protocol clients](#java-libraries), Maven [plugins](#sentry-maven-skin), etc. Ensuring that the entire project can build on GitHub or anyone's system took us a considerable amount of time, but we're proud of the result!

The MetricsHub project consists of three main repositories:

* [MetricsHub Community Connectors](https://github.com/metricshub/metricshub-community-connectors), where anyone can easily contribute with new connectors to collect metrics from anywhere!
* [MetricsHub](https://github.com/metricshub/metricshub), the main OpenTelemetry collection agent.
* [MetricsHub Connector Maven Plugin](https://github.com/metricshub/metricshub-connector-maven-plugin), the Maven plugin to build the documentation for the Community Connectors project.

### Java Libraries

While working on open-sourcing [MetricsHub](https://metricshub.com), we first had to publish a collection of Java libraries to handle various instrumentation protocols and operations, notably:

* [ipmi](https://github.com/sentrysoftware/ipmi), a Java library to connect to IPMI (forked from [Verax Systems](https://veraxsystems.com/ipmi-library-for-java/)).
* [winrm](https://github.com/sentrysoftware/winrm), a Java library to execute commands or WMI queries on a remote Windows system through WinRM.
* [wbem](https://github.com/sentrysoftware/wbem), a Java library to perform WBEM operations.
* [wmi](https://github.com/sentrysoftware/wmi), a Java library to execute commands or WMI queries on a remote Windows system, through WMI (on Windows only).

## Why Open Source

For 20+ years, [Sentry Software](https://sentrysoftware.com) has been developing proprietary software for a proprietary ecosystem. A few years ago, however, we started collaborating with open-source projects that our own products relied on:

* Raising issues we encountered;
* Documenting existing features;
* Fixing bugs;
* Adding features we needed.

And then we realized that if we wanted to fully collaborate with important open-source projects, like [OpenTelemetry](https://opentelemetry.io/), or with the [Green Software Foundation](https://greensoftware.foundation/), we needed to go open source ourselves!

The benefits of open-source software are multiple for end-users as well, as it guarantees our customers that our software products remain open, secure, and will even last long after us!

## Contributing to MetricsHub Repositories

Please carefully follow some [basic rules we've established](code-of-conduct.html) to ensure a healthy collaboration between different people, and refer to the [contributor's guide](contributing.html) to ensure you don't waste your time while trying to help!

## Licenses

Our open-source projects are released under various licenses, depending on the project's requirements, how it's supposed to be used, and its history. Please refer to the [licenses page](licenses.html) for more details. Check each [repository documentation site](repos.html) for specific information about each repository.

## Acknowledgments

Thank you to the [Apache Software Foundation](https://apache.org/) for leading the way into open source. They truly inspired us!

Thank you to the [Cloud-Native Software Foundation](https://www.cncf.io/) for incubating and nurturing the [OpenTelemetry project](https://www.cncf.io/projects/opentelemetry/).

Thank you to the [Linux Foundation](https://www.linuxfoundation.org/) for hosting the [Green Software Foundation](https://greensoftware.foundation/). Sentry Software is a member of both the [Linux Foundation](https://www.linuxfoundation.org/about/members) and the [Green Software Foundation](https://greensoftware.foundation/team).
