<!-- loioe1b625940c104b558e52f47afe5ddb4f -->

# Models

A model in the Model View Controller concept holds the data and provides methods to retrieve the data from the database and to set and update data.

***

![UI5 provides the following models: JSON, XML, Resource (all client-side); OData V4, and OData V2 (both
							server-side).](images/loioa99f15722c0a4520b7809c3951362896_LowRes.png)

OpenUI5 provides the following predefined models:

-   **OData models**: Enable binding of controls to data from OData services.

    > ### Note:  
    > Two OData models are available:
    > 
    > -   OData V4 for OData services using the OData V4 protocol
    > 
    > -   OData V2 for OData services using the OData V2 protocol

-   **JSON model**: Can be used to bind controls to JavaScript object data, which is usually serialized in the JSON format. The JSON model is a client-side model and, therefore, intended for small data sets, which are completely available on the client.

-   **XML model**: A client-side model intended for small data sets, which are completely available on the client. The XML model does not contain mechanisms for server-based paging or loading of deltas.

-   **Resource model**: Designed to handle data in resource bundles, mainly to provide texts in different languages.


Whether data can only be read from the model or also be written to the model using data binding differs between the models. For an overview, see [Binding Modes: One-way Binding, Two-way Binding, and One-time Binding](data-binding-68b9644.md#loio68b9644a253741e8a4b9e4279a35c247__section_BindingModes). Note that two-way binding is currently only supported for properties, and not for aggregations.

The JSON model, XML model, and the resource model are **client-side models**, meaning that the model data is loaded completely and is available on the client. Operations such as sorting and filtering are executed on the client without server requests.

The OData \(V4 or V2\) models are **server-side models** and only load required data from the server.

You can define several models for use with your application and assign single controls to a model. You can also define nested models, for example, a JSON model defined for the application and an OData model for a table control contained in the application.

-   **[OData Models](odata-models-cb44153.md "")**  

-   **[JSON Model](json-model-96804e3.md#loio96804e3315ff440aa0a50fd290805116 "The JSON model can be used to bind controls to JavaScript object data, which is
		usually serialized in the JSON format.")**  
The JSON model can be used to bind controls to JavaScript object data, which is usually serialized in the JSON format.
-   **[XML Model](xml-model-a53e71d.md#loioa53e71d85fae4d0887a8b58431197a27 "The XML model allows to bind controls to XML data. It is a client-side model intended
		for small datasets, which are completely available on the client. The XML model does not
		contain mechanisms for server-based paging or loading of deltas. It supports two-way
		binding.")**  
The XML model allows to bind controls to XML data. It is a client-side model intended for small datasets, which are completely available on the client. The XML model does not contain mechanisms for server-based paging or loading of deltas. It supports two-way binding.
-   **[Resource Model](resource-model-91f122a.md#loio91f122a36f4d1014b6dd926db0e91070 "The resource model is used as a wrapper for resource bundles. In data binding you use the resource model instance, for example, to bind texts of
		a control to language-dependent resource bundle properties.")**  
The resource model is used as a wrapper for resource bundles. In data binding you use the resource model instance, for example, to bind texts of a control to language-dependent resource bundle properties.
-   **[Custom Model](custom-model-91f1c7e.md "Custom models can be used if none of the models provided by OpenUI5 is suitable for
		the specific needs of an application.")**  
Custom models can be used if none of the models provided by OpenUI5 is suitable for the specific needs of an application.
-   **[Assigning the Model to the UI](assigning-the-model-to-the-ui-91f0d1c.md "If you don't want to use a component or descriptor file, you have to assign the model
		instance manually to the UI, before you can bind controls to this model
		instance.")**  
If you don't want to use a component or descriptor file, you have to assign the model instance manually to the UI, before you can bind controls to this model instance.
-   **[Setting the Default Binding Mode](setting-the-default-binding-mode-1a08f70.md "The default binding mode applies when a model instance is created. You can overwrite the
		default binding mode after model creation.")**  
The default binding mode applies when a model instance is created. You can overwrite the default binding mode after model creation.

**Related Information**  


[API Reference: `sap.ui.model`](https://ui5.sap.com/#/api/sap.ui.model)

