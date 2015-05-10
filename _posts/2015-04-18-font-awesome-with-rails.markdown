---
layout: post
title: "Font Awesome with Rails and Sass"
date: "2015-04-18 16:42:40 -0700"
---

[Font Awesome](http://fontawesome.io/) is a great way to bring icons into your
Rails project. Font Awesome icons are scalable vector graphics in a font package
 that enable you to use CSS to change the appearance of the icons.

These instructions will show how to install Font Awesome for use with the [Sass]
(http://sass-lang.com/) CSS extension language. Yes, There is a gem for that!

<h2>Add the Gem</h2>

Add [font-awesome-sass](https://github.com/FortAwesome/font-awesome-sass] to
 your `Gemfile`.

{% highlight ruby linenos %}
...
gem 'bootstrap-sass', '~> 3.2.0'
gem 'autoprefixer-rails'

gem 'font-awesome-sass'
{% endhighlight %}

Run `bundle install`

<h2>Import into Your Stylesheet</h2>

Import the Font Awesome styles in your `app/assets/stylesheets/application.css.scss`

{% highlight css linenos %}

@import "font-awesome-sprockets";
@import "font-awesome";

{% endhighlight %}

<h2>Rails Helpers</h2>

The gem `font-awesome-sass` also gives you a
 [Rails Helper](http://mixandgo.com/blog/the-beginner-s-guide-to-rails-helpers).

In your view to can put the helper

`icon('flag', ' ', class: 'big-red')`

In your `application.css.scss` file you can put the class.

{% highlight css linenos %}
.big-red {
  color: rgb(255, 0, 0);
  font-size: 5em;
}
{% endhighlight %}

![font awesome css example](/assets/images/big-red.png)



