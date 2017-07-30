page_main_title: Google Container Engine
main_section: Platform
sub_section: Integrations
page_title: GKE integration

# Google Container Engine Integration

Available under the Integration Family: **deploy**

`Google Container Engine` Integration is used to connect Shippable DevOps Assembly Lines platform to Google Container Engine that runs Kubernetes behind the scenes so that you can deploy Docker based applications

You can create this from the integrations page. This is the information you would require to create this integration

* **Name** -- friendly name for the integration
* **JSON Key** -- JSON Security Key for Google Cloud

## Resources that use this Integration
Resources are the bulding blocks of assembly lines and some types of resource refer to Integrations by their name. The following Resources Types can created with `Google Container Engine` Integration 

* [image]()
* [cluster]()
* [integration]()
* [provision]()

## Default Environment Variables
When you create a Resource with this integration, and use it as an `IN` or `OUT` into a Job that can execute user defined scripts, a set of environment variables are configured by the platform that may be useful to set the context before user defined scripts execute as part of the Job. These are variables available when this Resource is used

`<NAME>` is the the friendly name of the Resource

| Environment variable						| Description      |
| ------			 							|----------------- |
| `<NAME>`\_INTEGRATION\_JSON_KEY			| Access Key supplied in the integration |

## Further Reading
* GKE integration
* AWS integration
* runSH job
* runCLI job
* runCI job
* How to setup CI for my git repo

## TODO
| Tasks   |      Status    |
|----------|-------------|
| Hotlinking |  Open |
| Further Reading needs thinking|  Open |