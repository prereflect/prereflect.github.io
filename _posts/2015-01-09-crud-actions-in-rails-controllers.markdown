---
layout: post
title: "CRUD actions in Rails Controllers"
date: 2015-01-09 02:48:19 -0800
comments: true
categories: [CRUD, Ruby on Rails, Controllers, Ruby] 
---
> A frequent practice is to place the standard CRUD actions in each controller in the following order: index, show, new, edit, create, update and destroy. You may use any order you choose, but keep in mind that these are public methods; as mentioned earlier in this guide, they must be placed before any private or protected method in the controller in order to work.

{% highlight ruby linenos %}
class ThisIsAController < ApplicationController
  def index
  end

  def show
  end

  def new
  end

  def edit
  end

  def create
  end

  def update
  end

  def destroy
  end
end
{% endhighlight %}
from [Getting Started with Rails](http://guides.rubyonrails.org/getting_started.html#showing-articles)

