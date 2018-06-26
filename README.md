# Dynamic Endpoint Routing Platform
## DERP
`derp` is a platform for quickly provisioning an entire developer, testing, and production environment in the cloud. `derp` can provision DevOps pipelines, container orchestration solutions, load balancer, and auto-scaling groups with a single cli command.

### Pre-requisites
- If using AWS: AWS CLI installed on your OS with access to your AWS environment
- Git installed on your OS and configured for your code

### Installation
- CentOS: `yum install derp`

### Usage
Use the derp CLI to automate your entire environment, including pipelines and managed container orchestration environments for test/release.
Calling `derp` in your terminal will read your `.derp` configuration file and deploy your envronment.
If the `.derp` configuration file is not detected, a wizard will guide your through defining the file prior to deployment. This step will use git to push the `.derp` configuration file to your remote repo.
```
$ derp
```
