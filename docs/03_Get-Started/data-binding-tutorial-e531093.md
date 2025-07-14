<!-- loioe5310932a71f42daa41f3a6143efca9c -->

# Data Binding Tutorial

In this tutorial, we explain the concepts of data binding in OpenUI5.

Data binding is used to bind UI elements to data sources. This keeps the data in sync and allows data editing on the UI.

For data binding, you need a model and a binding instance: The model holds the data and provides methods to set the data or retrieve it from a server. It also provides a method for creating bindings to the data. When you call this method, a binding instance is created, which contains the binding information and provides an event, which is fired whenever the bound data changes. An element can listen to this event and update its visualization according to the new data.

The UI uses data binding to bind controls to the model which holds the application data, so that the controls are updated automatically whenever application data changes. Data binding is also used in reverse, when changes in the control, for example data entered by the user, cause updates in the underlying application data. This is called two-way binding.

***

## Preview

![Preview of three panels of the UI5 application that is going to be built in this tutorial. Contains three panels with name input fields, address details, and a product list.](images/loio896048ebce6b47488068c9630b71c43a_LowRes.png)

> ### Tip:  
> You don't have to do all tutorial steps in order; you can jump directly to any step you want. Just download the code from the previous step, copy it to your workspace, and ensure that the application runs by calling the `webapp/index.html` file.
> 
> You can view and download the files for all steps in the Demo Kit at [Data Binding](https://ui5.sap.com/#/entity/sap.ui.core.tutorial.databinding). Depending on your development environment you might need to adjust resource paths and configuration entries.
> 
> For more information check the [Downloading Code for a Tutorial Step](get-started-setup-tutorials-and-demo-apps-8b49fc1.md#loio8b49fc198bf04b2d9800fc37fecbb218__tutorials_download) section of the tutorials overview page [Get Started: Setup, Tutorials, and Demo Apps](get-started-setup-tutorials-and-demo-apps-8b49fc1.md).

1.  [Step 1: No Data Binding](step-1-no-data-binding-4cde849.md "In this step, we create a basic application and simply place some text on the screen using a standard sap.m.Text control.
		The text in this control is a hard-coded part of the control's definition; therefore, this is not an example of data binding!")  
In this step, we create a basic application and simply place some text on the screen using a standard `sap.m.Text` control. The text in this control is a hard-coded part of the control's definition; therefore, this is not an example of data binding!
2.  [Step 2: Creating a Model](step-2-creating-a-model-5278bfd.md "In this step, we create a model. It serves as a container for the data your application operates on.")  
In this step, we create a model. It serves as a container for the data your application operates on.
3.  [Step 3: Create Property Binding](step-3-create-property-binding-d70e989.md "Although there is no visible difference, the text on the screen is now derived from
		model data.")  
Although there is no visible difference, the text on the screen is now derived from model data.
4.  [Step 4: Two-Way Data Binding](step-4-two-way-data-binding-c72b922.md "In the examples we've looked at so far, we've displayed the value of a model property using a read-only field. We'll now change the user
		interface to display first and last name fields using sap.m.Input fields. We're also adding a check box control to enable or
		disable both input fields. This setup illustrates a feature known as &quot;two-way data binding&quot;. As the view now contains more controls, we're
		also moving the view definition into an XML file.")  
In the examples we've looked at so far, we've displayed the value of a model property using a read-only field. We'll now change the user interface to display first and last name fields using `sap.m.Input` fields. We're also adding a check box control to enable or disable both input fields. This setup illustrates a feature known as "two-way data binding". As the view now contains more controls, we're also moving the view definition into an XML file.
5.  [Step 5: One-Way Data Binding](step-5-one-way-data-binding-88756c0.md "Unlike the two-way binding behavior we've seen, one-way data binding is also possible. In this case, data travels in one direction only:
		from the model, through the binding instance, to the consumer (usually the property of a control), but never in the other direction. Let's
		modify the previous example to use one-way data binding. This shows how you can switch off the flow of data from the user interface back to
		the model if needed.")  
Unlike the two-way binding behavior we've seen, one-way data binding is also possible. In this case, data travels in one direction only: from the model, through the binding instance, to the consumer \(usually the property of a control\), but never in the other direction. Let's modify the previous example to use one-way data binding. This shows how you can switch off the flow of data from the user interface back to the model if needed.
6.  [Step 6: Resource Models](step-6-resource-models-9790d9a.md "Business applications often require language-specific (translatable) text used as labels and descriptions on the user
		interface.")  
Business applications often require language-specific \(translatable\) text used as labels and descriptions on the user interface.
7.  [Step 7: \(Optional\) Resource Bundles and Multiple Languages](step-7-optional-resource-bundles-and-multiple-languages-4e593b4.md "Resource bundles exist to enable an app to run in multiple languages without the need to change any code. To demonstrate this feature,
		let's create a German version of the app – in fact, all we need to do is create a German version of the resource bundle file. In our code, we
		activate the German locale for the ResourceModel.")  
Resource bundles exist to enable an app to run in multiple languages without the need to change any code. To demonstrate this feature, let's create a German version of the app – in fact, all we need to do is create a German version of the resource bundle file. In our code, we activate the German locale for the ResourceModel.
8.  [Step 8: Binding Paths: Accessing Properties in Hierarchically Structured Models](step-8-binding-paths-accessing-properties-in-hierarchically-structured-models-9373793.md "In Step 6 , we stated that the fields in a resource model are arranged in a flat structure; in other words, there is no hierarchy of
		properties. However, this is only true for resource models. The properties within JSON and OData models are usually arranged in a hierarchical
		structure. So, let's explore how to reference fields in a hierarchically structured model object.")  
In Step 6 , we stated that the fields in a resource model are arranged in a flat structure; in other words, there is no hierarchy of properties. However, this is only true for resource models. The properties within JSON and OData models are usually arranged in a hierarchical structure. So, let's explore how to reference fields in a hierarchically structured model object.
9.  [Step 9: Formatting Values](step-9-formatting-values-6fdf0ac.md "We'd also like to provide our users with a way of contacting Harry Hawk, so we're adding a link that sends an e-mail to Harry. To do this,
		we convert our data in the model to match the sap.m.URLHelper.normalizeEmail API. As soon as the user changes the name, the
		e-mail also changes. We need a custom formatter function for this.")  
We'd also like to provide our users with a way of contacting Harry Hawk, so we're adding a link that sends an e-mail to Harry. To do this, we convert our data in the model to match the `sap.m.URLHelper.normalizeEmail` API. As soon as the user changes the name, the e-mail also changes. We need a custom formatter function for this.
10. [Step 10: Property Formatting Using Data Types](step-10-property-formatting-using-data-types-9252ee4.md "OpenUI5 offers a set of simple data types, including Boolean,
			Currency, Date and Float. You can apply these data types to controls to ensure that the
		value displayed on the screen is formatted correctly. If the field is open for input, this also ensures that the user input meets the
		requirements of that data type. Let's add a new field called Sales Amount of type Currency. ")  
OpenUI5 offers a set of simple data types, including `Boolean`, `Currency`, `Date` and `Float`. You can apply these data types to controls to ensure that the value displayed on the screen is formatted correctly. If the field is open for input, this also ensures that the user input meets the requirements of that data type. Let's add a new field called *Sales Amount* of type `Currency`.
11. [Step 11: Validation Using sap/ui/core/Messaging](step-11-validation-using-sap-ui-core-messaging-b8c4e53.md "Up to this point, we've created a currency field that formats itself correctly. The currency data type can also validate user
		input to ensure it meets currency requirements. However, OpenUI5 manages data type
		validation functions and doesn't have a built-in mechanism for reporting error messages back to the UI. We therefore need a way to report
		error messages from validation functions back to the user. In this step, we're enabling validation for the entire app with a feature known as
		&quot;Messaging&quot;. Once this is set up, any validation error messages based on user input get passed to Messaging, which then
		connects them to the appropriate view and control that caused the error.")  
Up to this point, we've created a currency field that formats itself correctly. The *currency* data type can also validate user input to ensure it meets currency requirements. However, OpenUI5 manages data type validation functions and doesn't have a built-in mechanism for reporting error messages back to the UI. We therefore need a way to report error messages from validation functions back to the user. In this step, we're enabling validation for the entire app with a feature known as "Messaging". Once this is set up, any validation error messages based on user input get passed to `Messaging`, which then connects them to the appropriate view and control that caused the error.
12. [Step 12: Aggregation Binding Using Templates](step-12-aggregation-binding-using-templates-97830de.md "Aggregation binding, also known as &quot;list binding&quot;, lets a control bind to a list within the model data. This binding allows relative
		binding to the list entries by its child controls. ")  
Aggregation binding, also known as "list binding", lets a control bind to a list within the model data. This binding allows relative binding to the list entries by its child controls.
13. [Step 13: Element Binding](step-13-element-binding-6c7c5c2.md "Now, let's do something with that newly generated list. Typically, you use a list to allow selection of an item and then display the
		details of that item elsewhere. To accomplish this, we use a form with relatively bound controls and bind it to the selected entity via
		element binding.")  
Now, let's do something with that newly generated list. Typically, you use a list to allow selection of an item and then display the details of that item elsewhere. To accomplish this, we use a form with relatively bound controls and bind it to the selected entity via element binding.
14. [Step 14: Expression Binding](step-14-expression-binding-5cff8d1.md "An expression binding lets you display a calculated value on the screen, which is derived from values found in a model object. This
		feature allows you to insert simple formatting or calculations directly into the data binding string. In this example, we're changing the
		color of the price depending on whether it's above or below a certain threshold. The threshold value is stored in the JSON model. ")  
An expression binding lets you display a calculated value on the screen, which is derived from values found in a model object. This feature allows you to insert simple formatting or calculations directly into the data binding string. In this example, we're changing the color of the price depending on whether it's above or below a certain threshold. The threshold value is stored in the JSON model.
15. [Step 15: Aggregation Binding Using a Factory Function](step-15-aggregation-binding-using-a-factory-function-284a036.md "Instead of using a single hard-coded template control, we now opt for a factory function to generate different controls based on the data
		received at runtime. This approach is much more flexible and allows for the display of complex or heterogeneous data.")  
Instead of using a single hard-coded template control, we now opt for a factory function to generate different controls based on the data received at runtime. This approach is much more flexible and allows for the display of complex or heterogeneous data.

**Related Information**  


[Data Binding](../04_Essentials/data-binding-68b9644.md "You use data binding to bind UI elements to data sources to keep the data in sync and allow data editing on the UI.")

[Model View Controller \(MVC\)](../04_Essentials/model-view-controller-mvc-91f2334.md "The Model View Controller (MVC) concept is used in OpenUI5 to separate the representation of information from the user interaction. This separation facilitates development and the changing of parts independently.")

