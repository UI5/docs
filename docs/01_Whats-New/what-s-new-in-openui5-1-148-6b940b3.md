<!-- loio6b940b30f1294aaabfab8f918281fc94 -->

# What's New in OpenUI5 1.148

With this release OpenUI5 is upgraded from version 1.147 to 1.148.

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

1.148 

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

<sub>Deprecated•Feature•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Table` ** 

</td>
<td valign="top">

**`sap.ui.mdc.Table`**

-   The `ResponsiveTable` type of `sap.ui.mdc.Table` now supports all row action types: `Navigation`, `Delete`, and `Custom`. This brings it to feature parity with the `GridTable` type. Previously, only `Navigation` was supported.

    You can now define multiple row actions per row, including delete buttons. Two new enum values \(`Custom` and `Delete`\) have been added to `TableRowActionType`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.enums.TableRowActionType) .

-   Applications can now configure default export dialog settings via a new `defaultExportSettings` aggregation. Starting with the file name, developers can pre-populate the export dialog with default values shown to users. Additionally, any values the user has already modified in the export dialog are now preserved when `beforeExport` event handlers run, preventing those handlers from unintentionally overriding the user's input. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.export.TableExportSettings) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Table/sample/sap.ui.mdc.demokit.sample.table.TableExport).

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**Accessibility** 

</td>
<td valign="top">

**Accessibility** 

SAPUI5 is now using JAWS 2026 as a reference testing environment in SAPUI5. For more information, see the *Assistive technologies reference testing environment for SAPUI5* SAP Note [2564165](https://me.sap.com/notes/2564165).

<sub>Changed • Control • Info Only • 1.148 </sub> 

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

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

We've introduced a new `maxHeight` property in `sap.m.Popover`, giving you precise control over the popover's total height — including its header, content, and footer. This prevents the popover from growing too large or exceeding the `viewport` height in constrained layouts. When content exceeds the defined limit, scrolling is enabled automatically. The value accepts any CSS size unit, such as pixels \(300px\) or percentages \(50%\). For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Popover).

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

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

Integration Cards now automatically disable buttons and links that have no valid action configured, making it immediately clear to users which controls are interactive. Previously, such buttons appeared enabled but had no effect when selected.

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

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

The tokens popover in `sap.m.MultiInput` no longer displays an arrow when the control contains an input field. In such cases, the token list opens as a dropdown attached to the input. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.MultiInput/sample/sap.m.MultiInput). 

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

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

Integration Cards now support an optional separator line between the content and footer areas using the new `showSeparator` property in the card manifest footer configuration. This improves visual clarity, particularly for cards with dense content or multiple footer actions. The default value of this property is `false` to maintain backward compatibility with existing cards. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/footer/listWithSeparator) and the [API Reference](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/footer) in the Card Explorer.

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.MessageStrip`** 

</td>
<td valign="top">

**`sap.m.MessageStrip`**

`sap.m.MessageStrip` now supports rendering SAP icons inline within formatted text when `enableFormattedText` is set to `true`. This allows you to enrich message content with contextual icons, making messages more expressive and easier to understand at a glance. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.MessageStrip%23controlProperties).

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.MenuButton`** 

</td>
<td valign="top">

**`sap.m.MenuButton`**

`sap.m.MenuButton` now implements the `sap.ui.core.IFormContent` interface, allowing it to be used as content in the `sap.ui.layout.form.Form`, `sap.ui.layout.form.SimpleForm`, and `sap.ui.mdc.Field` aggregations — the same way the `Button` and `SegmentedButton` controls already can. This enables use cases such as placing a `MenuButton` in the toolbar of an `sap.ui.mdc.Table` to trigger actions like opening multi-select value help dialogs. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.MenuButton%23methods/Summary).

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Chart`** 

</td>
<td valign="top">

**`sap.ui.mdc.Chart`**

The `sap.ui.mdc.Chart` control now correctly handles multi-value criticality objects defined via the `@UI.ValueCriticality` annotation, rendering the appropriate semantic colors for each criticality level in both the chart and its legend. This allows users to visually distinguish between different criticality states at a glance, even when multiple values share the same level. Both single-value and multi-value criticality structures are supported.

<sub>Changed•Control•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

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

-   You can now provide `groupPaths` for an `sap.ui.model.Sorter` when creating a list binding. The binding adds these paths to the `$select` and `$expand` query options if you use auto-$expand/$select.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.Sorter%23constructor).

-   When you use data aggregation without group levels, the following features are supported experimentally:

    -   You can now create inactive single entity instances at the end of a list by providing the `bAtEnd` parameter with a value of `true` in the first call.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/create).

    -   The grand total now updates automatically unless it is marked as outdated after changes.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/isOutdated).

    -   When you change a property, the header context is marked as outdated only if that property is used in a `Sorter` or `Filter` object, or if a `$search` or custom query option is set. The grand total's context is marked as outdated if the changed property is used in a `Filter` object, or if a `$search` or custom query option is set.



<sub>Changed•Feature•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

New 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Modernization Guide** 

</td>
<td valign="top">

**Modernization Guide**

We've added a new Modernization Guide to help you move your OpenUI5 applications away from legacy code and prepare them for the future. The guide provides a consolidated, library-by-library overview of deprecated items, such as APIs, controls, themes, and patterns, along with their modern replacements and migration guidance. For more information, see [Modernization Guide](../02_Read-Me-First/modernization-guide-db49236.md).

<sub>New•User Documentation•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

New 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Documentation on ID Handling** 

</td>
<td valign="top">

**Documentation on ID Handling**

We have updated our documentation on how OpenUI5 handles IDs. Understanding ID handling is essential for building maintainable, testable, and adaptable applications. For more information, see [ID Handling in OpenUI5: The Complete Guide](../05_Developing_Apps/id-handling-in-openui5-the-complete-guide-f51dbb7.md).

<sub>New•User Documentation•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
<tr>
<td valign="top">

1.148 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Walkthrough and Quickstart Tutorials on GitHub** 

</td>
<td valign="top">

**Walkthrough and Quickstart Tutorials on GitHub**

You can now find a dedicated UI5 Tutorials repository on the UI5 GitHub organization. It contains the introductory Walkthrough and Quickstart tutorials, available in both JavaScript and TypeScript versions:

-   [Walkthrough tutorial \(JavaScript\)](https://ui5.github.io/tutorials/walkthrough/?lang=js) and [Walkthrough tutorial \(TypeScript\)](https://ui5.github.io/tutorials/walkthrough/?lang=ts)
-   [Quickstart tutorial \(JavaScript\)](https://ui5.github.io/tutorials/quickstart/?lang=js) and [Quickstart tutorial \(TypeScript\)](https://ui5.github.io/tutorials/quickstart/?lang=ts)

We're continuously adding more OpenUI5 tutorials to the repository. For more information, see [UI5 Tutorials](https://ui5.github.io/tutorials/).

<sub>Changed•User Documentation•Info Only•1.148</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-05-14

</td>
</tr>
</table>

