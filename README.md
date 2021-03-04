# Tidelift and GitLab Pipelines Integration

Tidelift can integrate with GitLab through [GitLab Pipelines](https://docs.gitlab.com/ee/ci/pipelines/).

This example will complete a basic `tidelift alignment save`, causing Tidelift to check the project's manifest against the correct Tidelift Catalog. If alignment is below 100%, the CLI will return status `0`, and the build will fail.

This is meant to be an example to build upon.

# Instructions

Assumptions: the Git project already has a `.tidelift` file with correct `TIDELIFT_ORGANIZATION` and `TIDELIFT_PROJECT` variables set. See the Tidelift [documentation](https://docs.tidelift.com/article/92-dot-tidelift-files) for more on `.tidelift` files.

Add the `.gitlab-ci.yml` configuration in this repository to your project repository. It will trigger GitLab Pipelines to run the Tidelift CLI inside a container. The only configuration you'll need to complete is to add a Protected Variable for `$TIDELIFT_API_KEY_PROTECTED_VARIABLE`. The value of this variable should be a Tidelift API key, as described [here](https://docs.tidelift.com/article/27-tracking-repositories-and-creating-api-keys).
