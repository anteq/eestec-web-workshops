# Backend
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg"; background-size: 80% -->

Remember how internet works?

Backend = server process. <br />
Any language, really.

<!-- .slide: data-background-image="http://www.reactiongifs.com/r/rbp.gif" -->
Any?

#### CGI (Common Gateway Interface)
An interface enabling communication between WWW server and other programms that run on server. <br />
![http://www.sergey.com/web_course/images/cgi.jpg](http://www.sergey.com/web_course/images/cgi.jpg)
Note:
Za pomocą programów CGI można dynamicznie (na żądanie klienta) generować dokumenty HTML, uzupełniając je np. treścią pobieraną z bazy danych.

Of course, usually it's in Python. Java. JavaScript. Scala. PHP.

How about a server... in C. :D <br />
<img src="http://kimkarpeles.com/wp-content/uploads/2013/05/work-in-progress1.png" height="300px"></img>
Note:
Exercise

---

#### Backend
# The meat

<!-- .slide: data-background-image="https://68.media.tumblr.com/bde33ad2ec722b87057642e8b9a8af1e/tumblr_nwy9cfQScI1ukrx8mo1_400.gif" --> 
#### Ok, but handling requests like that manually sucks.

### Remember
1. Engineers are lazy. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Engineers like to abstract. <!-- .element: class="fragment" data-fragment-index="2" -->

Therefore... we can automate this stuff!

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/39/38/cc/3938cc46030d661fc8d5f29199063447.gif" -->

A **web framework** is a way to automate repeating tasks (like request handling, socket operations, persisting the session etc.).

It also allows you to organize your code properly, use packages developed by community and soooo much more.

---

#### Backend
# MVC

If you'll remember one thing from this workshops - let it be it. :)

MVC = Model View Controller.

It's a *software architecture pattern* - a general reusable solution to a commonly occurring problem. In this case - organizing code in website.

1. Model - represents the problem or application logic <!-- .element: class="fragment" data-fragment-index="1" -->
2. View - describes how to present certain Model's part in user interface <!-- .element: class="fragment" data-fragment-index="2" -->
3. Controller - updates Model and refreshes View <!-- .element: class="fragment" data-fragment-index="3" -->
Note:
- MVC (wzorzec Model View Controller i jego odmiany) i jak jest robione gdzie indziej

1. Model - what is the data? <!-- .element: class="fragment" data-fragment-index="1" -->
2. Controller - what am I doing? <!-- .element: class="fragment" data-fragment-index="2" -->
3. View - what do I see? <!-- .element: class="fragment" data-fragment-index="3" -->

![http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png](http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png)

### Why?
- reusability of code <!-- .element: class="fragment" data-fragment-index="1" -->
- less mess <!-- .element: class="fragment" data-fragment-index="2" -->
- easy to test and troubleshoot <!-- .element: class="fragment" data-fragment-index="3" -->
- de facto a standard <!-- .element: class="fragment" data-fragment-index="4" -->

![](http://s2.quickmeme.com/img/21/2142bd8b63c2985b650a7796ee0767f0e07f8de2f6540dab06d1760b68faa134.jpg)