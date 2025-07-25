<!-- loiod9f16f2262a947ef9cd5b58f11c54b6e -->

# What's New in OpenUI5 1.98

With this release OpenUI5 is upgraded from version 1.97 to 1.98.

***

****


<table>
<tr>
<th valign="top">

Version

</th>
<th valign="top">

Type

</th>
<th valign="top">

Category

</th>
<th valign="top">

Title

</th>
<th valign="top">

Description

</th>
<th valign="top">

Action

</th>
<th valign="top">

Available as of

</th>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**OpenUI5 OData V2 Model** 

</td>
<td valign="top">

**OpenUI5 OData V2 Model**

The new version of the OpenUI5 OData V2 model introduces the following features:

-   The `sap.ui.model.odata.v2.ODataListBinding#create` method, which allows to create transient entries in a list binding similar to its counterpart in the OData V4 model. For more information, see [Creating Entities](../04_Essentials/odata-v2-model-6c47b2b.md#loio4c4cd99af9b14e08bb72470cc7cabff4).

-   You can now create inactive contexts using `sap.ui.model.odata.v2.ODataListBinding#create`. There is no POST request for an inactive context. The context will become active as soon as any of its properties is changed. Once this happens, the `createActivate` event is raised, enabling the application to create a new inactive context.

    Inactive contexts do not influence `sap.ui.model.odata.v2.ODataListBinding#getCount`. They are neither pending changes nor are they reset by `sap.ui.model.odata.v2.ODataModel#resetChanges`. For more information, see [Creating Entities](../04_Essentials/odata-v2-model-6c47b2b.md#loio4c4cd99af9b14e08bb72470cc7cabff4).

-   The `getAllCurrentContexts` method for list bindings returns all current contexts without raising a request.For more information, see [`sap.ui.model.ListBinding#getAllCurrentContexts`](https://ui5.sap.com/#/api/sap.ui.model.ListBinding%23methods/getAllCurrentContexts).


<sub>Changed•Feature•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**OpenUI5 OData V4 Model** 

</td>
<td valign="top">

**OpenUI5 OData V4 Model**

The new version of the OpenUI5 OData V4 model introduces the following features:

-   You can now replace a row context of a list with a sibling entity of the same collection. The sibling entity must be available as a :1 navigation property and is accessed with an operation binding. For more information, see [Draft Handling with the OData V4 Model](../04_Essentials/draft-handling-with-the-odata-v4-model-40986e6.md).

-   An application can now create inactive contexts in a list binding using the `bInactive` parameter of `sap.ui.model.odata.v4.ODataListBinding#create`, provided the update group of the binding is an `Auto` group. There is no POST request for an inactive context. The context will become active as soon as any of its properties is changed. Once this happens, the `createActivate` event is raised, enabling the application to create a new inactive context.

    Inactive contexts do not influence `sap.ui.model.odata.v4.ODataListBinding#getCount`. They are neither pending changes nor are they reset by `sap.ui.model.odata.v4.ODataListBinding#resetChanges` or `sap.ui.model.odata.v4.ODataModel#resetChanges`. For more information, see [Creating an Entity in a Collection](../04_Essentials/creating-an-entity-in-a-collection-c9723f8.md).

-   The `sap.ui.model.odata.v4.ODataListBinding#getAllCurrentContexts` method returns all current contexts without raising a request.

-   The experimental `sap.ui.model.odata.v4.ODataContextBinding#moveEntityTo` method introduced with OpenUI5 1.95 is deprecated.


<sub>Changed•Feature•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.DateTimePicker`, `sap.m.TimePicker`** 

</td>
<td valign="top">

**`sap.m.DateTimePicker`, `sap.m.TimePicker`**

We have introduced a shortcut button that focuses the current time. The button is shown if the new `showCurrentTimeButton` property is set to true. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.TimePicker) and the [Sample](https://ui5.sap.com/#/entity/sap.m.TimePicker/sample/sap.m.sample.TimePicker).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.DynamicDateRange` \(Experimental\)** 

</td>
<td valign="top">

**`sap.m.DynamicDateRange` \(Experimental\)**

-   When the user types something in the input field of the control, the displayed suggestion items now appear in groups if the `enableGroupHeaders` property is set to `true`.

-   We have added new standard options to the control that represent the first or the last day of the current week, month, quarter, or year.

-   The `StandardDynamicDateRangeKeys` is now an enumeration with keys matching the values. The default value of the `DynamicDateRange` control’s `options` property is now a full array of the keys \(before it was an empty array\).


For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.DynamicDateRange) and the [Samples](https://ui5.sap.com/#/entity/sap.m.DynamicDateRange).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.IconTabBar`** 

</td>
<td valign="top">

**`sap.m.IconTabBar`**

There is a change in the way how the control computes and displays the number of tabs that are in the overflow buttons at both sides of the tabs area, when the property overflow mode is set to `StartAndEnd`. Now, only the top-level tabs are counted and not the nested sub-tabs. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.IconTabBar) and the [Sample](https://ui5.sap.com/#/entity/sap.m.IconTabBar/sample/sap.m.sample.IconTabBarStartAndEndOverflow).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Label`** 

</td>
<td valign="top">

**`sap.m.Label`**

We have introduced a new `showColon` property. If set to `true`, a colon \(:\) character is added to the label. This feature is useful in cases when the Label is used independently. In contrast, when the Label is in a Form or in a Simple Form, the colon \(:\) character is displayed automatically regardless of the value of the `showColon` property. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Label).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.List`** 

</td>
<td valign="top">

**`sap.m.List`**

You can now display an avatar in your list instead of an image or icon. We have integrated the `sap.m.Avatar` control as an aggregation of `StandardListItem`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.StandardListItem%23aggregations) and the [Sample](https://ui5.sap.com/#/entity/sap.m.StandardListItem/sample/sap.m.sample.StandardListItemAvatar).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.p13n*`** 

</td>
<td valign="top">

**`sap.m.p13n*`**

We have made personalization within a table or list more reusable. Different panels with reusable content for the various types of personalization are now available for freestyle use in your application.

The following panels are available \(as experimental APIs\):

-   `sap.m.p13n.SelectionPanel`

    Defines a number of properties that allow you to select and deselect fields as columns in your table, for example, and to change their order.

-   `sap.m.p13n.SortPanel`

    Defines a number of properties that allow you to sort your items based on various criteria, for example, in ascending or descending order.

-   `sap.m.p13n.GroupPanel`

    Defines a number of properties that allow you to group your data.


The panels are aggregated to `sap.m.p13n.Popup` \(experimental\), which serves as a container for all the panels.

For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.p13n) and the [Sample](https://ui5.sap.com/#/entity/sap.m.p13n.Popup/sample/sap.m.sample.p13n.Popup).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.SinglePlanningCalendar`** 

</td>
<td valign="top">

**`sap.m.SinglePlanningCalendar`**

With the new `firstDayOfWeek` property, you can now set the first day of a week displayed in the Week and Month views of the control. If there is no valid value set, the default from the user locale is used. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.SinglePlanningCalendar) and the [Sample](https://ui5.sap.com/#/entity/sap.m.SinglePlanningCalendar/sample/sap.m.sample.SinglePlanningCalendarSnappingHeader).

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.upload.UploadSet`** 

</td>
<td valign="top">

**`sap.m.upload.UploadSet`**

For the `uploadCompleted` event, an additional JSON response object is now passed. Along with it, some of its parameters are also passed such as response, `responseXML`, `readyState`, status, and headers. It helps you to understand if the upload is complete.

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.integration.widgets.Card`** 

</td>
<td valign="top">

**`sap.ui.integration.widgets.Card`**

-   We have introduced a new filter type – Search \(experimental\). To define it, you only have to set the filter's `type` property to `Search`, and then specify the optional initial value of the filter and the placeholder of the field. For more information, see the [Search Filter](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/filters/search) section and the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/searchFilter) in the Card Explorer.

-   Integration cards now support \(experimentally\) CSRF tokens as a method to prevent CSRF attacks. For more information, see the [CSRF Tokens](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/configuration/csrfTokens) section and the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/data/csrf) in the Card Explorer.

-   The submit action of the Adaptive card supports binding syntax. This allows card developers to map the values entered by the end user to the payload structure expected by the back-end service. For more information, see the [Action Handlers](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/configuration/actionHandlers) section and the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/adaptive/adaptive-action-submit-custom-payload) in the Card Explorer.

