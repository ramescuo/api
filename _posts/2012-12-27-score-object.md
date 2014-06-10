---
category: Score
title: "The Score object"
layout: nil
---

The score object is represented in XML or in JSON and **`GET`** calls to the MuseScore.com API will send back a single object or an array.

### JSON example

{% highlight json %}
{
      "id":"1111",
      "vid":"152152",
      "dates":{
         "posted":"1370593443",
         "lastupdate":"1370593602"
      },
      "secret":"b364acd291",
      "uri":"http:\/\/api.musescore.com\/services\/rest\/score\/1111",
      "permalink":"http:\/\/musescore.com\/score\/1111",
      "user":{
         "uid":"400",
         "username":"Mozart"
      },
      "status":"ready",
      "sharing":"public",
      "comment_count":"0",
      "favoriting_count":0,
      "view_count":"14",
      "playback_count":"6",
      "download_count":4,
      "genre":"",
      "format":"",
      "license":"all-rights-reserved",
      "language":null,
      "title":"Title of my score",
      "description":"Galactic score",
      "metadata":{
         "title":"My First score",
         "subtitle":null,
         "composer":"WA Mozart",
         "poet":null,
         "pages":"9",
         "measures":"102",
         "lyrics":"0",
         "chordnames":"0",
         "keysig":"0",
         "duration":"474",
         "dimensions":"210x297",
         "parts":[
            {
               "part":{
                  "name":"Flute",
                  "program":"73"
               }
            },
            {
               "part":{
                  "name":"Piano",
                  "program":"0"
               }
            }
         ]
      }
   }
  {% endhighlight %}

**`id`**
: The score id, an integer. It's a unique identifier for the score

**`vid`**
: Version id of the score, an integer. It will change if the score is updated.

**`posted`**
: The date when the score has been posted in seconds, unix time.

**`lastupdate`**
: The date when score was last updated. The score file has changed or any metadata such as title.

**`secret`**
: The secret of the score, a unique string

**`uri`**
: API endpoint for this score

**`permalink`**
: Permalink to the score page on MuseScore.com, suitable for human

**`uid`**
: The unique identifier of the owner of this score

**`username`**
: The user screen name of the owner of this score

**`status`**
: The status of the score, currently only "ready" scores are presented through the API

**`sharing`**
: either **`public`** or **`private`**

**`comment_count`**
: Number of comments on this score

**`favoriting_count`**
: Number of users who favorited this score

**`view_count`**
: Number of views for this score

**`playback_count`**
: Number of plays for this score

**`download_count`**
: Number of downloads for this score

**`genre`**
:

**`format`**
:

**`license`**
: The license of the score 
* **`all-rights-reserved`**
* **`publicdomain`**
* **`cc-zero`**
* **`cc-by`**
* **`cc-by-sa`**
* **`cc-by-nd`**
* **`cc-by-nc`**
* **`cc-by-nc-sa`**
* **`cc-by-nc-nd`**

**`language`**
: Language of the lyrics as provided by the user. It's a [2 letters language code](http://api.drupal.org/api/function/_locale_get_predefined_list/6), null or empty if the user did not provide it

**`title`**
: Title of the score, as filed by the user when uploading the score. This title can be different from the one in metadata

**`description`**
: Description of the score, as file by the user when uploading or updating the score

#### Metadata

Metadata are automatically extracted from the score file

**`title`**
: The first title text of the score file

**`subtitle`**
: The first subtitle text in the score file

**`composer`**
: The first composer text in the score file

**`poet`**
: The first poet/lyricist text in the score file

**`pages`**
: The number of pages in the score, when the score is displayed as the user sees it in MuseScore 

**`measures`**
: The number of measures in the score

**`lyrics`**
: **`0`** if the score has no lyrics, **`1`** otherwise

**`chordnames`**
: **`0`** if the score has no chord names, **`1`** otherwise

**`keysig`**
: The first key signature of the score. \[-7;+7\] it's the number of flat/sharps for the first key signature, first staff of the score.

**`duration`**
: duration of the score in seconds, including repeats

**`dimensions`**
: paper size of the score in mm and formatted **`width`**x**`height`**

**`parts`**
: An array describing the parts of the score. Each part has a name and a [midi program number](http://en.wikipedia.org/wiki/General_MIDI#Melodic_sounds), zero based indexed.
