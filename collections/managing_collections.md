---
title: Managing collections
page_id: managing_collections
warning: false
---

# managing\_collections

This topic describes the tasks you can perform from the Collections tab in the sidebar.

* [Navigate through collections](managing_collections.md#navigate-through-collections)
* [Edit and view collection details](managing_collections.md#edit-and-view-collection-details)
* [Create a new collection](managing_collections.md#create-a-new-collection)
* [Reorder collections](managing_collections.md#reorder-collections)
* [Favoriting a collection](managing_collections.md#favoriting-a-collection)
* [Filter collections](managing_collections.md#filter-collections)
* [Delete a collection](managing_collections.md#delete-a-collection)
* [Recover a collection](managing_collections.md#recover-a-collection)
* [Share a collection](managing_collections.md#share-a-collection)
* [Other collection features](managing_collections.md#other-collection-features)
* [Adding folders](managing_collections.md#adding-folders)

## Navigate through collections

Click on a collection to show or hide the requests that comprise the Collection. Use the up and down arrow keys on your keyboard to navigate through the collections.

## Edit and view collection details

Expand the arrow \(▸\) to show the details view for the collection. Collapse the arrow \(◂\) to hide the details view. You can add metadata like name and description so that all the information a developer needs to use your API is available easily.

[![collection details view](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Details_View_New.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collection_Details_View_New.png)

## Create a new collection

Click the "new collection" icon on the top right, or [save a current request to a new collection](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collections/creating_collections/README.md).

[![new collection icon](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-create-new-collection-sidebar.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-create-new-collection-sidebar.png)

## Reorder collections

Collections can be sorted either alphabetically by name or by when they were last updated. To do this, select the "sort" icon on the top right and select `Sort by name` or `Sort by date`.

[![sort collections](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-reorder-collections-sidebar.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-reorder-collections-sidebar.png)

## Favoriting a collection

If you're working on a few collections in particular, you can click on the star icon to bring the collection\(s\) to the top of the list.

[![favorite a collection](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-favorite-sidebar+copy.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-favorite-sidebar+copy.png)

## Filter collections

If you have a lot of collections, filter collections in the sidebar using the search input field.

[![filter collections](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-filter-collections-sidebar.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/WS-filter-collections-sidebar.png)

## Delete a collection

Click the ellipsis \(...\)next to a collection, and select "Delete". If you didn't intend to delete the collection, you can always recover your deleted collections. Refer to the next section **Recover a collection** to learn how to retrieve your deleted collections.

## Recover a collection

Collections deleted can be recovered via your [web dashboard](https://app.getpostman.com/) by clicking your avatar icon in the upper-right corner, then selecting `Trash` from the drop-down menu. Locate the desired collection, hover your cursor over its row, then click `Restore`. You can also recover your deleted collections clicking 'Trash' directly from the app, as illustrated in the screen below:

[![sort collections](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Trash2.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Trash2.png)

The Trash feature is available only for the signed-in users. So, if you are not a registered user you'll still see the Trash option but as a disabled one.

**Note:** Postman offers different recovery plans for Free, Pro and Enterprise users.

* Users on Postman Free license can recover one-day old collections.
* Users on Postman Pro license can recover collections up to 15-days.
* Users on Postman Enterprise license can recover collections up to 30-days.

If your collection seems deleted and you are not able to recover from your deleted collections list, it is possible it is removed from a workspace rather than deleted. To check, navigate back to the main page of the web dashboard, then click `View all collections`. If listed, you can click on its share icon to move it back into a personal or shared workspace.

If you'd like to revert your collection to a previous state, you can do so by leveraging the collection's in-app [activity feed](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/workspaces/activity_feed_and_restoring_collections/README.md).

## Share a collection

To share a collection, see [sharing collections](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collections/sharing_collections/README.md).

## Other collection features

### Reorder requests

Within a collection or folder, you can reorder requests using drag and drop. You can also reorder folders within a collection using drag and drop.

### Save responses

Requests can also store [sample responses](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/sending_api_requests/responses/README.md) when saved in a collection.

### Use examples

With [examples](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collections/examples/README.md), you can mock raw responses and save them to a collection. Then, you’ll be able to generate a mock endpoint for each of them using Postman’s [mock service](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/mock_servers/intro_to_mock_servers/README.md).

### Add scripts

Requests stored inside a collection can contain [scripts](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/scripts/intro_to_scripts/README.md) to add dynamic behavior to the collection.

### Adding folders

Folders are a way to organize your API endpoints within a collection into intuitive and logical groups to mirror your workflow. Next to the collection to which you want to add a folder, click on the ellipsis \(...\) and select "Add Folder".

[![add folder from dropdown](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Add_Folder_Dropdown.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Add_Folder_Dropdown.png)

Add a name and description to the folder. The description is reflected in your API documentation.

You can add deeper levels of nesting for folders. Drag and drop the folders to reorder them to create the ultimate customized folder structure.

[![multi-level folders](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collections_Folder_View.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/Collections_Folder_View.png)
