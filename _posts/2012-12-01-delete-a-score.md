---
category: Score
path: '/score/{id}'
title: 'Delete a score'
type: 'DELETE'

layout: nil
---

This method allows the user to delete a score.

### Request

* **`{id}`** is the id of the score to delete.

### Response

{% highlight bash %}
$ curl 'http://api.musescore.com/score/17?oauth_consumer_key=your_consumer_key' -X DELETE
< HTTP/1.1 200 OK
{% endhighlight %}