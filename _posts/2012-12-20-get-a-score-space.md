---
category: Score
path: '/score/space/{id}'
title: 'Get score space info'
type: 'GET'

layout: nil
---

Send back the bounding boxes around the measures in the graphical representation. A scaling factor may apply. (12 for PNG).

### Parameters

Name 			 |  Type     | Description     |
:----------------|:----------|:----------------|
**`id`**     	 | integer    | unique id of the score 	|
**`secret`**     | string    | _optional_ 	   |
  
If the user is authenticated, the secret is not needed to access public resources. See [OAuth](#/authentication) for authentication.   


### Response


{% highlight bash %}
$ curl http://api.musescore.com/services/rest/score/583/time.xml?oauth_consumer_key=your_consumer_key
< HTTP/1.1 200 OK
{% endhighlight %}

{% highlight xml %}

<?xml version="1.0" encoding="utf-8"?>
<events is_array="true">
    <event>
      <elid>0</elid>
      <position>0</position>
    </event>
    <event>
      <elid>1</elid>
      <position>250</position>
    </event>
    <event>
       <elid>2</elid>
       <position>1159.090909090909</position>
    </event>
   ...
 </events>
 {% endhighlight %}

**`elid`** is the zero based index of the measure. The same id is used in the space representation.
**`position`** is a time position in ms and is in sync with the MP3 and the MIDI file provided by the API
