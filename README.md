# Dynamic Endpoint Routing Platform
## DERP
`derp` is a platform for quickly provisioning serverless endpoints as a service for use within a centralized application. The `derp` platform handles everything from website registry, serverless function code management, and endpoint routing integration.

### Pre-requisites
- If using AWS: AWS CLI installed on your OS with access to your AWS environment

### Installation
- CentOS: `yum install derp`

### Usage
Use the derp CLI to automate your local `derp` environment, including pipelines and environments for testing, release, etc.
Calling `derp` in your terminal will read your `.derp` configuration file and deploy your envronment.
If the `.derp` configuration file is not detected, a wizard will guide your through defining the file prior to deployment. This step will use `derp` to push the `.derp` configuration file to your `derp`.
```
$ derp
```
Once your environment has been deployed, you can create a new endpoint using the CLI:
```
$ derp new getUsers --http:get
```
This will create a new folder in your local environment called `getUsers` with a NodeJS stub for your endpoint as well as a `.derp` file for the endpoint.
```
$ cd getUsers && ls
$ .derp node_modules index.js package.json
```
That command also created a new endpoint within your remote `derp` application that you can view within the `derp` console. You can perform configuration on the endpoints in the `derp` console, the `derp` CLI, or the `.derp` file itself.
Upon modifying the `index.js` file for the `getUsers` endpoint, you can test it locally and/or deploy it to your `derp` application using the CLI:
```
$ derp debug
$ Application available at http://localhost:8080 including 2 endpoints.
$ derp deploy getUsers
$ getUsers endpoint has been deployed to your application at http://example.com/getUsers
```
