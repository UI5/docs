<!-- loioa264a9abf98d4caabbf9b027bc1005d8 -->

# Extending Apps

This section provides a comprehensive overview of OpenUI5's core extension mechanisms, covering single-level, multi-level, and adaptation approaches for customizing applications.

***

Each concept is explained in more detail, with coding samples, in the topics linked below.

> ### Note:  
> The extension mechanisms listed below are **not** mutually exclusive. For example, you can use view extensions via extension points alongside modern controller extensions.

***

## Configuration in the `manifest.json`

The basic OpenUI5 extension approach works through a `Component`'s `manifest.json` file and offers several ways to customize applications. You can merge custom and standard controllers through **controller extensions**, add custom content to existing views via **extension points**, which let you hook into pre-defined locations provided by the original application. For smaller changes, **view modifications** allow you to change specific control properties; this is particularly useful for hiding or showing elements by toggling the `visible` property. When the existing views or controllers don't quite fit your application's needs, or cannot be easily extended, **view replacements** or **controller replacements** can completely substitute the standard implementations.

For more information, see [Configuration in the manifest.json](configuration-in-the-manifest-json-c264d66.md).

***

## Extension Points

Extension points are pre-defined locations within views that let you insert custom content without modifying the original view structure. They're particularly useful for adding new UI sections to SAP-delivered applications, especially in SAP Fiori elements scenarios. Extension points provide a clean separation between standard and custom content, making your extensions maintainable across application updates.

For more information, see [Extension Points](extension-points-403c050.md).

***

## Controller Extensions

Controller extensions are among the most common and versatile extension mechanisms OpenUI5 offers, allowing you to enhance existing controller functionality without replacing the entire controller. You can configure controller extensions in two different ways:

-   **Simple object mixins:** Applied directly to an existing controller through the `manifest.json` configuration
-   **Class-based extensions:** Using the specialized `sap.ui.core.mvc.ControllerExtension` class for more advanced scenarios


The simple object-based approach supports single-layer extensions, which means that once a controller has been extended, it cannot be extended again. However, the `sap.ui.core.mvc.ControllerExtension` class enables multiple layers of controller extensions, allowing for more complex customization scenarios, such as for applications that need to be extended multiple times.

For more information, see [Controller Extensions](controller-extensions-21515f0.md).

***

## Further Extension Methods

***

### View Modification

View modifications let you change specific properties of controls in standard views without altering the original source code. They are currently restricted to the `visible` property for showing or hiding UI elements in your custom application.

For more information, see [View Modification](view-modification-aa93e1c.md).

***

### View Replacement

View replacements provide a complete substitution of existing views with custom implementations, providing maximum flexibility whenever extension points and view modifications aren't sufficient. This approach gives you full control over the UI structure and behavior for radical UI changes. Be careful, however, to use view replacements judiciously, as they require more maintenance effort when the base application is updated.

For more information, see [View Replacement](view-replacement-98861cf.md).

***

### Controller Replacement

Controller replacements provide a complete substitution of existing controllers with custom implementations, giving you full control over controller logic and lifecycle methods. Use this approach whenever controller extensions aren't sufficient and you need fundamental changes to you controller's behavior. Controller replacements are particularly useful for typed controllers that require the `extend` syntax or when you need complete control over your method execution order.

For more information, see [Controller Replacement](controller-replacement-b0b14bf.md).

-   **[Core Mechanisms for Extending Apps](core-mechanisms-for-extending-apps-7ac7f75.md "")**  

-   **[Providing Hooks in the Standard Controller](providing-hooks-in-the-standard-controller-8fbf4e7.md "Hooks are extension points in the controller code that are used to make controller
		extensions more stable.")**  
Hooks are extension points in the controller code that are used to make controller extensions more stable.
-   **[Extension Stability Across Application Updates](extension-stability-across-application-updates-aef3384.md "When extending OpenUI5 applications, it's essential to understand the
		compatibility implications that come with application updates.")**  
When extending OpenUI5 applications, it's essential to understand the compatibility implications that come with application updates.

