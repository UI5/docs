<!-- loiobe0cf40f61184b358b5faedaec98b2da -->

# Manifest \(Descriptor for Applications, Components, and Libraries\)

The manifest \(also known as descriptor for applications, components, and libraries, in short: app descriptor\) is inspired by the WebApplication Manifest concept introduced by the W3C. The manifest provides a central, machine-readable, and easy-to-access location for storing metadata associated with an application, an application component, or a library.

In general, the manifest describes the behavior of an app through attributes. When a section in the manifest does affect the behavior of an app, this is described in the [API Reference](https://ui5.sap.com/#/api/). for the corresponding namespace.

The data of the manifest is stored in JSON format in the `manifest.json` file. The developer creates the file with attributes in different namespaces. It contains, for example, the app ID, the version, the data sources used, along with the required components and libraries. The existence of the `manifest.json` file must be declared in the component metadata, which is then delivered as part of the application archive. After delivery, the file is read-only.

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_mkz_dgh_1cb"/>

## Manifest Schema

The manifest schema defines how you need to maintain the content of the manifest. It also specifies which namespaces and fields are available. The full schema is available as open source in a [repository on Github](https://github.com/UI5/manifest).

When the manifest schema changes, a new version is published alongside the release of the new OpenUI5 version. This new OpenUI5 version understands the updated schema and supports new features. The schema version you use is defined by the value of `_version`. The version number follows the pattern described under [Versioning and Maintenance of SAPUI5](https://ui5.sap.com/1.136.1/#/topic/91f021426f4d1014b6dd926db0e91070). In general, a new version with the same major version number is compatible with the previous one. It offers new features or marks certain features as deprecated, which you should migrate. A new major version can remove features that were previously deprecated, and these must be migrated.

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_manifest2"/>

## Manifest Version 2

Starting with OpenUI5 1.136, the new major version 2.x.x Using this new version ensures you follow best practices and are prepared for the future. As mentioned earlier, this new major version removes deprecated features. Check the [Migration Information for Upgrading the Manifest File](https://github.wdf.sap.corp/uics-innersource/ui5-docs/blob/main/docs/04_Essentials/migration-information-for-upgrading-the-manifest-file-a110f76.md) to learn about the changes needed to migrate to this version.

***

The table below shows the relationship between recent OpenUI5 versions and the manifest schema versions.

**Manifest Schema Version and OpenUI5 Version**


<table>
<tr>
<th valign="top">

\_Version

</th>
<th valign="top">

OpenUI5 Version

</th>
</tr>
<tr>
<td valign="top">

1.4.0

</td>
<td valign="top">

\>=1.38

</td>
</tr>
<tr>
<td valign="top">

1.17.0

</td>
<td valign="top">

\>=1.71

</td>
</tr>
<tr>
<td valign="top">

1.28.0

</td>
<td valign="top">

\>=1.84

</td>
</tr>
<tr>
<td valign="top">

1.37.0

</td>
<td valign="top">

\>=1.96

</td>
</tr>
<tr>
<td valign="top">

1.48.0

</td>
<td valign="top">

\>=1.108

</td>
</tr>
<tr>
<td valign="top">

1.51.0

</td>
<td valign="top">

\>=1.111

</td>
</tr>
<tr>
<td valign="top">

1.60.0

</td>
<td valign="top">

\>=1.120

</td>
</tr>
<tr>
<td valign="top">

1.61.0

</td>
<td valign="top">

\>=1.121

</td>
</tr>
<tr>
<td valign="top">

1.62.0

</td>
<td valign="top">

\>=1.122

</td>
</tr>
<tr>
<td valign="top">

1.63.0

</td>
<td valign="top">

\>=1.123

</td>
</tr>
<tr>
<td valign="top">

1.64.0

</td>
<td valign="top">

\>=1.124

</td>
</tr>
<tr>
<td valign="top">

1.65.0

</td>
<td valign="top">

\>=1.126

</td>
</tr>
<tr>
<td valign="top">

1.66.0

</td>
<td valign="top">

\>=1.129

</td>
</tr>
<tr>
<td valign="top">

1.67.2

</td>
<td valign="top">

\>=1.130

</td>
</tr>
<tr>
<td valign="top">

1.68.0

</td>
<td valign="top">

\>=1.131

</td>
</tr>
<tr>
<td valign="top">

1.69.0

</td>
<td valign="top">

\>=1.132

</td>
</tr>
<tr>
<td valign="top">

1.70.1

</td>
<td valign="top">

\>=1.133

</td>
</tr>
<tr>
<td valign="top">

1.72.0

</td>
<td valign="top">

\>=1.134

</td>
</tr>
<tr>
<td valign="top">

1.72.3

</td>
<td valign="top">

\>=1.135

</td>
</tr>
<tr>
<td valign="top">

2.0.0 *or* 1.73.1

</td>
<td valign="top">

\>=1.136

</td>
</tr>
<tr>
<td valign="top">

2.1.0 *or* 1.75.1

</td>
<td valign="top">

\>=1.137

</td>
</tr>
<tr>
<td valign="top">

2.1.0 *or* 1.76.0

</td>
<td valign="top">

\>=1.138

</td>
</tr>
<tr>
<td valign="top">

2.1.0 *or* 1.77.0

</td>
<td valign="top">

\>=1.139

</td>
</tr>
<tr>
<td valign="top">

2.1.1 *or* 1.78.0

</td>
<td valign="top">

\>=1.140

</td>
</tr>
<tr>
<td valign="top">

2.2.0 *or* 1.79.0

</td>
<td valign="top">

\>=1.141

</td>
</tr>
<tr>
<td valign="top">

2.3.1 *or* 1.80.1

</td>
<td valign="top">

\>=1.142

</td>
</tr>
<tr>
<td valign="top">

2.3.1 *or* 1.81.1

</td>
<td valign="top">

\>=1.143

</td>
</tr>
<tr>
<td valign="top">

2.4.0 *or* 1.82.0

</td>
<td valign="top">

\>=1.144

</td>
</tr>
</table>

For more information on the new fields introduced in each version and implications when upgrading, check out [Migration Information for Upgrading the Manifest File](migration-information-for-upgrading-the-manifest-file-a110f76.md).

For more information about Manifest releases, versions, and the supported and deprecated manifest sections, refer to the documentation [Manifest Changelog](https://github.com/SAP/ui5-manifest/blob/HEAD/CHANGELOG.md).

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__manifirst"/>

## Manifest First Function

By default, all [modern component instantiation methods](component-instantiation-guide-346599f.md) load the `manifest.json` file before creating the component instance. This approach enables preloading of dependencies \(libraries and components\), thereby improving component loading performance. Additionally, OData models can be configured with `preload: true` to ensure the early loading of metadata and annotations during component initialization.

The `manifest` option allows you to configure when and from where the manifest is loaded:

-   Default, equivalent to setting `manifest` to `true`.

    ```js
    // "Component" required from module "sap/ui/core/Component"
    // load manifest.json from default location and evaluate it before creating an instance of the component 
    Component.create({
      name: "sap.my.component",
    });
    ```

-   Specify an alternative URL as parameter for `manifest` for the component factory function:

    ```js
    // "Component" required from module "sap/ui/core/Component"
    // load via manifest URL
    Component.create({
      name: "sap.my.component",
      manifest: "any/location/sap/my/component/manifest.json"
    });
    ```

-   There are two possible scenarios for setting the `manifest` flag to `false`:

    1.  The component defines `manifest: "json"` in its [Component Metadata](component-metadata-0187ea5.md).

        In this case, the manifest is loaded and evaluated **after** the Component controller. All dependencies defined in the manifest will then also be loaded. Afterwards, the Component is instantiated.

    2.  The component does not define `manifest: "json"` in its [Component Metadata](component-metadata-0187ea5.md).

        This is typically the case for older legacy Components without a manifest. In this case, only the Component's class metadata is evaluated. No additional manifest file will be loaded.


    ```js
    // "Component" required from module "sap/ui/core/Component"
    // load component without loading a manifest first
    //  - Case 1: the manifest.json is loaded after the Component controller
    //  - Case 2: no manifest.json is loaded (legacy)
    Component.create({
      name: "sap.my.component",
      manifest: false
    });
    ```


> ### Note:  
> When you enable `manifest`, all legacy component metadata needs to be migrated into the manifest for applications/components. Only those entries in the manifest for components will be respected by the component and all other entries will be ignored.

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_rmc_3xj_mmb"/>

## Special `ui5://` URLs

Inside the manifest, you can use special URLs prefixed with `ui5://`. These URLs will be resolved automatically during component startup before any models are created.

The `ui5://` URLs have the following properties:

-   only absolute URLs are allowed, e.g. `ui5://my/path/to/sample`, but not `ui5:my/app/path`,
-   all URL prefixes to be used inside a `ui5://` URL must be registered on the UI5 loader beforehand \(see the example below\),
-   `sap.ui5/resourceRoots` can be part of a `ui5://` URL,
-   the component factory [`Component.create`](https://ui5.sap.com/#/api/sap.ui.core.Component%23methods/sap.ui.core.Component.create) takes care of defining the resource roots before any `ui5://` URLs are resolved.

***

### Example

One common use case is the resolution of local annotation files. By default the local annotation files are resolved relative to the manifest. When using a `ui5://` URL, you can enforce a different resolution, e.g. to a server-absolute URL.

In this sample, we make sure that the component location is registered as a path on the UI5 loader. Additionally, we assume that the host system is`http://localhost:8080` :

```js
sap.ui.loader.config({
    paths: {
        "my/url/prefix": "this/url/is/reachable"
    }
})
```

The following snippet shows a sample annotation file configuration in the `sap.app/dataSources` section of the manifest:

```json
{
    ...
    "sap.app": {
         "dataSources": {
             "OData": {
                "uri": "/path/to/odata/service",
                "type": "OData",
                "settings": {
                    "odataVersion": "2.0",
                    "annotations": ["annotations"]
                    ...
                }
            },
            ...
            "annotations": {
                "uri": "ui5://my/url/prefix/annotations.xml",
                "type": "ODataAnnotation"
            }
            ...
         }
    }
    ...
}
```

During startup of the respective component the resolution of the `ui5://` URL for the sample annotation will look like this:

```html
ui5://my/url/prefix/annotations.xml
```

is resolved to:

```html
http://localhost:8080/this/url/is/reachable/annotations.xml
```

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_mhs_vdp_znb"/>

## Manifest Content

> ### Note:  
> You can find an example `manifest.json` file with sample code for the manifest content [here](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_example).

The content for the is contained in the following namespaces: `without`, `sap.app`, `sap.ui`, and `sap.ui5` . The following tables show the application-specific attributes provided by the respective namespaces:

[No Namespace](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_nonamespace)

[`sap.app`](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_sap_app)

[`sap.ui`](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_sap_ui)

[`sap.ui5`](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_sap_ui5)

[`sap.card`](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_sap_card)

[`_version`](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_version)

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_nonamespace"/>

## No Namespace

**Attributes in the without namespace**


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`start_url` 

</td>
<td valign="top">

Start page of your app, if available

</td>
</tr>
<tr>
<td valign="top">

`$schema` 

</td>
<td valign="top">

JSON schema URI

</td>
</tr>
</table>

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_sap_app"/>

## `sap.app`

**Attributes in the mandatory sap.app namespace**


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`id` 

</td>
<td valign="top">

This is a mandatory attribute that must be provided in dot notation and specifies a unique ID for the project within the system. It serves as a reference point for most operations involving the manifest. For example, it must be specified in the target mapping when configuring a Launchpad App Descriptor in an ABAP system.

When developing an app or a reuse component, it must match the namespace provided in the corresponding `Component.js`

If, for example, a module is instantiated there as follows:

```js
   return UIComponent.extend("sap.ui.demo.walkthrough.Component", {

      metadata : {
         manifest: "json"
      },
   ...

```

then its `id` would be `sap.ui.demo.walkthrough`

If the manifest belongs to an app variant of an existing application \(the file nameis manifest.appdescr\_variant\), `sap.app/id` is the ID of this app variant. The ID of the underlying base application is then provided in `sap.ui5/componentName`.

> ### Note:  
> The ID must not exceed 70 characters. It must be unique.
> 
> In case of `sap.app/type=application`, the `sap.app/id` corresponds to the `id` of the UI5 component.



</td>
</tr>
<tr>
<td valign="top">

`type` 

</td>
<td valign="top">

A mandatory attribute. The following values are possible:

-   `application`: use if your `manifest.json` describes a **UI5 application**.For an example how to use a `manifest.json` for UI5 applications, see [Step 10: Descriptor for Applications](../03_Get-Started/step-10-descriptor-for-applications-8f93bf2.md) in the Walkthrough Tutorial.

-   `component`: use if your `manifest.json` describes a **reuse component** that is used in several apps. For further reuse component-specific configuration options, see [Manifest for Components \(Inside Libraries\)](manifest-for-components-inside-libraries-7701636.md).

-   `library`: use if your `manifest.json` describes a **UI5 library**. For further library-specific configuration options, see [Manifest for Libraries](manifest-for-libraries-b229914.md).

-   `card`: use if your `manifest.json` describes a **UI5 card**.For further card-specific configuration options, see [Integration Cards](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/overview/introduction).




</td>
</tr>
<tr>
<td valign="top">

`i18n` 

</td>
<td valign="top">

The i18n property is an **optional** attribute and contains one of the following:

-   A URL string to the properties file that contains the text symbols for the manifest; the URL is interpreted relative to the `manifest`.



-   An object that has been defined as described in [Supported Locales and Fallback Chain](supported-locales-and-fallback-chain-ec753bc.md) and [Terminologies](terminologies-eba8d25.md).

    > ### Note:  
    > The `sap.app/i18n` section only supports terminologies for Components. Library manifests **do not support** additional terminologies.


If the manifest contains placeholders in `{{...}}` syntax, but no `i18n` attribute has been provided, the default value `i18n/i18n.properties` is used to request a ResourceBundle.

</td>
</tr>
<tr>
<td valign="top">

`applicationVersion` 

</td>
<td valign="top">

Mandatory version of the app \(semantic version with the following format **`major.minor.patch`**\)

</td>
</tr>
<tr>
<td valign="top">

`embeds` 

</td>
<td valign="top">

Array of relative paths to the nested `manifest.json` files; attribute is mandatory if a nested `manifest.json` exists

</td>
</tr>
<tr>
<td valign="top">

`embeddedBy` 

</td>
<td valign="top">

Relative path back to the `manifest.json` file of an embedding component or library; attribute is mandatory for a nested `manifest.json` 

</td>
</tr>
<tr>
<td valign="top">

`title` 

</td>
<td valign="top">

Mandatory attribute; to make this property language dependent \(recommended\), use a key in double curly brackets: `{{key}}` 

</td>
</tr>
<tr>
<td valign="top">

`subTitle` 

</td>
<td valign="top">

Subtitle; to make this property language dependent \(recommended\), use a key in double curly brackets: `{{key}}` 

</td>
</tr>
<tr>
<td valign="top">

`shortTitle` 

</td>
<td valign="top">

Short version of the title; to make this property language dependent \(recommended\), use a key in double curly brackets: `{{key}}` 

</td>
</tr>
<tr>
<td valign="top">

`info` 

</td>
<td valign="top">

Needed for CDM \(Common Data Model\) conversion of tiles; to make this property language dependent \(recommended\), use a key in double curly brackets: `{{key}}` 

</td>
</tr>
<tr>
<td valign="top">

`description` 

</td>
<td valign="top">

Description; to make this property language dependent \(recommended\), use a key in double curly brackets: `{{key}}` 

</td>
</tr>
<tr>
<td valign="top">

`tags` 

</td>
<td valign="top">

Contains the following:

-   An array of **`keywords`**; either text or a language-dependent entry to be specified via `{{…}}` syntax, for example `"keywords": ["{{keyWord1}}","{{keyWord2}}"]`.

-   An array of **`technicalAttributes`** \(general technical attributes, for example, technical catalog, upper case and language-independent attributes\).




</td>
</tr>
<tr>
<td valign="top">

`dataSources` 

</td>
<td valign="top">

Unique key/alias for specifying the used data sources; contains the following information:

-   `uri`: Mandatory relative URL in the component; takes `embeddedBy` into account, if filled, or the server absolute of the data source, for example `"/sap/opu/odata/snce/PO_S_SRV;v=2/"`. `uri` should always be given in lower case.
-   `type`: Supported types:
    -   `OData` \(default\)
    -   `ODataAnnotation`
    -   `INA`
    -   `XML`
    -   `JSON`
    -   `FHIR`
    -   `http`
    -   `WebSocket`

-   `customType` \(As of 1.77\): `true`/`false`; if `true`, there is no validation on the `type` attribute
-   `settings`: Data source type-specific attributes \(key, value pairs\), which are:
    -   `odataVersion`: 2.0 \(default\), 4.0
    -   `localUri`: Relative URL to local metadata document or annotation URI
    -   `annotations`: Array of annotations which references an existing data source of type `ODataAnnotation` under `sap.app/dataSources`

    -   `maxAge`: Indicates the number of seconds the client is willing to accept with regard to the age of the data that is requested

    -   `objects`: Dictionary of \(catalog\) objects offered by the INA datasource \(as of 1.92\) consisting of:
        -   `objectName`: Mandatory CDS view name / analytical query name
        -   `objectType` - mandatory type of object \(`2C<DDICNAME>` or `CDSViewName`\); values: `query`, `cdsprojectionview`, `view`, `inamodel`
        -   `packageName`: Name of the package
        -   `schemaName`: Name of the schema





</td>
</tr>
<tr>
<td valign="top">

`cdsViews` 

</td>
<td valign="top">

Array of directly used CDS views

This attribute is optional and only added if used via INA protocol directly, not if used via OData service.

</td>
</tr>
<tr>
<td valign="top">

`offline` 

</td>
<td valign="top">

Indicates whether the app is running offline; default is `false` \(online\)

</td>
</tr>
<tr>
<td valign="top">

`sourceTemplate` 

</td>
<td valign="top">

If an app has been generated from a template, this attribute is filled automatically by the generation tool:

-   `id`: Mandatory ID of the template from which the app was generated

-   `version`: Mandatory version of the template from which the app was generated

-   `toolsId`: ID generated by the tool




</td>
</tr>
<tr>
<td valign="top">

`openSourceComponents` 

</td>
<td valign="top">

Array of directly used open source libraries for documentation purposes; not used when open source libraries are used via OpenUI5 capsulation

-   `name`: Mandatory name of the open source component

-   `version`: Required if the open source component is part of the app; not required if the open source component is part of the OpenUI5 dist layer

-   `packagedWithMySelf`: Indicates if the open source component is part of the app \(`true`\) or not \(`false`\)




</td>
</tr>
<tr>
<td valign="top">

`resources` 

</td>
<td valign="top">

Relative URL as a reference to a file \(naming convention is `resources.json`\) that contains a list of all resources needed by the app \(all resources inside the app\); the file is generated in an SAP Fiori tools \(in SAP Business Application Studio\) build step.

For a description of `resources.json`, see [The resources.json File](the-resources-json-file-adcbcf8.md).

</td>
</tr>
</table>

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_sap_ui"/>

## `sap.ui`

**Attributes in the mandatory sap.ui namespace**


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`technology` 

</td>
<td valign="top">

A mandatory attribute that specifies the UI technology; value is `UI5` 

</td>
</tr>
<tr>
<td valign="top">

`icons` 

</td>
<td valign="top">

Contains object with app-specific icons, which are:

-   `icon`: Icon of the app, can be chosen from [Icon Explorer](https://ui5.sap.com/test-resources/sap/m/demokit/iconExplorer/webapp/index.html) .
-   `favIcon`: ICO file to be used inside the browser and for desktop shortcuts

    > ### Note:  
    > `favIcon` is not set automatically by the framework. The icons can be set manually using the `sap/ui/util/Mobile` module and the `setIcons` function.

-   `phone`: 120x120 pixel version for iPhones with low pixel density
-   `phone@2`: 180x180 pixel version for iPhones with high pixel density
-   `tablet`: 152x152 pixel version for iPads with low pixel density
-   `tablet@2`: 167x167 pixel version for iPads with high pixel density



</td>
</tr>
<tr>
<td valign="top">

`deviceTypes` 

</td>
<td valign="top">

Mandatory; contains objects with device types on which the app is running, such as:

-   `desktop`: Indicator for whether desktop devices are supported, `true`, `false`
-   `tablet`: Indicator for whether tablet devices are supported, `true`, `false`
-   `phone`: Indicator for whether phone devices are supported, `true`, `false`



</td>
</tr>
</table>

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_sap_ui5"/>

## `sap.ui5`

The `sap.ui5` namespace is aligned with the former concept of component metadata and contributes the following OpenUI5-specific attributes for the manifest, see [Migrating from Component Metadata to Manifest](migrating-from-component-metadata-to-manifest-e282db2.md) for more details.

**Attributes in the sap.ui5 namespace**


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`resources` 

</td>
<td valign="top">

Specifies additional `css` and `js` resources of the Component.

CSS files are added to the head of the HTML page as a link tag. JavaScript files are loaded by the `require` mechanism.

Two settings can be defined per resource:

-   `uri` \(mandatory\): URLs are resolved relative to the Component, taking the `embeddedBy` setting into account \(if filled\).

-   `id` \(optional\): Only for `css` resources; the id for a CSS file's `<link>` element.


> ### Note:  
> Since 1.94 the usage of `js` resources is deprecated. Please use regular `dependencies` instead.



</td>
</tr>
<tr>
<td valign="top">

`dependencies` 

</td>
<td valign="top">

Mandatory; specifies the external dependencies that are loaded by the OpenUI5 core during the initialization phase of the component and used afterwards. These are the following libraries or components:

-   `minUI5Version`: Mandatory; Minimum version of OpenUI5 that your component requires; this information ensures that the features of the OpenUI5 runtime version of the component are available. This must be either a specific version or an array of versions where each major version can only be included once. If you specify an array that contains more than one version, and if version 1 is included, it must be at least 1.120.x. As OpenUI5 does not currently enforce use of the correct version, the `minUI5Version` is used for information purposes only. If the minimum OpenUI5 version criteria is not fulfilled, a warning is issued in the console log.

-   `libs`: ID \(namespace\) of the libraries that the OpenUI5 core should load for use in the component. If your app requires a minimum version of the lib, specify the `minVersion` for information purposes. Specify `lazy` to indicate that the lib shall be lazy loaded.

-   `components`: ID \(namespace\) of the components that the OpenUI5 core should load for use in your component. If your app requires a minimum version of the component, specify the `minVersion` for information purposes. Specify `lazy` to indicate that the component shall be lazy loaded.


For more information, see [Descriptor Dependencies to Libraries and Components](descriptor-dependencies-to-libraries-and-components-8521ad1.md).

</td>
</tr>
<tr>
<td valign="top">

`componentUsages` 

</td>
<td valign="top">

Specifies the used components with the a unique key/alias. Contains the following:

-   `name`: Mandatory name of the reuse component

-   `settings`: Settings of the component

-   `componentData`: Component data of the component

-   `lazy`: Indicates whether the component usage should be lazily loaded. Default value: `true`


For more information, see: [Component Instantiation Guide](component-instantiation-guide-346599f.md).

</td>
</tr>
<tr>
<td valign="top">

`models` 

</td>
<td valign="top">

> ### Note:  
> For component manifests only. Libraries can not define models.

Defines models that should be created or destroyed along the component's lifecycle. The key represents the model name. Use an empty string \(""\) for the default model.

-   `type`: Model class name
-   `uri`: Relative URL in the component, taking `embeddedBy` into account if filled, or server for absolute model
-   `settings`: Object that is passed to the model constructor.

    > ### Example:  
    > You can overwrite the default binding mode with the `defaultBindingMode` attribute \(enumeration of type `sap.ui.model.BindingMode`, with values. `Default`, `OneTime`, `OneWay`, `TwoWay`\). For OData models constructor see the following:
    > 
    > -   [sap.ui.model.odata.v2.ODataModel](https://ui5.sap.com/#/api/sap.ui.model.odata.v2.ODataModel/constructor)
    > 
    > -   [sap.ui.model.odata.v4.ODataModel](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel/constructor)
    > 
    > 
    > For ResourceModel constructor see:
    > 
    > -   [sap.ui.model.resource.ResourceModel](https://ui5.sap.com/#/api/sap.ui.model.resource.ResourceModel/constructor)
    > 
    > 
    > The attribute `enhanceWith` can be specified with `bundleUrl`, `bundleUrlRelativeTo` \(either `component` \(default\) or `manifest`\) or `bundleName` to provide a list of additional resource bundle configurations to enhance the `ResourceModel` with. Additional attributes can be found in [Supported Locales and Fallback Chain](supported-locales-and-fallback-chain-ec753bc.md) and [Terminologies](terminologies-eba8d25.md).

-   `dataSource`: String of key or alias from `sap.app dataSources` to reference an existing data source; the `type`, `uri` and `settings` properties are set according to the data source's `type`, `uri` and `settings` \(if not already defined\). If the type under `sap.app dataSources` is `OData`, an OData Model V2 is created automatically. If you need an OData Model V1, specify the `type` as well.
-   `preload`: Optional; Boolean with `true`, `false` \(default\)

    Defines whether or not the model is initialized \(preloaded\) before the component instance is created and while loading the component preload and its dependencies.

    For more information, see [Manifest Model Preload](manifest-model-preload-26ba6a5.md).




</td>
</tr>
<tr>
<td valign="top">

`rootView` 

</td>
<td valign="top">

Specifies the root view that shall be opened; can be the view name as a string for XML views, or the view configuration object with `viewName` for the view name as a string \(see [sap.ui.core.mvc.View.create](https://ui5.sap.com/#/api/sap.ui.core.mvc.View/methods/sap.ui.core.mvc.View.create)\) and `type` for the type \(enumeration of [sap.ui.core.mvc.ViewType](https://ui5.sap.com/#/api/sap.ui.core.mvc.ViewType)\), **id**, **async**, and other properties of `sap.ui.core.mvc.view`.

</td>
</tr>
<tr>
<td valign="top">

`autoPrefixId` 

</td>
<td valign="top">

true, false \(default\), Enables the auto prefixing for the UIComponent for IDs of ManagedObjects \(controls or elements\) which are created in the context of the `createContent` function, or any other invocation of the `Component.prototype.runAsOwner()` function \(for example a component's router uses this method when creating new views\).

In former OpenUI5 releases this prefixing of the ID needed to be done with `oComponent.createId` by overwriting the method `getAutoPrefixId`. The same can now be achieved declaratively by setting `autoPrefixId` to true.

</td>
</tr>
<tr>
<td valign="top">

`handleValidation` 

</td>
<td valign="top">

Possible values: `true` or `false` \(default\); used to enable or disable validation handling by the message manager for this component, see [Error, Warning, and Info Messages](error-warning-and-info-messages-62b1481.md) 

</td>
</tr>
<tr>
<td valign="top">

`config` 

</td>
<td valign="top">

Static configuration; specify the name-value pairs that you need in your component.

</td>
</tr>
<tr>
<td valign="top">

`routing` 

</td>
<td valign="top">

Provides configuration parameters for route and router, see [Routing and Navigation](routing-and-navigation-3d18f20.md) 

</td>
</tr>
<tr>
<td valign="top">

`extends` 

</td>
<td valign="top">

Used to extend another component.

-   `component`: ID \(namespace\) of the component being extended

-   `minVersion`: Specifies the minimum version of the component being extended, for information purposes if your app requires a minimum version of the component

-   `extensions`: Component or view extensions, which enable you to replace and extend views and controllers and also to modify the views, see [Extending Apps](../06_Extending_SAPUI5_Applications/extending-apps-a264a9a.md)




</td>
</tr>
<tr>
<td valign="top">

`contentDensities` 

</td>
<td valign="top">

Mandatory; contains an object with the content density modes that the app supports, see [Content Densities](content-densities-e54f729.md)

-   `compact`: Mandatory; indicates whether compact mode is supported \(`true`, `false`\)

-   `cozy`: Mandatory; indicates whether cozy mode is supported \(`true`, `false`\)




</td>
</tr>
<tr>
<td valign="top">

`resourceRoots` 

</td>
<td valign="top">

Map of URL locations keyed by a resource name prefix; only relative paths inside the component are allowed and no ".." characters

This attribute is intended for actual sub-packages of the component only, meaning that it must not be used for the component namespace itself.

> ### Note:  
> When loading with *manifest first*\(by using the property `manifest`\), the `resourceRoots` are evaluated before the component controller is loaded. Otherwise, the defined resource roots will be registered after the component controller is loaded and do not affect the modules being declared as dependencies in the component controller.



</td>
</tr>
<tr>
<td valign="top">

`componentName` 

</td>
<td valign="top">

An optional attribute that only has to be provided if your project is a variant of an existing application. In this case the `componentName` has to contain the `sap.app/id` of the existing application which is the basis of your variant.

</td>
</tr>
<tr>
<td valign="top">

`library/i18n` 

</td>
<td valign="top">

> ### Note:  
> For library manifests only.

Determines whether the library contains an i18n resource. The value can be either a boolean, a string, or an object.

A string value represents a bundle URL. Relative URLs are always resolved to the library origin. If no value is set, the default `messagebundle.properties` file is loaded.

An object value can contain additional resource bundle configuration, e.g. terminologies and supported locales. For the supported features and for sample definitions, see the respective entries at [Terminologies](terminologies-eba8d25.md) \(without `bundleUrlRelativeTo`\) and [Supported Locales and Fallback Chain](supported-locales-and-fallback-chain-ec753bc.md) .

> ### Note:  
> This attribute is beneficial if the name of the main resource bundle \(properties file\) used by your UI5 library differs from the default name `messagebundle.properties`



</td>
</tr>
<tr>
<td valign="top">

`commands` 

</td>
<td valign="top">

Specifies provided commands with a unique key/alias. Contains:

-   `shortcut`: String that describes a key combination. When the user presses the key combination, the command is triggered.


The name of the command that contains the `shortcut` definition acts as a prerequisite for using the `command` property of the `sap.ui.core.CommandExecution` module. For more information, see the [API Reference: `sap.ui.core.CommandExecution`](https://ui5.sap.com/#/api/sap.ui.core.CommandExecution). 

</td>
</tr>
</table>

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_sap_card"/>

## `sap.card`

**Attributes in the sap.card namespace**


<table>
<tr>
<th valign="top">

Attribute

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

`type` 

</td>
<td valign="top">

Describes the card type; possible values are `list` and `analytical` 

</td>
</tr>
<tr>
<td valign="top">

`header` 

</td>
<td valign="top">

Specifies the card's header area

</td>
</tr>
<tr>
<td valign="top">

`content` 

</td>
<td valign="top">

Specifies the type-dependent card content

</td>
</tr>
</table>

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_version"/>

## `_version`

-   On root level \(no namespace\): Describes the manifest format version \(mandatory\). Needs to be updated when migrating to a new manifest format version, see [Migrating from Component Metadata to Manifest](migrating-from-component-metadata-to-manifest-e282db2.md)

-   Inside namespace: Describes the namespace format version \(optional from version 1.38 on\)


***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_descriptor_schema"/>

## Manifest Schema

The newest flattened JSON schema is available on the SAP Open Source GitHub at [https://github.com/sap/ui5-manifest/](https://github.com/sap/ui5-manifest/) under Apache-2.0 License. It can be used to enable schema validation, code completion, and documentation.

***

<a name="loiobe0cf40f61184b358b5faedaec98b2da__section_example"/>

## Example

Current version of the `manifest.json`

> ### Note:  
> The following sample contains the **full scope of all available manifest properties**. Some properties might not be applicable for all `manifest.json` variants. For example, the `sap.ui5/models` \}, "liabilities": \{, "cdsService": \{ "uri": "/sap/bc/ina/ina1/sap/ex section is not supported for library "settings": \{ "localUri": "localServi

```

{
"_version": "1.82.0",
 
    "start_url": "index.html",
 
    "sap.app": {
        "id": "sap.fiori.appName",
        "type": "application",
        "i18n": "i18n/i18n.properties",
        "applicationVersion": {
            "version": "1.2.2"
        },
        "embeds": ["mycomponent1", "subpath/mycomponent2"],
        "embeddedBy": "../../",
        "title": "{{title}}",
        "subTitle": "{{subtitle}}",
        "shortTitle": "{{shorttitle}}",
        "description": "{{description}}",
        "info": "{{info}}",
        "tags": {
            "keywords": ["{{keyWord1}}", "{{keyWord2}}"],
            "technicalAttributes": ["ATTRIBUTE1", "ATTRIBUTE2"]
        },
        "dataSources": {
            "equipment": {
                "uri": "/sap/opu/odata/snce/po_s_srv;v=2/",
                "type": "OData",
                "settings": {
                    "odataVersion": "2.0",
                    "annotations": ["equipmentanno"],
                    "localUri": "model/metadata.xml",
                    "maxAge": 360
                }
            },
            "equipmentanno": {
                "uri": "/sap/bc/bsp/sap/nscbn_anf_eam/bscbn_equipment_srv.anno.xml",
                "type": "ODataAnnotation",
                "settings": {
                    "localUri": "model/annotations.xml"
                }
            }

                            "objectName": "SAPFinLiabilities",
                            "objectType": "cdsprojectionview"        },
        "cdsViews": [
            "VIEW1", "VIEW2"
        ],
        "resources": "resources.json",
        "offline": true,
        "sourceTemplate": {
            "id": "sap.ui.ui5-template-plugin.1worklist",
            "version": "1.0.0",
            "toolsId": "C12345678"
        },
        "destination": {
            "name": "SAP_ERP_FIN"
        },
        "openSourceComponents": [{
            "name": "D3.js",
            "packagedWithMySelf": false
        }]
    },
 
    "sap.ui": {
        "technology": "UI5",
        "icons": {
            "icon": "sap-icon://add-contact",
            "favIcon": "icon/F1373_Approve_Purchase_Orders.ico",
            "phone": "icon/launchicon/57_iPhone_Desktop_Launch.png",
            "phone@2": "icon/launchicon/114_iPhone-Retina_Web_Clip.png",
            "tablet": "icon/launchicon/72_iPad_Desktop_Launch.png",
            "tablet@2": "icon/launchicon/144_iPad_Retina_Web_Clip.png"
        },
        "deviceTypes": {
            "desktop": true,
            "tablet": true,
            "phone": false
        }
    },
 
    "sap.ui5": {
        "resources": {
            "css": [{
                "uri": "component.css",
                "id": "componentcss"
            }]
        },
        "dependencies": {
            "minUI5Version": "1.144.0",
            "libs": {
                "sap.m": {
                    "minVersion": "1.34.0"
                },
                "sap.ui.commons": {
                    "minVersion": "1.34.0",
                    "lazy": true
                }
            },
            "components": {
                "sap.ui.app.other": {
                    "minVersion": "1.1.0",
                    "lazy": true
                }
            }
        },
        "componentUsages": {
            "myusage": {
                "name": "my.used",
                "lazy": false,
                "settings": {},
                "componentData": {}
            }
        },
        "models": {
            "i18n": {
                "type": "sap.ui.model.resource.ResourceModel",
                "uri": "i18n/i18n.properties",
                "settings": {
                    "enhanceWith": [{
                        "bundleUrl": "i18n/i18n.properties",
                        "bundleUrlRelativeTo": "manifest"
                    }]
                }
            },
            "equipment": {
                "preload": true,
                "dataSource": "equipment",
                "settings": {}
            }
        },
        "rootView": {
            "viewName": "sap.ui.test.view.Main",
            "id" : "rootView",
            "async": true,
            "type": "XML"
        },
        "handleValidation": true,
        "config": {
 
        },
        "routing": {
 
        },
        "extends": {
            "component": "sap.fiori.otherApp",
            "minVersion": "0.8.15",
            "extensions": {}
        },
        "contentDensities": {
            "compact": true,
            "cozy": false
        },
        "resourceRoots": {
            ".myname": "./myname"
        },
        "componentName": "sap.fiori.appName",
        "library": {
            "i18n": true
        },
        "commands": {
            "Save": {
                "shortcut": "Ctrl+S"
            }
        }
    },

 

    "sap.fe": {},
    "sap.card": {}
}
```

For the following namespaces, the indicated teams are responsible:

-   sap.fe - in SAP Fiori elements responsibility

-   sap.card - in SAPUI5 responsibility


***

## Declaration in Component Metadata

The component declares the existence of the manifest by specifying `manifest: "json"` in the component metadata. Setting this flag makes the component load the `manifest.json` file and read the relevant entries for OpenUI5. This metadata is used to define the dependencies that need to be loaded in order to start the component. The following code snippet shows how to add the manifest link:

```js
sap.ui.define([
	"sap/ui/core/UIComponent"
], (UIComponent) => {
	"use strict";
	return UIComponent.extend("my.sample.Component", {
		metadata: {
			manifest: "json",
			interfaces: [
				"sap.ui.core.IAsyncContentCreation"
			]
		}
	});
});
```

***

## OpenUI5 API

At runtime, the manifest content can be accessed from the component via the following `sap.ui.core.Component` APIs:

```js
// Given: oComponent === instance of sap.ui.core.Component (e.g. returned by sap.ui.core.mvc.Controller#getOwnerComponent)
oComponent.getManifest(); // returns reference to the entire manifest object if it exists; otherwise returns null
oComponent.getManifestEntry("sap.app"); // returns reference to the configuration section of the manifest
oComponent.getManifestEntry("/sap.ui5/dependencies/libs"); // returns reference or value of the manifest configuration by path; the syntax must start with a slash
```

-   **[Migrating from Component Metadata to Manifest](migrating-from-component-metadata-to-manifest-e282db2.md "Overview, how the component metadata are mapped to the manifest (descriptor for
		applications, components and libraries). ")**  
Overview, how the component metadata are mapped to the manifest \(descriptor for applications, components and libraries\).
-   **[Migration Information for Upgrading the Manifest File](migration-information-for-upgrading-the-manifest-file-a110f76.md "Information how to add new attributes of manifest (also known as descriptor) versions
		higher than V2 (OpenUI5 1.30) to
		the manifest file.")**  
Information how to add new attributes of manifest \(also known as descriptor\) versions higher than V2 \(OpenUI5 1.30\) to the manifest file.
-   **[Manifest for Libraries](manifest-for-libraries-b229914.md "The manifest (also known as descriptor) for libraries contains a subset of the
		attributes in the manifest for applications and components.")**  
The manifest \(also known as descriptor\) for libraries contains a subset of the attributes in the manifest for applications and components.
-   **[Manifest for Components \(Inside Libraries\)](manifest-for-components-inside-libraries-7701636.md "The manifest (also known as descriptor) for components contains a subset of the
		attributes in the manifest for applications ")**  
The manifest \(also known as descriptor\) for components contains a subset of the attributes in the manifest for applications
-   **[The resources.json File](the-resources-json-file-adcbcf8.md "The resources.json file lists all resources in a component or library folder. It resides next to each
			manifest.json in the generated results.")**  
The `resources.json` file lists all resources in a component or library folder. It resides next to each `manifest.json` in the generated results.
-   **[Creating a Manifest File for Existing Apps](creating-a-manifest-file-for-existing-apps-3a9baba.md "Detailed description of the steps needed to create a manifest (also known as
        descriptor) V2 for applications file for an existing transactional app
            created by the customer based on SAP Fiori.")**  
Detailed description of the steps needed to create a manifest \(also known as descriptor\) V2 for applications file for an existing transactional app created by the customer based on SAP Fiori.
-   **[Descriptor Dependencies to Libraries and Components](descriptor-dependencies-to-libraries-and-components-8521ad1.md "Description of the performance-relevant attributes that are available for the descriptor
		for applications, components and libraries")**  
Description of the performance-relevant attributes that are available for the descriptor for applications, components and libraries
-   **[Manifest Model Preload](manifest-model-preload-26ba6a5.md "The preload flag  enables a preload mode for a model, thus improving
		the startup performance of an app or component.")**  
The `preload` flag enables a preload mode for a model, thus improving the startup performance of an app or component.
-   **[Enabling the Automatic Header Adaptation for Legacy Applications](enabling-the-automatic-header-adaptation-for-legacy-applications-0635156.md "Application developers can enable automatic adaptation of legacy applications from
		the manifest.json file also known as descriptor for applications,
		components and libraries.")**  
Application developers can enable automatic adaptation of legacy applications from the `manifest.json` file also known as descriptor for applications, components and libraries.

[sap.ui.core.UIComponent](https://ui5.sap.com/#/api/sap.ui.core.UIComponent)

[Component Metadata](component-metadata-0187ea5.md "The component class provides specific metadata for components by extending the ManagedObject class. The UIComponent class provides additional metadata for the configuration of user interfaces or the navigation between views.")

