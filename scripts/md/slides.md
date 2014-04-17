title: about:me
id: who

<p class="avatar rounded"></p>

<p>Rob Dodson</p>
<p>Staff Developer Advocate, <img src="images/logos/google_logo.png" style="height: 30px;margin: 0;"> <img src="images/logos/chrome_logo.png" style="height:27px;margin:0;vertical-align: top;"></p>

<p class="topmargin"></p>

<i class="icon icon-google-plus"></i>
<a rel="author" href="http://google.com/+RobDodson">google.com/+RobDodson</a>

<i class="icon icon-twitter"></i>
<a rel="author" href="http://twitter.com/rob_dodson">@rob_dodson</a>

<i class="icon icon-bookmark"></i> 
<a rel="author" href="http://robdodson.me">robdodson.me</a>

<aside class="note">
  <section>
    <p>Introduce yourself, mention contact info</p>
    <p>
      Quick show of hands, who here has heard of Polymer or Web Components?
    </p>
  </section>
</aside>

---

id: agenda
title: Today's agenda
class: large

<div class="topmargin">
  <div>
    <h3>What is Polymer?</h3>
    <br>
  </div>
  <div>
    <h3>Working with Polymer</h3>
    <br>
  </div>
  <div>
    <h3>Example time</h3>
    <br>
  </div>
</div>

<aside class="note">
  <section>
    <ul>
      <li>What is Polymer? What are Web Components?</li>
      <li>Start working with Polymer so you can use Web Components in modern browsers</li>
      <li>We'll save some time and show some cool demos</li>
    </ul>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">Let's go back in time...</h2>

<aside class="note">
  <section>
    <p>To understand Web Components we have to go back in time to the early days of the web design...</p>
  </section>
</aside>

---

id: netscape
#title: Understand where we came from
class: nobackdrop nobackground
#image: images/bgs/netscape_blank.png
content_class: flexbox vcenter
body_class: netscape


<template id="formexample" style="display: none">
  <style>body{margin:0;padding:0;}</style>
  <form>
    <table class="build" border="10" cellpadding="5" cellspacing="5">
    <tr><td><label>First name:</td><td><input type="name"></td></tr>
    <tr><td><label>Last name</td><td><input type="name"></label></td></tr>
    <tr><td>T-shirt size</td><td>
      <select>
        <option>Small</option>
        <option selected>Medium</option>
        <option>Large</option>
        <option>X-large</option>
      </select>
    </td></tr>
    <tr><td><label>Gender</label></td><td>Male: <input type="radio"  name="gender"> Female: <input type="radio" name="gender"></td></tr>
    <tr><td colspan="2"><input type="submit"></td></tr>
    </table>
  </form>
</template>

<iframe id="formframe" style="width:300px;border:none;height:240px;"></iframe>

<script>
  var clone = document.querySelector('#formexample').content.cloneNode(true);
  var div = document.createElement('div');
  div.appendChild(clone);
 document.querySelector('#formframe').srcdoc = div.innerHTML;
</script>

<aside class="note">
  <section>
    <br>
    <p>
      For many developers this is what their first site looked like. This is just HTML elements bolted together like Legos. It may seem dated, but it *is* a functioning web app.
    </p>
    <p>
      As we've been going through this JavaScript renaissance we've lost sight of the power of HTML elements. But when you stop to think about it...
    </p>
  </section>
</aside>

---

content_class: flexbox vcenter

<h2>Elements are the building blocks of the web</h2>
<img src="./images/screenshots/legos.png" style="position: absolute; bottom: -500px; right: -350px;">

<aside class="note">
  <section>
    <p>
      Elements have some really cool properties and I want to explore those for a second...
    </p>
  </section>
</aside>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>encapsulated</em></h2>

<aside class="note">
  <section>
    <p>Elements are encapsulated, and encapsulation is really hard to come by on the Web</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select>
  &lt;option>Small&lt;/option>
  &lt;option>Medium&lt;/option>
  &lt;option>Large&lt;/option>
&lt;/select>
</pre>

<select class="corner top right">
  <option>Small</option>
  <option>Medium</option>
  <option>Large</option>
</select>

<aside class="note">
  <section>
    <p>This is the code to make a select element show up. Notice how I didn't have to include any CSS to make this element look the way it looks. That's because those styles are baked into the element and scoped to the tag. They don't leak out onto the page.</p>
    <p>And when I click on it, it has behavior but I didn't need to write any JavaScript to make that happen and my JavaScript isn't going to accidentally break that behavior. That's because select is a well encapsulated object.</p>
  </section>
</aside>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>configurable</em></h2>

<aside class="note">
  <section>
    <p>Another cool feature of elements is that they're configurable</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select id="schwag">
  ...
  &lt;option <b>disabled</b>>Medium&lt;/option>
  &lt;option <b>disabled</b>>Large&lt;/option>
  &lt;option <b>selected</b>>XX-large&lt;/option>
