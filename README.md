# handlebars.jquery.js

 This [jQuery](http://jquery.com) Plugin lets you easily bind 
 [Handlebars.js](https://github.com/wycats/handlebars.js) templates to DOM
 elements.
 
 It's a simple and lean way to glue a model to a view.

## Features

  * write your Handlebars template just inside the DOM element
  * bind a model to the template
  * supports any kind of model that is compatible to jQuery's data() API
  * can render simple collections in combination with [collection.jquery.js](https://github.com/walski/collection.jquery.js) or compatible collections

## Installation

Just include jQuery, Handlebars and handlebars.jquery.js in your HTML Head:

<pre>
  &lt;!DOCTYPE html>

  &lt;html>
  &lt;head>
    &lt;script src="jquery-1.5.1.min.js" charset="utf-8">&lt;/script>
    &lt;script src="handlebars-0.9.0.pre.4.js" charset="utf-8">&lt;/script>
    &lt;script src="handlebars.jquery.js" charset="utf-8">&lt;/script>
  ...
</pre>

## Usage Examples

### Simple example

<pre>
  ...
  &lt;h1 data-title="It's a headline!">{{title}}&lt;/h1>
  ...
  &lt;script style="text/javascript">
    $('h1').template();
  &lt;/script>
  ...
</pre>

### Collections
<pre>
  ...
  &lt;ul>
    &lt;li>Some Fruit: {{name}}&lt;/li>
  &lt;/ul>
  ...
  &lt;script style="text/javascript">
    var banana = $({});
    banana.data('name', 'Banana');
    var apple = $({}); 
    apple.data('name', 'Green Apple');
    
    var fruits = $.collection(banana, apple);
    $('ul').template();
  &lt;/script>
  ...
</pre>

results in:

<pre>
  &lt;ul>
    &lt;li>Some Fruit: Banana&lt;/li>
    &lt;li>Some Fruit: Green Apple&lt;/li>
  &lt;/ul>
</pre>


See the *demo* folder for more examples.