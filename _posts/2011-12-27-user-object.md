---
category: User
title: "The User object"

layout: nil
---

The user object is represented in XML or in JSON and **`GET`** calls to the MuseScore.com API will send back a single object or an array.

### JSON example

{% highlight json %}
{
   "id":"5",
   "name":"Nicolas",
   "permalink":"http:\/\/musescore.com\/nicolas",
   "uri":"http:\/\/api.musescore.com\/services\/rest\/user\/5"
}
{% endhighlight %}

**`id`**
: The user id, an integer. It's a unique identifier for the user

**`name`**
: User name on MuseScore.com

**`uri`**
: API endpoint for this user

**`permalink`**
: Permalink to the user page on MuseScore.com, suitable for human
