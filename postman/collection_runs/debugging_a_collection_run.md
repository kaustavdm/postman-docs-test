---
title: Debugging a collection run
page_id: debugging_a_collection_run
warning: false
---

# debugging\_a\_collection\_run

Sometimes your Collection tests fail—even when you expect them all to pass.

When failure occurs, you can debug your requests in two ways:

* [Debugging using the Request and Response body](debugging_a_collection_run.md#debugging-using-the-request-and-response-body)
* [Debugging using the Postman Console](debugging_a_collection_run.md#debugging-using-the-postman-console)

Let's explore debugging request in an example using the [Postman Echo collection](https://docs.postman-echo.com/).

To add Postman Echo to your Postman builder view, go to [Postman Echo](https://docs.postman-echo.com/).

Click the **Run in Postman** button on the top right side of the screen. The Postman Echo collection appears in the sidebar of your Postman builder.

In your Postman builder view, click the **Runner** button in the left side of the header bar.

In the Collection Runner, select "Postman Echo" and click the **Run Postman Echo** button. \(You can also select the "Environment", "Iterations", "Delay" \(time\), "Log Repsonses", "Data", and "Persist Variables". But it's not necessary for this example.\) The image below shows the results of the collection run.

[![collection runner view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58531976.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58531976.png)

In the `Delete Cookies` request, we expect a certain cookie to be returned by the server.

Postman Echo's [Cookies](https://docs.postman-echo.com/#37368024-f6a8-0f70-85fc-7e876cde9e33)endpoint returns whatever cookies are sent to it. It also sends a JSON representation of these in the response body. We're using this to check if a certain cookie was returned.

As you can see, this test is failing. Let's investigate why.

## Debugging using the Request and Response body

[![tooltip for request](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532000.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532000.png) [![collection runner view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532254.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532254.png)

As the test says, we're expecting a cookie named `foo1` to be returned as part of the response.

If you click on any request name in your collection run, you'll notice a tooltip appear. This tooltip has useful information about to your request, information you might need to figure out what went wrong.

Expanding the `Response Body` section, we can see clearly that the response does not contain the cookie we expect.

Moreover, when we expand the `Response Headers` section, we see that the cookie was not sent at all. We infer something must be wrong with the way Postman Echo handles cookies. We can now go ahead and patch this up in our API and try again.

Note that only response bodies less than 300KBs are attempted to be displayed. Your response headers and bodies are never synced for security reasons.

You can control which bodies show up in this tooltip by using the `Log responses` dropdown when [starting a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/starting_a_collection_run/README.md).

## Debugging using the Postman Console

Debugging using the Postman Console requires you to have the console open before you start your run.

For more information about the Postman Console, see [Debugging and logs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/sending_api_requests/debugging_and_logs/README.md).

[![postman console view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532402.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58532402.png)

The Postman Console records all requests and displays them in a list.

Let's find the request that's causing problems here and expand its response headers. Here too, we see that the Postman Echo endpoint did not return a cookie, and indicates why our test is failing. We can then infer that the endpoint is misbehaving and needs to be reviewed.

Any `console.log` you have in your test scripts also appears here, so you can log in the console if you're debugging a complex test script.

For more information about collection runs, see:

* [Starting a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/starting_a_collection_run/README.md)
* [Using environments in collection runs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/using_environments_in_collection_runs/README.md)
* [Working with data files](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/working_with_data_files/README.md)
* [Running multiple iterations](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/running_multiple_iterations/README.md)
* [Building workflows](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/building_workflows/README.md)
* [Sharing a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/sharing_a_collection_run/README.md)
* [Command line integration with Newman](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/command_line_integration_with_newman/README.md)
* [Integration with Jenkins](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_jenkins/README.md)
* [Integration with Travis CI](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_travis/README.md)
* [Newman with Docker](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/newman_with_docker/README.md)

