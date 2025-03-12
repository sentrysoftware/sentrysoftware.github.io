keywords: license,apache,mit,bsd,agpl,gpl,lgpl,cla,contributor
description: Depending on the type and use of a MetricsHub open-source project, a different license will be used.
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

# Licenses

This page summarizes how MetricsHub open-source projects are licensed.

## Project types

| Project Type | Description | License | Examples |
| --- | --- | --- | --- |
| Java Library | A simple Java library that can be consumed by our other open-source projects, or even by external projects.<br/><br/>Artifacts are published on Maven Central. | [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0) | <ul><li>Jawk</li><li>WinRM Java library</li><li>Maven plugins</li></ul> |
| Non-Java Library | A non-Java project, with low licensing requirements | [MIT](https://opensource.org/license/mit/) | <ul><li>Reusable GitHub Actions</li></ul> |
| Product | A usable product (Java or non-Java).<br/><br/>Installable packages are published as part of a GitHub Release. | [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html) | <ul><li>MetricsHub</li></ul> |
| Web Site | Source to generate a public Web site | [MIT](https://opensource.org/license/mit/) | <ul><li>[metricshub.org](http://metricshub.org)</li></ul> |

## Contributor License Agreement

Some open-source projects at MetricsHub are used in commercial products. For example, the MetricsHub Agent (and its engine) is used in MetricsHub Enterprise. To allow MetricsHub to use open-source code in its commercial offering, all contributors are required to accept a specific [Contributor License Agreement](cla.md).
