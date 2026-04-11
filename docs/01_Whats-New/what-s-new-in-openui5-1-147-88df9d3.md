<!-- loio88df9d3d47294528a421428bf0323a13 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.147

With this release OpenUI5 is upgraded from version 1.146 to 1.147.

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

1.147 

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

<sub>Deprecated•Feature•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.List, sap.m.Table, sap.m.Tree`** 

</td>
<td valign="top">

**`sap.m.List, sap.m.Table, sap.m.Tree`**

We have changed the navigation indicator icon to a button. This feature improves accessibility and usability by providing clearer interaction patterns, keyboard navigation using [Enter\] as the keyboard shortcut, and consistent alignment when combined with custom actions in tables. For more information, see the [Samples](https://ui5.sap.com/#/entity/sap.m.Table).

<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Revamping of Theming Documentation** 

</td>
<td valign="top">

**Revamping of Theming Documentation**

We've restructured and revised the documentation for theming capabilities. It enables developers to understand how theming works in OpenUI5, from theme configuration and CSS custom properties to creating themable UIs and custom themes. For more information, see [Theming](../04_Essentials/theming-497c27a.md).

<sub>Changed•User Documentation•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.table.Title`** 

</td>
<td valign="top">

**`sap.m.table.Title`**

We have introduced a new `Title` control that displays the number of selected rows and the total number of rows within tables. The count information is shown alongside the header, with compact and extended display modes. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.table.Title) and the [Sample](https://ui5.sap.com/#/entity/sap.m.Table/sample/sap.m.sample.TableMultiSelectMode).

<sub>New•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.test.Opa5`** 

</td>
<td valign="top">

**`sap.ui.test.Opa5`**

We've introduced a `rightClick` property to the OPA `Press` action. When `true`, the action fires a native `contextmenu` event instead of a `click`, enabling automated tests to open and verify custom context menus on controls such as `sap.ui.table.Table` and `sap.m.Table`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.test.actions.Press%23controlProperties) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.test.Opa5/sample/sap.ui.core.sample.OpaTableAction).

<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.uxap.ObjectPageLayout`** 

</td>
<td valign="top">

**`sap.uxap.ObjectPageLayout`**

The `ObjectPageLayout` control now supports responsive header avatars. The new `breakpointChange` event allows the `ObjectPageLayout` header content to react to container media ranges, so avatars automatically resize. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.uxap.ObjectPageLayout) and the [Sample](https://ui5.sap.com/#/entity/sap.uxap.ObjectPageLayout/sample/sap.uxap.sample.ObjectPageResponsiveAvatar). 

<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.f.DynamicPage`** 

</td>
<td valign="top">

**`sap.f.DynamicPage`**

The `DynamicPage` control now supports responsive header avatars. The new `breakpointChange` event allows the `DynamicPage` header content to react to container media ranges, so avatars automatically resize. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.f.DynamicPage%23overview) and the [Sample](https://ui5.sap.com/#/entity/sap.f.DynamicPage/sample/sap.f.sample.DynamicPageResponsiveAvatar).

<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Deleted 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Removal of `sap.ui.webc.common`, `sap.ui.webc.main`, and `sap.ui.webc.fiori`** 

</td>
<td valign="top">

**Removal of `sap.ui.webc.common`, `sap.ui.webc.main`, and `sap.ui.webc.fiori`**

The experimental `sap.ui.webc.*` libraries, deprecated in OpenUI5 1.120, have now been removed. They are replaced by the Seamless Web Components concept, which provides a more flexible and future-proof way to integrate web components into OpenUI5 applications and removes the need for the `sap.ui.webc` wrapper libraries.

**Action:** If you use any `sap.ui.webc.*` libraries in your projects, migrate to Seamless Web Components. For more information, see [Using Web Components](../04_Essentials/using-web-components-1c80793.md).

<sub>Deleted•Feature•Required•1.147</sub>

</td>
<td valign="top">

Required 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

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

Samples are now available for the Bound Filters feature, which was introduced with OpenUI5 1.146. For more information, see [Bound Filters](../04_Essentials/sorting-grouping-and-filtering-for-list-binding-ec79a5d.md#loioec79a5d5918f4f7f9cbc2150e66778cc__section_BF) and the [Samples](https://ui5.sap.com/#/entity/sap.ui.model.Filter).

<sub>Changed•Feature•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

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

-   Creating inactive single entity instances. The first call must provide the `bAtEnd` parameter with a falsy value.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/create).

-   The `sap.ui.model.odata.v4.Context#isOutdated` function and the `@$ui5.context.isOutdated` client-side annotation are now available for the header context and the grand total row context. An outdated header context indicates that refreshing the list using `ODataListBinding#refresh` might reorder records or remove them from the list. An outdated grand total context means the grand total numbers might be incorrect, so you shouldn't display the grand total. You can display it again after you refresh the list.

    For more information, see the API Reference for [`v4.Context#isOutdated`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/isOutdated) and [`v4.ODataListBinding#refresh`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/refresh).

-   Performance is improved when you request side effects for contexts that represent single entity instances. We introduced this feature as experimental in OpenUI5 1.146.


<sub>Changed•Feature•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Switch`** 

</td>
<td valign="top">

**`sap.m.Switch`**

We have added a read-only mode by introducing the `editable` property. When set to `false`, the switch displays its current state but prevents user interaction, while remaining focusable. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Switch).

<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
<tr>
<td valign="top">

1.147 

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

-   We have introduced an option to display a navigation arrow indicator in UI Integration Cards of type List and Table. The arrow indicator —*"\>"* — will now appear at the item or row level whenever a navigation action is defined. For more information, see the [List Card Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/navigationCardActions/listNavigationArrow) and the [Table Card Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/navigationCardActions/tableNavigationArrow) in Card Explorer.

-   Columns in UI Integration Cards of type Table now support pop-in behavior. This is achieved through five new properties:

    -   The `autoPopinMode` property automatically calculates column breakpoints based on importance levels, eliminating the need for manual screen width configurations.
    -   The `importance` property defines column priority \(`High`, `Medium`, `Low`, or `None`\), determining the order in which columns pop in on smaller screens.
    -   The `hiddenInPopin` property accepts an array of importance levels that should be hidden entirely when popped in, rather than displayed below the row.
    -   The `popinLayout`property controls the visual layout of the pop-in area, with options for `Block`, `GridLarge`, and `GridSmall` layouts.
    -   The `autoPopinWidth` property sets a width threshold \(in rem units\) for flexible-width columns, enabling precise control over when specific columns pop in.

    These properties allow table cards to adapt across screen sizes, ensuring usability and readability. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/table/popin) in Card Explorer. 

-   The `baseUrl` property is no longer experimental and is now supported for production use. It serves as the base path for resolving relative URLs in card manifests, including data requests, icon paths, i18n resource bundles, and extension modules. Additionally, the `getRuntimeUrl()` method has been deprecated and replaced by the new `resolveUrl()` method. For more information, see the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/integrate/usage) in Card Explorer.


<sub>Changed•Control•Info Only•1.147</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-04-16

</td>
</tr>
</table>

