# Running protractor (or any selenium based project) on SNAP-CI

## The problem

The `chrome.conf.js` works (but not on Snap-CI) and matches documentation from [Selenimum](https://code.google.com/p/selenium/wiki/DesiredCapabilities) and [Protractor](https://github.com/angular/protractor/blob/master/docs/browser-setup.md). 

The `google-chrome.conf.js` uses the non-standard driver name that is on Snap-CI and only works on Snap-CI and isn't documented anywhere as far as I can tell or find.

## Testing it out

As documented on the [Protractor](http://angular.github.io/protractor/), this test was setup with the two different driver names. 

Before either test run:

1. `npm install -g protractor`
2. `webdriver-manager update`

Then run either one of the tests.

Standard driver name: `protractor chrome.conf.js`

Non-standard driver name: `protractor google-chrome.conf.js`
