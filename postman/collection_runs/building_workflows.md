---
title: Building workflows
page_id: building_workflows
warning: false
---

# Building workflows

When you start a collection run, all requests are run in the order you see them in the main app. So all requests are executed first, by order of the folder, and then any requests in the root of the collection.

However, you can override this behavior using a [built-in function](/postman/scripts/branching_and_looping.md) called `postman.setNextRequest()`. This function, as the name suggests, allows you to specify which request runs next.

Let's look at a sample collection to understand this function.

* [Getting started](building_workflows.md#getting-started)
* [Basic workflow](building_workflows.md#basic-workflow)
* [Advanced workflow](building_workflows.md#advanced-workflow)

## Getting started

Before you start, download and [import](/postman/collections/data_formats.md) [collection.json](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58793802.json) for the example we'll discuss in this topic.

## Basic workflow

Let's assume that we have a collection with four requests. If you run this collection directly, the collection runner runs all four requests in order.

[![setNextRequest in tests tab](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Runs_pg23.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Runs_pg23.png)

[![collection runner view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58793861.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58793861.png)

Let's now add `postman.setNextRequest()` to Request 1's test script, as shown. `postman.setNextRequest()` is a function with one argument, which is the name or ID of the request you want to run next.

In the example, we're setting the next request to Request 4 in the test script for Request 1. So the execution jumps to Request 4 after Request 1 has completed. If we run the same collection now, you'll see that only two requests are run now.

[![setNextRequest with request name as parameter](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Runs_pg24.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Runs_pg24.png)

[![collection runner view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58793875.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/58793875.png)

Note that `postman.setNextRequest()` only works with the collection runner and Newman where the intent is to run a collection, as opposed to sending a single request.

## Advanced workflow

Now that we have a good understanding of how `setNextRequest()` works, we can perform advanced actions.

Since you are no longer restricted by the order in which you define your requests, you can jump around your collection, establish conditional logic, or skip unnecessary requests.

This [blog post](https://blog.getpostman.com/2016/11/09/generate-spotify-playlists-using-a-postman-collection/) explains how you can write a collection that will generate Spotify playlists for you based on your favorite musical artists.

Remember these two facts as you use this workflow:

* `postman.setNextRequest()` is always executed at the end of the current request. This means that if you put this function before other code blocks anywhere in pre-request or test script, these blocks will still execute.
* `postman.setNextRequest()` has a scope, which is the source of your collection run. If you run a collection, you can jump to any request in the collection \(even requests inside folders, using the same syntax\). However, if you run a folder, the scope of `postman.setNextRequest()` is limited to that folder. So you can jump to any request in this folder, but not ones that are outside of the folder. It includes requests inside other folders, and also root-level requests in the collection. To read more about [running collections or folders](/postman/collection_runs/starting_a_collection_run.md).

For more information on collection runs, see:

* [Starting a collection run](/postman/collection_runs/starting_a_collection_run.md)
* [Using environments in collection runs](/postman/collection_runs/using_environments_in_collection_runs.md)
* [Working with data files](/postman/collection_runs/working_with_data_files.md)
* [Running multiple iterations](/postman/collection_runs/running_multiple_iterations.md)
* [Building workflows](/postman/collection_runs/building_workflows.md)
* [Sharing a collection run](/postman/collection_runs/sharing_a_collection_run.md)
* [Debugging a collection run](/postman/collection_runs/debugging_a_collection_run.md)
* [Command line integration with Newman](/postman/collection_runs/command_line_integration_with_newman.md)
* [Integration with Jenkins](/postman/collection_runs/integration_with_jenkins.md)
* [Integration with Travis CI](/postman/collection_runs/integration_with_travis.md)
* [Newman with Docker](/postman/collection_runs/newman_with_docker.md)

