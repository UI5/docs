<!-- loio5ee619fc1370463ea674ee04b65ed83b -->

# XML Templating

The XML templating concept enables you to use an XML view as a template. This template is transformed by an XML preprocessor on the source level, the XML DOM, at runtime just before an OpenUI5 control tree is created from the XML source.

The label texts and binding paths in the example below come from SAP Annotations for OData Version 2.0 \([http://www.sap.com/Protocols/SAPData](http://www.sap.com/Protocols/SAPData)\) such as `sap:semantics`, and from OData Version 4.0 annotations such as `com.sap.vocabularies.UI.v1.Badge`. Much more complex tasks than shown in this simple example are possible.

> ### Note:  
> HTML templating is no longer supported as of Version 1.56.

The transformation happens if a preprocessor for XML is called when the view is created, see lines 4 and 5 in the *Calling the XML Preprocessor* example. This preprocessor can be given one or more models along with a corresponding binding context, see lines 6 and 9; this concept exists for any OpenUI5 control's constructor. Typically, an OData model's meta model is given, along with the meta context corresponding to a data path. XML templating operates on meta data. If the data changes, the XML templating can **not** be executed again. This is due to the processing time. Only the resulting bindings are evaluated again.

If the view is loaded asynchronously, fragments and required modules are loaded asynchronously, too.

> ### Restriction:  
> XML templating is not directly supported with routing, that is, there is no way to declare that the XML Preprocessor should run on the target view of a route. Instead, you should define a [typed view](typed-view-e6bb33d.md) as the route's target and use that view's `createContent` method to create an XML view with templating.
> 
> In case you need access to models \(which are not yet available in that hook\), you should return some dummy content first \(for instance sap.m.HBox\), register to the view's modelContextChange event and create the inner view in that event's handler, finally adding it to the dummy content.
> 
> **Target Typed View For Routing**
> 
> ```
> sap.ui.define(["sap/ui/core/mvc/View", "sap/ui/core/mvc/XMLView"], function (View, XMLView) {
> 
>      return View.extend("some.package.RouteTargetView", {
>          createContent : function () {
>              return XMLView.create({
>                  preprocessors : {
>                      xml : {
>                          // ...
>                      }
>                  },
>                  viewName : "some.package.TemplateView"
>              }).then(function (oView) {
>                  // return View content
>                  return oView;
>              });
>          }
>      });
> });
> ```

In the example, `sPath = "/ProductSet('HT-1021')/ToSupplier"` and the corresponding meta context point to `"/dataServices/schema/0/entityType/0"` \(the entity type `BusinessPartner`\). The resulting view is bound to the data path within the OData model in order to display the supplier of that product.

***

<a name="loio5ee619fc1370463ea674ee04b65ed83b__section_preproc"/>

## Calling the XML Preprocessor

```js
1   View.create({
2      models : oModel,
3      preprocessors : {
4         xml : {
5            bindingContexts : {
6               meta : oMetaModel.getMetaContext(sPath)
7            },
8            models : {
9              meta : oMetaModel
10           }
11        }
12     },
13     type : ViewType.XML,
14     viewName : "sap.ui.core.sample.ViewTemplate.tiny.Template"
15  }).then(function (oTemplateView) {
16     oTemplateView.bindElement(sPath);
17     ...
18  }
```

The XML preprocessor traverses the view's XML DOM in a depth-first, parent-before-child manner and does the following:

-   All XML attributes which represent an available binding, that is, a binding based only on models available to the preprocessor, are replaced by the result of that binding. Formatters and so on can be used as with any SAPUI5 binding.

-   XML fragments are inlined; that is, the reference is replaced by the fragment's XML DOM and preprocessing takes place on that DOM as well.

-   The preprocessing instructions `<template:with>`, `<template:if>` and `<template:repeat>` are processed.


***

<a name="loio5ee619fc1370463ea674ee04b65ed83b__section_example"/>

## Example

See the [sap.ui.core.sample.ViewTemplate.tiny](https://ui5.sap.com/#/entity/sap.ui.core.mvc.XMLView/sample/sap.ui.core.sample.ViewTemplate.tiny) XML Templating sample. This sample is based on OData Version 4.0 annotations. It contains the following files worth noting:

-   An annotations file containing label texts and binding paths.

-   A component controller that creates an OData model \(Line 33\), waits for the meta model to be loaded \(Line 50\) and then creates a template view \(Line 51\) as its content. A preprocessor for XML is requested \(Line 54\) and settings are passed to it, namely the meta model and the binding context that identifies the starting point within that model. The resulting view is bound to the actual data \(model and path\).

-   A template view that includes a fragment twice \(Line 20 and 25\) to demonstrate how to reuse code.

-   An XML fragment that demonstrates a simple test \(Line 10\), using expression binding.


> ### Tip:  
> You can find more elaborate XML templating samples here: [XMLView](https://ui5.sap.com/#/entity/sap.ui.core.mvc.XMLView). 
> 
> Take a look at the demo scenario for a complete overview of all OData V4 notations.

> ### Caution:  
> The OData model used in this example is based on `GWSAMPLE_BASIC` and will not work unless a suitable proxy for back-end access is used. For simplicity, no mock data is included in this example.
> 
> For more information, see the Help topic, [Sample Service - Basic](http://help.sap.com/saphelp_nw74/helpdata/en/59/283fc4528f486b83b1a58a4f1063c0/frameset.htm).

**To run the sample with UI5 Tooling \(recommended\):** 

1.  [Create an account on the SAP Gateway Demo System \(ES5\)](https://developers.sap.com/tutorials/gateway-demo-signup.html).

2.  Download [sap.ui.core.sample.ViewTemplate.tiny](https://ui5.sap.com/#/entity/sap.ui.core.mvc.XMLView/sample/sap.ui.core.sample.ViewTemplate.tiny/code) as a zip file to your local machine \(find the *Download* button on the top right\).

3.  Extract the project folder to a desired location on your local machine.

4.  At your chosen location, open a new shell in your app root folder and execute `npm install`.

5.  After all dependencies have been installed, enter `npm start` to start the development server.

6.  Open `index.html` in your browser. You will need to enter the username and password for your ES5 account from Step 1.


**Component.js** 

```js
1   /*!
2    * OpenUI5
3    * (c) Copyright 2025 SAP SE or an SAP affiliate company.
4    * Licensed under the Apache License, Version 2.0 - see LICENSE.txt.
5    */
6    
7   /**
8    * @fileOverview Application component to display supplier of "/ProductSet('HT-1021')"
9    *   from GWSAMPLE_BASIC via XML Templating.
10   * @version @version@
11   */
12  sap.ui.define([
13      "sap/m/MessageBox",
14      "sap/m/Title",
15      "sap/m/VBox",
16      "sap/ui/core/library",
17      "sap/ui/core/UIComponent",
18      "sap/ui/core/mvc/View",
19      "sap/ui/model/odata/v2/ODataModel"
20  ], function(MessageBox, Title, VBox, library, UIComponent, View, ODataModel) {
21      "use strict";
22   
23      var TitleLevel = library.TitleLevel, // shortcut for sap.ui.core.TitleLevel
24          ViewType = library.mvc.ViewType; // shortcut for sap.ui.core.mvc.ViewType
25   
26      return UIComponent.extend("sap.ui.core.sample.ViewTemplate.tiny.Component", {
27           metadata : {
28              interfaces : ["sap.ui.core.IAsyncContentCreation"],
29              manifest: "json"
30           },
31   
32          createContent : function () {
33              var oModel = new ODataModel(
34                      "/sap/opu/odata/IWBEP/GWSAMPLE_BASIC/", {
35                      annotationURI : "/test-resources/sap/ui/core/demokit/sample/ViewTemplate/tiny"
36                          + "/annotations.xml",
37                      json : true,
38                      loadMetadataAsync : true
39                  }),
40                  oMetaModel = oModel.getMetaModel(),
41                  sPath = "/ProductSet('HT-1021')/ToSupplier",
42                  oViewContainer = new VBox({
43                      items : [
44                          new Title({text : "This is meant to be a pure code sample. "
45                              + "(To run it, you would need a proxy which is configured properly.)",
46                              titleStyle : TitleLevel.H3})
47                      ]
48                  });
49   
50              oMetaModel.loaded().then(function () {
51                  View.create({
52                      async : true,
53                      models : oModel,
54                      preprocessors : {
55                          xml : {
56                              bindingContexts : {
57                                  meta : oMetaModel.getMetaContext(sPath)
58                              },
59                              models : {
60                                  meta : oMetaModel
61                              }
62                          }
63                      },
64                      type : ViewType.XML,
65                      viewName : "sap.ui.core.sample.ViewTemplate.tiny.Template"
66                  }).then(function (oTemplateView) {
67                      oTemplateView.bindElement(sPath);
68                      oViewContainer.destroyItems();
69                      oViewContainer.addItem(oTemplateView);
70                  }, function (oError) {
71                      MessageBox.alert(oError.message, {
72                          icon : MessageBox.Icon.ERROR,
73                          title : "Missing Proxy?"
74                      });
75                  });
76              });
77   
78              // Note: synchronously return s.th. here and add content to it later on
79              return oViewContainer;
80          }
81      });
82  });
```

**Template.view.xml** 

```xml
1   <mvc:View
2       xmlns="sap.m"
3       xmlns:core="sap.ui.core"
4       xmlns:form="sap.ui.layout.form"
5       xmlns:mvc="sap.ui.core.mvc"
6       xmlns:template="http://schemas.sap.com/sapui5/extension/sap.ui.core.template/1">
7       template:require="{AH: 'sap/ui/model/odata/AnnotationHelper'}">
8       <!-- "meta" model's binding context MUST point to an entity type -->
9          <template:with path="meta>com.sap.vocabularies.UI.v1.Badge" var="badge">
10              <form:SimpleForm layout="ResponsiveGridLayout">
11                  <form:title>
12                      <core:Title text="{path: 'badge>HeadLine', formatter: '.AH.format'}"/>
13                  </form:title>
14   
15                  <Label text="{path: 'badge>Title/Label', formatter: '.AH.format'}"/>
16                  <Text text="{path: 'badge>Title/Value', formatter: '.AH.format'}"/>
17   
18                  <Label text="{path: 'badge>MainInfo/Label', formatter: '.AH.format'}"/>
19                  <template:with path="badge>MainInfo" var="field">
20                      <core:Fragment fragmentName="sap.ui.core.sample.ViewTemplate.tiny.Field" type="XML"/>
21                  </template:with>
22   
23                  <Label text="{path: 'badge>SecondaryInfo/Label', formatter: '.AH.format'}"/>
24                  <template:with path="badge>SecondaryInfo" var="field">
25                      <core:Fragment fragmentName="sap.ui.core.sample.ViewTemplate.tiny.Field" type="XML"/>
26                  </template:with>
27              </form:SimpleForm>
28          </template:with>
29  </mvc:View>
```

**Field.fragment.xml** 

```xml
1   <core:FragmentDefinition
2       xmlns="sap.m"
3       xmlns:core="sap.ui.core"
4       xmlns:template="http://schemas.sap.com/sapui5/extension/sap.ui.core.template/1">
5    
6       <!-- "field" MUST point to a com.sap.vocabularies.Communication.v1.DataField -->
7       <HBox>
8           <template:with path="field>Value" helper="AH.resolvePath" var="target">
9               <!-- go to entity type's property and check SAP Annotations for OData Version 2.0 -->
10              <template:if test="{= ${target>sap:semantics} === 'tel'}" >
11                  <core:Icon src="sap-icon://phone" width="2em"/>
12              </template:if>
13          </template:with>
14          <Text text="{path: 'field>Value', formatter: 'AH.format'}"/>
15      </HBox>
16  </core:FragmentDefinition>
```

The result is equivalent to the following handwritten XML view. Any references to the meta model are gone. Type information has been inserted into the bindings and an `"odata.concat"` expression for `badge>MainInfo/Value` has been processed by `sap.ui.model.odata.AnnotationHelper.format`, concatenating the company name and legal form.

**Resulting XML View** 

```xml
<mvc:View xmlns="sap.m" xmlns:core="sap.ui.core" xmlns:form="sap.ui.layout.form" xmlns:mvc="sap.ui.core.mvc">
  <form:SimpleForm>
    <form:title>
      <core:Title text="{path : 'BusinessPartnerID', type : 'sap.ui.model.odata.type.String', constraints : {'maxLength':'10','nullable':'false'}}"/>
    </form:title>
    <Label text="Name"/>
    <Text text="{path : 'CompanyName', type : 'sap.ui.model.odata.type.String', constraints : {'maxLength':'80'}} {path : 'LegalForm', type : 'sap.ui.model.odata.type.String', constraints : {'maxLength':'10'}}"/>
    <Label text="Phone"/>
    <HBox>
      <core:Icon src="sap-icon://phone" width="2em"/>
      <Text text="{path : 'PhoneNumber', type : 'sap.ui.model.odata.type.String', constraints : {'maxLength':'30'}}"/>
    </HBox>
    <Label text="Web"/>
    <HBox>
      <Text text="{path : 'WebAddress', type : 'sap.ui.model.odata.type.String', constraints : {}}"/>
    </HBox>
  </form:SimpleForm>
</mvc:View>
```

***

## Summary

Overall, XML templating is based on:

-   Preprocessing instructions such as `<template:if>`, which can be used inside XML views

-   An OData meta model which offers a unified access to both, OData V2 metadata and OData V4 annotations

-   A set of OData type implementations which add knowledge of OData types to OpenUI5

-   Expression binding which facilitates the use of expressions instead of custom formatter functions

-   The helper class `sap.ui.model.odata.AnnotationHelper` that offers formatter and helper functions to be used inside XML template views. It knows about the OData meta model and helps with standard tasks like accessing a label or providing a runtime binding path. It brings in the OData types, along with their facets. Its output uses expression binding, if needed.


> ### Note:  
> XML Templating works almost the same for OData V4 as for OData V2; for the differences see the *Annotations* section in [Meta Model for OData V4](meta-model-for-odata-v4-7f29fb3.md).

-   **[Preprocessing Instructions](preprocessing-instructions-c27d49c.md "Preprocessing intructions are processed by the XML preprocessor when it traverses the
		view's XML DOM.")**  
Preprocessing intructions are processed by the XML preprocessor when it traverses the view's `XML DOM`.
-   **[Annotation Helper](annotation-helper-dbec058.md " A collection of methods which help to consume OData Version 4.0 annotations in XML
		template views.")**  
 A collection of methods which help to consume OData Version 4.0 annotations in XML template views.
-   **[Debugging](debugging-153b357.md "For the debug levels DEBUG and ALL, the XML
		preprocessor writes a trace for what it exactly does.")**  
For the debug levels `DEBUG` and `ALL`, the XML preprocessor writes a trace for what it exactly does.

**Related Information**  


[Meta Model for OData V2](odata-v2-model-6c47b2b.md#loio341823349ed04df1813197f2a0d71db2 "The implementation sap.ui.model.odata.ODataMetaModel offers a unified access to both OData Version 2.0 metadata and Version 4.0 annotations.")

[Expression Binding](expression-binding-daf6852.md "Expression binding is an enhancement of the OpenUI5 binding syntax, which allows for providing expressions instead of custom formatter functions.")

[SAP Annotations for OData Version 2.0](http://www.sap.com/Protocols/SAPData)

[`sap.ui.model.odata.AnnotationHelper`](https://ui5.sap.com/#/api/sap.ui.model.odata.AnnotationHelper)

