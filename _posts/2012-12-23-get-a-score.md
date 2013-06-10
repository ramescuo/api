---
category: Score
path: '/score/{id}'
title: 'Get score'
type: 'GET'

layout: nil
---

Retrieves a given score.

### Parameters

Name 			 |  Type     | Description     |
:----------------|:----------|:----------------|
**`secret`**     | string    | _optional_ 	   |
  
If the user is authenticated, the secret is not needed to access public resources. See [[OAuth]] for authentication.                                                        

### Response

A score object

### Example

{% highlight bash %}
$ curl http://api.musescore.com/services/rest/score/583.xml?oauth_consumer_key=musichackday
< HTTP/1.1 200 OK
{% endhighlight %}