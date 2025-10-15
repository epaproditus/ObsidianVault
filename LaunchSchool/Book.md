# Introduction

## [A Brief JavaScript History](https://launchschool.com/books/javascript/read/introduction#briefhistory)

JavaScript was created at Netscape Communications by Brendan Eich in 1995. Netscape and Eich designed JavaScript as a scripting language for use with the company's flagship web browser, Netscape Navigator. Initially known as LiveScript, Netscape changed the name to JavaScript so they could position it as a companion for the Java language, a product of their partner, Sun Microsystems. Apart from some superficial syntactic similarities, though, JavaScript is in no way related to the Java programming language.

After its release, more and more browsers started adding JavaScript support. Still, for much of its history JavaScript was not regarded as a serious programming language. Its earliest releases suffered from notable performance and security issues, but developers had no alternatives. If they wanted to run programs in the browser, they had to use JavaScript.

In 2008, the creation of Google's open-source Chrome V8, a high-performance JavaScript engine, provided a crucial turning point for JavaScript. The subsequent proliferation of fast JavaScript engines made it possible for developers to build sophisticated browser-based applications with performance that competed with desktop and mobile applications.

Soon after, Ryan Dahl released an open-source, cross-platform environment called [Node.js](https://nodejs.org/en/). It provided a way to run JavaScript code from outside a browser. It freed JavaScript from the browser's confines and led directly to JavaScript's current popularity. Today, you can use JavaScript to write all kinds of applications, including browser, server, mobile, and desktop applications. Most major online companies today, including Facebook, Twitter, Netflix, and Google, all use JavaScript in their products.

## [JavaScript's Future](https://launchschool.com/books/javascript/read/introduction#javascriptsfuture)

JavaScript has come a long way since its original implementation: it took a mere 10 days to write it. The JavaScript standard, proposed for the first time as ECMAScript 1 in 1997, is, as of late 2018, in its 9th iteration (ES 2018). The differences between the specifications described in ECMAScript 1 and ES 2018 are immense: they seem to describe different languages. In the intervening years, JavaScript has undergone massive changes. Not everyone agreed with every change, but, taken together, they made JavaScript a more robust, secure, and expressive language.

The JavaScript community of today is arguably the most active community in programming. It sometimes seems that every week sees releases of new tools, frameworks, and libraries. There are preprocessors and transpilers of all sorts available, ranging from programs that translate modern JavaScript programs so older JavaScript engines can run them, to compiling entirely new languages with JavaScript. The JavaScript standard itself is a continuously evolving document, with improvements introduced at a rapid rate. JavaScript engines incorporate the changes almost as rapidly. New operating systems under development (e.g., Google's Fuchsia) are adding support for the development of native applications in JavaScript. All of this means that JavaScript has an exciting future. It's a great time to learn JavaScript!

## [Abstraction](https://launchschool.com/books/javascript/read/introduction#abstraction)

In programming and computer science in general, there is a concept called abstraction. Abstraction ensures that users are far removed from what's happening "under the hood." A simple example should help illustrate the concept.

Think about the mobile phone you use every day to communicate with your friends and loved ones. You want to make and receive calls, use text messaging, check your Facebook/Twitter accounts and perhaps take some photos. As a user, you use the manufacturer's user interface to access the phone's basic features, but you probably don't know or care how to repair your phone or write software for it.

A phone technician, on the other hand, needs a different type of interface at a lower level of abstraction. She needs to know how the components work together so she can repair phones that aren't working. Software engineers must understand how the software subsystems interoperate and must also concern themselves with the Operating System and software development tools. That, too, is at another lower abstraction level.

A similar analysis applies to computers. The user uses computers to listen to music, send emails, play games, and more. They interact with the applications that make these tasks possible without any knowledge of the low-level details.

Programmers, however, operate at a lower-level of abstraction by using a programming language like JavaScript. JavaScript, in turn, gets processed by a runtime environment (sometimes called an engine) written in some other still-lower-level languages like C++. In turn, these engines convert JavaScript code into other even lower-level code until, after several iterations, the original JavaScript code ends up as a series of 1s and 0s that the computer understands. In effect, every programming language requires lower level layers of code that make it easy to use.

There are also higher-level abstractions. Some JavaScript programmers use the language to design and build tools that operate at a higher level, including libraries and frameworks like jQuery and React that are popular today. These tools let JavaScript developers build programs on top of existing components, without needing to know how to implement the features they provide.

As a beginner, it's vital for you to understand how JavaScript, the programming language, and the trendy tools and frameworks that you may have heard about, are at two different levels of abstraction. It's possible to learn the basics of some of these tools without understanding JavaScript; however, to fully take advantage of their power, you must understand the fundamentals first. Learning JavaScript to depth helps you better understand frameworks, and reading and maintaining programs that use those frameworks becomes easier. Understanding lower levels of abstraction will help you make better use of tools with higher abstraction levels. This book teaches you JavaScript so that you can recognize and use higher level abstractions with more granularity.

## [Who This Book is For](https://launchschool.com/books/javascript/read/introduction#whothisbookisfor)

This book's intended audience is the inexperienced or brand-new programmer. If you apply the principles and techniques described here, you'll acquire a strong foundation on which to build your JavaScript programming career. You may use this knowledge to continue to learn more integrated concepts.

This book guides you through the common pitfalls and time-sinks that beginners often experience. It also should provide you with enough practice to commit JavaScript's basic syntax to long-term memory and help you acquire a certain level of **muscle memory** that will help you as a programmer. With this background, you can focus on solving real-world problems and building applications to solve them.

Being a programmer is often perceived as difficult. It really isn't. It does, however, require a particular temperament: patience, persistence, focus, logic, detail-oriented, etc. When a programmer understands and adopts this temperament, their work becomes less frustrating, more fun, and rewarding.

Perception of a task's difficulty is often inversely proportional to the patience of the person attempting it. If you're patient with yourself and willing to take the time to work through the exercises and apply the concepts, you'll soon develop the temperament you need. Before you realize what's happening, you'll find yourself solving problems with code.

A shift in thinking must take place for most people. That will come with practice. Once it happens, your progress will accelerate. That will, in turn, help you develop the ability to think deeply about any programming problem. Most programmers find that being able to think deeply about problems is satisfying, engaging, and a rewarding perk of programming!

## [What's Not Covered](https://launchschool.com/books/javascript/read/introduction#whatsnotcovered)

While skimming through the contents of this book, you may notice that it doesn't cover all the topics that other JavaScript books cover. The omissions are intentional: JavaScript and programming are huge topics, and you'll benefit most from focusing on the fundamentals. Our goal is to introduce you to programming. JavaScript, the language, happens to be the vehicle that we are using. As such, it covers the essential information you need to start your journey towards becoming a professional programmer.

Launch School's teaching philosophy centers around [Mastery Based Learning](https://launchschool.com/mastery), which means, among other things, that we introduce students to a new topic only when they have mastered the concepts needed to understand that topic. Learning the basic grammar of a programming language and solving computational problems with that language is a complex skill in its own right. You don't want to spend time learning peripheral information until you have the background and experience to solve programming problems with code.

Let's take a brief look at some of the topics that we chose to omit from this book, but which you may find in some other introductory JavaScript material. Bear in mind that we cover all of these topics in depth in our Core Curriculum at Launch School, so we don't ignore them. However, there's a time and a place where a novice programmer is ready to learn about certain topics.

### The DOM API

Historically, JavaScript was inextricably tied to the DOM (Document Object Model) API, which is what you use to manipulate content on a webpage. It is, in essence, the entire reason the language came about. Those days are past. While the DOM is still a major focus of JavaScript programmers, it's no longer quite so central to the language. Our goal isn't to teach you JavaScript for the DOM, but to teach it as a general programming language. Later, you can choose to add the DOM API to your toolkit, go the server-side route and learn about Node.js, or do something else entirely with your JavaScript knowledge.

### Asynchronous Programming

In the wild, JavaScript often has to deal with asynchronous operations: for example, requesting and then displaying data from a database. However, this is an advanced feature that is best understood when you have a solid grounding in the basics. There's a reason programmers joke about JavaScript "callback hell," and we don't want to get into that too soon. In the beginning, you won't have the context needed to understand why you need asynchronous operations. For that reason, we don't present it in this book.

### Object-Oriented JavaScript

Aside from a brief introduction to JavaScript objects, we'll leave the OOP concepts for the future. Right now, you need to focus on basic concepts; you need to absorb those concepts before you're ready to tackle OOP.

### Testing

Testing is crucial to writing good code; however, we don't believe that an "introduction to programming" book is the best place to cover it. Testing is a technique that is best learned after you've faced the problems that it attempts to solve. You need to have written sufficiently large programs to grasp that context. We cover testing extensively in our [Core Curriculum](https://launchschool.com/courses).

## [How to Read This Book](https://launchschool.com/books/javascript/read/introduction#howtoreadthisbook)

Reading about programming and writing a program aren't the same. If you read this entire book without ever writing a line of code, you may understand, intellectually, how to code, but you won't know how to **do it**. If someone asks you to solve a problem with a computer program, you won't be able to complete the task.

There is a "muscle memory" aspect to programming that books and courses often overlook. With the vast amount of information that a programmer must remember, practicing some skills until they become automatic is unquestionably crucial. It doesn't require much effort; it happens naturally through repetition and practice. You can learn with your fingers, and, when you do, you free up your brain to focus on higher-level abstractions.

If you want a real shot at learning how to code, you should do every exercise in this book. If you want to learn a musical instrument, you must _practice_ your scales on that instrument and develop proficiency before you can _play_ the instrument well.

Think of the exercises as though you are a musician practicing musical scales and writing a program as playing the instrument. Use the exercises to practice and cement the basics into your fingers. The more you practice, the more coding becomes second nature and subconscious, and that helps you learn to program.

This book's target audience is the beginner. In the world of computer programming, there is an enormous amount of information to learn; it isn't possible to learn it all. We recognize that, and intentionally avoid topics that aren't beneficial to the beginner. Trust these omissions; we've had some experience with teaching, and know how easy it is to get lost "down the rabbit hole" looking for information on unimportant topics. Instead, stay focused. You'll progress at a much faster rate if you do.

That about covers it. Get ready to build the skills you need to become a computer programmer. Don't worry; we'll be here to coach you along the way. Buckle up and enjoy the ride!