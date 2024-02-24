## Story of JavaScript 
<img src="https://th.bing.com/th/id/OIP.DpeuhHbnB6m2uE2A5UTpBAHaFj?w=240&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7" width="200px">
Brendan Eich: -The developer of JavaScript.

In 1993, the first web-browser was released, named Mosaic. After which Netscape Corporation was established and Netscape Navigator was released in 1994. In 1995, Netscape decided to add a scripting language to the Navigator, and Brendan Eich was hired to develop it. In 10 days, JavaScript was ready and named Live Script. In December 1995, it was renamed from Live Script to JavaScript. There was also a big reason behind naming JavaScript because at that time Java language was very famous, so they named JavaScript similar to Java to get fame in the market.

<img src="https://www.versionmuseum.com/images/applications/netscape-browser/netscape-browser%5E1995%5Enetscape-navigator-2.0-mac.jpg" width="200px">
Netscape Navigator(web-browser)



After this, Microsoft introduced its own web browser in 1995, which was named Internet Explorer. Now due to two web-browsers in the market, the browser war between Netscape Navigator and Internet Explorer has started. Microsoft created a new language for its Internet Explorer called JScript by reverse engineering. JScript was first released in 1996, which supported CSS. The biggest problem with this was that the web developer had to connect with more users, for which he had to work separately for both browsers. Later, Internet Explorer covered 95% of the market at the cost of its brand.

<img src="https://media.dcnews.ro/image/202105/w1200/logo-internet-explorer_66183000.jpg" width="200px">
Internet Explorer(browser)

Now it's time for the third browser. The third browser was released in 2004 by Mozilla called Firefox.


<img src="https://th.bing.com/th/id/OIP.met2AGps8yR80QgnYwdvgAHaHe?pid=ImgDet&rs=1" width="200px">
Firefox(browser)

Everyone was releasing their own web browser, so Google was also going to lag behind. Google released its browser, named Google chrome in 2008.it was the most powerful browser ever used the V8 engine in it.

<img src="https://th.bing.com/th/id/OIP.eWgDcQjWpovhVepWuer9jgHaD5?pid=ImgDet&rs=1" width="200px">
Google Chrome(browser)


For so many browsers, the web developer had to write code that would support all browsers. This work took a lot of time and was also a bit confusing. To solve this problem, a conference was held in 2008 and an agreement was reached with all browser companies that all would use the same standard language for their browsers. Script 5 was then standardized in December 2009, which was supported in all browsers. The biggest update for JavaScript was ECMAScript 6, which added a lot of new features in it like let const  arrow function etc.



# Brief intro to javascript?

JavaScript was initially created to “make web pages alive”.

The programs in this language are called scripts. They can be written right in a web page’s HTML and run automatically as the page loads.

Scripts are provided and executed as plain text. They don’t need special preparation or compilation to run.

In this aspect, JavaScript is very different from another language called Java.

But as it evolved, JavaScript became a fully independent language with its own specification called ECMAScript, and now it has no relation to Java at all.

Today, JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called the JavaScript engine.You can run javascript any where with javascript engine.

The browser has an embedded engine sometimes called a “JavaScript virtual machine”.

Different engines have different “codenames”. For example:

V8 – in Chrome, Opera and Edge.
SpiderMonkey – in Firefox.

There are other codenames like “Chakra” for IE, “JavaScriptCore”, “Nitro” and “SquirrelFish” for Safari, etc.

Javascript engine converts the javascript code to machine code to execute it fast.

Javscript is able to do.

1. Add new HTML to the page, change the existing content, modify styles.
2. React to user actions, run on mouse clicks, pointer movements, key presses.
3. Send requests over the network to remote servers, download and upload files (so-called AJAX and COMET technologies).
4. Get and set cookies, ask questions to the visitor, show messages.
5. Remember the data on the client-side (“local storage”).


