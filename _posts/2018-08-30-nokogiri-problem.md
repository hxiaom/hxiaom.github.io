---
layout: post
title: "Error in installing nokogiri (1.8.4)"
categories: Software
---

1. 在本地化Github Page的bundle install步骤报错如下
```
An error occurred while installing nokogiri (1.8.4), and Bundler cannot
continue.
Make sure that `gem install nokogiri -v '1.8.4' --source
'https://rubygems.org/'` succeeds before bundling.
```
解决方案：
```
gem install nokogiri -v '1.8.4' --source 'https://rubygems.org/'
```

2. 通过1.中解决方案中的命令，继续报错如下
```
Team Nokogiri will keep on doing their best to provide security
updates in a timely manner, but if this is a concern for you and want
to use the system library instead; abort this installation process and
reinstall nokogiri as follows:

    gem install nokogiri -- --use-system-libraries
        [--with-xml2-config=/path/to/xml2-config]
        [--with-xslt-config=/path/to/xslt-config]
```
参考https://github.com/SlatherOrg/slather/issues/227，解决方案：
```
sudo gem install nokogiri -v '1.8.4' -- --with-xml2-include=/usr/include/libxml2 --use-system-libraries
```

3. 通过2.中解决方案的命令，报错如下
```
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /usr/bin directory.
```
参考https://www.jianshu.com/p/b8406ff1e2f1，解决方案：
```
sudo gem install nokogiri -v '1.8.4' -n /usr/local/bin -- --with-xml2-include=/usr/include/libxml2 --use-system-libraries
```
