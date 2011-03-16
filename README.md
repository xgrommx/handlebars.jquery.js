# handlebars.jquery.js

 This [jQuery](http://jquery.com) Plugin lets you easily bind 
 [Handlebars.js](https://github.com/wycats/handlebars.js) templates to DOM
 elements.
 
 It's a simple and lean way to glue a model to a view.

## Features

  * write your Handlebars template just inside the DOM element
  * bind a model to the template
  * supports any kind of model that is compatible to jQuery's data() API

## Installation

Just include jQuery, Handlebars and handlebars.jquery.js in your HTML Head:

  <!DOCTYPE html>

  <html>
  <head>
    <script src="jquery-1.5.1.min.js" charset="utf-8"></script>
    <script src="handlebars-0.9.0.pre.4.js" charset="utf-8"></script>
    <script src="handlebars.jquery.js" charset="utf-8"></script>
  ...

## Usage Examples

Simple example:

  ...
  <h1 data-title="It's a headline!">{{title}}</h1>
  ...
  <script style="text/javascript">
    $('h1').template();
  </script>
  ...

See the *demo* folder for more examples.