


Use the Redoc Docker image







[* ← Back to Docs](/docs)[* Redoc Community Edition](/docs/redoc)[* Quickstart](/docs/redoc/deployment/html)[* Configuration](/docs/redoc/config)[* Deployment guides](/docs/redoc/deployment/intro)

[+ HTML element](/docs/redoc/deployment/html)[+ React component](/docs/redoc/deployment/react)[+ Docker image](/docs/redoc/deployment/docker)[+ Redocly CLI](/docs/redoc/deployment/cli)[* Vendor extensions](/docs/redoc/redoc-vendor-extensions)Last updated  1 year ago

How to use the Redoc Docker image
=================================

Redoc is available as a pre-built Docker image in [Docker Hub](https://hub.docker.com/r/redocly/redoc/).

If you have [Docker](https://docs.docker.com/get-docker/) installed, pull the image with the following command:

```
docker pull redocly/redoc
```

Then run the image with the following command:

```
docker run -p 8080:80 redocly/redoc
```

The preview starts on port 8080, based on the port used in the command, and can be accessed at `http://localhost:8080`. To exit the preview, use `control+C`.

By default Redoc starts with a demo Swagger Petstore OpenAPI definition located at http://petstore.swagger.io/v2/swagger.json. You can update this URL using the environment variable `SPEC_URL`.

For example:

```
docker run -p 8080:80 -e SPEC_URL=https://api.example.com/openapi.json redocly/redoc
```

Create a Dockerfile
-------------------

You can also create a Dockerfile with some predefined environment variables. Check out a sample [Dockerfile](https://github.com/Redocly/redoc/blob/main/config/docker/Dockerfile) in our code repo.

#### Was this helpful?

 Next pageOn this page[Create a Dockerfile](#create-a-dockerfile)


