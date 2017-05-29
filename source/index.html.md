---
title: cclipss iOS Documentation

language_tabs:

toc_footers:
  - <a href='https://github.com/rrainn/ios.developer.cclipss.com'>GitHub Documentation Repo</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:

search: true
---

# Introduction

Welcome to the cclipss iOS Documentation! If you use the cclipss iOS URL schema in a project or application we'd love to hear about it. You may even get a chance to be spotlighted by us. Email us at `support@cclipss.com` with your project details and `cclipss iOS API Project` as the subject!

This documentation is designed for cclipss iOS version 2.0+.


# Bookmarks

<aside class="notice">The user must be logged into the cclipss iOS application for bookmark URL's to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Add Bookmark

This endpoint displays the create bookmark view controller with query parameters filled in. User will still have ability to make changes to bookmark before saving or cancel creating the bookmark (don't rely on this to create the bookmark).

### HTTP Request

`cclipss://bookmark/add` OR `cclipss://bookmark/create`

### Query Parameters

Parameter | Default | Description | Example
--------- | ------- | ----------- | -------
url | nil | Bookmark URL that will be filled into bookmark view controller. | `https://cclipss.com`
title | nil | Bookmark title that will be filled into bookmark view controller. | `cclipss%20Website`
description | nil | Bookmark description that will be filled into bookmark view controller. | `The%20best%20bookmarking%20service%20ever`
project | nil | Bookmark project that will be selected in bookmark view controller. | `projectidhereprojectidhereprojectidhere0`
tags | nil | Bookmark tags that will be selected in bookmark view controller (separated by commas, if multiple). | `tagidheretagidheretagidheretagidhere0000,secondtagidheresecondtagidhere0000000000`
unread | true | If set to true, the bookmark will be marked as unread. If set to false, the bookmark will be marked as read. | `false`

### Examples

URL | Description
--- | -----------
`cclipss://bookmark/add` | Will display view controller to create bookmark with nothing prefilled.
`cclipss://bookmark/create?url=https://cclipss.com` | Will display view controller to create bookmark with `https://cclipss.com` prefilled as the URL.
`cclipss://bookmark/add?url=https://cclipss.com&title=cclipss%20Website` | Will display view controller to create bookmark with `https://cclipss.com` prefilled as the URL, and `cclipss Website` prefilled as the title.



## Edit Bookmark

This endpoint displays the edit bookmark view controller for the bookmark ID provided.

### HTTP Request

`cclipss://bookmark/edit/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bookmark to edit

### Examples

URL | Description
--- | -----------
`cclipss://bookmark/edit/bookmarkidherebookmarkidhere000000000000` | Will display view controller to edit bookmark for bookmark ID `bookmarkidherebookmarkidhere000000000000`.



## Delete Bookmark

This endpoint delete's the bookmark ID provided.

### HTTP Request

`cclipss://bookmark/delete/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bookmark to delete

### Examples

URL | Description
--- | -----------
`cclipss://bookmark/delete/bookmarkidherebookmarkidhere000000000000` | Will delete the bookmark ID `bookmarkidherebookmarkidhere000000000000`.



## View Bookmark

This endpoint open's the bookmark ID provided.

### HTTP Request

`cclipss://bookmark/view/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bookmark to view

### Examples

URL | Description
--- | -----------
`cclipss://bookmark/view/bookmarkidherebookmarkidhere000000000000` | Will view the bookmark ID `bookmarkidherebookmarkidhere000000000000`.




# Projects

<aside class="notice">The user must be logged into the cclipss iOS application for project URL's to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Add Project

This endpoint displays the create project view with query parameter filled in. User will still have ability to make changes to project before saving or cancel creating the project (don't rely on this to create the project).

### HTTP Request

`cclipss://project/add` OR `cclipss://project/create`

### Query Parameters

Parameter | Default | Description | Example
--------- | ------- | ----------- | -------
title | nil | Project title that will be filled into view. | `My%20Project`

### Examples

URL | Description
--- | -----------
`cclipss://project/add` | Will display view to create project with nothing prefilled.
`cclipss://project/create?title=My%20Project` | Will display view to create project with `My Project` prefilled as the title.



## Edit Project

This endpoint displays the edit project view for the project ID given.

### HTTP Request

`cclipss://project/edit/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the project to edit

### Examples

URL | Description
--- | -----------
`cclipss://project/edit/projectidhereprojectidhereprojectidhere0` | Will display edit view for project ID `projectidhereprojectidhereprojectidhere0`.



## Delete Project

This endpoint delete's the project ID provided.

### HTTP Request

`cclipss://project/delete/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the project to delete

### Examples

URL | Description
--- | -----------
`cclipss://project/delete/projectidhereprojectidhereprojectidhere0` | Will delete the project ID `projectidhereprojectidhereprojectidhere0`.



## Select Project

This endpoint select's/deselect's the project ID provided.

### HTTP Request

`cclipss://project/select/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the project to select or deselect

### Examples

URL | Description
--- | -----------
`cclipss://project/select/projectidhereprojectidhereprojectidhere0` | Will select or deselect the project ID `projectidhereprojectidhereprojectidhere0`.





# Tags

<aside class="notice">The user must be logged into the cclipss iOS application for tag URL's to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Add Tag

This endpoint displays the create tag view with query parameter filled in. User will still have ability to make changes to tag before saving or cancel creating the tag (don't rely on this to create the tag).

### HTTP Request

`cclipss://tag/add` OR `cclipss://tag/create`

### Query Parameters

Parameter | Default | Description | Example
--------- | ------- | ----------- | -------
title | nil | Tag title that will be filled into view. | `My%20Tag`

### Examples

URL | Description
--- | -----------
`cclipss://tag/add` | Will display view to create tag with nothing prefilled.
`cclipss://tag/create?title=My%20Tag` | Will display view to create tag with `My Tag` prefilled as the title.



## Edit Tag

This endpoint displays the edit tag view for the tag ID given.

### HTTP Request

`cclipss://tag/edit/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the tag to edit

### Examples

URL | Description
--- | -----------
`cclipss://tag/edit/tagidheretagidheretagidheretagidhere0000` | Will display edit view for tag ID `tagidheretagidheretagidheretagidhere0000`.



## Delete Tag

This endpoint delete's the tag ID provided.

### HTTP Request

`cclipss://tag/delete/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the tag to delete

### Examples

URL | Description
--- | -----------
`cclipss://tag/delete/tagidheretagidheretagidheretagidhere0000` | Will delete the tag ID `tagidheretagidheretagidheretagidhere0000`.



## Select Tag

This endpoint select's/deselect's the tag ID provided.

### HTTP Request

`cclipss://tag/select/:ID`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the tag to select or deselect

### Examples

URL | Description
--- | -----------
`cclipss://tag/select/tagidheretagidheretagidheretagidhere0000` | Will select or deselect the tag ID `tagidheretagidheretagidheretagidhere0000`.





# Search

<aside class="notice">The user must be logged into the cclipss iOS application for the search URL to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Search Term

This endpoint filters bookmarks by search term.

### HTTP Request

`cclipss://search`

### Query Parameters

Parameter | Default | Description | Example
--------- | ------- | ----------- | -------
query | nil | Search term to filter bookmarks by. | `cclipss`

### Examples

URL | Description
--- | -----------
`cclipss://search?query=cclipss` | Search and filter bookmarks by `cclipss`.



# Filter

<aside class="notice">The user must be logged into the cclipss iOS application for the filter URL to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Filter

This endpoint filters bookmarks by search term, and/or project ID's, and/or tag ID's. It also deselects project or tag ID's to filter by if already selected.

### HTTP Request

`cclipss://filter`

### Query Parameters

Parameter | Default | Description | Example
--------- | ------- | ----------- | -------
tags | nil | Tag ID's to filter bookmarks by. | `tagidheretagidheretagidheretagidhere0000,tagidheretagidheretagidheretagidhere1111`
projects | nil | Project ID's to filter bookmarks by. | `projectidhereprojectidhereprojectidhere0,projectidhereprojectidhereprojectidhere1`
search | nil | Search term to filter bookmarks by. | `cclipss`

### Examples

URL | Description
--- | -----------
`cclipss://filter?search=cclipss` | Search and filter bookmarks by `cclipss`.
`cclipss://filter?tags=tagidheretagidheretagidheretagidhere0000,tagidheretagidheretagidheretagidhere1111` | Filter bookmarks by tag ID's `tagidheretagidheretagidheretagidhere0000` and `tagidheretagidheretagidheretagidhere1111`.



# Sign up

## Sign up

This endpoint displays the sign up view so a user can create an account. If user is already logged in this will log the user out and present the sign up view.

### HTTP Request

`cclipss://signup`

### Examples

URL | Description
--- | -----------
`cclipss://signup` | Display the sign up view.




# Upgrade

<aside class="notice">The user must be logged into the cclipss iOS application for the upgrade URL to work. If user is not signed in the application will take no action and dismiss the request silently.</aside>

## Upgrade Account

This endpoint displays the upgrade view so a user can upgrade to the Silver Plan. If the current user is already upgraded the application will display the user's subscription details.

### HTTP Request

`cclipss://upgrade` OR `cclipss://subscription` OR `cclipss://subscribe`

### Examples

URL | Description
--- | -----------
`cclipss://signup` | Display the upgrade view.
`cclipss://subscription` | Display the upgrade view.
`cclipss://subscribe` | Display the upgrade view.