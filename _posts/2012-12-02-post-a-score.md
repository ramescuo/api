---
category: Score
path: '/score'
title: 'Post a score'
type: 'POST'

layout: nil
---

Creates a score belonging to the logged in user. Since a file asset is attached the request must be a **`multipart/form-data`** request. This method is only available if the user is logged in. See [Authentication](#/authentication)

### Parameters

Name                 | Type                | Description                        | 
:--------------------|:--------------------|:-----------------------------------|
**`score_data`**     | file, *required*    |  The score file, mscz format only  |
**`title`**          | string, *required*  |  Title of the score                |
**`description`**    | string              |  Description for the score         |

