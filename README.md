# General

## API design

* consistent naming
* defaulting and invalid input handling
* thinking of all possible paths (users will try use it in an unexpected way)
* let it be extensible
* freeze input when passed by reference
* [Details](http://coding.smashingmagazine.com/2012/10/09/designing-javascript-apis-usability/)

# Javascript in browser

## CSS animations/transitions

[Write animations/transitions in CSS](http://coding.smashingmagazine.com/2012/11/19/building-relationship-between-css-javascript/) and manage interaction by adding/removing classes in javascript. Detect browser support with Modernizr and provide a fallback using jQuery.

# Design

## Baseline

[Align baselines](http://coding.smashingmagazine.com/2012/12/17/css-baseline-the-good-the-bad-and-the-ugly/) within adjacent columns: set `line-height` and `margin + padding` to a multiple of the smallest text size in the page for each and very element. [Tool](https://github.com/jkeyes/baseline) to visually check.