<!-- loio8d7b2868b8d8441a803a3223754d72fc -->

# Right-to-Left Support

OpenUI5 application developers need to be aware of how applications behave when right-to-left \(RTL\) directionality is selected. Changing the directionality has a big impact on text-displaying controls, images and the alignment of the whole application.

OpenUI5 sets the RTL mode based on the current language which is usually picked automatically based on the locale configuration of the user's browser or profile data.

The default text direction is left-to-right \(LTR\). If you need to change the mode for testing purposes you can do it by using one of the following configuration switches:

-   URL parameter `sap-ui-rtl=true`

-   Configuration object: `window["sap-ui-config"].rtl = true;` 

-   Script tag configuration: `data-sap-ui-rtl="true"` 

-   Setting an RTL language as default language for the application.


OpenUI5 then sets the overall page direction to RTL and all OpenUI5 content is displayed in RTL mode. Self-written controls and content has to be tested separately. If your application comes with additional CSS and needs specific style rules for the RTL case, then use a selector starting with `html[dir=rtl]`.

-   **[API Properties for Right-to-Left Support in Text-Displaying Controls](api-properties-for-right-to-left-support-in-text-displaying-controls-7e7cd0a.md "Languages with right-to-left (RTL) text directionality keep the default directionality
		of numeric values and texts in left-to-right (LTR) mode. To ensure correct handling, two API
		properties have been introduced - textDirection and
			textAlign.")**  
Languages with right-to-left \(RTL\) text directionality keep the default directionality of numeric values and texts in left-to-right \(LTR\) mode. To ensure correct handling, two API properties have been introduced - `textDirection` and `textAlign`.

