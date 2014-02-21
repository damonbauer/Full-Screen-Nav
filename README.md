# jQuery Full Screen Nav | [Demo](http://damonbauer.me/projects/jquery-fullscreennav/)
The intent of this plugin is to make a `<nav>` menu overlay the full screen & calculate a size for links on page load and window resize. There are a few options, [which are defined below](#options).

The plugin uses `rem` units, so it requires at least IE 9 by default.

- [Installation](#installation)
- [Options](#options)
- [How to Get Help](#help)
- [Contribution](#contribution)
- [Credits](#credits)
- [License](#license)

<a name="installation"></a>
## Installation
<a name="html"></a>
### Expected HTML
Include a way to open the navigation menu, like so:
```html
<a href="#" class="open-menu-btn">Menu</a>
```

You should markup your HTML with a basic `<nav>` list, like so:
```html
<nav>
    <ul>
      <li><a href="#">Link 1</a></li>
      ...
    </ul>
</nav>
```

<a name="css"></a>
### Necessary CSS
You’ll have to set the `<nav>` offscreen to begin with. In the demo, I do this by setting a position and pulling it offscreen:

```css
nav {
	position: absolute;
	top:-100%;
	width:100%;
	z-index:10;
}
```

The  "openClass" option defines what class is added when the menu is opened. By default, this is `.open`. You need to add some CSS to position the menu back onto the screen when this class is active:

```css
nav.open {
	top: 0;
}
```

Also, you’ll need to position the close button. I do this by applying the following CSS (using the same class as defined in the plugin options [default is “.close-menu-btn”]):

```css
a.close-menu-btn {
    position: absolute;
    top:10px; right:10px;
}
```

### Include the plugin
Somewhere after you load jQuery, load the plugin, like so:
```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script src="/path/to/jquery.fullscreennav.js"></script>
```

### Call the plugin (with any desired options)
Finally, call the plugin. Using default options:
```javascript
$("nav").fullScreenNav();
```

Calling the plugin with [options](#options):
```javascript
$("nav").fullScreenNav({
	"option": "optionValue",
	...
});
```

<a name="options"></a>
## Options
All options are defined below with their default values.<br /><br />
`baseFontSize: 16`<br />
**baseFontSize** *(int or string)*: Used to calculate `rem`. If this option is `"16"`, 1rem = 16px. [Read more about rems](http://techtime.getharvest.com/blog/in-defense-of-rem-units).

`closeMenuBtnText: "×"`<br />
**closeMenuBtnText** *(string)*: Text for the close button when the menu opens. Default is the multiplication symbol (&times;).

`closeMenuBtnClass: ".close-menu-btn"`<br />
**closeMenuBtnClass** *(string)*: Class to add to close menu button.

`fontSizeDivisor: 2.25`<br />
**fontSizeDivisor** *(int or string)*: "1" would make the font-size fill all available space. I found 2.25 to be visually appealing. The larger the number, the smaller the text will become.

`menuBtn: ".open-menu-btn"`<br />
**menuBtn** *(string)*: Selector that, when clicked, opens the menu. You need to supply this item in your HTML [(see Expected HTML)](#html).

`openClass: ".open"`<br />
**openClass** *(string)* Class to add to nav menu when opening. You need to supply this in your CSS to position the `<nav>` on screen [(see Necessary CSS)](#css).

<a name="help"></a>
## How to Get Help
I’m happy to help where I can. Feel free to contact me using the following:
- [Email](mailto:hello@damonbauer.me)
- [Twitter](http://twitter.com/damon_bauer)
- File an issue

<a name="contribution"></a>
## Contribution
If you have something to contribute (code improvement, new feature, bug fix), I’m all ears. Just submit a pull request. If it’s useful & doesn't add too much bloat, it should be no problem to bring that in.

Please note: this is my first jQuery plugin, so there are probably lots of areas to improve. I’m open to code suggestions!

<a name="credits"></a>
## Credits/inspiration
The concept for this navigation menu first came from [Huge Inc] (http://www.hugeinc.com), [Big Spaceship](http://www.bigspaceship.com/) and [Codrops](http://tympanus.net/codrops/2014/02/06/fullscreen-overlay-effects/). The plugin code was started from the [jQuery Boilerplate](http://jqueryboilerplate.com/).

<a name="credits"></a>
## License
Do whatever you want [(read more)](LICENSE.md). If I helped you in any way (using the plugin, learning something from the code, etc), I’d love to hear about it!

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/damonbauer/full-screen-nav/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/damonbauer/full-screen-nav/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

