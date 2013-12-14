#Less-Pushy

Less-Pushy is a responsive off-canvas navigation menu using CSS transforms & transitions.

It's an updated version of Pushy, converted to use LESS and separate out some of the presentation styles.

To see the original Pushy in action, [see the Demo](http://www.christopheryee.ca/pushy).

##Features

- All styling defined in [LESS](http://lesscss.org/)
- Uses CSS transforms & transitions.
- Smooth performance on mobile devices.
- jQuery animation fallback for IE 7 - 9.
- Menu closes when a link is selected.
- Menu closes when the site overlay is selected.
- It's responsive!

##Requirements

- jQuery 1.9+
- Modernizr

##Usage

1. Include jQuery & Modernizr.

2. Add the stylesheet (pushy.css or pushy.min.css) in your head and the JS (pushy.j or pushy.min.js) file in your footer.

3. Insert the following markup into your body.

```html
<!-- Pushy Menu -->
<nav class="sidebar pushy pushy-left">
    <ul>
        <li><a href="#">Item 1</a></li>
        <li><a href="#">Item 2</a></li>
    </ul>
</nav>

<!-- Site Overlay -->
<div class="site-overlay"></div>

<!-- Your Content -->
<div id="container"></div>
```

##Modernizr

Pushy uses Modernizr to detect & test for ```CSS 3D Transforms``` support in the browser. Be sure to include this test in you are using the [Modernizr build tool](http://modernizr.com/download/#-csstransforms3d-shiv-cssclasses-teststyles-testprop-testallprops-prefixes-domprefixes-load).


##Tips

- Use the ```.push``` CSS class on HTML elements outside of the ```#container```.

```html
<header class="push">
    <h1>This is a Heading</h1>
    <h2>This is a subheading</h2>
</header>

<!-- Your Content -->
<div id="container"></div>
```

- Add the following to hide horizontal scroll bars when menu is open, disable the webkit tap highlight and fix the focus scrolling in Safari.


```css
html, body{
	overflow-x: hidden; /* prevents horizontal scroll bars */
	-webkit-tap-highlight-color: rgba(0,0,0,0); /* disable webkit tap highlight */
	height: 100%; /* fixes focus scrolling in Safari (OS X) */
}
```

- To change the width of the ```.pushy``` menu, just change the @menu-open-width value at the top of pushy.less:

```less

@menu-open-width: 200px;

```

##Browser Compatibility

| Desktop       | Mobile                           |
| ------------- | -------------------------------- |
| IE 7-10       | Chrome (Android 4.2.2)           |
| Chrome        | Android Browser (Android 4.2.2)  |
| Firefox       | Safari (iOS 6-7)                 |
| Safari (Mac)  |

##Version History

### Less-Pushy

0.1

- Converted all styles over to [LESS](http://lesscss.org/)
- Turned all configurable magic numbers into variables.
- Moved all presentational styles out of pushy.less, into demo.less.
- Added ability to have part of the menu showing when closed.
- Started version numbering over again on rename.
- Moved demo.less colours into less variables.
- Added site header to demo use of .push class.
- Tidy and remove unnecessary styles and other stuff.

### Pushy

0.9.1

- Added support for more menu items (with scroll bar).
- Added the .push CSS class. This adds pushy support to additional HTML elements outside of the container div.
- Fixed menu transition.
- Tested in iOS 7.
- Updated the demo file.

0.9.0

- Added a site overlay when Pushy is toggled
- Fixed horizonal scroll bar issue on mobile devices
- Disabled webkit tap highlight
- Rejiggered the JS file
- Updated to jQuery 1.10.1
- Updated the demo file

0.8.4

- Fixed performance issue with mobile devices
- Updated to jQuery 1.10
- Updated the demo file
- Updated the read me

##Thanks to

- [HTML5 Boilerplate](http://html5boilerplate.com/)
- [jQuery](http://jquery.com/)
- [Modernizr](http://modernizr.com/)
