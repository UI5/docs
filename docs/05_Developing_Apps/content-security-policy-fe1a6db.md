<!-- loiofe1a6dba940e479fb7c3bc753f92b28c -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Content Security Policy

Content Security Policy \(CSP\) adds an additional layer of security that can detect and mitigate certain types of attacks, such as cross-site scripting and data injection.

***

CSP restricts the sources from which the browser is allowed to load resources, such as scripts, fonts, and images:

-   CSP mitigates and reports XSS attacks; CSP-compatible browsers only execute scripts loaded in source files that are received from allowed sources.

-   CSP also mitigates packet sniffing attacks by specifying the protocols that may be used on the web server, for example, specifying that content must be loaded from HTTPS.


CSP is either enabled via a configuration in the web server to return the Content-Security-Policy HTTP header \(preferred solution\), or via the `<meta>` element in the meta tags of an HTML page.

For generic information about CSP, see [https://www.w3.org/TR/CSP2/](https://www.w3.org/TR/CSP2/).

***

<a name="loiofe1a6dba940e479fb7c3bc753f92b28c__section_chc_tmq_crb"/>

## CSP for OpenUI5 - Dos and Don'ts

For OpenUI5, we recommend that developers build their apps CSP-compliant, in particular regarding the loading of resources and the use of inline scripts.

***

### Policies Without `script-src 'unsafe-inline'`

To build CSP-compliant OpenUI5 without inline scripts, avoid the following:

-   `<script>` elements with inlined source code

-   Inline event handlers

-   `javascript:` URLs

-   `document.write()`, `createElement('script')`, and so on, if they are used to create inline scripts. Creating script references, such as `<script src="..."></script>`, or non-script content with them is okay.


***

### Policies Without `script-src 'unsafe-eval'`

`eval()` is currently still required in some parts of OpenUI5 for synchronous loading and other functionality. However, we recommend loading JavaScript resources asynchronously, which also avoids the use of `eval()`. For more information about asynchronous loading, see [Modules and Dependencies](../04_Essentials/modules-and-dependencies-91f23a7.md).For more information about avoiding synchronous APIs that might lead to synchronous loading, see [Deprecated Factories Replacement](../04_Essentials/deprecated-factories-replacement-491bd9c.md).

For a CSP policy that doesn't allow `eval()` you must also avoid the following elements when developing OpenUI5 apps:

-   `new Function()`

-   `<setTimeout(<non-fn>)`

    This will be ignored silently and not create a timer without `'unsafe-eval'`, that is, `<non-fn>` is never executed. `setTimeout(<fn>)` works with and without `'unsafe-eval'`.

-   `setInterval(<non-fn>)`

    This will be ignored silently and not create a repeated timer without `'unsafe-eval'`, that is, the `<non-fn>` is never executed. `setInterval(<fn>)` works with and without the `'unsafe-eval'`.


***

<a name="loiofe1a6dba940e479fb7c3bc753f92b28c__section_spl_4p3_2rb"/>

## Test Your Policies with `Report-Only`

> ### Note:  
> CSP is a complex subject with many interdependencies and dynamics. Example: A CSP-compliant control or function in your app might have a dependency to a deprecated API that is not fully CSP-compliant. In this case you may need to add `'unsafe-eval'` to the `script-src` directive. That's why it's important to test your policies to check this.

To test policies without enforcing them, set up CSP with the `Content-Security-Policy-Report-Only` response header and test with the **most restrictive** policy. Monitor the reports to add missing sources \(see [Directives](content-security-policy-fe1a6db.md#loiofe1a6dba940e479fb7c3bc753f92b28c__directives). When you have found the desired policy, replace the `Content-Security-Policy-Report-Only` header with `Content-Security-Policy` to enforce the policy.

***

<a name="loiofe1a6dba940e479fb7c3bc753f92b28c__directives"/>

## Directives

To run an app in an environment in which CSP has been enabled, OpenUI5 requires the following CSP directives and source entries:


<table>
<tr>
<th valign="top" rowspan="2">

Directive

</th>
<th valign="top" align="center" colspan="4">

Sources Required by the OpenUI5 Framework

</th>
<th valign="top" align="center">

Sources Required by the App

</th>
</tr>
<tr>
<th valign="top">

<code>&lt;source hosting OpenUI5&gt;</code>

\(equals `'self'` if OpenUI5 is hosted with the app\)

</th>
<th valign="top">

`data:`

</th>
<th valign="top">

`blob:`

</th>
<th valign="top">

Other Sources

</th>
<th valign="top">

Custom Sources \(Including 'self' for the App's Own Origin\)

</th>
</tr>
<tr>
<td valign="top">

`script-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
<td valign="top">

`'unsafe-eval'`

Required for synchronous loading of JavaScript resources.

Required for the following libraries:

-   `sap.ui.commons`
-   `sap.ui.ux3`

Most likely required for deprecated APIs, especially for programming model APIs, like old factories in the `sap.ui` namespace.

</td>
<td valign="top">

-   Requires `'self'` for loading application resources.
-   May require `'unsafe-inline'` or `'unsafe-eval'` depending on custom scripts.



</td>
</tr>
<tr>
<td valign="top">

`style-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
<td valign="top">

`'unsafe-inline'`

Required for the following libraries:

-   `sap.ui.commons`
-   `sap.ui.ux3`

Most likely required for deprecated APIs.

Certain libraries at least partly still require `'unsafe-inline'`, including:

-   All controls based on UI5 Web Components \(for example `sap.f`, `sap.ui.integration`\)
-   `sap.webc.*`



</td>
<td valign="top">

-   May require `'self'` and additional locations for application-specific styles and themes.
-   Requires `'unsafe-inline'` for custom controls using inline styles.



</td>
</tr>
<tr>
<td valign="top">

`img-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

 

</td>
<td valign="top">

May require `'self'` or additional locations for application-specific images \(such as custom themes or images in the back end\).

</td>
</tr>
<tr>
<td valign="top">

`font-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
<td valign="top">

May require `'self'` or additional locations for application-specific fonts.

</td>
</tr>
<tr>
<td valign="top">

`frame-src`

</td>
<td valign="top">

Required for using the support assistant and/or the diagnostics tool. Also required to avoid a fallback to `child-src`.\*

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

 

</td>
<td valign="top">

May require additional locations depending on the integration, application, or test scenario.

</td>
</tr>
<tr>
<td valign="top">

`worker-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

`child-src`\*\*

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

May be required by some specific OpenUI5 functionality.

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

`connect-src`

</td>
<td valign="top" align="center">

<span style="color:#007833;"><span class="SAP-icons-V5"></span></span>

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
<td valign="top">

Some specific OpenUI5 functionality may require `wss:`.

</td>
<td valign="top">

Requires `'self'` for loading application resources.

</td>
</tr>
</table>

\*In case `child-src` has been specified but no fallback for `frame-src` is intended, define `frame-src` with proper sources \(could also be `'none'`\).

\*\*`child-src` is still required for browsers that don't support `worker-src` yet.

***

<a name="loiofe1a6dba940e479fb7c3bc753f92b28c__section_c1k_gt3_2rb"/>

## Specific Restrictions

The following functions and features require additional CSP source entries or have certain restrictions:


<table>
<tr>
<th valign="top">

Library

</th>
<th valign="top">

Topic

</th>
<th valign="top">

Comment

</th>
</tr>
<tr>
<td valign="top" align="center" colspan="3">

<code><b>script-src 'unsafe-eval'</b></code>

</td>
</tr>
<tr>
<td valign="top">

`sap.ui.support`

</td>
<td valign="top">

Support Assistant - Temporary Rules

</td>
<td valign="top">

For temporary rules in the Support Assistant, dynamic code execution is essential, so it can't be removed. Support Assistant detects whether dynamic code execution is allowed and informs the user if temporary rules can be used or not.

</td>
</tr>
<tr>
<td valign="top" align="center" colspan="3">

<code><b>script-src 'wasm-unsafe-eval'</b></code>

</td>
</tr>
<tr>
<td valign="top">

`sap.ui.core`

</td>
<td valign="top">

Hyphenation

</td>
<td valign="top">

`script-src` requires `wasm-unsafe-eval`

When native hyphenation is not available, a third-party library \(Hyphenopoly\) is used. This library uses WASM, which leads to CSP issues due to browser limitations. There is a fallback to `asm.js`, if WASM can't be used.

</td>
</tr>
<tr>
<td valign="top" align="center" colspan="3">

<code><b>style-src 'unsafe-inline'</b></code>

</td>
</tr>
<tr>
<td valign="top">

`sap.m` and others

</td>
<td valign="top">

Controls that display provided HTML text \(for example `sap.m.FormattedText` and `sap.ui.core.HTML`\)

</td>
<td valign="top">

Certain controls display provided HTML text, for example `sap.m.FormattedText`. If the provided text contains a style attribute or a style element with inline styles, `'unsafe-inline'` is required for `style-src`.

It's recommended to use styling with the `class` attribute and external stylesheets.

</td>
</tr>
</table>