-   We have added support for more HTTP request methods. Together with GET and POST, Integration cards now also support PUT, PATCH, DELETE, OPTIONS, and HEAD methods. For more information, see the [Data Handling](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/features/data) section in the Card Explorer.

-   Object cards are \(experimentally\) enhanced with new item types and a new attribute. The new item types are `NumericData`, which shows some KPIs, and `Status`. The new attribute is `maxLines` - it represents the maximum number of lines the text can take. For more information, see the [Object Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/types/object) section, the [To Do Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/object/todoCard) sample, and [Additional Object Details](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/object/additionalObjectDetails) sample in the Card Explorer.

-   We have updated the `sap.ui.integration.widgets.Card` of type Adaptive with the new 1.01 version of UI5 Web Components. For more information, see the [Adaptive Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/types/adaptive) section in the Card Explorer.
-   We have updated the `sap.ui.integration.widgets.Card` of type Adaptive to support the newest templating and markdown features available for Microsoft Adaptive Cards, by getting the latest versions of `adaptivecards-templating`, `adaptive-expressions`, and `markdown-it`. Due to changes in the templating syntax, developers should adapt their applications when they switch to version 1.98. For more information, see the [Adaptive Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/types/adaptive) section and the [Templating](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/adaptive/templating) and [Markdown](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/adaptive/markdown) Samples in the Card Explorer. 

