# General

## API design

* [consistent naming](http://coding.smashingmagazine.com/2012/10/09/designing-javascript-apis-usability/#consistency)
* [defaulting and invalid input handling](http://coding.smashingmagazine.com/2012/10/09/designing-javascript-apis-usability/#handling-arguments)
* [let it be extensible](http://coding.smashingmagazine.com/2012/10/09/designing-javascript-apis-usability/#extensibility)
* [freeze input](http://coding.smashingmagazine.com/2012/10/09/designing-javascript-apis-usability/#the-reference-horror) when passed by reference
* thinking about all possible (even the ones not expected at first) combinations

## Configuration

[Environment variables](http://www.12factor.net/config) without grouping under `dev`, `qa`. References to backing services should preferably be made of [URLs](http://www.12factor.net/backing-services).

## Process model

[Share-nothing processes](http://www.12factor.net/concurrency) without sticky sessions to allow horizontal scalability. Restart on failure and daemonization handled by environment. Once started, the process listens to a port given in configuration so it can be referred by a URL and multiple can be spawned on the same physical machine.

# Javascript in browser

## Feature sniffing

Test for individual feature presence (like `if (el.classList) { /* */ }`), do not assume that having (or missing) one feature will mean having (or missing) any other, even if currently the combination does not exist.

## CSS animations/transitions

[Write animations/transitions in CSS](http://coding.smashingmagazine.com/2012/11/19/building-relationship-between-css-javascript/) and manage interaction by adding/removing classes in javascript. Detect browser support with Modernizr and provide a fallback using jQuery.

# Design

## Black and white

[Never use](http://ianstormtaylor.com/design-tip-never-use-black/), prefer light and dark greys.

## Baseline

[Align baselines](http://coding.smashingmagazine.com/2012/12/17/css-baseline-the-good-the-bad-and-the-ugly/) within adjacent columns: set `line-height` and `margin + padding` to a multiple of the smallest text size in the page for each and very element. [Tool](https://github.com/jkeyes/baseline) to visually check.