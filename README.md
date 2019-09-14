# Angular Learning

This project is developed to introduce and help you get understanding about Angular **Framework**. Point to note here that Angular is a **JavaScript Framework** and not a language or library.

Below content is inspired from [this site](https://www.sitepoint.com/angular-introduction/).

## What is (front-end) Framework / Library / Language?

(Front-end) Framework provide you a complete set of tools to develop your application; Whereas, libraries provide you a solution for a specific kind of requirement / problem. Languages (as we all know) is is a system of communication with a computer.
One major advantage of Angular framework is that it is _opinionated_, meaning it have it's own philosophy of how the web app should be built.

## History of Angualr Framework

In 2012, Google had introduced **AngularJs** _(kindly note, we are talking about AngularJS and not Angular here)_ to the world which was a sudden hit. It was built with the Model-View-Controller concept in mind, though authors of the framework often called it “Model-View-*” or even “Model-View-Whatever”. It came with many powerful features allowing the developer to create rich, **single-page applications (_the page does not refresh on navigation_)** quite easily. FYI, data-binding, dependency-injection, directives were few of the powerful feature of AngularJs. 

AngularJS became popular very quickly and received a lot of traction. Still, its maintainers decided to take another step further and proceeded to develop a new version which was initially named **Angular 2** (later, simply Angular without the “JS” part). It’s no coincidence the framework received a new name: actually, it was fully re-written and redesigned, while many concepts were reconsidered.

The first stable release of [Angular 2 was published in 2016](https://juristr.com/blog/2016/09/ng2-released/), and since then AngularJS started to lose its popularity in favor of a new version. One of the main features of Angular 2 was the ability to develop for multiple platforms: web, mobile, and native desktop (whereas AngularJS has no mobile support out of the box).

Then, to make things even more complex, by the end of 2016, Angular 4 was released. “So, where is version 3?”, you might wonder. I was asking the same question, as it appears that version 3 was never published at all! How could this happen? As explained in the official blog post, maintainers decided to stick with the semantic versioning since Angular 2.

Following this principle, changing the major version (for example, “2.x.x” becomes “3.x.x”) means that some breaking changes were introduced. The problem is that the Angular Router component was already on version 3. Therefore, to fix this misalignment it was decided to skip Angular 3 altogether. Luckily, the transition from Angular 2 to 4 was less painful than from AngularJS to Angular 2, though many developers were still quite confused about all this mess.

Angular 5 was released in November 2017. It is also backwards compatible with prior Angular versions.

As in Sept 2019, the latest version is Angular 8.


# Advantages of Angular

So, why Angular? Well, because it’s supported on various platforms (web, mobile, desktop native), it’s powerful, modern, has a nice ecosystem, and it’s just cool. Not convinced? Let me elaborate it for you then:

* **Angular presents you not only the tools but also design patterns to build your project in a maintainable way.** When an Angular application is crafted properly, you don’t end up with a tangle of classes and methods that are hard to modify and even harder to test. The code is structured conveniently and you won’t need to spend much time in order to understand what is going on.

* **It’s JavaScript, but better.** Angular is built with TypeScript, which in turn relies on JS ES6. You don’t need to learn a totally new language, but you still receive features like static typing, interfaces, classes, namespaces, decorators etc.

* **No need to reinvent the bicycle.** With Angular, you already have lots of tools to start crafting the application right away. You have directives to give HTML elements dynamic behavior. You can power up the forms using FormControl and introduce various validation rules. You may easily send asynchronous HTTP requests of various types. You can set up routing with little hassle. And there are many more goodies that Angular can offer us!

* **Components are decoupled.** Angular strived to remove tight coupling between various components of the application. Injection happens in NodeJS-style and you may replace various components with ease.

* **All DOM manipulation happens where it should happen.** With Angular, you don’t tightly couple presentation and the application’s logic making your markup much cleaner and simpler.

* **Testing is at the heart.** Angular is meant to be thoroughly tested and it supports both unit and end-to-end testing with tools like Jasmine and Protractor.

* **Angular is mobile and desktop-ready**, meaning you have one framework for multiple platforms.

* **Angular is actively maintained** and has a large community and ecosystem. You can find lots of materials on this framework as well as many useful third-party tools.

So, we can say that Angular is not just a framework, but rather a platform that empowers developers to build applications for the web, mobile, and the desktop.




# Requirements and setup to start learning Angular
_Let’s start building a complete web app sample project with Angular_

## Setup the Angular development environment
In this section we will show you how to setup your local development environment so you can start developing Angular apps. A real application development happens in a local development environment that could be your personal machine. Follow our setup instructions to create a new Angular project.

## Angular requirements: Install NodeJS and npm
Node.js and npm are fundamental to modern web development using Angular and other platforms. Node empowers client development and build tools. We are gonna use the node package manager (npm) to install all the JavaScript libraries dependencies. Get these right now if they’re not installed on your computer.

Note: Verify that you are running at least node 8.x and npm 6.x by running node -v and npm -v in a terminal/console window. Older versions may produce errors, but newer versions are always recommended.

## The Angular CLI
Angular apps are created and developed primarily through the Angular CLI (command line interface tool) that helps project creation, adding files, and performing a variety of ongoing development tasks.

The Angular CLI takes care of configuration and initialization of various libraries. It also helps us adding components, directives, services, etc, to already existing Angular applications. It’s also worth mentioning that the CLI uses Typescript and Webpack for module bundling, Karma for unit testing, and Protractor for an end to end testing. It includes everything you need to start writing your Angular application right away.

To install the Angular CLI globally, run the following command on your console npm install -g @angular/cli

Note: although it's not recommended, you may need to add "sudo" in front of these commands to install the utilities globally on Linux / Mac machines.

Important note: If you have an older version of the CLI installed in your computer, make sure you properly update it to the latest Angular CLI.



