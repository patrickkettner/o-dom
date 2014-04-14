# o-dom [![Build Status](https://travis-ci.org/Financial-Times/o-dom.png?branch=master)](https://travis-ci.org/Financial-Times/o-dom)

Origami DOM manipulation &amp; traversal helpers.


## Functions

### getClosestMatch

Get the first element that matches the selector by testing the element itself and traversing up through its ancestors in the DOM tree.

__Arguments__

* `el` < DOMElement > The DOM element to start from.
* `selector` < String > The CSS selector to match.


Example:

```javascript
var dom = require('o-dom');
var closestListItem = dom.getClosestMatch(document.querySelector('li a'), 'li');
```

## Development

This module is suitable for helper functions that provide a convenient means of performing commonly required generic manipulation or selection of DOM elements.  It should not be extended to contain:

* Selector functions where `querySelector` would suffice
* Anything event related
* Polyfills (use browserFeatures in origami.json for that)
* Anything that is has a good chance of being specific to a single component use case
