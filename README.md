# Tidelift and GitLab Pipelines Integration

Tidelift can integrate with GitLab through [GitLab Pipelines](https://docs.gitlab.com/ee/ci/pipelines/).

This example will complete a basic `tidelift alignment save`, causing Tidelift to check the project's manifest against the correct Tidelift Catalog. If alignment is below 100%, the CLI will return status `0`, and the build will fail.

This is meant to be an example to build upon.
