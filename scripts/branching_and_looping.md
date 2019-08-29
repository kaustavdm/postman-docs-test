---
title: Branching and looping
page_id: branching_and_looping
warning: false
---

# branching\_and\_looping

When running a collection, you can branch and loop across API requests in Postman using the `postman.setNextRequest("request_name");` function.

[![set next request method](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Test_script10.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Test_script10.png)

## Set the request to be executed next

```javascript
postman.setNextRequest("request_name");
```

## Stop workflow execution

```javascript
postman.setNextRequest(null);
```

Some salient points about `postman.setNextRequest()`:

1. Specify the name or ID of the subsequent request and the collection runner will take care of the rest.
2. It can be used in the pre-request or the test script. If there's more than one assignment, the last set value takes precedence.
3. If `postman.setNextRequest()` is absent in a request, the collection runner defaults to linear execution and moves to the next request

For more information about control flow, refer to [building workflows](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/building_workflows/README.md).

