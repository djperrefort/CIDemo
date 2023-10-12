# CI Demo For Microservices Application

This repository is used to demonstrate CI design using GitHub actions for a microservices application.

# How it Works

The CI in this repository supports the following workflow:

1. Developers checkout a new branch where they work on a well-defined issue (e.g. implementing a specific feature). 
   As commits are made to the feature branch and pushed to GitHub, the CI will automatically identify and run tests for all microservices that have a test suite.
2. Once ready, the feature branch is merged into the `main` branch.
   New documentation is automatically published to GitHub pages under the version `develop`
3. Developers can preview a running instance of their code by manually dispatching the `DevelopmentDeploy` workflow.
   Once they are finished, they can manually run the `DevelopmentTeardown` workflow to stop the running development instance.
4. The above process repeats until the team agrees to push a new version to production.
   A team member tags a release on GitHub and the CI automatically performs the following steps:
   - Runs the application test suites (just in case)
   - Publishes the microservices
   - Publishes a new copy of the documentation under the version number specified in the release

This is my edit
