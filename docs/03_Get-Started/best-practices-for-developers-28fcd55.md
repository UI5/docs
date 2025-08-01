<!-- loio28fcd55b04654977b63dacbee0552712 -->

# Best Practices for Developers

This page is a good starting point for you to ensure your code bases, specifically your OpenUI5 applications and libraries, are ready for the future and won't become outdated.

**On this page:**

-   [Best Practices for Legacy-Free Code](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_blfc)
-   [App Development](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_appdev)
-   [Control Development](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_ctrldev)
-   [Library Development](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_libdev)
-   [Testing](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_tst)

***

<a name="loio28fcd55b04654977b63dacbee0552712__section_blfc"/>

## Best Practices for Legacy-Free Code

The OpenUI5 framework is always evolving to benefit from newer features in web browsers \(like ECMAScript support\) or to account for their end of maintenance \(like the end of IE11 support\). This is a continuous journey towards future major framework versions and improvements.

It is therefore important that you keep applying best practices. To help you, we frequently update the documentation in many places. This page collects fundamental information and offers practical guidance, and it will continue to evolve over time.

> ### Note:  
> The following information is a preliminary yet practical collection of best practices to ensure legacy-free OpenUI5 development. We're continuously improving it to reflect our latest recommendations. It will be further enhanced to both help transform existing code bases and provide guidance for creating new code.

***

### Goals

The main objectives when migrating existing code or keeping it up to date with framework best practices are:

-   **No sync loading of code**

    This is for compliance with our Content Security Policy. For more information, see [Make Your App CSP Compliant](make-your-app-csp-compliant-1f81a09.md).

-   **No sync loading of data**

    This helps avoid deprecation warnings of web browsers regarding sync XHR.

-   **No use of global names**

    This helps avoid pollution of the global namespace and conflicts with other code on the page.

-   **No use of deprecated APIs**

    This reduces the API surface for easier usage and maintenance.


***

### Prerequisites

Before attempting to migrate or upgrade to a higher OpenUI5 version, make sure that your development does **not** use any undocumented internal framework resources. Also, double check that all compatibility guidelines have been followed, such as those mentioned in [Upgrading](../02_Read-Me-First/upgrading-9638e4f.md).

