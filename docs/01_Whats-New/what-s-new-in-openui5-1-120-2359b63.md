<!-- loio2359b636a11a4236bb754c2bbf31e97f -->

# What's New in OpenUI5 1.120

With this release OpenUI5 is upgraded from version 1.119 to 1.120.

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

1.120 

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

With OpenUI5 version 1.120.2, we have introduced the `findOn` function for selection plugins, which allows you to search for these plugins in a given table.

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.VariantManagement`** 

</td>
<td valign="top">

**`sap.m.VariantManagement`**

We have introduced `sap.m.VariantManagement`, which replaces `sap.ui.comp.variants.VariantManagement` and offers a set of equivalent features. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.VariantManagement).

<sub>New•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Deprecated 

</td>
<td valign="top">

Announcement 

</td>
<td valign="top">

**Deprecation of *Belize* Themes** 

</td>
<td valign="top">

**Deprecation of *Belize* Themes**

We have deprecated the *Belize* \(theme IDs: `sap_belize`, `sap_belize_plus`, `sap_belize_hcb`, `sap_belize_hcw`\) theme family as of OpenUI5 version 1.120.2.

We recommend that you switch to the *Horizon* theme family \(theme IDs: `sap_horizon`, `sap_horizon_dark`, `sap_horizon_hcb`, `sap_horizon_hcw`\).

<sub>Deprecated•Announcement•Recommended•1.120</sub>

</td>
<td valign="top">

Recommended 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.table*`** 

</td>
<td valign="top">

**`sap.ui.table*`**

-   The `sorted` property of `sap.ui.table.Column` has been deprecated. Instead, the `sortOrder` property has been enhanced to also support `None` \(using `sap.ui.core.SortOrder`\), which is now the default. To ensure backward compatibility, `sortOrder` is automatically changed from `None` to `Ascending` if the `sorted` property is set to `true`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.table.Column%23controlProperties) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.table.Table/sample/sap.ui.table.sample.Sorting).

-   We have improved the cell selection in these tables for `CellSelector` and the behavior when selecting cells and ranges.
    -   You can now use `sap.m.plugins.CellSelector` even with an inactive `DragDropConfig`. To control if the plugin is active, we have added the `enabled` property.

    -   When using the [Shift\] and [Up Arrow\], [Down Arrow\] keys for cell selection, the cell selection now takes precedence over the range selection. Pressing [Esc\] will remove the current cell selection. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.table.Table/sample/sap.ui.table.sample.SelectCopyPaste).



<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Field` \(experimental\)** 

</td>
<td valign="top">

**`sap.ui.mdc.Field` \(experimental\)**

We have enabled the autocomplete feature for this experimental control. If the user enters text into a field, the first item in the result list that matches the text typed in by the user is automatically completed.

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**`sap.m.table.ColumnWidthController`**

</td>
<td valign="top">

**`sap.m.table.ColumnWidthController`**

We have now enabled the resizing of columns for `sap.m.Table` and `sap.ui.table.Table`, and not just `sap.ui.mdc.Table`. To enable this feature, we have made `ColumnWidthController` available as an extension of `sap.m.p13n.SelectionController`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.table.ColumnWidthController), the [Sample](https://ui5.sap.com/#/entity/sap.ui.table.Table/sample/sap.m.sample.p13n.EngineGridTable) for `sap.ui.table.Table`, and the [Sample](https://ui5.sap.com/#/entity/sap.m.Table/sample/sap.m.sample.p13n.Engine) for `sap.m.Table`.

<sub>New•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

New 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Usage of Forms** 

</td>
<td valign="top">

**Usage of Forms**

To help users of forms choose the one that best suits their requirements, we have provided an overview of forms and how they can be used. For more information, see [Forms: Which One Should I Choose?](../08_More_About_Controls/forms-which-one-should-i-choose-d1d8eb0.md) .

<sub>New•User Documentation•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Announcement 

</td>
<td valign="top">

**Apply Best Practices to Become Future-Ready \(as of 1.120.2\)** 

</td>
<td valign="top">

**Apply Best Practices to Become Future-Ready \(as of 1.120.2\)**

The OpenUI5 framework has been evolving constantly, for instance to account for features in browser development \(such as modern ECMAScript support\) or their end of maintenance \(such as the end of IE11 support\). Substantial modularization efforts were a crucial step on this journey, which continues towards a future major version upgrade. In recent releases, but particularly with OpenUI5 1.120, a significant number of improvements have been introduced, for example the replacement of legacy APIs of the `Core` and `Configuration` modules.

To make sure that your code bases, that is, your OpenUI5 applications and libraries, do not become legacy but are ready for the future, please continue applying best practices. To support your efforts, we are updating the documentation in many places, with OpenUI5 1.120 but also beyond. [Best Practices for Developers](../03_Get-Started/best-practices-for-developers-28fcd55.md) aims to be a good starting point for you, collecting fundamental information and offering practical guidance. Thanks for your support!

<sub>Changed•Announcement•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Updated Configuration of the OpenUI5 Runtime** 

</td>
<td valign="top">

**Updated Configuration of the OpenUI5 Runtime**

We have implemented a modular, future-proof solution for configuration handling, and deprecated the legacy `sap.ui.core.Configuration` module. To reflect these deprecations and the entities replacing them, the API Reference has been updated and documentation on the [Deprecated Configuration API](../04_Essentials/deprecated-configuration-api-2acafbf.md) has been added \(as of 1.120.2\). For an updated list of configuration options, see [Configuration of the OpenUI5 Runtime](../04_Essentials/configuration-of-the-openui5-runtime-91f08de.md) and [Configuration Options and URL Parameters](../04_Essentials/configuration-options-and-url-parameters-91f2d03.md).

<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Reworked Walkthrough Tutorial** 

</td>
<td valign="top">

**Reworked Walkthrough Tutorial**

You can now take the Walkthrough tutorial with UI5 Tooling as our preferred development environment; the sample code for all tutorial steps has been updated to work with UI5 Tooling out of the box. We also included features of modern ECMAScript and added an additional step showing how to build an application.

For more information, see [Walkthrough Tutorial \(JavaScript\)](../03_Get-Started/walkthrough-tutorial-javascript-3da5f4b.md).

<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Localization** 

</td>
<td valign="top">

**Localization**

-   We now use the localization content of the Unicode Common Locale Data Repository \(CLDR\) version 43.0.0.

-   We now support the following additional locales \(as of 1.120.5\):

    -   mk\_MK
    -   cnr\_ME
    -   sr\_Cyrl\_RS


<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

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

The `transitionMessagesOnly` parameter is now supported by `sap.ui.model.odata.v2.ODataTreeBinding`.

<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

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

-   For recursive hierarchies, we now provide the `sap.ui.model.odata.v4.Context#isAncestorOf` API to check whether a node is an ancestor of another node.

    For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/isAncestorOf).

