---
title: Intro to mock servers
page_id: intro_to_mock_servers
warning: false
---

# Intro to mock servers

## What are mock servers

Delays on the front- or back-end make it difficult for dependent teams to complete their work efficiently. Postman's mock servers can alleviate those delays in the development process.

Before sending an actual request, front-end developers can create a mock server to simulate each endpoint and its corresponding response in a Postman Collection. Developers can view potential responses, without spinning up a back end.

## Why use mock servers

Creating a [mock example](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collections/examples/README.md) during the earliest phase of API development fosters clear communication among team members and aligns their expectations.

As a result, all teams in the development process can work in parallel; and dependent teams experience fewer delays.

## Types of mock servers

Postman lets you create two types of mock servers: private and public.

### Private mock servers

Private mock servers require users to add a Postman API key in the request header `x-api-key`, like: `x-api-key:<your postman API key>`.

If you create a private mock server, users can [share the underlying collection](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/workspaces/using_workspaces/README.md#sharing-collections-and-environments-in-workspaces) with the team or specific team members, and provide permissions to edit or view. Your team members can use their Postman API keys to consume the mock. Team members can use the mock if they have permissions to access the underlying collection.

### Public mock servers

Mock servers are public by default. Public mock servers are accessible to anyone. When you share a public mock server, users don’t need to add a Postman API key.

## Further reading

For more information about mock servers, see:

* [Setting up a mock server](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/mock_servers/setting_up_mock/README.md)
* [Mocking with examples](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/mock_servers/mocking_with_examples/README.md)
* [Mocking with the Postman API](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/mock_servers/mock_with_api/README.md)
* [Matching algorithm \(for mocks\)](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/mock_servers/matching_algorithm/README.md)

