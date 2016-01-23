# better-time-element<br>[![Build Status][travis-image]][travis-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Bower version][bower-image]][bower-url]
> Various `<time>` element extensions using [better-dom](https://github.com/chemerisuk/better-dom)

[LIVE DEMO](http://chemerisuk.github.io/better-time-element/)

## Features
* represent time in local format via `time[is=local-time]`
* [custom formats](#custom-formats) support via `data-format`
* [full i18n support](https://github.com/chemerisuk/better-i18n-plugin#multilingual-live-extensions) (if your language is missed - just translate strings from `i18n` folder and include a new file in your project)

## Installing
Use [bower](http://bower.io/) to download this extension with all required dependencies.

```sh
$ bower install better-time-element
```

This will clone the latest version of the __better-time-element__ into the `bower_components` directory at the root of your project.

Then append the following tags on your page:

```html
<script src="bower_components/better-dom/dist/better-dom.js"></script>
<script src="bower_components/better-time-element/dist/better-time-element.js"></script>
```

## Custom formats
Displayed date can be formatted using a `data-format` attribute on the element. For example:

```html
<time datetime="2016-01-23T11:12:58.089Z" is="local-time" data-format="EE, MMMM dd'th' yyyy"></time>
```

This will display the selected date like "Monday, December 8th 2014" on the input.

If `data-format` is not specified, date is formatted using the pattern "E, dd MMM yyyy".

Possible parameters for the format are:

|Letter |Date Component                                   |Presentation |Examples         |
|-------|-------------------------------------------------|-------------|-----------------|
|y      |Year                                             |Year         |2002; 02; 2      |
|M      |Month in year                                    |Month        |July; Jul; 07; 7 |
|w      |Week in year                                     |Number       |07; 7            |
|W      |Week in month                                    |Number       |2                |
|D      |Day in year                                      |Number       |009; 9           |
|d      |Day in month                                     |Number       |08; 8            |
|F      |Day of week in month (1st, 2nd, 3rd Tuesday)     |Number       |2                |
|E      |Day name in week                                 |Text         |Tuesday; Tu.     |
|u      |Day number of week (1 = Monday, ..., 7 = Sunday) |Number       |1                |

Number of letters in the parameter name specifies form of the output value, for instance:

```
"M" yields "1"
"MM" yields "01"
"MMM" yields "Jan"
"MMMM" yields "January"
```

## Browser support
#### Desktop
* Chrome
* Safari 6.0+
* Firefox 16+
* Opera 12.10+
* Internet Explorer 8+ (see [notes](https://github.com/chemerisuk/better-dom#notes-about-old-ies))

#### Mobile
* iOS Safari 6+
* Android 2.3+
* Chrome for Android

[travis-url]: http://travis-ci.org/chemerisuk/better-time-element
[travis-image]: http://img.shields.io/travis/chemerisuk/better-time-element/master.svg

[coveralls-url]: https://coveralls.io/r/chemerisuk/better-time-element
[coveralls-image]: http://img.shields.io/coveralls/chemerisuk/better-time-element/master.svg

[bower-url]: https://github.com/chemerisuk/better-time-element
[bower-image]: http://img.shields.io/bower/v/better-time-element.svg

