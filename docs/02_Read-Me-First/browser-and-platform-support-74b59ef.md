<!-- loio74b59efa0eef48988d3b716bd0ecc933 -->

# Browser and Platform Support

Supported browsers and platforms for the OpenUI5 libraries.

***

Generally, OpenUI5 does not support browsers or platforms that are no longer under general support by their respective vendors. Nevertheless, OpenUI5 may function on browser and platform combinations outside the officially supported scope.

***

<a name="loio74b59efa0eef48988d3b716bd0ecc933__section_bgw_kns_hnb"/>

## Browser Support

The following tables provide details on supported browsers and platforms.

**Supported Desktop Browsers and Operating Systems**


<table>
<tr>
<th valign="top" align="center">

Desktop

</th>
<th valign="top" align="center">

Google Chrome

</th>
<th valign="top" align="center">

Microsoft Edge

</th>
<th valign="top" align="center">

Mozilla Firefox

</th>
<th valign="top" align="center">

Apple Safari

</th>
</tr>
<tr>
<td valign="top">

**Windows** \(Version 11\)

</td>
<td valign="top" align="center">

Latest stable version

</td>
<td valign="top" align="center">

Latest stable version

</td>
<td valign="top" align="center">

Latest release and latest ESR

</td>
<td valign="top" align="center">

n/a

</td>
</tr>
<tr>
<td valign="top">

**macOS** \(Latest 2 major versions\)

</td>
<td valign="top" align="center">

Latest stable version

</td>
<td valign="top" align="center">

Latest stable version

</td>
<td valign="top" align="center">

\-

</td>
<td valign="top" align="center">

Latest version

</td>
</tr>
</table>

**Supported Mobile Browsers and Operating Systems**


<table>
<tr>
<th valign="top" align="center">

Mobile

</th>
<th valign="top" align="center">

Google Chrome

</th>
<th valign="top" align="center">

Apple Safari

</th>
</tr>
<tr>
<td valign="top">

**iOS & iPadOS** \(Latest version\)

</td>
<td valign="top" align="center">

\-

</td>
<td valign="top" align="center">

Latest version

</td>
</tr>
<tr>
<td valign="top">

**Android** \(Latest 3 major versions supported by Google\)

</td>
<td valign="top" align="center">

Latest stable version

</td>
<td valign="top" align="center">

n/a

</td>
</tr>
</table>

***

## Additional Information

-   Windows 10 support ended on October 14, 2025. Although OpenUI5 is expected to continue running on Windows 10, upgrade to Windows 11 is strongly recommended.
-   Touch input on Windows is supported, subject to the restrictions listed below.
-   For Firefox, ESR stands for Extended Support Release.
-   Support is provided for the latest WebView on Windows and iPadOS/iOS. Certain features may be limited compared to regular browsers.
-   If personal or organizational tracking prevention settings \(for example, in Microsoft Edge\) are too strict, loading OpenUI5 from hostnames ending in hana.ondemand.com may be blocked. To prevent this, load OpenUI5 from https://sdk.openui5.org/.


***

## Known Issues

Additional restrictions apply to specific OpenUI5 libraries as listed below:

-   `sap.sac.df`, `sap.ui.commons`, and `sap.ui.ux3` libraries do not support touch input on Windows.
-   `sap.sac.df`, `sap.ui.commons`, and `sap.ui.ux3` libraries are not supported on mobile devices.
-   `sap.ui.commons` and `sap.ui.ux3` are not supported in Google Chrome or Microsoft Edge on macOS.
-   [Visual Degradations](visual-degradations-f08f296.md) may occur for certain combinations of browsers and platforms.

***

## ECMAScript Support

OpenUI5 leverages modern ECMAScript, HTML5, and CSS3. Certain restrictions apply for the usage of ECMAScript by OpenUI5 applications. For more information, see [ECMAScript Support](ecmascript-support-0cb44d7.md).

***

## Supported Environments

-   For Windows, the specified browsers are also supported in virtual environments, such as Citrix and VMware. However, any issues found must be reproducible in a non-virtualized environment.
-   Current Apple iPhone, iPad, Samsung Galaxy S phone and Galaxy Tab S Android devices are used for testing and reproducing issues.

***

> ### Note:  
> Browsers are constantly evolving across various platforms. Browser upgrades may introduce changes that are not backward compatible and can affect the behavior of OpenUI5. SAP doesn't provide any warranty regarding the features or qualities of these browsers.

-   **[Visual Degradations](visual-degradations-f08f296.md "Depending on the combination of device and browser, visual degradations may occur in
		certain libraries.")**  
Depending on the combination of device and browser, visual degradations may occur in certain libraries.
-   **[Keyboard Shortcuts for OpenUI5 Tools](keyboard-shortcuts-for-openui5-tools-154844c.md "OpenUI5 provides tools for information, diagnostics and testing purposes that
		are accessible via keyboard shortcuts.")**  
OpenUI5 provides tools for information, diagnostics and testing purposes that are accessible via keyboard shortcuts.

