---
category: Score
path: '/score'
title: 'Search scores'
type: 'GET'

layout: nil
---

This method will retrieves all scores or search for scores with the following criteria

### Request

An unauthenticated request shows only public scores while an authenticated one will show all the scores the logged user has access to.

#### Filters

Name       | Type     | Description |
:----------|:---------|:------------|
**`text`**     | string   | a string to search for (use double quotes to do literal string matching) |
**`part`**     | integer |  \[-1;-128\] a [midi program number](http://en.wikipedia.org/wiki/General_MIDI#Melodic_sounds), zero based indexed. Drumset is 128 and -1 is undefined    |
**`parts`**    | integer |  the number of parts in the score. 1 for solo scores. 2 for duo etc...  |
**`language`**           | [2 letters language code](http://api.drupal.org/api/function/_locale_get_predefined_list/6)    |     Lyric language    |
**`page`**     | integer | Zero based index of the result page. Pages contain 20 results.     |
**`license`**     | license | *to_modify_commercially*, *to_use_commercially*, *to_share*, *to_play* (default)    |         

#### Sort criteria

A **`sort`** parameter can be used to sort the scores according to one of the following criteria.

Name       |  Description |
:----------|:---------|
**`view_count`** |  sort the score with the most viewed one first |
**`date_uploaded`** |  most recent score first|
**`comment_count`** |  sort the score with the most commented one first |
**`relevance`**     |  (default) sort the score with the most relevant according to the filters first |

### Response

An array of score objects.

### Example

* Piano + Flute
```http://api.musescore.com/services/rest/score.xml&oauth_consumer_key=musichackday&part=0,73```

* Sorted by view count 
```http://api.musescore.com/services/rest/score.xml&oauth_consumer_key=musichackday&part=0,73&sort=view_count```

* Filtering by licence
```http://api.musescore.com/services/rest/score.xml&oauth_consumer_key=musichackday&license=to_modify_commercially```

