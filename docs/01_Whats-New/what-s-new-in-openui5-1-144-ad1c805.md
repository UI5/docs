<!-- loioad1c8056995148148cb398d318c8f5b9 -->

# What's New in OpenUI5 1.144

With this release OpenUI5 is upgraded from version 1.143 to 1.144.

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

1.144 

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

-   When copying a node of a recursive hierarchy, the non-canonical path is now used.

-   Executing overloaded unbound functions is now supported.

-   Deleting a record from a flat list of unaggregated records with a grand total is now supported as an experimental feature. Note that the grand total is not updated.

-   Setting a context to keep-alive is now supported for single records in data aggregation scenarios.This is an experimental feature and subject to the restrictions listed in the [API Reference](https://ui5.sap.com/#/api/sap.ui.model.odata.v4.Context%23methods/setKeepAlive).


<sub>Changed•Feature•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

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

We now use the localization content of the Unicode Common Locale Data Repository \(CLDR\) version 48.0.0.

<sub>Changed•Feature•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.Panel`** 

</td>
<td valign="top">

**`sap.m.Panel`**

The `sap.m.Panel` control now expands and collapses when the [Space\] key is released \(`keyup` event\) rather than when it is pressed down \(`keydown` event\), enhancing usability. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Panel/sample/sap.m.sample.PanelExpanded).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

New 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.mdc.Geomap`** 

</td>
<td valign="top">

**`sap.ui.mdc.Geomap`**

We've introduced a new experimental `sap.ui.mdc.Geomap` control within the MDC library. This control provides a native UI5 surface for displaying interactive maps, visualizing `GeoJSON` data, and integrating vector and raster tiles from multiple providers, including ESRI, HERE, OpenStreetMap, and SAP HANA Spatial Services. Leveraging `MapLibre GL` for high-performance rendering, it includes features such as clustering, drawing and selection tools, various layer types \(fill, line, circle, heatmap, symbol\), and supports responsive pan, zoom, rotate, and tilt capabilities. The control integrates with standard UI5 lifecycle, data binding, events, and aggregations. Note that as an experimental API, its features and interfaces may be subject to change. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.mdc.Geomap) and the [Samples](https://ui5.sap.com/#/entity/sap.ui.mdc.Geomap). You can also check out the tutorial [How to Use MDC GeoMap](https://github.com/SAP-samples/ui5-mdc-json-tutorial/tree/main/u2/ex1).

<sub>New•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.ui.unified.ColorPicker`** 

</td>
<td valign="top">

**`sap.ui.unified.ColorPicker`**

We have improved the accessibility of the control by updating label attributes and grouping logic. Additionally, clicking the *Change Color Mode* button now prompts the screen reader to announce the values for RGBA or HSL modes, enhancing accessibility feedback.

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

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

The redesigned control now features a modern input-like appearance, enhancing user experience by replacing the browse button with a `Value-help` icon and adding a *Clear* icon for removing selected files. Selected files are now displayed as tokens, providing a more intuitive and visually appealing interface while keeping all existing functionalities. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.unified.FileUploader).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.PlanningCalendar, sap.m.SinglePlanningCalendar`** 

</td>
<td valign="top">

**`sap.m.PlanningCalendar, sap.m.SinglePlanningCalendar`**

We have improved the accessibility of the controls by converting the invisible reference for the *View* switch into a visible label. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.PlanningCalendar/sample/sap.m.sample.PlanningCalendar).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

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

