# Welcome to Equinox! - last updated: July 2019

Equinox is Drupal 8 theme created to make your life as a themer easier. It is based on a few pretty cool ideas that some smart people have had -- [Inverted Triangle CSS (ITCSS)](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/), [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/), and [BEM](http://getbem.com/) (kinda -- you'll have to add a lot of that in yourself as you write your code). 


==================================================
## Structure
==================================================

Yeah it may look like a lot of directories but hear me out. 

### The Vendor Directory
### The Settings Directory
### The Tools Directory

This directory is a place for your mixins and functions to live. As of this writing, there are two mixins included: Respond-to and Transition. See the _mixins.scss partial for details. Respond-to is a really brilliant and wonderful mixin available for handling responsive styles. It is a mobile-first (ie it compiles as a `min-width` declaration) media query mixin. Please use it to keep things consistent. Custom breakpoints can be added/subtracted from the breakpoints map as needed but keeping your breakpoints to a minimum is good for your theme. Use respond-to to keep things clean and consistent. This layer does not output CSS.

### The Generic Directory

This is the first layer of YOUR code that outputs CSS. This directory is for reset styles and/or normalizing. As of this writing, this theme has included [normalize.css](https://github.com/necolas/normalize.css/). Additionally, there is a resets partial for site-wide and site-specific resets that you may need. A couple are already included that are regularly needed for Drupal theming. 

### The Atoms Directory

This directory is where you'll style the small elements of your site. This includes things like `p`, `a`, `h1`. It will also include site-specific elements, for instance if your site needs thumbnails for your blog post teasers, their styles can go here. Don't forget about individual form and list elements, and buttons too! 

### The Molecules Directory

This directory is where you'll style your medium-sized design components. Molecules are comprised of Atoms, but are not as complex as Organisms. A good example of a Molecule would be a form -- a text input + a dropdown select + a submit button. Styling for those individual pieces should go in Atoms! The styles for the `form` Molecule are specific to the grouping of these elements into a form. (In other words, your `form` styles found here will likely be more about the form's padding/margins, layout/placement and responsiveness vs its aesthetic.)

### The Organisms Directory

This directory is where you'll style your largest, most complex page elements. Organisms are groups of Molecules and come together to create full page layouts. A good example of an Organism would be the header comprised of a search form, social media icons, a menu, a logo. Also included is a Views partial for Views-specific styling. Paragraphs styles can be found in the Molecules Directory however, depending on the project, it may make more sense to move it to Organisms.

### The Utilities Directory

This directory is mainly for Helper class. This is the last layer of the inverted triangle and thus this code is meant to override previously defined styles. The hope is that with using this architecture, you will end up with a theme that is componentized, portable, flexible (ie not brittle), and shouldn't require (much) usage of the !important tag. See section on Parker down below.

==================================================
## Compiling
==================================================

This theme is currently meant to be compiled using [Prepros](https://prepros.io/). You will want to make sure the Autoprefixer option is turned ON. 


==================================================
## Notes
==================================================

### Syntax and keeping things clean

+ This theme is meant to follow Drupal's CSS coding standards found here: https://www.drupal.org/docs/develop/standards/css/css-formatting-guidelines.

+ Indentation should be 2 spaces!

+ There should be no empty spaces at ends of lines, no characters/spaces on empty lines.

+ Single line comments should use two forward slashes, a space, be capitalized at the start, and end with a period. (You will find some single line comments using the /**/ syntax instead, this was done deliberately to denote larger sections of text) 

+ Pseudo-element definitions (before, after) should use two colons. `::before`, `::after`

+ Pseudo-classes should use one colon `:focus`, `:hover` 


==================================================
## What's in The Future for Equinox?
==================================================

### Gulp

It wouldn't take much to set up Gulp to compile the SCSS in this theme. As of this writing however, the company this theme was built for is using Prepros for all our compiling needs thus this theme is not NPM-enabled. It could be useful in the future as we have included Bootstrap (grid-only) and Font Awesome.

### Parker

Enable Parker https://github.com/katiefenn/parker




### Libraries

Add FontAwesome Library -- attach it only to templates where it's needed?