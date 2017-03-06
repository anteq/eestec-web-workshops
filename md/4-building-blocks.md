# Building blocks
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg" -->

What is nowadays' web application made of?

You can think of it on maaaany levels.
E.g.
- domain name
- "look and feel"
- content to appear on the site
- hosting

---

#### Building blocks
## A brief explanation of how Internet works

- When you type eestec.net... 
- it resolves eestec.net to IP address that identifies the computer that has our site
- then our browser sends a HTTP request to this server: "hey, GET me this page"
- server has a process listening on :80 port 
- looks up the file on the HDD
- the page is like this (sample html page with a quote from HP)
- and sends it back to you
- your browser parses it
- and displays
- TADA
We could use some images here. Or yt video.

The computer that hosts our site is called "server". But it's nothing special really. Just a computer, usually without a screen and with great Internet connection.
No magic here :(.

---

#### Building blocks
# Dynamic Web

But... we don't want our site to have just a quote. Or text.
We want fireworks, login page, and randomized quotes!!11!
Note:
Not sure if it's proper naming though.

# How do we make dynamic page?
E.g. let's start with a randomized quote.
(that's a question)

#### You can...
## have different files with different quotes.
Naive, but ok. May work for a few quotes, but difficult in maintenance.

#### You can...
## have quotes as array of strings and make a process return a randomized quote instead of a html file
This might work, but it's hard to return sth more than 

### You can...
## have quotes as array of strings and create a HTML template and make your process replace the {{place for quote}}
That's just fine... but array of strings isn't the best possible way to do that, right?

### You can...
## store quotes and create a HTML template and make your process replace the {{place for quote}}
Scalable and cool.

## nowadays
Web service (usually) = Back-end + Front-end

# Why do you think it's worth to separate it?
(that's a question)

### Reason 1: Easier to maintain
Note:
When code is modular, it's much easier to work on it. 

### Reason 2: Many front-end apps to one back-end...
Note:
Mobile, destkop and web app use the same server.

### Reason 3: And many back-end apps to one front-end...
Note:
Frontend 

### Reason 4: Programmers like to ABSTRACT
Note:
Frontend dev doesn't need to know how the backend works - treats it like blackbox.
Backend dev doesn't need to know how data is presented.


