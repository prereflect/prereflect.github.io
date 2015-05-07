---
layout: post
title: "An Incredibly Brief Introduction to Relational Databases"
date: 2015-01-07 06:39:26 -0800
comments: true
categories: [Tealeaf Academy, Schema, SQL]
---

This from  the first reading assignment for the class. 
[An Incredibly Brief Introduction to Relational Databases](http://archive.oreilly.com/pub/a/ruby/excerpts/ruby-learning-rails/intro-ruby-relational-db.html) from Appendix B - [Learning Rails](http://shop.oreilly.com/product/9780596518783.do)  

##Keys

The *primary key* is a unique identifier for a row in a table.  
A *foreign key* is a *primary key* from a table stored in another table to allow  access the data.

##Data Types

Rails supports these data types in tables

{% highlight ruby %}
:binary
:boolean
:date
:datetime
:decimal
:float
:integer
:primary_key
:references
:string
:text
:time
:timestamp
{% endhighlight %}

And with PostgreSQL you can also use these

{% highlight ruby %}
:hstore
:json
:array
:cidr_address
:ip_address
:mac_address
{% endhighlight %}

##Connecting Tables

A *foreign key* is a *primary key* from another table stored to allow a table to access the data.  
*Student_id* is a *foreign key* in the *Award* table.  
*award_id* is a *foreign key* in the *presenter* table.  

![Connected Tables](http://cdn.oreilly.com/excerpts/9780596518776/figs/web/rail_ab04.png "Connected Tables")

##Many-to-Many Connections

Using a table to join two tables to allow many-to-many connections.  
Classic example is students and their courses.  

![Many-to-Many](http://cdn.oreilly.com/excerpts/9780596518776/figs/web/rail_ab05.png "Many-to-Many Connections")

##Database Normalization

from [Wikipedia](http://en.wikipedia.org/wiki/Database_normalization)

- Free the database of modification anomalies
- Minimize redesign when extending the database structure
- Avoid bias towards any particular pattern of querying

