---
layout: post
title: How HelmetJS works,
tag: ExpressJS, JavaScript, Backend, Middleware
---
### Part 2: How HelmetJS works

## What is HelmetJS?
Helmet is a installable npm package and a type of **middleware** used in Express.JS applications by providing a form of app security for HTTP Response headers. It automatically setting HTTP headers by default unless configured specifically by the developer. 

## How it works
It helps secure your app by configurating the HTTP headers to hide sensitive information in your HTTP header responses about the server an app is running on. In the cybersecurity realm, it acts as security safeguard to hide the fingerprint or identity of underlying technologies used (server version, OS, etc.). 

Countermeasures HelmetJS provides
* Content Security Policy
* XSS Filtering
* HTTP Strict Transport Security


## Setting up HelmetJS
After setting our helmet dependency to use within the package.json. We add helmet to our express app in our main server.js file or the index.js in a typical JS server project directory. 

```
/* index.js for express in a JS backend app */

//call our dependencies from package.json
const express = require("express"); 
const helmet = require("helmet");


const app = express();

//apply helmet functionality to express app
app.use(helmet());

```
It works as a single wrapper^1 function that calls and invokes several  functions in itself. all eleven of wrapped middleware functions are enabled by default


---
 * readme for Helmet package https://github.com/helmetjs/helmet/blob/master/README.md