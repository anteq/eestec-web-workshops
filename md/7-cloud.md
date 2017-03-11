# Scaling up
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg" -->

#### More users => more problems.

---

#### Scaling up
# A story

So let's assume that...

<!-- .slide: data-background-image="https://az616578.vo.msecnd.net/files/2016/02/28/6359227563928979181633060127_giphy.gif" -->
#### ... your product...

<!-- .slide: data-background-image="http://i.imgur.com/Rfs4RM3.gif" -->
#### ... becomes a big success.

<!-- .slide: data-background-image="https://media.giphy.com/media/kGbJ7AgPJlcVW/giphy.gif" -->
#### Your clients want more...

<!-- .slide: data-background-image="http://www.breakingbadgifs.com/gifs/gifs/gus-fring/breaking-bad-gif-gus-fring-6071591.gif" -->
#### ... new clients are lining up to do business with you ...

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/3d/e0/6f/3de06f8950f474cd775a0b03aac7e3f7.jpg" -->
#### ... but your app wasn't designed to handle that much people!

<!-- .slide: data-background-image="http://a.fod4.com/misc/tumblr_m1z9b7NEc51rt40rso1_500.gif" -->
#### People are calling you, telling that the site is slow...

<!-- .slide: data-background-image="http://a.fod4.com/misc/bbs4e42.gif" -->
#### ... and you're sick of it creating hotfixes instead of changing the app's architecture.

<!-- .slide: data-background-image="http://gifrific.com/wp-content/uploads/2012/08/Jesse-Pinkman-Walter-White-handshake.gif" -->
#### You cannot handle it alone.

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/68/37/b1/6837b1f2d98dc72baa5286ad1b33db7d.jpg" -->
#### You may try to add more resources, people to help...

<!-- .slide: data-background-image="http://a.fod4.com/misc/tumblr_m1b1c2SAPN1r94e9jo1_500.gif" -->
#### ...but you don't want to handle them! That's too much mess?

What do you do?

<!-- .slide: data-background-image="https://media.tenor.co/images/21b7acf789efdc9e6919623111c21bfd/raw" -->

You go all the way up to the sky.

<!-- .slide: data-background-image="https://media.giphy.com/media/PaKMBTzu2G0Qo/giphy.gif" -->

---

#### Scaling up  
# Cloud as a developer

Remember the building blocks?

1. Server.
2. Database.
3. Server process.
4. HTML.
5. CSS.
6. JS.

Cloud allows you to focus on the important stuff - the content.

### But that means that I lose control over some parts!!1!!

<!-- .slide: data-background-image-"https://uproxx.files.wordpress.com/2013/08/01-1-bright-side.gif" -->

## Why?
- easy to scale
- easy to maintain
- easy to start


#### Scaling up
# Different ways

You can keep control over different layers. <br />
(start drawing here)

## IaaS (Infrastructure as a Service)
Note:
As the name suggests, provides you the computing infrastructure, physical or (quite often) virtual machines and other resources like virtual-machine disk image library, block and file-based storage, firewalls, load balancers, IP addresses, virtual local area networks etc. Examples: Amazon EC2, Windows Azure, Rackspace, Google Compute Engine.

## PaaS (Platform as a Service)
Note: as the name suggests, provides you computing platforms which typically includes operating system, programming language execution environment, database, web server etc. Examples: AWS Elastic Beanstalk, Windows Azure, Heroku, Force.com, Google App Engine, Apache Stratos.

## SaaS (Software as a Service)
Note: model you are provided with access to application softwares often referred to as on-demand softwares. You don't have to worry about the installation, setup and running of the application. Service provider will do that for you. You just have to pay and use it through some client. Examples: Google Apps, Microsoft Office 365.

![http://pbxl.co.jp/wordpress/wp-content/uploads/2015/05/cloud_en.png](http://pbxl.co.jp/wordpress/wp-content/uploads/2015/05/cloud_en.png)

![http://mschnlnine.vo.llnwd.net/d1/inetpub/kevinremde/Images/679669067395_DBE9/image_3.png](http://mschnlnine.vo.llnwd.net/d1/inetpub/kevinremde/Images/679669067395_DBE9/image_3.png)

---

#### Scaling up  
# Cloud as a user

![https://www.youtube.com/watch?v=TTNgV0O_oTg](https://www.youtube.com/watch?v=TTNgV0O_oTg)

So...

- Gmail uses cloud.
- Youtube uses cloud.
- Your phone uses cloud.

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
# Blocked pipes

MQ to the rescue!

---

#### Scaling up
# Availability

![yt](SdVWAX2Js-g)

CDN (Content Delivery Network). Content.

Content = Static files => such as video, pictures and pages that don't change

- Amazon CloudFront
- CloudFlare
- MaxCDN
- M$ Azure
- ...

