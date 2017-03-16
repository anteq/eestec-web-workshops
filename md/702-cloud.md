#### Scaling up
# And about the cloud...

Amazon <br />
![yt](jOhbTAU4OPI)

[https://console.aws.amazon.com/s3/home?region=eu-central-1#](https://console.aws.amazon.com/s3/home?region=eu-central-1#)

---

#### Scaling up
# Not f**ing things up

In big application... it's easy to mess something up.

Like, commit one bad line.

Or forget to do something.

Solution?

### Tests
- Unit tests
- Integration tests
- Sanity tests
- Acceptance tests

You can even have a test environment!

```
http://yourawesomeapp.com
http://test.yourawesomeapp.com
```
We call it **production** environment and **test** environment.

---

#### Scaling up
# Automation

Every time you change something in your code you need to...

- commit the code
- compile the app <!-- .element: class="fragment" data-fragment-index="1" -->
- run some tests <!-- .element: class="fragment" data-fragment-index="2" -->
- deploy to test environment <!-- .element: class="fragment" data-fragment-index="3" -->
- run other tests <!-- .element: class="fragment" data-fragment-index="4" -->
- deploy to production environment <!-- .element: class="fragment" data-fragment-index="5" -->
- restart server <!-- .element: class="fragment" data-fragment-index="6" -->
- maybe something else <!-- .element: class="fragment" data-fragment-index="7" -->
- (after some time) it works! <!-- .element: class="fragment" data-fragment-index="8" -->

### Remember
1. Engineers are lazy. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Engineers like to abstract. <!-- .element: class="fragment" data-fragment-index="2" -->

So why bother?

- commit the code <!-- .element: class="fragment" data-fragment-index="1" -->
- MAGIC <!-- .element: class="fragment" data-fragment-index="2" -->
- (after some time) it works! <!-- .element: class="fragment" data-fragment-index="3" -->

### Continuous (.*)
![https://4.bp.blogspot.com/-L0bNvBeUJ0M/VwAwnxFmZEI/AAAAAAAABcg/kitQ5yqe3BsIprPs_E714JzVjIRPVN72w/s1600/CI_CDY_CDT_04.png](https://4.bp.blogspot.com/-L0bNvBeUJ0M/VwAwnxFmZEI/AAAAAAAABcg/kitQ5yqe3BsIprPs_E714JzVjIRPVN72w/s1600/CI_CDY_CDT_04.png)

### Jenkins
![http://www.tothenew.com/blog/wp-content/uploads/2016/09/jenkins_image.png](http://www.tothenew.com/blog/wp-content/uploads/2016/09/jenkins_image.png) <!-- .element: style="height:300px" --> <br />
Used by Facebook, LinkedIn, Tumblr, Netflix and many many more
Note:
[Online demo](https://ci.jenkins-ci.org/)

### Similar: Chef
![https://spaceapetech.files.wordpress.com/2015/11/chef_logo.png](https://spaceapetech.files.wordpress.com/2015/11/chef_logo.png) <!-- .element: style="height:300px" --> <br />
A little bit different though - focused on deployment part. <br />
Used by Facebook, MSN, Bloomberg, GE, Yahoo...

### Similar: Travis
![https://www.freebsdnews.com/wp-content/uploads/Travis-CI-logo.jpg](https://www.freebsdnews.com/wp-content/uploads/Travis-CI-logo.jpg) <!-- .element: style="height:300px" --> <br />
A little bit different though - really simple integration with open source. <br />
Used by Zendesk, Heroku, BitTorrent and many many more...

---

#### Scaling up
# Managing dependencies

Libraries, bundles, gems?!

Generally our app should have:
- a program that downloads all the dependencies and knows where to find them
- a list of dependencies to be downloaded

Javascript (browser): e.g. bower && Bower.json
![https://johnpapa.net/content/images/2016/05/861bower.jpg](https://johnpapa.net/content/images/2016/05/861bower.jpg)

Javascript (server): e.g. node && package.json
![http://npm.click/images/packagejson.png](http://npm.click/images/packagejson.png)

Python: e.g. pip && requirements.txt
![https://morannachum.files.wordpress.com/2015/03/img5.png](https://morannachum.files.wordpress.com/2015/03/img5.png)

Java: e.g. Maven && pom.xml
![https://netbeans.org/images_www/articles/72/javaee/mavenentapp/maven-earpom.png](https://netbeans.org/images_www/articles/72/javaee/mavenentapp/maven-earpom.png)

Ruby: e.g. gem && Gemfile
![https://softcover.s3.amazonaws.com/636/ruby_on_rails_tutorial_4th_edition/images/figures/cloud9_gemfile_4th_ed.png](https://softcover.s3.amazonaws.com/636/ruby_on_rails_tutorial_4th_edition/images/figures/cloud9_gemfile_4th_ed.png)

...

---

#### Scaling up
# Blocked pipes

![yt](AskUF2mebi4)

---

#### Scaling up
# Caching

...

---

#### Scaling up
# Availability

Kinda like cloud, but also not.
![yt](SdVWAX2Js-g)
Note: Cheaper etc.

CDN (Content Delivery Network). Content. <br />
Content = Static files => such as video, pictures and pages that don't change

- Amazon CloudFront
- CloudFlare
- MaxCDN
- M$ Azure
- ...
