<!-- loioe10db71fdbd7420a879cac921b025da5 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.139

With this release OpenUI5 is upgraded from version 1.138 to 1.139.

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

**End of Cloud Provisioning for OpenUI5 Versions \(Q3/2025\)** 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q3/2025\)**

The following OpenUI5 versions will be removed from the OpenUI5 Content Delivery Network \(CDN\) after the end of Q3/2025.

**Minor Versions Reaching Their End of Cloud Provisioning**

The following versions including all patches will be removed entirely:

-   1.121
-   1.124
-   1.125
-   1.126
-   1.127
-   1.128

**Action**: Upgrade to a version that is still in maintenance.

**Patch Versions Reaching Their End of Cloud Provisioning**

The following patches will be removed:

-   1.71.66
-   1.84.46
-   1.96.31 to 1.96.33
-   1.108.30 to 1.108.34
-   1.120.16 to 1.120.20
-   1.121.5
-   1.124.1 to 1.124.6
-   1.125.0
-   1.126.0 to 1.126.1.
-   1.127.0
-   1.128.0

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

1.139 

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

<sub>Deprecated•Feature•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.FilterBar`** 

</td>
<td valign="top">

**`sap.ui.mdc.FilterBar`**

We have now slightly adapted the option to filter for empty dates in the dynamic date range selection: The operator used is now called *Not Specified \(empty\)*. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc/src/sap/ui/mdc/condition/Operator.js) for `tokenTextForTypes`.

<sub>Changed•Control•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**`sap.m.IllustratedMessage`** 

</td>
<td valign="top">

**`sap.m.IllustratedMessage`**

We've introduced new Support Assistant rules for the `IllustratedMessage` control to identify deprecated illustration sizes and types. This update helps you maintain compatibility and adhere to the current design standards in your applications.

For more information, see [Support Assistant](../04_Essentials/support-assistant-57ccd7d.md).

<sub>New•Feature•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.OverflowToolbarTokenizer`** 

</td>
<td valign="top">

**`sap.m.OverflowToolbarTokenizer`**

We have introduced a new experimental `sap.m.OverflowToolbarTokenizer` control. It integrates the existing `sap.m.Tokenizer` into `sap.m.Toolbar` and `sap.m.OverflowToolbar`, enhancing their responsive behavior and token management capabilities. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.OverflowToolbarTokenizer) and the [Samples](https://ui5.sap.com/#/entity/sap.m.OverflowToolbarTokenizer).

<sub>New•Control•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**OpenUI5 Filters** 

</td>
<td valign="top">

**OpenUI5 Filters**

We have provided the filter operators `sap.ui.model.FilterOperator.NotAll` and `sap.ui.model.FilterOperator.NotAny`. Just like the existing operators `sap.ui.model.FilterOperator.All` and `sap.ui.model.FilterOperator.Any`, these new operators are supported only by the `sap.ui.model.odata.v4.ODataModel`.

For more information, see [Filtering with Any, All, NotAny, and NotAll](../04_Essentials/filtering-5338bd1.md#loio5338bd1f9afb45fb8b2af957c3530e8f__section_FAANN)and the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.FilterOperator%23properties).

<sub>Changed•Feature•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

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

We have enhanced selection and accessibility in the `sap.m.Menu` control:

-   We have improved the logic to keep the menu popover open when using key combinations with [Shift\] \([Shift\] + [Enter\], [Shift\] + [Spacebar\]\) and when using [Shift\] + Click. This enables users to select items within groups without closing the menu if the `ItemSelectionMode` is set to `SingleSelect` or `MultiSelect`. If `ItemSelectionMode` is set to `None`, or items are outside of a group, the menu popover will close regardless of the Shift key combination. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Menu/sample/sap.m.sample.MenuSelectable/code). 
-   We have introduced new logic for managing `aria-label` attributes for the `MenuItemGroup` based on selection mode, therefore providing clearer context on item selection options in groups. The `aria-label` attributes are tailored to the `itemSelectionMode` settings—`None`, `SingleSelect`, and `MultiSelect`—enhancing accessibility by indicating whether items are non-selectable, single-selectable, or multi-selectable, thereby aiding users who rely on assistive technologies.

<sub>Changed•Control•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
<tr>
<td valign="top">

1.139 

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

We have enhanced the pagination experience for UI Integration Cards of declarative card type Table. When opening a child card using the *Show More* option, the dialog adjusts to fit the required width without unnecessary stretching. Additionally, the table headers in the card content are now sticky, ensuring they remain visible while scrolling through extensive data sets. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/pagination/table).

<sub>Changed•Control•Info Only•1.139</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-08-07

</td>
</tr>
</table>

