<!-- loio0809f2d07bee4782bfb322b452ab3ae3 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.153

With this release OpenUI5 is upgraded from version 1.152 to 1.153.

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

**End of Cloud Provisioning for OpenUI5 Versions \(Q3/2026\)** 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q3/2026\)**

The following OpenUI5 versions will be removed from the OpenUI5 Content Delivery Network \(CDN\) after the end of Q3/2026.

**Minor Versions Reaching Their End of Cloud Provisioning**

The following versions including all patches will be removed entirely:

-   1.133
-   1.138
-   1.140

**Action**: Upgrade to a version that is still in maintenance.

**Patch Versions Reaching Their End of Cloud Provisioning**

The following patches will be removed:

-   1.71.71 to 1.71.72
-   1.84.51
-   1.96.39 to 1.96.41
-   1.108.42 to 1.108.43
-   1.120.32 to 1.120.36
-   1.133.3
-   1.136.2 to 1.136.6
-   1.138.0
-   1.140.0

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

1.153 

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

<sub>Deprecated•Feature•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.ValueHelp`** 

</td>
<td valign="top">

**`sap.ui.mdc.ValueHelp`**

Stakeholders can now consume the control in stand-alone fashion \(for example, triggered by pressing a button\) through newly public APIs. The enhancement makes APIs for connecting controls, clearing conditions, and retrieving the control available to developers.

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Table`, `sap.ui.mdc.Chart`** 

</td>
<td valign="top">

**`sap.ui.mdc.Table`, `sap.ui.mdc.Chart`**

Toolbar action separators are now enabled by default for these controls, visually grouping related actions according to the SAP Design System guidelines. Separators are automatically inserted between action groups based on the `ActionLayoutData` position property. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Table/sample/sap.ui.mdc.demokit.sample.table.TableActions).

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

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

A new `enabled` property in the `aggregationConfiguration` payload allows explicit control of data aggregation behavior, overriding the automatic detection. Setting it to `true` forces aggregation \(for supported table types\), `false` disables it completely \(ignoring variants and `p13n` modes\), and `undefined` preserves the existing auto-detection behavior. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.odata.v4.TableDelegate.Payload).

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.table.Table`** 

</td>
<td valign="top">

**`sap.ui.table.Table`**

The vertical scrollbar now includes a position indicator and draggable scroll handle that shows the current viewport range \(visible rows\). The handle appears during scrolling and automatically hides after 3 seconds of inactivity. The feature is controlled via the new `showScrollHandle` property. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.table.Table/sample/sap.ui.table.sample.Basic).

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Table`, `sap.ui.table.Table` ** 

</td>
<td valign="top">

**`sap.m.Table`, `sap.ui.table.Table` **

Keyboard shortcuts [Ctrl\] + [A\]  and [Ctrl\] + [Shift\] + [A\]  for selecting and deselecting all rows in `sap.m.Table` now function from any focused element within the table, including cells, headers, and controls like checkboxes or buttons. This enhancement provides consistent, reliable row selection behavior without requiring users to first focus a specific row.

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Input`** 

</td>
<td valign="top">

**`sap.m.Input`**

The `sap.m.Input` control has a new `descriptionAlign` property that controls the alignment of the description text within the input wrapper. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Input).

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Select`** 

</td>
<td valign="top">

**`sap.m.Select`**

`sap.m.Select` now supports grouped list items. Use `sap.ui.core.SeparatorItem` with a text property to define group headers, or the new `addItemGroup` method for programmatic grouping. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Select) and the [Samples](https://ui5.sap.com/#/entity/sap.m.Select).

<sub>Changed•Control•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
<tr>
<td valign="top">

1.153 

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

You can now filter properties of `EnumType` using `sap.ui.model.Filter`. For more information, see [EnumTypes](../04_Essentials/filtering-5338bd1.md#loio5338bd1f9afb45fb8b2af957c3530e8f__section_enumType).

<sub>Changed•Feature•Info Only•1.153</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-10-01

</td>
</tr>
</table>