&lt;/select>
</pre>

<select id="schwag" class="corner top right">
  <option disabled>Small</option>
  <option disabled>Medium</option>
  <option disabled>Large</option>
  <option selected>XX-large</option>
</select>

<aside class="note">
  <section>
    <p>Notice how easy it is to change the behavior of select by adding a few attributes. No JS required!</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight" style="margin-left: -100px;">
&lt;select <b>size="4"</b> <b>multiple</b>>
  &lt;option>Do&lt;/option>
  &lt;option>Re&lt;/option>
  &lt;option>Mi&lt;/option>
  ...
&lt;/select>
</pre>

<select size="4" multiple class="corner top right">
  <option>Do</option>
  <option>Re</option>
  <option>Mi</option>
  <option>Fa</option>
  <option>So</option>
  <option>La</option>
  <option>Ti</option>
  <option>Do</option>
</select>

<aside class="note">
  <section>
    <p>And if you add a multiple attribute then you get a completely different presentation and behavior! Now we can select multiple items at once just by holding down the cmd/ctrl key.</p>
  </section>
</aside>

---

hidden: true
class: large
content_class: flexbox vcenter


<pre class="nohighlight">
&lt;select>
  &lt;option>Small&lt;/option>
  <s>&lt;li>Medium&lt;/li></s>
  &lt;option>Large&lt;/option>
&lt;/select>
</pre>

<select class="corner top right">
  <option>Small</option>
  <li>Medium</li>
  <option>Large</option>
</select>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>composable</em></h2>

<aside class="note">
  <section>
    <p>Meaning you can treat elements like Legos and bolt them together</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;select>
  &lt;optgroup label="German Cars">
    &lt;option>Mercedes&lt;/option>
    &lt;option>Audi&lt;/option>
  &lt;/optgroup>
  ...
&lt;/select>
</pre>

<select class="corner top right">
  <optgroup label="German Cars">
    <option value="mercedes">Mercedes</option>
    <option value="audi">Audi</option>
  </optgroup>
  <optgroup label="American cars">
    <option value="ford">Ford</option>
    <option value="gm">GM</option>
  </optgroup>
</select>

<aside class="note">
  <section>
    <p>For example, if you wrap your option elements in optgroups, then the select element is smart enough to know that it should render differently. Now you get subheadings inside your dropdown.</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
<b>&lt;form></b>
  &lt;select name="size">
    &lt;option value="s">Small&lt;/option>
    &lt;option value="m">Medium&lt;/option>
    &lt;option value="l">Large&lt;/option>
  &lt;/select>
<b>&lt;/form></b>
</pre>

<aside class="note">
  <section>
    <p>And if you put a select element inside of a form element then you've created a much more complex component. Now whenever the form is submitted it will take the value from the select and pass that along to our server.</p>
    <p>This is one of the main goals of good composability: building complex things out of simple building blocks</p>
  </section>
</aside>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded">Elements are <em>programmable</em></h2>

<aside class="note">
  <section>
    <p>Lastly, elements are programmable. I've shown you a lot of the declarative side of things, but don't forget that elements also have a nice *imperative* API for things that don't make sense to show in markup.</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
var foo = mySelect.selectedIndex;
</pre>

<aside class="note">
  <section>
    <p>selectedIndex, for example, wouldn't be very useful in HTML, but it makes total sense to have it in JavaScript.</p>
    <p>So when you're working with elements you get the best of both worlds: a nice declarative syntax for bolting things together, and a programmable API for when you need to delve into script.</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vleft

<h2 style="margin-top: 33%">So what happened?</h2>

<aside class="note">
  <section>
    <p>It seems like a great model, right? So why don't we primarily work with elements anymore?</p>
    <p>The main reason is because there just aren't enough elements to capture the breadth of what we want to do on the web. And because the platform has never given us the ability to extend HTML, we've been forced to invent solutions.</p>
  </section>
</aside>

---

id: tab-examples
title: Building a tab component today

<div class="build flexbox vcenter centered">
<img src="images/screenshots/tabs/jquery.png">
<img src="images/screenshots/tabs/kendo.png">
<img src="images/screenshots/tabs/yui.png">
<img src="images/screenshots/tabs/angular.png">
<img src="images/screenshots/tabs/sencha.png">
<img src=""> <!-- intentional. holder to see all images together -->
</div>

<aside class="note">
  <section>
    <p>Let's look at how we build UI today. This is an example of building a tabs widget.</p>
    <p>This first example is really typical of something like Bootstrap. Lots of boilerplate markup which you'll have to copy and paste over and over again in your app. Cover it with CSS and maybe use some jQuery to kick off the behavior.</p>
    <p>Now that we're going through a JavaScript renaissance, we're starting to move more of the responsiblity for rendering our UI out of our markup and into or JS. So here's an example from kendo UI. Less markup, but more JS</p>
    <p>And here's YUI... Angular... EXT.js... The problem here is that if we build a great component using one framework, we can't share it with people using a different framework. We're silo'd.</p>
  </section>