To build and serve your project in accordance with best practices, we recommend using the latest version of [UI5 Tooling](https://sap.github.io/ui5-tooling/).

***

### Supporting Tool - UI5 Linter

[UI5 linter](https://github.com/UI5/linter) is a command-line tool to identify legacy code in your OpenUI5 project. It checks JavaScript, TypeScript, XML, JSON, and other files in your project and reports findings if legacy code is used. UI5 linter is our state-of-the-art tool to get and keep your OpenUI5 project legacy-free.

***

### Deprecated APIs

In general, **you must not use deprecated APIs** anymore, such as `sap.ui.getCore()`. You can find deprecated APIs in the [API Reference](https://ui5.sap.com/#/api/deprecated), in the [What's New Viewer](https://help.sap.com/whats-new/67f60363b57f4ac0b23efd17fa192d60?Type=Deleted%3BDeprecated), and in the reports by our [Support Assistant](../04_Essentials/support-assistant-57ccd7d.md) and [UI5 linter](https://github.com/UI5/linter). For new projects, we recommend the use of TypeScript, because usage of deprecated APIs can then be detected easily.

Also, see the relevant warnings and errors logged to the browser's dev console during runtime. You might need to increase the `sap-ui-log-level`. For more information, see [Logging and Tracing](../04_Essentials/logging-and-tracing-9f4d62c.md).

Some APIs may be only partially deprecated, for instance passing a non-object `vName` to [`sap.ui.core.theming.Parameters.get`](https://ui5.sap.com/#/api/sap.ui.core.theming.Parameters%23methods/sap.ui.core.theming.Parameters.get). Refer to the API Reference for individual APIs. UI5 linter can also help detecting the deprecated usage of such APIs.

Using the native web API `XMLHttpRequest#open` with `false` as the third argument outside of workers is also deprecated, and browsers might end its support. Therefore, in addition to avoiding already deprecated OpenUI5 APIs, you must not call low-level APIs such as `jQuery.ajax` with a disabled `async` option either.

**Additional Information:**

-   [Don't Use Deprecated or Experimental Features](don-t-use-deprecated-or-experimental-features-a8bd1a8.md)
-   [Deprecated Core API](../04_Essentials/deprecated-core-api-798dd9a.md)
-   [Deprecated Configuration API](../04_Essentials/deprecated-configuration-api-2acafbf.md)
-   [Use Only Public APIs](use-only-public-apis-b0d5fe2.md)
-   [Adapting to the Modularization of the Core](../04_Essentials/adapting-to-the-modularization-of-the-core-b8fdf0c.md)
-   [Replacement of Deprecated jQuery APIs](../04_Essentials/replacement-of-deprecated-jquery-apis-a075ed8.md)
-   [Deprecated Factories Replacement](../04_Essentials/deprecated-factories-replacement-491bd9c.md)
-   [Synchronous `XMLHttpRequest`](https://xhr.spec.whatwg.org/#the-open()-method)

***

### Third-Party Libraries

Do not use any third-party libraries unless they are explicitly documented for usage by applications, for example in the [Test Starter](../04_Essentials/test-starter-032be2c.md) documentation. For more information, see [Third-Party Open Source Libraries](../02_Read-Me-First/compatibility-rules-91f0873.md#loio91f087396f4d1014b6dd926db0e91070__Open_Source).

The integrated QUnit and Sinon libraries can be used via the [Test Starter](../04_Essentials/test-starter-032be2c.md). Do not use the deprecated libraries QUnit 1 and Sinon 1.

Do not use jQuery APIs; use OpenUI5 APIs or native browser APIs instead.

***

### Modules

**Defining and Requiring Modules**

-   Avoid accessing modules via global names.

-   Use `sap.ui.define` for defining a new module, including its eager dependencies.

-   Use `sap.ui.require` for requiring a module lazily at a later point in time.

-   Add only valid module IDs from the API Reference \(documented as Module: .../.../...\) to the dependency list.


For more information, see [Best Practices for Loading Modules](../04_Essentials/best-practices-for-loading-modules-00737d6.md).

**Requiring Third-Party Libraries**

When requiring third-party libraries that export global names and support AMD at the same time, ensure having a `shim` with `amd:true` defined via [`sap.ui.loader.config`](https://ui5.sap.com/#/api/sap.ui.loader%23methods/sap.ui.loader.config) beforehand. Use the required module value instead of the global name of the third-party library. For information on the usage of third-party libraries shipped with OpenUI5, see [Third-Party Libraries](best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__TPL).

**Troubleshooting**

Identify and resolve cyclic dependencies with the help of the OpenUI5 configuration parameter `sap-ui-xx-debug-module-loading=true`. Identified modules are logged in the browser console \([F12\]\) with the message '**cycle detected**'. Ensure that the console shows all levels of logs incl. "Verbose" ones to see this message.

***

<a name="loio28fcd55b04654977b63dacbee0552712__section_appdev"/>

## App Development

In the following we'll focus on crucial aspects of app development, specifically on asynchronous loading and best practices around Components, Controllers, Views, Fragments, Models, and ResourceBundles.

***

### Asynchronous Loading

-   Use asynchronous loading for views, fragments, components, and resource bundles to enhance performance; see, for example, [Deprecated Factories Replacement](../04_Essentials/deprecated-factories-replacement-491bd9c.md).
-   Implement the `sap.ui.core.IAsyncContentCreation` marker interface in your [Component.js file](../04_Essentials/component-controller-27ce0e4.md) to allow the content to be created fully asynchronously and for a stricter handling of certain types of errors during its view processing.
-   Make sure that dependent libraries and components are preloaded before modules from the respective preload are accessed. For example, if the `sap.f.FlexibleColumnLayout` control is part of the root view, `"sap.f": {}` should be included in the `sap.ui5/dependencies/libs` section of the `manifest.json`. Avoid setting `{ "lazy": true }` if the application does not intend to preload the bundle manually. For more information, see [Ensure that Library Preloads are Enabled](../05_Developing_Apps/performance-speed-up-your-app-408b40e.md#loio408b40efed3c416681e1bd8cdd8910d4__section_LibraryPreloads).

**Additional Information:**

-   [Use Asynchronous Loading](use-asynchronous-loading-676b636.md)
-   [Is Your Application Ready for Asynchronous Loading?](is-your-application-ready-for-asynchronous-loading-493a15a.md)
-   [Performance Checklist](performance-checklist-9c6400e.md)
-   [Load Only What You Really Need](load-only-what-you-really-need-e8fca3e.md)
-   [Performance: Speed Up Your App](../05_Developing_Apps/performance-speed-up-your-app-408b40e.md)

***

### OpenUI5 Object Creation

When creating instances of OpenUI5 controls programmatically \(i.e. not declaratively via XML View or Fragment\), then:

-   Don't use the global name of a control. Require the corresponding module dependency instead.
-   Use `createId` to ensure there are no ID collisions, e.g. [`sap.ui.core.mvc.View#createId`](https://ui5.sap.com/#/api/sap.ui.core.mvc.View%23methods/createId) to prefix the control's ID with the view ID.

**Additional Information:**

-   [Use Stable IDs](use-stable-ids-79e910e.md)

***

### Data Binding

-   When creating data binding programmatically, add the data types to the dependency list and create instances on your own. Do **not** specify their global names.

-   When creating an aggregation binding with a template, explicitly set the `templateShareable` option to either `true` or `false`: Use `true` if your code manages the lifecycle of the template instance, or `false` if you prefer the framework to handle this automatically. For more information, see [Lifecycle of Binding Templates](../04_Essentials/lifecycle-of-binding-templates-3a4a9e5.md).

-   When an [Expression Binding](../04_Essentials/expression-binding-daf6852.md) refers to any of the built-in global symbols `odata.compare`, `odata.fillUriTemplate`, or `odata.uriEncode`, the corresponding modules must be required by the surrounding code \(either via [`template:require`](../04_Essentials/require-263f6e5.md), [`core:require`](../04_Essentials/require-modules-in-xml-view-and-fragment-b11d853.md), or in the controller code\):

    -   `odata.compare`: `sap/ui/model/odata/v4/ODataUtils`
    -   `odata.fillUriTemplate`: `sap/ui/thirdparty/URITemplate`
    -   `odata.uriEncode`: `sap/ui/model/odata/ODataUtils`
    -   To cover **all** built-in global symbols of the `odata` namespace at once, you can import `sap/ui/model/odata/ODataExpressionAddons`


**Additional Information:**

-   [Require Modules in XML View and Fragment](../04_Essentials/require-modules-in-xml-view-and-fragment-b11d853.md)
-   [XML Templating](../04_Essentials/xml-templating-5ee619f.md)

***

### Standalone Apps

-   During OpenUI5 bootstrapping, assign `module:sap/ui/core/ComponentSupport` or a separate JavaScript file to `data-sap-ui-on-init`.

-   Avoid inline scripts or inline styles.


**Additional Information:**

-   [Declarative API for Initial Components](../04_Essentials/declarative-api-for-initial-components-82a0fce.md)

***

### Component / `manifest.json`

**Component Creation**

-   To create a root component, favor leveraging the `sap/ui/core/ComponentSupport` module over the `sap.ui.core.ComponentContainer`.

-   When creating a component via `sap.ui.core.ComponentContainer`, avoid setting a falsy value to the `manifest` property if the `async` property is kept undefined. Do not set the `async` property to `false`.

-   `sap.ui.core.Component#createComponent` must not be used with `async: false`.


**`manifest.json`**

-   Use Manifest Version 2. For more information, see [Manifest Version 2](../04_Essentials/manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__section_manifest2).
-   Don't use the section `sap.ui5/resources/js` as it's deprecated. Use regular dependencies in the `Component.js` file instead.

-   Unless the component intends to load specific OpenUI5 libraries manually on demand, avoid adding `{ lazy: true }` to the `sap.ui5/dependencies/libs` section.


**Dependency Management**

Before using the Component's `EventBus` instance via `Component#getEventBus`, define the `sap/ui/core/EventBus` as a dependency in your component controller \(`Component.js`\).

**Bundling**

Prevent bundling modules \(`Component-preload.js`\) into strings.

-   Leverage [UI5 Tooling](https://sap.github.io/ui5-tooling/) to build the bundle. Avoid generating the application bundle with legacy build tooling, such as grunt-openui5.

-   Avoid declaring `var`, `let`, or `const` in the global scope above `sap.ui.define`. If absolutely required, replace e.g. `var myGlobal` with `globalThis.myGlobal` and/or wrap the module definition in an *Immediately Invoked Function Expression* \(IIFE\) if applicable.

-   For third-party libraries that have to define variables globally or must be exempted from being modified \(e.g. due to legal or license reasons\), [exclude them from the bundle](https://sap.github.io/ui5-tooling/v3/pages/Configuration/#excludes).


***

### Controller / Views / Fragments

-   Don't use views of type `HTMLView`, `JSView`, or `JSONView` as they are deprecated. Use `XMLView` or [Typed View](../04_Essentials/typed-view-e6bb33d.md) instead.

-   Don't use `sap.ui.getCore().byId()` or`Element.getElementById()`. Use `this.byId()` or `this.getView().byId()` to address controls in your views or fragments.

-   Don't use native HTML, SVG, or inline CSS style within your XML view or fragment. Instead, consider using the [`sap.ui.core.HTML`](https://ui5.sap.com/#/api/sap.ui.core.HTML) control or your own notepad control. Existing inline CSS must be migrated to an external style sheet.

-   Don't use view cloning via `sap.ui.core.mvc.View#clone` as it's deprecated. Instead, call the respective factory function \(e.g. `XMLView.create`\) with the View's name.

-   Use the `loadFragment` method of the `sap.ui.core.mvc.Controller` to load fragments asynchronously.

-   Don't use global names in your XML. Ensure that the target function or object is defined as a module and require the defined module via [`core:require` in the XML](../04_Essentials/require-modules-in-xml-view-and-fragment-b11d853.md). Use `template:require` if the XML content needs preprocessing.

-   Use the module name syntax \(e.g., `module:myapp/views/MyView`\) when creating a Typed View, Controller, or JS Fragment via factory API. This syntax provides greater flexibility by allowing you to name entities without requiring the `.view.js`, `.controller.js`, or `.fragment.js` suffixes.


**Additional Information:**

-   [Use the MVC Concept](use-the-mvc-concept-07afcf4.md)
-   [Keep Your Views Short and Simple](keep-your-views-short-and-simple-b0d7db7.md)
-   [View Cloning \(deprecated\)](../04_Essentials/view-cloning-deprecated-a575619.md)
-   [Instantiation of Fragments](../04_Essentials/instantiation-of-fragments-04129b2.md)
-   [Programmatically Instantiating XML Fragments](../04_Essentials/programmatically-instantiating-xml-fragments-d6af195.md)
-   [Formatting, Parsing, and Validating Data](../04_Essentials/formatting-parsing-and-validating-data-07e4b92.md)

***

### Models

-   Take care of destroying programmatically created models to prevent memory leaks.

-   Built-in framework models \(such as `ODataModel` or `JSONModel`\) and their related classes are considered *final*. They must not be modified or extended. For more information, see [Custom Model](../04_Essentials/custom-model-91f1c7e.md).


**OData V4 Model**

-   When using computed annotations, do **not** use global names; use `template:require` instead. For more information, see [XML Templating](../04_Essentials/xml-templating-5ee619f.md).

-   Don't use the [`synchronizationMode`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel%23constructor) as it's deprecated.


**OData V2 Model**

-   [`v2.ODataModel#createEntry`](https://ui5.sap.com/#/api/sap.ui.model.odata.v2.ODataModel%23methods/createEntry): Defining an array for the `mParameters.properties` is deprecated since OpenUI5 1.120. Pass the initial values as an object instead.

-   [`v2.ODataModel#refreshSecurityToken`](https://ui5.sap.com/#/api/sap.ui.model.odata.v2.ODataModel%23methods/refreshSecurityToken): Pass `true` for the `bAsync` parameter explicitly as its default value is `false`.


**JSON Model**

[`JSONModel#loadData`](https://ui5.sap.com/#/api/sap.ui.model.json.JSONModel%23methods/loadData): Do **not** pass `false` to the `bAsync` and `bCache` parameters, which are deprecated.

**Additional Information:**

-   [Meta Model for OData V4](../04_Essentials/meta-model-for-odata-v4-7f29fb3.md)
-   OData V2 Model: [Creating Entities](../04_Essentials/odata-v2-model-6c47b2b.md#loio4c4cd99af9b14e08bb72470cc7cabff4)

***

### Strict Error Handling

Implement strict error handling to address critical issues.

-   Ensure that the minimum log level includes warnings \(e.g. `sap-ui-log-level=WARNING`\).

-   Starting with OpenUI5 1.120.2, check for `[FUTURE FATAL]` log messages in the browser dev console.

-   Starting with OpenUI5 1.121, use the experimental URL parameter `sap-ui-xx-future=true` to enforce throwing exceptions for fatal warnings and errors.

-   Starting with OpenUI5 2.0, critical findings will throw exceptions by default, requiring prior resolution.


***

<a name="loio28fcd55b04654977b63dacbee0552712__section_ctrldev"/>

## Control Development

***

### Control Rendering

-   Ensure a dependency on the renderer or embed it within the control class.

-   Use the rendering `apiVersion 2` or `apiVersion 4`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.core.RenderManager%23overview).

-   When utilizing [`RenderManager#icon`](https://ui5.sap.com/#/api/sap.ui.core.RenderManager%23methods/icon) during rendering, include a dependency to `sap/ui/core/IconPool` in your code.

-   Don't rely on [`rerender`](https://ui5.sap.com/#/api/sap.ui.core.Control%23methods/rerender) as it is deprecated.

-   Avoid overriding `invalidate` for unintended purposes. Custom logic before or after rendering should be implemented in `onBeforeRendering` or `onAfterRendering`. The actual rendering should be implemented in the `render` function of the control's renderer.
-   Let the framework handle the invalidation instead of calling `invalidate` directly. It takes care of properly invalidating all affected controls, for example, when a managed control state changes via generated mutators or data binding.

**Additional Information:**

-   [`RenderManager`](https://ui5.sap.com/#/api/sap.ui.core.RenderManager)
-   [OpenUI5 Control Development Guidelines](../07_Developing_Controls/openui5-control-development-guidelines-4549da6.md)

***

<a name="loio28fcd55b04654977b63dacbee0552712__section_libdev"/>

## Library Development

***

### Library Dependency and Init

-   Don't use `sap.ui.getCore().initLibrary` to initialize the library as it's deprecated. Use the import of `sap/ui/core/Lib` and call its [`Lib.init()`](https://ui5.sap.com/#/api/sap.ui.core.Lib%23methods/sap.ui.core.Lib.init) instead.

-   Don't use the global namespace of the library to add types. Use the return value of `Lib.init` instead to add them.

-   Use the library `apiVersion 2`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.core.Lib%23methods/sap.ui.core.Lib.init).

-   Use [`sap.ui.base.DataType.registerEnum`](https://ui5.sap.com/#/api/sap.ui.base.DataType%23methods/sap.ui.base.DataType.registerEnum) to register enums that shall be usable as a type of control properties.

-   Define the `appData/manifest/i18n` section in the `.library` file or the `sap.app/i18n` section in the `manifest.json`, so that the framework can load resource bundles in advance.

-   Properly define library dependencies in all places where it is required. For more information, see [Dependencies to Libraries](../04_Essentials/descriptor-dependencies-to-libraries-and-components-8521ad1.md#loio8521ad1955f340f9a6207d615c88d7fd__section_DEPLIB).


**Additional Information:**

-   [The library.js File](../07_Developing_Controls/the-library-js-file-bd039ed.md)
-   [Defining Control Properties](../07_Developing_Controls/defining-control-properties-ac56d92.md)
-   [Manifest \(Descriptor for Applications, Components, and Libraries\)](../04_Essentials/manifest-descriptor-for-applications-components-and-libraries-be0cf40.md)

***

### Bundling

Prevent bundling modules \(`library-preload.js`\) into strings.

-   Leverage [UI5 Tooling](https://sap.github.io/ui5-tooling/) to build the bundle. Avoid generating the library bundle with legacy build tooling, such as grunt-openui5.

-   Avoid declaring `var`, `let`, or `const` in the global scope above `sap.ui.define`.

-   For third-party libraries, set `requiresTopLevelScope="false"` to the `/library/appData/packaging/raw-module` tag within the `.library` file, **provided that** the third-party library is allowed to be bundled together and does not require access to the global scope. Otherwise, consider [excluding the third-party library from the bundle](https://sap.github.io/ui5-tooling/v3/pages/Configuration/#excludes_1).


***

<a name="loio28fcd55b04654977b63dacbee0552712__section_tst"/>

## Testing

-   When replacing deprecated APIs with their successors, additional care has to be taken in the test code. Sometimes, deprecated APIs have been handled via spies or stubs in tests. As the OpenUI5 framework also replaces calls to deprecated APIs, such **stubs or spies might no longer achieve what they're expected to achieve**. As creating spies or stubs usually involves a different syntax than that for normal calls, alternative search patterns might be required to identify such spies or stubs

-   OpenUI5 entities that have previously been looked up via their global name \(controls, controllers, components\) are now looked up as modules.

    -   If tests create implementations of such entities, they must be implemented in a way that a module lookup can find them: either as individual files or as embedded and named `sap.ui.define` statements.
    -   As modules can only be loaded and executed once, each test implementation must have a unique module name. The same name cannot be used multiple times as was the case with globals.

-   Migrate an existing QUnit and OPA test setup to the [Test Starter](../04_Essentials/test-starter-032be2c.md) concept.
-   Transform existing QUnit tests that are based on the outdated QUnit 1 version to using QUnit 2.
-   Do not rely on the outdated Blanket.js \(`qunit-coverage.js`\) anymore. As of OpenUI5 1.113, code coverage measurement via IstanbulJS \(`qunit-coverage-istanbul.js`\) is the recommended option. For more information, see [Code Coverage Measurement](../04_Essentials/code-coverage-measurement-7ef3242.md).

-   **[Don't Use Deprecated or Experimental Features](don-t-use-deprecated-or-experimental-features-a8bd1a8.md "To keep your apps future proof and up to date with the latest improvements, you should
		only use artifacts (such as features, APIs, themes, etc.) that are still actively
		developed.")**  
To keep your apps future proof and up to date with the latest improvements, you should only use artifacts \(such as features, APIs, themes, etc.\) that are still actively developed.
-   **[Load Only What You Really Need](load-only-what-you-really-need-e8fca3e.md "The amount of resources and data that your app loads will directly affect the performance of your app. You should declare all dependencies
		and remove unused libraries and classes from your code.")**  
The amount of resources and data that your app loads will directly affect the performance of your app. You should declare all dependencies and remove unused libraries and classes from your code.
-   **[Use the MVC Concept](use-the-mvc-concept-07afcf4.md "MVC (Model-View-Controller) is a concept for structuring your software. It makes it easier to maintain and to extend your
		apps.")**  
MVC \(Model-View-Controller\) is a concept for structuring your software. It makes it easier to maintain and to extend your apps.
-   **[Keep Your Views Short and Simple](keep-your-views-short-and-simple-b0d7db7.md "The view part of your app reflects what users can see and interact with. You should use a suitable set of UI controls that match your
		scenario and keep things simple.")**  
The view part of your app reflects what users can see and interact with. You should use a suitable set of UI controls that match your scenario and keep things simple.
-   **[Use Stable IDs](use-stable-ids-79e910e.md "If you keep the IDs of controls, elements, and components stable, you can be sure that other OpenUI5 features will be able to identify them correctly during
		processing.")**  
If you keep the IDs of controls, elements, and components stable, you can be sure that other OpenUI5 features will be able to identify them correctly during processing.
-   **[Make Your App CSP Compliant](make-your-app-csp-compliant-1f81a09.md "CSP stands for Content Security Policy and is a security standard to prevent cross-site scripting or other code injection
		attacks.")**  
CSP stands for Content Security Policy and is a security standard to prevent cross-site scripting or other code injection attacks.
-   **[Use Asynchronous Loading](use-asynchronous-loading-676b636.md "Asynchronous loading is the way to go: It makes your applications a lot faster and, through that, better to use.")**  
Asynchronous loading is the way to go: It makes your applications a lot faster and, through that, better to use.
-   **[Use Only Public APIs](use-only-public-apis-b0d5fe2.md "OpenUI5 APIs are classified into different types. Only APIs of type
			public should be used by application developers.")**  
OpenUI5 APIs are classified into different types. Only APIs of type `public` should be used by application developers.
-   **[Is Your Application Ready for Asynchronous Loading?](is-your-application-ready-for-asynchronous-loading-493a15a.md "Find a collection of information that helps you to find out if your application is ready
		for asynchronous loading.")**  
Find a collection of information that helps you to find out if your application is ready for asynchronous loading.
-   **[Performance Checklist](performance-checklist-9c6400e.md "Follow these steps to apply performance best practices to your application.")**  
Follow these steps to apply performance best practices to your application.

