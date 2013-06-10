---
category: Score
path: '/score/{id}'
title: 'Delete a score'
type: 'DELETE'

layout: nil
---

This method allows the user to delete a score.

### Parameters

Name 			 |  Type     | Description              |
:----------------|:----------|:-------------------------|
**`id`**     	 | integer   | unique id of the score 	|

### Response

{% highlight bash %}
$ curl 'http://api.musescore.com/score/17?oauth_consumer_key=your_consumer_key' -X DELETE
< HTTP/1.1 200 OK
{% endhighlight %}