</aside>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight" style="margin-top: -50px;">
&lt;x-tabs&gt;
  &lt;x-tab&gt;Tab 1&lt;/x-tab&gt;
  &lt;x-tab&gt;Tab 2&lt;/x-tab&gt;
  &lt;x-tab&gt;Tab 3&lt;/x-tab&gt;
&lt;/x-tabs&gt;
</pre>

<aside class="note">
  <section>
    <p>And it's a shame because really all we want is something like this. If this existed I would just use it, the same way I use `select`.</p>
    <p>Thankfully, today it is possible to start creating elements like this, thanks to a new set of technologies called Web Components</p>
  </section>
</aside>

---

content_class: flexbox vleft

<h2 style="font-size: 60px; line-height: 1.25;">Web Components are a set of <strong>emerging standards</strong> that allow developers to <strong>extend HTML</strong>.</h2>

<aside class="note">
  <section>
    <p>In a nutshell this means "giving developers the ability to create their own tags that have scoped CSS styles and encapsualted markup and behavior."</p>
  </section>
</aside>

---

class: nobackdrop nobackground browser-support
content_class: flexbox vcenter

<div class="flexbox">
  <h2>Templates</h2>
  <div class="browser-support-row">
    <div class="supported"><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Custom Elements</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Shadow DOM</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>HTML Imports</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported partial"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<aside class="note">
  <section>
    <p>There's no one Web Components technology, it's actually 4 different technologies which collectively form the Web Components umbrella</p>
    <ul>
      <li>Templates give you the ability to create reusable bits of DOM markup. If you've used a library like handlebars or mustache before then it should feel familiar. The difference now is that there is an actual &lt;template&gt; tag in the browser</li>
      <li>Custom elements give you the ability to create your own custom HTML elements. The x-tabs example from before is an instance of a custom element.</li>
      <li>Shadow DOM is the ability to create scoped styles and encapsulated markup. So you can put some HTML and CSS inside of the Shadow DOM and you're guaranteed your element will render as intended.</li>
      <li>Finally HTML Imports give you the ability to load external HTML files into your document. These files can contain resources like CSS, JavaScript and (most likely) custom element defintions.</li>
    </ul>
    <p>Talk about support chart. It's good, but developers won't use Web Components until they're supported in *all* browsers. But we want developer feedback before we ship these things. For that reason we created Polymer.</p>
  </section>
</aside>

---

class: nobackdrop nobackground yum
content_class: flexbox vcenter centered

<img src="images/logos/lockup.svg" style="height:180px;">

---

content_class: flexbox vleft

<h2 style="font-size: 60px; line-height: 1.25;">Polymer is a library that uses the latest <strong>web technologies</strong> to let you create <strong>custom HTML elements</strong>.</h2>

<!-- font-size: 42px; width: 52%; line-height: 1.3; -->

<aside class="note">
  <section>
    <p>It gives you the power of web components today</p>
    <p>You can start working with them and give feedback to the browser makers</p>
    <p>So... how do we do that?</p>
  </section>
</aside>

---

id: layers-of-polymer
class: polymer-diagram
title: Layers of Polymer

<div id="blocks-3d">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<div class="build diagram-explanations">
  <div id="diagram-animate-in" data-build-index="1"></div>
  <div id="diagram-explode" data-build-index="2"></div>

  <div id="diagram-elements" class="diagram-explanation" data-build-index="6">
    <h3 class="elements bold">Elements</h3>
    <p>Reusable custom elements (in progress)</p>
  </div>

  <div id="diagram-polymer" class="diagram-explanation" data-build-index="5">
    <h3 class="core bold">Polymer</h3>
    <p>An opinionated way to work with Web Components</p>
  </div>

  <div id="diagram-platform" class="diagram-explanation" data-build-index="4">
    <h3 class="platform bold">Platform</h3>
    <p>Web Components polyfills for all <br>modern browsers</p>
  </div>

  <div id="diagram-native" class="diagram-explanation" data-build-index="3">
    <h3 class="bold">Native</h3>
    <p>The current browser landscape</p>
  </div>
</div>

<aside class="note">
  <section>
    <p>Here's a breakdown of how we add support for Web Components into all browsers</p>

    <ul>
      <li>Native: We start off with whatever level of support your current browser has. If that's something like mobile safari it might mean there's no support for web components at all!</li>
      <li>Platform: Polyfills web component support and jumps everyone into the future so they can start creating their own elements</li>
      <li>Polymer: Features and sugars. Things not on the standards track but we think are awesome so we include them. Two-way data binding, automatic node finding and a great declarative syntax</li>
      <li>Elements: Lastly, we include a set of pre-built elements which are ready to be dropped into any project</li>
    </ul>
  </section>
