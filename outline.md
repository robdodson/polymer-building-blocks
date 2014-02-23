Intro
---

Hey I'm Rob Dodson,

I'm a developer advocate on the Google Chrome team and specifically I work on a project called Polymer. Quick show of hands, how many of you have heard of or worked with Polymer before?

So our agenda today is we're going to first figure out what is Polymer and what are Web Components, and then we're going to show off some cool stuff that actually uses all of these new tools.


Let's talk about tabs
---

To kick things off, I want to start by looking at tabs. Here I've got some vertical tabs and some horizontal ones. And tabs are a seemingly easy UI element to implement (essentially a horizontal or vertical list) but in practice they can be a pain in the butt. I want to show you some examples of what I'm talking about...


Building a tab component on the web
---

If you're using a library like Bootstrap or Foundation you might build your tabs like this. You'd copy a bunch of code out of their docs and paste it into your app. Which means eventually your whole app is full of boilerplate markup that you've pulled out of some framework. And that's bad :(

As we've gone through this JavaScript renaissance, we've started moving more of this effort out of our markup and into our JS. So here's an example that uses KendoUI. Less markup, but more JS. And it goes on and on until you end up with something like EXT where it's just all JavaScript. And that's kind of bad because we're forcing JavaScript to do all of this stuff that it wasn't intended for. It also makes it harder for designers because they can't do anything without using our huge javascript framework. -- TODO: Why else is it bad?


<tabs/>
---

It's disappointing because really all we want is this. If a <tabs> tag existed, I wouldn't think twice about using it, the same way I don't think about using <input> or <textarea>. But because this *doesn't* exist, we're forced to work around the browser's shortcomings. And that means we waste time and effort.

Now, we do have elements which are *kind of* like tabs. We have the <select> element. And I want to take a moment to explore the <select> element because I think the more we understand about why HTMLElements are awesome, the easier it will be for us to figure out how the web should look in the coming years.


<select/>
---

1. Select is easy to grok and comes with built in behavior and style
2. Select is easy to configure
3. You can drastically change the appearance of select with one attribute
4. You can compose elements inside of select and change its behavior and appearance
5. Select is kind of bullet proof
6. You can compose select inside of another element to build something bigger and more complex.


Working with elements...
---


<tabs/>
---

So, how do we make this a reality. How do we bring the tabs element to everyone.


polymer
---

At Google we've been working on a project called Polymer.

and, in a nutshell, Polymer is a library for creating your own HTML Elements.


standards
---

Under the hood, polymer leverages emerging web standards like Templates, etc. which are collectively referred to as Web Components.

These standards are working their way through the W3C right now, and Polymer aims to get developers working with them early so developers can give feedback to the W3C.


Layers of Polymer
---

So, how do we do that? That sounds like a really big thing!

It helps to think of Polymer in terms of layers. At the very bottom you have the current browser landscape. So, whatever's possible in browsers today.

The first thing we add is a layer of polyfills called "The Platform." The Platform adds support for the specs that make up Web Components. The platform's job is to jump everyone into the future and to make it possible to create your own elements. Over time, as browser makers add support for the Web Components technologies, the platform will go away.

Next we add a layer of sugaring called polymer.js. This layer adds additional features like data-binding, change handlers and automatic node finding.

Finally, we have a set of drop-in elements that ship with polymer that any developer can use to start building their application.


Using Elements
---

You don't have to know about their internals

They're easy to add to your project
