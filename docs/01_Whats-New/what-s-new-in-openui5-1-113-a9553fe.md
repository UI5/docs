<!-- loioa9553fe29f174452ae86de7b6da4b5f6 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.113

With this release OpenUI5 is upgraded from version 1.112 to 1.113.

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

1.113 

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

We have further improved the usability and accessibility of the *View Settings* dialog: You can now move items up and down using keyboard shortcuts. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.comp.smarttable.SmartTable/sample/sap.ui.comp.sample.smarttable).

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

<sub>Deprecated•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Code Coverage Powered by `Istanbul`** 

</td>
<td valign="top">

**Code Coverage Powered by `Istanbul`**

OpenUI5 already provides a deep integration of `QUnit` and code coverage measurement. We now introduce `Istanbul` as a modern JavaScript code instrumenter, which is intended to eventually replace the former, now legacy solution based on `Blanket.js`.

To start taking advantage of the more future-proof and feature-rich `Istanbul` solution, see the updated [code coverage documentation](../04_Essentials/code-coverage-measurement-7ef3242.md).

<sub>Changed•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**OpenUI5 Date and Time Formatting** 

</td>
<td valign="top">

**OpenUI5 Date and Time Formatting**

The new version of OpenUI5 introduces the following formatting features:

-   You can now centrally configure calendar week numbering via the new `calendarWeekNumbering` configuration parameter. Note that the `calendarWeekNumbering` format option introduced with OpenUI5 1.108 for `sap.ui.core.format.DateFormat` overrules the central configuration.

    For more information, see [Configuration Options and URL Parameters](../04_Essentials/configuration-options-and-url-parameters-91f2d03.md).

-   We provide the new `intervalDelimiter` format option for `sap.ui.core.format.DateFormat`. If an `intervalDelimiter` is set, the locale-specific rules for displaying a range as defined in the Common Locale Data Repository are overruled; the two parts of the range are formatted individually, and the given delimiter is used.


<sub>Changed•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

-   You can now delete nested transient records that were created using the experimental Deep Create feature provided with OpenUI5 1.112. Any initial data handed over to `sap.ui.model.odata.v4.ODataListBinding#create` can now contain nested entities.

    For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataListBinding/methods/create).

-   In read-only scenarios, you can now combine the experimental hierarchy feature introduced with OpenUI5 1.105 with the `sap.ui.model.odata.v4.Context#setKeepAlive` and `sap.ui.model.odata.v4.ODataModel#getKeepAliveContext` data synchronization methods described in [Data Reuse](../04_Essentials/data-reuse-648e360.md).

    For more information, see the API Reference for [`setKeepAlive`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context/methods/setKeepAlive) and [`getKeepAliveContext`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel/methods/getKeepAliveContext).

-   The `sap.ui.model.odata.v4.Context#resetChanges` API introduced as an experimental feature with OpenUI5 1.109 is now generally available.

    For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context/methods/resetChanges).


<sub>Changed•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

You can now prevent the activation of a new inactive entity by using `sap.ui.base.Event#preventDefault` in the handler of the `createActivate` event of an `sap.ui.model.odata.v2.ODataListBinding`. Note that user input into inactive rows is regarded as a pending change by `sap.ui.model.odata.v2.ODataModel#hasPendingChanges`; it can be reset using `sap.ui.model.odata.v2.ODataModel#resetChanges`.

For more information, see the API Reference for [`hasPendingChanges`](https://ui5.sap.com/#/api/sap.ui.model.odata.v2.ODataModel/methods/hasPendingChanges), [`resetChanges`](https://ui5.sap.com/#/api/sap.ui.model.odata.v2.ODataModel/methods/resetChanges), and [`Event.preventDefault`](https://ui5.sap.com/#/api/sap.ui.base.Event/methods/preventDefault).

<sub>Changed•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.112

</td>
<td valign="top">

Deleted 

</td>
<td valign="top">

Announcement 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q1/2023\)** 

</td>
<td valign="top">

**End of Cloud Provisioning for OpenUI5 Versions \(Q1/2023\)**