</aside>

---

hidden: true
id: philosophy
title: Three ways to work with Polymer
build_lists: true
class: large
#content_class: flexbox vcenter

<div class="build topmargin">
  <div>
    <h3><b class="elements">Using</b> elements</h3>
    <br>
  </div>
  <div>
    <h3><b class="core">Creating</b> elements</h3>
    <br>
  </div>
  <div>
    <h3>Utilizing the modern web <b class="platform">platform</b></h3>
    <br>
  </div>
</div>

---

content_class: flexbox vcenter

<h2>Three ways to work with Polymer</h2>

<aside class="note">
  <section>
    <p>So there's really 3 ways to work with Polymer</p>
  </section>
</aside>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Using</em> elements</h2>

<aside class="note">
  <section>
    <p>You can use the elements that Polymer and the open source community provide</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Creating</em> elements</h2>

<aside class="note">
  <section>
    <p>You can create your own elements</p>
  </section>
</aside>

---

body_class: platform-fill
content_class: flexbox vcenter

<h2 class="faded">Utilizing the modern web <em>platform</em></h2>

<aside class="note">
  <section>
    <p>Or you can work directly with that shimmed web platform level. If you're not ready to use Web Components but maybe you want to play around with imports or one of the other technologies then you can actually break off the indivudal polyfills and use them stand alone</p>
  </section>
</aside>

---

id: using-elements
title: Using <label class="elements">elements</label>
subtitle: <a href="http://www.polymer-project.org/docs/elements/" class="nounderline">polymer-project.org/docs/elements/</a>
class: nobackdrop nobackground segue elements polymer-diagram
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<aside class="note">
  <section>
    <p>(wait for animation)</p>
    <p>Let's start by talking about how you can use elements</p>
  </section>
</aside>

---

body_class: elements-fill
content_class: flexbox vcenter

<h2 style="font-size: 55px; letter-spacing: 0;">Everything is an element</h2>

<aside class="note">
  <section>
    <p><b>We want you to reach for the element</b></p>
  </section>
</aside>

<aside class="note">
  <section>
    <p>When you get started using elements we really want to get you into the mindset of thinking about "everything as an element." When you feel yourself reaching for the JavaScript, stop yourself, and ask "Could I solve this problem with an element instead."</p>
  </section>
</aside>

---

id: polymer-ui-elements
title: Polymer UI elements
subtitle: visual elements

<div class="pull-right flexbox vcenter" style="width: 40%;margin-top:-100px;">
  <img src="images/polymer/uielements/polymer-ui-tabs.png" style="width:100%">
  <div class="flexbox vcenter" style="height:auto;">
  <img src="images/polymer/uielements/sidebarmenu.png">
  <img src="images/polymer/uielements/polymer-ui-toggle-button.png" style="margin-left:20px;">
  </div>
  <img src="images/polymer/uielements/toolbar.png" style="width:100%">
</div>

`<polymer-ui-accordion>`

`<polymer-ui-animated-pages>`

`<polymer-ui-overlay>`

