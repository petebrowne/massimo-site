---
title: Getting Started
---
Massimo is a static website builder that allows you to use dynamic technologies
such as Haml & Sass for rapid&nbsp;development.

*Massimo's code is inspired by other website generators like [Jekyll](http://github.com/mojombo/jekyll) and [Webby](http://webby.rubyforge.org/).*


Features
--------

* Renders templates and views using [Tilt](http://github.com/rtomayko/tilt)
* Uses familiar helper methods from [Padrino::Helpers](http://github.com/padrino/padrino-framework)
* Supports custom helper methods like [Rails](http://rubyonrails.org/) and [Sinatra](http://www.sinatrarb.com/)
* Concats javascripts using [Sprockets](http://getsprockets.org/)
  and then compresses them using whichever library you want
* Renders stylesheets using either [Sass](http://sass-lang.com/) or [Less](http://lesscss.org/)
* Automatically creates pretty URLs


Installation
------------

    gem install massimo


Getting Started
---------------
    
    massimo generate my-site
    cd my-site
    massimo build
    