<sub>Changed•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Deprecated 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.f.IllustratedMessage` / `sap.m.IllustratedMessage`** 

</td>
<td valign="top">

**`sap.f.IllustratedMessage` / `sap.m.IllustratedMessage`**

The `sap.f.IllustratedMessage` and its related classes are now moved to the `sap.m` library. The `sap.f` classes and their documentation are kept for compatibility reasons and are marked as deprecated. All of them extend their `sap.m` version.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.f.IllustratedMessage).

<sub>Deprecated•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
<tr>
<td valign="top">

1.98 

</td>
<td valign="top">

Deprecated 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.P13n*`** 

</td>
<td valign="top">

**`sap.m.P13n*`**

The following entities have been deprecated and replaced with the new personalization panels:

-   `sap.m.P13nDialog`

-   `sap.m.P13nColumnsPanel`

-   `sap.m.P13nSortPanel`

-   `sap.m.P13nGroupPanel`


<sub>Deprecated•Control•Info Only•1.98</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2022-01-27

</td>
</tr>
</table>

**Parent topic:**[Previous Versions](previous-versions-6660a59.md "")

**Related Information**  


[What's New in OpenUI5 1.136](what-s-new-in-openui5-1-136-a82754d.md "With this release OpenUI5 is upgraded from version 1.135 to 1.136.")

[What's New in OpenUI5 1.135](what-s-new-in-openui5-1-135-93d7630.md "With this release OpenUI5 is upgraded from version 1.134 to 1.135.")

[What's New in OpenUI5 1.134](what-s-new-in-openui5-1-134-c512d71.md "With this release OpenUI5 is upgraded from version 1.133 to 1.134.")

[What's New in OpenUI5 1.133](what-s-new-in-openui5-1-133-86d7605.md "With this release OpenUI5 is upgraded from version 1.132 to 1.133.")

[What's New in OpenUI5 1.132](what-s-new-in-openui5-1-132-bd2e61f.md "With this release OpenUI5 is upgraded from version 1.131 to 1.132.")

[What's New in OpenUI5 1.131](what-s-new-in-openui5-1-131-7d24d94.md "With this release OpenUI5 is upgraded from version 1.130 to 1.131.")

[What's New in OpenUI5 1.130](what-s-new-in-openui5-1-130-85609d4.md "With this release OpenUI5 is upgraded from version 1.129 to 1.130.")

[What's New in OpenUI5 1.129](what-s-new-in-openui5-1-129-d22b8af.md "With this release OpenUI5 is upgraded from version 1.128 to 1.129.")

[What's New in OpenUI5 1.128](what-s-new-in-openui5-1-128-1f76220.md "With this release OpenUI5 is upgraded from version 1.127 to 1.128.")

[What's New in OpenUI5 1.127](what-s-new-in-openui5-1-127-e5e1317.md "With this release OpenUI5 is upgraded from version 1.126 to 1.127.")

[What's New in OpenUI5 1.126](what-s-new-in-openui5-1-126-1d98116.md "With this release OpenUI5 is upgraded from version 1.125 to 1.126.")

[What's New in OpenUI5 1.125](what-s-new-in-openui5-1-125-9d87044.md "With this release OpenUI5 is upgraded from version 1.124 to 1.125.")

[What's New in OpenUI5 1.124](what-s-new-in-openui5-1-124-7f77c3f.md "With this release OpenUI5 is upgraded from version 1.123 to 1.124.")

[What's New in OpenUI5 1.123](what-s-new-in-openui5-1-123-9d00ac7.md "With this release OpenUI5 is upgraded from version 1.122 to 1.123.")

[What's New in OpenUI5 1.122](what-s-new-in-openui5-1-122-5d078da.md "With this release OpenUI5 is upgraded from version 1.121 to 1.122.")

[What's New in OpenUI5 1.121](what-s-new-in-openui5-1-121-91a4a2f.md "With this release OpenUI5 is upgraded from version 1.120 to 1.121.")

[What's New in OpenUI5 1.120](what-s-new-in-openui5-1-120-2359b63.md "With this release OpenUI5 is upgraded from version 1.119 to 1.120.")

[What's New in OpenUI5 1.119](what-s-new-in-openui5-1-119-0b1903a.md "With this release OpenUI5 is upgraded from version 1.118 to 1.119.")

[What's New in OpenUI5 1.118](what-s-new-in-openui5-1-118-3eecbde.md "With this release OpenUI5 is upgraded from version 1.117 to 1.118.")

[What's New in OpenUI5 1.117](what-s-new-in-openui5-1-117-029d3b4.md "With this release OpenUI5 is upgraded from version 1.116 to 1.117.")

[What's New in OpenUI5 1.116](what-s-new-in-openui5-1-116-ebd6f34.md "With this release OpenUI5 is upgraded from version 1.115 to 1.116.")

[What's New in OpenUI5 1.115](what-s-new-in-openui5-1-115-409fde8.md "With this release OpenUI5 is upgraded from version 1.114 to 1.115.")

[What's New in OpenUI5 1.114](what-s-new-in-openui5-1-114-890fce1.md "With this release OpenUI5 is upgraded from version 1.113 to 1.114.")

[What's New in OpenUI5 1.113](what-s-new-in-openui5-1-113-a9553fe.md "With this release OpenUI5 is upgraded from version 1.112 to 1.113.")

[What's New in OpenUI5 1.112](what-s-new-in-openui5-1-112-34afc69.md "With this release OpenUI5 is upgraded from version 1.111 to 1.112.")

[What's New in OpenUI5 1.111](what-s-new-in-openui5-1-111-7a67837.md "With this release OpenUI5 is upgraded from version 1.110 to 1.111.")

[What's New in OpenUI5 1.110](what-s-new-in-openui5-1-110-71a855c.md "With this release OpenUI5 is upgraded from version 1.109 to 1.110.")

[What's New in OpenUI5 1.109](what-s-new-in-openui5-1-109-3264bd2.md "With this release OpenUI5 is upgraded from version 1.108 to 1.109.")

[What's New in OpenUI5 1.108](what-s-new-in-openui5-1-108-66e33f0.md "With this release OpenUI5 is upgraded from version 1.107 to 1.108.")

[What's New in OpenUI5 1.107](what-s-new-in-openui5-1-107-d4ff916.md "With this release OpenUI5 is upgraded from version 1.106 to 1.107.")

[What's New in OpenUI5 1.106](what-s-new-in-openui5-1-106-5b497b0.md "With this release OpenUI5 is upgraded from version 1.105 to 1.106.")

[What's New in OpenUI5 1.105](what-s-new-in-openui5-1-105-4d6c00e.md "With this release OpenUI5 is upgraded from version 1.104 to 1.105.")

[What's New in OpenUI5 1.104](what-s-new-in-openui5-1-104-69e567c.md "With this release OpenUI5 is upgraded from version 1.103 to 1.104.")

[What's New in OpenUI5 1.103](what-s-new-in-openui5-1-103-0e98c76.md "With this release OpenUI5 is upgraded from version 1.102 to 1.103.")

[What's New in OpenUI5 1.102](what-s-new-in-openui5-1-102-f038c99.md "With this release OpenUI5 is upgraded from version 1.101 to 1.102.")

[What's New in OpenUI5 1.101](what-s-new-in-openui5-1-101-7733b00.md "With this release OpenUI5 is upgraded from version 1.100 to 1.101.")

[What's New in OpenUI5 1.100](what-s-new-in-openui5-1-100-27dec1d.md "With this release OpenUI5 is upgraded from version 1.99 to 1.100.")

[What's New in OpenUI5 1.99](what-s-new-in-openui5-1-99-4f35848.md "With this release OpenUI5 is upgraded from version 1.98 to 1.99.")

[What's New in OpenUI5 1.97](what-s-new-in-openui5-1-97-fa0e282.md "With this release OpenUI5 is upgraded from version 1.96 to 1.97.")

[What's New in OpenUI5 1.96](what-s-new-in-openui5-1-96-7a9269f.md "With this release OpenUI5 is upgraded from version 1.95 to 1.96.")

[What's New in OpenUI5 1.95](what-s-new-in-openui5-1-95-a1aea67.md "With this release OpenUI5 is upgraded from version 1.94 to 1.95.")

[What's New in OpenUI5 1.94](what-s-new-in-openui5-1-94-c40f1e6.md "With this release OpenUI5 is upgraded from version 1.93 to 1.94.")

[What's New in OpenUI5 1.93](what-s-new-in-openui5-1-93-f273340.md "With this release OpenUI5 is upgraded from version 1.92 to 1.93.")

[What's New in OpenUI5 1.92](what-s-new-in-openui5-1-92-1ef345d.md "With this release OpenUI5 is upgraded from version 1.91 to 1.92.")

[What's New in OpenUI5 1.91](what-s-new-in-openui5-1-91-0a2bd79.md "With this release OpenUI5 is upgraded from version 1.90 to 1.91.")

[What's New in OpenUI5 1.90](what-s-new-in-openui5-1-90-91c10c2.md "With this release OpenUI5 is upgraded from version 1.89 to 1.90.")

[What's New in OpenUI5 1.89](what-s-new-in-openui5-1-89-e56cddc.md "With this release OpenUI5 is upgraded from version 1.88 to 1.89.")

[What's New in OpenUI5 1.88](what-s-new-in-openui5-1-88-e15a206.md "With this release OpenUI5 is upgraded from version 1.87 to 1.88.")

[What's New in OpenUI5 1.87](what-s-new-in-openui5-1-87-b506da7.md "With this release OpenUI5 is upgraded from version 1.86 to 1.87.")

[What's New in OpenUI5 1.86](what-s-new-in-openui5-1-86-4c1c959.md "With this release OpenUI5 is upgraded from version 1.85 to 1.86.")

[What's New in OpenUI5 1.85](what-s-new-in-openui5-1-85-1d18eb5.md "With this release OpenUI5 is upgraded from version 1.84 to 1.85.")

[What's New in OpenUI5 1.84](what-s-new-in-openui5-1-84-dc76640.md "With this release OpenUI5 is upgraded from version 1.82 to 1.84.")

[What's New in OpenUI5 1.82](what-s-new-in-openui5-1-82-3a8dd13.md "With this release OpenUI5 is upgraded from version 1.81 to 1.82.")

[What's New in OpenUI5 1.81](what-s-new-in-openui5-1-81-f5e2a21.md "With this release OpenUI5 is upgraded from version 1.80 to 1.81.")

[What's New in OpenUI5 1.80](what-s-new-in-openui5-1-80-8cee506.md "With this release OpenUI5 is upgraded from version 1.79 to 1.80.")

[What's New in OpenUI5 1.79](what-s-new-in-openui5-1-79-99c4cdc.md "With this release OpenUI5 is upgraded from version 1.78 to 1.79.")

[What's New in OpenUI5 1.78](what-s-new-in-openui5-1-78-f09b63e.md "With this release OpenUI5 is upgraded from version 1.77 to 1.78.")

[What's New in OpenUI5 1.77](what-s-new-in-openui5-1-77-c46b439.md "With this release OpenUI5 is upgraded from version 1.76 to 1.77.")

[What's New in OpenUI5 1.76](what-s-new-in-openui5-1-76-aad03b5.md "With this release OpenUI5 is upgraded from version 1.75 to 1.76.")

[What's New in OpenUI5 1.75](what-s-new-in-openui5-1-75-5cbb62d.md "With this release OpenUI5 is upgraded from version 1.74 to 1.75.")

[What's New in OpenUI5 1.74](what-s-new-in-openui5-1-74-c22208a.md "With this release OpenUI5 is upgraded from version 1.73 to 1.74.")

[What's New in OpenUI5 1.73](what-s-new-in-openui5-1-73-231dd13.md "With this release OpenUI5 is upgraded from version 1.72 to 1.73.")

[What's New in OpenUI5 1.72](what-s-new-in-openui5-1-72-521cad9.md "With this release OpenUI5 is upgraded from version 1.71 to 1.72.")

[What's New in OpenUI5 1.71](what-s-new-in-openui5-1-71-a93a6a3.md "With this release OpenUI5 is upgraded from version 1.70 to 1.71.")

[What's New in OpenUI5 1.70](what-s-new-in-openui5-1-70-f073d69.md "With this release OpenUI5 is upgraded from version 1.69 to 1.70.")

[What's New in OpenUI5 1.69](what-s-new-in-openui5-1-69-89a18bd.md "With this release OpenUI5 is upgraded from version 1.68 to 1.69.")

[What's New in OpenUI5 1.68](what-s-new-in-openui5-1-68-f94bf93.md "With this release OpenUI5 is upgraded from version 1.67 to 1.68.")

[What's New in OpenUI5 1.67](what-s-new-in-openui5-1-67-a6b1472.md "With this release OpenUI5 is upgraded from version 1.66 to 1.67.")

[What's New in OpenUI5 1.66](what-s-new-in-openui5-1-66-c9896e9.md "With this release OpenUI5 is upgraded from version 1.65 to 1.66.")

[What's New in OpenUI5 1.65](what-s-new-in-openui5-1-65-0f5acfd.md "With this release OpenUI5 is upgraded from version 1.64 to 1.65.")

[What's New in OpenUI5 1.64](what-s-new-in-openui5-1-64-0e30822.md "With this release OpenUI5 is upgraded from version 1.63 to 1.64.")

[What's New in OpenUI5 1.63](what-s-new-in-openui5-1-63-e8d9da7.md "With this release OpenUI5 is upgraded from version 1.62 to 1.63.")

[What's New in OpenUI5 1.62](what-s-new-in-openui5-1-62-771f4d5.md "With this release OpenUI5 is upgraded from version 1.61 to 1.62.")

[What's New in OpenUI5 1.61](what-s-new-in-openui5-1-61-d991552.md "With this release OpenUI5 is upgraded from version 1.60 to 1.61.")

[What's New in OpenUI5 1.60](what-s-new-in-openui5-1-60-5a0e1f7.md "With this release OpenUI5 is upgraded from version 1.58 to 1.60.")

[What's New in OpenUI5 1.58](what-s-new-in-openui5-1-58-7c927aa.md "With this release OpenUI5 is upgraded from version 1.56 to 1.58.")

[What's New in OpenUI5 1.56](what-s-new-in-openui5-1-56-108b7fd.md "With this release OpenUI5 is upgraded from version 1.54 to 1.56.")

[What's New in OpenUI5 1.54](what-s-new-in-openui5-1-54-c838330.md "With this release OpenUI5 is upgraded from version 1.52 to 1.54.")

[What's New in OpenUI5 1.52](what-s-new-in-openui5-1-52-849e1b6.md "With this release OpenUI5 is upgraded from version 1.50 to 1.52.")

[What's New in OpenUI5 1.50](what-s-new-in-openui5-1-50-759e9f3.md "With this release OpenUI5 is upgraded from version 1.48 to 1.50.")

[What's New in OpenUI5 1.48](what-s-new-in-openui5-1-48-fa1efac.md "With this release OpenUI5 is upgraded from version 1.46 to 1.48.")

[What's New in OpenUI5 1.46](what-s-new-in-openui5-1-46-6307539.md "With this release OpenUI5 is upgraded from version 1.44 to 1.46.")

[What's New in OpenUI5 1.44](what-s-new-in-openui5-1-44-a0cb7a0.md "With this release OpenUI5 is upgraded from version 1.42 to 1.44.")

[What's New in OpenUI5 1.42](what-s-new-in-openui5-1-42-468b05d.md "With this release OpenUI5 is upgraded from version 1.40 to 1.42.")

[What's New in OpenUI5 1.40](what-s-new-in-openui5-1-40-fbab50e.md "With this release OpenUI5 is upgraded from version 1.38 to 1.40.")

[What's New in OpenUI5 1.38](what-s-new-in-openui5-1-38-f218918.md "With this release OpenUI5 is upgraded from version 1.36 to 1.38.")