-   For recursive hierarchies, we provide the following **experimental APIs and features**. Note that they must not be used in productive applications yet:

    -   `sap.ui.model.odata.v4.Context#getParent` and `sap.ui.model.odata.v4.Context#requestParent` to retrieve the parent of a node

        For more information, see the API Reference for [`Context#getParent`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/getParent) and [`Context#requestParent`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/requestParent).

    -   Creating new root nodes

        For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding%23methods/create).

    -   Moving nodes to become root nodes \(as of 1.120.2\)

        For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/move).

    -   Deleting nodes, even if an initial expansion has been set using the `expandTo` parameter of `$$aggregation` / `v4.ODataListBinding#setAggregation`

        For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/delete).

    -   Creating nodes, even if an initial expansion has been set using the `expandTo` parameter of `$$aggregation` / `v4.ODataListBinding#setAggregation` \(as of 1.120.2\)

        For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4ODataListBinding%23methods/create).

    -   Moving nodes, even if the hierarchy has been fully expanded using the `expandTo` parameter of `$$aggregation` / `v4.ODataListBinding#setAggregation` \(as of 1.120.2\).

        For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/move).


-   The `withCredentials` model parameter is no longer experimental; you can now use it in productive applications.

    For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel).


<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

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

We have deprecated all entities of `sap.ui.core.Core`, except for the `ready` method. For more information, see [Deprecated Core API](../04_Essentials/deprecated-core-api-798dd9a.md) \(as of 1.120.2\)and the [API Reference](https://ui5.sap.com/#/api/sap.ui.core.Core).

We have also deprecated the entire `sap.ui.core.Configuration` module. For more information, see *Updated Configuration of the OpenUI5 Runtime* in this What's New \(as of 1.120.2\).

We have changed the status of the `sap.ui.webc` library from experimental to deprecated.

For a complete list of all deprecations, see [Deprecated APIs](https://ui5.sap.com/#/api/deprecated).

<sub>Deprecated•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**TypeScript** 

</td>
<td valign="top">

**TypeScript**

The `$...Settings` types \(the structures describing what data can be passed into constructors\) now also contain the `specialSettings` \(non-bindable data for initialization, like the `id`, `objectBindings`, `bindingContexts`, and the `componentData` for Components\).

<sub>Changed•Feature•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.tnt.SideNavigation`** 

</td>
<td valign="top">

**`sap.tnt.SideNavigation`**

We have added a new `width` property to the control. Depending on the theme, the control has a minimum width set. You can use the new property to increase the width. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.tnt.SideNavigation).

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

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

We now provide a new `date` formatter. In contrast to the existing `dateTime` formatter, the new date formatter doesn’t include time in the formatted value by default. For more information, see the [Card Formatters](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/formatters/dateAndTime) section and [Date](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/dateAndTime/date) sample in the Card Explorer.

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Avatar`** 

</td>
<td valign="top">

**`sap.m.Avatar`**

We have introduced a new `active` property that allows applications to control the avatar's active state when the user interacts with it or opens/closes the user menu. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Avatar).

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

</td>
</tr>
<tr>
<td valign="top">

1.120 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.f.FlexibleColumnLayout`** 

</td>
<td valign="top">

**`sap.f.FlexibleColumnLayout`**

Users can now easily customize the width of a column by dragging the column separators.

<sub>Changed•Control•Info Only•1.120</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-11-02

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

[What's New in OpenUI5 1.98](what-s-new-in-openui5-1-98-d9f16f2.md "With this release OpenUI5 is upgraded from version 1.97 to 1.98.")

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

