<!-- loio91f0d8ab6f4d1014b6dd926db0e91070 -->

# Binding Types

Depending on the different use cases, you can use different binding types: property binding, context binding, list binding, and tree binding.

***

-   **Property binding** allows properties of the control to get automatically initialized and updated from model data. You can only bind control properties to model properties of a matching type, or you use a formatter or a data type to parse and convert the data as needed For more information, see [Formatting, Parsing, and Validating Data](formatting-parsing-and-validating-data-07e4b92.md).

-   **Context binding** \(or **element binding**\) allows to bind elements to a specific object in the model that creates a binding context and allows relative binding within the control and all of its children. This is especially helpful in list-detail scenarios.

-   **Aggregation binding** \(**list binding** or **tree binding**\) is used to automatically create child controls according to model data, either by cloning a template control or by using a factory function:

    -   **List binding** binds to a flat list, for example an array in a JSON model or a flat collection in an OData model.
    -   **Tree binding** binds to hierarchical data, for example a nested array in a JSON model or a hierarchical collection in an OData model. It is typically used with tree controls such as `sap.ui.table.TreeTable`.

    > ### Note:  
    > The model has a default size limit to avoid too much data being rendered on the UI. This size limit determines the number of entries used for the list bindings. The default size limit is 100 entries.
    > 
    > This means that controls that don't support paging or don't request data in chunks \(e.g. `sap.m.ComboBox`\) only show 100 entries even though the model contains more items.
    > 
    > To change this behavior, you can either set a size limit in the model by using `oModel.setSizeLimit` or set the `length` property of the `oBindingInfo` parameter of the [`sap.ui.base.ManagedObject#bindAggregation`](https://ui5.sap.com/#/api/sap.ui.base.ManagedObject/methods/bindAggregation) method.


-   **[Property Binding](property-binding-91f0652.md "With property binding, you can initialize properties of a control automatically and
		update them based on the data of the model.")**  
With property binding, you can initialize properties of a control automatically and update them based on the data of the model.
-   **[Context Binding \(Element Binding\)](context-binding-element-binding-91f05e8.md "Context binding (or element binding) allows you to bind elements to a specific object in the model data, which will create a binding
		context and allow relative binding within the control and all of its children. This is especially helpful in list-detail
		scenarios.")**  
Context binding \(or element binding\) allows you to bind elements to a specific object in the model data, which will create a binding context and allow relative binding within the control and all of its children. This is especially helpful in list-detail scenarios.
-   **[List Binding and Tree Binding \(Aggregation Binding\)](list-binding-and-tree-binding-aggregation-binding-91f0577.md "List binding and tree binding are both also referred to as aggregation binding. List
		binding binds to a flat list and is used to automatically create child controls according to
		model data. Tree binding works the same way but binds to hierarchical data.")**  
List binding and tree binding are both also referred to as aggregation binding. List binding binds to a flat list and is used to automatically create child controls according to model data. Tree binding works the same way but binds to hierarchical data.

