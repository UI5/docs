<!-- loio346599f0890d4dfaaa11c6b4ffa96312 -->

# Component Instantiation Guide

Components are the core building blocks of OpenUI5 applications. This guide explains the various ways to instantiate components, when to use each approach, and how to migrate from older mechanisms to modern alternatives.

**On this page:**

-   [Overview of Instantiation Mechanisms](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_OVW)
-   [Component Factories](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_COF)
-   [Choosing the Right Instantiation Mechanism](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_INM)
-   [Initial Components](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_INC) - How to create the main application component
-   [Nesting Components](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_NCP) - How to structure your app into smaller components and nesting them
-   [Migration Guidelines](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_MIG) - How to migrate your legacy code
-   [Best Practices](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_BPR)

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_OVW"/>

## Overview of Instantiation Mechanisms

OpenUI5 provides several mechanisms for component instantiation, each suited for different scenarios:

-   **`ComponentSupport` Module** - Declarative approach for initial application components
-   **Routing with Nested Components** - The routing definition allows for navigation-based creation and rendering of *nested* components
-   **`Component.create()` Factory Function** - Modern factory function; the recommended approach for programmatic component creation with full application control and responsibility. Needs a `ComponentContainer` to render.
-   **`Component#createComponent()` Factory Function** - Recommended approach to create a *reuse component* defined in an application component's `manifest.json`. Needs a `ComponentContainer` to render.
-   **`ComponentContainer`** - Container element for rendering components; can load and instantiate a component but also accepts any other programmatically created component, e.g. via `Component.create()` or `Component#createComponent`

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_COF"/>

## Component Factories

OpenUI5 provides two modern component factories:

-   **`Component.create()`**
-   **`Component#createComponent()`**

This section outlines the usage of the `Component.create()` API as it is the most flexible and versatile way to create a component instance. Keep in mind, however, that the full responsibility for component orchestration and rendering lies with the application.

