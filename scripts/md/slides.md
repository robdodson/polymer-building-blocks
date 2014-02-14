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

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;tabs&gt;
  &lt;tab&gt;Tab 1&lt;/tab&gt;
  &lt;tab&gt;Tab 2&lt;/tab&gt;
  &lt;tab&gt;Tab 3&lt;/tab&gt;
&lt;/tabs&gt;
</pre>

---

id: tab-examples
title: Building a tab component on the web...

<div class="build flexbox vcenter centered">
<img src="images/screenshots/tabs/jquery.png">
<img src="images/screenshots/tabs/kendo.png">
<img src="images/screenshots/tabs/yui.png">
<img src="images/screenshots/tabs/angular.png">
<img src="images/screenshots/tabs/sencha.png">
<img src=""> <!-- intentional. holder to see all images together -->
</div>

---

body_class: readable
class: nobackdrop nobackground

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

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
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

---

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

---

content_class: flexbox vleft

<h2 style="margin-top: -100px; margin-bottom: 50px;">
  When I work with elements...
</h2>
<h3>Use components which are fast by default</h3>
<h3>Lower the barrier of entry for new developers</h3>
<h3>Reduce the amount of code I have to write</h3>

---

class: large
content_class: flexbox vcenter

<pre class="nohighlight">
&lt;tabs&gt;
  &lt;tab&gt;Tab 1&lt;/tab&gt;
  &lt;tab&gt;Tab 2&lt;/tab&gt;
  &lt;tab&gt;Tab 3&lt;/tab&gt;
&lt;/tabs&gt;
</pre>

---

class: nobackdrop nobackground yum
content_class: flexbox vcenter centered

<h2><img src="images/polymer/polymer-p.png" style="height:90px;box-shadow:none;margin-right:10px;">Polymer</h2><br>
<!-- <h3 class="auto-fadein"><a href="http://polymer-project.org">polymer-project.org</a></h3> -->

---

hidden: true
id: polymeroneliner
body_class: checkers
image: images/polymer/homepage_with_chrome.png
title: polymer-project.org
class: nobackdrop nobackground fill highlight

<div class="build">
  <div class="calloutbox"></div>
</div>

---

id: whatispolymer
body_class: whatispolymer
title: Soooo Polymer is...
class: nobackdrop nobackground fullviewport

<div class="build">
  <h3 class="platform">Polyfills?</h3>
  <h3 class="core">A framework?</h3>
  <h3 class="elements">UI widgets?</h3>
</div>

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

---

title: What is it?

<span class="pull-right auto-fadein"><img src="images/polymer/architecture-diagram.png" style="height:450px"></span>

<div class="build">
  <div>
    <div class="platform bold">Polyfill libraries</div>
    <br>
    <p>Shadow DOM, Custom Elements, HTML Imports, Pointer Events...</p>
  </div>
  <div class="topmargin">
    <div class="core bold">Sugaring layer</div>
    <br>
    <p>expresses opinionated way to use web component concepts together</p>
  </div>
  <div class="topmargin">
    <div class="elements bold">UI Components</div>
    <br>
    <p>comprehensive set (in progress)</p>
  </div>
</div>

---

hidden: true
class: platform nobackdrop nobackground
content_class: flexbox vcenter quote

<blockquote>Utilize the <b>modern</b> web platform.</blockquote>

---

hidden: true
class: large
content_class: flexbox vcenter centered

<h2 class="auto-fadein">1st-class support for spec features...</h2>

---

hidden: true
title: Lifecycle callbacks <label class="spec">Custom Elements</label>
body_class: platform-bg
polymer_link: http://www.polymer-project.org/polymer.html#lifecyclemethods

