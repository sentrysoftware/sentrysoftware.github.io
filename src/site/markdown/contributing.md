keywords: contributor
description: MetricsHub established some rules to make sure your contributions are valued properly.
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

# Contributing

You have found a bug or you have an idea for a cool new feature? Contributing code is a great way to give something back to
the open source community. Before you dig right into the code there are a few guidelines that we need contributors to
follow so that we can have a chance of keeping on top of things.

<!-- MACRO{toc|fromDepth=1|toDepth=2|id=toc} -->

## Getting started

* Make sure you have a [GitHub account](https://github.com/join).
* Find the corresponding [repository on GitHub](repos.html).
* Submit a **GitHub issue** in the repository to request a change, **assuming one does not already exist**.
  * Clearly describe the issue including steps to reproduce when it is a bug.
  * Include screenshots and outputs whenever relevant.
  * If known, explain what should be changed to fix the problem.
  * If possible, specify how to test the new feature.
* [Fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) and check out your forked repository.

## Making changes

* Ensure your fork of the repository is up-to-date (use [GitHub's fork sync feature](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork), and pull to your local clone of the repository).
* Create a _topic branch_ for your isolated work, named `feature/short-description` (the name is prefixed with `feature/` even if your change fixes a bug).
  * Usually you should base your branch on the `main` branch.
  * A good topic branch name can be the GitHub issue id (#_nnn_) plus a short description, e.g. `feature/issue-53-fix-https-certificate`.
  * If you have submitted multiple JIRA issues, try to maintain separate branches and pull requests.
  * Check our [branching model](branching.html) for more details.
* Make commits of logical units.
  * Make sure your commit messages are meaningful and in the proper format. Your commit message should contain the key of the GitHub issue.
  * Example: `Issue #53: Changed the implementation of the keystore`
* Respect the original code style:
  * Only use tabs for indentation.
  * Create minimal diffs -- disable _On Save_ actions like _Reformat Source Code_ or _Organize Imports_. If you feel the source code should be reformatted or refactored somehow, create a separate PR for this change first. **Smaller changes are more likely to get approved by reviewers!**
* Make sure you have added the necessary tests for your changes, typically in `src/test/java`.
* Run all the tests with `mvn clean verify` to ensure nothing else was accidentally broken.
* Build the project site with `mvn site` and verify the configured code quality reports (in the **Project Reports** section).

### Making trivial changes

Cosmetic or trivial changes in a project, like indentation, white spaces, typos, or minor refactoring **don't require** creating a dedicated GitHub issue, but they must not be mixed with other significant changes: a separate commit and separate Pull Request must be submitted.

In this case, the _topic branch_ should be named `trivial/short-description`.

## Submitting changes

* Push your changes to a topic branch in your fork of the repository.
* Submit a _Pull Request_ (PR) to the corresponding repository in the `metricshub` organization.
  * Verify _Files Changed_ shows only your intended changes and does not include additional files or changes like white spaces, etc.
  * Make sure all automatic checks are successful.
  * Verify comments produced automatically by code quality automatic checks.
* When implementing additional changes after reviewers suggestions, simply commit and push such changes. **Never squash or rebase commits that you have already pushed!**
* Once your PR is merged (if approved), [sync your forked repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork), pull these changes to your locally cloned repository and delete your branch.

**By submitting a PR to one of MetricsHub's repositories, you accept the terms of the [MetricsHub Contributor License Agreement (CLA)](cla.md).**

## Builds

To facilitate external contributions, automatic builds don't happen on MetricsHub's internal Jenkins server, but directly in GitHub with [GitHub Actions](https://docs.github.com/en/actions/quickstart).

Whenever possible, MetricsHub open-source projects must use shared workflows from the [sentrysoftware/workflows](https://github.com/sentrysoftware/workflows) repository to build, deploy artifacts, and release new versions.

## Java libraries

MetricsHub's open-source Java library projects are published on Maven Central. We will enforce several requirements to ensure the quality of our libraries:

* The project must publish its _Maven Site_ (`mvn site`) with full reports as GitHub Pages:
  * [Checkstyle](https://checkstyle.org/)
  * [CPD](https://docs.pmd-code.org/latest/pmd_userdocs_cpd.html)
  * [PMD](https://pmd.github.io/)
  * [SpotBugs](https://spotbugs.github.io/)
  * Unit tests
  * Javadoc
* Maven's artifact _groupId_ must be `org.metricshub`
* License must be [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0) and all source files must include a header with the Apache-2.0 notice. We use `mvn license:update-file-header` to update the source file headers.
* Publish the Javadoc and Source artifacts along with the main artifact

Pull Requests will trigger the [maven-build.yml](https://github.com/sentrysoftware/workflows/blob/main/.github/workflows/maven-build.yml) GitHub Action workflow to make sure the project builds.

SNAPSHOT artifacts will be deployed automatically to the [Maven Central Snapshot repository](https://s01.oss.sonatype.org/content/repositories/snapshots/) on changes on the `main` branch with the [maven-central-deploy.yml](https://github.com/sentrysoftware/workflows/blob/main/.github/workflows/maven-central-deploy.yml) GitHub Action workflow.

Releases are performed with the [maven-central-release.yml](https://github.com/sentrysoftware/workflows/blob/main/.github/workflows/maven-central-release.yml) GitHub Action workflow, which deploys the artifacts in a [staging repository on Maven Central](https://s01.oss.sonatype.org/content/groups/staging). The staging repository must be **released** manually once validated by the testing team, which makes the artifact available on Maven Central for good. Login to [https://s01.oss.sonatype.org/](https://s01.oss.sonatype.org/) to release the staging repository.

Happy coding! 😊

## Additional resources

* [Git Branching Model](branching.html)
* [Maven Project Repository Template](https://github.com/sentrysoftware/oss-maven-template)
* [General GitHub documentation](https://help.github.com/)
* [GitHub pull request documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