> ### Note:  
> The following information concerns important upcoming changes for end users. These changes may require end users to adjust and/or test cases to be adapted, but they won't stop or disrupt software or processes.

The following OpenUI5 versions will be removed from the OpenUI5 Content Delivery Network \(CDN\) after the end of Q1/2023.

**Minor Versions Reaching Their End of Cloud Provisioning**

The following versions including all patches will be removed entirely:

-   1.90
-   1.93
-   1.97
-   1.98

Action: Upgrade to a version that’s still in maintenance.

**Patch Versions Reaching Their End of Cloud Provisioning**

The following patches will be removed:

-   Long-term maintenance versions:

    -   1.38.52 to 1.38.53
    -   1.71.40-1.71.43
    -   1.84.20 to 1.84.22
    -   1.96.3 to 1.96.6

    Action: Upgrade to the latest available patch for the respective OpenUI5 version.


For more information, see [UI5 Releases Ending Service in 2023](https://blogs.sap.com/2022/12/05/ui5-releases-ending-service-in-2023/) and [Version Overview](https://sdk.openui5.org/versionoverview.html).

<sub>Deleted•Announcement•Required•1.112</sub>

</td>
<td valign="top">

Required 

</td>
<td valign="top">

2023-03-31

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

-   Using the new `customStateIcon` property, you can now set custom state-icons for the items in Table, List, and Object cards. Before this change, states like `Error`, `Warning`, `Success`, or `Information`, only had default icons. For more information, see the [Table Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/table) section and the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/table/visibleColumns) in the Card Explorer.

-   Integration cards now support the `IllustratedMessage` control to provide more informative and consistent error messages. When the application is in debug mode \(when the URL parameter `sap-ui-debug=true` is set\), the *Show More* button opens a dialog with relevant additional \(more technical\) information.

-   We have enhanced the Table card with several new properties:

    -   You can use the new `highlight` property to show the state of each table row. Additionally, the `highlightText` property conveys the semantic of this state for better accessibility.
    -   The `additionalText` property gives you the option to display additional text in the table identifier column.

    For more information, see the [Table Card](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/table) section and the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/table/highlight) in the Card Explorer. 


<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**`sap.ui.test.Opa5`** 

</td>
<td valign="top">

**`sap.ui.test.Opa5`**

We have introduced a new `fetchWaiter`, which checks for currently ongoing fetch requests.

<sub>Changed•Feature•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.SuggestionsPopover`** 

</td>
<td valign="top">

**`sap.m.SuggestionsPopover`**

We have restricted the width of input suggestions to a maximum of 40 rem for optimal user experience. Limiting the width of suggestions allows users to easily scan and select options. However, if the input field is wider than 40 rem, the width of the suggestions matches the input’s width.

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.IllustratedMessage`** 

</td>
<td valign="top">

**`sap.m.IllustratedMessage`**

We have introduced a new `Survey` illustration type and four new illustrations to the default illustration set: `sapIllus-Dialog-NoColumnsSet`, `sapIllus-Dot-NoColumnsSet`, `sapIllus-Scene-NoColumnsSet`, and `sapIllus-Spot-NoColumnsSet`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.IllustratedMessage). 

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.unified.FileUploader`** 

</td>
<td valign="top">

**`sap.ui.unified.FileUploader`**

We have implemented two new methods in the control's API, a trigger to open the native file upload picker and a getter to return the file input type element from the control DOM representation.

For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.unified.FileUploader). 

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

We have implemented an **enabled** property to the Side Panel item, which disables the controls and UI elements inside it.

For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.f.SidePanel/sample/sap.f.sample.SidePanel). 

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

</td>
</tr>
<tr>
<td valign="top">

1.113 

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

We have implemented a new mode to select one or more dates in **SinglePlanningCalendar**. Тhe single day option is enabled by default, the multi-date selection option is possible by using a key combination \([Ctrl\] + [Meta key\]  and select the dates\) or by activating the new **MultiDateSelectionMode** property.

For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.SinglePlanningCalendar/sample/sap.m.sample.SinglePlanningCalendarDateSelection). 

<sub>Changed•Control•Info Only•1.113</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2023-04-20

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

