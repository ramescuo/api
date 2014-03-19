---
category: Score
path: '/score'
title: 'Post a score'
type: 'POST'

layout: nil
---

Creates a score belonging to the logged in user. Since a file asset is attached the request must be a **`multipart/form-data`** request. This method is only available if the user is logged in. See [Authentication](#/authentication)

### Parameters

Name                 | Type                | Description                       | 
:--------------------|:--------------------|:----------------------------------|
**`score_data`**     | file, *required*    | the score file, mscz format only  |
**`title`**          | string, *required*  | Title of the score                |
**`description`**    | string              |  Description for the score        |
**`private`**        | boolean             | 1: private ; 0: *public*          |
**`license`**        | string              | *all-rights-reserved*, cc-by, cc-by-sa, cc-by-nd, cc-by-nc, cc-by-nc-sa, cc-by-nc-nd, publicdomain, cc-zero                            |
**`tags`**           | string              | *comma separated* list of tags    |
