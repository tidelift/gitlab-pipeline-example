# Tidelift and GitLab Pipelines Integration

Tidelift can integrate with GitLab through [Pipelines](https://docs.gitlab.com/ee/ci/pipelines/) and [Code Quality](https://docs.gitlab.com/ee/ci/testing/code_quality.html).

This example will complete a basic `tidelift alignment save`, causing Tidelift to check the project's manifest for issues such as vulnerabilites or deprecation.
It then generates a Code Quality report that can be viewed in the GitLab UI to see newly introduced issues.

This is meant to be an example to build upon.

# Instructions

## Assumptions

* This example is for a Python-based project. You may need to tweak the `image:` yaml value in the configuration based upon your project.

## Quick start
Add the `.gitlab-ci.yml` configuration in this repository to your project repository and examine it, especially the comments.

The configuration will trigger GitLab Pipelines to run the Tidelift CLI inside a container during CI. The only configuration you'll need to complete is to add a Protected Variable for `$TIDELIFT_API_KEY_PROTECTED_VARIABLE`. The value of this variable should be a Tidelift API key, as described [here](https://support.tidelift.com/hc/en-us/articles/4406286623380-API-authentication-and-keys).
