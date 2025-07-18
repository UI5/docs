<!-- loiod935dbf196d34997bf1ac42ac3e81579 -->

# Step 36: Content Density

In this step of our Walkthrough tutorial, we adjust the content density based on the user's device. OpenUI5 contains different content densities allowing you to display larger controls for touch-enabled devices and a smaller, more compact design for devices that are operated by mouse. In our app, we will detect the device and adjust the density accordingly.

***

## Preview

  
  
**The content density is compact on desktop devices and cozy on touch-enabled devices**

![The graphic has an explanatory text.](images/loiof216b131c492448d8a1df25db2b9a26d_LowRes.png "The content density is compact on desktop devices and cozy on touch-enabled
					devices")

***

## Coding

You can view and download all files at [Walkthrough - Step 36](https://ui5.sap.com/#/entity/sap.m.tutorial.walkthrough/sample/sap.m.tutorial.walkthrough.36).

***

## webapp/Component.js

```js
...

		getContentDensityClass() {
			return Device.support.touch ? "sapUiSizeCozy" : "sapUiSizeCompact";
		}
	});
});
```

To prepare the content density feature we will also add a helper method `getContentDensityClass`. OpenUI5 controls can be displayed in multiple sizes, for example in a `compact` size that is optimized for desktop and non-touch devices, and in a `cozy` mode that is optimized for touch interaction. The controls look for a specific CSS class in the HTML structure of the application to adjust their size.

This helper method queries the `Device` API directly for touch support of the client and returns the CSS class `sapUiSizeCompact` if touch interaction is not supported and `sapUiSizeCozy` for all other cases. We will use it throughout the application coding to set the proper content density CSS class.

***

## webapp/controller/App.controller.js

```js
sap.ui.define([
	"sap/ui/core/mvc/Controller"
], (Controller) => {
	"use strict";

	return Controller.extend("ui5.walkthrough.controller.App", {

		onInit() {
			this.getView().addStyleClass(this.getOwnerComponent().getContentDensityClass());
		}
	});
});
```

We add an `onInit` method to the app controller that is called when the app view is instantiated. There, we query the helper function that we defined on the app component in order to set the corresponding style class on the app view. All controls inside the app view will now automatically adjust to either the compact or the cozy size, as defined by the style.

***

## webapp/manifest.json

```json
...
  "sap.ui5": {
    ...  
    },
    "contentDensities": {
      "compact": true,
      "cozy": true
    }
    ...
  }
```

In the `contentDensities` section of the `sap.ui5` namespace, we have to specify the modes that the application supports. Containers like the SAP Fiori launchpad allow switching the content density based on these settings.

As we have just enabled the app to run in both modes depending on the devices capabilities, we can set both to `true` in the application descriptor.

**Parent topic:**[Walkthrough Tutorial \(JavaScript\)](walkthrough-tutorial-javascript-3da5f4b.md "In this tutorial we will introduce you to all major development paradigms of OpenUI5.")

**Next:**[Step 35: Device Adaptation](step-35-device-adaptation-d63a15e.md "We now configure the visibility and properties of controls based on the device that we run the application on. By making use of the sap.ui.Device API and defining a device model we will make the app look great on many devices.")

**Previous:**[Step 37: Accessibility](step-37-accessibility-ff7cab1.md "In this step we're going to improve the accessibility of our app.")

**Related Information**  


[Content Densities](../04_Essentials/content-densities-e54f729.md "The devices used to run apps that are developed with OpenUI5 run on various different operating systems and have very different screen sizes. OpenUI5 contains different content densities for certain controls that allow your app to adapt to the device in question, allowing you to display larger controls for touch-enabled devices and a smaller, more compact design for devices that are operated by mouse.")

[API Reference: `sap.ui.Device`](https://ui5.sap.com/#/api/sap.ui.Device)

