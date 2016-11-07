`base.html` represents the absolute minimum that you should include in your base template.


## Usage

```
curl http://basehtml.xyz > base.html
```


## Rationale

[HTML Boilerplate][html5-bp] is the gold standard of HTML base templates but over the years has become (a little) bloated.

We don't need to force decisions about JS / CSS layout in our base template, you're an adult - you can make those mistakes yourself.
It should no longer be considered best practice to always include [JQuery][jquery] (or really any third party JS / CSS).
Plus, and this is awesome, if you're using a [modern SSL configuration][ssl-config] you no longer have to worry about IE 10 compatibility.

This `base.html` project aims to be as minimal and un-opinionated as possible, including _only_ things that would be considered best practice for 99% of web projects.


## Browser Support

100%! No, but really, there's nothing in the `base.html` that will break in any (relatively modern) browser.
What's not included is code that specifically adds support for older browsers.
That means there's no CSS reset, [`normalize.css`][normalize] or [`modernizr.js`][modernizr] - so if you want to support old version of IE you'll have to include those yourself.

If you want to use HTML5-style markup (`<section>`, `<article>`, `<nav>`, etc.) and still support IE9 you'll need to include something like [`html5shiv`][html5shiv].


## What about...

#### ...setting a favicon?

Just include `favicon.ico` in the root of your site as recommended by Audrey R's amazingly detailed [favicon-cheat-sheet][favicon-cheat-sheet].

#### ...including a css reset?

Sure. Use whichever one you want! You just have to include it yourself.

#### ...Google Analytics?

There's a bunch of analytics options out there and Google provides one of them.
Our aim is to not be opinionated so you'll need to include your own analytics package.


## Contributing

Before committing please make sure that any changes pass `htmlhint` (with the default settings).


## Resources

- Josh Buchea's excellent [HEAD][head] project
- [HTML5 Boilerplate][html5-bp]


  [head]: http://gethead.info/
  [html5-bp]: https://github.com/h5bp/html5-boilerplate
  [jquery]: https://jquery.com
  [ssl-config]: https://mozilla.github.io/server-side-tls/ssl-config-generator/
  [normalize]: https://necolas.github.io/normalize.css/
  [modernizr]: https://modernizr.com/
  [favicon-cheat-sheet]: https://github.com/audreyr/favicon-cheat-sheet
  [html5shiv]: https://github.com/aFarkas/html5shiv
