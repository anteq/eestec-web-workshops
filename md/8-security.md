# Security

### Everyone makes mistakes!

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/89/fa/06/89fa06b360359633a8d2f3887cd85fe1.jpg" -->

### One about a few chars that brought Chrome down
https://www.youtube.com/watch?v=0fw5Cyh21TE

## Remember:
- Build your apps like you're being attacked, beacuse eventually you will be!
- Never trust user input
- Assume that anything sent to your website is malicious unless proven otherwise
- Prepare for the worst
- Think "How could I break this?"

## Authentication and Authorization is not the same thing!!!
- Veryfiny that a user provided their security credentials correctly
- Confirming that a particular user has access to a specific resource
Note:
1. authentication 2. Authorization
Note: 
https://dzone.com/articles/10-most-common-web-security-vulnerabilities

## Open Web Application Security Project (Good guy OWASP)
- 

### 1. Injection Flaws
Happens while passing unfiltered data
Never use a blacklist - hard to create, easy to bypass
Note:
SQL injection, browser, LDAP server (katalogowanie)

## 1. Injection Flaws (Prevention)
- Filter and conquer
- Rely on framework's filtering functions

## 2. Broken Authentication 
- Today nobody roll their own authentication code because it is to hard
### Possible problems:
- The URL might contain the session ID and leak it in the referer header to someone else
- The passwords might not be encrypted either in storage or transit
- The session IDs might be predictable, thus gaining access is trivial
- Session fixation might be possible
- Session hijacking might be possible, timeouts not implemented right or using HTTP (no SSL)

## 2. Broken Authentication (Prevention)
- Again - use framework

## 3. Cross Site Scripting (XSS)
### In other words - input sanitazation failure
Note: 
An attacker gives your web application JavaScript tags on input. When this input is returned to the user unsanitized, the user's browser will execute it. It can be as simple as crafting a link and persuading a user to click it, or it can be something much more sinister. On page load, the script runs and, for example, can be used to post your cookies to the attacker

### One about a XSS security hole in Twitter
https://www.youtube.com/watch?v=zv0kZKC6GAM

## 3. Cross Site Scripting (XSS) (Prevention)
### DO NOT return HTML tags to the client
Note:
Usually, the workaround is simply converting all HTML entities—so that script is returned as <>script <>. The other often employed method of sanitization is using regular expressions to strip away HTML tags using regular expressions on < and >, but this is dangerous. A lot of browsers will interpret severely broken HTML just fine. Better to convert all characters to their escaped counterparts. 

## 4. Insecure Direct Object References
### Internal object such as a file or database key is exposed to the user

## 4. Insecure Direct Object References (Prevention)
- Perform user authorization properly and consistently
- Whitelist the choices
- store data internally and not rely on it being passed from the client via CGI parameters
- and use frameworks :)

## 5. Security Misconfiguration
- Running the application with debug enabled in production.
- Having directory listing enabled on the server, which leaks valuable information.
- Running outdated software (think WordPress plugins, old phpMyAdmin).
- Having unnecessary services running on the machine.
- Not changing default keys and passwords. (Happens way more frequently than you'd believe!)
- Revealing error-handling information to the attackers, such as stack traces.

## 5. Security Misconfiguration (Prevention)
- Good (preferably automated) "build and deploy" process, which run test on deploy

## 6. Sensitive Data Exposure
### Sensitive data should be encrypted at all times, including in transit and at rest
###  Credit card information and user passwords should never travel or be stored unencrypted, and passwords should always be hashed

## 6. Sensitive Data Exposure (Prevention)
- In transit: Use HTTPS with a proper certificate and PFS (Perfect Forward Secrecy). Do not accept anything over non-HTTPS connections. Have the secure flag on cookies.
- In storage: This is harder. First and foremost, you need to lower your exposure. If you don't need sensitive data, shred it.

# Data you don't have can't be stolen 
//Stan Lee

## 7. Missing Function-Level Access Control 
- In other words an authorization failure

## 7. Missing Function-Level Access Control (Prevention)
On the server side, authorization must always be done! Always! I really mean always!

## 8. Cross Site Request Forgery (CSRF)
If you are logged in on one tab on your bank's homepage, for example, and they are vulnerable to this attack, another tab can make your browser misuse its credentials on the attacker's behalf, resulting in the confused deputy problem. The deputy is the browser that misuses its authority (session cookies) to do something the attacker instructs it to do.
Note:
Fun fact: CSRF is also the method people used for cookie-stuffing in the past until affiliates got wiser.

## 8. Cross Site Request Forgery (CSRF) (Prevention)
Store a secret token in a hidden form field which is inaccessible from the third-party site

## 9. Using Components With Known Vulnerabilities
Note:
The title says it all. Again, I'd classify this as more of a maintenance/deployment issue. Before incorporating new code, do some research, possibly some auditing. Using code that you got from a random person on GitHub or some forum might be very convenient, but is not without risk of serious web security vulnerability.
I have seen many instances, for example, where sites got owned (i.e., where an outsider gains administrative access to a system), not because the programmers were stupid, but because a third-party software remained unpatched for years in production. This is happening all the time with WordPress plugins, for example. If you think they will not find your hidden phpMyAdmin installation, let me introduce you to DirBuster.
The lesson here is that software development does not end when the application is deployed. There has to be documentation, tests, and plans on how to maintain and keep it updated, especially if it contains third-party or open-source components.

## 9. Using Components With Known Vulnerabilities (Prevention)
- do not be a copy-paste coder
- Stay up to date

## 10. Unvalidated Redirects and Forwards
- This is once again an input filtering issue
Note:
Suppose that the target site has a redirect.php module that takes a URL as a GETp parameter. Manipulating the parameter can create a URL on targetsite.comthat redirects the browser to malwareinstall.com. When the user sees the link, they will seetargetsite.com/blahblahblah, which the user thinks is trusted and is safe to click. Little do they know that this will actually transfer them onto a malware drop (or any other malicious) page. Alternatively, the attacker might redirect the browser to targetsite.com/deleteprofile?.

## 10. Unvalidated Redirects and Forwards (Prevention)
- Don't do redirects at all (they are seldom necessary)
- Have a static list of valid locations to redirect to
- Whitelist the user-defined parameter, but this can be tricky
