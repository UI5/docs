<!-- loio9bbbfaa828a14fee8ca9ac31464cc073 -->

# Step 15: Nested Views \(TypeScript\)

Our panel content is getting more and more complex and now it is time to move the panel content to a separate view. With that approach, the application structure is much easier to understand, and the individual parts of the app can be reused.

***

## Preview

  
  
**The panel content is now refactored to a separate view \(No visual changes to last step\)**

![The graphic has an explanatory text.](images/loiof3724d2f97e94a78b27d8ab01ff9c37d_LowRes.png "The panel content is now refactored to a separate view (No visual changes to last
               step)")

***

<a name="loio9bbbfaa828a14fee8ca9ac31464cc073__section_rjd_vt2_syb"/>

## Coding

You can view all files at [OpenUI5 TypeScript Walkthrough - Step 15: Nested Views](https://github.com/sap-samples/ui5-typescript-walkthrough/tree/main/steps/15) and [download the solution as a zip file](https://sap-samples.github.io/ui5-typescript-walkthrough/ui5-typescript-walkthrough-step-15.zip).

***

<a name="loio9bbbfaa828a14fee8ca9ac31464cc073__section_xkd_njy_nzb"/>

## webapp/controller/HelloPanel.controller.ts \(New\)

In our `webapp/controller` folder we create a new `HelloPanel.controller.ts` file and move the `onShowHello` method from the app controller to it, so we get a reusable asset.

```js
import Controller from "sap/ui/core/mvc/Controller";
import MessageToast from "sap/m/MessageToast";
import JSONModel from "sap/ui/model/json/JSONModel";
import ResourceModel from "sap/ui/model/resource/ResourceModel";
import ResourceBundle from "sap/base/i18n/ResourceBundle";

/**
 * @namespace ui5.walkthrough.controller
 */
export default class HelloPanel extends Controller {
    
    onShowHello(): void {
        // read msg from i18n model
        // functions with generic return values require casting 
        const resourceBundle = (this.getView()?.getModel("i18n") as ResourceModel)?.getResourceBundle() as ResourceBundle;
        const recipient = (this.getView()?.getModel() as JSONModel)?.getProperty("/recipient/name");
        const msg = resourceBundle.getText("helloMsg", [recipient]) || "no text defined";
        // show message
        MessageToast.show(msg);
    }
};
```

***

<a name="loio9bbbfaa828a14fee8ca9ac31464cc073__section_hfz_fky_nzb"/>

## webapp/view/HelloPanel.view.xml \(New\)

We create a new `HelloPanel.view.xml` file in our `webapp/view` folder and move the whole panel from the app view to it. We also reference the controller we just created for the view by setting it to the `controllerName` attribute of the XML view.

```xml
<mvc:View
   controllerName="ui5.walkthrough.controller.HelloPanel"
   xmlns="sap.m"
   xmlns:mvc="sap.ui.core.mvc">
   <Panel
      headerText="{i18n>helloPanelTitle}"
      class="sapUiResponsiveMargin"
      width="auto">
      <content>
         <Button
            text="{i18n>showHelloButtonText}"
            press=".onShowHello"
            class="myCustomButton"/>
         <Input
            value="{/recipient/name}"
            valueLiveUpdate="true"
            width="60%"/>
         <FormattedText
            htmlText="Hello {/recipient/name}"
            class="sapUiSmallMargin sapThemeHighlight-asColor myCustomText"/>
      </content>
   </Panel>
</mvc:View>
```

***

<a name="loio9bbbfaa828a14fee8ca9ac31464cc073__section_sjd_vt2_syb"/>

## webapp/view/App.view.xml

In the app view, we remove the panel control and its content and put the `XMLView` control into the content of the page instead. We add the `viewName` attribute with the value `ui5.walkthrough.view.HelloPanel` to reference the new view that now contains the panel.

```xml
<mvc:View
	controllerName="ui5.walkthrough.controller.App"
	xmlns="sap.m"
	xmlns:mvc="sap.ui.core.mvc"
	displayBlock="true">
	<Shell>
		<App class="myAppDemoWT">
			<pages>
				<Page title="{i18n>homePageTitle}">
					<content>
						<mvc:XMLView viewName="ui5.walkthrough.view.HelloPanel"/>
					</content>
				</Page>
			</pages>
		</App>
	</Shell>
</mvc:View>
```

***

## webapp/controller/App.controller.ts

We remove the `onShowHello` method from the app controller, as this is not needed anymore.

```js
import Controller from "sap/ui/core/mvc/Controller";

/**
 * @namespace ui5.walkthrough.controller
 */
export default class App extends Controller {
};
```

We have now moved everything out of the app view and controller. The app controller remains an empty stub for now, we will use it later to add more functionality.

**Parent topic:**[Walkthrough Tutorial \(TypeScript\)](walkthrough-tutorial-typescript-dad1905.md "In this tutorial we'll introduce you to all major development paradigms of OpenUI5. We'll demonstrate the use of TypeScript with OpenUI5 and highlight the specific characteristics of this approach.")

**Next:**[Step 14: Custom CSS and Theme Colors \(TypeScript\)](step-14-custom-css-and-theme-colors-typescript-4cc841e.md "Sometimes we need to define some more fine-granular layouts and this is when we can use the flexibility of CSS by adding custom style classes to controls and style them as we like.")

**Previous:**[Step 16: Dialogs and Fragments \(TypeScript\)](step-16-dialogs-and-fragments-typescript-4b2e306.md "In this step, we will take a closer look at another element which can be used to assemble views: the fragment.")

**Related Information**  


[API Reference: `sap.ui.core.mvc.XMLView`](https://ui5.sap.com/#/api/sap.ui.core.mvc.XMLView%23controlProperties)

