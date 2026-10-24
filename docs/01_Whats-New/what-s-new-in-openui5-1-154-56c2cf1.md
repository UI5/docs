<!-- loio56c2cf1bbbfa45cfa22fccb09639d3e5 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.154

With this release OpenUI5 is upgraded from version 1.153 to 1.154.

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

**End of Cloud Provisioning for OpenUI5 Versions \(Q4/2026\)** 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q4/2026\)**

The following OpenUI5 versions will be removed from the OpenUI5 Content Delivery Network \(CDN\) after the end of Q4/2026.

**Minor Versions Reaching Their End of Cloud Provisioning**

The following versions including all patches will be removed entirely:

-   1.84
-   1.141

**Action**: Upgrade to a version that is still in maintenance.

**Patch Versions Reaching Their End of Cloud Provisioning**

The following patches will be removed:

-   1.38.65
-   1.71.73 to 1.71.74
-   1.96.42
-   1.108.44 to 1.108.46
-   1.120.37 to 1.120.38
-   1.136.7 to 1.136.10
-   1.139.0 to 1.139.2
-   1.142.0

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

1.154 

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

A new `footer` aggregation \(`sap.ui.core.Control`\) has been added to `sap.ui.mdc.Table`. Table types that support a footer \(for example, `GridTableType`\) display it below the table. This allows applications to display messages to guide users in analytical edit scenarios. With `ResponsiveTableType`, the footer has no effect but it is retained and applied automatically when the table type is switched. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.Table%23methods/getFooter) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Table/sample/sap.ui.mdc.demokit.sample.table.TableTypes).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

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

<sub>Deprecated•Feature•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

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

The new version of the OpenUI5 OData V4 model introduces experimental support for the following features when using data aggregation with group levels:

-   Creating, updating, and deleting single, unaggregated records as well as calling bound actions for these records. For more information, see *Editing* in [Data Aggregation and Recursive Hierarchy](../04_Essentials/data-aggregation-and-recursive-hierarchy-7d91431.md).
-   Automatically expanding the visually grouped hierarchy by a given number of group levels using the `MultiLevelExpand` function. For more information, see [`MultiLevelExpand`](https://github.com/SAP/odata-vocabularies/blob/main/vocabularies/Analytics.md#MultiLevelExpand) and the `expandTo` parameter in the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/setAggregation).
-   The `isOutdated` method introduced in OpenUI5 1.147 for header contexts and grand total row contexts is now also available for contexts of group headers. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/isOutdated).

<sub>Changed•Feature•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Using Native HTML in XML Views** 

</td>
<td valign="top">

**Using Native HTML in XML Views**

You can now use native HTML tags directly in XML views via the new `sap.html` library, freely mixing them with OpenUI5 controls while staying in the OpenUI5 programming model. The library replaces the XHTML namespace approach, which has been deprecated since OpenUI5 1.120.

For more information, see [Using Native HTML in XML Views](../04_Essentials/using-native-html-in-xml-views-be54950.md).

<sub>Changed•Feature•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.IconTabFilter`** 

</td>
<td valign="top">

**`sap.m.IconTabFilter`**

The `interactionMode` property of `sap.m.IconTabFilter` and the associated `sap.m.IconTabFilterInteractionMode` enum are no longer experimental and are now available for productive use. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.IconTabFilter) and the [Samples](https://ui5.sap.com/#/entity/sap.m.IconTabFilter).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Popover`** 

</td>
<td valign="top">

**`sap.m.Popover`**

`sap.m.Popover` now supports keyboard-based resizing. When the resizable property is set to true and the popover has focus, you can resize it using the [Shift\] + [Arrow\]  keys. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Popover) and the [Sample](https://ui5.sap.com/#/entity/sap.m.Popover/sample/sap.m.sample.Popover).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Link`** 

</td>
<td valign="top">

**`sap.ui.mdc.Link`**

`sap.ui.mdc.Link` now supports a standalone navigation popover pattern: the link can be opened programmatically from any control using `Link.open()`, without being placed inside an `mdc:Field`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.Link) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Link/sample/sap.ui.mdc.demokit.sample.LinkCustomControl).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.ObjectNumber`** 

</td>
<td valign="top">

**`sap.m.ObjectNumber`**

`sap.m.ObjectNumber` now supports a `displayMode` property that enables column-aligned display of numbers, making values easier to compare. Use `Currency` mode for currency values, `Unit` mode for other numeric values, or keep the existing behavior with `Default` mode. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.ObjectNumber) and the [Samples](https://ui5.sap.com/#/entity/sap.m.ObjectNumber).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.NumericInput`** 

</td>
<td valign="top">

**`sap.m.NumericInput`**

The new `sap.m.NumericInput` control provides a reliable, dedicated input for numeric values, including support for minimum and maximum values, step size, and decimal precision.

This control is experimental and its API may change in future versions. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.NumericInput) and the [Samples](https://ui5.sap.com/#/entity/sap.m.NumericInput).

<sub>New•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
<tr>
<td valign="top">

1.154 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Panel`** 

</td>
<td valign="top">

**`sap.m.Panel`**

The `sap.m.Panel` now supports a new `None` value for the `accessibleRole` property. This allows developers to remove the landmark role from purely presentational panels to avoid unnecessary noise for screen reader users. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Panel).

<sub>Changed•Control•Info Only•1.154</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-29

</td>
</tr>
</table>