We have improved the accessibility of the control. The *Next* and *Previous* buttons in the header are now focusable and have titles. The `aria-label` attributes for date range selections now offer detailed information about the range, and an announcement is added when focusing on a day within the range.

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.m.StepInput`** 

</td>
<td valign="top">

**`sap.m.StepInput`**

Flexible input precision is now enabled, allowing users to enter numbers with varying decimal places, regardless of the `displayValuePrecision` setting. If the input precision does not match the specified `displayValuePrecision`, the `ValueState` property is set to `Error`. If `ValidationMode` is set to `FocusOut`, the error state applies on focus out; if it is set to `LiveChange`, it updates immediately. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.StepInput/sample/sap.m.sample.StepInput).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

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

We have improved focus padding and overflow properties to ensure that focus outlines are consistently visible and properly aligned. This enhancement boosts visual accessibility and user interaction by maintaining clear visibility of critical UI elements. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.m.Switch/sample/sap.m.sample.Switch).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

</td>
<td valign="top">

Changed 

</td>
<td valign="top">

Control 

</td>
<td valign="top">

**`sap.tnt.ToolPage`** 

</td>
<td valign="top">

**`sap.tnt.ToolPage`**

The responsiveness of `sap.tnt.ToolPage` has been changed from device-based detection to screen-width breakpoints. There are now two main scenarios: screen widths of 599 pixels or less \(*ToolPage* is collapsed by default\), and those of 600 pixels or more \(*ToolPage* is expanded by default\). This automatic behavior can be overridden by setting the `sideExpanded` property. For more information, see the [Sample](https://ui5.sap.com/#/entity/sap.tnt.ToolPage/sample/sap.tnt.sample.ToolPage) and the [API Reference](https://ui5.sap.com/#/api/sap.tnt.ToolPage).

<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
<tr>
<td valign="top">

1.144 

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

-   To align with the latest theming design updates, the Card Explorer has been updated to replace static card screenshots with interactive UI5 Integration Cards. This change enhances the user experience by enabling direct interaction with the cards within the demo pages. Additionally, deep-link synchronization with the browser URL is now enabled to improve the navigation experience. For more information, see the [Card Explorer](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/overview/introduction). 

-   UI Integration Cards of declarative card type Analytical now support click detection on individual chart segments, providing detailed information about exactly what users clicked. When `actionableArea` is set to "Chart," card developers can now use the new `chartEventData` model to access specific event data within the action parameter binding, including measurement names. This event data contains information about which specific sector of the chart is clicked. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/analytical/stackedColumnWithMeasureActions) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/analytical) in Card Explorer.
-   UI Integration Cards of declarative card type Object now support radio buttons as input controls, offering greater flexibility in user interaction. This functionality is accomplished by setting the `type=”RadioButtonGroup”` for the Object card group item that contains a set of radio button options with attributes `key`, `title`, and `enabled`. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/object/form) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/object) in Card Explorer.
-   Tile-like cards now have improved accessibility, ensuring a better user experience for individuals relying on screen readers. By adjusting roles and labels, the update prevents redundant announcements, making navigation and information retrieval more efficient.
-   The `sap.ui.integration.widgets.CardFacade` API is no longer experimental. This release stabilizes the facade, enhances its long-term support, and aligns it with modern Integration Card usage patterns. As part of the cleanup, several methods were deprecated to ensure consistent and future-proof development, including `getParameters`, `getDomRef`, `setVisible`, and `getModel`. For more information, see the [API Reference](https://ui5.sap.com/#/api/sap.ui.integration.widgets.CardFacade).
-   UI Integration Cards of declarative card type Analytical can now display tooltips. Users can now view tooltips when hovering over individual points on the charts, provided this feature is configured in the `manifest.json` file by setting the `tooltip` property. For more information, see the [Sample](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/analytical/tooltips) and the [Documentation](https://ui5.sap.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/typesDeclarative/analytical) in Card Explorer.
-   The UI5 MCP Server now supports the development of UI Integration Cards. In its latest version, v0.2.1, it introduces three new tools dedicated to UI Integration Cards. These tools assist Large Language Models in creating new UI Integration Cards from scratch or editing existing ones, following the best practices for card development. The new tools include:

    -   Best practice guidance for your agent: `get_integration_cards_guidelines`.
    -   Scaffolding a new card: `create_integration_card`.
    -   Validating the card’s manifest: `run_manifest_validation`.


<sub>Changed•Control•Info Only•1.144</sub>

</td>
<td valign="top">

Info Only 

</td>
<td valign="top">

2026-01-22

</td>
</tr>
</table>

