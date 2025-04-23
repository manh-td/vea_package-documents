


Use the Redoc CLI







[* ← Back to Docs](/docs)[* Redoc Community Edition](/docs/redoc)[* Quickstart](/docs/redoc/deployment/html)[* Configuration](/docs/redoc/config)[* Deployment guides](/docs/redoc/deployment/intro)

[+ HTML element](/docs/redoc/deployment/html)[+ React component](/docs/redoc/deployment/react)[+ Docker image](/docs/redoc/deployment/docker)[+ Redocly CLI](/docs/redoc/deployment/cli)[* Vendor extensions](/docs/redoc/redoc-vendor-extensions)Last updated  5 days ago

How to use the Redocly CLI
==========================

With Redocly CLI, you can bundle your OpenAPI definition and API documentation (made with Redoc) into an HTML file and render it locally.

Step 1 - Install Redocly CLI
----------------------------

First, you need to install the `@redocly/cli` package.

You can install it [globally](/docs/cli/installation#install-globally) using npm or Yarn.

Or you can install it during [runtime](/docs/cli/installation#use-npx-at-runtime) using npx or Docker.

Step 2 - Build the HTML file
----------------------------

The Redocly CLI `build-docs` command builds Redoc into an HTML file.

To build an HTML file using Redocly CLI, enter the following command, replacing `apis/openapi.yaml` with your API definition file's name and path:

```
redocly build-docs apis/openapi.yaml
```

See the [build-docs](/docs/cli/commands/build-docs) documentation for more information on the different options and ways you can use the command.

Also, check out [Redocly CLI commands](/docs/cli/commands), for more information on the different things you can do with Redocly CLI including linting, splitting, and bundling your API definition file.

#### Was this helpful?

 Next pageOn this page[Step 1 - Install Redocly CLI](#step-1---install-redocly-cli)[Step 2 - Build the HTML file](#step-2---build-the-html-file)


