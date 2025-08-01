<!-- loio3a9728ec31f94ca18a7d543ce419d85d -->

# OData V2 Mock Server Tutorial

In this tutorial, we will explore some advanced features of the OData V2 mock server.

If no OData V2 service is available or you simply don't want to depend on the OData back-end connectivity for your development and tests, the mock server can mimic the OData V2 back-end calls. It is designed to simulate an OData V2 provider by intercepting the HTTP communication made to the server, and providing a fake output. All this is transparent to the data binding and usage of the OData V2 model.

In certain scenarios, using only the built-in OData V2 simulation of the mock server is insufficient for completely server-independent tests. For example, if your application is using an OData feature that is not supported by the mock server, or if your application invokes a function import that depends on a server specific implementation \(and thus is also not simulated generically\). We will demonstrate how to use function callbacks in order to change existing mock requests.

Additionally, we will demonstrate how to mock an additional request that is not simulated out of the box by the OpenUI5 OData V2 mock server.

> ### Caution:  
> The tutorial describes how to use some advanced features of the mock server, disregarding the legal aspects of shipping mock data. Usually the mock data and mock server invocation is done in a test folder that is not shipped to customers. Be very careful that you don't ship mock data!

***

## Preview

![Preview of the UI5 application that is going to be built in this tutorial. Displays a list of upcoming meetups generated from mock data.](images/loio8f2176b473a54bbd87e8287732e4eb8e_LowRes.png)

> ### Tip:  
> You don't have to do all tutorial steps sequentially, you can also jump directly to any step you want. Just download the code from the previous step, and start there.
> 
> You can view and download the files for all steps in the Demo Kit at [Mock Server](https://ui5.sap.com/#/entity/sap.ui.core.tutorial.mockserver). Depending on your development environment you might have to adjust resource paths and configuration entries.
> 
> For more information check the [Downloading Code for a Tutorial Step](get-started-setup-tutorials-and-demo-apps-8b49fc1.md#loio8b49fc198bf04b2d9800fc37fecbb218__tutorials_download) section of the tutorials overview page [Get Started: Setup, Tutorials, and Demo Apps](get-started-setup-tutorials-and-demo-apps-8b49fc1.md).

***

## Prerequisites

You should be familiar with the concepts explained in the [Walkthrough Tutorial \(JavaScript\)](walkthrough-tutorial-javascript-3da5f4b.md) tutorial and with the OData specification.

1.  [Step 1: Initial App Without Mock Data](step-1-initial-app-without-mock-data-7a78f1b.md "We start with a simple app scenario with a list of items bound to an OData V2 service.")  
We start with a simple app scenario with a list of items bound to an OData V2 service.
2.  [Step 2: Creating a Mock Server to Simulate Data](step-2-creating-a-mock-server-to-simulate-data-50897de.md "In this step, we add the OData V2 mock server to our app.")  
In this step, we add the OData V2 mock server to our app.
3.  [Step 3: Handling Custom URL Parameters](step-3-handling-custom-url-parameters-46c1ca4.md "In this step, we add the functionality to interpret URL parameters in our local mock
		server configuration.")  
In this step, we add the functionality to interpret URL parameters in our local mock server configuration.
4.  [Step 4: Calling a Function Import](step-4-calling-a-function-import-95e5b87.md "In this step, we change the binding of the list to a function import call that returns only upcoming meetups instead of the entire
		collection.")  
In this step, we change the binding of the list to a function import call that returns only upcoming meetups instead of the entire collection.

**Related Information**  


[Mock Server](../04_Essentials/mock-server-69d3cbd.md "A mock server mimics one or more back-end services. It is used to simplify integration testing and to decouple UI development from service development. By using a mock server you can develop and test the UI even if the service in the back end is incomplete or unstable.")

