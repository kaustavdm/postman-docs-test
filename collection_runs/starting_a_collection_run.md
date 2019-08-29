---
title: Starting a collection run
page_id: starting_a_collection_run
warning: false
---

# starting\_a\_collection\_run

Collections are groups of requests that can be run together as a series of requests, against a corresponding environment.

You can use scripts to build integration test suites, pass data between API requests, and build workflows that mirror your actual use case of APIs.

## Customizing requests in collection runner

The collection runner allows for customizing the execution of requests in the following ways:

* **Order of execution**: The requests execute in the order they appear on the **Run order** pane of the collection runner. The execution can be reordered by dragging and dropping.
* **Selective execution**: Requests can be prevented from executing by disabling them using the preceeding check boxes in the **Run order** pane of the collection runner.

This topic describes how to configure collection run parameters for:

* [Collection or folder](starting_a_collection_run.md#collection-or-folder)
* [Environment](starting_a_collection_run.md#environment)
* [Iterations](starting_a_collection_run.md#iterations)
* [Delay](starting_a_collection_run.md#delay)
* [Log responses](starting_a_collection_run.md#log-responses)
* [Data](starting_a_collection_run.md#data)
* [Persist variables](starting_a_collection_run.md#persist-variables)
* [Run collection without using stored cookies](starting_a_collection_run.md#run-collection-without-using-stored-cookies)
* [Save cookies after collection run](starting_a_collection_run.md#save-cookies-after-collection-run)

[![collection run parameters](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/starting_a_collection_run/collection_run_parameters.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/starting_a_collection_run/collection_run_parameters.png)

## Collection or folder

The collection or folder you want to run.

When you run a collection, all requests in the collection are sent in the order they appear in the main app. As a result each folder is run, and each request inside the folder, is sequentially executed. When you select a folder, only that folder is executed and only requests inside the folder are sent. You can, however, change the order to more closely mirror your workflow when you use the `postman.setNextRequest()` method. You will also be able to use the collection runner for form-data request and binary file bodies containing files.

To learn more about how to build a workflow, see [Building workflows](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/building_workflows/README.md).

## Environment

The environment to use when a collection runs.

To learn how to use environments in collection runs, see [Using environments in collection runs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/using_environments_in_collection_runs/README.md).

## Iterations

The number of times the collection will run.

Sending different data in each iteration and setting a higher iteration counts usually ensures the stability of your APIs.

To learn how to run multiple iterations, see [Running multiple iterations](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/running_multiple_iterations/README.md).

## Delay

The interval \(in milliseconds\) between each request in a collection run.

## Log responses

Limits response logging when the collection runs.

By default, all responses are logged for debugging purposes. For large collections, you can change this setting to improve performance.

Here's more detail about default logging:

* For all requests, responses for all requests will be logged.
* For failed requests, only responses for requests with at least one failing test will be logged.
* For no requests, no responses will be logged.

To learn how to debug collection requests, see [Debugging a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/debugging_a_collection_run/README.md).

## Data

Supplies a data file to use for the collection run.

To learn more about how to use a date file for a collection run, see [Working with data files](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/working_with_data_files/README.md).

## Persist variables

By default, any environment changes in the collection runner are not reflected in the request builder. Enabling this option saves the values of the variables at the end of the run, **overwriting previous values**.

To learn more about Keep variable values in a collection run, see [Using environments in collection runs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/using_environments_in_collection_runs/README.md).

## Run collection without using stored cookies

A request from the collection may require cookies to run. Collection runner can allow/prevent the request from accessing the cookie by the **Run collection without using stored cookies** option. Enabling this allows collection runs without using cookies stored in the cookie manager.

## Save cookies after collection run

A request in the collection may create/update cookies during execution. The Collection runner provides an option to save the cookie to the cookie manager, **overwriting any existing cookie**. Enabling this saves the cookies for the session to the cookie manager.

For more information about collections runs, see:

* [Using environments in collection runs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/using_environments_in_collection_runs/README.md)
* [Working with data files](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/working_with_data_files/README.md)
* [Running multiple iterations](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/running_multiple_iterations/README.md)
* [Building workflows](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/building_workflows/README.md)
* [Sharing a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/sharing_a_collection_run/README.md)
* [Debugging a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/debugging_a_collection_run/README.md)
* [Command line integration with Newman](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/command_line_integration_with_newman/README.md)
* [Integration with Jenkins](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_jenkins/README.md)
* [Integration with Travis CI](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_travis/README.md)
* [Newman with Docker](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/newman_with_docker/README.md)

