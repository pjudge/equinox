# Welcome to Equinox! - last updated: September 13, 2019

Equinox is a Drupal 8 base theme meant to provide very basic styles and basic page layout for your new Drupal project. It is meant to be used as a base from which to extend [the sub-theme Solstice](https://github.com/IQ-Solutions/solstice). 


## Dependencies

This theme alone has no dependencies.

This theme, when extended by Solstice, requires that the [Component Libraries](https://www.drupal.org/project/components) module be installed and enabled.  


## Usage

From within your Drupal project root (or whatever directory your `composer.json` file lives in), run `composer require iq/equinox` to install in `themes/custom`. Use alone or, ideally, [download Solstice](https://github.com/IQ-Solutions/solstice) as your sub-theme and do all your theming in there in a componentized environment.

These are the regions that Equinox ships with:
* Top Bar 
* Header
* Primary Menu
* Breadcrumb
* Above Content
* Sidebar Left
* Content
* Sidebar Right
* Footer

Equinox also ships with some basic block configuration (see `config/install`) to ensure you're starting with blocks in sensible regions. 

## What's in The Future for Equinox?

_TODO_

