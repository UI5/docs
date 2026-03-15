<!-- loio6ccfe053009944079b5e1d6d516d3de9 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.146

With this release OpenUI5 is upgraded from version 1.145 to 1.146.

> ### Note:  
> Content marked as <span style="color:#666666;"><span class="SAP-icons-V5"></span></span>**[Preview](https://help.sap.com/docs/whats-new-disclaimer)** is provided as a courtesy, without a warranty, and may be subject to change. For more information, see the [preview disclaimer](https://help.sap.com/docs/whats-new-disclaimer).

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

Upcoming 

</td>
<td valign="top">

Deleted 

</td>
<td valign="top">

Announcement 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q1/2026\)** 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q1/2026\)**

The following OpenUI5 versions will be removed from the OpenUI5 Content Delivery Network \(CDN\) after the end of Q1/2026.

**Minor Versions Reaching Their End of Cloud Provisioning**

The following versions including all patches will be removed entirely:

-   1.124
-   1.127
-   1.130
-   1.131
-   1.132

**Action**: Upgrade to a version that is still in maintenance.

**Patch Versions Reaching Their End of Cloud Provisioning**

The following patches will be removed:

-   1.38.63
-   1.71.68 to 1.71.69
-   1.84.48 to 1.84.49
-   1.96.36 to 1.96.37
-   1.108.38 to 1.108.39
-   1.120.24 to 1.120.27
-   1.124.9
-   1.127.5
-   1.130.2 to 1.130.5
-   1.131.1
-   1.132.0 to 1.132.1

**Action**: Upgrade to the latest available patch for the respective OpenUI5 version.

For more information, see [Version Overview](https://sdk.openui5.org/versionoverview.html).

<sub><span style="color:#666666;"><span class="SAP-icons-V5"></span></span>**[Preview](https://help.sap.com/docs/whats-new-disclaimer)**•Deleted•Announcement•Info Only•Upcoming</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

9999-01-01

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Deprecated 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Deprecations** 

</td>
<td valign="top">

**Deprecations**

There are currently no major deprecations. For a complete list of all deprecations, see [Deprecated APIs](https://ui5.sap.com/#/api/deprecated).

<sub>Deprecated•Feature•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Table`** 

</td>
<td valign="top">

**`sap.ui.mdc.Table`**

The selected row count is now displayed in table headers next to the total row count. If the `showRowcount` property is set to `true`, this feature automatically updates the header to show how many items are currently selected, making it easier to track selections in large data sets and improving user awareness during multi-select operations in OData-V4-based tables. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Table/sample/sap.ui.mdc.demokit.sample.table.UploadSetwithTablePlugin).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Models** 

</td>
<td valign="top">

**Models**

The `value1` and `value2` parameters of `sap.ui.model.Filter` now support data binding. For more information, see [Bound Filters](../04_Essentials/sorting-grouping-and-filtering-for-list-binding-ec79a5d.md#loioec79a5d5918f4f7f9cbc2150e66778cc__section_BF)and the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.Filter).

<sub>Changed•Feature•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

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

-   Experimental support for the following features when using data aggregation without group levels:

    -   Creating single entity instances. The first call must provide the `bAtEnd` parameter with a falsy value.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/create).

    -   Applying side effects on contexts that represent single entity instances.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/requestSideEffects).


-   The new `sap.ui.model.odata.v4.ODataModel#requestSideEffects` method enables applying side effects to all bindings matching specified absolute paths at the model level.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel%23methods/requestSideEffects).


<sub>Changed•Feature•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.FormattedText`** 

</td>
<td valign="top">

**`sap.m.FormattedText`**

Support for the HTML strikethrough tag \(<s\>\) has been added to the list of allowed tags in the control, enabling application developers to use strikethrough formatting.

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.f.SidePanel`** 

</td>
<td valign="top">

**`sap.f.SidePanel`**

A new `title` aggregation has been added to the `SidePanelItem`. This aggregation accepts the `sap.m.Title` control, enabling application developers to set title properties directly, such as the heading level and text styling, without requiring extra control APIs. If no title is specified, the control preserves backward compatibility by creating a default title as before. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.f.SidePanel).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Menu`** 

</td>
<td valign="top">

**`sap.m.Menu`**

A new `open` event is introduced, which is fired after the menu has been opened. Application developers can now reliably determine when a menu has finished opening. The `open` event complements the existing `closed` event, providing consistent lifecycle event handling for opening and closing the menu. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Menu%23events/Summary).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

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

We have improved the keyboard handling. It now moves through appointments in visual order from earliest to latest. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.SinglePlanningCalendar/sample/sap.m.sample.SinglePlanningCalendar).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.DatePicker`, `sap.m.DateTimePicker`, `sap.m.DateRangeSelection`** 

</td>
<td valign="top">

****`sap.m.DatePicker`, `sap.m.DateTimePicker`, `sap.m.DateRangeSelection`****

The mobile dialog implementations of the controls have been updated to display a *Cancel* button in the footer. Additionally, a default *Select* title is displayed when no external labels are associated with the control. These changes align with the Horizon visual design specification.

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Dialog`** 

</td>
<td valign="top">

**`sap.m.Dialog`**

The control's accessibility has been enhanced. When dialogs are draggable or resizable, the visual focus now targets the dialog itself instead of the header. The initial focus is set to the first focusable element within the dialog. You can reach the drag and resize focus handler using the *Tab* key, while mouse dragging continues on the header. Screen readers provide instructions on how to interact with the dialog. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Dialog/sample/sap.m.sample.Dialog).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Carousel`** 

</td>
<td valign="top">

**`sap.m.Carousel`**

Responsive layout mode is now available. The number of visible pages in the carousel automatically adjusts to the available width. To enable responsive layout, set the `responsive`property in the `customLayout` to `true`. Additionally, you can define a minimum page width \(in pixels\) using the `minPageWidth` property. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Carousel/sample/sap.m.sample.CarouselWithDisplayOptions).

<sub>Changed•Control•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
<tr>
<td valign="top">

1.146 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**`sap.ui.mdc.Chart`** 

</td>
<td valign="top">

**`sap.ui.mdc.Chart`**

We've added a new exercise to the UI5 MDC Tutorial on GitHub. This hands-on example demonstrates how to integrate a `Chart.js` with the MDC Chart control. For more information, see [Exercise 7: How to Use the MDC Chart with Chart.js](https://github.com/SAP-samples/ui5-mdc-json-tutorial/tree/main/u3/ex1).

<sub>Changed•User Documentation•Info Only•1.146</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-03-19

</td>
</tr>
</table>

