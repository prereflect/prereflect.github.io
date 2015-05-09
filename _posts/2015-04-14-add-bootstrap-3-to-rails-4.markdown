---
layout: post
title: "Add Bootstrap 3 to Rails 4"
date: "2015-04-14 14:34:06 -0700"
---

In this post I will go through the process to add
 [Bootstrap 3](http://getbootstrap.com/)
to a [Rails](http://rubyonrails.org/) 4 web app.

First add two gems to your `/Gemfile`

[bootstrap-sass](https://github.com/twbs/bootstrap-sass) and
[autoprefixer-rails](https://github.com/ai/autoprefixer-rails)

{% highlight ruby linenos %}
gem 'bootstrap-sass' '~> 3.3.4'
gem 'autoprefixer-rails'
{% endhighlight %}

autoprefixer-rails adds vendor prefixes to the CSS.

Run `bundle install` to bring the gems into your app.

Add `//= require bootstrap-sprockets` on the line above
 `//= require_tree .` in your `/app/assets/javascripts/application.js` file.

{% highlight javascript linenos %}
...

// Read Sprockets README (https://github.com/rails/sprockets#sprockets-directives) for details
// about supported directives.
//
//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require bootstrap-sprockets
//= require_tree .
{% endhighlight %}

Delete everything in your `app/assets/stylesheets/application.css` and place
 these two lines.

{% highlight ruby linenos %}
@import 'bootstrap-sprockets'
@import 'bootstrap'
{% endhighlight %}

Rename your `app/assets/stylesheets/application.css` stylesheet to
`application.css.sass` to be able to use [Sass](http://sass-lang.com/).

That's it, you're ready to go!
