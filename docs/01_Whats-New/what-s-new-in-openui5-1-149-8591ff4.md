<!-- loio8591ff45464a40dda698b719fecbdccb -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.149

With this release OpenUI5 is upgraded from version 1.148 to 1.149.

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

1.149 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Announcement 

</td>
<td valign="top">

**Demo Kit** 

</td>
<td valign="top">

**Demo Kit**

An Illustration Explorer is now available in the Demo Kit Resources. Use it to browse the available UI5 illustrations, preview them across sets and themes, and find the right illustration for your app flows and empty states. For more information, see the [Resources](https://ui5.sap.com/#/resources). 

<sub>New•Announcement•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

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

The recurring concept, introduced in version 1.128 for non-working time periods, is now extended to appointments. You can define recurring appointments for any period type — daily, weekly, monthly, or custom occurrences. For example, a weekly 1:1 every Monday at 11 AM or a daily standup every workday at 10 AM. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.SinglePlanningCalendar/sample/sap.m.sample.SinglePlanningCalendarRecurringItem).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.uxap.ObjectPageSection`** 

</td>
<td valign="top">

**`sap.uxap.ObjectPageSection`**

Key users can now add an IFrame as a subsection within an existing `sap.uxap.ObjectPageSection` using UI Adaptation. Previously, IFrames could only be added as standalone sections in an ObjectPageLayout. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.uxap.ObjectPageSection).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.tnt.NavigationListItem`** 

</td>
<td valign="top">

**`sap.tnt.NavigationListItem`**

You can now add tags to navigation list items using the new `tag` aggregation. Tags use `sap.m.ObjectStatus` to display status indicators, counters, and metadata, such as *Beta*, *New*, *5 Pending*, or *Critical*, directly on navigation entries. Tags are visible when the navigation list is expanded and hidden when collapsed. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.tnt.NavigationListItem) and the [Samples](https://ui5.sap.com/#/entity/sap.tnt.NavigationListItem).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

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

The arrow icon in `sap.m.Panel` is now animated when the panel expands or collapses. The animation plays when the animation mode is set to Basic or Full. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Panel%23overview).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.MultiComboBox`** 

</td>
<td valign="top">

**`sap.m.MultiComboBox`**

Invalid or incomplete values entered by the user are now cleared from the input field when focus leaves the control. Valid selected tokens are not affected. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.MultiComboBox).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.MultiInput`** 

</td>
<td valign="top">

**`sap.m.MultiInput`**

The *n More* /*n Items* overflow popover in `sap.m.MultiInput` now uses the associated label as its title in the mobile full-screen dialog. If no label is available, it falls back to *All Items*.

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Tokenizer`** 

</td>
<td valign="top">

**`sap.m.Tokenizer`**

Pressing [Esc\] in `sap.m.Tokenizer` now deselects all selected tokens, aligning the behavior with `sap.m.MultiInput` and `sap.m.MultiComboBox`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Tokenizer) and the [Samples](https://ui5.sap.com/#/entity/sap.m.Tokenizer).

<sub>Changed•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Deprecated 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.ActionSheet`** 

</td>
<td valign="top">

**`sap.m.ActionSheet`**

We have deprecated `sap.m.ActionSheet`. Use `sap.m.Menu` and `sap.m.MenuItem` instead. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.ActionSheet). 

<sub>Deprecated•Control•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Built-in Browser Console Debug Utilities** 

</td>
<td valign="top">

**Built-in Browser Console Debug Utilities**

A global `ui5` object in the browser console now provides convenient access to modules, controls, and framework internals for interactive inspection and debugging. The provided utilities are experimental and may change or be removed in future versions. For more information, see [Experimental Debug Tools](../04_Essentials/debugging-c9b0f8c.md#loio81526aa4f21944109eef190bc06767b1).

<sub>Changed•Feature•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**`sap.ui.model.odata.type.ODataType`** 

</td>
<td valign="top">

**`sap.ui.model.odata.type.ODataType`**

The `sap.ui.model.odata.type.ODataType#getPlaceholderText` method now accepts two new optional parameters, `oMinimum` and `oMaximum`. You can use them to compute a placeholder that fits within a specific date range. This feature is available for all OData types that use `sap.ui.core.format.DateFormat` for formatting:

-   `sap.ui.model.odata.type.Date`
-   `sap.ui.model.odata.type.DateTime`
-   `sap.ui.model.odata.type.DateTimeOffset`
-   `sap.ui.model.odata.type.DateTimeWithTimezone`
-   `sap.ui.model.odata.type.Time`
-   `sap.ui.model.odata.type.TimeOfDay`

For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.type.ODataType%23methods/getPlaceholderText).

<sub>Changed•Feature•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
<tr>
<td valign="top">

1.149 

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

The new version of the OpenUI5 OData V4 model introduces experimental support for the following features when using data aggregation without group levels:

-   When a side effect changes a property, the header context is marked as outdated only if that property is used in a `Sorter` or `Filter` object, or if a `$search` or custom query option is set. The grand total's context is marked as outdated if the changed property is used in a `Filter` object, or if a `$search` or custom query option is set.

-   The `groupPaths` provided with an `sap.ui.model.Sorter` are evaluated when you apply these sorters using `sap.ui.model.odata.v4.ODataListBinding#sort`. The binding adds these paths to the `$select` and `$expand` query options if you use auto-$expand/$select. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/sort).


<sub>Changed•Feature•Info Only•1.149</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-06-11

</td>
</tr>
</table>

