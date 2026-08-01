<!-- loioe824a0e2e4ad4de9b5c0892eae43746a -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.151

With this release OpenUI5 is upgraded from version 1.150 to 1.151.

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

-   1.84
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

1.151 

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

<sub>Deprecated•Feature•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

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

A table of type `ResponsiveTable` bound to OData V4 can now be grouped by invisible columns through all regular personalization channels \(for example, the settings dialog, column menu, and `StateUtil`\). Previously, only visible columns could be grouped because properties for invisible columns might not have been loaded. This restriction has now been removed.

<sub>Changed•Control•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

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

-   When you use data aggregation without group levels, the experimental restriction is removed for `v4.Context#setKeepAlive`, `v4.ODataListBinding#create`, `v4.Context#delete`, and `v4.Context#requestSideEffects`.

-   The `v4.ODataModel#getKeepAliveContext` and `v4.ODataListBinding#getKeepAliveContext` methods now support data aggregation.
-   The `v4.ODataMetaModel#requestValueListInfo` method no longer throws an error if several value lists with fixed values are used together with the `ValueListRelevantQualifiers` annotation, but no context is provided to evaluate the `ValueListRelevantQualifiers`. In this case, all value list mappings are returned, leaving it to the application to pick the one to use. For more information, see [`ValueListRelevantQualifiers`](https://github.com/SAP/odata-vocabularies/blob/main/vocabularies/Common.md#ValueListRelevantQualifiers).
-   The `Promise` returned by `v4.ODataContextBinding#invoke` now resolves with an object containing the body with the stream and the return headers if the return type of the action or function is `Edm.Stream` and the `groupId` `$stream` is used.For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.ODataContextBinding%23methods/invoke).


<sub>Changed•Feature•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**`sap.ui.core.message.Message` and `sap/ui/core/Messaging`** 

</td>
<td valign="top">

**`sap.ui.core.message.Message` and `sap/ui/core/Messaging`**

`sap.ui.core.message.Message` now provides a public `isValidation()` method that returns `true` for messages produced by client-side type validation or parse errors \(`validationError`, `parseError`, `formatError` binding events\). Previously, this information was tracked internally but had no stable API. Use this method to distinguish framework-generated validation messages from application-created ones. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.core.message.Message%23methods/isValidation).

`sap/ui/core/Messaging` now provides a public `getMessages()` method that returns all current messages as a flat array. Previously, retrieving all messages required going through `getMessageModel().getData()`. This convenience API removes that indirection. For more information, see the [API Reference](https://ui5.sap.com/#/api/module:sap/ui/core/Messaging%23methods/sap/ui/core/Messaging.getMessages).

<sub>Changed•Feature•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**Documentation on Composite Controls** 

</td>
<td valign="top">

**Documentation on Composite Controls**

We have updated our documentation on how composite controls are implemented in OpenUI5. The revised version provides improved guidance for building composite controls and for migrating away from the deprecated `sap.ui.core.XMLComposite` class. A new topic, *Synchronizing Properties via a `$this` Model*, introduces a reusable helper pattern that reconstructs `XMLComposite`'s implicit `$this` model on a standard `sap.ui.core.Control`.

For more information, see [Composite Controls](../07_Developing_Controls/composite-controls-d6bab27.md) and [Synchronizing Properties via a $this Model](../07_Developing_Controls/synchronizing-properties-via-a-this-model-8b9014d.md).

<sub>Changed•User Documentation•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

User Documentation 

</td>
<td valign="top">

**OData V4, Data Binding, and Navigation & Routing Tutorials on GitHub** 

</td>
<td valign="top">

**OData V4, Data Binding, and Navigation & Routing Tutorials on GitHub**

The tutorials mentioned above are now available in the dedicated UI5 Tutorials repository on the UI5 GitHub organization. Each tutorial is available in both JavaScript and TypeScript versions:

-   [OData V4 tutorial \(JavaScript\)](https://ui5.github.io/tutorials/odatav4/?lang=js) and [OData V4 tutorial \(TypeScript\)](https://ui5.github.io/tutorials/odatav4/?lang=ts)
-   [Data Binding tutorial \(JavaScript\)](https://ui5.github.io/tutorials/databinding/?lang=js) and [Data Binding tutorial \(TypeScript\)](https://ui5.github.io/tutorials/databinding/?lang=ts)
-   [Navigation & Routing tutorial \(JavaScript\)](https://ui5.github.io/tutorials/navigation/?lang=js) and [Navigation & Routing tutorial \(TypeScript\)](https://ui5.github.io/tutorials/navigation/?lang=ts)

More OpenUI5 tutorials are continuously added to the repository. For more information, see [UI5 Tutorials](https://ui5.github.io/tutorials/).

<sub>Changed•User Documentation•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

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

`sap.tnt.SideNavigation` now supports search and filtering of navigation items via a new `filterSection` aggregation. Add a `sap.tnt.SideNavigationSearchField` to this aggregation to let users quickly locate items in large navigation structures — the list filters dynamically and matching items are highlighted. When search is active, footer items either move to the main list or are hidden if no matches are found. Note that search is not available when the side navigation is collapsed. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.tnt.SideNavigation/sample/sap.tnt.sample.SideNavigationSearch).

<sub>Changed•Control•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`UI Integration Cards`** 

</td>
<td valign="top">

**`UI Integration Cards`**

-   The Object Card group item now supports a `valueEntries` property, allowing a single item to display multiple values stacked vertically. This is useful for displaying multi-line addresses, multiple email links, or current versus previous values. Each entry supports its own tooltip, actions, and visibility. When provided, `valueEntries` takes precedence over `value`. Note that this property works with `Default` item types only. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/object/valueEntries) and the [API Reference](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/object) in the Card Explorer.
-   The `sap.ui.integration.widgets.Card` control now provides a `getContextDependencies()` method that returns an array of context paths the card depends on from its manifest. This allows host applications to detect context dependencies early and activate loading placeholders before the card renders. Note that this method is experimental and its API may change in future versions. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.integration.widgets.Card/methods/getContextDependencies).
-   The card manifest now supports a `badges` property in `sap.card/badges`, allowing card developers to define badges declaratively. This lets the back end determine which badges to display at render time without requiring host application code. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/badges/basic) and the [API Reference](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/features/badges) in the Card Explorer.


<sub>Changed•Control•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Geomap`** 

</td>
<td valign="top">

**`sap.ui.mdc.Geomap`**

`GeomapLegendControl` is now available in `sap.ui.mdc.Geomap` for displaying map legends. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.Geomap/sample/sap.ui.mdc.demokit.sample.Geomap.choroplethMap).

<sub>Changed•Control•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
<tr>
<td valign="top">

1.151 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.unified.Calendar`** 

</td>
<td valign="top">

**`sap.ui.unified.Calendar`**

`sap.ui.unified.Calendar` and `sap.ui.unified.calendar.Month` now support a `showWeekNumbersHeader` Boolean property that controls whether a "Calendar Week" abbreviation \(*CW*\) is shown in the header cell of the week number column. This helps users identify the column more easily, improving usability. The abbreviation is hidden by default. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.unified.Calendar).

<sub>Changed•Control•Info Only•1.151</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-08-06

</td>
</tr>
</table>

