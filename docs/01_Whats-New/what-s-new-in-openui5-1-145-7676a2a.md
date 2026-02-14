<!-- loio7676a2ac551e46a69636753e4637eb89 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# What's New in OpenUI5 1.145

With this release OpenUI5 is upgraded from version 1.144 to 1.145.

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

1.145 

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

<sub>Deprecated•Feature•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.VariantManagement`** 

</td>
<td valign="top">

**`sap.m.VariantManagement`**

We have simplified the saving of views: Users can now save a new view more efficiently by pressing [Ctrl\]/ [Command\] + [Enter\] to confirm the save without having to navigate to the *Save* button. The field of the view name is now automatically focused and editable upon opening the *Save View* dialog, enhancing workflow speed and user experience. In a similar way, users can save changes in the *Manage Views* dialog by pressing [Ctrl\]/ [Command\] + [Enter\]. Also, users can now save changes of individual views in the list of views by pressing [Ctrl\]/ [Command\] + [S\]. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc/sample/sap.ui.mdc.demokit.sample.TableFilterBarJson).

<sub>Changed•Control•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

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

We have adapted the personalization in the *Adapt Filters* dialog: The new concept allows users to easily personalize filter bars while ensuring accessibility compliance with adapted screen reader announcements. This feature enhances user efficiency and satisfaction by providing a user experience that meets accessibility standards. We have made the following major changes:

-   We have moved *List View* and *Group View* to two new tab pages, *List* and *Group*.

-   All values are now always visible, so we have removed the *Show Values* button.

-   We have added the new *Sort* button under *List*, which users can use to switch to a sort mode to change the sort order of the fields. To switch back to the mode before, they can use the *Edit* button.

-   To make filters visible , users can press the *Visible* button.

-   To remove filters, users can press the *Remove* button.

-   Users can now add a new filter by selecting *Add Filter*.

-   To apply the filters, users can now use the new *Filter* button next to *OK* and *Cancel* instead of *Go*.


For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.ui.mdc.FilterBar/sample/sap.ui.mdc.demokit.sample.FilterbarTypes).

<sub>Changed•Control•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

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

-   Refreshing a single entity using `v4.Context#refresh` or `v4.Context#requestRefresh` is now supported as an experimental feature for flat lists of unaggregated records with a grand total. In this case, the grand total is updated.For more information, see the API Reference for [`v4.Context#refresh`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/refresh) and [`v4.Context#requestRefresh`](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/requestRefresh).

-   Filtering by dynamic property is now supported in data aggregation scenarios that don't use the `groupLevels` and `grandTotal` parameters.


<sub>Changed•Feature•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

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

-   The `sap.ui.mdc.Chart` control is no longer experimental. Its API has proven stable through extensive use.
-   The chart’s toolbar now provides expanded personalization options and greater flexibility for applications to position custom actions. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.Chart%23aggregations).


<sub>Changed•Control•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.PlanningCalendar`** 

</td>
<td valign="top">

**`sap.m.PlanningCalendar`**

Until now, the `showWeekNumbers` property visualized only week numbers in the views showing dates \(*Days*, *Week*, and *Month* view\). Now, we have enabled the property to display week ranges in the *Months* view. For more information, see the [Sample](https://ui5.sap.com/#/entitysap.m.PlanningCalendar/samplesap.m.sample.PlanningCalendarWeekNumbering).

<sub>Changed•Control•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
<tr>
<td valign="top">

1.145 

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

-   The updated Card Explorer documentation now includes a new section for Card actions. This section features examples of supported actions, including *Navigation*, *Submit*, *Custom \(Experimental\)*, and *Show/Hide Card \(Experimental\)*. Additionally, it includes new samples. Use it to learn how to implement interactive features, such as row-level actions, nested cards, dynamic data updates, and to show full details in a child card. For more information, see the [Card Explorer](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/exploreOverview/actionCards).
-   As part of our ongoing effort to share the latest features and capabilities of UI Integration Cards with the broader SAP community, a new comprehensive article, [Declarative UI Integration Cards - Consistent Framework With Flexible Content Capabilities](https://community.sap.com/t5/technology-blog-posts-by-sap/declarative-ui-integration-cards-consistent-framework-with-flexible-content/ba-p/14320024), is now available in the SAP Community portal's **Technology Blog Posts by SAP** section. It offers an in-depth introduction to Declarative Integration Cards.
-   We have updated one of the most popular tutorials on UI Integration Cards: [https://developers.sap.com/tutorials/appstudio-sapui5-integrationcard-create.html](https://developers.sap.com/tutorials/appstudio-sapui5-integrationcard-create.html). The tutorial now uses the Northwind data service to guide learners through configuring an Integration Card that displays dynamic data.
-   UI Integration Cards of declarative card type Table now support inverted object status. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/table) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/table/tableColumnProperties) in Card Explorer. 

<sub>Changed•Control•Info Only•1.145</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-02-19

</td>
</tr>
</table>

