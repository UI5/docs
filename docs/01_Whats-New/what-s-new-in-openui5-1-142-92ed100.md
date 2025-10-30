<!-- loio92ed100c9bef4f24b62e0419d2ea22bc -->

# What's New in OpenUI5 1.142

With this release OpenUI5 is upgraded from version 1.141 to 1.142.

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

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Tokenizer`** 

</td>
<td valign="top">

**`sap.m.Tokenizer`**

-   The `Tokenizer` control can now be used in forms. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Tokenizer%23controlProperties).
-   The control now includes multi-line display and a *Clear All* button, enhancing user experience by allowing tokens to wrap across multiple lines and enabling one-click token removal. This facilitates efficient handling of many tokens, improving app visibility and usability. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.Tokenizer%23overview) and the [Sample](https://ui5.sap.com/#/entity/sap.m.Tokenizer/sample/sap.m.sample.TokenizerMultiLine).

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.table.AnalyticalTable`, `sap.ui.table.Table`, `sap.ui.table.TreeTable`** 

</td>
<td valign="top">

**`sap.ui.table.AnalyticalTable`, `sap.ui.table.Table`, `sap.ui.table.TreeTable`**

We have enhanced the `RowAction` functionality in `sap.ui.table` to display up to three actions, with the `Navigation` action always displayed on the far right. If more than three actions have been defined, an overflow menu is shown. For more information, see the [API Reference](https://ui5.sap.com/#/api/ap.ui.table.RowAction) and the [Sample](https://ui5.sap.com/#/entity/sap.ui.table.Table/sample/sap.ui.table.sample.RowAction).

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

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

You can now use the `Edm.Decimal` type with a new `scale="floating"` option, which is necessary for working with ABAP DECFLOAT types. The OData V4 model supports OData V4.01 services within this scope. For more information, see [Transition to OData V4.01](../04_Essentials/transition-to-odata-v4-01-cda632b.md)and the `scale` parameter in the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.type.Decimal%23constructor).

<sub>Changed•Feature•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Button`** 

</td>
<td valign="top">

**`sap.m.Button`**

The screen reader announcement for buttons styled as `Emphasized` has been updated to Default Action, improving accessibility for users relying on assistive technologies. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Button/sample/sap.m.sample.Button).

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Feature 

</td>
<td valign="top">

**Demo Kit: New AI Integration Demo App** 

</td>
<td valign="top">

**Demo Kit: New AI Integration Demo App**

We've introduced a new AI Integration demo app. It illustrates how to seamlessly integrate UI5 Web Components into the OpenUI5 framework, enabling developers to test AI use cases. For more information, see the [Demo Apps](https://ui5.sap.com/#/demoapps/).

<sub>Changed•Feature•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.SegmentedButton`** 

</td>
<td valign="top">

**`sap.m.SegmentedButton`**

The new `contentMode` property enables flexible width behavior with values of `ContentFit` or `EqualSized`. These options offer greater control over button sizing, allowing for either content-based or uniform widths, thereby enhancing the design and consistency of the user interface. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.m.SegmentedButton).

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

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

The new `dateTimeWithTimezone` formatter allows datetime values to be converted to different time zones, enhancing the flexibility and accuracy of time-related data across various regions. This feature is useful for applications that require precise time zone adjustments for global users. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/dateAndTime/dateAndTimeWithTimezone) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/formatters/dateAndTime) in the Card Explorer.

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
<tr>
<td valign="top">

1.142 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Carousel`** 

</td>
<td valign="top">

**`sap.m.Carousel`**

Accessibility attributes and keyboard navigation handling have been updated to improve user experience, including changes to roles and rendering adaptations. These enhancements ensure better navigation and interaction for users relying on assistive technologies. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Carousel/sample/sap.m.sample.CarouselWithMorePages). 

<sub>Changed•Control•Info Only•1.142</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2025-10-30

</td>
</tr>
</table>

