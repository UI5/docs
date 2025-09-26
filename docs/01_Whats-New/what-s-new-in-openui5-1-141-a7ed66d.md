<!-- loioa7ed66de00934a8ebd8ec054e18182ad -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.141

With this release OpenUI5 is upgraded from version 1.140 to 1.141.

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

1.141 

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

-   The new `state` property enables card developers to incorporate predefined value state icons in the Default Card Header, enhancing the card's visual status indication. This feature is useful for quickly conveying the status of a card through a status-colored, non-interactive message icon, improving clarity and user experience. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/defaultHeader/messageIcon) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/headers/default).

-   Integration Cards now offer a centralized approach to organizing child cards and referencing them by key in the `ShowCard` action type. This feature enhances semantic clarity, streamlines card management, and enables centralized configuration of child card settings through the Configuration Editor. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/cardActions/showHideCard) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/configuration/childCards).

<sub>Changed•Control•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

****`sap.ui.unified.Calendar` 

</td>
<td valign="top">

**`sap.ui.unified.Calendar`**

To improve accessibility, the tooltips for the *Month*, *Year*, and *Year Range Picker* buttons are now more descriptive. You will also find that the buttons' labels and descriptions have been improved. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.unified.Calendar/sample/sap.ui.unified.sample.CalendarSingleDaySelection).

<sub>Changed•Control•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

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

We've improved error handling by integrating `sap.m.IllustratedMessage` to provide clear explanations and guidance when chart display issues occur. This feature enhances user experience by offering informative error messages and solutions, ensuring chart compatibility and usability.

<sub>Changed•Control•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.RatingIndicator`** 

</td>
<td valign="top">

**`sap.m.RatingIndicator`**

The updated rating indicator lets you reset your rating by double-clicking the same star. This enhancement improves user experience by offering a simple way to revert to an unrated state without leaving the interface.

<sub>Changed•Control•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

</td>
<td valign="top">

New 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Component Instantiation Guide** 

</td>
<td valign="top">

**Component Instantiation Guide**

We have added a comprehensive component instantiation guide as the central resource for all component instantiation topics. It explains the different ways to instantiate components, when to use each approach, and how to migrate from older mechanisms to modern, asynchronous alternatives. This update is part of a general revision of our documentation related to OpenUI5 components. For more information, see our [Component Instantiation Guide](../04_Essentials/component-instantiation-guide-346599f.md).

<sub>New•User Documentation•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Best Practices for Developers** 

</td>
<td valign="top">

**Best Practices for Developers**

We strongly advise against directly instantiating components using their constructor. You must create the `sap.ui.core.(UI)Component` class and its subclasses only through the supported mechanisms described in our Component Instantiation Guide. For more information, see [Best Practices for Developers - Component / `manifest.json`](../03_Get-Started/best-practices-for-developers-28fcd55.md#loio28fcd55b04654977b63dacbee0552712__section_appdev) and the [Component Instantiation Guide](../04_Essentials/component-instantiation-guide-346599f.md#loio346599f0890d4dfaaa11c6b4ffa96312__section_OVW).

<sub>Changed•User Documentation•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
<tr>
<td valign="top">

1.141 

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

-   You can now use the `earlyRequests` parameter of the `sap.ui.model.odata.v4.ODataModel` with back ends that do not support the security token.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel%23constructor).

-   The `copy` parameter of `sap.ui.model.odata.v4.Context#move`, introduced experimentally with OpenUI5 1.135, is now available for productive use.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/move).

-   The new `sap.ui.model.odata.v4.ODataModel#setContinueOnError` method allows you to set the `continue-on-error` preference. If the back end applies this preference, it continues processing a batch request after a failed change set or request. Note that restrictions apply when using the `setContinueOnError` method. For more information, see [Continue-On-Error](../04_Essentials/batch-control-74142a3.md#loio74142a38e3d4467c8d6a70b28764048f__section_COE)and the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataModel%23methods/setContinueOnError).

-   In preparation for OData Version 4.01, the `sap.ui.model.odata.v4.ODataModel` now raises warnings if you use custom query options that represent system query options in OData Version 4.01. For example, in OData Version 4.0, `select` is a custom query option, but in OData Version 4.01, it is a different denomination of `$select`.


<sub>Changed•Feature•Info Only•1.141</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-02

</td>
</tr>
</table>

