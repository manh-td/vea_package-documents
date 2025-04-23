


Use the Redoc React component







[* ← Back to Docs](/docs)[* Redoc Community Edition](/docs/redoc)[* Quickstart](/docs/redoc/deployment/html)[* Configuration](/docs/redoc/config)[* Deployment guides](/docs/redoc/deployment/intro)

[+ HTML element](/docs/redoc/deployment/html)[+ React component](/docs/redoc/deployment/react)[+ Docker image](/docs/redoc/deployment/docker)[+ Redocly CLI](/docs/redoc/deployment/cli)[* Vendor extensions](/docs/redoc/redoc-vendor-extensions)Last updated  3 months ago

How to use the Redoc React component
====================================

Before you start
----------------

Install the following dependencies required by Redoc if you do not already have them installed:

* `react`
* `react-dom`
* `mobx`
* `styled-components`
* `core-js`

If you have npm installed, you can install these dependencies using the following command:

```
npm i react react-dom mobx styled-components core-js
```

Step 1 - Import the `RedocStandalone` component
-----------------------------------------------

```
import { RedocStandalone } from 'redoc';
```

Step 2 - Use the component
--------------------------

You can either link to your OpenAPI definition with a URL, using the following format:

```
<RedocStandalone specUrl="url/to/your/spec"/>
```

Or you can pass your OpenAPI definition as an object, using the following format:

```
<RedocStandalone spec={/* spec as an object */}/>
```

Optional - Pass options
-----------------------

Options can be passed into the RedocStandalone component to alter how it renders.

For example:

```
<RedocStandalone
  specUrl="http://petstore.swagger.io/v2/swagger.json"
  options={{
    nativeScrollbars: true,
    theme: { colors: { primary: { main: '#dd5522' } } },
  }}
/>
```

For more information on configuration options, refer to the [Configuration options for Reference docs](https://redocly.com/docs/api-reference-docs/configuration/functionality/) section of the documentation. Options available for Redoc are noted, "Supported in Redoc CE".

Optional - Specify `onLoaded` callback
--------------------------------------

You can also specify the `onLoaded` callback, which is called each time Redoc is fully rendered or when an error occurs (with an error as the first argument).

```
<RedocStandalone
  specUrl="http://petstore.swagger.io/v2/swagger.json"
  onLoaded={(error) => {
    if (!error) {
      console.log('Yay!');
    }
  }}
/>
```
#### Was this helpful?

 Next pageOn this page[Before you start](#before-you-start)[Step 1 - Import the RedocStandalone component](#step-1---import-the-redocstandalone-component)[Step 2 - Use the component](#step-2---use-the-component)[Optional - Pass options](#optional---pass-options)[Optional - Specify onLoaded callback](#optional---specify-onloaded-callback)


