---
layout: post
title: "Project has one Project Manager..."
date: 2015-01-27 05:53:09 -0800
comments: true
categories: [Ruby on Rails, ActiveRecord]
---

from [ActiveRecord::Associations::ClassMethods](http://api.rubyonrails.org/classes/ActiveRecord/Associations/ClassMethods.html)

{% highlight ruby linenos %}
class Project < ActiveRecord::Base
  belongs_to              :portfolio
  has_one                 :project_manager
  has_many                :milestones
  has_and_belongs_to_many :categories
end
{% endhighlight %}

> The project class now has the following methods (and more) to ease the traversal and manipulation of its relationships:

`Project#portfolio`  
`Project#portfolio=(portfolio)`  
`Project#portfolio.nil?`

`Project#project_manager`  
`Project#project_manager=(project_manager)`  
`Project#project_manager.nil?`

`Project#milestones.empty?`  
`Project#milestones.size`  
`Project#milestones`  
`Project#milestones<<(milestone)`  
`Project#milestones.delete(milestone)`  
`Project#milestones.destroy(milestone)`  
`Project#milestones.find(milestone_id)`  
`Project#milestones.build`  
`Project#milestones.create`

`Project#categories.empty?`   
`Project#categories.size`  
`Project#categories`  
`Project#categories<<(category1)`  
`Project#categories.delete(category1)`  
`Project#categories.destroy(category1)`




