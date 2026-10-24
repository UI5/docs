<!-- loioe5310932a71f42daa41f3a6143efca9c -->

# Data Binding Tutorial

In this tutorial, we explain the concepts of data binding in OpenUI5.

This tutorial has been moved.

-   For a JavaScript version, see [JavaScript Data Binding Tutorial on GitHub](https://ui5.github.io/tutorials/databinding/?lang=js).
-   For a TypeScript version, see [TypeScript Data Binding Tutorial on GitHub](https://ui5.github.io/tutorials/databinding/?lang=ts).

-   **[Step 1: No Data Binding](step-1-no-data-binding-4cde849.md "In this step, we create a basic application and simply place some text on the screen using a standard sap.m.Text control.
		The text in this control is a hard-coded part of the control's definition; therefore, this is not an example of data binding!")**  
In this step, we create a basic application and simply place some text on the screen using a standard `sap.m.Text` control. The text in this control is a hard-coded part of the control's definition; therefore, this is not an example of data binding!
-   **[Step 2: Creating a Model](step-2-creating-a-model-5278bfd.md "In this step, we create a model. It serves as a container for the data your application operates on.")**  
In this step, we create a model. It serves as a container for the data your application operates on.
-   **[Step 3: Create Property Binding](step-3-create-property-binding-d70e989.md "Although there is no visible difference, the text on the screen is now derived from
		model data.")**  
Although there is no visible difference, the text on the screen is now derived from model data.
-   **[Step 4: Two-Way Data Binding](step-4-two-way-data-binding-c72b922.md "In the examples we've looked at so far, we've displayed the value of a model property using a read-only field. We'll now change the user
		interface to display first and last name fields using sap.m.Input fields. We're also adding a check box control to enable or
		disable both input fields. This setup illustrates a feature known as &quot;two-way data binding&quot;. As the view now contains more controls, we're
		also moving the view definition into an XML file.")**  
In the examples we've looked at so far, we've displayed the value of a model property using a read-only field. We'll now change the user interface to display first and last name fields using `sap.m.Input` fields. We're also adding a check box control to enable or disable both input fields. This setup illustrates a feature known as "two-way data binding". As the view now contains more controls, we're also moving the view definition into an XML file.
-   **[Step 5: One-Way Data Binding](step-5-one-way-data-binding-88756c0.md "Unlike the two-way binding behavior we've seen, one-way data binding is also possible. In this case, data travels in one direction only:
		from the model, through the binding instance, to the consumer (usually the property of a control), but never in the other direction. Let's
		modify the previous example to use one-way data binding. This shows how you can switch off the flow of data from the user interface back to
		the model if needed.")**  
Unlike the two-way binding behavior we've seen, one-way data binding is also possible. In this case, data travels in one direction only: from the model, through the binding instance, to the consumer \(usually the property of a control\), but never in the other direction. Let's modify the previous example to use one-way data binding. This shows how you can switch off the flow of data from the user interface back to the model if needed.
-   **[Step 6: Resource Models](step-6-resource-models-9790d9a.md "Business applications often require language-specific (translatable) text used as labels and descriptions on the user
		interface.")**  
Business applications often require language-specific \(translatable\) text used as labels and descriptions on the user interface.
-   **[Step 7: \(Optional\) Resource Bundles and Multiple Languages](step-7-optional-resource-bundles-and-multiple-languages-4e593b4.md "Resource bundles exist to enable an app to run in multiple languages without the need to change any code. To demonstrate this feature,
		let's create a German version of the app – in fact, all we need to do is create a German version of the resource bundle file. In our code, we
		activate the German locale for the ResourceModel.")**  
Resource bundles exist to enable an app to run in multiple languages without the need to change any code. To demonstrate this feature, let's create a German version of the app – in fact, all we need to do is create a German version of the resource bundle file. In our code, we activate the German locale for the ResourceModel.
-   **[Step 8: Binding Paths: Accessing Properties in Hierarchically Structured Models](step-8-binding-paths-accessing-properties-in-hierarchically-structured-models-9373793.md "In Step 6 , we stated that the fields in a resource model are arranged in a flat structure; in other words, there is no hierarchy of
		properties. However, this is only true for resource models. The properties within JSON and OData models are usually arranged in a hierarchical
		structure. So, let's explore how to reference fields in a hierarchically structured model object.")**  
In Step 6 , we stated that the fields in a resource model are arranged in a flat structure; in other words, there is no hierarchy of properties. However, this is only true for resource models. The properties within JSON and OData models are usually arranged in a hierarchical structure. So, let's explore how to reference fields in a hierarchically structured model object.
-   **[Step 9: Formatting Values](step-9-formatting-values-6fdf0ac.md "We'd also like to provide our users with a way of contacting Harry Hawk, so we're adding a link that sends an e-mail to Harry. To do this,
		we convert our data in the model to match the sap.m.URLHelper.normalizeEmail API. As soon as the user changes the name, the
		e-mail also changes. We need a custom formatter function for this.")**  
We'd also like to provide our users with a way of contacting Harry Hawk, so we're adding a link that sends an e-mail to Harry. To do this, we convert our data in the model to match the `sap.m.URLHelper.normalizeEmail` API. As soon as the user changes the name, the e-mail also changes. We need a custom formatter function for this.
-   **[Step 10: Property Formatting Using Data Types](step-10-property-formatting-using-data-types-9252ee4.md "OpenUI5 offers a set of simple data types, including Boolean,
			Currency, Date and Float. You can apply these data types to controls to ensure that the
		value displayed on the screen is formatted correctly. If the field is open for input, this also ensures that the user input meets the
		requirements of that data type. Let's add a new field called Sales Amount of type Currency. ")**  
OpenUI5 offers a set of simple data types, including `Boolean`, `Currency`, `Date` and `Float`. You can apply these data types to controls to ensure that the value displayed on the screen is formatted correctly. If the field is open for input, this also ensures that the user input meets the requirements of that data type. Let's add a new field called *Sales Amount* of type `Currency`.
-   **[Step 11: Validation Using sap/ui/core/Messaging](step-11-validation-using-sap-ui-core-messaging-b8c4e53.md "Up to this point, we've created a currency field that formats itself correctly. The currency data type can also validate user
		input to ensure it meets currency requirements. However, OpenUI5 manages data type
		validation functions and doesn't have a built-in mechanism for reporting error messages back to the UI. We therefore need a way to report
		error messages from validation functions back to the user. In this step, we're enabling validation for the entire app with a feature known as
		&quot;Messaging&quot;. Once this is set up, any validation error messages based on user input get passed to Messaging, which then
		connects them to the appropriate view and control that caused the error.")**  
Up to this point, we've created a currency field that formats itself correctly. The *currency* data type can also validate user input to ensure it meets currency requirements. However, OpenUI5 manages data type validation functions and doesn't have a built-in mechanism for reporting error messages back to the UI. We therefore need a way to report error messages from validation functions back to the user. In this step, we're enabling validation for the entire app with a feature known as "Messaging". Once this is set up, any validation error messages based on user input get passed to `Messaging`, which then connects them to the appropriate view and control that caused the error.
-   **[Step 12: Aggregation Binding Using Templates](step-12-aggregation-binding-using-templates-97830de.md "Aggregation binding, also known as &quot;list binding&quot;, lets a control bind to a list within the model data. This binding allows relative
		binding to the list entries by its child controls. ")**  
Aggregation binding, also known as "list binding", lets a control bind to a list within the model data. This binding allows relative binding to the list entries by its child controls.
-   **[Step 13: Element Binding](step-13-element-binding-6c7c5c2.md "Now, let's do something with that newly generated list. Typically, you use a list to allow selection of an item and then display the
		details of that item elsewhere. To accomplish this, we use a form with relatively bound controls and bind it to the selected entity via
		element binding.")**  
Now, let's do something with that newly generated list. Typically, you use a list to allow selection of an item and then display the details of that item elsewhere. To accomplish this, we use a form with relatively bound controls and bind it to the selected entity via element binding.
-   **[Step 14: Expression Binding](step-14-expression-binding-5cff8d1.md "An expression binding lets you display a calculated value on the screen, which is derived from values found in a model object. This
		feature allows you to insert simple formatting or calculations directly into the data binding string. In this example, we're changing the
		color of the price depending on whether it's above or below a certain threshold. The threshold value is stored in the JSON model. ")**  
An expression binding lets you display a calculated value on the screen, which is derived from values found in a model object. This feature allows you to insert simple formatting or calculations directly into the data binding string. In this example, we're changing the color of the price depending on whether it's above or below a certain threshold. The threshold value is stored in the JSON model.
-   **[Step 15: Aggregation Binding Using a Factory Function](step-15-aggregation-binding-using-a-factory-function-284a036.md "Instead of using a single hard-coded template control, we now opt for a factory function to generate different controls based on the data
		received at runtime. This approach is much more flexible and allows for the display of complex or heterogeneous data.")**  
Instead of using a single hard-coded template control, we now opt for a factory function to generate different controls based on the data received at runtime. This approach is much more flexible and allows for the display of complex or heterogeneous data.

**Related Information**  


[Data Binding](../04_Essentials/data-binding-68b9644.md "You use data binding to bind UI elements to data sources to keep the data in sync and allow data editing on the UI.")

[Use the MVC Concept](use-the-mvc-concept-07afcf4.md "MVC (Model-View-Controller) is a concept for structuring your software. Separating the representation of information from the user interaction makes it easier to maintain and to extend your apps.")

