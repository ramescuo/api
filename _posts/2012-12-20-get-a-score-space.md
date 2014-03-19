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
$ curl http://api.musescore.com/services/rest/score/583/space.xml?oauth_consumer_key=your_consumer_key
< HTTP/1.1 200 OK
{% endhighlight %}

{% highlight xml %}
<?xml version="1.0" encoding="utf-8"?>
  <elements is_array="true">
    <element>
       <id>0</id>
       <x>1183.1868963254592</x>
       <y>2356.5019173228343</y>
       <sx>1014.2236806299212</sx>
       <sy>1321.9491732283464</sy><page>0</page>
    </element>
    <element><id>1</id>...</element>
  </elements>
 {% endhighlight %}

**`id`** is the unique id of the measure
**`x`** and **`y `** are the coordinates of the measures in the page.
**`sx`** and **`sy`** are the width and the height of a measure.