### Javascript can do only limited things in browser.
1. JavaScript on a webpage may not read/write arbitrary files on the hard disk, copy them or execute programs. It has no direct access to OS functions.
2. Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions, like “dropping” a file into a browser window or selecting it via an <input> tag.
3. There are ways to interact with the camera/microphone and other devices, but they require a user’s explicit permission. So a JavaScript-enabled page may not sneakily enable a web-camera, observe the surroundings and send the information to the NSA.
4. Different tabs/windows generally do not know about each other. Sometimes they do, for example when one window uses JavaScript to open the other one. But even in this case, JavaScript from one page may not access the other page if they come from different sites (from a different domain, protocol or port).
5. This is called the “Same Origin Policy”. To work around that, both pages must agree for data exchange and must contain special JavaScript code that handles it. We’ll cover that in the tutorial.
6. JavaScript can easily communicate over the net to the server where the current page came from. But its ability to receive data from other sites/domains is crippled. Though possible, it requires explicit agreement (expressed in HTTP headers) from the remote side. Once again, that’s a safety limitation.
7. Such limitations do not exist if JavaScript is used outside of the browser, for example on a server. Modern browsers also allow plugins/extensions which may ask for extended permissions.

## What makes JavaScript unique?
There are at least three great things about JavaScript:

1. Full integration with HTML/CSS.
2. Simple things are done simply.
3. Supported by all major browsers and enabled by default.

JavaScript is the only browser technology that combines these three things.

## Languages “over” JavaScript

The syntax of JavaScript does not suit everyone’s needs. Different people want different features.

That’s to be expected, because projects and requirements are different for everyone.

So, recently a plethora of new languages appeared, which are transpiled (converted) to JavaScript before they run in the browser.

Modern tools make the transpilation very fast and transparent, actually allowing developers to code in another language and auto-converting it “under the hood”.

Examples of such languages:

1. CoffeeScript is “syntactic sugar” for JavaScript. It introduces shorter syntax, allowing us to write clearer and more precise code. Usually, Ruby devs like it.
2. TypeScript is concentrated on adding “strict data typing” to simplify the development and support of complex systems. It is developed by Microsoft.
3. Flow also adds data typing, but in a different way. Developed by Facebook.
4. Dart is a standalone language that has its own engine that runs in non-browser environments (like mobile apps), but also can be transpiled to JavaScript. Developed by Google.
5. Brython is a Python transpiler to JavaScript that enables the writing of applications in pure Python without JavaScript.
6. Kotlin is a modern, concise and safe programming language that can target the browser or Node.



## Summary

1. JavaScript was initially created as a browser-only language, but it is now used in many other environments as well.
2. Today, JavaScript has a unique position as the most widely-adopted browser language, fully integrated with HTML/CSS.
3. There are many languages that get “transpiled” to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.


# Defination

Js is a high-level,single-threaded garbage collected interpreted or jist in time compiled,prototype-based, multiparadigm dynamic language with a non blocking event loop made famus for building websites it was created in 1995 in just one week by brenden eich with the goal of adding an easy to learn scripting language to netscape browser it was originally named Mocha but the genius marketing people of the time wanted it to sound like that sexy new java language today its a fully featured language that contains to evolve through the Ecma-script standards. 

1. Mocha
2. Es3
3. Es5
4. Es6
5. Ts

Its well known for building frontend web applicaions because its only language other than web-assembly that is nativelly supported in browsers however.
Its an interpred language but tools like V8 engine and chromium uses a JIT compiler to convert ot to machine code at run time.


# Javascript language

1. Interpreted
2. c-styleSyntax
3. Dynamic Typing
4. Object-Oriented
5. Prototype-bases
6. Functions
7. Single-Threaded


It is originally designed as a client-side scripting language to enhance web pages with interactivity and dynamic content. But now it becomes a versetile language thats why it is also used for server-side development.


Js can interact with dom to modify the content of the webpage also with conditions and used to style pages dynamically.




