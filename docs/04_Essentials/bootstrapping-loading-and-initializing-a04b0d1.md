<!-- loioa04b0d10fb494d1cb722b9e341b584ba -->

# Bootstrapping: Loading and Initializing

To use OpenUI5 features in your HTML page, you have to load and initialize the SAPUI5 library.

You can use the OpenUI5 bootstrap script in your page to initialize OpenUI5 runtime automatically as soon as the script is loaded and executed by the browser. For simple use cases as well as the default OpenUI5 installation, this is sufficient to build and run UIs.

> ### Note:  
> If you run your app standalone, the bootstrap is added to your HTML page. In an SAP Fiori launchpad environment, the launchpad executes the bootstrap and no additional HTML page is needed to display the app.

The following code snippet shows a typical bootstrap script tag:

```html
<script id="sap-ui-bootstrap"
     src="resources/sap-ui-core.js"
     data-sap-ui-async="true"
     data-sap-ui-on-init="..."
     data-sap-ui-compat-version="edge"
     data-sap-ui-resource-roots='{ "my.app": "./" }'>
</script>
```

In addition to the above snippet, you can specify a set of OpenUI5 libraries with `data-sap-ui-libs="sap.m, sap.ui.layout, sap.ui.unified, ..."` if there is no manifest.json to declare dependent libraries. More options that can be configured with `data-` can be found in [Configuration Options and URL Parameters](configuration-options-and-url-parameters-91f2d03.md).

***

<a name="loioa04b0d10fb494d1cb722b9e341b584ba__section_sct_d5h_4bc"/>

## `Core.ready` State

After bootstrapping, if `sap-ui-on-init` has not been configured already, you can use the `sap/ui/core/Core` singleton to either `await` the Core's `ready` state or provide a callback function:

```js
sap.ui.require(["sap/ui/core/Core"], async (Core) => {
    // Either usage of Core.ready() as a Promise
    await Core.ready();
    // ...

    // Or usage of a callback function
    Core.ready(() => {
        // ...
    });
});
```

> ### Note:  
> The module export of `sap/ui/core/Core` is **not** a class, but the singleton `Core` instance itself.
> 
> The `sap.ui.core.Core` class must not be instantiated, except by the framework itself.

***

<a name="loioa04b0d10fb494d1cb722b9e341b584ba__section_OBBU"/>

## Overview of Bootstrap Base URLs

OpenUI5 provides several bootstrap URLs for different use cases. The following table gives an overview of the most important bootstrap base URLs:


<table>
<tr>
<th valign="top">

Resource

</th>
<th valign="top">

Description

</th>
<th valign="top">

Usage

</th>
</tr>
<tr>
<td valign="top">

UI5 Tooling

</td>
<td valign="top">

You can access the libraries hosted by UI5 Tooling under `resources/sap-ui-core.js`<sup>1</sup>.

</td>
<td valign="top">

Development

</td>
</tr>
<tr>
<td valign="top">

Content Delivery Network \(CDN\)

</td>
<td valign="top">

You can access the libraries externally from a CDN, which can be either an SAP-hosted CDN or a custom-hosted CDN.

For more information, see [Variant for Bootstrapping from Content Delivery Network](variant-for-bootstrapping-from-content-delivery-network-2d3eb2f.md).

</td>
<td valign="top">

Development/productive applications

</td>
</tr>
<tr>
<td valign="top">

Cache Buster for OpenUI5 

</td>
<td valign="top">

You can access the libraries consuming the cache buster for OpenUI5 under `resources/sap-ui-cachebuster/sap-ui-core.js`<sup>1</sup>.

For more information, see [Cache Buster for OpenUI5](cache-buster-for-openui5-91f0809.md).

</td>
<td valign="top">

Productive applications with available cache buster deployed

</td>
</tr>
</table>