`<polymer-ui-card>` [demo](http://www.polymer-project.org/components/polymer-ui-card/smoke.html)

`<polymer-ui-sidebar-menu>` [demo](http://www.polymer-project.org/components/polymer-ui-sidebar-menu/smoke.html)

`<polymer-ui-tabs>` [demo](http://www.polymer-project.org/components/polymer-ui-tabs/smoke.html)

`<polymer-ui-toggle-button>` [demo](http://www.polymer-project.org/components/polymer-ui-toggle-button/smoke.html)

`<polymer-ui-theme-aware>`

<aside class="note">
  <section>
    <p>Stress that elements are experimental (and visually disjointed) but let them know we're building something real.</p>
  </section>
</aside>

<aside class="note">
  <section>
    <p>To help you out we've created some reusable UI elements. So we have things like polymer-ui-card (click on link and show demo), which is a nice swipeable Google Now style card</p>
    <p>We've also got polymer-ui-sidebar, (click on link and show demo) which is your classic expanding/collapsing sidebar</p>
    <p>And yes, we even include our own version of tabs!</p>
  </section>
</aside>

---

id: polymer-ui-tabs-demo
title: Everything is an element
subtitle: Tabs revisited

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-tabs.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-ui-tabs selected="0"&gt;
  &lt;span&gt;Home&lt;/span&gt;
  &lt;span&gt;About&lt;/span&gt;
  &lt;span&gt;Contact&lt;/span&gt;
&lt;/polymer-ui-tabs&gt;
</pre>

<div class="component-demo">
<link rel="import" href="bower_components/polymer-ui-tabs/polymer-ui-tabs.html">
<output>
  <polymer-ui-tabs selected="0">
    <span>Home</span>
    <span>About</span>
    <span>Contact</span>
  </polymer-ui-tabs>
</output>

</div>

<aside class="note">
  <section>
    <p>So this is the polymer-tabs element. To load it into your application you just import the polymer-ui-tabs.html file using an html import (point out we're doing that in the top right corner) and then the element is ready to use. No setup necessary!</p>
  </section>
</aside>

---

id: polymer-ui-collapsible-demo
title: Everything is an element
subtitle: Collapsible elements

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-collapsible.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;" data-lang="HTML">
&lt;polymer-ui-collapsible&gt;
  &lt;h3 class="polymer-ui-collapsible-header"&gt;Click Me!&lt;/h3&gt;
  &lt;div&gt;
    some content...
  &lt;/div&gt;
&lt;/polymer-ui-collapsible&gt;
</pre>

<div class="component-demo" style="height:100%">
<link rel="import" href="bower_components/polymer-ui-collapsible/polymer-ui-collapsible.html">
<output>
  <polymer-ui-collapsible>
    <h3 class="polymer-ui-collapsible-header" style="font-weight: bold;">Click Me!</h3>
    <p style="font-size: 18px; line-height: 1.4;">
      Realm of the galaxies at the edge of forever, made in the interiors of collapsing stars dispassionate extraterrestrial observer, rings of Uranus extraplanetary rich in heavy atoms shores of the cosmic ocean, white dwarf finite but unbounded!
    </p>
    <p style="font-size: 18px; line-height: 1.4;">
      Realm of the galaxies at the edge of forever, made in the interiors of collapsing stars dispassionate extraterrestrial observer, rings of Uranus extraplanetary rich in heavy atoms shores of the cosmic ocean, white dwarf finite but unbounded!
    </p>
  </polymer-ui-collapsible>
</output>

</div>

<aside class="note">
  <section>
    <p>Here's another example. This is polymer-ui-collapsible, which we can use to show and hide a bit of content. This is something I see people using jQuery for all the time. But with polymer-ui-collapsible there's no need to delve into JavaScript just to toggle a bit of content. Doing it in markup saves serious time!</p>
  </section>
</aside>

---

hidden: true
id: polymer-ui-toggle-button-demo
title: Everything is an element
subtitle: Toggle Button Element

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-toggle-button.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-ui-toggle-button offcaption="Nope"&gt;
&lt;/polymer-ui-toggle-button&gt;
</pre>

<div class="component-demo">
<link rel="import"
  href="bower_components/polymer-ui-toggle-button/polymer-ui-toggle-button.html">

<output style="zoom: 2.5;">
  <polymer-ui-toggle-button offcaption="Nope"></polymer-ui-toggle-button>
</output>

</div>

---

hidden: true
body_class: elements-fill
content_class: flexbox vcenter

<h2>You don't have to know about their internals</h2>

---

title: Polymer elements
subtitle: non-visual utility elements
content_class: columns-2

<span class="bold blue">Layout</span>

`<polymer-layout>`

`<polymer-flex-layout>`

`<polymer-grid-layout>`

<span class="bold blue">View</span>

`<polymer-media-query>`

`<polymer-page>`

<span class="bold blue">Services / libs</span>

`<polymer-shared-lib>`

`<polymer-google-jsapi>`

<span class="bold blue">Data</span>

`<polymer-localstorage>`

`<polymer-xhr>`

`<polymer-jsonp>`

`<polymer-file>`

`<polymer-meta>` 

<span class="bold blue">Behavior / interaction</span>

`<polymer-signals>`

`<polymer-selector>`

<aside class="note">
  <section>
    <p>When you start working with Web Components the mind naturally goes toward UI...</p>
    <p>But there are a lot of things we already do in markup that are non-visual</p>
    <p>So we've created elements for doing things like layout, ajax, localstorage and even working with the file system. It might sound weird to think of using an HTML tag to do AJAX, but when you actually start using it you'll realize it's an *awesome* way to work.</p>
  </section>
</aside>

---

id: polymer-flex-demo
title: Everything is an element
subtitle: flexbox...using DOM

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-flex-layout.html</span>">
</pre>

<pre class="prettyprint" style="font-size: 30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-flex-layout <b data-action="vertical">vertical</b> <b>iscontainer</b>>
  &lt;div>Header&lt;/div>
  &lt;div <b data-action="flex">flex</b>>Body&lt;/div>
  &lt;div>Footer&lt;/div>
&lt;/polymer-flex-layout>
</pre>


<div class="component-demo" style="height:100%">
<link rel="import" href="bower_components/polymer-flex-layout/polymer-flex-layout.html">
<output>
  <polymer-flex-layout vertical iscontainer title="Click me to add children">
    <div>Header</div>
    <div flex>Body</div>
    <div>Footer</div>
  </polymer-flex-layout>
</output>

</div>

<aside class="note">
  <section>
    <p>Here's an example: This is polymer-flex-layout, which contains all the functionality of CSS flexbox in an easy to use tag. Toggle the vertical attribute to lay children out horizontally. Toggle the flex attribute to make your child fill as much space as it can.</p>
    <p>This demonstrates an important point about Web Components and what you can do when you're able to extend the platform. It gives you the power to create your own things if you're not satisfied with the current implementation in the browser. Flexbox is too complicated so why not make it easier.</p>
  </section>
</aside>

---

hidden: true
id: polymer-ajax-demo
title: Everything is an element
subtitle: AJAX...using DOM

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-ajax.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;">
<b>&lt;polymer-ajax url="http://gdata.youtube.com/feeds/api/videos/"
              params='{"q":"chrome", "alt":"json"}'>
&lt;/polymer-ajax></b>
</pre>

<pre class="prettyprint" data-lang="JS" data-run-demo>
var ajax = document.querySelector('polymer-ajax');
ajax.addEventListener(<b>'polymer-response'</b>, function(e) {
  console.log(JSON.parse(<b>this.response</b>).feed.entry);
});
<b>ajax.go();</b>
</pre>

<div class="component-demo">
<link rel="import" href="bower_components/polymer-ajax/polymer-ajax.html">
<output><div>Hit run...</div></output>
</div>

<aside class="note">
  <section>
    <p>We have link tags and script tags which pull in external resources...</p>
    <p>Elements are composable</p>
  </section>
</aside>

---

hidden: true
content_class: flexbox vcenter

<h2>They're easy to add to your project</h2>

---

id: creating-elements
title: Creating <label class="core">elements</label>
subtitle: <a href="http://www.polymer-project.org/polymer.html" class="nounderline">polymer-project.org/polymer.html</a>
class: nobackdrop nobackground segue core polymer-diagram
#content_class: flexbox vcenter
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<aside class="note">
  <section>
    <p>We've talked a bit about using elements, now let's look at how you can create your own elements. Polymer is going to make this really easy for you!</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Declarative</em> element registration</h2>

<aside class="note">
  <section>
    <p>The declarative syntax that Polymer enables makes it super simple to start defining your own tags.</p>
  </section>
</aside>

---

id: declarative-registration
title: Declarative registration
#subtitle: Declarative registration

<pre class="corner prettyprint">
&lt;link rel="import" href="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="my-element" <b>noscript</b>&gt;
  &lt;template&gt;
    &lt;style&gt;h2 { color: orange; }&lt;/style&gt;
    &lt;h2&gt;Hello from my-element!&lt;/h2&gt;
  &lt;/template&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;my-element&gt;&lt;/my-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <my-element></my-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>Mention <b>noscript</b></p>
  </section>
</aside>

---

id: declarative-registration-proto
title: Declarative registration
#subtitle: Declarative registration with prototypes

<pre class="corner prettyprint">
&lt;link rel="import" href="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.html</span>">
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="hello-element"&gt;
  &lt;template&gt;
    &lt;h2&gt;I can say hello&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('hello-element', {
    sayHello: function() { alert('Howdy folks!'); }
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <hello-element></hello-element>
  </output>
</div>

<aside class="note">
  <section>
  <p>Lifecycle callbacks for when an element is created, added to the document, removed from the document or has an attribute changed.</p>
  <p>But what about when you want to actually visualize these properties</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Binding</em> expressions</h2>

<aside class="note">
  <section>
  <p>Data binding removes glue code</p>
  </section>
</aside>

---

id: two-way-binding
title: Binding Expressions

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;" data-lang="HTML">
&lt;polymer-element name="owner-element"&gt;
  &lt;template&gt;
    &lt;h2&gt;<b>{{owner}}</b> built me with Polymer&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('owner-element', {
    <b>owner: 'Rob'</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;" data-lang="HTML">
&lt;owner-element&gt;&lt;/owner-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <owner-element></owner-element>
  </output>
</div>

<aside class="note">
  <section>
  <p><b>Highlight owner</b></p>
  <p>Elements are configurable, so how do we let the user change the value of owner</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded"><em>Published</em> properties</h2>

---

id: published-properties
title: Published properties

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;polymer-element name="owner-element" <b>attributes="owner"</b>&gt;
  &lt;template&gt;
    &lt;h2&gt;<b>{{owner}}</b> built me with Polymer&lt;/h2&gt;
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('owner-element', {
    <b>owner: 'Rob'</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;owner-element <b>owner="Alex"</b>&gt;&lt;/owner-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px;">
    <owner-element owner="Alex"></owner-element>
  </output>
</div>

<aside class="note">
  <section>
  <p>We're creating a link between the publicly exposed attribute and the value in our prototype</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded">Declarative <em>event handlers</em></h2>

---

id: declarative-event-handlers
title: Declarative Event Handlers

<pre class="prettyprint" style="font-size:27px; line-height: 1.2;">
&lt;polymer-element name="click-element"&gt;
  &lt;template&gt;
    <b>&lt;button on-click="{{setMessage}}"&gt;Click me&lt;/button&gt;</b>
    <b>&lt;span&gt;{{message}}&lt;/span&gt;</b>
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('click-element', {
    <b>message: 'Waiting to be clicked...'</b>
    <b>setMessage: function() { this.message = 'I was clicked!' }</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px; zoom: 2;">
    <click-element></click-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>Explain why onclick is bad but on-click is awesome</p>
  </section>
</aside>

---

body_class: core-fill
content_class: flexbox vcenter

<h2 class="faded">Automatic <em>node finding</em></h2>

---

id: automatic-node-finding
title: Automatic Node Finding

<pre class="prettyprint" style="font-size:30px; line-height: 1.2;">
&lt;polymer-element name="focus-element"&gt;
  &lt;template&gt;
    <b>&lt;button on-click="{{setFocus}}"&gt;Set Focus&lt;/button&gt;</b>
    <b>&lt;input id="nameInput" type="text"&gt;</b>
  &lt;/template&gt;
  &lt;script&gt;
  Polymer('focus-element', {
    <b>setFocus: function() { this.$.nameInput.focus(); }</b>
  });
  &lt;/script&gt;
&lt;/polymer-element&gt;
</pre>

<div class="component-demo">
  <output style="display: block; padding: 10px; zoom: 2;">
    <focus-element></focus-element>
  </output>
</div>

<aside class="note">
  <section>
    <p>Explain why id's are bad but these are awesome</p>
  </section>
</aside>

---

hidden: true
title: Polymer features
subtitle: declarative web components

- Declarative element registration: `<polymer-element>`
- Declarative inheritance: `<polymer-element extends="...">`
- Declarative two-way data-binding: `<input id="input" value="{{foo}}">`
- Declarative event handlers: `<button on-click="{{handleClick}}">`
- Published properties: `xFoo.bar = 5 <-> <x-foo bar="5">`
- Property change watchers: `barChanged: function() {...}`
- Automatic node finding: `this.$.input.value = 5`
- PointerEvents / PointerGestures by default
- Support for Web Animations

<div class="build centered bold topmargin blue">
<span style="font-size:50px;">Be declarative. Write less code.</span>
</div>

<aside class="note">
  <section>
    <p>Registering your own element is kind of a wordy, verbose process</p>
    <p>You want to have a super button that inherits from your base button</p>
    <p>Two-way binding is awesome. You'll be amazed at how easy it is to build an entire application with nothing but binding</p>
    <p><b>We want to do things that make sense for developers</b></p>
  </section>
</aside>

---

hidden: true
id: more-complex-elements
title: Define an API
subtitle: complex elements require more juice...

<pre data-code-cycle class="prettyprint" data-lang="HTML" style="font-size:25px;line-height: 1.4;">
</pre>

<textarea selected>
<polymer-element name="my-input" noscript>
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
  <script>Polymer('my-input');</script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="text" id="in" style="color: orange;">
  </template>
  <script>
    Polymer('my-input', {
      get length() { return this.$.in.value.length; },
      ready: function() { ... }
    });
  </script>
</polymer-element>
</textarea>
<textarea>
&lt;polymer-element name="my-input">
  &lt;template>
    &lt;link rel="stylesheet" href="styles.css">
    &lt;input id="in" type="text">
  &lt;/template>
  &lt;script src="path/to/elements/myinput.js">&lt;/script>
&lt;/polymer-element>
</textarea>

- Properties/methods are added to `prototype`
- `this` refers to the element itself (e.g. `this.localName == "my-input"`)
- Can reference external scripts/stylesheets (e.g. CSP friendly)

<!-- <pre class="prettyprint" data-lang="HTML">
&lt;polymer-element name="my-input" constructor="MyInput">
  &lt;template>
    <b>&lt;link rel="stylesheet" href="styles.css"></b>
    &lt;input type="text">
  &lt;/template>
  <b>&lt;script src="path/to/elements/myinput.js">&lt;/script></b>
&lt;/polymer-element>
</pre> -->

---

hidden: true
id: published-properties
title: Publishing properties & data-binding
polymer_link: http://www.polymer-project.org/polymer.html#published-properties

2. **Inside** the element &rarr; use data-binding
2. **Outside** the element &rarr; users configure us using attributes

<pre data-code-cycle class="prettyprint" data-lang="HTML">
</pre>

<textarea selected>
<polymer-element name="my-input">
  <template>
    <input type="text" style="color: orange;">
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="{{type}}" style="color: {{color}};">
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input">
  <template>
    <input type="{{type}}" style="color: {{color}};" value="{{val}}">
    <polymer-localstorage name="myInputStorage" value="{{val}}"></polymer-localstorage>
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
</textarea>
<textarea>
<polymer-element name="my-input" attributes="type color">
  <template>
    <input type="{{type}}" style="color: {{color}};" value="{{val}}">
    <polymer-localstorage name="myInputStorage" value="{{val}}"></polymer-localstorage>
  </template>
  <script>
    Polymer('my-input', {
      type: 'text', 
      color: 'orange'
    });
  </script>
</polymer-element>
<my-input color="red"></my-input>
</textarea>

<!--
- User overrides `color` but `type` remains its default ("text")
- Since `val` isn't published, can't use it as a bindable attribute.
-->

---

hidden: true
title: Features in action
subtitle: responsive design...using DOM
#content_class: smaller 

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">platform.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-media-query.html</span>">
</pre>

<pre class="prettyprint" data-lang="html">
&lt;polymer-element name="responsive-layout" attributes="responsive">
  &lt;template>
    <b>&lt;polymer-media-query query="max-width:640px" queryMatches="{{isPhone}}">&lt;/...</b>
    &lt;template if="{{isPhone && responsive}}"> &lt;!-- Phone markup -->
      &lt;content>&lt;/content>
    &lt;/template>
    &lt;template if="{{!responsive}}"> &lt;!-- Non-responsive case -->
     ...
    &lt;/template>
  &lt;/template>
  &lt;script>Polymer('responsive-layout', {responsive: false});&lt;/script>
&lt;/polymer-element>
</pre>

<pre class="prettyprint" data-lang="User's HTML">
&lt;responsive-layout <b>responsive</b>>
  &lt;div>...&lt;/div>
&lt;/responsive-layout>
</pre>

---

id: the-platform
title: The <label class="platform">platform</label>
subtitle: <a href="http://www.polymer-project.org/docs/start/platform.html" class="nounderline">polymer-project.org/docs/start/platform</a>
class: nobackdrop nobackground segue platform polymer-diagram
#content_class: flexbox vcenter
keep_content: true

<div id="blocks-3d" class="in" style="top: 10%;">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

---

body_class: platform-fill
content_class: flexbox vleft

<h2 class="faded" style="font-size: 54px;">The platform is a <em>layer of polyfills</em> that adds support for emerging standards, like <em>Web Components</em>, to all <em>modern browsers</em>.</h2>

---

id: platform-polyfills
title: Platform polyfills
subtitle: supporting new web technologies today
class: nobackdrop nobackground browser-support

<div class="flexbox">
  <h2>Templates</h2>
  <div class="browser-support-row">
    <div class="supported"><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>HTML Imports</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported partial"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Custom Elements</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="flexbox">
  <h2>Shadow DOM</h2>
  <div class="browser-support-row">
    <div><img src="images/logos/browsers/safari_logo.png"></div>
    <div class="supported partial"><img src="images/logos/browsers/ff_logo.png"></div>
    <div class="supported"><img src="images/logos/chrome_logo.png"></div>
    <div class="supported"><img src="images/logos/browsers/opera_logo.png"></div>
    <div><img src="images/logos/browsers/ie10_logo.png"></div>
  </div>
</div>

<div class="build">
  <span id="polyfill-support-all"></span>
</div>

---

body_class: platform-fill
content_class: flexbox vleft

<h2 class="faded" style="font-size: 52px;">Additional features include <em>Mutation Observers</em>, <em>Pointer Events</em>, <em>Web Animations</em>, and much more.</h2>

---

id: evaporate-platform
class: polymer-diagram

<div id="blocks-3d">
  <img id="native-3d" class="block-3d" src="./images/polymer/diagram/native.svg">
  <img id="platform-3d" class="block-3d" src="./images/polymer/diagram/platform.svg">
  <img id="polymer-3d" class="block-3d" src="./images/polymer/diagram/polymer.svg">
  <img id="elements-3d" class="block-3d" src="./images/polymer/diagram/elements.svg">
</div>

<div class="diagram-explanations" style="margin-top: 250px;">
  <div class="diagram-explanation">
    <h3 style="font-size: 35px; line-height: 1.5;">As browsers implement the specifications supported by the platform, the need for this <br>layer <strong>decreases</strong>.</h3>
  </div>
  <div class="build">
    <div id="platform-shrink" class="diagram-explanation">
      <h3 style="font-size: 35px; line-height: 1.5;">...till eventually it's all <strong>gone</strong>.</h3>
    </div>
  </div>
</div>


---

id: polymerurl
class: nobackdrop nobackground yum do-transition
content_class: flexbox vcenter centered

<div class="build">
<h2><a href="http://polymer-project.org"><span class="elements">polymer</span><span class="hide">-</span><span class="core">project</span><span class="hide">.</span><span class="platform">org</span></a></h2>
</div>

---
