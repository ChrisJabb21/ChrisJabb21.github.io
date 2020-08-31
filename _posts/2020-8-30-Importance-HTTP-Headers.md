---
layout: post
title: Importance of Securing HTTP Headers
tag: ExpressJS, Java, JavaScript, Backend, Middleware, InfoSec
author: Chris Jabbour
---

Securing HTTP Headers in a web app provides a layer of protection based on what is suitable for your app and security goals. It is done by setting up an app's HTTP response headers to prevent sensitive information being exposed when passed between a server and a client. We can use middleware modules that lets allows setting and configuring the response headers for a client-server based web application.

## :// Why bother with HTTP Headers?
---
Without setting up and configuring the HTTP headers in an application, each response from the client will return a http header that can reveal server information (e.g. Apache, Express, or IIS) and other details that can be exploited by vulnerabilities. This becomes important if your app is handling sensitive and confidential user information.

If a malicious actor, or hopefully a penetration tester or white hat hacker, has enough information on your underlying technologies or the version of your server. The data revealed can lead it be used as part of an attack using an exploit strategy that can lead to a data breach. Whatever that is good news depends on who finds it first. Another way to get information on a server or host is using a vulnerablity scanner like Metasploit to check running services and their versions for vulnerablities.



## :// Safeguards and what they protect from
---

* Disabling Cache-Control Header ``` cache-control: no-cache, no-store, must-revalidate``` to prevent caching of confidental resources.

* Enforcing HTTPS to protect connections against Man in the Middle attacks.

* Enabling XSS filtering to protect against cross site scripting attacks.

* setting ```X-Frame-Options: SAMEORIGIN``` to block clickjacking.

* using X-Content-Type-Options header to prevent MIME-sniffing attacks.

---

I will get to a more code based approach and example of this in my next post on the HelmetJS package which I came across while learning the Node and Express JS frameworks; going into detail on how it achieves security and configures your HTTP headers automatically for a Express app. I can go into more details about the how the attacks occur in another post.

This is all I have for this post. I just wanted to briefly go over the security importance of HTTP headers.  If there is anything you would like me to add or any comments and suggestions feel free to reach out to me on my social platforms. Until next time, happy creating, learning and exploring. 


## Keywords / Learn More
* Web Application Security
* Middleware 
* HTTP Headers
* Spring Security for Spring
* HelmetJS for Express and Node

## Further Reading & References 
 * [Don't let your response headers talk to loudly by Troy Hunt](https://www.troyhunt.com/shhh-dont-let-your-response-headers/)
* [How To Secure Your Web App With HTTP Headers](https://www.smashingmagazine.com/2017/04/secure-web-app-http-headers/) 
* [How to use metasploit to scan for vulnerabilities](https://jonathansblog.co.uk/how-to-use-metasploit-to-scan-for-vulnerabilities)
* [Spring Security 5.2.2 Security HTTTP Response Headers ](https://docs.spring.io/spring-security/site/docs/5.0.x/reference/html/headers.html)
* [HelmetJS see-also page](https://helmetjs.github.io/see-also/)
