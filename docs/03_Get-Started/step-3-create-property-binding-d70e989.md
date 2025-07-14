<!-- loiod70e9894c09b4c27a98d4850d4e90f2c -->

# Step 3: Create Property Binding

Although there is no visible difference, the text on the screen is now derived from model data.

***

## Preview

![The browser shows the text "Hi, my name is Harry Hawk"](images/loio6d391d527601499fbeb3734246b2c067_LowRes.png)

***

## Coding

You can view and download all files in the Demo Kit at [Data Binding - Step 3](https://ui5.sap.com/#/entity/sap.ui.core.tutorial.databinding/sample/sap.ui.core.tutorial.databinding.03).

Assign the `text` property of the `sap.m.Text` control to the value `{/greetingText}`. The curly brackets enclosing a binding path \(binding syntax\) are automatically interpreted as a binding. These binding instances are called property bindings. In this scenario, the control's `text` property is bound to the `greetingText` property at the root of the default model. The slash \(`/`\) at the beginning of the binding path signifies an absolute binding path.

**webapp/view/App.view.xml**

```
<mvc:View
	xmlns="sap.m"
	xmlns:mvc="sap.ui.core.mvc">
	<Text text="{/greetingText}"/>
</mvc:View>
```

**Parent topic:**[Data Binding Tutorial](data-binding-tutorial-e531093.md "In this tutorial, we explain the concepts of data binding in OpenUI5.")

**Next:**[Step 2: Creating a Model](step-2-creating-a-model-5278bfd.md "In this step, we create a model. It serves as a container for the data your application operates on.")

**Previous:**[Step 4: Two-Way Data Binding](step-4-two-way-data-binding-c72b922.md "In the examples we've looked at so far, we've displayed the value of a model property using a read-only field. We'll now change the user interface to display first and last name fields using sap.m.Input fields. We're also adding a check box control to enable or disable both input fields. This setup illustrates a feature known as &quot;two-way data binding&quot;. As the view now contains more controls, we're also moving the view definition into an XML file.")

**Related Information**  


[Binding Types](../04_Essentials/binding-types-91f0d8a.md "Depending on the different use cases, you can use different binding types: Propety binding, context binding, and list binding.")

[Property Binding](../04_Essentials/property-binding-91f0652.md "With property binding, you can initialize properties of a control automatically and update them based on the data of the model.")