1.  **`Component.create()`**

    The static `Component.create()` factory allows you to pass the name of a component, as well as some additional options like the URL for a `manifest.json`. The return value of this factory is a Promise that resolves with the final component instance once it is fully constructed.

    > ### Note:  
    > For more information on the manifest, see [Manifest First Function](manifest-descriptor-for-applications-components-and-libraries-be0cf40.md#loiobe0cf40f61184b358b5faedaec98b2da__manifirst).

    ```js
    // Basic factory call
    const oBasicComponent = await Component.create({
        name: "sap.my.component",
    });
    ```

    You can also pass a dedicated URL for the `manifest.json` to the factory function. In this case, the URL has to point to the `manifest.json` directly and must be resolved by the caller:

    ```js
    // Creating a Component with a manifest URL
    const oComponentWithManifestURL = await Component.create({
        name: "sap.my.component",
        manifest: "any/location/sap/my/component/manifest.json"
    });
    ```

2.  **`Component#createComponent()`**

    The `Component#createComponent()` factory is explained below in [Nesting Components](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_NCP).


***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_INM"/>

## Choosing the Right Instantiation Mechanism

The table below shows the recommended approach per scenario. We recommend initializing the first application component via the `ComponentSupport` in the initial HTML page. However, if needed, a component can also be created programmatically using the`Component.create()` factory method in combination with a `ComponentContainer`. All recommended approaches allow for an optimized manifest-first loading.


<table>
<tr>
<th valign="top">

Scenario

</th>
<th valign="top">

Recommended Approach

</th>
<th valign="top">

Reason

</th>
</tr>
<tr>
<td valign="top">

Initial application component

</td>
<td valign="top">

`ComponentSupport`

</td>
<td valign="top">

Declarative; internally creates a `ComponentContainer` and automatically loads the referenced component

</td>
</tr>
<tr>
<td valign="top">

Navigation-based component creation

</td>
<td valign="top">

Routing definition in `manifest.json`

</td>
<td valign="top">

Versatile declarative defintion of navigation targets; allows for seamless nesting of components. This approach is especially important when routing is used within nested components as it prevents conflicts that could otherwise arise when multiple components react to the same browser hash change.

</td>
</tr>
<tr>
<td valign="top">

Nested/reuse components

</td>
<td valign="top">

`ComponentContainer` with `usage`

</td>
<td valign="top">

Required for rendering a component; allows for automatic lifecycle management. Nested components can make use their own routing to create further nested components \(see navigation-based component creation\).

</td>
</tr>
<tr>
<td valign="top">

Programmatic *reuse* component creation

</td>
<td valign="top">

`Component#createComponent()`

</td>
<td valign="top">

Asynchronous factory; allows to manually orchestrate the loading of a nested reuse component defined in the respective component instance's `manifest.json` \(via `sap.ui5/componentUsages`\). The newly created component is automatically marked as owned by its parent component, which allows for additional manifest-driven extensions.

</td>
</tr>
<tr>
<td valign="top">

Programmatic component creation

</td>
<td valign="top">

`Component.create()`

</td>
<td valign="top">

Asynchronous factory; allows to manually orchestrate the loading

</td>
</tr>
</table>

> ### Caution:  
> Do not use deprecated legacy mechanisms! For the sake of completeness we also have to mention the deprecated `sap.ui.component()` synchronous factory function. **We strongly advise against using this factory function.**

The modern approaches offers several significant advantages:

-   **Asynchronous loading** prevents blocking the UI thread
-   **Manifest-first** loading optimizes dependency resolution and early model loading/creation
-   **Promise-based** API for manual orchestration and error handling
-   **Future-proof** as synchronous requests are deprecated by all major browsers and are no longer available in legacy-free variants of OpenUI5

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_INC"/>

## Initial Components

The following sections outline the recommended ways to instantiate the initial application component. For a detailed guide on how to create nested components and subdivide your application, see [Nesting Components](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_NCP).

***

### `ComponentSupport` - Declarative Approach

The `ComponentSupport` module enables declarative component instantiation directly in HTML, making it the recommended approach for initial application components.

**Good to know:**

-   **HTML is case-insensitive:** Properties and settings of a component are defined in camelCase. In HTML, you need to specify them with hyphens, e.g. `data-handle-validation` for `handleValidation`
-   **Automatic optimization:** The `ComponentSupport` enforces manifest-first loading and asynchronous behavior by default
-   **Lifecycle management:** By default, the lifecycle management is configured to be `Container` \(see [`sap.ui.core.ComponentLifecycle`](https://ui5.sap.com/#/api/sap.ui.core.ComponentLifecycle) and the section about `ComponentContainer`s below\)

For samples regarding the `ComponentSupport`, see [Declarative API for Initial Components](declarative-api-for-initial-components-82a0fce.md).

**Setup and Usage**

Enable `ComponentSupport` in your bootstrap:

```html
<!-- index.html -->
<script id="sap-ui-bootstrap"
    src="resources/sap-ui-core.js"
    data-sap-ui-on-init="module:sap/ui/core/ComponentSupport"
    data-sap-ui-async="true"
    data-sap-ui-resource-roots='{ "my.app": "./" }'
    data-...="...">
</script>
```

You now can declaratively define components directly in HTML using data attributes on a container DOM element \(in this sample a `<div>` element\):

```html
<!-- index.html -->
<body id="content" class="sapUiBody sapUiSizeCompact" role="application">
    <div data-sap-ui-component
        data-id="myRootComponentContainer"
        data-name="my.app"
        data-height="100%"
        data-settings='{ "id": "myRootComponent" }'
        data-handle-validation="true"
        data-...="...">
    </div>
</body>
```

For more information, see the [API Reference: `module:sap/ui/core/ComponentSupport`](https://ui5.sap.com/#/api/module:sap/ui/core/ComponentSupport).

**Advanced Usage**

For scenarios requiring a pre-initialization setup, you can use a dedicated `init` module and manually load the `ComponentSupport`. Once it is loaded, it automatically detects any declarative component definition in the HTML page's DOM \(see the sample above\).

```html
<script id="sap-ui-bootstrap"
    data-sap-ui-on-init="module:my/app/startupEfforts"
    ...>
</script>
```

```js
// my/app/startupEfforts.js
sap.ui.define(["my/app/MyModule"], (MyModule) => {
    "use strict";
    // Execute prerequisite code, e.g. loading additional application data, connecting to back-end services, etc.
    MyModule.init().then(() =>
        sap.ui.require(["sap/ui/core/ComponentSupport"])
    );
});
```

***

### `ComponentContainer` - Programmatic Approach

Sometimes it is necessary to programmatically create a component and render it in a specific part of the application and/or HTML page. For these use cases we provide a `ComponentContainer` control, which has a special `component` association that holds the reference to the component instance.

> ### Note:  
> You cannot use `placeAt()` directly on components - they must always be wrapped in a `ComponentContainer`.

`ComponentContainer`s provide:

-   **Lifecycle management:** Forwards lifecycle methods \(`onBeforeRendering`, `onAfterRendering`\) to its associated component
-   **Separation:** Decouples control tree and data binding between parent and child components. A component associated in a `ComponentContainer` has no parent control. The `Component#getParent()` function will return `null` even though the `ComponentContainer` itself is aggregated in the control tree.
-   **Model propagation:** Despite the above-mentioned strict separation, setting the `propagateModel` property to `true` forwards models and binding contexts to the associated component. By default, a component associated in a `ComponentContainer` does not take part in the model propagation process.
-   **Rendering context:** Provides the necessary wrapper for component rendering

**Using `ComponentContainer`s**

**Method 1: Container-managed component creation**

```js
// "ComponentContainer" required from module "sap/ui/core/ComponentContainer"
var oContainer = new ComponentContainer({
    name: "samples.components.sample",
    manifest: true
});
oContainer.placeAt("target");
```

**Method 2: Pre-created component association**

```js
// "Component" required from module "sap/ui/core/Component"
// "ComponentContainer" required from module "sap/ui/core/ComponentContainer"
Component.create({
    name: "samples.components.sample",
}).then(function(oComponent) {
    // Note: the Component instance (oComponent) is only associated in the ComponentContainer, not aggregated!
    var oContainer = new ComponentContainer({
        component: oComponent
    });
    oContainer.placeAt("target");
});
```

**Lifecycle Management**

The `ComponentContainer` allows you to define a `lifecycle` of a component and how it is coupled to the lifecylce of the container.For more information, see the [API Reference: `sap.ui.core.ComponentLifecycle`](https://ui5.sap.com/#/api/sap.ui.core.ComponentLifecycle).

> ### Note:  
> The default is `sap.ui.core.ComponentLifecycle.Legacy`.

```js
// "ComponentContainer" required from module "sap/ui/core/ComponentContainer"
// "coreLibrary" required from module "sap/ui/core/library"
var oContainer = new ComponentContainer({
    name: "samples.components.sample",
    lifecycle: coreLibrary.ComponentLifecycle.Container,
    manifest: true
});
```

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_NCP"/>

## Nesting Components

Nesting components enables you to subdivide your application into multiple smaller, independent parts, each with their own dedicated set of dependencies and resources. For example, consider a shop application that displays a list of products. The editing functionality must only be visible to administrators and thus does not need to be loaded and prepared for other users. Nested components allow you to decouple this functionality. This approach minimizes the initial payload required to start your main component, improving application startup performance and resource utilization.

There are several ways of nesting components into each other:

-   [Routing with Nested Components](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__RWNC) \(i.e. with targets of `Component` type\) - Recommended for most use cases; must be used when nested components have routing enabled. This approach is especially important when routing is used within nested components as it prevents conflicts that could otherwise arise when multiple components react to the same browser hash change.
-   [Programmatic Instantiation](component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__PI) \(i.e. via `componentUsage`\)

***

### Manifest Configuration

Before we can configure nested components via routing or instantiate them programmatically, we first need to declare them in the `sap.ui5/componentUsages` section of your parent component's `manifest.json`:

```json
{
    "sap.ui5": {
        "componentUsages": {
            "myreuse": {
                "name": "sap.reuse.component",
                "settings": {},
                "componentData": {},
                "lazy": false
            }
        }
    }
}
```

**Configuration Options:**

-   **`name`:** Component identifier \(mandatory\)
-   **`settings`:** Component-specific settings
-   **`componentData`:** Data passed to component's constructor
-   **`lazy`:** Controls preloading behavior \(`false` = preload, `true` = load on demand\)

***

### Routing With Nested Components

Nesting components with target-based navigation is the recommended way to achieve a separation of functionality and concerns. This approach is especially important when routing is used within nested components as it prevents conflicts that could otherwise arise when multiple components react to the same browser hash change.

Using routing with nested components requires:

-   **Asynchronous routing** enabled in all components
-   **Component target** configuration in parent routing
-   **Proper `componentUsages`** declaration

For more information, see [Enabling Routing in Nested Components](enabling-routing-in-nested-components-fb19f50.md).

**Routing Configuration \(`manifest.json`\):**

-   **`type: "Component"`:** Tells the framework's routing that we want to instantiate a component
-   **`usage`:** References the key from `componentUsages` in the `manifest.json`
-   **`options`:** Additional options for the component. This object is merged with the corresponding object from the `componentUsages` section of the `manifest.json`.
-   **`containerOptions`:** Additional options passed to the `ComponentContainer`'s constructor

> ### Note:  
> The routing configuration also provides a `"View"` target type.
> 
> When multiple components have their own routing configuration, their individual routers coordinate hash access to prevent conflicts. This allows for sub-routing and ensures deterministic navigation across the component hierarchy.
> 
> For more information, see [Routing Configuration](routing-configuration-9023130.md).

```json
{
    "sap.ui5": {
        "componentUsages": {
            "myreuse": {
                "name": "reuse.component",
                "lazy": false
            }
        },
        "routing": {
            "config": {
                "async": true
            },
            "routes": [{
                "name": "componentRoute",
                "pattern": "component",
                "target": "componentTarget"
            }],
            "targets": {
                "componentTarget": {
                    "type": "Component",
                    "usage": "myreuse",
                    "options": {
                        // Additional component options
                    },
                    "containerOptions": {
                        // ComponentContainer options
                    }
                }
            }
        }
    }
}
```

***

### Programmatic Instantiation

In certain scenarios, programmatic component instantiation is required, such as opening a dialog component when a user performs a specific action. The `Component` class provides a factory function to asynchronously create reuse components that are declared in the manifest. While this approach requires additional application code, it offers greater control and flexibility, allowing you to precisely orchestrate the loading and instantiation of nested components.

**Simplified usage:**

```js
const oComponent = await this.createComponent("myreuse");
```

**Extended usage:**

```js
const oComponent = await this.createComponent({
    usage: "myreuse",
    settings: {},
    componentData: {}
});
```

**Adding the component to the control tree:**

To add your newly created component into the control tree, you need to associate it with a `ComponentContainer`:

```js
// associate the component in a ComponentContainer
const oContainer = new ComponentContainer({
    component: oComponent
});
// and place it into the control tree
myView.addContent(oContainer);
```

**`ComponentContainer` with owner component:**

To add your newly created component into the control tree, you need to associate it with a `ComponentContainer`:

This approach **only works** if you ensure that the `ComponentContainer` is instantiated within the "owner scope" of the component defining the `componentUsage`. For more information, see [The Owner Component](the-owner-component-a7a3138.md).

For more information, see the `usage` options outlined in the [API Reference for `ComponentContainer`](https://ui5.sap.com/#/api/sap.ui.core.ComponentContainer%23controlProperties) and the [API Reference for `Component#runAsOwner`](https://ui5.sap.com/#/api/sap.ui.core.Component%23methods/runAsOwner) used in the example below.

```js
// Ensure that the ComponentContainer is created in the correct owner scope!
oMyAppComponent.runAsOwner(() => {
    const oContainer = new ComponentContainer({
        usage: "myreuse"
    })
    oContainer.placeAt("target");
})
```

***

### Declarative Usage in XML Views

To declaratively create a component from within an XML view, simply place it in the XML DOM:

```
<mvc:View xmlns:mvc="sap.ui.core.mvc" xmlns:core="sap.ui.core" ...>
    <core:ComponentContainer usage="myreuse" manifest="true" />
</mvc:View>
```

> ### Note:  
> Depending on how you create the XML view, you may need to ensure that the "Owner Scope" is correctly set. For more information, see [The Owner Component](the-owner-component-a7a3138.md).

If your view is created programmatically and not via a routing target, you need to wrap the view's factory call in a corresponding [`Component#runAsOwner`](https://ui5.sap.com/#/api/sap.ui.core.Component%23methods/runAsOwner) call:

```
oMyAppComponent.runAsOwner(() => {
    const oMyView = await XMLView.create(...);
    // add the view to the control tree
});
```

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_MIG"/>

## Migration Guidelines

The OpenUI5 framework is continuously evolving to leverage modern web standards and browser capabilities while maintaining backward compatibility. However, to ensure your applications remain performant, secure, and future-ready, migrating from legacy component APIs to modern alternatives is essential.

> ### Note:  
> For comprehensive guidance on modernizing your codebase, see [Best Practices for Developers](../03_Get-Started/best-practices-for-developers-28fcd55.md), which provides detailed recommendations for legacy-free OpenUI5 development.

***

### Legacy `sap.ui.component()` Factory

The legacy `sap.ui.component()` factory function creates components synchronously, which blocks the UI thread and violates Content Security Policy requirements, making migration to asynchronous alternatives essential for modern OpenUI5 development.

**Legacy approach:**

```js
createContent: function() {
    var oReuseComponent = sap.ui.component({
        "name": "sap.reuse.component"
    });
}
```

**Modern approach:**

```js
createContent: function() {
    var oReuseComponentPromise = this.createComponent({
        "usage": "reuse"
    });
}
```

***

### Legacy Component Dependencies

**Legacy definition in manifest.json:**

```json
{
    "sap.ui5": {
        "dependencies": {
            "components": {
                "sap.reuse.component": {}
            }
        }
    }
}
```

**Modern definition in manifest.json:**

```json
{
    "sap.ui5": {
        "componentUsages": {
            "reuse": {
                "name": "sap.reuse.component",
                "lazy": false
            }
        }
    }
}
```

***

<a name="loio346599f0890d4dfaaa11c6b4ffa96312__section_BPR"/>

## Best Practices

1.  **Always use asynchronous APIs**, i.e. `Component.create()` instead of `sap.ui.component()`
2.  **Prefer `ComponentSupport`** for initial components over manual `ComponentContainer` creation
3.  **Declare reuse components** in `componentUsages` rather than in `dependencies`
4.  **Enable async routing** in all components when using nested component routing
5.  **Use routing with nested components** for nested components that define their own routing
6.  **Use proper lifecycle management** via the `ComponentContainer`'s `lifecycle` property
7.  **Leverage manifest-first** loading for optimal performance

**Related Information**  


[Declarative API for Initial Components](declarative-api-for-initial-components-82a0fce.md "The declarative API enables you to define the initially started component directly in the HTML markup.")

[Enabling Routing in Nested Components](enabling-routing-in-nested-components-fb19f50.md "Every OpenUI5 component can define routing configuration in its manifest and a UI5 router instance will be created automatically after the component is instantiated.")

[Descriptor Dependencies to Libraries and Components](descriptor-dependencies-to-libraries-and-components-8521ad1.md "Description of the performance-relevant attributes that are available for the descriptor for applications, components and libraries")

[The Owner Component](the-owner-component-a7a3138.md "If you wish to extend your view or controller, you must define the extension in the manifest.json of their owner component.")

[API Reference: `sap.ui.core.Component`](https://ui5.sap.com/#/api/sap.ui.core.Component)

[API Reference: `sap.ui.core.ComponentContainer`](https://ui5.sap.com/#/api/sap.ui.core.ComponentContainer)

[API Reference: `ComponentSupport`](https://ui5.sap.com/#/api/module:sap/ui/core/ComponentSupport)

