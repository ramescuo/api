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
      "license":null,
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


  