keywords: gitflow, github, git
description: MetricsHub uses a simplified branching model for its open-source projects.
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

## Branching Model

Branching model here is **simplified** and doesn't follow [*Gitflow*](https://nvie.com/posts/a-successful-git-branching-model/):

* 1 `main` branch.
* `feature/short-description` branches for new features and bug fixes, or `trivial/short-description` for trivial changes, like indentation, white spaces, etc.
* `release/vX.Y.Z` branches for releases (this is done automatically by the [release workflow](https://github.com/sentrysoftware/workflows/tree/main?tab=readme-ov-file#maven-central-release)).
* No `hotfix` or `bugfix` branches.
* `vX.Y.Z` tags for each release (this is done automatically by the [release workflow](https://github.com/sentrysoftware/workflows/tree/main?tab=readme-ov-file#maven-central-release)).
* Pull Requests (PR):
  * The PR requests to merge your branch in your repository into the `main` branch of the `metricshub.github.io` repository.
  * 1 code review is required to merge the PR.
  * PRs are "merged", **not** squashed, and **not** rebased.
  * No sign-off is required (for now).
