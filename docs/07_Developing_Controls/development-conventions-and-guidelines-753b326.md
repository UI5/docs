<!-- loio753b32617807462d9af483a437874b36 -->

# Development Conventions and Guidelines

To keep the OpenUI5 code readable and maintainable, development conventions and guidelines are introduced. We strongly recommend that you follow these guidelines even if you find them violated somewhere. For files that are consistently **not** following these rules and for which adhering to the rules would make the code worse, follow the local style. If you want to contribute your content to OpenUI5, you **have to** follow these conventions and guidelines.

> ### Note:  
> This list is not complete.

***

## General Guidelines

The following list gives some general guidelines to be adhered to when developing content for OpenUI5:

-   Always consider the developers who **use** your control or code! Do not surprise them, but give them what they expect. And make it simple.

-   Use tabs, not spaces, for indentation; adhere to local standards in the file.

-   Use Unix line endings \(LF-only\).

-   Text files must be UTF-8 encoded \(HANA\); only `*.properties` and `*.hdbtextbundle` files must be ISO8859-1 encoded as defined in the corresponding standard.

    This is the status quo. As this causes issues, it may be subject to change..

-   An 80-character line length guideline does **not** exist.

-   Use comments; do **not** rephrase the code, but tell the reader what is **not** in the code. Describe why your code does what it does. Prefer line comments.


-   **[JavaScript Coding Guidelines](javascript-coding-guidelines-eded636.md "Provides an overview of the guidelines for JavaScript coding for OpenUI5.")**  
Provides an overview of the guidelines for JavaScript coding for OpenUI5.
-   **[TypeScript Guidelines](typescript-guidelines-192397d.md "Provides an overview how to develop OpenUI5 control libraries in
		TypeScript.")**  
Provides an overview how to develop OpenUI5 control libraries in TypeScript.
-   **[OpenUI5 Control Development Guidelines](openui5-control-development-guidelines-4549da6.md "Content developers developing OpenUI5 controls should follow the guidelines outlined
		below with regard to APIs, behavior, and themes/CSS.")**  
Content developers developing OpenUI5 controls should follow the guidelines outlined below with regard to APIs, behavior, and themes/CSS.
-   **[Product Standards and Acceptance Criteria](product-standards-and-acceptance-criteria-bafc686.md "To be of high quality and usable in mission-critical business software, OpenUI5 needs to
		fulfill specific product standards and acceptance criteria. While these are not directly
		related to code conventions, the most important standards and criteria are mentioned here,
		because new code needs to fulfill these requirements.")**  
To be of high quality and usable in mission-critical business software, OpenUI5 needs to fulfill specific product standards and acceptance criteria. While these are not directly related to code conventions, the most important standards and criteria are mentioned here, because new code needs to fulfill these requirements.
-   **[File Names and Encoding](file-names-and-encoding-104135d.md "Some target platforms of OpenUI5 impose technical restrictions on the naming or structure
		of resources (files).For this, rules for file names and encoding have been
		introduced.")**  
Some target platforms of OpenUI5 impose technical restrictions on the naming or structure of resources \(files\).For this, rules for file names and encoding have been introduced.
-   **[Git Guidelines](git-guidelines-b2f5639.md "For using Git for developing content for OpenUI5, rules and guidelines for the use of Git
		and the content of commit messages have been introduced.")**  
For using Git for developing content for OpenUI5, rules and guidelines for the use of Git and the content of commit messages have been introduced.
-   **[JSDoc Guidelines](jsdoc-guidelines-eeaa5de.md "")**  

-   **[Tools](tools-41de83f.md "For the tools used for OpenUI5 content development, guidelines and recommendations have
		been introduced.")**  
For the tools used for OpenUI5 content development, guidelines and recommendations have been introduced.

