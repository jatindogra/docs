page_main_title: Security and permissions features of the Shippable platform
main_section: Platform
sub_section: Security
page_title: Security Overview

# Security & Permissions

The Shippable CI/CD and DevOps platform is built keeping in mind that any security lapses are unforgivable and damaging to all organizations. This includes our own organization, since our customers trust us with their intellectual property.

Please read our blog on [Security best practices at Shippable](http://blog.shippable.com/security-best-practices-shippable-ci-cd-devops) for an overview of how we handle security at Shippable.

The sections below talk about security and permissions feature built into the product to ensure that your automation scripts are secure and you can grant the right level of access to every team member.

## Separation of secrets from automation scripts

Most CI/CD providers offer a way for you to encrypt your secrets so that you're not forced to include passwords, token, and other sensitive information in plain text your automation scripts. At Shippable as well, we support secure environment variables which are encrypted key:value pairs you can use in your configuration.

However, we believe that encrypted strings are problematic due to the unwieldiness of managing a completely meaningless sequence of characters. For example:

```
env:
  global:
    # UGLY secure variables....
    - secure: YtSX204QeZ4hJ89DCrH/3W+XjbGCBfkhWPwJumHCBMVGkmpF4XWwbLqG65IZtQlRMNRlwI3vsTksDhXnK3ng2nsUUBPyzxbcVI7AJMgd2tIGjGzxqcCLemel+sA+ES/2TBFyy5+mlE2/RqohUWw/xRj45nHQqEIC0xwDmQcQvFObaMjLgceI01uv7AxdLVDpOVMO2i7g7Bxwvfru3EtUVZB+siTAUn28WbCesgSFhNIZa56z+4CpYRfTQP6lfrIWlhtcsHPlb6T0rqXO3gRkaFIBgMLj5Ab/eIeHoOfcdJ/YjsV4NjCYqH/9QgMNMj46EEfcsK2IiFCyFu6X/HwCTw==

```

To improve the experience around handling secrets, we have introduced the concept of **Integrations**, which allow users to store their sensitive information with a friendly name that can be used to configure CI or Assembly Line workflows. These Integrations are encrypted at rest and in flight, and are stored in our Vault.

This means you will never again accidentally disclose keys, passwords or other sensitive information, while still retaining the ability to identify who added an integration and which third-party provider it connects to. It is also easy to manage the underlying values in one place without needing to go update all your scripts.

For more on the advantages of using Integrations, [read our docs here](/platform/integration/overview).

## User permissions

We support the following levels of permissions for your Assembly Lines and jobs:

* Ability to view a job or Assembly Line
* Ability to take an action , e.g. run a job or pin a version of a resource
* No ability to view or take an action

You can configure these permissions through your source control provider and the Shippable platform will respect them.

For more information, read our document on [Managing permissions with RBAC](/platform/security/ci-cd-permissions).