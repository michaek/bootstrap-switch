Bootstrap-switch v.1.9-dev
========================

You can now also use radio buttons and checkboxes as switches.


Demo
----
http://www.bootstrap-switch.org


Usage
-----
Just include Twitter Bootstrap, jQuery, Bootstrap Switch CSS and Javascript
``` html
<meta http-equiv="X-UA-Compatible" content="IE=9; IE=8;" />
<link rel="stylesheet" href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.2/css/bootstrap-combined.min.css">
<link rel="stylesheet" href="bootstrap-switch.css">

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script src="bootstrap-switch.js"></script>  // master
<script src="http://cdnjs.cloudflare.com/ajax/libs/bootstrap-switch/1.7/bootstrap-switch.min.js">  // from cdnjs.com
```

Less
----
If you want to use your bootstrap vars edit bootstrapSwitch.less and then compile the less file
``` bash
lessc static/less/bootstrap-switch.less static/stylesheets/bootstrap-switch.css
```

Supported browsers
------------------
I'm not going to support ancient browsers! (it works on IE8+)

Basic Example
-------------
checkboxes:

``` html
<div class="make-switch">
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch">
    <input type="radio">
</div>
```


Large, small or mini
--------------------
checkboxes:

``` html
<div class="make-switch switch-large">  <!-- switch-large, switch-small or switch-mini -->
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch switch-large">  <!-- switch-large, switch-small or switch-mini -->
    <input type="radio">
</div>
```


Colors
------
checkboxes:

``` html
<div class="make-switch" data-on="danger" data-off="warning">  <!-- primary, info, success, warning, danger and default -->
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch" data-on="danger" data-off="warning">  <!-- primary, info, success, warning, danger and default -->
    <input type="radio">
</div>
```


Animation
---------
checkboxes:

``` html
<div class="make-switch" data-animated="false">
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch" data-animated="false">
    <input type="radio">
</div>
```


Text
-----
checkboxes:

``` html
<div class="make-switch" data-on-label="SI" data-off-label="NO">
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch" data-on-label="SI" data-off-label="NO">
    <input type="radio">
</div>
```


Text Label
----------
checkboxes:

``` html
<div class="make-switch" data-text-label="My Slider Text">
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch" data-text-label="My Slider Text">
    <input type="radio">
</div>
```


HTML Text
----------
checkboxes:

``` html
<div class="make-switch" data-on-label="<i class='icon-ok icon-white'></i>" data-off-label="<i class='icon-remove'></i>">
    <input type="checkbox">
</div>
```

radioboxes:

``` html
<div class="make-switch" data-on-label="<i class='icon-ok icon-white'></i>" data-off-label="<i class='icon-remove'></i>">
    <input type="radio">
</div>
```


Initial values
--------------
checkboxes:

``` html
<div class="make-switch">
    <input type="checkbox" checked="checked" disabled="disabled">
</div>
```
radioboxes:


``` html
<div class="make-switch">
    <input type="radio" checked="checked" disabled="disabled">
</div>
```


Event handler
-------------
``` javascript
$('#mySwitch').on('switch-change', function (e, data) {
    var $el = $(data.el)
      , value = data.value;
    console.log(e, $el, value);
});
```

Methods
-------
``` javascript
$('#mySwitch').bootstrapSwitch('toggleActivation');
$('#mySwitch').bootstrapSwitch('isActive');
$('#mySwitch').bootstrapSwitch('setActive', false);
$('#mySwitch').bootstrapSwitch('setActive', true);
$('#mySwitch').bootstrapSwitch('toggleState');
$('.mySwitch').bootstrapSwitch('toggleRadioState'); // the radiobuttons need a class not a ID, don't allow uncheck radio switch
$('.mySwitch').bootstrapSwitch('toggleRadioStateAllowUncheck'); // don't allow uncheck radio switch
$('.mySwitch').bootstrapSwitch('toggleRadioStateAllowUncheck', false); // don't allow uncheck radio switch
$('.mySwitch').bootstrapSwitch('toggleRadioStateAllowUncheck', true); // allow uncheck radio switch
$('#mySwitch').bootstrapSwitch('setState', true);
$('#mySwitch').bootstrapSwitch('setState', true || false, true); // sets the state without getting the switch-change event
$('#mySwitch').bootstrapSwitch('setOnLabel', onValue); // sets the text of the "on" label
$('#mySwitch').bootstrapSwitch('setOffLabel', offValue); // sets the text of the "off" label
$('#mySwitch').bootstrapSwitch('setTextLabel', labelValue); // sets the text of the middle label
$('#mySwitch').bootstrapSwitch('setIconLabel', iconValue); // sets the icon of the middle label
$('#mySwitch').bootstrapSwitch('setOnClass', onClass); // sets the left color class
$('#mySwitch').bootstrapSwitch('setOffClass', offClass); // sets the right color class
$('#mySwitch').bootstrapSwitch('setAnimated', animated); // sets true or false for animation
$('#mySwitch').bootstrapSwitch('setSizeClass', size); // sets 'switch-mini', 'switch-small' or 'switch-large'
$('#mySwitch').bootstrapSwitch('status');  // returns true or false
$('#mySwitch').bootstrapSwitch('destroy');
```

## Compass Installation

Add this line to your application's Gemfile:

    gem 'bootstrap-switch'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install bootstrap-switch

In your compass.rb, you'll need 

    require 'bootstrap-switch'

Then you can put the following in your scss files:

    @import 'bootstrap-switch';

## Development

Installing [Grunt](http://gruntjs.com/) will make things a lot easier for you! Take a look at Gruntfile.js for all the tasks that are available.

Running `grunt sassify` will take the existing Less and generate new .scss files for Sass support.

Running `grunt test` will verify that the Less and Sass still generate the expected CSS.

When you're ready to bump the version, `grunt bump:patch` or `grunt bump:minor` will take care of updating files, committing and tagging for you.


License
-------
Licensed under the Apache License, Version 2.0
http://www.apache.org/licenses/LICENSE-2.0
