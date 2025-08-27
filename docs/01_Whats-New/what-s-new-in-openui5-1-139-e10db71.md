<!-- loioe10db71fdbd7420a879cac921b025da5 -->

# What's New in OpenUI5 1.139

With this release OpenUI5 is upgraded from version 1.138 to 1.139.

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

We have now slightly adapted the option to filter for empty dates in the dynamic date range selection: The operator used is now called *Not Specified \(empty\)*. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.condition.Operator) for `tokenTextForTypes`.

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

