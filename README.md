### HttpClient
---
https://github.com/nahi/httpclient

```
httpclient get https://www.google.co.jp/?q=ruby
httpclient

get "http://www.google.co.jp/", :q => :ruby

```

```
require 'httpclient'
c = HTTPClient.new
c.redirect_uri_callback = proc { |uri, res| URI.escape(res.headers["Location"]) }
p c.get("http://bit.ly/eDWCrk", :follow_redirect => true)

```



