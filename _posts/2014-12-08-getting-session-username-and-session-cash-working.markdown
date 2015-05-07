---
layout: post
title: "Getting session[:username] and session[:cash] working"
date: 2014-12-03 02:00:00 -0800
comments: true
categories: [Development, HTTP]
---
{% highlight ruby linenos %}
<p><%= session[:player_name] %>, you have $<%= session[:player_cash] %></p>
<p>How much do you want to bet?</p>
<form action='/make_bet' method='post'class="navbar-form pull-left">
  <p><input type="text" class="span3" name="player_bet"></p>
  <p><button type="submit" class="btn">Bet!</button></p>
</form>
{% endhighlight %}

I spent a lot of time trying to get params[:username] working in the .erb file in the view template after it was redirected. I thought params[] persisted throughout the session. It does not. It needs to be stored in session[].

{% highlight ruby linenos %}
post '/set_name' do
  new_player
  session[:player_name] = params[:player_name]
  redirect '/bet'
end
{% endhighlight %}
