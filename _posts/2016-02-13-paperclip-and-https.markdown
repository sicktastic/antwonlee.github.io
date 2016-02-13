---
layout: post
title:  "Paperclip and HTTPS"
date:   2016-02-13 07:00:00
categories: Rails
banner_image: ""
featured: false
comments: true
---

Paperclip comes with setting for https. Set the values for <code>s3_protocol</code> to <code>https</code>.

Youc an review the documents <a href="http://www.rubydoc.info/gems/paperclip/Paperclip/Storage/S3" target="_blank">here</a>.

<!--more-->

{% highlight ruby %}
# config/environments/production.rb
config.paperclip_defaults = {
  :storage => :s3,
  :s3_region => ENV['S3_REGION'],
  :s3_protocol => :https,
  :s3_credentials => {
    :bucket => ENV['S3_BUCKET_NAME'],
    :access_key_id => ENV['AWS_ACCESS_KEY_ID'],
    :secret_access_key => ENV['AWS_SECRET_ACCESS_KEY']
  }
}
{% endhighlight %}
