# o-dom [![Build Status](https://travis-ci.org/Financial-Times/o-dom.png?branch=master)](https://travis-ci.org/Financial-Times/o-dom)

Origami DOM manipulation &amp; traversal helpers.


## Functions

### getClosestMatch

Get the first element that matches the selector by testing the element itself and traversing up through its ancestors in the DOM tree.

__Arguments__

* `el` < DOMElement > The DOM element to start from.
* `selector` < String > The CSS selector to match.

__Returns__

< DOMElement > or `false`

Example:

```javascript
var dom = require('o-dom');
var closestListItem = dom.getClosestMatch(document.querySelector('li a'), 'li');
```

### getIndex

Get the index of an element.

__Arguments__

* `el` < DOMElement > The DOM element whose index to get.

__Returns__

< Number >

Example, assuming this HTML structure:

```html
<ul>
	<li></li>
	<li id="target"></li>
	<li></li>
</ul>
```

`dom.getIndex(document.getElementById('target'));` would return 1.

## Development

This module is suitable for helper functions that provide a convenient means of performing commonly required generic manipulation or selection of DOM elements.  It should not be extended to contain:

* Selector functions where `querySelector` would suffice
* Anything event related
* Polyfills (use browserFeatures in origami.json for that)
* Anything that is has a good chance of being specific to a single component use case

----

## Licence

This software is published by the Financial Times under the [MIT licence](http://opensource.org/licenses/MIT).