Support for the [lifecycle methods](http://www.polymer-project.org/polymer.html#lifecyclemethods)...but shorter names!

<pre class="prettyprint" data-lang="HTML">
Polymer('my-input', {
  ready: function() { ... }, // Polymer addition for when element is fully initialized.
  <b>created: function() { ... },</b>
  <b>enteredView: function() { ... },</b>
  <b>leftView: function() { ... },</b>
  <b>attributeChanged: function(attrName, oldVal, newVal) { ... }</b>
});
</pre>

Use cases:

- perform setup/teardown work
- notification when element is inserted/removed from page

---

hidden: true
id: insertion-point-api
title: Insertion points <label class="spec">Shadow DOM</label>
subtitle: define an internal structure
body_class: platform-bg

<pre class="prettyprint" data-lang="my-tabs.html">
&lt;polymer-element name="my-tabs" noscript>
  &lt;template>
    &lt;style>...&lt;/style>
    &lt;header>
      <b>&lt;content select="h2">&lt;/content></b>
    &lt;/header>
    <b>&lt;content select="section">&lt;/content></b>
  &lt;/template>
&lt;/polymer-element>
</pre>

<pre class="prettyprint" data-lang="html" data-run-demo="http://ebidel.github.io/polymer-experiments/polymer-and-angular/together/">
&lt;link rel="import" href="my-tabs.html">
<b>&lt;my-tabs></b>
  &lt;h2>Title&lt;/h2>
  &lt;section>content&lt;/section>
  &lt;h2>Title 2&lt;/h2>
  ...
<b>&lt;/my-tabs></b>
</pre>

<div class="build" style="position: absolute;bottom:20px;right:160px;">
<img src="images/screenshots/tabs.png" style="height: 300px;
width: auto;
box-shadow: 0 0 5px #999;">
</div>

---

hidden: true
title: Scoped styling <label class="spec">Shadow DOM</label>
body_class: platform-bg
polymer_link: http://www.polymer-project.org/articles/styling-elements.html

Support for styling features (scoped styles, `applyAuthorStyles`, etc.)

<pre class="prettyprint" data-lang="HTML">
&lt;polymer-element name="my-element">
  &lt;template>
    &lt;style>...&lt;/style> &lt;!-- Styles are scoped to the element -->
  &lt;/template>
  &lt;script>
    Polymer('my-element', {
      <b>applyAuthorStyles: true,</b>
      <b>resetStyleInheritance: false</b>
    });
  &lt;/script>
&lt;/polymer-element>
</pre>

- Polymer attempts to polyfill most Shadow DOM style features

---

hidden: true
title: Bundle &amp; deliver CSS/HTML/JS <label class="spec">HTML Imports</label>
body_class: platform-bg

Reuse others' components:

<pre class="prettyprint" data-lang="awesome-menu.html">
<b>&lt;link rel="import" href="x-toolbar.html">
&lt;link rel="import" href="menu-item.html"></b>

&lt;polymer-element name="awesome-menu">
  &lt;template>
    <b>&lt;x-toolbar responsive>
      &lt;menu-item src="images/do.png" selected>Do&lt;/menu-item>
      &lt;menu-item src="images/re.png">Re&lt;/menu-item>
      &lt;menu-item src="images/mi.png">Mi&lt;/menu-item>
    &lt;x-toolbar></b>
  &lt;/template>
  ...
&lt;/polymer-element>
</pre>

<pre class="prettyprint" data-lang="User's page">
&lt;link rel="import" href="awesome-menu.html">
&lt;awesome-menu>&lt;/awesome-menu>
</pre>

---

class: nobackdrop nobackground
content_class: flexbox vcenter quote

<blockquote class="large">Everything is an element.</blockquote>

---

title: Using <label class="elements">elements <i class="icon-puzzle-piece elements"></i></label>
subtitle: <a href="http://www.polymer-project.org/docs/elements/" class="nounderline">polymer-project.org/docs/elements/</a>
class: nobackdrop nobackground segue elements
#content_class: flexbox vcenter
keep_content: true

<div class="overlay top"></div>
<div class="overlay bottom"></div>

---

id: polymer-ui-elements
title: Polymer UI elements
subtitle: visual elements
body_class: elements-bg

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

`<polymer-ui-card>` [demo](http://www.polymer-project.org/polymer-all/polymer-ui-elements/polymer-ui-card/index.html)

`<polymer-ui-sidebar-menu>` [demo](http://www.polymer-project.org/polymer-all/polymer-ui-elements/polymer-ui-sidebar-menu/index.html)

`<polymer-ui-tabs>` [demo](http://www.polymer-project.org/polymer-all/polymer-ui-elements/polymer-ui-tabs/index.html)

`<polymer-ui-toggle-button>` [demo](http://www.polymer-project.org/polymer-all/polymer-ui-elements/polymer-ui-toggle-button/index.html)

`<polymer-ui-theme-aware>`

---

id: polymer-ui-tabs-demo
title: Everything is an element
subtitle: Tabs revisited
body_class: elements-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-ui-elements" data-tooltip="bower install polymer-ui-elements">polymer-ui-tabs.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;" data-lang="HTML">
&lt;polymer-ui-tabs selected="0"&gt;
  &lt;span&gt;Home&lt;/span&gt;
  &lt;span&gt;About&lt;/span&gt;
  &lt;span&gt;Contact&lt;/span&gt;
&lt;/polymer-ui-tabs&gt;
</pre>

<div class="component-demo" style="height:100%">
<link rel="import" href="bower_components/polymer-ui-tabs/polymer-ui-tabs.html">
<output>
  <polymer-ui-tabs selected="0">
    <span>Home</span>
    <span>About</span>
    <span>Contact</span>
  </polymer-ui-tabs>
</output>

</div>

---

title: Polymer elements
subtitle: non-visual utility elements
body_class: elements-bg
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

---

id: polymer-flex-demo
title: Everything is an element
subtitle: flexbox...using DOM
body_class: elements-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-flex-layout.html</span>">
</pre>

<pre class="prettyprint" data-lang="HTML">
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

---

id: polymer-ajax-demo
title: Everything is an element
subtitle: AJAX...using DOM
body_class: elements-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-ajax.html</span>">
</pre>

<pre class="prettyprint" style="font-size:25px;">
<b>&lt;polymer-ajax url="http://gdata.youtube.com/feeds/api/videos/"
              params='{"alt":"json"}'>&lt;/polymer-ajax></b>
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

---

hidden: true
title: Real-world examples of polymer-ajax
class: nobackdrop
content_class: flexbox vcenter centered
body_class: elements-bg

<h2 style="margin-top:-100px;"><a href="http://www.chromestatus.com/features">chromestatus.com/features</a></h2>

<h2 style="margin-top:50px;"><a href="http://www.polymer-project.org/build/">polymer-project.org/build/</a></h2>


---

hidden: true
id: polymer-file-demo
title: Everything is an element
subtitle: read files...using DOM
body_class: elements-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-file.html</span>">
</pre>

<pre class="prettyprint centered" style="font-size:25px;">
&lt;polymer-file <b data-tooltip="'dataurl', 'arraybuffer', 'binarystring', 'text'">readas</b><b>="dataurl"</b>>&lt;/polymer-file>
</pre>

<pre class="prettyprint" data-lang="JS" data-run-demo>
var pFile = document.querySelector('polymer-file');

pFile.addEventListener(<b>'polymer-result'</b>, function(e) {
  console.log(<b>this.result</b>);
});

<b>pFile.blob = new Blob(['abc'], {type: 'text/plain'});</b> // Set the file to read

<b>pFile.read();</b>
</pre>

<div class="component-demo">
<!-- <link rel="import" href="bower_components/polymer-file/polymer-file.html"> -->
<output><div>Hit run...</div></output>
</div>

---

title: Creating <label class="core">elements <i class="icon-beaker core"></i></label>
subtitle: <a href="http://www.polymer-project.org/polymer.html" class="nounderline">polymer-project.org/polymer.html</a>
class: nobackdrop nobackground segue core
#content_class: flexbox vcenter
keep_content: true

<div class="overlay top"></div>
<div class="overlay bottom"></div>

---

title: Polymer features
subtitle: declarative web components
body_class: core-bg
build_lists: true

- Declarative element registration: `<polymer-element>`
- Declarative inheritance: `<polymer-element extends="...">`
- Declarative two-way data-binding: `<input id="input" value="{{foo}}">`
- Declarative event handlers: `<button on-click="{{handleClick}}">`
- Published properties: `xFoo.bar = 5 <-> <x-foo bar="5">`
- Property change watchers: `barChanged: function() {...}`
- Automatic node finding: `this.$.input.value = 5`
- PointerEvents / PointerGestures by default

<div class="build centered bold topmargin blue">
<span style="font-size:50px;">Be declarative. Write less code.</span>
</div>

---

hidden: true
title: Default attributes
body_class: core-bg
polymer_link: http://www.polymer-project.org/polymer.html#defaultattrs

User-defined attributes are included on each instance of the element:

<pre class="prettyprint" data-lang="HTML">
&lt;polymer-element name="my-input" <b>customattr</b> <b>class="active"</b>>
  &lt;template>...&lt;/template>
&lt;/polymer-element>

&lt;my-input>&lt;/my-input>
</pre>

Instances include your attributes: 

<pre class="prettyprint centered" style="font-size:25px">
  &lt;my-input customattr class="active">&lt;/my-input>
</pre>

---

id: more-complex-elements
title: Define an API
subtitle: complex elements require more juice...
body_class: core-bg

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

id: published-properties
title: Publishing properties & data-binding
body_class: core-bg
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
title: Expressions
body_class: core-bg
polymer_link: http://www.polymer-project.org/docs/polymer/expressions.html

Expressions can go anywhere `{{}}` live:

    <div>Jill has {{ daughter.children.length + son.children.length }} grandchildren</div>

Conditional attributes:

    <input type="checkbox" checked?="{{activate}}">

Dynamic classes:

    <div class="{{ {active: user.selected, big: user.type == 'super'} | tokenList }}"> 
    <!-- <div class="active big"> -->

---

hidden: true
title: Dynamic markup
subtitle: additional magic for HTML <code>&lt;template></code>
body_class: core-bg
polymer_link: http://www.polymer-project.org/platform/template.html

Conditionals:

    <template if="{{ isActive }}">
      <!-- shown if isActive property is true -->
    </template>

    <template if="{{ showDefault || users.length < 10 }}">
      ...
    </template>

Iteration:

    <template repeat="{{ user in users }}">
      <template repeat="{{ file in user.files }}">
        {{ user.name }} owners {{ file.name }}
      </template>
    </template>

---

hidden: true
title: Features in action 
subtitle: data-binding / published properties
body_class: core-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-ajax.html</span>">
</pre>

<pre class="prettyprint" data-lang="html">
&lt;polymer-element name="youtube-videos" attributes="query">
  &lt;template>
    &lt;polymer-ajax url="http://gdata.youtube.com/feeds/api/videos/" params="<b>{{params}}</b>"
                  <b>handleAs="json"</b> <b>response="{{response}}"</b> <b>auto</b>>&lt;/polymer-ajax>
    &lt;ul>
      <b>&lt;template repeat="{{entry in response.feed.entry}}">
        &lt;li>{{entry.title.$t}}&lt;/li>
     &lt;/template></b>
    &lt;/ul>
  &lt;/template>
  &lt;script>
    Polymer('youtube-videos', {
      ready: function() { <b>this.params = {alt: 'json', q: this.query};</b> }
    });
  &lt;/script>
&lt;/polymer-element>
</pre>

<pre>
&lt;youtube-videos query="cats">&lt;/youtube-videos>
</pre>

---

title: Features in action
subtitle: responsive design...using DOM
body_class: core-bg
#content_class: smaller 

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
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

hidden: true
title: Features in action
subtitle: $ referencing / changed watchers / declarative events
body_class: core-bg

<pre class="corner prettyprint">
&lt;script src="<span alt="bower install polymer" data-tooltip="bower install polymer">polymer.min.js</span>">&lt;/script>
&lt;link rel="import" href="<span alt="bower install polymer-elements" data-tooltip="bower install polymer-elements">polymer-file.html</span>">
</pre>

<pre class="prettyprint" data-lang="html">
&lt;polymer-element name="read-me" <b>on-click="{{onClick}}"</b>>
  &lt;template>
    &lt;polymer-file <b>id="file"</b> readas="arraybuffer" <b>result="{{result}}"</b>>&lt;/polymer-file>
  &lt;/template>
  &lt;script>
    Polymer('read-me', {
      <b>resultChanged: function() {</b>
       console.log(this.result);
      <b>},</b>
      <b>onClick: function(e, detail, sender) {
       this.$.file.read();
     }</b>
    });
  &lt;/script>
&lt;/polymer-element>
</pre>

<pre class="prettyprint" data-lang="User's JS">
var el = document.createElement('read-me');
<b>el.blob = new Blob(['abc'], {type: 'text/plain'});</b>
</pre>

---

hidden: true
title: FOUC prevention
body_class: core-bg

Initially hide elements using `polymer-veiled` class or manage a list in JS:

1. Add `polymer-veiled` class:

        <x-foo class="polymer-veiled">If you see me, elements are upgraded!</x-foo>
        <div class="polymer-veiled"></div>

2. `Polymer.veiledElements = ['x-foo', 'div'];`

- - - -

- `polymer-unveiled` swapped in at `WebComponentsReady` event &rarr; elements fade-in.
- **Note:** `polymer-veiled` is added to `<body>` by default.

---

title: Polymer <label class="platform">platform <i class="icon-cogs platform"></i></label>
class: nobackdrop nobackground segue platform
#content_class: flexbox vcenter
keep_content: true

<div class="overlay top"></div>
<div class="overlay bottom"></div>

---

id: polymerurl
class: nobackdrop nobackground yum do-transition
content_class: flexbox vcenter centered

<div class="build">
<h2><a href="http://polymer-project.org"><span class="elements">polymer</span><span class="hide">-</span><span class="core">project</span><span class="hide">.</span><span class="platform">org</span></a></h2>
</div>

---
