# touch-input-nav

> Scopes touch-web tabbed input navigation to input elements inside the same form

[![NPM version](https://badge.fury.io/js/touch-input-nav.png)](http://badge.fury.io/js/touch-input-nav) [![Travis Status](https://travis-ci.org/ChrisWren/touch-input-nav.png)](https://travis-ci.org/ChrisWren/touch-input-nav) <a href="https://saucelabs.com/u/cthewrenopen">
  <img src="https://saucelabs.com/buildstatus/cthewrenopen" alt="Selenium Test Status" />
</a>

![toutch-input-nav](http://i.imgur.com/B55z1Zy.gif)

*Video made using [SimFinger](https://github.com/atebits/SimFinger)*

## Why use this plugin?

By default, mobile browsers allow users to "tab" or navigate between input fields regardless of which form they belong to. The problem is if you have multiple input fields on your mobile website/webapp which are not related, the user will be able to navigate between these unrelated fields. The goal of this tool is to only provide input navigation to related input fields by disabling navigation between unrelated fields.

## Installation

### Zip

Download a zip of the [latest release](https://github.com/ChrisWren/touch-input-nav/releases/latest) which includes both minfied and un-minified versions.

### bower

```bash
bower install touch-input-nav
```

### browserify

```bash
npm install --save-dev touch-input-nav
```

## Usage

*Note: this module is dependent on jQuery.*

This module will add a global listener for the `focus` event on all input, select, and textarea elements and then when a focus event occurs, it will disable all other input elements that are not inside the focused element's parent `form` element. It applies a class on the disabled elements so that they appear enabled in case they are visible within the viewport. A user can still tap on these `disabled` elements, just not tab to them as they are not a part of the same form.

```js
// no module loader
window.touchInputNav();

// requirejs
define(['touch-input-nav'], function (touchInputNav) {
  touchInputNav();
});

// browserify
require('touch-input-nav')();
```

### touchInputNav([className])

#### className
Type: `string`

A class to allow for custom styling of the disabled state. This can be used to override how the disabled state is presented for form input elements outside of the current form scope.

## Targeted mobile browsers which have tabbed input navigation
- iOS Safari/Chrome

*Note: all other browsers will have no input field disabling applied.*

# Changelog

 - **0.0.1** - Made jquery a proper dependency for browserify, used proper require.js module definition syntax.
 - **0.0.0** - Initial release.
