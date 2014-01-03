# touch-input-nav

> Scopes touch-web tabbed input navigation to input elements inside the same form

![touch-input-nav](http://i.imgur.com/adaP4uB.gif)

*Video made using [SimFinger](https://github.com/atebits/SimFinger)*

## Installation

### Zip

Download a [zip](https://github.com/ChrisWren/touch-input-nav/archive/master.zip) which includes both minfied and un-minified versions.

### bower

```bash
bower install touch-input-nav
```

### browserify

```bash
npm install --save-dev touch-input-nav
```

## Usage

*Note that this module is dependent on jQuery.*

This module will add a global listener for the `focus` event on all input, select, and textarea elements and then when the focus event occurs, it will disable all other input elements that are not inside the focused-element's parent `form` element. It applies a class on the disabled elements so that they appear enabled in case they are visible within the viewport. A user can still click on these `disabled` elements, just not tab to them as they are not a part of a form-flow.

```js
    touchInputNav();
});
```

### touchInputNav([className])

#### className
Type: `string`

A class to allow for custom styling of the disabled state. This can be used to override how the disabled state is presented for form input elements outside of the current form scope.

## Current Browsers supported

- iOS Safari/Chrome

*Note: all other browsers will have no input field disabling applied.*