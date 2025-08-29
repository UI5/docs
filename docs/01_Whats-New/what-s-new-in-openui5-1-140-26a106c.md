<!-- loio26a106cc313d48e6b52b78c7c331f818 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.140

With this release OpenUI5 is upgraded from version 1.139 to 1.140.

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

1.140 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Tree`, `sap.ui.table.Table`, `sap.ui.table.TreeTable`** 

</td>
<td valign="top">

**`sap.ui.table.Table`, `sap.ui.table.TreeTable`**

To provide basic support of the OpenUI5 OData V4 model, we have made the `ODataV4SingleSelection` and `ODataV4MultiSelection` plugins available for tables in `sap.ui.table` to support the selection features of `sap.ui.model.odata.v4.ODataListBinding`. Also, we have made the `ODataV4Aggregation` and `ODataV4Hierarchy` plugins available to support the hierarchical data and data aggregation features of `sap.ui.model.odata.v4.ODataListBinding`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.table) for the V4 plugins.

<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.p13n`\*** 

</td>
<td valign="top">

**`sap.m.p13n`\***

We have adapted the validation for *Filter* in the *View Settings* dialog \(`sap.m.p13n`\): Application developers can now provide a warning if users enter, for example, an amount without specifying a currency in an `sap.ui.mdc.Chart` \(experimental\) or `sap.ui.mdc.Table` or in the *Adapt Filters* dialog. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.FilterDelegateObject) for tables and charts and the [API Reference](https://ui5.sap.com/#/api/module:sap/ui/mdc/FilterBarDelegate%23methods/sap/ui/mdc/FilterBarDelegate.determineValidationState) for the filter bar.

<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

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

-   You can now bind the count of a collection-valued navigation property without binding the entire collection. For more information, see [Binding A Navigation Property's Count](../04_Essentials/binding-collection-inline-count-77d2310.md#loio77d2310b637b490495d78b393ed6aa64__section_BNPC).

-   Within a `$batch` request, a `GET` request caused by refreshing a list binding's row context is now merged with additional property `GET` requests for the same entity.


<sub>Changed•Feature•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Typed JSON Model for TypeScript Projects** 

</td>
<td valign="top">

**Typed JSON Model for TypeScript Projects**

We have introduced `sap.ui.model.json.TypedJSONModel` and `sap.ui.model.json.TypedJSONContext` as strongly-typed wrappers around `sap.ui.model.json.JSONModel` and `sap.ui.model.Context`. These wrappers don't affect runtime behavior. They enable autocompletion features in IDEs and support static type checking during development. Note that these wrappers aren't available in JavaScript projects. For more information, see [Using the Typed JSON Model](../04_Essentials/json-model-96804e3.md#loiob8cd1692485d4108af607af347982dd9).

<sub>Changed•Feature•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.MessagePopover`** 

</td>
<td valign="top">

**`sap.m.MessagePopover`**

The `MessagePopover` control now includes a title in its header, ensuring compliance with accessibility guidelines and offering clearer context for the content presented.

<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.f.ProductSwitchItem`** 

</td>
<td valign="top">

**`sap.f.ProductSwitchItem`**

The `ProductSwitchItem` control now supports custom images through the new `imageSrc` property, enabling developers to display distinct, branded icons. This feature improves visual appeal while ensuring consistent alignment and sizing. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.f.ProductSwitchItem%23overview).

<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

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

We have introduced updates to align with the latest design and accessibility specification. Key changes include:

-   The [Space\] and [Enter\] keys now exhibit equivalent behavior for both single-click and dual-click items and consistently trigger navigation actions. When navigation items are in a collapsed state, these keys now open a popover for items with sub-items.

-   ARIA labels have been added for submenus.

-   Parent items are replicated within submenus to maintain context for selectable items with child elements.

-   An `aria-description` attribute has been added for dual-click parent menu items.


<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
<tr>
<td valign="top">

1.140 

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

-   We have added a new property `useMainDestinations` that allows child cards to access and use destinations specified in main cards. Destination management is now streamlined by centralizing configuration within the main card, resulting in a cleaner and more efficient setup for complex card hierarchies. This enhancement is especially useful for hosting environments that need to process main card manifests to manage destinations. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/destinations/childCardUsingDestinations) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/configuration/destinations) in the Card Explorer.

-   We have updated Integration Cards to align with the latest design guidelines concerning header layout. Rendering order is updated to prioritize actions, followed by status text and date timestamp. When both the `status` and `dataTimestamp` are displayed, they will now appear below the *Actions* button in the header, if custom actions are attached to the card. If no custom actions are present, the `status` or `dataTimestamp` will remain in the top-right corner position. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/list/myCampaigns) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/headers/default) in the Card Explorer.


<sub>Changed•Control•Info Only•1.140</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-09-04

</td>
</tr>
</table>

