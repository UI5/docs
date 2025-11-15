<!-- loio2edc3f99883e4a068f040d9e844f14fa -->

# Text Customization

When extending OpenUI5 applications, you often need to add custom localized texts or override existing ones. OpenUI5 provides flexible mechanisms for enhancing resource models with additional localization files, allowing you to integrate multilingual content.

You have two options for extending localized texts:

1.  Use the `enhanceWith` setting of a resource model in the `manifest.json`.

2.  Implement a programmatic extension by manually enhancing a resource model.

The enhanced resource model follows a fallback chain: It first tries to resolve localized texts from your custom resource bundle. If a text key isn't found, it falls back to the original application's resource bundle. This approach ensures that your extensions can both add new translations and override existing ones.

***

## Using the `enhanceWith` Setting

The recommended approach is to configure resource model enhancements declaratively in your `manifest.json` file:

```
{
  "sap.ui5": {
    "models": {
      "i18n": {
        "type": "sap.ui.model.resource.ResourceModel",
        "settings": {
          "bundleName": "my.extended.app.i18n.i18n",
          "async": true,
          "supportedLocales": ["en", "de", "fr"],
          "fallbackLocale": "en",
          "enhanceWith": [
            {
              "bundleName": "my.extension.i18n.i18n",
              "bundleUrlRelativeTo": "manifest"
            }
          ]
        }
      }
    }
  }
}
```

***

## Programmatic Enhancement in Controller Extensions

When declarative configuration isn't sufficient, you can programmatically enhance resource models, e.g. within your controller extensions. Here's the modern way to implement this pattern:

**`Extension.controller.js`** \(JavaScript\):

```js
sap.ui.define([
  "sap/ui/core/mvc/ControllerExtension",
  "sap/ui/model/resource/ResourceModel"
], (ControllerExtension, ResourceModel) => {
  "use strict";

  return ControllerExtension.extend("my.extension.controller.Extension", {
    override: {
      onInit() {
        // Call the original onInit method
        this.base.onInit.apply(this, arguments);

        // Create and enhance the resource model
        this._setupLocalizedTexts();
      }
    },

    _setupLocalizedTexts() {
      // Create a new resource model.
      // Note: The model is created in async mode, any bindings to the i18n model will be updated once the correspondin bundle is loaded
      const oResourceModel = new ResourceModel({
        bundleName: "my.original.app.i18n.i18n",
        async: true,
        supportedLocales: ["en", "de", "fr", "..."],
        fallbackLocale: "en"
      });

      // Enhance with custom localization
      // Note: The enhance() API behaves asynchronously for models that have been created with "async: true"
      oResourceModel.enhance({
        bundleName: "my.extension.i18n.i18n"
      });

      this.getView().setModel(oResourceModel, "i18n");
    }
  });
});
```

**`Extension.controller.ts`** \(TypeScript equivalent\):

```js
import ControllerExtension from "sap/ui/core/mvc/ControllerExtension";
import ResourceModel from "sap/ui/model/resource/ResourceModel";

/**
 * @namespace my.extension.controller
 */
export default class Extension extends ControllerExtension {

  static readonly overrides = {
    onInit: function(this: Extension) {
      // Call the original onInit method
      this.base.onInit.apply(this, arguments);

      // Create and enhance the resource model
      this._setupLocalizedTexts();
    }
  };

  private _setupLocalizedTexts(): void {
    // Create a new resource model.
    // Note: The model is created in async mode, any bindings to the i18n model will be updated once the corresponding bundle is loaded
    const resourceModel = new ResourceModel({
      bundleName: "my.original.app.i18n.i18n",
      async: true,
      supportedLocales: ["en", "de", "fr", "..."],
      fallbackLocale: "en"
    });

    // Enhance with custom localization
    // Note: The enhance() API behaves asynchronously for models that have been created with "async: true"
    resourceModel.enhance({
      bundleName: "my.extension.i18n.i18n"
    });

    this.getView().setModel(resourceModel, "i18n");
  }
}
```

***

## Best Practices

When implementing localized texts for extended apps, follow these contemporary guidelines:

1.  **Use async loading:** Always set `async: true` when creating `ResourceModel`s to avoid blocking the UI thread.
2.  **Specify supported locales:** Define `supportedLocales` and a `fallbackLocale`.
3.  **Leverage manifest configuration:** Prefer a declarative model configuration in your `manifest.json` over programmatic instantiation. The component itself then takes care of correctly instantiating the models.
4.  **Implement proper fallback chains:** Ensure your extensions gracefully handle missing translations by falling back to base application texts.

**Related Information**  


[Terminologies](../04_Essentials/terminologies-eba8d25.md "By defining terminologies together with additional resource bundles, an application can easily be switched from one scenario or industry to another.")