1\) The sample mentions `sap-ui-core.js` as a bootstrap file. An overview of more bootstrap files is given in [Overview of Bootstrap Files](bootstrapping-loading-and-initializing-a04b0d1.md#loioa04b0d10fb494d1cb722b9e341b584ba__section_OBF).

***

<a name="loioa04b0d10fb494d1cb722b9e341b584ba__section_OBF"/>

## Overview of Bootstrap Files

OpenUI5 provides several bootstrap files for different use cases. The following table gives an overview of the most important resources and the respective use cases. The resource names refer to the `resources/` folder in the OpenUI5 installation. You can find possible base URLs in [Overview of Bootstrap Base URLs](bootstrapping-loading-and-initializing-a04b0d1.md#loioa04b0d10fb494d1cb722b9e341b584ba__section_OBBU).


<table>
<tr>
<th valign="top">

Resource

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`sap-ui-core.js`

</td>
<td valign="top">

This is the standard bootstrap file, which we recommend to use for typical use cases. It already contains jQuery, `jquery-ui-position` and only the minimum required parts of the core library \(`sap.ui.core`\). Required files are loaded dynamically using XMLHttpRequest \(XHR\).

For more information, see [Standard Variant for Bootstrapping](standard-variant-for-bootstrapping-91f1f45.md).

</td>
</tr>
<tr>
<td valign="top">

`sap-ui-core-nojQuery.js`

</td>
<td valign="top">

You use this bootstrap file for applications with their own jQuery version. It also contains the minimum required parts of the core library, but **not** jQuery and `jquery-ui-position`.

For more information, see [noJQuery Variant for Bootstrapping](nojquery-variant-for-bootstrapping-91f1dd0.md).

</td>
</tr>
<tr>
<td valign="top">

`sap/ui/core/library-preload.js`

</td>
<td valign="top">

This file contains most of the modules that are contained in the `sap.ui.core` library, but the modules are parsed and executed only on demand, and not immediately.

> ### Caution:  
> An application must not reference this file. If the configuration option is set to `preload`, OpenUI5 automatically loads the file.

For more information, see [Standard Variant for Bootstrapping](standard-variant-for-bootstrapping-91f1f45.md).

</td>
</tr>
<tr>
<td valign="top">

`sap-ui-custom*.js`

</td>
<td valign="top">

File names that match this pattern are reserved for custom merged files used by the application.

> ### Note:  
> The proposed naming scheme for these files needs to be adapted in future versions for the same encapsulation reasons as mentioned above.



</td>
</tr>
</table>

-   **[Standard Variant for Bootstrapping](standard-variant-for-bootstrapping-91f1f45.md "The standard variant for bootstrapping loads all JavaScript modules of a library in
		advance with one single request for performance reasons.")**  
The standard variant for bootstrapping loads all JavaScript modules of a library in advance with one single request for performance reasons.
-   **[Variant for Bootstrapping from Content Delivery Network](variant-for-bootstrapping-from-content-delivery-network-2d3eb2f.md "OpenUI5 can either be
            loaded locally with a relative path from a Web server or externally from a Content
            Delivery Network (CDN).
    ")**  
OpenUI5 can either be loaded locally with a relative path from a Web server or externally from a Content Delivery Network \(CDN\). 
-   **[noJQuery Variant for Bootstrapping](nojquery-variant-for-bootstrapping-91f1dd0.md "The noJQuery variant supports bootstrapping for an application that already
        integrates jQuery or uses a different jQuery version than OpenUI5.")**  
The noJQuery variant supports bootstrapping for an application that already integrates jQuery or uses a different jQuery version than OpenUI5.
-   **[Initialization Process](initialization-process-91f2c90.md#loio91f2c9076f4d1014b6dd926db0e91070 "The initialization process starts after OpenUI5 runtime is
		loaded.")**  
The initialization process starts after OpenUI5 runtime is loaded.
-   **[Deprecated Core API](deprecated-core-api-798dd9a.md "This page describes important aspects of the deprecation of the sap.ui.core.Core API facade, as most of its
                methods have been deprecated. It shows a migration path away from the deprecated legacy APIs and towards their future-proof
                alternatives.")**  
This page describes important aspects of the deprecation of the `sap.ui.core.Core` API facade, as most of its methods have been deprecated. It shows a migration path away from the deprecated legacy APIs and towards their future-proof alternatives.
-   **[Configuration of the OpenUI5 Runtime](configuration-of-the-openui5-runtime-91f08de.md "OpenUI5 provides several options for the configuration of the OpenUI5 runtime. The possible ways to provide input for the available
		configuration options are described in detail.")**  
OpenUI5 provides several options for the configuration of the OpenUI5 runtime. The possible ways to provide input for the available configuration options are described in detail.

